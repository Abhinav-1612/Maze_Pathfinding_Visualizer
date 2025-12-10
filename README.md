# Maze_Pathfinding_Visualizer
An interactive Python application that visualizes various pathfinding algorithms in real-time. Built with Tkinter, this tool allows you to draw custom mazes and watch how different algorithms explore and find paths through them.

Features-
Interactive Maze Creation: Draw walls, set start and goal positions with mouse clicks
Multiple Algorithms: Compare 5 different pathfinding algorithms
Real-time Visualization: Watch algorithms explore the maze step-by-step
Performance Metrics: Track nodes explored, path length, cost, and execution time
Adjustable Speed: Control visualization speed with a slider
Algorithm Comparison: See which algorithms guarantee optimal paths

Algorithms Implemented-
AlgorithmOptimalDescriptionBFS (Breadth-First Search) YesExplores uniformly in all directions, guarantees shortest pathDFS (Depth-First Search) NoMemory efficient but doesn't guarantee optimal pathA* (A-Star)✅ YesUses heuristic function (f = g + h) for optimal pathfindingBest-First Search NoGreedy algorithm using only heuristic, fast but not optimalIDA* (Iterative Deepening A*)✅ YesMemory efficient optimal search with iterative deepening

Requirements-
Python 3.6+
tkinter (usually comes pre-installed with Python)
No additional packages required! All dependencies are part of Python's standard library.

🔧 Installation
Clone this repository:

bashgit clone https://github.com/Abhinav-1612/maze-pathfinder.git
cd maze-pathfinder

Run the application:

bashpython maze_pathfinder.py

🎮 How to Use
Step 1: Create Your Maze

Draw Walls: Select "Wall" mode and click/drag to draw black obstacles
Set Start Point: Select "Start" mode and click to place the green starting position
Set Goal Point: Select "Goal" mode and click to place the red target position
Erase: Select "Erase" mode to remove walls or reset start/goal

Step 2: Choose Algorithm
Select one of the 5 pathfinding algorithms from the dropdown menu.
Step 3: Find Path
Click "Find Path" to watch the algorithm work! Adjust the speed slider to control visualization speed.
Step 4: Analyze Results
View statistics including:

Path length (number of cells)
Optimal path cost (total steps)
Nodes explored
Execution time
Whether the path is optimal

🎨 Color Legend
ColorMeaning🟢 GreenStart position🔴 RedGoal position⬛ BlackWalls/Obstacles🔵 Light BlueVisited cells during search🟡 YellowFinal path found🟠 OrangeCurrent cell (IDA* only)
📊 Understanding the Output
The application provides detailed statistics both in the GUI and console:
============================================================
Algorithm: A*
Result: PATH FOUND
Path Length: 45 cells
Optimal Path Cost: 45 steps
Nodes Explored: 234
Time Taken: 0.156 seconds
Is Optimal: YES
============================================================
🔍 Algorithm Details
BFS (Breadth-First Search)
Explores nodes level by level
Guarantees shortest path in unweighted graphs
Higher memory usage for large mazes

DFS (Depth-First Search)
Explores as far as possible along each branch
Memory efficient (uses stack)
Does NOT guarantee shortest path

A* Search
Uses both actual cost (g) and heuristic estimate (h)
Formula: f(n) = g(n) + h(n)
Optimal and efficient with good heuristic

Best-First Search
Greedy approach using only heuristic
Fast but may find suboptimal paths
Good for quick approximate solutions

IDA* (Iterative Deepening A*)
Combines benefits of A* and iterative deepening
Memory efficient (linear space complexity)
Optimal like A* but uses less memory

🎯 Use Cases
Education: Learn how pathfinding algorithms work visually
Algorithm Comparison: Compare performance of different algorithms
AI/Game Development: Understand pathfinding for game AI
Interview Preparation: Practice graph traversal concepts

🛠️ Technical Details
Grid Size: 25 rows × 40 columns (customizable in code)
Cell Size: 20 pixels
Heuristic: Manhattan distance for A*, Best-First, and IDA*
Movement: 4-directional (up, down, left, right)

📝 Code Structure
MazePathfinder
├── __init__()          # Initialize GUI and settings
├── setup_ui()          # Create interface elements
├── draw_grid()         # Render the maze
├── bfs()               # Breadth-First Search implementation
├── dfs()               # Depth-First Search implementation
├── astar()             # A* Search implementation
├── best_first_search() # Best-First Search implementation
├── ida_star()          # IDA* implementation
└── Helper methods for visualization and path reconstruction
🤝 Contributing
Contributions are welcome! Feel free to:

Report bugs
Suggest new features
Submit pull requests
Improve documentation

🙏 Acknowledgments
Inspired by classic pathfinding visualization tools
Built with Python's Tkinter for cross-platform compatibility
Implements standard graph traversal algorithms from computer science

