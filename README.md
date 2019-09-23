# MADDPG

This is a pytorch implementation of MADDPG on [Multi-Agent Particle Environment(MPE)](https://github.com/openai/multiagent-particle-envs), the corresponding paper of MADDPG is [Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments](https://arxiv.org/abs/1706.02275).

## Requirements

- python=3.6.5
- [Multi-Agent Particle Environment(MPE)](https://github.com/openai/multiagent-particle-envs)
- torch=1.1.0

## Quick Start

```shell
$ python main.py ----scenario-name=simple_tag evaluate-episodes=10
```

Directly run the main.py, then the algrithm will be tested on scenario 'simple_tag' for 10 episodes, using the pretrained model.

## Note

We have train the agent on scenario 'simple_tag', but the model we provide is not the best because we don't want to waste time on training, you can keep training it for better performence.

The default setting of Multi-Agent Particle Environment(MPE) is sparse reward, you can change it to dense reward by replacing 'shape=False' to 'shape=True' in multiagent-particle-envs/multiagent/scenarios/simple_tag.py/adversary_reward().