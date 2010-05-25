###Definition

A **basis** of a [[free module|free R-module]] $M$ is a linear [[isomorphism]] $B\colon M \to \oplus_{i\in I}R$.

We see how this is equivalent to the classical definition of a basis as a linearly independent spanning set:

+-- {: .un_lemma}
######Lemma

A basis for a free $R$-module $M$ determines a unique generating set for $M$ of linearly independent elements of $M$. 
=--

+-- {: .proof}
###### Proof 
Fix a basis $B$ for $M$ over $R$.  Then let $a_i\coloneqq (\delta_{ij})_{j\in I}$ for each $i\in I$.  Since $B$ is an isomorphism, each $a_i$ determines a unique element $b_i \coloneqq B^{-1}(a_i)$.  Since every element of $M$ is of the form $B^-1(x)$ for $x\in \oplus_{i\in I}R$, and since every element of $\oplus_{i\in I}R$ can be written as a finite $R$-linear combination of the $a_i$, this proves that $\{b_i\}_{i\in I}$ generates $M$.  To show linear independence, we again apply $B$ and its linearity.  The result is immediate.
=--
