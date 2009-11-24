#Classical Morita theorem#

Given rings $R$ and $S$, the following properties are equivalent

1. The categories of left $S$-modules and left $R$-modules are equivalent;
1. The categories of right $S$-modules and right $R$-modules
are equivalent;
1. There are bimodules ${}_R M_S$ and ${}_S N_R$ such that $\otimes_R M$ and $\otimes_S N$ form an adjoint equivalence between the category of right $S$- and the category of right $R$-modules;
1. The ring $R$ is isomorphic to the endomorphism ring of a [[generator]] in the category of left (or right) $S$-modules;
1. The ring $S$ is isomorphic to the endomorphism ring of a [[generator]] in the category of left (or right) $R$-modules.

+-- {: .query}
[[Dmitri Pavlov]]: Tsit-Yuen Lam in his book "Lectures on modules and rings" on pages 488 and 489 states the Morita equivalence theorem using progenerators (i.e., finitely generated projective generators) instead of just generators.  Are these two versions equivalent?
=--

+-- {: .query}
[[Dmitri Pavlov]]: I would like to state the Morita equivalence theorem as a 2-equivalence between two bicategories: The bicategory of rings, bimodules and their intertwiners and the bicategory of abelian categories that are equivalent to the category of modules over some ring (i.e., abelian categories that have all small coproducts and a compact projective generator), Eilenberg-Watts functors between these categories (i.e., right exact functors that commute with direct sums) and natural transformations.  Is it possible to do this and what is the precise statement then?
=--

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

A **Morita morphism** of [[Lie groupoids]] is, even though it is not typically made explicit in the literature, precisely a (local) acyclic fibration with respect to the [[folk model structure]] on groupoids, which in turn is the same as an [[anafunctor]] of Lie groupoids. 
A Morita equivalence of Lie groupoids then is a span as above, equivalently an invertible anafunctor.
+--{: .query}
[[David Roberts]]: More precisely, a Morita morphism is a span of Lie groupoids such that the \'source leg\' has an anafunctor pseudoinverse. Anafunctors are only examples of Morita morphisms, in the sense that open covers $\coprod U_i \to M$ are examples of surjective submersions.

I'm also not sure that this should be called the folk model structure, as I don't think it exists for groupoids internal to $Diff$. Details of the model structure are in a paper by Everaert, Kieboom and van der Linden, but seem to be tailored towards groupoids internal to categories of algebraic things (e.g semiabelian categories). I think the best one can do is a category of fibrant objects, but that is not something I've looked at much.

_Toby_:  For me, an anafunctor involves a surjective submersion rather than an open cover, which is how that got in there.  The important thing is to have equivalent hom-categories.

[[David Roberts]]: I'm not what I was thinking at the time, but you are pretty much right: the definition of anafunctors depends on a choice of a subcanonical singleton [[Grothendieck pretopology]], so it was remiss of me to demand the use of open covers :) As for the definition of Morita morphism, I now can't remember if that referred to the span which is an arrow in the localised 2-category or the arrow in the unlocalised 2-category that is sent to an equivalence under localisation. At least for me, the terminology Morita morphism evokes the generalisation from a Morita equivalence (a span of weak equivalences) to a more general morphism in that setting.

_Toby_:  I think that a Morita morphism should be a span, although now I\'m not sure that this is what the text says, is it?  I should check a reference and then change it.

[[David Roberts]]: I'm fairly sure I've heard Lie groupoid people (Ping Xu springs immediately to mind) speak about a Morita morphism as being a fully faithful, essentially surjective (in the appropriate sense) internal functor, but I disagree with their usage. If this is indeed the case, we could note the terminological discrepancies
=--
Lie groupoids up to Morita equivalence are equivalent to [[differentiable stack]]s. This relation between Lie groupoids and their stacks of torsors is analogous to the relation between algebras and their categories of modules, which is probably the reason for the choice of terminology.

+-- {: .query}

So is it true that there is a model category structure on algebras such that Morita equivalences of algebras are spans  of acyclic fibrations with respect to that structure?

[[Zoran Škoda]]: Associative (nonunital) algebras make a [[semi-abelian category]], ins't it ? So one could then apply
the general results of van den Linden published in TAC to 
get such a result, using regular epimorphism pretopology, it seems to me. It is probably known to the experts in this or another form. 

=--

[[!redirects Morita equivalences]]