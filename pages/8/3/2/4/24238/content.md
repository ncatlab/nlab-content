
* [[Ulrik Buchholtz]], [[Egbert Rijke]]:

  **The real projective spaces in homotopy type theory**

  Proceedings of the 32nd Annual ACM/IEEE Symposium on Logic in Computer Science 

  LICS 2017 **86** (2017) 1–8

  [arxiv:1704.05770](https://arxiv.org/abs/1704.05770)

  [doi:10.5555/3329995.3330081](https://dl.acm.org/doi/10.5555/3329995.3330081)

on the [[real projective space]] in [[homotopy type theory]].



> **Abstract.** [[homotopy type theory|Homotopy type theory]] is a version of [[Martin-Löf dependent type theory|Martin-Löf type theory]] taking advantage of its [[relation between category theory and type theory|homotopical models]]. In particular, we can use and construct [[objects]] of [[homotopy theory]] and reason about them using [[higher inductive types]]. In this article, we construct the [[real projective spaces]], key players in [[homotopy theory]], as certain [[higher inductive types]] in [[homotopy type theory]]. The classical definition of [[real projective space|$\mathbb{R}P^n$]], as the [[quotient space]] identifying [[antipode|antipodal points]] of the [[n-sphere|$n$-sphere]], does not translate directly to homotopy type theory. Instead, we define $\mathbb{R}P^n$ by [[induction]] on $n$ simultaneously with its [[tautological line bundle|tautological bundle]] of $2$-element sets. As the base case, we take $\mathbb{R}P^{-1}$ to be the [[empty type]]. In the [[induction|inductive step]], we take $\mathbb{R}P^{n+1}$ to be the [[mapping cone]] of the projection map of the [[tautological line bundle|tautological bundle]] of $\mathbb{R}P^{n}$, and we use its universal property and the [[univalence axiom]] to define the [[tautological line bundle|tautological bundle]] on $\mathbb{R}P^{n+1}$. 
By showing that the total space of the [[tautological line bundle|tautological bundle]] of $\mathbb{R}P^n$ is the [[n-sphere]], we retrieve the classical description of $\mathbb{R}P^{n+1}$ as $\mathbb{R}P(n)$ with an $(n+1)$-cell [[space attachment|attached]] to it. The infinite dimensional [[real projective space]], defined as the [[sequential colimit]] of the $\mathbb{R}P^n$ with the canonical inclusion maps, is equivalent to the [[Eilenberg-MacLane space]] $K(\mathbb{Z}/2\mathbb{Z},1)$, which here arises as the subtype of the [[universe]] consisting of $2$-element types. Indeed, the infinite dimensional [[projective space]] classifies the $0$-sphere bundles, which one can think of as synthetic line bundles. 
These constructions in homotopy type theory further illustrate the utility of homotopy type theory, including the interplay of [[type theory|type theoretic]] and [[homotopy theory|homotopy theoretic]] ideas.

category: reference