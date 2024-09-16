---
title: "Quadratic Equation"
date: 2022-09-26T21:31:24+10:00
mathjax: true
draft: false
---

# Introduction  
In this very short blog post I want to go through the derivation of the quadratic equation as a simple teaching exercise. 
As most of us are aware from high school, 
when solving for the solutions  to the following equation 
$$
ax^2 + bx + c = 0,\qquad a \neq 0
$$
one can use the quadratic equation, which has the general form. 
$$
x_{1, 2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

## Derivation 

### Initial Setup
To derive this equation one can use the following steps, 
$$
ax^2 + bx + c = 0 \implies  ax^2 + bx  =-c
$$
As $a \neq 0$ we can divide through to get 
$$
x^2 + \frac{b}{a}x = -\frac{c}{a}
$$

### Completing the Square 

Another fundamental piece of mathematics knowledge the most readers will be familier with is "completing the square". 

The general technique to complete the square is shown below 
$$
ax^2 + bx + c \implies \left( ax + \frac{b}{2}\right)^2 + c - \frac{b^2}{4}
$$

### Finishing Up

Using this knowledge we can now complete and solve the quadratic equation 
$$
x^2 + \frac{b}{a}x = -\frac{c}{a} \implies \left(x + \frac{b}{2a}\right)^2 - \frac{b^2}{4a^2} = -\frac{c}{a}
$$

$$
 \left(x + \frac{b}{2a}\right)^2 = \frac{b^2}{4a^2}-\frac{c}{a}
$$

$$
x + \frac{b}{2a}= \pm\sqrt{\frac{b^2}{4a^2}-\frac{c}{a}} 
$$

$$
x = -  \frac{b}{2a}  \pm\sqrt{\frac{b^2}{4a^2}-\frac{c}{a}} 
$$
$$
x = -  \frac{b}{2a}  \pm\sqrt{\frac{b^2}{4a^2}-\frac{c \cdot 4a }{4a^2}} 
$$
$$
x = -  \frac{b}{2a}  \pm\frac{\sqrt{b^2-4ac}}{2a}
$$

Which is the required result. $$\blacksquare$$  








