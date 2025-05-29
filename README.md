
markdown
Copy
Edit
# C++ Pathfinding Visualizer

A console-based and SFML-enhanced C++ pathfinding visualizer that supports multiple search algorithms on a randomly generated maze. Includes algorithm performance comparisons in a summary table.

---

## 🔧 Features

- ✅ **Randomly generated, always solvable mazes**
- ✅ **Pathfinding algorithms implemented**:
  - Breadth-First Search (BFS)
  - Depth-First Search (DFS)
  - Dijkstra's Algorithm
  - A* Search
  - Jump Point Search (JPS) — with 8-directional movement
- ✅ **Menu system using SFML**
- ✅ **Comparison table** (Path length, Time taken, Nodes explored, Operations)
- ✅ **Supports 8-directional movement**

---


## How It Works

1. **Maze Generation**  
   - A 25×50 grid maze is randomly generated.
   - Guarantees at least one valid path from start to end.
   - GUI rendering using SFML

2. **SFML Menu**  
   - Presents a graphical menu to choose algorithms or quit.
   - Displays final result metrics (time, length, nodes, operations).

3. **Algorithms**  
   Each algorithm visualizes the pathfinding process in the console and outputs performance metrics.

---

## Algorithms Explained

| Algorithm | Heuristic | Weighted | Explores All Nodes | Supports 8-Direction | Fast |
|----------|------------|-----------|---------------------|----------------------|------|
| BFS      | ❌         | ❌        | ✅                  | ✅                   | ⚪    |
| DFS      | ❌         | ❌        | ❌ (deep)           | ✅                   | ⚪    |
| Dijkstra | ❌         | ❌        | ✅                  | ✅                   | ⚪    |
| A*       | ✅ (Manhattan/Diagonal) | ❌ | ✅        | ✅                   | ✅    |
| JPS      | ✅         | ❌        | ❌ (pruned)         | ✅                   | ✅✅   |

---



## Installation

### Requirements

- C++17 or later
- [SFML 2.5+](https://www.sfml-dev.org/) (if using the GUI version)
- Windows / Linux (tested)
- Visual Studio or g++ / Clang

### Building with Visual Studio

Open .sln file

Right-click solution → Retarget if necessary

Ensure SFML is properly linked (The files in repository are for vs 2022 using SFML version 2.5.1)

Build & Run



### Maze Generation

Uses randomized obstacle placement with a guarantee of at least one valid path from Start to Goal

Ensures mazes are roomy and not overly congested

### Output

After running, the program generates:

- ✅ Visualized path in console
- ✅ Performance metrics:
  - Algorithm used
  - Time taken (in milliseconds)
  - Path length
  - Nodes explored
  - Operations performed

### 📁 Example Output (in Console)

```yaml
Algorithm: A* Search
Time Taken: 2.41 ms
Path Length: 68
Nodes Explored: 152
Operations: 328
```

---

### 💡 Usage

- Launch the app.

- Maze is generated.

- Press Enter to view the algorithm menu.

- Select an algorithm.

- Maze solution is visualized.

- Metrics and comparison table are shown/exported.

---
  

### FAQ

Q: Can I disable SFML and run purely in console?  
A: Yes. The console version works independently of SFML.  

Q: Does this work with different grid sizes?  
A: Yes. You can configure the grid size in the source code.  

Q: Is this cross-platform?  
A: Yes, it works on Windows, Linux, and macOS (with SFML installed).  

---

### Future Plans

Maze editor and custom input

CSV export for algorithm benchmarks <br> <br>


--- 

### Author

Made by Hamza Yasir (hamza.yasir.6789@gmail.com)  
NamePull requests and suggestions welcome!
