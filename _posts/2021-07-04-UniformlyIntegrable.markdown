---
layout: post
title: "A sufficient condition to be uniformly integrable"
date: 2021-07-04 16:00:30 -0000
categories: Probability
page.mathjax: true
---
Here we talk about a sufficient condition for real random variables $$ (X_\lambda )_{\lambda \in \Lambda}$$ to be uniformly integrable.

<h1>Definition of being uniformly integrable</h1>

&& \sup_{\lambda \in \Lambda} {E \lvert X_\lambda \rvert : \lvert X_\lambda \rvert \gt m }

Let us assume that there are a sequence of random variables, taking values in $$\mathbb{R}^{d_1},$$ $$ X_n (n=1,2,...)$$ weakly converges to $$ X $$, $$ (X_n \overset{w}{\longrightarrow} X )$$ and another sequence of r.v.s $$Y_n (n=1,2,...)$$, taking values in $$\mathbb{R}^{d_2}$$, weakly converging to a constant $$ (Y_n \overset{w}{\longrightarrow} c )$$. They are not necessarilly independent. Even in such a case can we conclude that $$ (X_n, Y_n) \overset{w}{\longrightarrow} (X,c)?$$ The answer is yes, and here I described an outline of the proof. As it is just an outline, several details of the proof are omitted. Therefore, omitted parts should be searched for on Google if they are of interest of a reader.
<h1>Assumed knowledge</h1>
Let $$(\Omega,\mathcal{F},P)$$ be a probability space. Let $$(S,\mathcal{B})$$ a measurable space. Let $$X : \Omega \to S$$ a random variable. Let the law of $$X$$ be $$\mu$$. Similarly Let $$X_n (n=1,2,...): \Omega \to S$$ a random variable. Let the law of $$X_n$$ be $$\mu_n$$. Here, there is a theorem.

$$E(f(X))=\int f(x) d\mu$$

for any measurable function $$f S \to [0, \infty]$$

Weak convergence of a sequence of random variables $$ X_n (n=1,2,...)$$ to $$X$$ is defined by

$$E(\exp (i\theta^T X_n)) \longrightarrow E(\exp (i\theta^T X)),$$


where $$\theta \in \mathbb{R}^{d_1},$$ and $$\theta^T$$ is its transposition.

This is equivalent to

$$ \int f d\mu_n = \int f d\mu$$

for all bounded and coutinuous functions.



<h1>The outline of the proof</h1>
It is sufficient if we show

$$ E(\exp (i \theta_1^T X_n + i \theta_2^T Y_n)) \to E(\exp (i \theta_1^T X + i \theta_2^T c))$$

Let's show
$$\lvert E(\exp (i \theta_1^T X_n + i \theta_2^T Y_n)) - E(\exp (i \theta_1^T X + i \theta_2^T c)) \rvert \lt \epsilon$$ for any $$\epsilon \gt 0$$ if $$n$$ is sufficiently large.

$$\lvert E(\exp (i \theta_1^T X_n + i \theta_2^T Y_n)) - E(\exp (i \theta_1^T X + i \theta_2^T c)) \rvert $$
$$=\lvert E(\exp (i \theta_1^T X_n + i \theta_2^T Y_n)) - E(\exp (i \theta_1^T X_n + i \theta_2^T c)) + E(\exp (i \theta_1^T X_n + i \theta_2^T c)) - E(\exp (i \theta_1^T X + i \theta_2^T c)) \rvert$$

$$\leq \lvert E(\exp (i \theta_1^T X_n + i \theta_2^T Y_n)) - E(\exp (i \theta_1^T X_n + i \theta_2^T c))\rvert + \lvert E(\exp (i \theta_1^T X_n + i \theta_2^T c)) - E(\exp (i \theta_1^T X + i \theta_2^T c)) \rvert$$

$$\leq E \lvert \exp (i \theta_1^T X_n + i \theta_2^T Y_n) - \exp (i \theta_1^T X_n + i \theta_2^T c) \rvert + \lvert E(\exp (i \theta_1^T X_n + i \theta_2^T c)) - E(\exp (i \theta_1^T X + i \theta_2^T c)) \rvert$$

Let us evaluate the first term. We focus on the fact that, as $$ (Y_n \overset{w}{\longrightarrow} c (\in \mathbb{R}^{d_2}) )$$, $$Y_n$$ also converges in probability. Therefore, for any $$ \delta $$, for all $$\epsilon>0$$, there is an $$ N$$ , $$ P(\lvert Y_n-Y \rvert \geq \delta) \lt \epsilon/4$$ if $$ n>N. $$In addition, $$ \exp (i \theta_1^T x + i \theta_2^T y)$$ is uniformly continuous function of $$(x,y)$$. Therefore, for all $$\epsilon>0$$, there is a $$\delta$$ fulfilling, $$ \lvert \exp (i \theta_1^T x_1 + i \theta_2^T y_1)-  \exp (i \theta_1^T x_2 + i \theta_2^T y_2) \rvert <\epsilon/4$$ if $$\lvert (x_1,y_1)-(x_2,y_2)\rvert< \delta. $$ Based on these, if $$n$$ is large enough,

$ E\lvert \exp (i \theta_1^T X_n + i \theta_2^T Y_n) - \exp (i \theta_1^T X_n + i \theta_2^T c) \rvert $

$$=\int_{\lvert Y_n-c \rvert \lt \delta} \lvert \exp (i \theta_1^T X_n + i \theta_2^T Y_n) - \exp (i \theta_1^T X_n + i \theta_2^T c) \rvert dP + \int_{\lvert Y_n-c \rvert \geq \delta} \lvert \exp (i \theta_1^T X_n + i \theta_2^T Y_n) - \exp (i \theta_1^T X_n + i \theta_2^T c) \rvert dP$$

$$\lt \epsilon /4 + \int_{\lvert Y_n-c \rvert \geq \delta}  2  dP <\epsilon/2$$


The second term will become $$<\epsilon/2$$ if $$n$$ is large enough because $$ \int f d\mu_n = \int f d\mu$$

for all bounded and coutinuous functions. Therefore,

$$E \lvert \exp (i \theta_1^T X_n + i \theta_2^T Y_n) - \exp (i \theta_1^T X_n + i \theta_2^T c) \rvert + \lvert E(\exp (i \theta_1^T X_n + i \theta_2^T c)) - E(\exp (i \theta_1^T X + i \theta_2^T c)) \rvert \lt \epsilon$$

for any $$\epsilon \gt 0.$$ This means $$ (X_n, Y_n) \overset{w}{\longrightarrow} (X,c) $$.