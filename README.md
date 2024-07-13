## Genetic Algorithm for Solving Quadratic Equation
### Overview
this project demonstrates a genetic algorithm approach to find a solution for a quadratic equation x^2+9x+18. The algorithm implies techniques such as initialization, selection, crossover, mutation, and fitness evaluation to evolve a population of potential solutions.

### Usage
To run the genetic algorithm, execute the main script geneticalgo.ipynb. Ensure Python 3.x is installed on your system.

### Parameters
  CHROMOSOME_LENGTH: Total length of each chromosome .
  
  POPULATION_SIZE: Number of chromosomes in the population .

  MUTATION_RATE: Probability of mutation for each bit in an offspring .
  
  MAX_GENERATIONS: Maximum number of generations before termination .

## Fitness Function
The fitness function used in this implementation is defined as:

##### fitness_function(x):
    return abs(1*x**2 + 9*x + 18)
## Key Components
### Chromosome Representation:
Each chromosome is represented as an 8-bit binary string:

3 bits for the integer part.
5 bits for the fractional part.
### Fitness Function: 
Evaluates how well each chromosome's decoded value solves the quadratic equation. Fitness is based on minimizing the absolute difference between the equation's value at the decoded 
𝑥
x and zero.

### Initialization: 
Generates an initial population of chromosomes randomly.

### Selection:
Tournament selection is used to choose parents based on their fitness for reproduction.

### Crossover: 
Uniform crossover is applied to create offspring by randomly selecting bits from two parents.

### Mutation: 
Introduces variability by randomly flipping bits in offspring chromosomes. The mutation rate is set to 10% (MUTATION_RATE = 0.1).

### Termination: 
The algorithm terminates after a maximum of 10 generations (MAX_GENERATIONS = 10) or when a satisfactory solution is found.

### Genetic Algorithm Execution
The genetic algorithm (genetic_algorithm function) orchestrates the iterative process of selection, crossover, mutation, and fitness evaluation over multiple generations to find the optimal solution.
