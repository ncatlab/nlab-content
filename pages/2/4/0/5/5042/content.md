
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[dg-Lie algebras]] may be thought of (see [[relation between L-∞ algebras and dg-Lie algebras|here]]) as the "strict" [[strong homotopy Lie algebras]]. As such they support a [[homotopy theory]]. The _[[model category]]_ structure on dg-Lie algebras is one way to present this homotopy theory. This is used for instance in [[deformation theory]], see at _[[formal moduli problems]]_.

For dg-Lie algebras in positive degree and over the rational numbers this model structure, due to ([Quillen 69, theorem II](#Quillen69)) is one of the algebraic models for presenting [[rational homotopy theory]] (see there) of [[simply connected topological spaces]].

## Definition

+-- {: .num_prop #ProjectiveModelStructureOndgLieAlgebras}
###### Proposition

There exists a [[model category]] structure $(dgLie_k)_{proj}$ on the category $dgLie_k$ of [[dg-Lie algebras]] over a commutative [[ring]] $k \supset \mathbb{Q}$ such that

* [[fibrations]] the [[surjective maps]]

* [[weak equivalences]] the [[quasi-isomorphisms]] on the underlying [[chain complexes]].

=--

For dg-Lie algebras in degrees $ \geq n \geq 1$, this is due to [Quillen 69](#Quillen69). For unbounded dg-Lie algebras this is due to ([Hinich 97](#Hinich97)).


This becomes a [[simplicial category]] with simplicial [[mapping spaces]] given by

$$
  dgLie(\mathfrak{g}, \mathfrak{h})
   \coloneqq
  ([k] \mapsto Hom_{dgLie}(\mathfrak{g} , \Omega^\bullet(\Delta^k) \otimes\mathfrak{h}))
  \,,
$$

where 

* $\Omega^\bullet(\Delta^k)$ is the [[dg-algebra]] of [[polynomial differential forms]] on the $k$-[[simplex]];

* $\Omega^\bullet(\Delta^k)\otimes \mathfrak{h}$ is the canonical dg-Lie algebra structure on the [[tensor product]].

([Hinich 97, 4.8.2](#Hinich97), following [Bousfield-Gugenheim 76](model structure on dg-algebras#HomComplexes))

This enrichment satisfies together with the model structure some of the properties of a [[simplicial model category]] ([Hinich 97, 4.8.3, 4.8.4](#Hinich97)), but not all of them.


## Properties
 {#Properties}

### Relation to $L_\infty$-algebras
 {#RectificationResolution}

dg-Lie algebras with this model structure are a _rectification_ of [[L-∞ algebras]]: for $Lie$ the [[Lie operad]] and $\widehat Lie$ its standard [[cofibrant resolution]], [[algebras over an operad]] over $Lie$ in chain complexes are [[dg-Lie algebras]] and algebras over $\widehat Lie$ are [[L-∞ algebras]] and by the rectification result discussed at _[[model structure on dg-algebras over an operad]]_ there is an induced [[Quillen equivalence]]

$$
  Alg(\widehat Lie) \stackrel{\simeq}{\to} Alg(Lie)
$$

between the [[model structure for L-∞ algebras]] which is [[transferred model structure|transferred]] from the  [[model structure on chain complexes]] (unbounded propjective) to the above model structure on chain complexes.

There is also a [[Quillen equivalence]] from the model structure on dg-Lie algebras to the [[model structure on dg-coalgebras]]. This is part of a web of Quillen equivalences that identifies dg-Lie algebra/$L_\infty$-algebras with [[infinitesimal object|infinitesimal]] [[derived stack|derived]] [[∞-stacks]] ("[[formal moduli problems]]"). More on this is at _[[model structure for L-∞ algebras]]_.

Specifically, there is ([Quillen 69](#Quillen)) an [[adjunction]]

$$
  (\mathcal{R} \dashv i) \;\colon\;
  dgLie \stackrel{\overset{\mathcal{R}}{\leftarrow}}{\underset{i}{\to}} dgCoCAlg 
$$

between [[dg-coalgebras]] and dg-Lie algebras, where the [[right adjoint]] is the (non-full) inclusion that regards a dg-Lie algebra as a [[differential graded coalgebra]] with co-binary differential, and where the [[left adjoint]] $\mathcal{R}$ ("rectification") sends a dg-coalgebra to a dg-Lie algebra whose underlying graded [[Lie algebra]] is the [[free Lie algebra]] on the underlying [[chain complex]]. Over a [[field]] of [[characteristic]] 0, this adjunction is a [[Quillen equivalence]] between the [[model structure for L-∞ algebras]] on $dgCoCAlg$ and the model structure on $dgLie$ ([Hinich 98, theorem 3.2](#Hinich98)).

In particular, therefore the composite $i \circ \mathcal{R}$ is a [[resolution]] functor for $L_\infty$-algebras.

For more see at *[[relation between L-∞ algebras and dg-Lie algebras]]*.

### Relation to dg-coalgebras
 {#RelationToDgCoalgebras}

Via the above relation to $L_\infty$-algebras, dg-Lie algebras are also connected by a composite adjunction to [[dg-coalgebras]]. We dicuss the direct adjunction.

Throughout, let $k$ be of [[characteristic zero]].

+-- {: .num_defn #CEfunctor}
###### Definition
**(Chevalley-Eilenberg dg-coalgebra)**

Write

$$
  CE 
    \;\colon\;
  dgLieAlg_{k}
    \longrightarrow
  dgCocAlg_k
$$

for the [[Chevalley-Eilenberg algebra]] functor. It sends a dg-Lie algebra $(\mathfrak{g}, \partial, [-,-])$ to the [[dg-coalgebra]]

$$
  CE(\mathfrak{g},\partial,[-,-])
   \;\coloneqq\;
  \left(
    \vee^\bullet \mathfrak{g}[1]  
    ,\;
    D = \partial + [-,-]
  \right)
  \,,
$$

where on the right the extension of $\partial$ and $[-,-]$ to graded [[derivations]] is understood.

=--

For dg-Lie algebras concentrated in degrees $ \geq n \geq 1$ this is due to ([Quillen 69, appendix B, prop 6.2](#Quillen)). For unbounded dg-algebras, this is due to ([Hinich 98, 2.2.2](#Hinich98)).


+-- {: .num_defn #LeftAdjointToCEfunctor}
###### Definition

For $(X,D) \in dgCocalg_k$  write

  $$
    \mathcal{L}(X,D)
     \coloneqq
    \left(
       F(\overline{X}[-1]),\; 
       \partial \coloneqq D + (\Delta - 1 \otimes id - id \otimes 1)
    \right)
    \;\in dgLieAlg_k\;
  $$

  where
  
  1. $\overline{X} \coloneqq ker(\epsilon)$ is the [[kernel]] of the [[counit]], regarded as a [[chain complex]];

  1. $F$ is the [[free Lie algebra]] functor (as graded Lie algebras);

  1. on the right we are extending $(\Delta - 1 \otimes id - id \otimes 1) \colon \overline{X} \to \overline{X} \otimes \overline{X}$ as a Lie algebra [[derivation]] 


=--

For dg-Lie algebras concentrated in degrees $ \geq n \geq 1$ this is due to ([Quillen 69, appendix B, prop 6.1](#Quillen)). For unbounded dg-algebras, this is due to ([Hinich 98, 2.2.1](#Hinich98)).


+-- {: .num_prop #CEAdjunction}
###### Proposition

The [[functors]] from def. \ref{CEfunctor} and def. \ref{LeftAdjointToCEfunctor} are [[adjoint functor|adjoint]] to each other:

$$
  dgLieAlg_k
   \underoverset
     {\underset{CE}{\longrightarrow}}
     {\overset{\mathcal{L}}{\longleftarrow}}
     {\bot}
  dgCocAlg_k
  \,.
$$

Moreover, for $X \in dgCocAlg_k$ and $\mathfrak{g} \in dgLieAlg_k$ then the adjoint [[hom sets]] are [[natural isomorphism|naturally isomorphic]]

$$
  Hom(\mathcal{L}(X), \mathfrak{g})
   \simeq
  Hom(X, CE(\mathfrak{g}))
    \simeq
  MC(Hom(\overline{X},\mathfrak{g}))
$$

to the [[Maurer-Cartan elements]] in the Hom-dgLie algebra from $\overline{X}$ to $\mathfrak{g}$.


=--

For dg-Lie algebras concentrated in degrees $ \geq n \geq 1$ this is due to ([Quillen 69, appendix B, somewhere](#Quillen)). For unbounded dg-algebras, this is due to ([Hinich 98, 2.2.5](#Hinich98)).

+-- {: .num_prop #QuillenAdjunctionCE}
###### Proposition

The adjunction $(\mathcal{L} \dashv CE)$ from prop. \ref{CEAdjunction} is a [[Quillen adjunction]] between then projective [[model structure on dg-Lie algebras]] as the [[model structure on dg-coalgebras]]

$$
  (dgLieAlg_k)_{proj}
   \underoverset
     {\underset{CE}{\longrightarrow}}
     {\overset{\mathcal{L}}{\longleftarrow}}
     {\bot}
  (dgCocAlg_k)_{Quillen}
  \,.
$$

=--

([Hinich 98, lemma 5.2.2, lemma 5.2.3](#Hinich98))

Moreover:

+-- {: .num_prop}
###### Proposition

In non-negatively graded dg-coalgebras, both [[Quillen functors]] $(\mathcal{L} \dashv CE)$ from prop. \ref{QuillenAdjunctionCE} preserve all [[quasi-isomorphisms]], and both the [[adjunction unit]] and the [[adjunction counit]] are quasi-isomorphisms.

=--

For dg-algebras in degrees $\geq n \geq 1$ this is ([Quillen 76, theorem 7.5](#Quillen76)). In unbounded degrees this is ([Hinich 98, prop. 3.3.2](#Hinich98))

+-- {: .num_theorem}
###### Theorem

The Quillen adjunctin from prop. \ref{QuillenAdjunctionCE} is a [[Quillen equivalence]]:

$$
  (dgLieAlg_k)_{proj}
   \underoverset
     {\underset{CE}{\longrightarrow}}
     {\overset{\mathcal{L}}{\longleftarrow}}
     {{}_{\phantom{qu}}\simeq_{Qu}}
  (dgCocAlg_k)_{Quillen}
  \,.
$$


=--

([Hinich 98, theorem 3.2](#Hinich98)) using ([Quillen 76 II 1.4](#Quillen76))



### Relation to simplicial Lie algebras

The [[normalized chains complex]] functor from [[simplicial Lie algebras]] constitutes a [[Quillen adjunction]] from the projective [[model structure on simplicial Lie algebras]], see [there](model+structure+on+simplicial+Lie+algebras#QuillenAdjunctionTodgLieAlgebras).

## Related concepts

* [[model structure on dg-coalgebras]]

* [[model structure on simplicial Lie algebras]]

* [[model structure for L-∞ algebras]]

* [[relation between L-∞ algebras and dg-Lie algebras]]

## References

The model structure on dg-Lie algebras in [[characteristic zero]] and in  degrees $\geq n \geq 1$ goes back to 

* {#Quillen69} [[Dan Quillen]], section II.5 and appendix B of _Rational homotopy theory_, Annals of Math., 90(1969), 205&#8211;295 ([JSTOR](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf)) 
 
This is extended to a model structure on dg-Lie algebras in unbounded degrees in

* {#Hinich97} [[Vladimir Hinich]], _Homological algebra of homotopy algebras_, Comm. in algebra, 25(10)(1997), 3291&#8211;3323 ([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))

and the corresponding [[Quillen adjunction]] to the [[model structure on dg-coalgebras]] in unbounded degrees is discussed in

* {#Hinich98} [[Vladimir Hinich]], _DG coalgebras as formal stacks_, Journal of Pure and Applied Algebra Volume 162, Issues 2&#8211;3, 24 August 2001, Pages 209&#8211;250 ([arXiv:math/9812034](http://arxiv.org/abs/math/9812034))


See also section 2.1 of 

* [[Jacob Lurie]], _[[Formal moduli problems]]_

Review with discussion of [[homotopy limits]] and [[homotopy colimits]] is in 

* {#Walter06} [[Ben Walter]], section 4 of _Rational Homotopy Calculus of Functors_ ([arXiv:math/0603336](http://arxiv.org/abs/math/0603336))

[[!redirects model structures on dg-Lie algebras]]
