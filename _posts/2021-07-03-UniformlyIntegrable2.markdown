---
layout: post
title: "A sufficient condition to be uniformly integrable"
date: 2021-07-03 16:00:30 -0000
categories: Probability
page.mathjax: true
---
Here we talk about a sufficient condition for real random variables $$ (X_\lambda )_{\lambda \in \Lambda}$$ to be uniformly integrable.

<h1>Definition of being uniformly integrable</h1>

$$ \sup_{\lambda \in \Lambda} E[\lvert X_\lambda \rvert : \lvert X_\lambda \rvert \gt m ] \longrightarrow 0$$

as $$m \longrightarrow \infty $$.

What is the meaning of $$E[X: a \, condition  \, A]$$? It means $$E[X*1_{the \, condition \, A}]$$ where $$1_{the \, condition \, A}$$ is a function whose value is equal to 1 where the condition A holds and whose value is equal to 0 otherwise.

With the uniform integrability, we can prove other propositions and theorems, so it is useful. For example, if random variables, taking values in $$\mathbb{R},$$ $$ X_n (n=1,2,...)$$ weakly converges to $$X,$$ we can show $$X, X_n \in L^1(P)$$ and $$E[X_n] \longrightarrow E[X]\, , E \lvert X_n \rvert \longrightarrow E \lvert X \rvert $$.



<h1>A sufficient condition</h1>

Let $$\phi$$ be a non-decreasing function $$ \phi, [0, \infty) \to [0, \infty)$$,

and fulfills  $$ \lim_{x \to +\infty} \phi(x) =\infty$$, $$\sup_{\lambda \in \Lambda}E[\lvert X_\lambda \rvert \phi (\lvert X_\lambda \rvert) ] \lt \infty. $$ Then, $$ (X_\lambda )_{\lambda \in \Lambda}$$ is uniformly integrable.

<h1>A proof</h1>
$$ E[\lvert X_\lambda \rvert : \lvert X_\lambda \rvert \gt m ] \leq E[\lvert X_\lambda \rvert : \phi ( \lvert X_\lambda \rvert ) \gt \phi (m) ]$$

We now take m sufficiently large so that $$ \phi(m) \gt 0$$, under which $$\phi ( \lvert X_\lambda \rvert ) \gt \phi (m) \Leftrightarrow \phi ( \lvert X_\lambda \rvert ) / \phi (m) > 1. $$

Therefore, 

$$E[\lvert X_\lambda \rvert : \phi ( \lvert X_\lambda \rvert ) \gt \phi (m) ] \lt $$

$$E[\lvert X_\lambda \rvert \phi ( \lvert X_\lambda \rvert ) / \phi (m): \phi ( \lvert X_\lambda \rvert ) \gt \phi (m) ] =$$

$$E[\lvert X_\lambda \rvert \phi ( \lvert X_\lambda \rvert ): \phi ( \lvert X_\lambda \rvert ) \gt \phi (m) ]/ \phi(m) \lt$$

$$E[\lvert X_\lambda \rvert \phi ( \lvert X_\lambda \rvert )]/ \phi(m)$$

By taking $$\sup$$ in regard to $$\lambda,$$ We obtain

$$\sup_{\lambda \in \Lambda}E[\lvert X_\lambda \rvert : \phi ( \lvert X_\lambda \rvert ) \gt \phi (m) ] \lt \sup_{\lambda \in \Lambda} E[\lvert X_\lambda \rvert \phi ( \lvert X_\lambda \rvert )]/ \phi(m) = Const / \phi(m).$$
Based on the sufficient condition given, this value converges to zero when $$ m \longrightarrow \infty.$$ Therefore,$$ (X_\lambda )_{\lambda \in \Lambda}$$ are uniformly integrable.

<h1>a special case</h1>
Especially, if there is a $$\delta > 0 $$, and if $$\sup_{\lambda \in \Lambda} E[\lvert X_\lambda \rvert^{1+\delta} ] \lt \infty,$$ $$ (X_\lambda )_{\lambda \in \Lambda}$$ are uniformly integrable.