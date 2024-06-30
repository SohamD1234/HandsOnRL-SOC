For Week 3, we will be looking at two classes of algorithms to deal with prediction and control problems, when we don't know the model of the environment :
1: Monte Carlo Methods
2: Temporal Difference Learning
The primary reading material for this week will be Chapters 5 and 6 of Grokking DRL. Also, if you are interested in a more theoretical approach, you may also refer to chapters 5 and 6 from Sutton and Barto and additionally chapter 7 for Eligibility Traces, which acts as a bridge between these two classes of algorithms.

# Week 3

In this week and the next, we shall properly learn about Multiarmed Bandits and Finite Markov Decision Processes.

Your mission, should you choose to accept it is as follows:

## Assignment-1

For your assignment you have to implement some policies for the MultiArmed Bandit problem.

The file structure:

* `bandits.py` contains the class for the bandit. You do not need to edit this unless you want to add input formats, for eg. batchwise. Currently implemented two types of distribution for bandit arms:
  * `"Bernoulli"` : Returns a reward of 1 with fixed probabilities.

  * `"Gaussian"` : Returns reward from a Gaussian Distribution with fixed mean (dependent on the arm) and `variance=1`.

    The class `Bandit` also keeps tract of $\text{regret} = k \cdot \text{optimal-reward} - \sum R_t$ which can be accessed at any timestamp using `get_regret()` function.

    Note that for Thompson sampling the Beta Distribution (```np.random.beta```) is the conjugate prior for a Bernoulli Distribution.

* `agents.py` contains the class for agents and sub classes for each policy type. You only need to implement the subclasses (again, unless you want to add something or fix bugs).

* `results.py` show us your results -> train the algorithms and plot the graphs. Be creative.
