# final-project: Terrain Generator Using Cellular Automata
Description: A cellular atomata based terrain generator that cretes cavelike or island structures by applying smoothing rules to a random noise grid. 

- I will use a Cell class that represents a unit of terrain, either wall or empty space.
- I will also use a 2D grid of Cell objects to represent the entire map.
- Terrain evolves over multiple generations, or steps of the automaton, based on the states of neighboring cells. 

Variables + Data Structures:
- grid: 2D array of cell objects representing the current terrain state.
- Collumns, Rows: dimensions of the grid.
- initialWallProbability: the chance that a given cell starts as a wall.
- steps: number of cellular automata passes to smooth the terrain.
- neighborsToSurvive: number of wall neighbors for a cell to stay/become a wall

I will create a grid of 400x400. Randomly assign each cell to be a wall or space based on initialWallProbability. 
I will run "steps" generations of the automaton to refine the terrain. 

the terrain grid will be black for walls, white for space. 

Classes:
cell properties: 
- x,y: position on the grid
- isWall: true if its a wall, false if not.
methods:
- display(): draws the cell
- countWallNeighbors(grid): returns the number of adjacent walls (including diagonals)

Smoothing
- for each cell: if the number of neighboring wall cells is greater than 4, the cell becomes a wall, otherwise the cell becomes empty. 
