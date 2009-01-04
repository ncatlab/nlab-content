#Idea#

A _Grothendieck topology_ on a category is a choice of morphisms in that category which are regarded as [[cover|covers]].

A category equipped with a Grothendieck topology is a [[site]].  Sometimes all sites are required to be [[small category|small]].

Probably the main point of having a site is so that one can define [[sheaf|sheaves]], or more generally [[stack|stacks]], on it.  In particular, the category of sheaves on a (small) site is a [[Grothendieck topos]].

#Definition#

+-- {: .un_defn}
###### Definition
A _Grothendieck topology_ $J$ on a category $C$ assigns to each object $c$ a collection of [[sieve|sieves]] on $c$ which are called _covering sieves_, satisfying the following axioms: 

*  If $F$ is a [[sieve]] that covers $c$ and $g: d \to c$ is any morphism, then the pullback sieve $g^* F$ covers $d$. 

* The maximal [[sieve]] $id: \hom(-, c) \hookrightarrow \hom(-, c)$ is always a covering sieve; 

* Two [[sieve|sieves]] $F, G$ of $c$ cover $c$ if and only if their intersection $F \cap G$ covers $c$. (Here the saturation condition is important.) 

* If $F$ is a sieve on $c$ such that the sieve 
    $\bigcup_d \{g: d \to c| g^* F \; covers \; d\}$
    is a covering sieve of $c$, then $F$ itself covers $c$. 
=--

The set of covering sieves of an object $c$ is denoted $J(c)$, and the first axiom guarantees that we have a functor $J: C^{op} \to Set$.

## Comparison with Lawvere-Tierney topologies ##

There is a beautifully compact and elegant description of Grothendieck topologies by means of [[Lawvere-Tierney topology|Lawvere-Tierney topologies]]: 

Grothendieck topologies as described above are special cases: a Grothendieck topology on $C$ is equivalent to a [[Lawvere-Tierney topology]] on the presheaf topos $Set^{C^{op}}$. We proceed to unpack this equivalence. 

In the first place, we need to understand the subobject classifier in $E = Set^{C^{op}}$. But according to the definition, $\Omega$ is simply the representing object for the functor 

$$Sub: E^{op} \to Set$$ 

which takes an object $F$ of $E$ to the collection of subobjects of $F$, $Sub(F)$. In other words, $Sub(F) \cong \hom_E(F, \Omega)$. Applied to $F = \hom_C(-, c)$, we have then 

$$Sub(\hom_C(-, c)) \cong \hom_{Set^{C^{op}}}(\hom_C(-, c), \Omega) \stackrel{Yoneda}{\cong} \Omega(c)$$ 

In other words, we find that the functor $\Omega: C^{op} \to Set$ is defined by 

$$\Omega(c) = \{sieves on c\}$$ 

Next, if $J$ is a Grothendieck topology on $C$, then the collection of $J$-covering sieves on $c$ [which we denoted by $J(c)$] is a subcollection of all sieves on $c$, and so we have an inclusion 

$$J(c) \hookrightarrow \Omega(c)$$ 

and this inclusion is natural in $c$, by virtue of the first axiom on covering sieves. Thus we have a subobject

$$J \hookrightarrow \Omega$$ 

and again, by definition of subobject classifier, this subobject corresponds to a uniquely determined element 

$$j \in \hom_E(\Omega, \Omega)$$ 

which is just the Lawvere-Tierney operator $j: \Omega \to \Omega$. 

The other axioms for covering sieves translate neatly into properties of $j$. 

...

#Terminology#

The term "topology" for this concept is hallowed by tradition and the name of Grothendieck, but some people consider it to be somewhat unfortunate. While "a category equipped with a (Grothendieck) topology" is, in fact, sort of a generalization of "a set equipped with an (ordinary) topology," the relationship between a category and its topology is quite different from the relationship between a set and its topology.  In particular, when we construct a site from a topological space, the objects of the category are the _open sets_, not the points, of the space.

This use of "topology" can also lead to confusion since for a topologist, there is a completely different and very natural meaning of "topology on a category:" namely, topologies on its sets of objects and morphisms making it into an [[internalization|internal category]] in [[Top]].  The topologist's definition is, of course, a conservative extension of the classical notions of "topology on a set" and even "topology on a group," while there are no nontrivial Grothendieck topologies on a group considered as a 1-object category.

Furthermore, the use of "topology" for a category with a system of covers also leads to the use of "continuous" for a functor which preserves covers.  This is (in some people's opinion) doubly unfortunate, since "continuous functor" is used not only by topologists to mean an internal or [[enriched category|enriched]] functor over Top, but also by many category-theorists to mean a functor that preserves all small [[limit|limits]].  This is especially confusing since covers are more akin to colimits than limits. Moreover, while a continuous function between topological spaces does induce a a cover-preserving functor between categories of open sets, the function and the functor go in opposite directions.

In _Sketches of an Elephant_, Peter Johnstone introduced the term __(Grothendieck) coverage__ for a system of covers on a category.  (To be precise, he used "Grothendieck coverage" for what is traditionally called a "Grothendieck topology," and "coverage" for what is traditionally called a "basis for a Grothendieck topology"---another confusing word, since it has little to do with the usual notion of basis for a topology.)  He used __local operator__ instead of  "Lawvere-Tierney topology," but one could easily say "Lawvere-Tierney coverage" to retain the attribution.
