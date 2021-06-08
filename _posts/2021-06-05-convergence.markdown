---
layout: post
title: "The relationships between different types of convergences"
date: 2021-06-05 16:00:30 -0000
categories: Probability
---

This blog post shows that if a sequence of random variables converges $$P$$-a.s., then such a sequence also weekly converges.

Let $$X,X_n (n=1,2,...)$$ be real value random variables. Let ($$ S,\bf{B},\mu $$ ) be a probability space.
<h1>Step 1</h1>
$$ X_n \overset{n \to \infty}{\longrightarrow} X, \quad P$$-a.s. then $$ \lim_{n \to +\infty} \lVert X_n-X \rVert _0 = 0$$, where $$ \lVert X \rVert_0= \int  \min (1,\lvert X \rvert) d\mu$$. This can be proved by dominated convergence theory. Namely,
$$ \lim_{n \to +\infty} \lVert X_n-X \rVert_0= \lim_{n \to +\infty}\int  \min (1,\lvert X_n-X \rvert) d\mu= \int  \lim_{n \to +\infty} \min (1,\lvert X_n-X \rvert) d\mu=\int  \min (1,0) d\mu=0$$

Let us notice that we can use Lebegue's dominated convergence theory because

$$min(1,f) \lt 1$$ and $$\int 1 d\mu = 1 \lt \infty$$
<h1>Step 2</h1>
Then we can prove that the convergence in probability as well. In fact,

$$\delta 1_{(\lvert X \rvert \geq \delta)} \leq \min (1,\lvert X \rvert) $$

, which we integrate to obtain

$$\delta \mu(\lvert X \rvert \geq \delta) \leq  \lVert X \rVert_0. $$

Therefore, for any $$\delta$$

$$ \lim_{n \to +\infty} \mu(\lvert X_n-X \rvert \geq \delta)= 0, $$

which means $$ X_n \overset{n \to \infty}{\longrightarrow} X$$ in probability.
<h1>Step 3</h1>
Based on it, we can prove that $$ E\lvert f(X_n)-f(X) \rvert \overset{n \to \infty}{\longrightarrow} 0,$$ if f is bounded and uniformly continuous.

For all $$\epsilon$$, there is a $$\delta$$ such that if $$\lvert X_n-X \rvert \lt \delta, \lvert f(X_n)-f(X) \rvert \lt \epsilon /2$$. Let us suppose $$\lvert f(x) 1rvert \lt M $$.Then if $$ X_n \overset{n \to \infty}{\longrightarrow} X$$ in probability,




