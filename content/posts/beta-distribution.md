---
title: "Beta Distribution"
date: 2022-03-29T22:25:22+10:00
draft: true
---


# Beta Regression

Today at work we had to deal with the problem of regressing on some 
fractional data, i.e, it lay in the interval $x \in (0,1)$.  

It was suggested that this should be modelled using a logistice regression 
model, however, I thought that this would be a good opportunity to use a 
Beta regression model due the the opvious efficiency advantage it would 
have in the case where the modeled data did indeed originated from a Beta distribution. 

## $Beta(\alpha, \beta)$ 

The beta probability distribution is a member of the exponential family, it has two parameters
$\alpha$ and $\beta$, and the following probability density function.
$$
f(x; \alpha, \beta) = \frac{1}{B(\alpha, \beta)}x^{\alpha - 1}(1 - x)^{\beta - 1}, x \in \mathbb{R}_{(0,1)}
$$

Where $B(\alpha, \beta)$ is the  beta function, and can be  defined in terms of the $\Gamma$ function.

$$
B(\alpha, \beta) = \frac{\Gamma(\alpha) \Gamma(\beta)}{\Gamma(\alpha + \beta)} = \int_{0}^{\infty} t^{\alpha - 1} (1 - t)^{\beta - 1}dt
$$

This releationship then allows for a relatively easy derivation of $\mathbb{E}[X], Var(X)$ as well as the mode of a beta distribution.
$$
\begin{aligned}
	\mathbb{E}[X] =& \frac{1}{B(\alpha, \beta)}\int_{0}^{1} x^{\alpha }(1 - x)^{\beta - 1} dx \\
	              =& \frac{1}{B(\alpha, \beta)}\underbrace{\int_{0}^{1} x^{\alpha }(1 - x)^{\beta - 1} dx}_{B(\alpha + 1, \beta)} \\
	              =& \frac{1}{B(\alpha, \beta)}B(\alpha + 1, \beta) \\
	              =& \frac{\Gamma(\alpha + \beta)}{\Gamma(\alpha)\Gamma(\beta)}\frac{\Gamma(\alpha + 1)\Gamma(\beta)} {\Gamma(\alpha  + \beta)}\\
	              =& \frac{\Gamma(\alpha + \beta)}{\Gamma(\alpha)\Gamma(\beta)}\frac{(\alpha + 1)\Gamma(\alpha)\Gamma(\beta)} {(\alpha  + \beta)\Gamma(\alpha+ \beta)}\\
				  =& \frac{\alpha}{\alpha + \beta}
\end{aligned}
$$
as $\Gamma(x + 1) = x\Gamma(x), x \in \mathbb{R}^+$. 
Similarly for calculating $Var(X)$ we can use the same trick as before. 
$$
\begin{aligned}
     \mathbb{E}[X^2] =& \frac{1}{B(\alpha, \beta)}\int_{0}^{1} x^{\alpha + 1 }(1 - x)^{\beta - 1} dx \\
	              =& \frac{1}{B(\alpha, \beta)}\underbrace{\int_{0}^{1} x^{\alpha + 1 }(1 - x)^{\beta - 1} dx}_{B(\alpha + 2, \beta)} \\
	              =& \frac{1}{B(\alpha, \beta)}B(\alpha + 2, \beta) \\
	              =& \frac{\Gamma(\alpha + \beta)}{\Gamma(\alpha)\Gamma(\beta)}\frac{\Gamma(\alpha + 2)\Gamma(\beta)} {\Gamma(\alpha  + \beta)}\\
	              =& \frac{\Gamma(\alpha + \beta)}{\Gamma(\alpha)\Gamma(\beta)}\frac{(\alpha + 1)\Gamma(\alpha)\Gamma(\beta)} {(\alpha + 1  + \beta)\Gamma(\alpha+ \beta)}\\
				  =& \frac{\alpha + 1}{\alpha + \beta + 1}

\end{aligned}
$$
therefore

$$
\begin{aligned}
Var[X] &= \frac{\alpha + 1}{\alpha + \beta + 1} - \frac{\alpha^2}{\alpha^2 + 2\alpha\beta + \beta^2} \\
       &= \frac{(\alpha + 1)(\alpha^2 + 2\alpha\beta + \beta^2)}{\alpha + \beta + 1} - \frac{\alpha^3 + \alpha^2\beta + \alpha^2}{\alpha^2 + 2\alpha\beta + \beta^2} \\
\end{aligned}
$$


$$
f(x) = \frac{1}{\sqrt{2\pi}\sigma^2}e^{\frac{1}{2\sigma^2}(x - \mu)^2}
$$



