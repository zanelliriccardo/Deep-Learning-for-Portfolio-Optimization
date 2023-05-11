# Deep-Learning-for-Portfolio-Optimization

Implementation of this paper:
[Paper](https://jfds.pm-research.com/content/iijjfds/2/4/8.full.pdf)

Paper describe how to optimize [Sharpe Ratio](https://en.wikipedia.org/wiki/Sharpe_ratio) using deep learning.

As I need to define Sharpe Ratio as loss function I need to implement a custom training.

Also I tried to change the objective from LSTM to directly optimize Sharpe Ratio in LSTM for prediction and optimize Sharpe Ratio through quadratic programming.
But Sharpe Ratio is not a convex function, so we have many possibilities:
- Dual problem
- Do some transformations in order to achieve convexity
- Change approach and implement a neural network to maximize numerator(returns) and a neural network to minimize denominator(volatility). This is a min-max game like what happens in Generative Adversarial Networks

