# CartPole Environment

This environment is part of the Classic Control environments which contains general information about the environment.

## Task

The agent has to decide between two actions - moving the cart left or right - so that the pole attached to it stays upright. You can find more information about the environment and other more challenging environments at [Gymnasium's website](https://gymnasium.farama.org/environments/classic_control/cart_pole/).

### CartPole

As the agent observes the current state of the environment and chooses an action, the environment *transitions* to a new state, and also returns a reward that indicates the consequences of the action. In this task, rewards are +1 for every incremental timestep and the environment terminates if the pole falls over too far or the cart moves more than 2.4 units away from center. This means better performing scenarios will run for longer duration, accumulating larger return.

The CartPole task is designed so that the inputs to the agent are 4 real values representing the environment state (position, velocity, etc.). We take these 4 inputs without any scaling and pass them through a small fully-connected network with 2 outputs, one for each action. The network is trained to predict the expected value for each action, given the input state. The action with the highest expected value is then chosen.

## Packages

First, let's import needed packages. Firstly, we need [Gymnasium](https://gymnasium.farama.org/) for the environment, installed by using `pip`. This is a fork of the original OpenAI Gym project and maintained by the same team since Gym v0.19.
