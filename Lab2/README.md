# Nim game with evolution strategy (+ and ,) 

## Nim Game
Is a game for two.
It starts with a series of stacks containing a certain number of elements agreed upon at the beginning by the players.

 ![image](https://github.com/Zafonte/computational-intelligence/blob/main/Lab2/readme-images/nim%20.png)

1. Players take turns removing any number of elements from any stack, from one to all, but without changing the other stacks.
2. The player who removes the last element on the playing field loses. 
3. It is not possible to skip the move.

How Nim Game works: https://it.wikipedia.org/wiki/Nim

NOTE: In my case, the player who takes the last element loses

## Lab 2
The goal of the game is to **avoid** taking the last object.

* Task2.1: An agent using fixed rules based on *nim-sum* (i.e., an *expert system*)
* Task2.2: An agent using evolved rules using ES
   
## Task2.1 
I used teaching assistant (code) solution to solve the problem.

## Task2.2 
First, I studied evolutionary algorithms from the book Essentials of Metaheuristics by Sean Luke and the slides provided to me by the professor. 
Then, based on the pseudocodes provided by the book and the *rastrigin* code provided by Professor Squillero I implemented my own solution to the problem.

My idea was to have one of the two players play with the best strategy among proposed lambdas and in particular the choice of the latter have it done through the use of an evolutionary algorithm.
To each strategy I assign a winning percentage and a weight.
My algorithm uses a fitness function to calculate the quality of each action where by quality I meant the player's winning percentage with the use of that specific strategy. 
In addition, the delivery required using Gaussian mutation in order to perform exploration or exploitation, so I used sigma to go in and change the weight assigned to each strategy and specifically a small sigma value if the new solution is close to the old one in terms of "goodness, %win" and a large sigma value vice versa. 

Currently my code does not work, but I am continuing to work on it to figure out what is wrong. 

## (μ,λ) - ES pseudocode
 ![image](https://github.com/Zafonte/computational-intelligence/blob/main/Lab2/readme-images/ES1.png)
 
## (μ+λ) - ES pseudocode
 ![image](https://github.com/Zafonte/computational-intelligence/blob/main/Lab2/readme-images/ES2.png)

