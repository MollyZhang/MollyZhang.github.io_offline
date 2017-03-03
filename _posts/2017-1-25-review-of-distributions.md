---
layout: post
excerpt: "Bernoulli, Bionomial, Uniform, Exponential and Normal Distributions"
thumbnail: ""
comments: true
---

### Some Definitions

#### **Expectation**

* If $X$ is discrete-valued with probability mass function $f(x)$:  
 $$ E(X) = \sum\limits_{x}^{}x\cdot P(X=x) = \sum\limits_{x}^{} x \cdot f(x)$$

* If $X$ is a continous variable with probability density function $f(x)$:  
 $$ E(X) = \int_{-\infty}^{\infty} x \cdot f(x)dx $$


#### **Variance**
Let $E(X) = \mu$, then $Var(X) = E[(X-\mu)^2]$ and $Var(X) = E(X^2) - E(X)^2$. Standard deviation $\sigma = \sqrt{Var(X)}$. 

* If $X$ is discrete-valued:  
 $$ Var(X) = \sum\limits_{x} (x-\mu)^2 \cdot P(X=x) $$

* If $X$ is a continous:  
 $$ Var(X) = \int_{-\infty}^{\infty} (x-\mu)^2 \cdot f(x)dx $$

#### **Skewness**
$\gamma_1 = E[(\frac{X-\mu}{\sigma})^3]$ 


### Discrete Distributions

#### **Bernoulli Distribution**
 Example: throw a coin once with probablility p resulting in heads  
* Probability mass function $f(x;p) = p^x(1-p)^{1-x}$ for $x \in$ {1, 2}  
* Expectation $E(x) = p$  
* Variance $Var(x) = p(1-p)$  

#### **Binomial Distribution**
Example: throw a coin n times with probablility p resulting in heads in each throw
* Probability mass function $f(x;n,p) = \binom{n}{x}p^x(1-p)^{n-x}$
* Expectation $E(x = np$  
* Variance $Var(x) = np(1-p)$  

#### **Multinomial Distribution**
Generalization of Binomial Distribution. Example: throw a dice with k sides n times. $p_i$ is the probability of getting side $i$, $x_i$ is the number of times side $i$ is seen.  
* Probability mass function $ f(x_1, ... , x_k;n,p_1, ... , p_k) = \frac{n!}{x_1! \cdot \cdot \cdot x_k!} {p_1}^{x_1} \cdot \cdot \cdot {p_k}^{x_k} I_{ \\{ \sum_{i=1}^{k}x_i = n \\}}(x)$
* Expectation $E(x_i) = np_i$  
* Variance $Var(x_i) = np_i(1-p_i)$  


#### **Genometric Distribution**
Example: How many times do you need to throw a coin until you see first heads? p is the probability of getting heads in one throw.
* Probability mass function $f(x;p) = p(1-p)^{x-1}$
* Expectation $E(x) = 1/p$  
* Variance $Var(x) = \frac{1-p}{p^2}$ 


#### **Poisson DIstribution**
Example: The rate of observing heads out of 100 coin throws is $\lambda$, what's the probability of oberving k heads after throwing coins 100 times.  
* Probability mass function $f(k; \lambda) = P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}$
* Expectation $E(X) = \lambda $
* Variance $Var(X) = \lambda $




### Continous Distributions

#### **Uniform Distribution**  
Example: A coin might be fair or loaded with a probability from 0 to 1 continously and equally.  
* Probability density function $f(x \| a,b) = \frac{1}{b-a} I_{ \\{ a \leq x \leq b \\}}(x)$
* Expectation $E(X) = \frac{a+b}{2} $
* Variance $Var(X) = \frac{(b-a)^2}{12} $



#### **Exponential Distribution**

#### **Normal Distribution**













### Notes:

* [This tutorial](http://www.markdowntutorial.com/lesson/5/) gave me a great tutorial/review of markdown format.

* [This article](http://cwoebker.com/posts/latex-math-magic) helped me display the above math equations on markdown files.
