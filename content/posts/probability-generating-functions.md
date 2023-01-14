---
title: "Bernoulli and Geometric Distribution PGF"
date: 2022-03-08T22:15:07+10:00
draft: true
mathjax: true
tags: ["maths", "probability", "probability generating functions"]
---

In this post we are going to go over the derivation of probability generating 
function of the Bernoulli distribution. 

## Probability Generating Function 

The probability generating function often referred to as the *PGF* has the following definition 

$$ \mathcal{G}\_{X} (z) = \mathbb{E}\_{X}[z^k] = \sum_{k = 0}^{\infty} P(x = k)z^k $$

## Bernoulli

As can be recalled from previous posts, the Bernoulli distribution has the PDF 

$$
f(x) = {n\choose k} p^x (1- p)^x
$$

The PGF is then 

$$
 \mathcal{G}\_{X} (z)= \sum_{k = 0}^{\infty}  \mathbb{P}(x = k)z^k = \mathbb{P}(x = 0)z^0 + \mathbb{P}(x = 1)z^1 = p + (1 - p)z  
$$


## Geometric

The Geometric distribution has the PGF 

$$
f(x) = (1 - p)^{k-1}p
$$

The PGF is then 

$$
 \mathcal{G}\_{X} (z) =   \sum_{k = 0}^{\infty} \mathbb{P}(x = k)z^k =  \sum_{k = 0}^{\infty}(1 - p)^{k-1}p z^k   
$$

From here we can easily see that 
$$
 \mathcal{G}\_{X} = \sum_{k = 0}^{\infty}(1 - p)^{k}(1 - p)^{-1}p z^k = \frac{p}{1 - p} \sum_{k = 0}^{\infty} (1 - p)^kz^k
$$
This is a geometric series with a radius of convergence when $$|(1 - p)z| < 1$$
Which should always be the case, as \\(p \in (0,1)\\), and \\(z\\) is chosen 
to be in the same interval to assure convergence.


Hence, the PGF of a Geometric Distribution is 

$$
 \mathcal{G}\_{X}=   \frac{p}{1 - p} \frac{1}{1  - z - pz}  
$$




