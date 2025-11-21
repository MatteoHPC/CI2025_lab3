# CI2025_lab3

## SHORTEST PATH

This is the problem presentation.

Given a list of cities and their relative distances, find the shortest possible route between all possible pairs of cities.

## PROBLEM CREATOR

The problem creator the professor supplied to us needs the following parameters:

***
    negative_values = [False, True]
    noise_level = [0, 0.1, 0.5, 0.8]
    density = [0.2, 0.5, 0.8, 1]
    size = [10, 20, 50, 100, 200, 500, 1000]
***

So we have to loop over each combination of these.

## REPOSITORY STRUCTURE

This is the README, the entry point that explains what is done.

The file *"shortest_path.ipynb"* is a notebook that contains the code to solve the problem for all parameter settings. For each possible parameter combination it creates the problem instance and solves the problem. With a fixed seed, the problem instances will always be the same for each parameter setting in the loop.

## SOLVING ALGORITHM

The algorithm to solve the problem is **A*** with **minimum edge heuristic**

It also avoids negative loops.

### A* Algorithm Implementation:

A* is an informed search algorithm that combines the actual cost from the start node (g-score) with a heuristic estimate to the goal (h-score) to efficiently find the optimal path. The algorithm maintains a priority queue of nodes to explore, always expanding the node with the lowest f-score = g-score + h-score.

The heuristic function uses the minimum edge weight in the entire graph as a lower bound estimate for reaching any goal node.

The implemented algorithm will be compared against NetworkX's Bellman-Ford algorithm as a reference to validate correctness, especially for problem instances with negative edge weights.

## FINAL NOTES

Notebook and report (README) were written by Matteo Zito, with the support of OpenAI's GPT-5 model, used only as a programming assistant.


