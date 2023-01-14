---
title: "Normal Distribution"
date: 2022-03-08T23:44:00+10:00
draft: true
---


## The Normal Distribution 

The normal or *Gaussian* distribution is perhaps the most common distribution occuring in nature. 
This is due to the relatively special properties it has for larger sample sizes. 
However, these properties will be the topic of another blog post. 
Instead, in this post we are simply going to outline the basic mathematical structure of the normal distribution.

### Probability Density Function 

The probability density function of a
$$ \mathcal{N}(\mu, \sigma^2) $$
normal distribution is 

$$
f(x) = \frac{1}{\sqrt{2\pi\sigma^2}}e^{\frac{1}{2\sigma^2}(x - \mu)^2}, x \in \mathbb{R} 
$$


### Mean 

The derivation of the mean of a normal distribution is relatively straight forward. 
$$
\mathbb{E}[X] =  \int_{x = 0}^{\infty} \frac{1}{\sqrt{2\pi\sigma^2}}xe^{\frac{1}{2\sigma^2}(x - \mu)^2} dx
$$

