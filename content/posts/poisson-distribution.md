---
title: "Poisson distribution"
date: 2023-01-15T22:02:22+10:00
draft: false
tags: ["statistics", "distributions"]
mathjax: true 
---

# Poisson Distribution 


The general form of the pdf for the Poisson distribution is 

$$
f(x; \lambda)  = \mathbb{P}(X = x)  = \frac{\lambda^x e^{-\lambda}}{x!}
$$

And in this instance we say that the R.V \\(X \sim P(\lambda)\\). 

# PGF

The Probability Generating function of a Poisson Distribution has the following form  

$$
\begin{aligned}
\mathcal{G}\_{X}(z) &= \sum_{k = 1}^{\infty} z^k\frac{\lambda^k e^{-\lambda}}{k!} \\\\ 
                 &= e^{-\lambda}\sum_{k = 1}^{\infty} \frac{(\lambda z)^{k}}{k!} \\\\
                 &= e^{-\lambda}e^{\lambda z} \\\\
                 &= e^{\lambda(z - 1)} 
\end{aligned}
$$

Hence, 

$$
\begin{aligned}
	\mathbb{E}[X] &= \mathcal{G}'(1) \\\\
                      &= |_{z = 1} \lambda e^{\lambda(z -1)}  \\\\
                      &= \lambda
\end{aligned}
$$





