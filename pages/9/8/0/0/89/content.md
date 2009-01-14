#Definition#

## In algebra ##

In its original sense, a **Morita equivalence** is a morphism between two algebras which induces an equivalence on their respective categories of modules.

## In homotopy theory ##

In any [[homotopy theory]] context a **Morita equivalence** between objects $C$ and $D$ is  a span 

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

In the context of [[Lie groupoid]] theory a **Morita morphism** is, even though it is not generally made explicit in the literature, precisely a (local) acyclic fibration with respect to the [[folk model structure]] on groupoids, which in turn is the same as an [[anafunctor]] of Lie groupoids. 
A morita equivalence of Lie groupoids then is a span as above, equivalently a [[anafunctor|saturated anafunctor]].

Lie groupoids up to Morita equivalence are equivalent to [[differentiable stack]]s. This relation between Lie groupoids and their stacks of torsors is analogous to the relation between algebras and their categories of modules, which is probably the reason for the choice of terminology.

+-- {: .query}

So is it true that there is a model category structure on algebras such that Morita equivalences of algebras are spans  of acyclic fibrations with respect to that structure?

=--
