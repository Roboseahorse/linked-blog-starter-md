## Do Now

> [!QUESTION]- I parked my car at work. It breaks down. What do I do?
> Identify the problem, check simple causes first, then arrange breakdown assistance or a garage if needed.
> Use a logical step-by-step approach rather than trying random solutions.

## Problem Solving Techniques

Problem solving in computer science uses different techniques to make difficult problems easier to understand and solve.

### Visualisation

**Visualisation** represents a problem or algorithm visually, such as with a [[Flowchart]] or graph.

- Often easier to understand than raw data or a table of numbers.
- Graphs use **nodes** and **edges**, with weights representing values such as distance or cost.

> [!NOTE] Key Idea
> Visualisation helps you see relationships, routes and stages in a problem more clearly.

### Euclid's GCD Algorithm

Euclid's algorithm finds the **greatest common divisor (GCD)**, the largest integer that divides two numbers exactly.

```text
r = 1
WHILE r <> 0
    r = x mod y
    x = y
    y = r
ENDWHILE
OUTPUT x
```

For `x = 420` and `y = 66`, the GCD is **6**.

| r | x | y |
|---:|---:|---:|
| 1 | 420 | 66 |
| 24 | 66 | 24 |
| 18 | 24 | 18 |
| 6 | 18 | 6 |
| 0 | 6 | 0 |

## Searching for Solutions

### Exhaustive Search

An **exhaustive search** tries every possible solution until the best or correct one is found.

- It can work well for small problems.
- The number of possibilities can increase very quickly as the problem grows.
- This can make exhaustive search impractical for large problems.

### Backtracking

**Backtracking** explores a possible route, then goes back when it reaches a dead end or finds a route that isn't useful.

- Commonly used with [[Depth-First Search]].
- Useful for mazes, graphs and route-finding problems.
- It avoids continuing down paths that won't lead to a useful solution.

> [!IMPORTANT] Example
> In a maze, follow one path until a dead end is reached. Then return to the previous choice and try another path.

## Heuristic Methods

A **heuristic** is a rule of thumb, educated guess or practical method used to find a good solution quickly.

- It doesn't guarantee the optimal solution.
- It's useful when checking every possible solution would take too long.
- Examples include routing, transportation, circuit design, virus checking, DNA analysis and [[Artificial Intelligence]].

### Travelling Salesman Problem

The [[Travelling Salesman Problem]] asks for the shortest route that visits every required city and returns to the start.

A heuristic can find a **good enough** route much faster than testing every possible route.

## Data Mining

**Data mining** is the process of analysing large amounts of data to discover patterns, connections and associations.

Common uses include:

- Targeted marketing.
- Predicting resource demands.
- Detecting fraud and cybersecurity issues.
- Finding connections between apparently unrelated events.

### Big Data

**Big data** describes extremely large or complex datasets. It is commonly described using the **3 Vs**:

| V | Meaning |
|---|---|
| **Volume** | The amount of data |
| **Variety** | Different forms and types of data |
| **Velocity** | The speed at which data is generated and processed |

[[Parallel Computing]] can help process big-data tasks by running work concurrently across multiple processors or computers.

## Performance Modelling

**Performance modelling** considers how efficient an algorithm is.

- [[Big O Notation]] describes how execution time or memory requirements grow as the problem size increases.
- Algorithms can also be compared by timing their execution.
- Some algorithms become impractically slow as the input size grows.

> [!NOTE]
> Choosing an algorithm isn't only about getting the correct result. Its time and space requirements also matter.

## Pipelining

**Pipelining** overlaps the execution of multiple instructions.

- An instruction moves through several processing stages.
- When it moves to the next stage, another instruction can enter the pipeline.
- This is similar to an assembly line and improves processor throughput.

## Exam Summary

| Technique | Main idea |
|---|---|
| **Visualisation** | Represent a problem visually to make it easier to understand |
| **Backtracking** | Explore a path, then return and try another if necessary |
| **Heuristics** | Quickly find a good solution without guaranteeing the best one |
| **Data mining** | Analyse large datasets to identify useful patterns |
| **Performance modelling** | Assess the time and space efficiency of algorithms |
| **Pipelining** | Overlap instruction stages to improve processor throughput |

## Self-Check

> [!QUESTION]- What is backtracking?
> Exploring a route and returning to an earlier point when the route fails or a better option needs to be tried.

> [!QUESTION]- Why are heuristics useful?
> They can find a good solution quickly when testing every possible solution would take too long.

> [!QUESTION]- What are the 3 Vs of big data?
> **Volume, Variety and Velocity.**

> [!QUESTION]- What does performance modelling help assess?
> How efficiently an algorithm uses execution time and memory as the problem size changes.

## Related Notes

- [[Algorithms]]
- [[Big O Notation]]
- [[Graphs]]
- [[Depth-First Search]]
- [[Parallel Computing]]
- [[Artificial Intelligence]]
