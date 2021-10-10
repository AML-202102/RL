# Reinforcement Learning Homework

## Part 1: Basic Q-learning using Frozen Lake environment (2.5 points)

OpenAI created a library called [gym](https://gym.openai.com/envs/#classic_control), which provides several environments to visualize the result of your reinforcement learning algorithms. In this part, you will use the Frozen Lake environment. For better visualization, this part must be run on Jupyter as we provide a Jupyter Notebook. The updated Jupyter Notebook must be submitted to the repository before October, 25th. 

### Initialization

  1) Initialize the Q-table so that you get a matrix of 0 with the correct dimensions.
  2) Explain, in this environment, what would be an episode and why do we use the parameter max_steps_per_episode. 

### Exploration vs Exploitation

  1) Implement the exploitation action in case your threshold is greater than the exploration rate. 
  2) Explain how the trade-off between exploration and exploitation evolves through episodes. 

### Baseline results 

Run every cell of your code and visualize what is happening. Can you reach the frisbee? 

Add your final Q-table to your report and explain the different values (some close to 0, others closer to 1).

### Experiments 

You will work on the 3 following parameters: learning_rate, discount_rate, exploration_decay_rate. Choose 2 other values than the one already implemented in the baseline for each parameter and perform a search grid ( you must get 9 experiments at the end). Add your results to the report, discuss your value choices and conclude about the best parameters combination. 

## Part 2 : Deep Q-Network using CartPole environment (2.5 points)

The CartPole environment is also provided by the gym library. The aim is to keep the pole as verticale as possible by moving right or left. If the pole reach an angle bigger than 15° or -15° the episode is over. The objective of the game is to reach 195 moves in one episode, which means keeping the pole in the [-15°;15°] range for 195 moves. 

In order to run your scripts correctly, you should create a conda environment and download the following libraries. 

    #Setup
    conda create --name RL
    conda activate RL
    conda install python==3.9
    conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch
    pip install matplotlib
    pip install gym
    pip install pyglet
    
Start by reading the script carrefuly. You may not understand everything but you should recognize some concepts discussed in class (ReplayMemory, Agent, EpsilonGreedyStrategy, QValues) and the training loop process. 

### Initialization

  1) We know that Deep Q-Network takes images as input, therefore add the correct input dimensions to the script in the DQN class. 
  2) Before running the baseline, you must choose the correct network to use in the get_current and get_next functions of the QValues class. According to your choice, you must also remplace the "None" in the training loop. 

Now, you can run the baseline and visualize your algorithm learning how to keep the pole verticale. You must add the final plot to your report and discuss you result. Explain why the average line is 0 until 100 episodes. 

#Acknowledgment

