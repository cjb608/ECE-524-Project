# ECE-524-Project
Project repository for ECE 524 Spring 2022: Optimal Scientific Victory Path for Civilization VI

This repository contains a solution to an optimazation problem inspired by the popular turn based strategy game Civilization VI. It was designed and implemented in Julia using JuMP and Gurobi.

Civilization VI is a popular strategic game where each player's goal is to achieve victory through various paths (domination, scientific, diplomatic, etc.) Replicating every single detail in the game is indeed challenging given the scale of the game. Therefore, this project focuses on the scientific victory path and finds the optimal path through the technology tree.

In the baseline model, each technology in the tree costs science to research, and the player receives a certain amount of science per turn which they can contribute to researching one technology at a time. The tech tree represents the prerequisites for each technology. In other words, in order to research a technology the player must have researched all parent technologies in the tech tree. Also, players may choose to use production to construct research buildings to generate more science per turn, and each research building is unlocked by certain technologies.

For players to win a science victory, they must launch: a satellite, a moon landing, and a mars colony - each of which has an associated technology to research in the tech tree. Thus, the objective of this optimization problem is to find the optimal path through the tech tree that allows the players to complete research for and launch each of the victory requirements at the earliest possible turn. By transforming a rather complex game setting to an optimization model, our group hopes to offer players a new perspective on improving the chance of achieving a scientific victory.

The project is organized as follows: First a baseline mathematical model as well as the alternative model with more variables and assumptions closer to the real game are defined. Next the necessary data is obtained via a web scraping script writen in python. After the data is gathered, a solution to each model is presented. Finally, the results from the optimization model and their implications as discussed in detail.
