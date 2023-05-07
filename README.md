Download Link: https://assignmentchef.com/product/solved-ipc144-assignment-final-assignment
<br>
<h1>Your Task – Source Code</h1>

Download or clone the final assessment part-2 (<strong>Final-P2</strong>) from <a href="https://github.com/Seneca-144100/Final-Part-2"><strong>https://github.com/Seneca</strong></a><a href="https://github.com/Seneca-144100/Final-Part-2"><strong>144100/Final</strong></a><a href="https://github.com/Seneca-144100/Final-Part-2"><strong>–</strong></a><a href="https://github.com/Seneca-144100/Final-Part-2"><strong>Part</strong></a><a href="https://github.com/Seneca-144100/Final-Part-2"><strong>–</strong></a><a href="https://github.com/Seneca-144100/Final-Part-2"><strong>2</strong></a> <u>The Bike Race</u>

You have been tasked with developing a program to read the information about a bike race from a text file and produce a report on it.  The race is a major event and could attract up to 5,000 participants. The potential of having such high volume of data will require you to be efficient in how the data is read, stored and processed.  There are three timestamps recorded for each rider:

<ol>

 <li>The start time</li>

 <li>The time when the rider crested the top of a mountain pass that is on the route</li>

 <li>The completion time (or the time at which the rider withdrew)</li>

</ol>

In the event that a rider does not complete the course, they are marked as having not completed and the time at which they withdrew is recorded but not used in any calculations and riders who do not finish are not eligible for any awards.

Riders are organized into categories based on <strong>age</strong> and the <strong>race length</strong>.  Age groupings are determined by age ranges, where <strong>16-20</strong> are <strong>juniors</strong>, <strong>21-34</strong> are <strong>adults</strong> and <strong>35 or older</strong> are <strong>seniors</strong>.  There are three different races lengths, <strong>S</strong> (<strong>short, 50km</strong>), <strong>M</strong> (<strong>medium, 75 km</strong>), and <strong>L</strong> (<strong>long, 100 km</strong>).  The race will have different start times for each category but this has no impact on the times it will take the riders to complete the course.

You cannot guarantee that enough riders will enter for each category to win all awards available and awards that are not awarded will be listed as “<strong>Not Awarded</strong>”.

<u>For example</u>:

<ol>

 <li>If you request a report for the winners of each category and there is a category with no entrants, you would list it as “Not Awarded” rather than putting a rider’s name.</li>

 <li>Likewise, if you request a report for the top 3 riders in each category and a category only has 2 entrants, then you just print the top 2 entrants.</li>

</ol>

The following is a sample of the file “<strong><u>data.txt</u></strong>” which will be read by the program. Each line of the file contains the name of the rider, age, race length (S, M, or L), the clock time of the race start, clock time of cresting the mountain and clock time of finishing the race. In the event that a rider withdraws, there is a “W” at the end of the line and the mountain time will be zero if they did not make it that far while the finish time will be when the rider withdrew. <strong>====================== Sample “<u>data.txt</u>” File =====================</strong>

Eddy Mercx, 72 M 1:10 1:59 2:58

Jocelyn Lovell, 60 M 1:10 0:00 1:34 W

Jason Gaudet, 28 M 1:10 2:11 3:09

Claude Van Gogh, 20 M 1:10 2:25 3:24

Lance Armstrong, 40 M 1:10 2:02 3:05

Arlenis Sierra, 26 L 1:00 1:51 2:41

Billy F. Gibbons, 62 S 1:20 2:42 4:28

Charlie Watt, 66 S 1:20 3:08 5:39

Cecilie Ledwig, 23 L 1:00 1:49 2:38

Nikki Sixx, 48 S 1:20 2:59 4:58

Kirsten Wild, 34 L 1:00 1:55 2:54

Eddie Van Halen, 63 S 1:20 2:10 3:55

Rachel McKinnon, 37 L 1:00 1:39 2:41

Angus Young, 61 S 1:20 2:02 3:10

<strong>======================= End Sample Data File =======================</strong>

<strong><em><u>NOTE</u></em></strong><em>: Remember this data file could likely contain a maximum 5,000 records</em>

<ul>

 <li>The above sample “<strong>txt</strong>” file is included and should be used in your development.</li>

 <li>You should take a backup of this file so you can modify it with different data to thoroughly test your reporting logic (not all scenario’s are demonstrated in the example)</li>

</ul>




<h2>File Helper Module</h2>

A “<strong>file_helper</strong>” module has been provided for you and your code <u>must use the provided</u> <strong><em><u>readFileRecord()</u></em></strong><u> function</u> in order to read each line of the data file.

The code requires the use of a <strong><em>RiderInfo</em></strong> structure.  The <strong><em>RiderInfo</em></strong> structure members are purposely missing and will require you to define them based on the code in the <strong><em>readFileRecord()</em></strong> function.




<strong><em><u>NOTE</u></em></strong><strong><em>: You are <u>not to modify</u> the “file_helper” module files with the exception of completing the RiderInfo structure members in the “file_helper.h” file. </em></strong>




<h2>Additional Module’s</h2>

You are free to design your solution as you see fit, however, your solution design should implement additional modularity if/when possible.

<h2>Application Main Entry Point (main)</h2>

You will be required to develop the main function (application entry point) in the file “<strong>main.c</strong>” that will launch your solution.




<h2>Menu &amp; Reporting Options</h2>

The following menu/reporting options must be offered:

<ul>

 <li><strong>“Display the best 3 riders in a category” </strong></li>

</ul>

<em><u>Note</u></em><em>: “best” means the <u>fastest</u> completed times (lowest duration)</em>

<ul>

 <li><strong>“Display all riders in a category” </strong></li>

 <li><strong>“Display the worst 3 riders in a category” </strong></li>

</ul>

<em><u>Note</u></em><em>: “worst” means the <u>slowest</u> completed times (highest duration)</em>

<ul>

 <li><strong>“Display the winners in all categories” </strong></li>

 <li><strong>“Exit the application” </strong></li>

</ul>




The following two pages, is an example output execution of the minimum expected behaviour of how your solution should work.




<u>Note</u>

<ul>

 <li>You are encouraged to improve on the menu in a way you think would be more user-friendly</li>

</ul>




<ul>

 <li>Your solution should closely (if not exactly) match the tabular format used in the example reporting output/display parts</li>

</ul>




<ul>

 <li><strong>The example does not show all possible data output scenario’s described in the requirements such as the scenario for “Not Awarded”. However, it is <u>expected</u> your solution will work and behave as required in <u>all possible</u> <u>cases</u></strong>.</li>

</ul>




<h2>Example Execution</h2>

<strong>Highlighted</strong> text represents user input.

******************** Seneca Cycling Race Results ********************

What would you like to do?

<ul>

 <li>– Exit</li>

 <li>– Print top 3 riders in a category</li>

 <li>– Print all riders in a category</li>

 <li>– Print last 3 riders in a category</li>

 <li>– Print winners in all categories</li>

</ul>

<h3>: 1</h3>




Which category (S, M, L): <strong>s </strong>




Rider                    Age Group Time

—————————————

Angus Young                 Senior 1:50

Eddie Van Halen             Senior 2:35

Billy F. Gibbons            Senior 3:08




What would you like to do?

<ul>

 <li>– Exit</li>

 <li>– Print top 3 riders in a category</li>

 <li>– Print all riders in a category</li>

 <li>– Print last 3 riders in a category</li>

 <li>– Print winners in all categories</li>

</ul>

<h3>: 2</h3>




Which category (S, M, L): <strong>S</strong>




Rider                    Age Group Time Withdrew

————————————————

Angus Young                 Senior 1:50       No

Eddie Van Halen             Senior 2:35       No

Billy F. Gibbons            Senior 3:08       No

Nikki Sixx                  Senior 3:38       No

Charlie Watt                Senior 4:19       No

Jocelyn Lovell              Senior  N/A      Yes




What would you like to do?

<ul>

 <li>– Exit</li>

 <li>– Print top 3 riders in a category</li>

 <li>– Print all riders in a category</li>

 <li>– Print last 3 riders in a category</li>

 <li>– Print winners in all categories</li>

</ul>

<h3>: 3</h3>




Which category (S, M, L): <strong>S</strong>




Rider                    Age Group Time

—————————————

Billy F. Gibbons            Senior 3:08

Nikki Sixx                  Senior 3:38

Charlie Watt                Senior 4:19




What would you like to do?

<ul>

 <li>– Exit</li>

 <li>– Print top 3 riders in a category</li>

 <li>– Print all riders in a category</li>

 <li>– Print last 3 riders in a category</li>

 <li>– Print winners in all categories</li>

</ul>

<h3>: 4</h3>




Rider                    Age Group Category Time

————————————————

Angus Young                 Senior    50 km 1:50

Eddy Mercx                  Senior    75 km 1:48

Cecilie Ledwig               Adult   100 km 1:38




What would you like to do?

<ul>

 <li>– Exit</li>

 <li>– Print top 3 riders in a category</li>

 <li>– Print all riders in a category</li>

 <li>– Print last 3 riders in a category</li>

 <li>– Print winners in all categories</li>

</ul>

: <strong>0</strong>




Keep on Riding!




<h1>Reflection</h1>

<strong><u>Each student</u></strong> must submit a reflection and will be independently graded (if you are working in a group, only the source code portion will be a shared grade).  Please provide answers to the following in a text file named <strong><em><u>reflect.txt</u></em></strong>.  Remember, include your <strong><u>DIGITAL SIGNATURE</u></strong> as described on page one of this document.

Your reflection answers should be detailed and accurate.  A suitable response should be <strong>at least 100 words</strong> for <strong><u>each</u></strong> reflection question.  This implies your <strong><u>overall</u></strong> reflection must be a <strong>minimum of 300 words (not including the question if you repeat it in the answer)</strong>.

<ul>

 <li>This program can greatly benefit from modular programming. Describe how you decided to make your program more modular.  For each function you created, describe you decided to make the function and why its contents should be in one function.</li>

 <li>The text for the categories is repeated a lot. Describe how you stored this efficiently to reduce wasting memory.  Why is the technique you used more space efficient than other techniques?  Pick one other technique that is less efficient than your method and describe why your method is superior (better).</li>

 <li>Reading the data from the file presented some challenges. Explain how the readFileRecord() function determined when the end of line (record) had been reached, given that some of the riders might have withdrawn and would have a different number of fields on the line. Describe another technique you could use to handle the differing number of fields on each line (record).</li>

</ul>