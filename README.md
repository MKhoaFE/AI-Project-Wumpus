Wumpus World
1. Overview

A Python simulation of Wumpus World, where a human or AI agent solves the map based on gathered knowledge.

Language: Python 3

Libraries: PyGame (or Tkinter) for GUI

IDE: VSCode / PyCharm
-------------------------------------

2. How to Run
python main.py <mode> <arguments>


random: Generate a 10x10 random map

python main.py random <row> <col> <pits> <wumpus> <gold>
# Example:
python main.py random 0 0 7 7 7


file: Load a map from maps/ folder

python main.py file <filename>
# Example:
python main.py file original.txt


When running, you’ll see two buttons:

STEP: Move agent step-by-step

RUN ALL: Let agent solve the whole map (pause with STEP)
-------------------------------------

3. Main Components

Map & Tile: Store pit, wumpus, gold, breeze, stench, agent position.

GameState: Track visited, safe tiles, and previous states.

Agent:

Uses Knowledge Base + PL-Resolution (CNF) to detect safe/danger tiles.

Moves via safe node list; pathfinding with UCS.

Shoots wumpus when position is certain.

GUI: Renders the world, processes actions from agent or player.

4. Notes & Limitations

PL-Resolution is computationally heavy; late-game reasoning is slower.

Tried local search optimization, but kept original method for completeness.

5. References
- [Github_1](https://github.com/malea/hunt-the-wumpus)
- [Github_2](https://github.com/khamkarajinkya/Agent-for-wumpus-world)
- [Github_3](https://github.com/bsmorton/Wumpus-World-Python)