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
