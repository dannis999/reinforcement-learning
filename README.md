# 代码阅读笔记

```python
# DQN
discount_factor = 0.99
learning_rate = 0.001
epsilon = 1.0
epsilon_decay = 0.999
epsilon_min = 0.01
batch_size = 64
train_start = 1000
memory = deque(maxlen=2000)
mini_batch = random.sample(self.memory, batch_size)

# PG
discount_factor = 0.99
learning_rate = 0.001
discounted_rewards -= np.mean(discounted_rewards)
discounted_rewards /= np.std(discounted_rewards)

# A2C
discount_factor = 0.99
actor_lr = 0.001
critic_lr = 0.005

# A3C
actor_lr = 0.001
critic_lr = 0.001
discount_factor = .99
hidden1, self.hidden2 = 24, 24
threads = 8
```

# 原来的 README

<p align="center"><img width="90%" src="images/Reinforcement-Learning.png"></p>

--------------------------------------------------------------------------------

> Minimal and clean examples of reinforcement learning algorithms presented by [RLCode](https://rlcode.github.io) team.
>
> Maintainers - [Woongwon](https://github.com/dnddnjs), [Youngmoo](https://github.com/zzing0907), [Hyeokreal](https://github.com/Hyeokreal), [Uiryeong](https://github.com/wooridle), [Keon](https://github.com/keon)

From the basics to deep reinforcement learning, this repo provides easy-to-read code examples. One file for each algorithm.
Please feel free to create a [Pull Request](https://github.com/rlcode/reinforcement-learning/pulls), or open an [issue](https://github.com/rlcode/reinforcement-learning/issues)!

## Dependencies
1. Python 3.5
2. Tensorflow 1.0.0
3. Keras
4. numpy
5. pandas
6. matplot
7. pillow
8. Skimage
9. h5py

### Install Requirements
```
pip install -r requirements.txt
```

## Table of Contents

**Grid World** - Mastering the basics of reinforcement learning in the simplified world called "Grid World"

- [Policy Iteration](./1-grid-world/1-policy-iteration)
- [Value Iteration](./1-grid-world/2-value-iteration)
- [Monte Carlo](./1-grid-world/3-monte-carlo)
- [SARSA](./1-grid-world/4-sarsa)
- [Q-Learning](./1-grid-world/5-q-learning)
- [Deep SARSA](./1-grid-world/6-deep-sarsa)
- [REINFORCE](./1-grid-world/7-reinforce)

**CartPole** - Applying deep reinforcement learning on basic Cartpole game.

- [Deep Q Network](./2-cartpole/1-dqn)
- [Double Deep Q Network](./2-cartpole/2-double-dqn)
- [Policy Gradient](./2-cartpole/3-reinforce)
- [Actor Critic (A2C)](./2-cartpole/4-actor-critic)
- [Asynchronous Advantage Actor Critic (A3C)](./2-cartpole/5-a3c)

**Atari** - Mastering Atari games with Deep Reinforcement Learning

- **Breakout** - [DQN](./3-atari/1-breakout/breakout_dqn.py), [DDQN](./3-atari/1-breakout/breakout_ddqn.py) [Dueling DDQN](./3-atari/1-breakout/breakout_ddqn.py) [A3C](./3-atari/1-breakout/breakout_a3c.py)
- **Pong** - [Policy Gradient](./3-atari/2-pong/pong_reinforce.py)

**OpenAI GYM** - [WIP]

- Mountain Car - [DQN](./4-gym/1-mountaincar)
