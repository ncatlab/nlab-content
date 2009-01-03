#Idea#

A _sieve_ is a formalization of the notion of [[cover]] in the context of [[sheaf and topos theory]].

The motivating example is from the category [[Top]] of topological spaces. Take $c = X$ to be any topological space and let $\{d_i\} = \{U_i\}$ be a cover of $X$ by open subsets $U_i$ in the ordinary sense (i.e. each $U_i$ is an open subset of $X$ and their joint union is $X$, $\cup_i U_i = X$), then 
$\pi : (\sqcup_i U_i) \stackrel{\sqcup_i U_i \hookrightarrow_i X}{\to} X$ is a _cover_ of $X$. 

The **idea of sieves** is to regard such a cover of an object in a category as a [[presheaf]] on that category.

A choice of collections of morphism $d \to c$ into an object $c \in C$  for each $d \in C$ reminds one of the [[representable functor]] [[presheaf]]
$\hom_C(-, c): C^{op} \to Set$ which assigns to each $d \in C$ the set of _all_ morphisms from $d$ to $c$. Every choice of covers of $c$ is therefore for each $d \in C$ a subset of the value of this functor evaluated at $d$. This begins to look like an [[monomorphism|monic]] [[natural transformation]] into this functor. Indeed, it turns out that one can assume without restriction of generality that the assignment of covers of $c$ can always be extended to such a monic natural transformation, and hence one formalizes the notion of "collection of covers" of $c$ as a [[subobject]] $i: F \hookrightarrow \hom(-, c)$ of the functor represented by $c$: a _sieve_ at $c$. 

For instance, in the topological example considered above, each open covering $\sqcup_i U_i \to X$ induces a subfunctor $\bigcup_i \hom(-, U_i) \to \hom(-, X)$ where on the left we take a union of subfunctors $\hom(-, U_i) \to \hom(-, X)$. 

#Definition#

+-- {: .un_defn}
###### Definition
A _sieve_ (Fr. _crible_) on an object $c$ is a subfunctor (a [[subobject]] in the [[functor category]]) of the [[representable functor]] $\hom_C(-, c): C^{op} \to Set$. 
=--

Thus, a sieve on $c$, $i: F \hookrightarrow \hom(-, c)$, may be described as a function which assigns to each object $d$ a collection of morphisms $f: d \to c$ into $c$. Naturality of the inclusion $i$ means that whenever $f: d \to c$ belongs to the sieve and $g: e \to d$ is any morphism, then $f g: e \to c$ also belongs to the sieve. 

Sometimes this condition (of a sieve being closed under the operation of pulling back along an arbitrary morphism $g: e \to d$) is called a "saturation condition". At any rate, given any collection of morphisms targeted at $c$, we can always close it up or saturate it, to obtain a sieve on $c$. 

Notice that because the pullback of a subfunctor $i: F \hookrightarrow \hom(-, c)$ along any morphism $\hom(-, g): \hom(-, d) \to \hom(-, c)$ is again a subfunctor $g^* F$ of $d$, sieves are closed under pulling back. Concretely, 

$$g^* F = \bigcup_{e \in Ob(C)} \{f: e \to d: g f \in F\}
\,.$$

#Remarks#

* Sieves are used to define [[Grothendieck topology]] and [[site]].