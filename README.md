Download Link: https://assignmentchef.com/product/solved-comp1020-lab4-a-randomarray-class
<br>
<ul>

 <li>Multidimensional arrays</li>

</ul>

Notes:

<ul>

 <li>Make sure your TA has recorded your mark before leaving.</li>

 <li>The three exercises are independent – you can do them in any order.</li>

 <li>Only one of the three exercises is required. The Gold exercise is not much more difficult than the Silver exercise this time (some students may actually find it easier).</li>

</ul>




<ol>

 <li>Download the file <strong>java</strong> and save it as <strong>RandomArray.java</strong> before using it. The supplied <strong>TestLab4Bronze.java</strong> program will expect it to be named this way.</li>

 <li>This class creates rectangular two-dimensional arrays filled with random positive integer values. Some of the class is written for you. Complete it by adding code in the four places marked <strong>//***ADD YOUR CODE HERE***</strong>.

  <ol>

   <li>Add a private instance variable that will hold a 2-dimensional array of integers.</li>

   <li>Complete the constructor, which will create the 2-dimensional array, with the specified number of rows and columns, containing values from <strong>0</strong> to <strong>range-1</strong>. The code to generate such random numbers is supplied in the comments.</li>

   <li>Complete the <strong>getRow</strong> method, which will return a copy (clone or deep copy) of the specified row of the array, as an array of integers of the correct length. In this method, use the built-in <strong>arraycopy</strong> method to copy the values from the original array into the result, as demonstrated in class.</li>

   <li>Complete the <strong>getCol</strong> method, which will return a copy (clone or deep copy) of the specified column of the array, as an array of integers of the correct length. In this method, you will have to copy the values yourself using a <strong>for</strong> loop since the <strong>arraycopy</strong> method cannot be used in this situation.</li>

  </ol></li>

 <li>Run the supplied <strong>java</strong> program to test your class. Sample output from this program is shown below. User input is in blue. Your numbers will be different.</li>

</ol>

<strong>How many rows? </strong><strong>3</strong>

<strong>How many columns? </strong><strong>4</strong>

<strong>The rows contain: </strong>

<strong>Row 0: [15, 92, 48, 87] </strong>

<strong>Row 1: [74, 32, 24, 10] </strong>

<strong>Row 2: [55, 0, 50, 14] </strong>

<strong> </strong>

<strong>The columns contain: </strong>

<strong>Column 0: [15, 74, 55] Column 1: [92, 32, 0] </strong>

<strong>Column 2: [48, 24, 50] </strong>

<strong>Column 3: [87, 10, 14] </strong>

<ol>

 <li>Download the file <strong>java</strong> and save it as <strong>MagicSquare.java</strong> before using it. The supplied <strong>TestLab4Silver.java</strong> program will expect it to be named this way.</li>

 <li>This class creates a square two-dimensional array which is a “magic square”. A magic square of “order n” is a square with n rows and n columns that contains each of the numbers from 1 to n<sup>2</sup>. The sum of every row, every column, and the two diagonals, must be the same. For example, an order 5 magic square is shown below. Every row, column, and diagonal adds up to the same thing (65). Such squares are very old, with early examples dating back to 2200BC.</li>

</ol>

11  24   7  20   3

17   5  13  21   9

23   6  19   2  15

4  12  25   8  16

10  18   1  14  22

<ol start="3">

 <li>Some of the class is written for you. Complete it by adding code in the three places marked</li>

</ol>

<strong>//***YOUR CODE HERE***</strong>.

<ol>

 <li>Add a private instance variable that will hold the magic square as a 2-dimensional array of integers.</li>

 <li>Complete the constructor, which will create a magic square with a given size (n), which must be an <em>odd number</em>. (You don’t have to check.) To do this, use a very old technique called “de la Loubere’s algorithm” (note that this will give a different square from the one shown above):</li>

 <li>Place the numbers in the square in order, from 1 to n<sup>2</sup>, starting with the 1 in the centre of the bottom row. ii. If the number you just placed is divisible by n, then the next one goes immediately above it.

  <ul>

   <li>If the number you just placed is <em>not</em> divisible by n, then the next one goes diagonally down and to the right.</li>

  </ul></li>

</ol>

<ol>

 <li>Both the rows and the columns are cyclic. If you go off the top of the square, reenter at the bottom. If you go off the bottom of the square, re-enter at the top. Do the same for the columns. <strong>Hint</strong>: This can easily be accomplished using the mod operator (%).</li>

 <li>See the sample output below for examples of squares constructed this way.</li>

</ol>

<ol>

 <li>Complete the <strong>toString</strong> method, which will return the proper <strong>String</strong> to use to print the magic square. It should contain tabs (<strong><sub>t</sub></strong>) between the columns and newlines (<strong><sub>
</sub></strong>) between the rows.</li>

</ol>




<ol start="4">

 <li>Run the supplied <strong>java</strong> program to test your class. Sample output from this program is shown below. User input is in blue.</li>

</ol>

<strong>Enter a small odd number, or 0 to quit:</strong><strong>3</strong>

<strong> </strong>

<strong>The magic square is: </strong>

<strong>4     9      2       </strong>

<strong>3     5      7       </strong>

<strong>8     1      6       </strong>

<strong> </strong>

<strong>Enter a small odd number, or 0 to quit:</strong><strong>7</strong>

<strong> </strong>

<strong>The magic square is: </strong>

<strong>22    31     40     49     2      11     20      </strong>

<strong>21    23     32     41     43     3      12      </strong>

<strong>13    15     24     33     42     44     4       </strong>

<strong>5     14     16     25     34     36     45      </strong>

<strong>46    6      8      17     26     35     37      </strong>

<strong>38    47     7      9      18     27     29      </strong>

<strong>30    39     48     1      10     19     28      </strong>

<strong> </strong>

<strong>Enter a small odd number, or 0 to quit:</strong><strong>0</strong><strong> That was fun. Bye!</strong><strong>  </strong>




<ol>

 <li>Download the file <strong>java</strong> and save it as <strong>CrosswordGrid.java</strong> before using it. The supplied <strong>TestLab4Gold.java</strong> program will expect it to be named this way.</li>

 <li>This class creates and displays a blank crossword puzzle grid. All that’s missing are the clues. A crossword puzzle grid consists of a rectangular (usually square) array of squares. Some squares are black, some are white, and some of the white ones have numbers in the corner. An integer array will be used to represent this, as follows:

  <ol>

   <li>Black squares will be represented by -1.</li>

   <li>White squares with no number in them will be represented by 0.</li>

   <li>White squares that contain a number will be represented by that number.</li>

  </ol></li>

</ol>

A file will be provided that will specify the size of the puzzle, and the pattern of black and white squares. It will contain the number of rows (r), the number of columns (c), and then r*c values which will be only -1 (black) or 0 (white). For example, the file might contain

<strong> 4  4 </strong>

<strong>-1  0  0 -1 </strong>

<strong> 0  0  0  0 </strong>

<strong> 0  0  0  0 </strong>

<strong>-1  0  0 -1 </strong>

Your mission, should you choose to accept it, is to read in this file, create the array containing the -1s and 0s, and then add the clue numbers in the appropriate squares (as described below). This will require about 20 lines of Java code in total.




<ol start="3">

 <li>A large amount of code is supplied for you, including all of the file handling and the graphical output. Complete it by adding code in two places marked <strong>//***ADD YOUR CODE HERE***</strong>.

  <ol>

   <li>Complete the constructor. A <strong>Scanner</strong> object has been set up for you that will allow you to read data from a text file chosen by the user using a standard dialog box. (Take a look at the supplied code to see how this is done if you like.) You can read from <strong>inFile</strong> in exactly the same way that you usually read from <strong>keyboard</strong>. Read in the values from the file and set up the pre-defined <strong>grid</strong></li>

   <li>Complete the <strong>putInNumbers</strong> method, which will change some of the 0’s in the array to positive numbers instead. The numbers should start at 1 in the top left, and increase going across the rows, and down the columns, as shown in the example below. The rules for placing numbers are:

    <ol>

     <li>An empty square should get a number <em>if</em> there is a black square immediately above it, <em>or</em> it is in the top row.</li>

     <li>An empty square should get a number <em>if</em> there is a black square immediately to the left of it, <em>or</em> it is in the leftmost column.</li>

    </ol></li>

  </ol></li>

</ol>

<ul>

 <li>Note that a square might get a number for both of these reasons.</li>

</ul>

<ol start="4">

 <li>Download the file <strong>txt</strong>. Also download and compile the <strong>StdDraw.java</strong> file and the <strong>TestLab4Gold.java</strong> file. Make sure all the files are in the same folder. Run the</li>

</ol>

<strong>TestLab4Gold</strong> program. A dialog box will appear asking you to choose a file. Choose the file <strong>CrosswordGridPattern.txt</strong>. A graphics window should appear containing the crossword puzzle grid shown below.

<strong> </strong>

Just for fun: You can use the Save… command in the graphics window to save this file as a .jpg image. Print it out and solve the puzzle using these clues:




<table width="353">

 <tbody>

  <tr>

   <td width="222"><strong>Across</strong></td>

   <td width="131"><strong>Down</strong></td>

  </tr>

  <tr>

   <td width="222">1: And so on…</td>

   <td width="131">1: A small dash</td>

  </tr>

  <tr>

   <td width="222">4: Abbreviation for 4 down</td>

   <td width="131">2: A drink from Tim’s</td>

  </tr>

  <tr>

   <td width="222">7: Prefix for “new”</td>

   <td width="131">3: What computers do</td>

  </tr>

  <tr>

   <td width="222">8: Trig. function</td>

   <td width="131">4: A Faculty at the U of M</td>

  </tr>

  <tr>

   <td width="222">9: Sphere of influence</td>

   <td width="131">5: A small bed</td>

  </tr>

  <tr>

   <td width="222">11: A dessert</td>

   <td width="131">6: But __ it art?</td>

  </tr>

  <tr>

   <td width="222">12: A type of pet</td>

   <td width="131">10: Base 2 (abbrev.)</td>

  </tr>

  <tr>

   <td width="222">14: ___ serious!</td>

   <td width="131">12: Big ___</td>

  </tr>

  <tr>

   <td width="222">15: Feline</td>

   <td width="131">13: Sweet potato</td>

  </tr>

  <tr>

   <td width="222">17: Unity</td>

   <td width="131">14: Board game</td>

  </tr>

  <tr>

   <td width="222">18: Punk offshoot</td>

   <td width="131">16: Get back __ work!</td>

  </tr>

 </tbody>

</table>


