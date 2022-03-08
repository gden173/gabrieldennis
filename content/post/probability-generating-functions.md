---
title: "Probability Generating Functions"
date: 2022-03-08T22:15:07+10:00
draft: false
mathjax: true
---


In this post we are going to go over the derivation of some of the most commonly used probability 
generating transforms.

## Probability Generating Function 

The probability generating function, often reffered to as the *PGF* has the following definition 

$$
\mathcal{G}_{X}(z) = E_{X}[z^k] = \sum_{k = 0}^{\infty} P(x = k)z^k 
$$

## Bernoulli

As can be recalled from previous posts, the bernoulli distribution, has the pdf 
$$
f(x) = {n\choose k} p^x (1- p)^x
$$

The PGF is then 

$$
\mathcal{G}(z) =   \sum_{k = 0}^{\infty} P(x = k)z^k = P(x = 0)z^0 + P(x = 1)z^1 = p + (1 - p)z  

$$


## Geometric

The Geometric distribution has the pgf 
$$
f(x) = (1 - p)^{k-1}p
$$

The PGF is then 

$$
\mathcal{g}(z) =   \sum_{k = 0}^{\infty} p(x = k)z^k =  \sum_{k = 0}^{\infty}(1 - p)^{k-1}p z^k   
$$

From here we can easily see that 

$$
\mathcal{g}(z) =   \sum_{k = 0}^{\infty}(1 - p)^{k}(1 - p)^{-1}p z^k = \frac{p}{1 - p} \sum_{k = 0}^{\infty} (1 - p)^kz^k
$$
This is a geometric series with a radius of convergence when $|(1 - p)z| < 1$, 

$$
\mathcal{g}(z) =   \frac{p}{1 - p} \frac{1}{1  - z - pz}  
$$




## Binomial



## Poisson

## Exponential

## Weibal 

## Normal


## Cauchy

## Gumbel
