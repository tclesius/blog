---
title: Math rendering
date: 2026-11-22
description: An example post showing inline and display math rendered with KaTeX.
---

Math is rendered to HTML when the site builds, so there is no JavaScript on the page. The KaTeX stylesheet is only loaded on pages that contain math.

## Inline

Wrap inline math in single dollar signs: the Gaussian integral is $\int_{-\infty}^{\infty} e^{-x^2}\,dx = \sqrt{\pi}$, and Euler's identity is $e^{i\pi} + 1 = 0$. `\(...\)` works too: \(a^2 + b^2 = c^2\).

## Display

Double dollar signs give you a centered block:

$$
\operatorname{softmax}(z)_i = \frac{e^{z_i}}{\sum_{j=1}^{K} e^{z_j}}
$$

Scaled dot-product attention:

$$
\operatorname{Attention}(Q, K, V) = \operatorname{softmax}\!\left(\frac{QK^\top}{\sqrt{d_k}}\right) V
$$

## Aligned equations

Bayes' rule, step by step:

$$
\begin{aligned}
p(\theta \mid x) &= \frac{p(x \mid \theta)\, p(\theta)}{p(x)} \\
&= \frac{p(x \mid \theta)\, p(\theta)}{\int p(x \mid \theta')\, p(\theta')\, d\theta'} \\
&\propto p(x \mid \theta)\, p(\theta)
\end{aligned}
$$

## Matrices

$$
\begin{bmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{bmatrix}
\begin{bmatrix} x \\ y \end{bmatrix}
=
\begin{bmatrix} x\cos\theta - y\sin\theta \\ x\sin\theta + y\cos\theta \end{bmatrix}
$$

## Cases

$$
\operatorname{ReLU}(x) =
\begin{cases}
x & \text{if } x > 0 \\
0 & \text{otherwise}
\end{cases}
$$

## Gradient descent

The update rule $\theta_{t+1} = \theta_t - \eta \nabla_\theta \mathcal{L}(\theta_t)$ minimizes the loss

$$
\mathcal{L}(\theta) = \frac{1}{N} \sum_{n=1}^{N} \bigl(y_n - f_\theta(x_n)\bigr)^2 .
$$

Long equations scroll sideways on small screens instead of breaking the layout:

$$
\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s} = \prod_{p \text{ prime}} \frac{1}{1 - p^{-s}} = \frac{1}{1^s} + \frac{1}{2^s} + \frac{1}{3^s} + \frac{1}{4^s} + \frac{1}{5^s} + \frac{1}{6^s} + \cdots
$$
