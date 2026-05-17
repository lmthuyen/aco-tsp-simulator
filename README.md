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

**Algorithm Enhancements:**

* **2-opt Local Search** - refines tours by reversing path segments; includes a Passes slider and Best Ant Only toggle for speed control
* **Candidate List (K neighbors)** - limits city evaluation to K nearest neighbors per step, speeding up each iteration significantly
* **Population Restart**: resets pheromones after N iterations without improvement to escape local optima

**Tech Stack:**
* Vanilla HTML / CSS / JavaScript
* HTML5 Canvas API for visualization
* File API for .tsp input and Blob export

**Usage:**
* Open aco-tsp.html in any modern browser. Load kroA100.tsp to benchmark against the known optimal of 21,282.

**Benchmark Result:**
* Validated on kroA100.tsp (100 cities) - Baseline: 22,307 (~4.82% gap). With all enhancements ON: consistently below 22,000.

**Built With AI Assistance:**
* Generated using NotebookLM over 3 prompt iterations, with manual corrections for TSPLIB file parsing, distance calculation accuracy, and canvas rendering performance. Enhancements and optimizations added iteratively using Claude.

**WebApp Preview**

<img width="1920" height="993" alt="Screenshot 2026-05-16 at 10 33 20 PM" src="https://github.com/user-attachments/assets/802302ec-6e59-4851-9b9e-9f0a472d29c9" />
<img width="305" height="930" alt="Screenshot 2026-05-16 at 10 32 27 PM" src="https://github.com/user-attachments/assets/fb33c064-8d9a-46dd-beb3-bc0499a2805a" />
