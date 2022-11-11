## Authors

- [@NadimSalameh](https://github.com/NadimSalameh)


# 🎯 The Goal of the Game

- You have managed to find Blunder. His circuits are programmed with an algorithm which has made him lose all sense of humor or fun. You decide to return his system to his original behavior.

- The first trait of character that you are going to work on is his passion for money. Blunder can detect bank notes several miles away.

- Your objective is to write a program that will lead him to always find the most money possible, wherever it is.

# 	✔️ Rules

- To check that your algorithm works properly, Blunder is placed in a room at the entrance of a building. There is a sum of money in each of the rooms that make up this building. Each room has exactly two doors which you can use to get out. Each door leads either to a new room or to the outside of the building.

- Blunder must collect as much money as possible, by going from room to room, without being able to go back, until he gets out of the building. Thanks to his sensors, Blunder can analyze the building right from the outset in order to detect the list of rooms and the money contained in each of them. This analysis of the rooms will be provided as input for your program so that you can implement an algorithm that will make the best decisions.

- Each room in the building has a unique number. Each door of a room is marked with a number, which represents the number of the room that it opens, or E if it opens to the outside of the building. Several doors can lead to one room but due to the layout of the building it is impossible for Blunder to go through the same room twice. Some doors open in one direction only.

- The first room in which Blunder finds himself has the number 0.

# 🎦 Example 
![In this example, Blunder pockets $40 by going through the rooms 0, 2, 3 and 5 before leaving the building.](https://github.com/NadimSalameh/Blunder-Codingame/blob/main/Bender2-example.png)
* In this example, Blunder pockets $40 by going through the rooms 0, 2, 3 and 5 before leaving the building.
# 🔴Game Input and Output
# Input

*Line 1*: the number N of rooms in the building.

*N following lines*: one line with a room number (integer), a sum of money (integer), the two numbers of the rooms which are accessible (integers or E if the door is an exit). These four values are separated by a white space.

# Output 
An integer representing the maximum amount of money that Blunder can collect by taking a series of doors to reach the outside of the building.

# ⚠️ Constraints
0 < N < 10000




# Approach to solve the problem

In this puzzle,I implemented a pathfinding algorithm, where the goal is not the shortest path but maximizing earnings. I represented the bulding as a tree of rooms. Each room has a number, money, doors and depth in the tree. I calculated the maximum depth of each room reachable from the start with [DFS](https://en.wikipedia.org/wiki/Depth-first_search).  I Find the path with the max total money using a modifed version of [Dijkstra's algorithm](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm), prioritizing the room with the highest depth.

# Run the Code

You can run the code by downloading the repository:

- Click the green "clone or download repository" button on the top right of the repository.
- In order to clone, you will need to have git installed on your computer. Then run these commands:
```console
1.git clone URL (The URL of repo you can copy it by clicking on the green 
button on the top right then copy URl)
2.python Game.py (Be sure you are in the right directory)

```
or simply you can copy the code and past it in your jupyter notebook or VS code then run it.
* After runing the python file you have to enter the inputs mentionned above.
# Example for input:
5 (First input the number of rooms)

0 15 1 2 *(0: number(index) of the room, 15: $15 amount of money,1 and 2 are the number of accessible rooms)*

1 18 3 4 

2 19 E E (E: Exit the building)

3 45 E E

4 50 E E

*ouput*:
83 
## Technology and Tools

* Python

* VS code

* [Dijkstra's algorithm](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)

* [DFS](https://en.wikipedia.org/wiki/Depth-first_search)

* [PathFinding](https://en.wikipedia.org/wiki/Pathfinding)

* [Memoization](https://en.wikipedia.org/wiki/Memoization)

* [Dynamic_programming](https://en.wikipedia.org/wiki/Dynamic_programming)

* [Recursion](https://en.wikipedia.org/wiki/Recursion)
