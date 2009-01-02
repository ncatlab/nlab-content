#Idea#

The structure of a _site_ on a category $C$ is a structure that regards each object of $C$ as a space and determines which morphisms from collections of objects of $C$ to a given object of $C$ behave as _covers_ of spaces.

#Definition#

* A _sieve_ (Fr. _crible_) on an object $c$ is a subfunctor of the [[representable functor]] $\hom_C(-, c): C^{op} \to Set$. 

Thus, a sieve on $c$, $i: F \hookrightarrow \hom(-, c)$, may be described as a function which assigns to each object $d$ a collection of morphisms $f: d \to c$ into $c$. Naturality of the inclusion $i$ means that whenever $f: d \to c$ belongs to the sieve and $g: e \to d$ is any morphism, then $f g: e \to c$ also belongs to the sieve. 

Sometimes this condition (of a sieve being closed under the operation of pulling back along an arbitrary morphism $g: e \to d$) is called a "saturation condition". At any rate, given any collection of morphisms targeted at $c$, we can always close it up or saturate it, to obtain a sieve on $c$. 

Notice that because the pullback of a subfunctor $i: F \hookrightarrow \hom(-, c)$ along any morphism $\hom(-, g): \hom(-, d) \to \hom(-, c)$ is again a subfunctor $g^* F$ of $d$, sieves are closed under pulling back. Concretely, 

$$g^* F = \bigcup_{e \in Ob(C)} \{f: e \to d: g f \in F\}$$

* A Grothendieck topology $J$ on a category $C$ assigns to each object $c$ a collection of sieves on $c$ which are called _covering sieves_, satisfying the following axioms: 
: If $F$ is a sieve that covers $c$ and $g: d \to c$ is any morphism, then the pullback sieve $g*F$ covers $d$. 
: The maximal sieve $id: \hom(-, c) \hookrightarrow \hom(-, c)$ is always a covering sieve; 
: Two sieves $F, G$ of $c$ cover $c$ if and only if their intersection $F \cap G$ covers $c$.  
: If $F$ is a sieve on $c$ such that the sieve 
$$\bigcup_d \{g: d \to c| g^*F \ covers\ d\}$$
is a covering sieve of $c$, then $F$ itself covers $c$. 

The set of covering sieves of an object $c$ is denoted $J(c)$, and the first axiom guarantees that we have a functor $J: C^{op} \to Set$. A **site** is a category $C$ equipped with a Grothendieck topology $J$. 

**Definition:** Given a site $(C, J)$, a _sheaf_ over that site is a presheaf 

$$X: C^{op} \to Set$$ 

such that whenever $i: F \hookrightarrow \hom(-, c)$ is a covering sieve, the map 

$$X(c) \stackrel{Yoneda}{\cong} Set^{C^{op}}(\hom(-, c), X) \stackrel{Set^{C^{op}}(i, X)}{\to} Set^{C^{op}}(F, X)$$ 

is an isomorphism. 

## Comparison with Lawvere-Tierney topologies ##

...

+--{.query}
I admit this article is brutally abstract. One thing it will need is illustrative examples, and it could probably stand gentler exposition. -- Todd
=--

