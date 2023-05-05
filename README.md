Download Link: https://assignmentchef.com/product/solved-cst-370-homework-5
<br>
<h1>Problems</h1>

<table width="340">

 <tbody>

  <tr>

   <td width="277">1    Grid Walk</td>

   <td width="63">10 points</td>

  </tr>

  <tr>

   <td width="277">2    Heuristics</td>

   <td width="63">10 points</td>

  </tr>

  <tr>

   <td width="277">3    Elevations</td>

   <td width="63">15 points</td>

  </tr>

  <tr>

   <td width="277">4    Optimizing Routes</td>

   <td width="63">15 points</td>

  </tr>

  <tr>

   <td width="277">5    Essential Services</td>

   <td width="63">15 points</td>

  </tr>

 </tbody>

</table>




<h1>1.       Grid Walk (10 points)</h1>

<a href="https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/grid-walk"><strong>https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/grid-walk</strong></a>

Given a grid with obstacles, we want to find the shortest path from a starting position to an ending position using Dijkstra’s algorithm. In this grid, you can move in all 8 directions: Up, Down, Left, Right, and the 4 diagonals.

<h2>Input</h2>

<ul>

 <li>The first line contains an integer, <em>n</em>, the dimension of the <em>nxn </em> • The second line contains two space-separated integers, the starting position in the order row column.</li>

 <li>The third line contains two space-separated integers, the ending position in the order row column.</li>

 <li>The next n lines contain the space separated row. Each element is either a O indicating no obstacle or a X indicating an obstacle.</li>

</ul>

<h2>Constraints</h2>

You can assume a path exists (and therefore that the starting and ending positions are Os) and that the starting and ending positions are in-bounds.

<h2>Output</h2>

The output contains a single line with an integer, the length of the shortest path (where each move, whether up, down, left, right, or diagonal) counts as 1 step.

Sample Input 1                                                          Sample Output 1

<table width="622">

 <tbody>

  <tr>

   <td width="311">40 23 1X X O XX X O OX X X OX O O O</td>

   <td width="311">4</td>

  </tr>

 </tbody>

</table>

Sample Input 2                                                          Sample Output 2

<table width="622">

 <tbody>

  <tr>

   <td width="311">60 15 2O O O O O XX X O X O OO O X O O XX O O O O OO O X X X OX O O X O O</td>

   <td width="311">5</td>

  </tr>

 </tbody>

</table>

<h1>2.       Heuristics (10 points)</h1>

<a href="https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/heuristics"><strong>https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/heuristics</strong></a>

Given a grid with obstacles, we want to find the shortest path from a starting position to an ending position. This time we’d like to use the A-Star algorithm. In this grid, you can only move in four directions: up, down, left, right therefore the heuristic that we will use will be the manhatten distance algorithm.

<h2>Input</h2>

<ul>

 <li>The first line contains an integer, <em>n</em>, the dimension of the <em>nxn </em> • The second line contains two space-separated integers, the starting position in the order row column.</li>

 <li>The third line contains two space-separated integers, the ending position in the order row column.</li>

 <li>The next n lines contain the space separated row. Each element is either a O indicating no obstacle or a X indicating an obstacle.</li>

</ul>

<h2>Constraints</h2>

You can assume a path exists (and therefore that the starting and ending positions are Os) and that the starting and ending positions are in-bounds.

<h2>Output</h2>

The output contains a single line with an integer, the length of the shortest path (where each move, whether up, down, left, or right) counts as 1 step.

Sample Input 1                                                          Sample Output 1

<table width="622">

 <tbody>

  <tr>

   <td width="311">40 23 1X X O XX X O OX X X OX O O O</td>

   <td width="311">6</td>

  </tr>

 </tbody>

</table>

Sample Input 2                                                          Sample Output 2

<table width="622">

 <tbody>

  <tr>

   <td width="311">60 15 2O O O O O XX X O X O OO O X O O XX O O O O OO O X X X OX O O X O O</td>

   <td width="311">12</td>

  </tr>

 </tbody>

</table>

<h1>3.       Elevations (15 points)</h1>

<a href="https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/elevations"><strong>https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/elevations</strong></a>

I like running to different places but hate running uphill. I have a number of typical routes I run and I’d like to know the least elevation change it would take me to reach them. Help me find the elevation change to get from my house to each of the places I run to, taking only the routes I know. You will receive the list of pleces, the routes I know how to take, and the elevation change per route.

<h2>Starter code</h2>

The code below will help you read input for this problem.

<ul>

 <li>C++: <a href="https://repl.it/@dsyang/Elevations-cpp">https://repl.it/@dsyang/Elevations-cpp</a></li>

 <li>Java: <a href="https://repl.it/@dsyang/Elevations-java">https://repl.it/@dsyang/Elevations-java</a></li>

 <li>Python: <a href="https://repl.it/@dsyang/Elevations-py">https://repl.it/@dsyang/Elevations-py</a></li>

</ul>

<h2>Input</h2>

<ul>

 <li>The first line will contain a location, my home.</li>

 <li>The next line will contain an integer, <em>r</em>, the number of routes I run.</li>

 <li>Finally, the last <em>r </em>lines will contain the routes, consisting of comma-separated endpoints followed by the elevation change along that route.</li>

</ul>

<h2>Constraints</h2>

You cannot assume the graph is connected; there may be a place I cannot reach taking only routes that I know.

<h2>Output</h2>

<ul>

 <li>The output will consist of <em>n </em></li>

 <li>each line consists of a place name (in alaphabetical order), followed by a colon, a space, and the least elevation change to that place from my source.</li>

 <li>If there is no route to that place, print ”NONE” instead.</li>

</ul>




Sample Output 1

<table width="622">

 <tbody>

  <tr>

   <td width="311">Home9Bookworks, Home, 95Bookworks, Aquarium, -50Home, Aquarium, 150 Home, Starbucks, 12Home, Beach, -100Beach, Starbucks, 55Aquarium, Bookworks, 50 Starbucks, Carmel, 200Carmel, Home, -100</td>

   <td width="311">Bookworks: 200Home: 0Aquarium: 150Starbucks: -45Beach: -100 Carmel: 155</td>

  </tr>

 </tbody>

</table>







<h1>4.       Optimizing Routes (15 <sub>points)</sub></h1>

<a href="https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/optimizing-routes"><strong>https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/optimizing-routes</strong></a>

I have my set ways of traveling to places I visit often. However, I’m curious if my routes are actually the best routes according to maps. Determine the difference in my route and the supposed best route for each of my destinations. subsection*Starter code The code below will help you read input for this problem.

<ul>

 <li>C++: <a href="https://repl.it/@dsyang/Optimizing-Routes-cpp">https://repl.it/@dsyang/Optimizing-Routes-cpp</a></li>

 <li>Java: <a href="https://repl.it/@dsyang/Optimizing-Routes-java">https://repl.it/@dsyang/Optimizing-Routes-java</a></li>

 <li>Python: <a href="https://repl.it/@dsyang/Optimizing-Routes-py">https://repl.it/@dsyang/Optimizing-Routes-py</a></li>

</ul>

<h2>Input</h2>

<ul>

 <li>The first line will contain a location, my home.</li>

 <li>The next line will contain an integer <em>n</em>, the number of places I visit often enough to have a set route, followed by how long my route to that place takes.</li>

 <li>The next line will contain an integer, <em>r</em>, the number of roads.</li>

 <li>Finally, the last <em>r </em>lines will contain the roads, consisting of comma-separated endpoints followed by the time it takes to travel the road.</li>

</ul>

<h2>Constraints</h2>

You can assume all the weights are positive (it takes time to travel a road) and that all locations have unique names. You may choose which appropriate path-finding algorithm to use to solve this problem.

<h2>Output</h2>

<ul>

 <li>The output will consist of <em>n </em></li>

 <li>Each line consists of a destination I visit often, followed by a space, followed by either ”FASTEST” if my route is equal to or faster than the recommended route. ”NO PATH” if there is no recommended route from my home to that location. Or an integer <em>x </em>representing how much faster the recommended route is.</li>

 <li>The <em>n </em>destinations will be ordered alphabetically, case-insensitive. This means Carmel will come before CSUMB.</li>

</ul>

Sample Output 1

<table width="622">

 <tbody>

  <tr>

   <td width="321">Home4Bookworks, 9CSUMB, 16East Village, 6Carmel Beach, 2117Presidio, Bookworks, 3Presidio, Aquarium, 3Presidio, Colton Hall, 2 Presidio, Home, 5Home, Carmel Village, 17Home, REI, 12REI, CSUMB, 3Home, CSUMB, 16Home, East Village, 6Home, 17-Mile Drive, 10Home, Colton Hall, 4Home, Sushi Time, 10CSUMB, Sushi Time, 7Carmel Beach, 17-Mile Drive, 12East Village, Colton Hall, 5Colton Hall, Home, 4Carmel Village, Carmel Beach, 4</td>

   <td width="301">Bookworks NO PATHCarmel Beach FASTEST CSUMB 1East Village FASTEST</td>

  </tr>

 </tbody>

</table>

<h1>5.       Essential Services (15 <sub>points)</sub></h1>

<a href="https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/all-pairs"><strong>https://www.hackerrank.com/contests/cst370-s19-hw5/challenges/all-pairs</strong></a>

King’s Landing is trying to evaluate the quality of life of its citizens. One of the components is the time it takes each citizen to get to every essential service. Given the citizens and services, find the distance from each citizen to each service.

<h2>Starter code</h2>

The code below will help you read input for this problem.

<ul>

 <li>C++: <a href="https://repl.it/@dsyang/Essential-Services-cpp">https://repl.it/@dsyang/Essential-Services-cpp</a></li>

 <li>Java: <a href="https://repl.it/@dsyang/Essential-Services-java">https://repl.it/@dsyang/Essential-Services-java</a></li>

 <li>Python: <a href="https://repl.it/@dsyang/Essential-Services-py">https://repl.it/@dsyang/Essential-Services-py</a></li>

</ul>

<h2>Input</h2>

<ul>

 <li>The first line contains an integer, <em>c</em>, the number of citizens.</li>

 <li>The next <em>c </em>lines contain the citizens’ names.</li>

 <li>The next line contains an integer, <em>s</em>, the number of services.</li>

 <li>The next <em>s </em>lines contain the services’ names.</li>

 <li>The next line contains an integer, <em>e</em>, the number of direct routes.</li>

 <li>Each of the next <em>e </em>lines contains a direct route which consists of two comma-separated entities (citizens or servies) and a time it takes to get from one to the other.</li>

</ul>

<h2>Constraints</h2>

You can assume all the weights are positive (it takes time to get from one place to the other) and that all citizens and services have unique names.

<h2>Output</h2>

<ul>

 <li>The output will consist of <em>c </em>+ 1 lines.</li>

 <li>The first line consists of the services in alphabetical order, space-separated.</li>

 <li>The next <em>c </em>lines consist of a citizen and their times from each service. You should have <em>s </em>space-separated integers, the time from each service in alphabetical order, followed by the citizen name (in alphabetical order).</li>

</ul>

Sample Output 1

<table width="622">

 <tbody>

  <tr>

   <td width="311">5CerseiRobert JamieQyburn Tomin2CastleChurch9Castle, Robert, 15Robert, Qyburn, 155Robert, Tomin, 15Castle, Tomin, 35Qyburn, Church, 15 Robert, Jamie, 30Jamie, Church, 115Robert, Cersei, 300Cersei, Church, 60</td>

   <td width="311">Castle Church220 60 Cersei 45 115 Jamie170 15 Qyburn 15 145 Robert30 160 Tomin</td>

  </tr>

 </tbody>

</table>


