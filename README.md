Download Link: https://assignmentchef.com/product/solved-comp2710-homework-3-the-greatest-puzzle-solver-of-all-time
<br>



In the land of Puzzlevania, Aaron, Bob, and Charlie had an argument over which one of them was the greatest puzzle-solver of all time.  To end the argument once and for all, they agreed on a duel to the death (this makes sense?). Aaron was a poor shot and only hit this target with a probability of 1/3. Bob was a bit better and hit his target with a probability of 1/2. Charlie was an expert marksman and never missed. A hit means a kill and the person hit drops out of the duel.




To compensate for the inequities in their marksmanship skills, the three decided that they would fire in turns, starting with Aaron, followed by Bob, and then by Charlie. The cycle would repeat until there was one man standing. That man would be remembered for all time as the Greatest Puzzle-Solver of All Time.




An obvious and reasonable strategy is for each man to shoot at the most accurate shooter still alive, on the grounds that this shooter is the deadliest and has the best chance of hitting back.




Write a program to simulate the duel using this strategy. Your program should use random numbers and the probabilities given in the problem to determine whether a shooter hits his target. You will likely want to create multiple functions to complete the problem. My solution had only one function to simulate the duels and it passed in the odds and the three guys as pass-by-reference parameters.  Once you can simulate a duel, add a loop to your program that simulates 10,000 duels. Count the number of times that each contestant wins and print the probability of winning for each contestant (e.g., for Aaron your might output “Aaron won 3612/10000 duels or 36.12%).




<strong>Strategy 2:</strong> An alternative strategy for Aaron is to intentionally miss on his first shot. Write a function to simulate Strategy 2. Your program will determine which strategy is better for Aaron.




<strong>Note:</strong> You must provide the following user interface. Red text might be different for different runs due to the random number. You do not need to display text in red.







<table width="576">

 <tbody>

  <tr>

   <td width="576">*** Welcome to Puzzlevania’s Duel Simulator ***Unit Testing 1: Function – at_least_two_alive()Case 1: Aaron alive, Bob alive, Charlie alive<sup> </sup><sup>  </sup>  <sup>Case passed … </sup>Case 2: Aaron dead, Bob alive, Charlie aliveCase passed …Case 3: Aaron alive, Bob dead, Charlie alive Case passed …     Case 4: Aaron alive, Bob alive, Charlie dead          Case passed …Case 5: Aaron dead, Bob dead, Charlie alive <sup> </sup><sup>  </sup>        <sup>Case passed … </sup>Case 6: Aaron dead, Bob alive, Charlie deadCase passed …<sub> </sub>   Case 7: Aaron alive, Bob dead, Charlie dead Case passed …<sub> </sub>       Case 8: Aaron dead, Bob dead, Charlie dead Case passed …  Press any key to continue…<sup> </sup><sup> </sup>Unit Testing 2: Function Aaron_shoots1(Bob_alive, Charlie_alive)Case 1: Bob alive, Charlie aliveAaron is shooting at Charlie                 Aaron misses.Case 2: Bob dead, Charlie alive  Aaron is shooting at CharlieCharlie is dead.Case 3: Bob alive, Charlie dead               Aaron is shooting at Bob              Aaron misses.Press any key to continue… <sub> </sub>Unit Testing 3: Function Bob_shoots(Aaron_alive, Charlie_alive)    Case 1: Aaron alive, Charlie aliveBob is shooting at Charlie           Charlie is dead.Case 2: Aaron dead, Charlie alive<sub> </sub>              Aaron is shooting at Charlie Bob missedCase 3: Aaron alive, Charlie dead <sub> </sub>            Bob is shooting at Aaron Aaron is dead.  Press any key to continue… <sup> </sup>Unit Testing 4: Function Charlie_shoots(Aaron_alive, Charlie_alive) <sup> </sup>Case 1: Aaron alive, Bob alive             Charlie is shooting at Bob           Bob is dead.Case 2: Aaron dead, Bob aliveCharlie is shooting at BobBob is deadCase 3: Aaron alive, Bob dead              Charlie is shooting at Aaron               Aaron is dead.Press any key to continue…  Unit Testing 5: Function Aaron_shoots2(Bob_alive, Charlie_alive)       Case 1: Bob alive, Charlie aliveAaron intentionally misses his first shot                Both Bob and Charlie are alive.Case 2: Bob dead, Charlie alive            Aaron is shooting at Charlie               Charlie is dead.Case 3: Bob alive, Charlie dead            Aaron is shooting at Bob            Aaron misses.Press any key to continue… </td>

  </tr>

 </tbody>

</table>







<table width="576">

 <tbody>

  <tr>

   <td width="576"><sup> </sup><sup> </sup>Ready to test strategy 1 (run 10000 times):Press any key to continue… …… … Bob won Aaron won 4137/100003612/10000 duels or  duels or 41.3736.12% %Charlie won 2251/10000 duels or 22.51% Ready to test strategy 2 (run 10000 times):   Press any key to continue………  …<sup> </sup><sup> </sup>Aaron won 4099/10000 duels or 40.99%  Bob won 2552/10000 duels or 25.52% <sub> </sub> Charlie won 3349/10000 duels or 33.49%  Strategy 2 is better than strategy 1.</td>

  </tr>

 </tbody>

</table>




<strong><em><u>Requirements:</u></em></strong>

<ol>

 <li>You must following the above user interface to implement your program.</li>

</ol>




<ol start="2">

 <li>You must implement the following functions:

  <ul>

   <li>bool at_least_two_alive(bool A_alive, bool B_alive, C_alive)</li>

  </ul></li>

</ol>

/* Input: A_alive indicates whether Aaron is alive */

/*        B_alive indicates whether Bob is alive */

/*        C_alive indicates whether Charlie is alive */

/* Return: true if at least two are alive */

/*         otherwise return false */

<ul>

 <li>void Aaron_shoots1(bool&amp; B_alive, bool&amp; C_alive)</li>

</ul>

/* Strategy 1: Use call by reference

<ul>

 <li>Input: B_alive indicates whether Bob alive or dead</li>

 <li>C_alive indicates whether Charlie is alive or dead * Return: Change B_alive into false if Bob is killed.</li>

 <li>Change C_alive into false if Charlie is killed. */</li>

</ul>

<ul>

 <li>void Bob_shoots(bool&amp; A_alive, bool&amp; C_alive)</li>

</ul>

/* Call by reference

<ul>

 <li>Input: A_alive indicates if Aaron is alive or dead</li>

 <li>C_alive indicates whether Charlie is alive or dead * Return: Change A_alive into false if Aaron is killed.</li>

 <li>Change C_alive into false if Charlie is killed. */</li>

</ul>

<ul>

 <li>void Charlie_shoots(bool&amp; A_alive, bool&amp; B_alive)</li>

</ul>

/* Call by reference

<ul>

 <li>Input: A_alive indicates if Aaron is alive or dead</li>

 <li>B_alive indicates whether Bob is alive or dead * Return: Change A_alive into false if Aaron is killed.</li>

 <li>Change B_alive into false if Bob is killed. */</li>

</ul>

<ul>

 <li>void Aaron_shoots2(bool&amp; B_alive, bool&amp; C_alive)</li>

</ul>

/* Strategy 2: Use call by reference

<ul>

 <li>Input: B_alive indicates whether Bob alive or dead</li>

 <li>C_alive indicates whether Charlie is alive or dead * Return: Change B_alive into false if Bob is killed.</li>

 <li>Change C_alive into false if Charlie is killed.</li>

</ul>

*/




<ol start="3">

 <li>You must implement five unit test drivers (five functions) to test the above five functions. (see also the user interface above)</li>

</ol>




<ol start="4">

 <li>You must use assert in your test driver.</li>

</ol>




<ol start="5">

 <li>You must define four constants in your implementation. For example, the total number (i.e., 10,000) of runs can be defined as a constant.</li>

</ol>




<strong><em><u>Hints:</u></em></strong>

<ol>

 <li>How to implement “Press any key to continue…”</li>

</ol>

cout &lt;&lt; “Press any key to continue…”;

cin.ignore().get(); //Pause Command for Linux Terminal

<strong>Note:</strong> you can implement the above two lines as a function to be repeatedly called by other functions in your program.




<ol start="2">

 <li>You may need to use the following libraries.</li>

</ol>




# include &lt;iostream&gt;

# include &lt;stdlib.h&gt;

# include &lt;assert.h&gt; # include &lt;ctime&gt;




<ol start="3">

 <li>Initialize your random number generator:  srand(time(0));</li>

</ol>




<ol start="4">

 <li>A sample code of generating a random number is given below:</li>

</ol>




/* Assume that the probabilty of hit a target is 25 percent */ int shoot_target_result; shoot_target_result = rand()%100;




if (shoot_target_result &lt;= 25) {  cout&lt;&lt;“Hit the target
”;




/* add more code here */    }




<ol start="5">

 <li>Please follow the following sample test driver to implement all the test drivers.</li>

</ol>




void test_at_least_two_alive(void) {

cout &lt;&lt; “Unit Testing 1: Function – at_least_two_alive()
”;




cout &lt;&lt; “Case 1: Aaron alive, Bob alive, Charlie alive
”;  assert(true == at_least_two_alive(true, true, true));       cout &lt;&lt; “Case passed …
”;




cout &lt;&lt; “Case 2: Aaron dead, Bob alive, Charlie alive
”;  assert(true == at_least_two_alive(false, true, true));       cout &lt;&lt; “Case passed …
”;




cout &lt;&lt; “Case 3: Aaron alive, Bob dead, Charlie alive
”;  assert(true == at_least_two_alive(true, false, true));       cout &lt;&lt; “Case passed …
”;




/* add test cases 4-6 below */

…

}




<ol start="6">

 <li>If your strategy 1 is better than your strategy 2, then please check your source code. In this case, it is likely that you have incorrectly implemented strategy 2. Please ensure that strategy 2 is better than strategy 1.</li>

 <li>The framework of the source code is given below:</li>

</ol>




<table width="576">

 <tbody>

  <tr>

   <td width="576"># include &lt;iostream&gt; # include &lt;stdlib.h&gt;# include &lt;assert.h&gt; # include &lt;ctime&gt; using namespace std; <strong> </strong><strong>// FUNCTION PROTOTYPES </strong>bool at_least_two_alive(bool A_alive, bool B_alive, C_alive);/* Input: A_alive indicates whether Aaron is alive           B_alive indicates whether Bob is aliveC_alive indicates whether Charlie is alive    Return: true if at least two are alive            otherwise return false*//**  Add other function prototypes below*/void test_at_least_two_alive(void);/* This is a test driver for at_least_two_alive() */ /**  Add more prototypes for other test drivers below*/int main() {/**  This is the main function*  …*/}<strong> </strong><strong>// FUNCTION DEFINITIONS </strong>/* Implementation of at_least_two_alive() */bool at_least_two_alive(bool a_alive, bool b_alive, bool c_alive) { /* add the implementation below */}/* Implementation of the test driver for at_least_two_alive() */ void test_at_least_two_alive(void) {cout &lt;&lt; “Unit Testing 1: Function – at_least_two_alive()
”; cout &lt;&lt; “Case 1: Aaron alive, Bob alive, Charlie alive
”;  assert(true == at_least_two_alive(true, true, true));     cout &lt;&lt; “Case passed …
”; cout &lt;&lt; “Case 2: Aaron dead, Bob alive, Charlie alive
”;        assert(true == at_least_two_alive(false, true, true));     cout &lt;&lt; “Case passed …
”; /* add test cases 4-6 below */  <strong><em>           </em></strong> }</td>

  </tr>

 </tbody>

</table>

<strong><em><u>Programming Environment:</u></em></strong>

Write a program in C++.

<strong><em><u>Grading:</u></em></strong>

<ol>

 <li>(5 points)<strong> Use comments to provide a heading at the top of your code</strong> containing your name, Auburn Userid, filename. And pair partner’s info, if applicable. Also describe any help or sources that you used (as per the syllabus). See the sample below</li>

</ol>

<strong>// name: Sally Ride, szr0001 </strong>

<strong>// partner: Lizz Jones, lzj0001                  </strong><strong>(“NONE” if work alone)</strong>

<strong>// filename: hw01.cpp</strong>

<h1>// due date: 08/31/2018 // problem: determine how much diet soda it is possible to drink</h1>

<strong>// collaboration: I got help with data types from the TA.</strong>

<strong>    </strong><strong>(OR “I did not use any external sources for this assignment.”)</strong>

<strong>Note:</strong> You will lose <strong>at least 40 points</strong> if there are compilation errors or warning messages when we compile your source code. You will <strong>lose points</strong> if you: do not use the specific program file name, or do not have comments, or do not have a comment block on <strong>EVERY</strong> program you hand in.


