[//]: # (Image References)

[image1]: https://github.com/ga32riv/Navigation-Project-1/blob/main/Score%20plot.png "Score plot"

# Report

Deep Reinforcement Learning nanodegree (Udacity)

Project 1: Navigation

## Algorithm

The agent was trained using a simple deep Q-learning algorithm from this [paper](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf), where the Q-function is estimated using a deep neural network. Unlike in the paper where convolutional layers were used with raw pixels as input, a fully connected layer was used in our case. The algorithm also includes experience replay and fixed Q targets.


### NN Model Architecture
The used Neural Network has 3 fully connected layers using ReLu activation function as follows:

- Fully connected layer - input (state size): 37 - output: 64
- Fully connected layer - input: 64 - output: 64
- Fully connected layer - input: 64 - output (action size): 4

### Used Parameters

    BUFFER_SIZE = int(1e5)  # replay buffer size
    BATCH_SIZE = 64         # minibatch size
    GAMMA = 0.99            # discount factor (agent only cares only about if immediate rewards if GAMMA = 0)
    TAU = 1e-3              # for soft update of target parameters
    LR = 5e-4               # learning rate 
    UPDATE_EVERY = 4        # how often to update the network

    eps_start=1.0, eps_end=0.01, eps_decay=0.995
    eps = max(eps_end, eps_decay*eps) # decreasing epsilon (eps = 0, the agent always selects a greedy action)

## Results
```
Episode 100	Average Score: 1.37
Episode 200	Average Score: 4.83
Episode 300	Average Score: 8.05
Episode 400	Average Score: 11.01
Episode 500	Average Score: 12.58
Episode 543	Average Score: 13.04
Environment solved in 443 episodes!	Average Score: 13.04
```
![Score plot][image1]

## Ideas for Future Work

Try to get better results by implementing algorithms such as:
- Double DQN
- Dueling DQN
- Prioritized experience replay
- Rainbow
