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

+--{+ .query}
[[Zoran Škoda]]: Urs, it does not make sense part of what you originally wrote: the Morita equivalence is NOT a morphism of algebras which induces an equivalence. The equivalence is given by a pair of bimodules, not a morphism of algebras. So one can view them as an invertible 1-cell in a 2-category $\mathrm{Rng}$, but not as a special 1-cell in 1-category of rings as you wrote. 

By the way, in this entry below I like to avoid word context, because word "context" in Morita theory has a specific meaning (Morita context). 
=--

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

=--
