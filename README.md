Download Link: https://assignmentchef.com/product/solved-ee328-operating-system-1
<br>



<h1>Snake-Like Increment Tables</h1>




<h2>1 PROBLEM</h2>

<h3>1.1 DESCRIPTION</h3>

This program will create small, snake-like increment tables, up to 9×9 in size. It starts from 1, and the value keep increasing by one. For the first row, it increase from left to right; for the second row, it increase from right to left; the third row, from left to right, … , etc. Just like a snake.

<h3>1.2 SAMPLE</h3>

&gt;java SnakeTable

Enter table size 1-9, 0 to exit: 9

1             2         3         4         5         6         7         8         9

<ul>

 <li>17 16             15             14             13             12             11             10</li>

 <li>20 21             22             23             24             25             26             27</li>

 <li>35 34             33             32             31             30             29             28</li>

 <li>38 39             40             41             42             43             44             45</li>

 <li>53 52             51             50             49             48             47             46</li>

 <li>56 57             58             59             60             61             62             63</li>

 <li>71 70             69             68             67             66             65             64</li>

 <li>74 75             76             77             78             79             80             81</li>

</ul>

Enter table size 1-9, 0 to exit: 3

1         2       3

<ul>

 <li>5 4</li>

 <li>8 9</li>

</ul>

Enter table size 1-9, 0 to exit: 1

1

Enter table size 1-9, 0 to exit: 746

please enter a number in the range 0-9

Enter table size 1-9, 0 to exit: -231 please enter a number in the range 0-9

Enter table size 1-9, 0 to exit: 0

<h3>1.3 SPECIFICATION</h3>

The program should repeatedly request input in the range 0-9 (sample code to get console input is below). Numbers outside this range should be politely rejected. 0 will stop execution of the program. Numbers not parseable as integers should also cause the program to exit. For input in the 1-9 range, the program should produce a multiplication table as shown above. The formatting does not have to precisely match the above, but the numbers should be in columns. You may use any combination of tabs and spaces for formatting. I would avoid Java’s NumberFormatter classes for this one, but if you’re feeling daring, go for it.

<h2>2 ALGORITHM</h2>

<h3>2.1 BASIC ALGORITHM</h3>

After read in the user input we use a function printSnake() to print the snake table. It’s easy to learn that in odd rows the number is increasing while the number is decreasing in even rows. Considering the row is denoted as i and the column is denoted as j, the algorithm is designed below.

<ul>

 <li>For odd rows the numbers are set to be n * (i – 1) + j.</li>

 <li>For even rows the numbers are set to be n * i + 1 – j.</li>

</ul>

<h3>2.2 ROBUSTNESS CONSIDERATION</h3>

In order to improve the robustness of user input we use regular expression [0-9] to catch correct input. If the input is out of bound or characteristics other than numbers the command line window will display “please enter a number in the range 0-9”. Particularly, when the input equals ’0’ the function printSnake() will not be executed and the program will exit.

<h2>3 RESULTS</h2>

<h3>3.1 ENVIRONMENT</h3>

<ul>

 <li>Windows 10</li>

 <li>Java Development Kit 1.8.0_131</li>

 <li>Eclipse</li>

</ul>

<h3>3.2 SCREENSHOTS OF THE RESULT</h3>

We use command line to compile and execute the program. The result is shown in Fig. 3.1.

Figure 3.1: Screenshot of Snake-Like Increment Table

<h3>3.3 THOUGHTS</h3>

It is the first Java program I have ever written except “hello world!”. Java has a lot of interesting features and I will try to make full use of them in the future.