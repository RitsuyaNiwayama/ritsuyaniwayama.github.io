---
layout: post
title: "The relationships between different types of convergences"
date: 2021-06-05 16:00:30 -0000
categories: Probability
---

This blog post shows that, if a sequence of random variables converges $$P$$-a.s., then such a sequence also weakly converges.

Let $$X,X_n (n=1,2,...)$$ be real value random variables. Let ($$ S,\bf{B},\mu $$ ) be a probability space.
<h1>Step 1</h1>
We will firstly prove that, if $$ X_n \overset{n \to \infty}{\longrightarrow} X, \quad P$$-a.s. then $$ \lim_{n \to +\infty} \lVert X_n-X \rVert _0 = 0$$, where $$ \lVert X \rVert_0= \int  \min (1,\lvert X \rvert) d\mu$$, using Lebesgue's dominated convergence theory. Namely,
$$ \lim_{n \to +\infty} \lVert X_n-X \rVert_0= \lim_{n \to +\infty}\int  \min (1,\lvert X_n-X \rvert) d\mu= \int  \lim_{n \to +\infty} \min (1,\lvert X_n-X \rvert) d\mu=\int  \min (1,0) d\mu=0$$

Let us notice that we can use Lebesgue's dominated convergence theory because

$$min(1,f) \lt 1, so \int 1 d\mu = 1 \lt \infty.$$


<h1>Step 2</h1>
Then we prove that the convergence in probability when

$$ \lim_{n \to +\infty} \lVert X_n-X \rVert_0=0.$$

In fact, assuming $$\delta \in (0,1),$$

$$\delta 1_{(\lvert X \rvert \geq \delta)} \leq \min (1,\lvert X \rvert), $$

which we integrate to obtain

$$\delta \mu(\lvert X \rvert \geq \delta) \leq  \lVert X \rVert_0. $$

Therefore, we see, by putting $$ X_n-X $$ in the both sides of the equation, for any $$\delta \in (0,1)$$,

$$ \lim_{n \to +\infty} \mu(\lvert X_n-X \rvert \geq \delta)= 0, $$

which means $$ X_n \overset{n \to \infty}{\longrightarrow} X$$ in probability.
<h1>Step 3</h1>
Based on it, we can prove that $$ E\lvert f(X_n)-f(X) \rvert \overset{n \to \infty}{\longrightarrow} 0,$$ if f is bounded and uniformly continuous.

For all $$\epsilon \gt 0$$, there is a $$\delta$$ such that if $$\lvert X_n-X \rvert \lt \delta, \lvert f(X_n)-f(X) \rvert \lt \epsilon /2$$ (uniformly continuous). Let us suppose $$\lvert f(x) \rvert \lt M $$ (bounded). Then if $$ X_n \overset{n \to \infty}{\longrightarrow} X$$ in probability, by setting n large, we can make $$  \mu(\lvert X_n-X \rvert \geq \delta) \lt \epsilon/4M. $$ Under this condition,

$$ E\lvert f(X_n)-f(X) \rvert =$$

$$\int_{\lvert X_n-X \rvert \lt \delta} \lvert f(X_n)-f(X) \rvert d\mu + \int_{\lvert X_n-X \rvert \geq \delta} \lvert f(X_n)-f(X) \rvert d\mu  <$$

$$\epsilon /2 + \int_{\lvert X_n-X \rvert \geq \delta}  2M  d\mu <\epsilon$$

<h1>Step 4</h1>
As the characteristic function of a probability measure is bounded and uniformly continuous, $$ \lvert E( \exp (i \theta X_n))-E(\exp(i \theta X)) \rvert \lt E\lvert \exp (i \theta X_n)-\exp(i \theta X) \rvert \overset{n \to \infty}{\longrightarrow} 0.$$ This means $$ X_n \overset{n \to \infty}{\longrightarrow} X$$ weakly.



