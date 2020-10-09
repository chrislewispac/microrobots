Microrobots Research Project
============================

Contents
------

This repository contains the workproduct of a research project motivated by the board game [Microrobots](https://boardgamegeek.com/boardgame/191543/micro-robots).
 
1. Motivation for Research Problem
2. Rules of the Game
3. Mathematical Model of the Game
   1. The Game as a Graph Problem
      1. What type of graph? Always planar?
      2. Connectedness?
      3. Models of the graph 
         1. embedded/image?
            1. planar?
               1. [Tutte spring embedding](https://en.wikipedia.org/wiki/Tutte_embedding#:~:text=Tutte's%20spring%20theorem%2C%20proven%20by,resulting%20planar%20embedding%20is%20convex.) useful?
               2. [Euler characteristic](https://en.wikipedia.org/wiki/Euler_characteristic#Plane_graphs) useful?
         2. adjacency matrix & eigenvalues/eigenvectors?
            1. [Kirchhoff's Theorem](https://en.wikipedia.org/wiki/Kirchhoff%27s_theorem)
4. Computational methods for answering these questions
   1. Model the board
      1. 4 slots
   2. Model the tiles
      1. 4 tiles
   3. Model the placements of the tiles on the board (slot & rotation)
      1. exactly 1 tile per slot 
      2. 4 independent rotational positions for each tile
   4. Model the nodes on the final board (labelled graph)
      1. Tile
      2. Number 
      3. Color
      4. (x,y) coordinate
   5. Model the edges on the final board
      1. if on the same x or y axis AND 
      2. same number OR same color
   6. Compute the connectedness (efficiency matter for this purpose?)
      1. DFS? spanning tree
      2. You can find the [Laplacian matrix of the graph](https://math.uchicago.edu/~may/REU2013/REUPapers/Marsden.pdf) and check the multiplicity of eigenvalue zero of the Laplacian matrix, if the multiplicity of zero is one then graph is connected, if multiplicity of eigenvalue zero of Laplacian matrix of the graph is two or more then it is disconnected
   7. Compute the "sameness" in context of the rules of the game.
5. Abstractions, Open Questions, & Future Investigation
   1. Do these findings hold generally?
      1. e.g. a connected planar graph, embedded in the plane, always has 4 sub graphs with the following characteristics.
      2. e.g. to form a connected planar graph of three subgraphs with the following constraints each sub graph must have the following characteristics.