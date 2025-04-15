A* Pathfinding Visualizer in Python

🚀 Introduction

 This project is a Python-based visualizer for the A* (A-star) pathfinding algorithm built using Pygame. It allows users to interactively place start and end points, draw obstacles, and watch in real-time how A* finds the shortest path on a grid.
Whether you're learning about graph algorithms or just enjoy visualizing how intelligent routing works, this tool provides a clean and intuitive way to see A in action*.

📊 Algorithm Explanation

A (A-star)* is a widely used pathfinding and graph traversal algorithm, popular in many fields like AI, games, and robotics. It aims to find the shortest path from a start node to an end node while avoiding obstacles (barriers) using the formula:

f(n) = g(n) + h(n)

Where:

•	g(n) is the cost to reach node n from the start node.

•	h(n) is the heuristic estimate of the cost to reach the goal from node n.

In this implementation, we use Manhattan Distance as the heuristic h(n).


🛠️ Implementation in Brief

✅ Features:

•	Interactive grid setup via mouse

•	Left-click to:

o	Set start point (Orange)

o	Set end point (Green)

o	Add barriers (Black)

•	Right-click to erase

•	Press SPACE to start the algorithm

•	Live visualization of:

o	Open set (Red)

o	Closed set (Turquoise)

o	Final path (Purple)

🔧 Tech Stack:

•	Python 3

•	Pygame for UI and drawing

•	Priority Queue for open set tracking

🧱 Grid Logic:

Each tile (or "spot") on the grid is an object storing:

•	Its position

•	Color (status)

•	List of neighboring spots

•	Methods to update status or reset


📈 A* Algorithm Flow



•	A[Start Node] --> B{Open Set Not Empty?}

•	B -- Yes --> C[Choose Node with Lowest f(n)]

•	C --> D{Is Goal Node?}

•	D -- Yes --> E[Reconstruct Path and Exit]

•	D -- No --> F[For Each Neighbor]

•	F --> G{Is Path Better?}

•	G -- Yes --> H[Update g(n), f(n), and came_from]

•	H --> I[Add to Open Set if not present]

•	I --> B

•	G -- No --> B

•	B -- No --> J[No Path Found]



🧠 Future Ideas

•	Add diagonal movement support

•	Add more algorithms (Dijkstra, BFS, DFS)

•	Customizable grid weights

•	Dynamic Obstacle Handling 


This project was created as a learning project to deeply understand A* and Pygame, and also to provide an intuitive tool for others to visualize pathfinding logic.



