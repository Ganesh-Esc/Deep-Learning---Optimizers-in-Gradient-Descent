# Deep-Learning---Optimizers-in-Gradient-Descent
# Optimizers in Gradient Descent: Improving Neural Network Training ⚙️

![Deep Learning](https://img.shields.io/badge/Topic-Optimization-brightgreen)

Imagine you are a data scientist tasked with building a neural network to classify food items as healthy or unhealthy based on their nutritional information. After trying different network architectures and hyperparameter tuning, your model is still underfitting and performing poorly. What else can you do?

This lab demonstrates that the choice of **optimizer** can play a significant role in the neural network training process. We will explore how different optimization algorithms can dramatically affect a model's convergence speed and final performance on a real-world classification problem.

---

## 🎯 Objectives

After completing this lab, you will be able to:

* **Explain** several popular optimizers used in deep learning.
* **Evaluate** their performance in a real-world classification scenario.
* **(Optional)** Implement the Adam optimizer from scratch to understand its mechanics.

---

## 🛠️ What is an Optimizer?

An optimizer is an algorithm that adapts the neural network's weights and learning rate to minimize the loss function. Think of the training process as a hiker trying to find the lowest point in a mountainous valley (the loss function landscape). The optimizer is the strategy the hiker uses to navigate—how big of a step to take (learning rate) and in which direction (gradient). A good optimizer helps the hiker reach the bottom quickly and without getting stuck.

### Popular Optimizers Covered:

* **Stochastic Gradient Descent (SGD):** The fundamental optimizer. It updates the weights based on the gradient calculated from a small batch of data. It's simple but can be slow and noisy.
* **Momentum:** An extension of SGD that helps accelerate gradient vectors in the right direction. It adds a fraction of the previous update step to the current one, which helps to navigate ravines and prevents getting stuck in local minima, much like a ball rolling down a hill gathers momentum.
* **RMSprop (Root Mean Square Propagation):** An adaptive learning rate optimizer that maintains a per-parameter learning rate. It divides the learning rate by an exponentially decaying average of squared gradients, which helps to handle non-stationary objectives.
* **Adam (Adaptive Moment Estimation):** One of the most popular and effective optimizers. It combines the ideas of Momentum and RMSprop by using moving averages of both the gradient (first moment) and the squared gradient (second moment). It's generally a great default choice for most problems.

---

## 📝 Lab Workflow

1.  **Data Preparation:** Load and preprocess the food nutrition dataset.
2.  **Baseline Model:** Build a neural network and train it using the standard `SGD` optimizer to establish a performance baseline.
3.  **Implement Different Optimizers:** Train the *exact same* network architecture multiple times, swapping out the optimizer in the `.compile()` step each time (e.g., using `SGD` with momentum, `RMSprop`, and `Adam`).
4.  **Evaluate Performance:** Plot the training and validation accuracy/loss curves for each optimizer on the same chart. Compare their convergence speed and final performance metrics.
5.  **Analyze Results:** Discuss the observed differences. Which optimizer trained the fastest? Which one achieved the highest accuracy?
6.  **(Optional) Adam from Scratch:** Move beyond the Keras API and implement the Adam update rule manually to gain a deeper appreciation for how it works under the hood.
