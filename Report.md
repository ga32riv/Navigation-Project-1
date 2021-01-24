[//]: # (Image References)

[image1]: https://github.com/ga32riv/Navigation-Project-1/blob/main/Score%20plot.png "Score plot"

# Report

## Algorithm

### NN Model Architecture
The used Neural Network has 3 fully connected layers usin ReLu activation function as follows:

- Fully connected layer - input (state size): 37; output: 64
- Fully connected layer - input: 64; output: 64
- Fully connected layer - input: 64; output (action size): 4

### Used Parameters

    BUFFER_SIZE = int(1e5)  # replay buffer size
    BATCH_SIZE = 64         # minibatch size
    GAMMA = 0.99            # discount factor
    TAU = 1e-3              # for soft update of target parameters
    LR = 5e-4               # learning rate 
    UPDATE_EVERY = 4        # how often to update the network

    eps_start=1.0, eps_end=0.01, eps_decay=0.995
    eps = max(eps_end, eps_decay*eps) # decreasing epsilon

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

Implementing/adding other algorithms such as:
- double DQN
- dueling DQN
- prioritized experience replay!
