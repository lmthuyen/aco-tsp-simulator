# ACO Traveling Salesman Simulator - Browser-Based Metaheuristic Tool
A single-file, browser-based Ant Colony Optimization (ACO) simulator for the Traveling Salesman Problem (TSP), built with vanilla HTML, CSS, and JavaScript. Developed as part of a Decision Models course project (BANA 4095), this app runs the full Ant System algorithm entirely in the browser with real-time visualization.

**Features:**
* Load TSPLIB .tsp files or randomly generate city sets
* Real-time canvas visualization of pheromone trails, ant movement, and best tour path
* Live stats panel showing best tour length, current iteration, and convergence chart
* Interactive sliders for all 5 ACO parameters (ants, alpha, beta, rho, speed) with color-filled progress indicators
* Start, Pause, and Reset controls without losing simulation state
* Export best solution as a downloadable text file with route, distance, and parameters
* Uses EUC_2D integer-rounded distance formula for TSPLIB-accurate results
* Optimized canvas rendering with glowing star aesthetic for city nodes

**Tech Stack:**
Vanilla HTML / CSS / JavaScript
HTML5 Canvas API for visualization
File API for .tsp input and Blob export

**Usage:**
* Open aco-tsp.html in any modern browser. Load kroA100.tsp to benchmark against the known optimal tour of 21,282.

**Benchmark Result:**
* Validated on kroA100.tsp (100 cities) - achieved 22,307 with optimized parameters (~4.82% gap from optimal), a reasonable result for a metaheuristic approach on an NP-hard problem.

**Built With AI Assistance:**
* Generated using NotebookLM over 3 prompt iterations, with manual corrections for TSPLIB file parsing, distance calculation accuracy, and canvas rendering performance.
