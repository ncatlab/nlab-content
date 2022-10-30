#Classical Morita theorem#

Given rings $R$ and $S$, the following properties are equivalent

1. The categories of left $S$-modules and left $R$-modules are equivalent;
1. The categories of right $S$-modules and right $R$-modules
are equivalent;
1. There are bimodules ${}_R M_S$ and ${}_S N_R$ such that $\otimes_R M$ and $\otimes_S N$ form an adjoint equivalence between the category of right $S$- and the category of right $R$-modules;
1. The ring $R$ is isomorphic to the endomorphism ring of a [[generator]] in the category of left (or right) $S$-modules;
1. The ring $S$ is isomorphic to the endomorphism ring of a [[generator]] in the category of left (or right) $R$-modules.

#Definitions#

##In algebra##

Two rings are **Morita equivalent** if the equivalent statements in Morita theorem above are true. A **Morita equivalence** is a weakly invertible 1-cell in the bicategory $\mathrm{Rng}$ of rings, bimodules and 
morphisms of bimodules.


## In homotopy theory ##

In any [[homotopy theory]] framework a **Morita equivalence** between objects $C$ and $D$ is  a span 
$$
  C \lt \stackrel{\simeq}{\leftarrow}
  \hat C
  \stackrel{\simeq}{\to} \gt
  D
$$
where both legs are acyclic fibrations.

In particular, if the ambient [[homotopical category]] is a [[category of fibrant objects]], then the _factorization lemma_ (see there) ensures that _every_ weak equivalence can be factored as a span of acyclic fibrations as above. 

Important fibrant objects are in particular [[infinity-groupoid]]s (for instance [[Kan complex]]es are fibrant in the standard [[model structure on simplicial sets]] and [[omega-groupoid]]s are fibrant with respect to the Brown-Golasinski [[folk model structure]]). And indeed, Morita equivalences play an important role in the theory of groupoids with extra structure:

## In Lie groupoid theory ##

A **Morita morphism** of [[Lie groupoid]]s is, even though it is not typically made explicit in the literature, precisely a (local) acyclic fibration with respect to the [[folk model structure]] on groupoids, which in turn is the same as an [[anafunctor]] of Lie groupoids. 
A Morita equivalence of Lie groupoids then is a span as above, equivalently an invertible anafunctor.

Lie groupoids up to Morita equivalence are equivalent to [[differentiable stack]]s. This relation between Lie groupoids and their stacks of torsors is analogous to the relation between algebras and their categories of modules, which is probably the reason for the choice of terminology.

+-- {: .query}

So is it true that there is a model category structure on algebras such that Morita equivalences of algebras are spans  of acyclic fibrations with respect to that structure?

[[Zoran Škoda]]: Associative (nonunital) algebras make a semi-abelian category, ins't it ? So one could then apply
the general results of van den Linden published in TAC to 
get such a result, using regular epimorphism pretopology, it seems to me. It is probably known to the experts in this or another form. 
=--
