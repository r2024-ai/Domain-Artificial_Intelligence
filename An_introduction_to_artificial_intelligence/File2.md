# Uninformed Search

Chapter 3
(Based on slides by Stuart Russell, Subbarao Kambhampati,
Dan Weld, Oren Etzioni, Henry Kautz, Richard Korf, and
other UVV-AI faculty)

## What is a State?
* All information about the environment
* All information necessary to make a decision for the task at hand.
## Agent's Knowledge Representation

|Type|State representation|Focus|
|--|--|--|
|Atomic|States are indivisible; No internal structure|Search|
|Propositional(aka factored)|States are made of state variables that take values(Propositional or Multivalued or Continuous)|Search+Inferencein logical (Prop logic) and probabilistic (bayes nets) representations|
|Relational|States describe the objects in the world and their inter-relations|Search+Inference in predicate logic (or relational prob. Models)|
|First-order|+functions over objects|Search+lnference in first order logic (or first order probabilistic models)|


![alt text](image-30.png)

## Atomic Agent
* Input
    * Set of States
    * Operators[and costs]
    * Start state
    * Goal state[test]
* Output
    * Path: start => a state satisfying goal test
    * [May require shortest path]

## Example - The 8-puzzle
![alt text](image-31.png)

* States? locations of tiles
* actions? move blank left, right, up down
* goal test? = goal state(given)
* path cost? 1 per move

* [Note : optimal solution of n-Puzzle family is NP-hard]

![alt text](image-32.png)

![alt text](image-33.png)

## Example - Romania
* On holiday in Romania; currently in Arad.
* Flight leaves tomorrow from Bucharest
* Formulate goal:
    * be in Bucharest
* Formulate problem:
    * states: various cities
    * actions: drive between cities
* Find solution:
    * sequence of cities, e.g., Arad, Sibiu, Fagaras, Bucharest

## Example - N Queens

![alt text](image-34.png)

## Implementation - states vs nodes
![alt text](image-35.png)