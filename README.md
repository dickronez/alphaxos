# AlphaXos

### Self play with Deep Reinforcement Learning: Deep Q-Learning using Xs and Os in an Open AI Gym-like Environment

What?
- Concise working example of self-play Deep Q-Learning
- You may find it a useful example in discussing and understanding Alpha Zero / AlphaGo Zero (AZ/AGZ)
- Environment similar to those in OpenAI gym at gym/envs/toy_text/ 

Agents:
- ChaosAgent: Same as DQNAgent, but Epsilon-greedy during play (not just during training)
- DQNAgent: Double-Deep Q-Learning agent trained with keras-rl
- RandomAgent: always plays a random (but valid) move
- HumanAgent: takes keyboard input

### Comparison with AlphaZero / AlphaGo Zero

Similar to AZ/AGZ:
- reinforcement learning for a binary board game
- game state represented via board input matrix
- uses single neural network, instead of separate policy and value networks like earlier AlphaGos
- learns entirely from self-play (in the case of AlphaXos, also learns from play against purely random player, as well as self-play)
- no human-engineered features or logic

Different from AZ/AGZ:
- uses Deep Q Learning (as opposed to the Monte Carlo Tree Search variation of Policy Improvement used by AZ/AGZ)
- AGZ used rotated/reflected board positions to increase sample efficiency.  AZ does not do this.  AlphaXos does not currently do this.
- uses a shallow keras FF network (instead of a deep residual network in the case of AGZ; it is not clear what architecture was used for AZ)
- uses single 2D matrix for representing board including both players, instead of a multi-layer matrix like AZ/AGZ
- adjusts representation of board depending on turn side, as opposed to AGZ which provides turn side as input to the network
- probably many other things!

### Next steps

- lots

### References

- Alpha Zero: https://arxiv.org/abs/1712.01815
- AlphaGo Zero: https://deepmind.com/documents/119/agz_unformatted_nature.pdf
- OpenAI gym: https://github.com/openai/gym/
- Keras-RL: https://github.com/keras-rl/keras-rl
- Keras: https://keras.io/
- DQNs: https://www.nature.com/articles/nature14236

Copyright (c) 2018 Robin Chauhan

License: The MIT License
