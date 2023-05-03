Download Link: https://assignmentchef.com/product/solved-cpsc2150-homework-4
<br>
For this assignment we will continue to work on our Tic-Tac-Toe game, but we will not be adding any new functionality to our program. We will be creating automated test cases for our IGameBoard interface and implementations using JUnit. You do not need to create test cases for the GameScreen class.

<h1>Requirements</h1>

You will create two Junit test classes, one for each implementation of the IGameBoard interface. These classes should be name TestGameBoard and TestGameBoardMem. The test cases can be exactly the same in each class, you will just need to change the implementation used. If you create a private helper method to call the constructor like we did in the lab (The Factory Method Pattern), this will be an easy change to make.

You must test the following methods in each Junit test class. Each test case should have it’s own JUnit test function.

Test the following methods:

<h2>Constructor</h2>

–       Create 3 distinct test cases for the constructor

<h3>CheckSpace</h3>

<ul>

 <li>Create 3 distinct test cases for CheckSpace CheckHorizontalWin</li>

 <li>Create 4 distinct test cases</li>

</ul>

CheckVerticalWin

<ul>

 <li>Create 4 distinct test cases</li>

</ul>

<h3>CheckDiagonalWin</h3>

<ul>

 <li>Create 7 distinct test cases</li>

 <li>Note, the different diagonals are distinct</li>

</ul>

CheckForDraw

<ul>

 <li>Create 4 distinct test cases</li>

</ul>

<h3>WhatsAtPos</h3>

<ul>

 <li>Create 5 distinct test cases isPlayerAtPos</li>

 <li>Create 5 distinct test cases</li>

</ul>

<h3>PlaceMarker</h3>

–      Create 5 distinct test cases

Your JUnit test code must also use the Factory Method Design Pattern by having a private method that calls the constructor for your IGameBoard object and returns it. By always using the Factory Method, you will be able to complete the Junit code for TestGameBoard, then copy and paste the code and change only this helper method and the file name to create TestGameBoardMem.

You will also need an additional private helper method that will take in a 2D array of characters and return a string representation of that array. This string representation should exactly match what the toString method returns from our GameBoard classes. This will allow you to create an “expected” version of the GameBoard in a 2D array, then get the string version to compare to the actual output of your GameBoard. So your process for comparing your expected GameBoard and your actual GameBoard will look like this:

<ol>

 <li>Create an empty “expected” 2D array</li>

 <li>Call the factory method to create your empty IGameBoard object “gb”</li>

 <li>Foreach token you need to place for your test case

  <ol>

   <li>Use placeMarker to place it on your IGameBoard object “gb”</li>

   <li>Place that same character in the same location in your 2D array “expected”</li>

  </ol></li>

 <li>Call your helper method to create the expected string version of your 2D array</li>

 <li>Call assertEquals to ensure your expected string and gb.toString() are equivalent</li>

</ol>

<h1>The Program Report</h1>

Along with your code you must submit a well formatted report with the following parts:

<h2>Requirements Analysis</h2>

Fully analyze the requirements of this program. Express all functional requirements as user stories. Remember to list all non-functional requirements of the program as well. Creating test cases is not a functional or non-functional requirement, so these should be the same as previous assignments.

<h2>Design</h2>

Create a UML class diagram for each class and interface in the program. Also create UML Activity diagrams for every method in your GameScreen class and every method in your GameBoard or GameBoardMem class (except the constructor). If a method is defined as a default method in the interface, you need to update it to remove any mention of the 2D array or other private data of the GameBoard class, and instead refer to primary methods. If a method is provided as a default method in the interface you only need to provide an Activity Diagram for the default method, you do not need to include the Activity for each implementation as well.

You do not need to create diagrams for your Test classes that you will make for this assignment, so these diagrams are the same from the previous assignment.

<h2>Testing</h2>

In your report include a description for each test case which includes your input values, your expected output, and a reason for why you chose this test case and what makes it distinct. Remember that the current state of the GameBoard is part of the input and part of the output. This can be a bulleted list or a table.

<h2>Deployment</h2>

Provide instructions about how your program can be compiled and run. Since you are required to submit a makefile with your code, this should be pretty simple. Your makefile should include targets to compile your program (default), run your program (run) compile your test cases (test) and run your test cases (make testGB and make testGBmem). Your makefile must work on the school unix machines. Your classpath for Junit may be different on your personal machine. Make sure you are using Junit 4. Your makefile is more important when it comes to testing (hard to run test cases won’t ever be used), so it is worth more points for this assignment.

<h1>Additional Requirements and Tips</h1>

<ul>

 <li>You must include a makefile with your program. We should be able to run and test your program by unzipping your directory and using the make, make run, make test, make testGB and make testGBmem</li>

 <li>Your makefile must work on the school unix Your classpath for Junit may be different on your personal machine. Make sure you are using Junit 4.</li>

 <li>If you discover any failures with your test cases, you will need to find the underlying fault and correct it.</li>

 <li>Your UML Diagrams must be made electronically. I recommend the freely available program draw.io, but if you have another diagramming tool your prefer feel free to use that.</li>

 <li>Hard coded values are acceptable (and necessary) for our input and expected output values in our Junit code</li>

 <li>You will need to call several methods in order to set up your test case. That is fine, as long as your Assert statements are only testing one method. Remember if you run your test cases and you have failed test cases for whatsAtPos and checkDiagonalWin, you want to fix whatsAtPos first, as that method is called in checkDiagonalWin.</li>

 <li>You do not need to follow the entire process in your main function to test your IGameBoard class, because our input is hard coded and always follows our preconditions. This means o You aren’t asking the user for input o You aren’t validating input o You don’t need to call checkSpace before placing tokens since they are hard coded and we know the column is free

  <ul>

   <li>You don’t need to call checkForWinner after every token placement</li>

   <li>You aren’t printing anything to the screen o You don’t need to follow the turn order when placing tokens.</li>

  </ul></li>

 <li>Remember test cases should be distinct in a meaningful way. The difference between checking for a win with the exact same board, but swapping X’s and O’s is not distinct, as IGameBoard doesn’t actually care what the character is. Two test cases are distinct if there is a reasonable expectation as to why one test case could pass while the other could fail.</li>

 <li>You do not need to use any specific method (such as path testing) to identify test cases.</li>

 <li>Remember to think about what was challenging for you when you were writing code. What mistakes did you make in earlier attempts? Those would be good scenarios to test for.</li>

 <li>Make sure you are using JUnit 4, not the JUnit 3 shortcut on the school unix</li>

 <li>The JUnit code for the test cases will be very similar for each method. Make sure you get one example working, then copy and paste to change the input values and expected output values.</li>

 <li>Remember to follow the best practices we discussed for JUnit test cases. They are different than the best practices for our normal production code.</li>

 <li>You may need to use several assert statements to check to see if everything worked correctly by checking the string representation, the return value of the method, the getter methods, and so on.</li>

 <li>While writing JUnit code is not necessarily difficult, it is time consuming. Thinking of all the test cases and fixing any faults you find will also take some time. Avoid the temptation to put this assignment of because it’s “just” writing test cases.</li>

 <li>You should not create test cases that violate the preconditions for the method being tested.</li>

</ul>