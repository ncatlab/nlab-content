
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
**Morita equivalence** is a categorical concept of equivalence that is in general weaker than [[isomorphism]] or [[equivalence]] (of category). The concept has originated in [[ring theory]] in K. Morita's groundbreaking investigation into the equivalence relation between rings $R, S$ induced by an equivalence $Mod_R\cong Mod_S$ of their category of modules.

Nowadays, the term is applied in different but closely related senses in a wide range of mathematical fields, and one speaks of _Morita equivalent_ [[categories]], [[algebraic theories]], [[geometric theories]] and so on.

Typically, such Morita situations involve three ingredients: a 'syntactic' ground level to which the respective concept of _Morita equivalence_ applies, a 'hypersyntactic' level that obtains from an 'idempotent' completion, and a second process of completion to a 'semantic' level where the equivalence relation for the syntactic ground level is defined by plain equivalence of category e.g. Morita equivalence for _small categories_ is defined as equivalence of their presheaf categories with [[Cauchy completion]] as intermediate hypersyntactic level.

So the broad intuition is that Morita equivalence is a _coarse grained semantic equivalence that obtains between syntactic gadgets_ - basically two [[theory|theories]] that have up to equivalence the same category of [[model|models]]. The role of the intermediate hypersyntactic level in this analogy is that of an 'ideal syntax' (syntax classifier) that already reflects the relations at the semantic level. The categorical equivalence (via bimodules)  from the semantic level then shows up at the intermediate level as a ('Cauchy convergent'$\sim$ 'fgp-module') bidirectional _translation_ from one syntax into another.

## Classical Morita theorem

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

## Definitions

### In algebra

Two rings are **Morita equivalent** if the equivalent statements in Morita theorem above are true. A **Morita equivalence** is a weakly invertible 1-cell in the bicategory $\mathrm{Rng}$ of rings, bimodules and 
morphisms of bimodules.

A theorem in ring theory says that the [[center]] of a ring is isomorphic to the center of its category of modules and that Morita equivalent rings have isomorphic centers. Especially, two _commutative_ rings are Morita equivalent precisely when they are isomorphic!

This shows that the property of _having center $Z$ up to isomorphism_ is stable within Morita equivalence classes. Properties of this kind are sufficiently important to deserve a special name:

A property $P$ of rings is called a **Morita invariant** iff whenever $P$ holds for a ring $R$, and $R$ and $S$ are Morita equivalent then $P$ also holds for $S$. Another classical example is the property of being [[simple ring|simple]]. (cf. Cohn 2003)

### In homotopy theory 

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

### In Lie groupoid theory 

A **[[Morita morphism]] equivalence** of [[Lie groupoids]] is an [[anafunctor]] that is invertible, equivalently an invertible [[Hilsum-Skandalis morphism]]/[[bibundle]].

Lie groupoids up to Morita equivalence are equivalent to [[differentiable stack]]s. This relation between Lie groupoids and their stacks of torsors is analogous to the relation between algebras and their categories of modules, which is probably the reason for the choice of terminology.



## References

* wikipedia, _[Morita equivalence](http://en.wikipedia.org/wiki/Morita_equivalence)_

* P. M. Cohn, _Further Algebras and Applications_ , Springer Heidelberg 2003. (sec. 4.4-4.5 pp.148ff)

* [[Ralf Meyer]], _Morita equivalence in algebra and geometry_ ([[MeyerMoritaEquivalence.pdf:file]])

* [[Ross Street]], _Quantum Groups - A Path to Current Algebra_, Cambridge UP 2007. ([ps-draft](http://www-texdev.ics.mq.edu.au/Quantum/Quantum.ps))


[[!redirects Morita equivalences]]