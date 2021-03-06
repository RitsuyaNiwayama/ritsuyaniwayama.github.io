---
layout: post
title: "Completion of the measure space"
date: 2021-09-23 5:00:30 -0000
categories: Probability
page.mathjax: true
---
Here we prove a few propositions related to completion of the probability space. 
<h1>The definition of Null set</h1>
Let $$(\Omega,\mathcal{F},P)$$ be a probability space. $$N$$ ($$\subset \Omega$$) is called null set if $$N$$ fulfils
$$ N \subset \widetilde{N}$$, $$P(\widetilde{N})=0$$. The set of all null sets for a given probability measure $$P$$ will write here $$\mathcal{N}^P$$. If $$\mathcal{N}^P \subset \mathcal{F}$$, the probability measure ($$\mathcal{F},P$$) is complete, which is the definition of the completeness. Completion means "adding $$\mathcal{N}^P$$ to $$\mathcal{F}$$ so that $$P$$ is complete". Below, we describe a concrete process of the completion.


<h1>An extension of the sigma algebra</h1>

$$\widetilde{\mathcal{F}} \stackrel{\text{def.}}{=} \{B \subset \Omega; \text{There exists } A,\widetilde{A}\in \mathcal{F}, A\subset B \subset \widetilde{A}, P(\widetilde{A} \setminus A)=0\}$$

First, we prove the proposition that $$ \widetilde{\mathcal{F}} = \sigma[\mathcal{F} \cup \mathcal{N}^P]$$. The right side is the minimum sigma algebra including $$\mathcal{F} \cup \mathcal{N}^P$$. Let us prove the proposition.

First, we show $$ \widetilde{\mathcal{F}} \subset \sigma[\mathcal{F} \cup \mathcal{N}^P]$$. Let us select arbitrarily a $$ B \in \widetilde{\mathcal{F}}$$. There exists $$A,\widetilde{A}\in \mathcal{F}, A\subset B \subset \widetilde{A}, P(\widetilde{A} \setminus A)=0$$. Because $$B \setminus A \subset \widetilde{A} \setminus A$$ and $$P(\widetilde{A} \setminus A)=0$$, $$B \setminus A \in \mathcal{N}^P$$. Thus $$B(=A+ B \setminus A) \in \sigma[\mathcal{F} \cup \mathcal{N}^P]$$.

Second, we show $$ \widetilde{\mathcal{F}} \supset \sigma[\mathcal{F} \cup \mathcal{N}^P]$$. Any $$A \in \mathcal{F}$$ fulfils $$A \subset A \subset A, P(A \setminus A)=P(\emptyset)=0$$, so$$\widetilde{\mathcal{F}} \supset \mathcal{F}$$. Any $$N \in \mathcal{N}^P$$ has at least one $$A \supset N, P(A)=0$$, so $$ \emptyset \subset N \subset A, P(A \setminus \emptyset)=P(A)=0$$, which means $$\widetilde{\mathcal{F}} \supset \mathcal{N}^P$$. Therefore, $$\widetilde{\mathcal{F}} \supset \mathcal{F} \cup \mathcal{N}^P$$. Now if we show that $$\widetilde{\mathcal{F}}$$ is a sigma algebra, it is sufficient to show $$ \widetilde{\mathcal{F}} \supset \sigma[\mathcal{F} \cup \mathcal{N}^P]$$ because the  $$\sigma[\mathcal{F} \cup \mathcal{N}^P]$$ is the minimum sigma algebra including $$\mathcal{F} \cup \mathcal{N}^P$$ by definition.

- First, $$\emptyset (\in \mathcal{F})$$ fulfils $$\emptyset \subset \emptyset \subset \emptyset, P(\emptyset \setminus \emptyset)=P(\emptyset)=0$$, which means $$\emptyset \in \widetilde{\mathcal{F}}$$. 
- Second, for any $$B \in \widetilde{\mathcal{F}}$$, there are $$A,\widetilde{A}\in \mathcal{F}, A\subset B \subset \widetilde{A}, P(\widetilde{A} \setminus A)=0$$. Because $$A,\widetilde{A}\in \mathcal{F}$$, $$\Omega \setminus A,\Omega \setminus \widetilde{A}\in \mathcal{F}$$, and $$\Omega \setminus A \supset \Omega \setminus B \supset \Omega \setminus \widetilde{A}$$. Here, $$P(\{\Omega \setminus A\} \setminus \{\Omega \setminus \widetilde{A}\})=P(\widetilde{A} \setminus A)=0$$. Therefore, $$\Omega \setminus B \in \widetilde{\mathcal{F}}$$.
- Third, let be $$ A_i,\widetilde{A_i}\in \mathcal{F}, A_i\subset B_i \subset \widetilde{A_i}, P(\widetilde{A_i} \setminus A_i)=0, (i=1,2,3,...)\}$$. Then $$A=\cup A_i\subset B=\cup B_i \subset \widetilde{A}=\cup \widetilde{A_i}, P(\widetilde{A} \setminus A)\leq P(\cup ( \widetilde{A_i} \setminus A_i)) \leq \Sigma P(\widetilde{A_i} \setminus A_i)=0$$. Therefore, $$ B=\cup B_i \in \widetilde{\mathcal{F}}$$.

Thus, $$\widetilde{\mathcal{F}}$$ is a sigma algebra, so $$ \widetilde{\mathcal{F}} \supset \sigma[\mathcal{F} \cup \mathcal{N}^P]$$. Overall, $$ \widetilde{\mathcal{F}} = \sigma[\mathcal{F} \cup \mathcal{N}^P]$$.

<h1>An extention of the measure</h1>
For a $$B \in \widetilde{\mathcal{F}}$$, we define a measure $$\widetilde{P}$$ by $$\widetilde{P}(B)=P(A)$$, where $$A,\widetilde{A}\in \mathcal{F}, A\subset B \subset \widetilde{A}, P(\widetilde{A} \setminus A)=0$$.

Is this really a measure? This question is actually composed of two sub-questions. 1) Is the value of $$\widetilde{P}(B)$$ unique for all $$B$$? 2) Does $$\widetilde{P}(B)$$ have sigma additivity?

Here we prove the uniqueness of the value of $$\widetilde{P}(B)$$, which means the value does not depend on the choice of $$A,\widetilde{A} \in \mathcal{F}$$. Let be $$A_1,\widetilde{A_1},A_2,\widetilde{A_2} \in \mathcal{F}$$, fulfiling $$ A_i\subset B \subset \widetilde{A_i}, P(\widetilde{A_i} \setminus A_i)=0, i =1,2$$. Here what we want to show is $$P(A_1)=P(A_2)$$, meaning that the value of $$P(B)$$ does not depend on the choice of$$A, \widetilde{A}$$.

$$P(A_1)= P(A_1 \cap A_2)+P(A_1 \setminus A_2)$$, and as $$A_1 \subset \widetilde{A_2}$$, $$0 \leq P(A_1 \setminus A_2) \leq P(\widetilde{A_2} \setminus A_2) =0$$. Thus,$$P(A_1)=P(A_1 \cap A_2)$$. Similarly, $$P(A_2)=P(A_1 \cap A_2)$$, which leads $$P(A_1)=P(A_2)$$. Thus, $$P(B)$$ does not depend on the choice of $$A, \widetilde{A}$$.

Next, we prove the sigma additivity of $$\widetilde{P}(B)$$. $$\widetilde{P}(\emptyset)=P(\emptyset)=0$$. Let be $$ A_i,\widetilde{A_i}\in \mathcal{F}, A_i\subset B_i \subset \widetilde{A_i}, P(\widetilde{A_i} \setminus A_i)=0, (i=1,2,3,...)$$. We also assume that $$B_i \cap B_j = \emptyset (i \neq j)$$. In this case $$A_i \cap A_j \leq B_i \cap B_j = \emptyset (i \neq j)$$. Meanwhile, $$A=\Sigma A_i\subset B=\Sigma B_i \subset \widetilde{A}=\cup \widetilde{A_i}, P(\widetilde{A} \setminus A)\leq P(\cup ( \widetilde{A_i} \setminus A_i)) \leq \Sigma P(\widetilde{A_i} \setminus A_i)=0$$, which leads $$\widetilde{P}(B)=P(A)$$. Because of the sigma additivity of $$P$$, $$P(A)=\Sigma P(A_i)=\Sigma \widetilde{P}(B_i)$$. Thus, we obtain $$\widetilde{P}(B)=\Sigma \widetilde{P}(B_i)$$. Thus, the sigma additivity of $$\widetilde{P}$$ was shown.

Thus, $$\widetilde{P}$$ is a probability measure.

<h1>Voil??, la compl??tion.</h1>
Here we show that $$\mathcal{N}^\widetilde{P}=\mathcal{N}^P$$. As $$ \widetilde{\mathcal{F}} = \sigma[\mathcal{F} \cup \mathcal{N}^P]$$, this means $$(\widetilde{F},\widetilde{P})$$ is complete.

$$\mathcal{N}^\widetilde{P} \subset \mathcal{N}^P$$: Let be $$B \in \mathcal{N}^\widetilde{P}$$. As $$B \in \mathcal{F}$$, there are $$A,\widetilde{A}\in \mathcal{F}, A\subset B \subset \widetilde{A}, P(\widetilde{A} \setminus A)=0$$, which also defines $$\widetilde{P}(B)=P(A)=0$$. This leads $$P(\widetilde{A})=0$$. Thus,$$B \subset \widetilde{A} \in \mathcal{F}: P(\widetilde{A})=0$$. This means $$B \in \mathcal{N}^P$$. Thus, $$\mathcal{N}^\widetilde{P} \subset \mathcal{N}^P$$.

$$\mathcal{N}^\widetilde{P} \supset \mathcal{N}^P$$: Let be $$N \in \mathcal{N}^P$$. This means there is $$A (\in \widetilde{F}) \supset N$$, fulfiling $$P(A)=0$$. From the definition of $$\widetilde{P}$$, $$\widetilde{P}(A)=0$$. Therefore $$N \in \mathcal{N}^\widetilde{P}$$. Thus, $$\mathcal{N}^\widetilde{P} \supset \mathcal{N}^P$$.

Thus, $$(\widetilde{F},\widetilde{P})$$ is complete.
