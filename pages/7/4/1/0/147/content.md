#Idea#

The structure of a _site_ on a [[category]] $C$ is a structure that regards each [[object]] $c$ of $C$ as a [[space and quantity|space]] and determines which [[morphism]]s $\pi : d \to c$ from collections $d := \{\sqcup_i d_i\}$ of [[object]]s of $C$ to $c$ behave as _covers_ of spaces.

## Examples

* In the category [[Top]] of topological spaces take $c = X$ to be any topological space and let $\{d_i\} = \{U_i\}$ be a cover of $X$ by open subsets $U_i$ in the ordinary sense (i.e. each $U_i$ is an open subset of $X$ and their joint union is $X$, $\cup_i U_i = X$), then 
$\pi : (\sqcup_i U_i) \stackrel{\sqcup_i U_i \hookrightarrow_i X}{\to} X$ is a _cover_ of $X$ in the general sense of sites. 

##Formalization

A choice of collections of morphism $d \to c$ into an object $c \in C$  for each $d \in C$ reminds one of the [[representable functor]] [[presheaf]]
$\hom_C(-, c): C^{op} \to Set$ which assigns to each $d \in C$ the set of _all_ morphisms from $d$ to $c$. Every choice of covers of $c$ is therefore for each $d \in C$ a subset of the value of this functor evaluated at $d$. This begins to look like an [[monomorphism|monic]] [[natural transformation]] into this functor. Indeed, it turns out that one can assume without restriction of generality that the assignment of covers of $c$ can always be extended to such a monic natural transformation, and hence one formalizes the notion of "collection of covers" of $c$ as a [[subobject]] $i: F \hookrightarrow \hom(-, c)$ of the functor represented by $c$: a _sieve_ at $c$. 

For instance, in the topological example considered above, each open covering $\sqcup_i U_i \to X$ induces a subfunctor $\bigcup_i \hom(-, U_i) \to \hom(-, X)$ where on the left we take a union of subfunctors $\hom(-, U_i) \to \hom(-, X)$. 

#Definition#

* A _sieve_ (Fr. _crible_) on an object $c$ is a subfunctor of the [[representable functor]] $\hom_C(-, c): C^{op} \to Set$. 

Thus, a sieve on $c$, $i: F \hookrightarrow \hom(-, c)$, may be described as a function which assigns to each object $d$ a collection of morphisms $f: d \to c$ into $c$. Naturality of the inclusion $i$ means that whenever $f: d \to c$ belongs to the sieve and $g: e \to d$ is any morphism, then $f g: e \to c$ also belongs to the sieve. 

Sometimes this condition (of a sieve being closed under the operation of pulling back along an arbitrary morphism $g: e \to d$) is called a "saturation condition". At any rate, given any collection of morphisms targeted at $c$, we can always close it up or saturate it, to obtain a sieve on $c$. 

Notice that because the pullback of a subfunctor $i: F \hookrightarrow \hom(-, c)$ along any morphism $\hom(-, g): \hom(-, d) \to \hom(-, c)$ is again a subfunctor $g^* F$ of $d$, sieves are closed under pulling back. Concretely, 

$$g^* F = \bigcup_{e \in Ob(C)} \{f: e \to d: g f \in F\}$$

* A Grothendieck topology $J$ on a category $C$ assigns to each object $c$ a collection of sieves on $c$ which are called _covering sieves_, satisfying the following axioms: 

  *  If $F$ is a sieve that covers $c$ and $g: d \to c$ is any morphism, then the pullback sieve $g^* F$ covers $d$. 

  * The maximal sieve $id: \hom(-, c) \hookrightarrow \hom(-, c)$ is always a covering sieve; 

  * Two sieves $F, G$ of $c$ cover $c$ if and only if their intersection $F \cap G$ covers $c$.  

  * If $F$ is a sieve on $c$ such that the sieve 
    $\bigcup_d \{g: d \to c| g^* F \; covers \; d\}$
    is a covering sieve of $c$, then $F$ itself covers $c$. 

The set of covering sieves of an object $c$ is denoted $J(c)$, and the first axiom guarantees that we have a functor $J: C^{op} \to Set$. A **site** is a category $C$ equipped with a Grothendieck topology $J$. 


## Comparison with Lawvere-Tierney topologies ##

...

+--{.query}
I admit this article is brutally abstract. One thing it will need is illustrative examples, and it could probably stand gentler exposition. -- [[Todd Trimble|Todd]]

[[Urs Schreiber|Urs]] says: I have now tried to expand a bit on the "Idea" part and provided a motivating example there. 
Moreover, I moved the definition of [[sheaf]] to a separate entry. Below I give links to the existing entries [[stack]] and [[infinity-stack]], which I had written. It would be desireable to eventually harmonize the discussion at [[infinity-stack]] with the discussion here a bit more and expand on the relation between the two.
=--


#Remarks#

On a category equipped with the structure of a site one can consider 

 * [[sheaf|sheaves]]

 * [[stack|stacks]]

 * [[infinity-stack|infinity stacks]].

