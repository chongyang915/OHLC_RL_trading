# OHLC_RL_trading
Reinforcement learning trading using OHLC data

# OpenAI Gym Trading Environment with DRL
# using Keras on Python 3.6

## Overview

This project provides a general environment for stock market trading simulation using [OpenAI Gym](https://gym.openai.com/). 
Training data is a close price of each day, which is downloaded from Google Finance, but you can apply any data if you want.
Also, it contains simple Deep Q-learning and Policy Gradient from [Karpathy's post](http://karpathy.github.io/2016/05/31/rl/).

In fact, the purpose of this project is not only providing a best RL solution for stock trading, but also building a general open environment for further research.  
**So, please, manipulate the model architecture and features to get your own better solution.**

## Note

This fork uses [stock_market_reinforcement_learning](https://github.com/david200340105/stock_market_reinforcement_learning).
which uses [stock_market_reinforcement_learning](https://github.com/kh-kim/stock_market_reinforcement_learning).

## Changes
 
- fixed issues preventing me from running it on Ubuntu 16.04.4 LTS, Python 3.6.4, Keras 2.1.5, Tensorflow 1.6.0 and Gym 0.10.4

## Requirements

- Python 3.6
- Numpy
- HDF5
- Keras
- Tensorflow
- OpenAI Gym

## How to use

Install

	$ pip install -r requirements.txt

Train Deep Q-learning:

    $ python dqn.py <portfolio filename> [model_filename]

Train Policy Gradient:

	$ python pg.py <portfolio filename> [model_filename]

For example:

	$ python pg.py portfolio.csv model # model filename without extension

After model is trained, you can test it against all symbols in portfolio:

	$ python test.py model # model filename without extension

Please be aware that the provided neural network architecture in this repo is too small to learn. It may under-fit if you try to learn every stock data. 
It just fitted for 10 to 100 stock data for a few years, thus you need to design your own architecture and **let me know if you have better one!**


## Reference

[1] [Playing Atari with Deep Reinforcement Learning](http://arxiv.org/abs/1312.5602)  
[2] [Deep Reinforcement Learning: Pong from Pixels](http://karpathy.github.io/2016/05/31/rl/)  
[3] [KEras Reinforcement Learning gYM agents, KeRLym](https://github.com/osh/kerlym)  
[4] [Keras plays catch, a single file Reinforcement Learning example](http://edersantana.github.io/articles/keras_rl/)
