---
layout: post
title: "G measurable r.v.s go out of conditional expectations"
date: 2021-07-29 5:00:30 -0000
categories: Probability
page.mathjax: true
---
Here we show a proof of a useful proposition related to conditional expectation. It is also a nice
<h1>A proposition to prove in this post</h1>
Let $$X$$ and $$Z$$ be real value random variables (r.v.s).$$Z$$ is $$\operatorname{\mathcal{G}-measurable}$$. We assume $$X \quad and \quad XZ \in L^1(P)$$. Then,

$$ E[ZX\mid \mathcal{G}]=ZE[X \mid \mathcal{G}]$$.

Let's review notations here first and prove it.
<h1>Notations</h1>
Let $$(\Omega,\mathcal{F},P)$$ be a probability space. Let $$E[X]$$ be $$\int_\Omega XdP.$$ Let $$ \mathcal{G} $$ be a $$\operatorname{sub- \sigma -algebra}$$
 of $$\mathcal{F}.$$
Let $$A \in \mathcal{G}$$ be a set. $$E[X:A]$$ denotes $$E[X*1_{A}]$$ where $$1_{A}$$ is a function whose value is equal to 1 in A and whose value is equal to 0 outside A.

Let us take a real value random variable $$X$$, which is $$\operatorname{\mathcal{F}-measurable}$$. There is an almost surely unique $$\operatorname{\mathcal{G}-measurable}$$ r.v. $$Y$$ that fulfills


$$Q(A)=E[X:A]=E[Y:A] \quad$$for all $$A \in \mathcal{G}$$
This random variable is actually
$$Y=dE[X:A]|_{\mathcal{G}}/dP|_{\mathcal{G}}=dQ|_{\mathcal{G}}/dP|_{\mathcal{G}}$$, where this derivative means Radon-Nikodym derivative on $$\mathcal{G}$$. We call such r.v. $$Y$$ conditional expectation.

$$Y=E[X\mid \mathcal{G}].$$

If two variables X and Y fulfill $$E[X:A]=E[Y:A] \quad$$for all $$A \in \mathcal{G}$$, then their conditional expectations on $$\mathcal{G}$$ are almost surely identical.

<h1>Theorems used to prove the poposition</h1>

<h4>A characteristics of conditional expectation</h4>
To prove the proposition, here we introduce one characteristics of conditional expectation. Let us suppose $$ X_n \longrightarrow X \in L^1(P)$$. Then, $$E[\lvert X  -X_n\rvert \mid \mathcal{G}]\longrightarrow 0$$ as $$n \to \infty .$$

This is because 
$$E[E[\lvert X  -X_n\rvert \mid \mathcal{G}]]=E\lvert X  -X_n\rvert$$. If the right side of this equation goes to zero as $$n \to \infty ,$$ the right side goes to zero as well, and vice versa.

<h4>Simple random variable</h4>
A simple $$\operatorname{\mathcal{G}-measurable}$$ random variable $$X$$ on $$\Omega$$ is one fulfilling


$$X = \Sigma_{k=1}^{n}\alpha_k 1_{A_k}$$ where


$$\Omega = \bigcup_{k=1}^{n} A_k$$, $$\quad A_j\cap{A_k}=\emptyset$$ if $$j\neq k$$, $$\quad \forall k, A_k \in \mathcal{G}$$.


According to a proposition from the measure theory, if there is a $$\operatorname{\mathcal{G}-measurable}$$ random variable $$X$$, there exists a sequence of simple $$\operatorname{\mathcal{G}-measurable}$$ random variables $$X_n, n \in \mathbb{N}$$ that fulfills $$\lvert X_n\rvert \leq \lvert X \rvert$$, $$ \lim_{n \to +\infty} X_n=X.$$

<h4>Dominant convergence theorem</h4>
Let $$Y$$ be a non negative $$ \operatorname{\mathcal{G}-measurable}$$ random variable and $$\int_{\Omega} YdP \lt \infty.$$ Let $$X$$ and $$X_n, n \in \mathbb{N}$$ be $$\operatorname{\mathcal{G}-measurable}$$. Let us suppose that $$ \lim_{n \to +\infty} X_n=X,$$ and that$$ \sup_n X_n \leq Y.$$ Then $$\lim_{n \to +\infty} \int_{\Omega} \lvert X-X_n \rvert dP =0.$$ According to triangle inequality, this also means

$$\lim_{n \to +\infty} \int_{\Omega} X_n dP =  \int_{\Omega}XdP$$

<h1>A proof of the proposition</h1>
We are ready to prove $$ E[ZX\mid \mathcal{G}]=ZE[X \mid \mathcal{G}]$$. Here, $$X$$ and $$Z$$ are real r.v.s. $$Z$$ is $$\operatorname{\mathcal{G}-measurable}$$. We assume $$X and XZ \in L^1(P)$$.

We prove it for $$Z$$ that are simple. We use the fact that if there is a $$\operatorname{\mathcal{G}-measurable}$$ r.v. Y fulfilling $$E[X:A]=E[Y:A] \quad$$for all $$A \in \mathcal{G}$$, it is unique and is $$E[X\mid \mathcal{G}].$$

Here we can write $$Z = \Sigma_{k=1}^{n}\alpha_k 1_{B_k}$$, where $$\Omega = \bigcup_{k=1}^{n} B_k$$, $$\quad B_j\cap{B_k}=\emptyset$$ if $$j\neq k$$, $$\quad \forall k, B_k \in \mathcal{G}$$. For an arbitrary $$A \in \mathcal{G}$$,$$E[ZX:A]=E[\Sigma_{k=1}^{n}\alpha_k 1_{B_k}X:A]=\Sigma_{k=1}^{n}\alpha_k E[1_{B_k}X:A]=$$

$$\Sigma_{k=1}^{n}\alpha_k E[X:A\cap{B_k}]=$$

$$\Sigma_{k=1}^{n}\alpha_k E[E[X\mid \mathcal{G}]:A\cap{B_k}]=$$

$$\Sigma_{k=1}^{n}\alpha_k E[1_{B_k} E[X\mid \mathcal{G}]:A]=$$

$$\Sigma_{k=1}^{n} E[\alpha_k 1_{B_k} E[X\mid \mathcal{G}]:A]=$$

$$ E[\Sigma_{k=1}^{n} \alpha_k 1_{B_k} E[X\mid \mathcal{G}]:A]=$$


$$ E[Z E[X\mid \mathcal{G}]:A]$$

Namely,by taking the most left and right side, $$E[ZX:A]=E[Z E[X\mid \mathcal{G}]:A], \forall A \in \mathcal{G}$$. Both sides are signed measure absolutely continuous with respect to P. Therefore, by taking their Radon-Nikodym derivatives. We get
$$E[ZX\mid \mathcal{G}]=E[Z E[X\mid \mathcal{G}]\mid \mathcal{G}]=Z E[X\mid \mathcal{G}]$$ Thus, the proposition was proved for simple $$\operatorname{\mathcal{G}-measurable} Z$$.

Now, we extend it to $$\operatorname{\mathcal{G}-measurable} Z$$ that are not necesarilly simple. For any such Z, there exists sequences of r.v.s fulfilling $$\lvert Z_n\rvert \leq \lvert Z \rvert$$, $$ \lim_{n \to +\infty} Z_n=Z. $$Therefore, $$\lvert Z_n X\rvert \leq \lvert ZX \rvert$$, $$ \lim_{n \to +\infty} Z_n X 1_A=ZX 1_A.$$ 

Such $$Z_n s$$ fulfill $$E[Z_nX:A]=E[Z_n E[X\mid \mathcal{G}]:A]$$. We will show that when in the limit of $$n \to \infty$$, we will get $$E[ZX:A]=E[Z E[X\mid \mathcal{G}]:A].$$ Let us start with the left side. As $$ZX1_A \in L^1 (P)$$ according to dominance convergence theorem, $$ \lim_{n \to +\infty} \int_A \lvert Z_n X -ZX\rvert dP=0.$$ Therefore, $$\lim_{n \to +\infty} E[Z_nX: A]=E[ZX: A].$$

On the other hand, according to the characteristics of conditional expectation introduced above, $$\lim_{n \to +\infty} E[E[\lvert Z_n X-ZX\rvert \mid\mathcal{G}]]=0 $$, which leads $$E[E[Z_nX\mid \mathcal{G}]] \overset{n \to \infty}{\longrightarrow}E[E[ZX\mid \mathcal{G}]]$$ Therefore, considering $$Z_nE[X\mid \mathcal{G}]=E[Z_nX\mid \mathcal{G}]\quad a.s.$$, $$\lim_{n \to +\infty}E[Z_nE[X\mid \mathcal{G}]:A]=\lim_{n \to +\infty}E[E[Z_nX\mid \mathcal{G}]:A] =E[E[ZX\mid \mathcal{G}]:A]$$.

Overall, this means$$E[ZX: A]=\lim_{n \to +\infty}E[Z_nX:A]=\lim_{n \to +\infty}E[Z_n E[X\mid \mathcal{G}]:A]=E[E[ZX\mid \mathcal{G}]:A]$$ Thus, there RN-derivatives on $$\mathcal{G}$$ are a.s. equivalent. Namely, $$ E[ZX\mid \mathcal{G}]=ZE[X \mid \mathcal{G}]$$.
