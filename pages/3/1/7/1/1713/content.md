The notion of fibration theory was created by James Wirth in his PhD thesis in 1965. It allows classification of what would now be called $\infty$-[[principal infinity-bundle|bundles]].


### The axioms ###

A *fibration theory* $E$ is an assignment of a [[category]] $E(B)$ to each [[topological space]] $B$ and a [[contravariant functor]] $f^*:E(C) \to E(B)$ to each continuous map $f:B \to C$ such that $id^*$ is the [[identity functor]]. $E$ is required to satisfy the following
+-- {: .query}
How can $id^*$ be an identity functor when that is not contravariant?  Maybe each $f^*$ is a covariant functor but the mapping $f \mapsto f^*$ is a contravariant functor?  But then it\'s automatic that $id^* = id$ (and furthermore that $(f ; g)^* = f^* \circ g^*$).  ---Toby

[[David Roberts]]: whoops! I didn't pick that up. I think you are partly right: it should be some sort of contravariant assignment $f\mapsto f^*$, but maybe not functorial (since I believe that *category* should be replaced as I said below). The protoypical example, AFAICS, is assigning the category of locally homotopy trival fibrations over the given space. It is not spelled out in detail in the paper.
=--

1. For a numerable open [[cover]] $U = \coprod U_i$ of a space $B$ and a system of objects (morphisms) $E_i$ over each $U_i$ such that $E_i$ and $E_j$ agree over $U_i\cap U_j$, then there is a unique common extension of the $E_i$ over $B$
   +-- {: .query}
   What makes an open cover 'numerable'?  ---Toby

[[David Roberts]]: A cover is numerable if it admits a subordinate partition of unity. [[numerable open cover|Numerable open covers]] form a site. The axiom is there to link locally homotopically trivial fibrations and Dold fibrations (see theorem 2.3 in Wirth-Stasheff, due to Dold.) 

Also, the uniqueness should at least be demoted to unique-up-to-isomorphism.
   =--
1. If $\phi$ is a morphism in $E(B)$ such that each restriction $\phi|_{U_i}$ for a numerable open cover $U$ of $B$ is a [[homotopy equivalence]], then $\phi$ is a homotopy equivalence. If $H\in E(I\times B)$, then the restrictions $H|_{\{t\}\times B}$ are homotopy equivalent (for objects) or homotopic (for morphisms)
1. (Mapping cylinder axiom) If $\phi:F \to F' \in E(B)$ is a homotopy equivalence, then there is an object $M(\phi)\in E(I\times B)$ which serves as a *mapping cylinder* for $\phi$. That is, $M(\phi)$ restricts to $F$ at $t=0$ and to $F'$ at $t=1$ with a characterising homotopy equivalence $\psi_M:M(\phi) \to I\times F'$ which restricts to $\{0\}\times\phi$, respectively $\{1\}\times id$.

+--{: .query}
[[David Roberts]]: The axioms are just copied from Wirth--Stasheff JHRS 1(1) 2006, p 273. They need to be clarified a little, as the notion of homotopy and homotopic are undefined. We could ask that $E(B)$ is a category of fibrant objects or a Quillen model category or $(\infty,1)$-category or a category with an interval objects or something. One could even ask for a subcategory of $Top$ which is closed under some conditions. In that instance, something needs to be said about the compatibility of homotopies etc with the functors $f^*$.

_Toby_:  I know that you\'re just copying things, so maybe you don\'t know the answers to my questions, but so far I don\'t even understand the parts that I should be able to understand!
=--
