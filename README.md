# ConstructorWordGuess
 (https://github.com/nikitamehata23/ConstructorWordGuess)
## Table of contents
  * [About this project](#about-this-project)
  * [Getting started](#contribute)
    * [Clone the repository](#clone-repository)
    * [Install the dependencies](#dependencies)
  * [Starting the game](#start-game)
  * [Playing the game](#play-game)
  * [Technologies used to create app](#technologies-used)

## <a name="about-this-project"></a> About this project
This project is a command line version of the classic WordGuess constructor. This game uses similar logic browser based wordguessing game created, but with this game, I created a command line version using Javascript constructor functions to create letter and word objects, the inquirer npm package to prompt users to guess a letter, and Node.js to run the Javascript code from the command line. For more information on how this project was constructed and put together, see [Structure of the project](#structure-of-project).

## Starting the game
  1. [Install the dependencies](#dependencies)

#### <a name="structure-of-project"></a> Structure of the project
<p>After you clone the repository, navigate to the project root directory (constructor-hangman). The project directory structure is set up as follows:</p>
<ul>
  <li> 
  	<p><b>Letter.js</b>: Contains a constructor, Letter. This constructor displays an underlying character or a blank placeholder             (underscore), depending on whether or not the user has guessed the letter. This constructor includes:</p>
  	<ul>
  		<li>A string value to store the underlying character for the letter.</li>
  		<li>A boolean value that stores whether that letter has been guessed yet by the user.</li>
  		<li>A function that returns the underlying character if the letter has been guessed, or a placeholder (underscore) if the letter has not been guessed.</li>
  		<li>A function that takes a character as an argument and checks it against the underlying character, updating the stored boolean value to true if it was guessed correctly</li>
  	</ul>
  </li>
  <li>
  	<p><b>Word.js</b>: Contains a constructor, Word that depends on the Letter constructor. This is used to create an object representing the current word the user is attempting to guess. The constructor includes:</p>
  	<ul>
  		<li>An array of new Letter objects representing the letters of the underlying word.</li>
  		<li>A function that returns a string representing the word. This calls the function on each letter object (defined in Letter.js) that displays the character or an underscore and concatenates those together.</li>
  		<li>A function that takes a character as an argument and calls the guess function on each letter object (defined in Letter.js).</li>
  	</ul>
  </li>
  <li>
  	<p><b>index.js</b>: The file containing the logic for the course of the game, which depends on Word.js and:</p>
  	<ul>
  		<li>Randomly selects a word and uses the Word constructor to store it.</li>
  		<li>Prompts the user for each guess and keeps track of the user's remaining guesses.</li>
  	</ul>
  </li>
  <li><b>package.json</b>: Lists the project dependencies (third party npm packages) and their version numbers.</li>
  <li><b>.gitignore</b>: Any file or directory listed inside this file will not be tracked by GitHub when code is committed.</li>
  <li><b>package-lock.json</b>: Dependency tree for the project. Lists all the dependencies and their versions.</li>
</ul>

### <a name="dependencies"></a> Install the dependencies
<p>The following npm packages are dependencies to the project. You must install these packages in the project root directory (constructor-hangman) to be able to play Hangman from the command line.</p>
<p>After you clone the repository to a local directory, change directory to the project root directory (constructor-hangman) and run the following command to install the required npm packages:</p>
<pre>npm install</pre>
<ul>
	<li>inquirer npm package (https://www.npmjs.com/package/twitter) - used to prompt users for a letter throughout the game.</li>
	<li>cli-color npm package (https://www.npmjs.com/package/cli-color) - used to add color to the game.</li>
  	<li>figlet npm package (https://www.npmjs.com/package/figlet) - used to convert text into ASCII art - drawings made out of text characters.</li>
  	<li>is-letter npm package (https://www.npmjs.com/package/is-letter) - used for form valiation. This package is used to check if the value the user enters is a letter (for example, "a") or not a letter (for example, "aba").</li>
  	<li>boxen npm package (https://www.npmjs.com/package/boxen) - used to create boxes in terminal.</li>
</ul>
<p>Version information for each of these packages is available in the package.json file in the project root directory.</p>


## <a name="start-game"></a> Starting the game
<p>To start the game, run the following command from the project root directory (constructor-hangman):</p>
<pre>node index.js</pre>
<p>When you run this command, you will see the following screen:</p>
<pre>
$ node index.js



![Screenshot (36)](https://user-images.githubusercontent.com/50224446/60312051-66d85400-991f-11e9-8ab6-ff93b8afc96d.png)



![Screenshot (37)](https://user-images.githubusercontent.com/50224446/60312056-6b047180-991f-11e9-8b2f-707052a2c32c.png)
![Screenshot (38)](https://user-images.githubusercontent.com/50224446/60312063-722b7f80-991f-11e9-9f82-b0b4d9ad725b.png)
![Screenshot (39)](https://user-images.githubusercontent.com/50224446/60312065-75267000-991f-11e9-8ba6-0429413fc1c3.png)

![Screenshot (40)](https://user-images.githubusercontent.com/50224446/60312067-76f03380-991f-11e9-935e-1bb566390118.png)
![Screenshot (41)](https://user-images.githubusercontent.com/50224446/60312071-79eb2400-991f-11e9-8dd9-6ea4e70c9f6d.png)
![Screenshot (42)](https://user-images.githubusercontent.com/50224446/60312076-7e174180-991f-11e9-9aed-18bba1a77f6c.png)
![Screenshot (43)](https://user-images.githubusercontent.com/50224446/60312079-80799b80-991f-11e9-86eb-a65f456ec538.png)

![Screenshot (45)](https://user-images.githubusercontent.com/50224446/60312084-84a5b900-991f-11e9-9ccf-584d5a6b65a2.png)




![Screenshot (36)](https://user-images.githubusercontent.com/50224446/60312051-66d85400-991f-11e9-8ab6-ff93b8afc96d.png)



![Screenshot (37)](https://user-images.githubusercontent.com/50224446/60312056-6b047180-991f-11e9-8b2f-707052a2c32c.png)
![Screenshot (38)](https://user-images.githubusercontent.com/50224446/60312063-722b7f80-991f-11e9-9f82-b0b4d9ad725b.png)
![Screenshot (39)](https://user-images.githubusercontent.com/50224446/60312065-75267000-991f-11e9-8ba6-0429413fc1c3.png)

![Screenshot (40)](https://user-images.githubusercontent.com/50224446/60312067-76f03380-991f-11e9-935e-1bb566390118.png)
![Screenshot (41)](https://user-images.githubusercontent.com/50224446/60312071-79eb2400-991f-11e9-8dd9-6ea4e70c9f6d.png)
![Screenshot (42)](https://user-images.githubusercontent.com/50224446/60312076-7e174180-991f-11e9-9aed-18bba1a77f6c.png)
![Screenshot (43)](https://user-images.githubusercontent.com/50224446/60312079-80799b80-991f-11e9-86eb-a65f456ec538.png)

![Screenshot (44)](https://user-images.githubusercontent.com/50224446/60312083-82dbf580-991f-11e9-846d-69a9de42c657.png)

![Screenshot (45)](https://user-images.githubusercontent.com/50224446/60312084-84a5b900-991f-11e9-9ccf-584d5a6b65a2.png)

## <a name="technologies-used"></a> Technologies used to build app
 * Node.js (https://nodejs.org/en/)
  * Javascript constructor functions

