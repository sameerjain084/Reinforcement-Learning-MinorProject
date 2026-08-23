# Reinforcement Learning -- Flappy Bird

A Deep Reinforcement Learning project that uses a **Deep Q-Network
(DQN)** to train an agent to play **Flappy Bird**.

The project demonstrates core reinforcement learning concepts such as
**experience replay, Q-learning, neural networks, exploration
vs. exploitation, and model training**.

## 📌 Project Overview

The goal of this project is to train an AI agent that learns to play
Flappy Bird through interaction with the game environment.

Instead of being given the correct actions, the agent learns by:

1.  Observing the current game state.
2.  Choosing an action such as jumping or doing nothing.
3.  Receiving a reward or penalty.
4.  Storing the experience in a replay memory.
5.  Sampling previous experiences to train the DQN.
6.  Gradually improving its gameplay through repeated training.

## 🧠 Reinforcement Learning Approach

This project uses a **Deep Q-Network (DQN)**.

The agent estimates the value of possible actions using a neural
network:

**Q(state, action) → expected future reward**

The agent uses an **epsilon-greedy strategy** to balance:

-   **Exploration** -- trying different actions.
-   **Exploitation** -- choosing the action currently believed to be
    best.

Experience replay is used to make training more stable by storing
previous experiences and training on randomly sampled batches.

## 📂 Project Structure

``` text
Reinforcement-Learning-MinorProject/
│
├── agent.py
├── dqn.py
├── experience_replay.py
├── game_flappy_bird.py
├── parameters.yaml
├── .gitignore
└── README.md
```

### Files

  -----------------------------------------------------------------------
  File                                Purpose
  ----------------------------------- -----------------------------------
  `agent.py`                          Contains the reinforcement learning
                                      agent and its decision/training
                                      logic.

  `dqn.py`                            Defines the Deep Q-Network used to
                                      estimate action values.

  `experience_replay.py`              Implements replay memory for
                                      storing and sampling past
                                      experiences.

  `game_flappy_bird.py`               Contains the Flappy Bird
                                      game/environment used for training
                                      and interaction.

  `parameters.yaml`                   Stores configurable training/model
                                      parameters.

  `.gitignore`                        Prevents generated files, caches,
                                      logs, and local environment files
                                      from being committed.
  -----------------------------------------------------------------------

## 🔄 Training Workflow

``` text
        ┌─────────────────┐
        │  Flappy Bird    │
        │   Environment   │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │  Observe State  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │   DQN Agent     │
        │ Choose Action   │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Environment     │
        │ gives Reward    │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Experience      │
        │ Replay Memory   │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Sample Batch &   │
        │ Train DQN       │
        └────────┬────────┘
                 │
                 └──────► Repeat
```

## ⚙️ Requirements

Make sure Python is installed.

Recommended:

-   Python 3.9+
-   PyTorch
-   NumPy
-   PyYAML
-   Pygame

Install the dependencies with:

``` bash
pip install torch numpy pyyaml pygame
```

If the project contains a `requirements.txt` file in the future,
dependencies can instead be installed with:

``` bash
pip install -r requirements.txt
```

## ▶️ Running the Project

Clone the repository:

``` bash
git clone <your-repository-url>
cd Reinforcement-Learning-MinorProject
```

Install dependencies:

``` bash
pip install torch numpy pyyaml pygame
```

Then run the main game/training script:

``` bash
python game_flappy_bird.py
```

> If your project uses a different file as the training entry point, run
> that file instead.

## 📊 Training

During training, the agent repeatedly interacts with the environment.

A typical learning cycle is:

``` text
State
  ↓
Select Action
  ↓
Take Action
  ↓
Receive Reward
  ↓
Store Experience
  ↓
Sample Replay Batch
  ↓
Update Neural Network
  ↓
Repeat
```

The training configuration can be adjusted through `parameters.yaml`.

## 🛠️ Technologies Used

-   **Python**
-   **PyTorch**
-   **NumPy**
-   **Pygame**
-   **PyYAML**
-   **Deep Q-Learning (DQN)**
-   **Experience Replay**
-   **Epsilon-Greedy Exploration**

## 🎯 Learning Objectives

This project was developed to understand and implement:

-   Reinforcement Learning fundamentals
-   Markov Decision Processes
-   Q-Learning
-   Deep Q-Networks
-   Experience Replay
-   Exploration vs. Exploitation
-   Reward-based learning
-   Neural-network-based action selection
-   Training an autonomous game-playing agent

## 🚀 Future Improvements

Possible improvements include:

-   Add a target network for more stable DQN training.
-   Add model checkpoint saving and loading.
-   Visualize training performance using TensorBoard.
-   Plot rewards and scores across episodes.
-   Tune hyperparameters automatically.
-   Compare DQN with Double DQN or Dueling DQN.
-   Add evaluation mode for the trained agent.
-   Improve the state representation and reward function.

## 👨‍💻 Author

**Sameer Jain**

B.Tech -- Computer Science Engineering\
Cloud Computing & Automation\
VIT Bhopal University

------------------------------------------------------------------------

⭐ If you found this project useful, consider giving the repository a
star!
