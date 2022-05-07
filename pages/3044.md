+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[model category]] structure on the [[category]] of  [[dg-coalgebras]].

## Definition

Let $k$ be a [[field]] of [[characteristic]] 0.


+-- {: .num_prop #TheCETangentAdjunction}
###### Proposition

There is a pair of [[adjoint functors]]

$$
  (\mathcal{L} \dashv \mathcal{C})
  \;\colon\;
  dgLieAlg_k
   \underoverset
      {\underset{\mathcal{C}}{\longrightarrow}}
      {\overset{\mathcal{L}}{\longleftarrow}}
      {\bot}
  dgCoCAlg_k
$$

between the category of [[dg-Lie algebras]]and that of dg [[cocommutative coalgebras]], where the [[right adjoint]] sends a dg-Lie algebra $(\mathfrak{g}_\bullet, [-,-])$ to its [[Chevalley-Eilenberg algebras|Chevalley-Eilenberg coalgebra]], whose underlying coalgebra is the [[free graded co-commutative coalgebra]] on $\mathfrak{g}[1]$ and whose differential is given on the tensor product of two generators by the Lie bracket $[-,-]$.

=--

For (pointers to) the details, see at _[model structure on dg-Lie algebras -- Relation to dg-coalgebras](model%20structure%20on%20dg-Lie%20algebras#RelationToDgCoalgebras)_.




+-- {: .num_theorem }
###### Theorem

There exists a [[model category]] structure on $dgCoCAlg_k$ for which

* the cofibrations are the (degreewise) [[injections]];

* the weak equivalences are those morphisms that become [[quasi-isomorphisms]] under the functor $\mathcal{L}$ from prop. \ref{TheCETangentAdjunction}.

Moreover, this is naturally a [[simplicial model category]] structure.  

=--

This is ([Hinich98, theorem, 3.1](#Hinich98)). More details on this are in the relevant sections at _[[model structure for L-infinity algebras]]_.

## Properties




### Relation to dg-Lie algebras
  {#RelationTodgLieAlgbras}


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
  dgCoCAlg_k
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

For $(X,D) \in dgCoCAlg_k$  write

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
  dgCoCAlg_k
  \,.
$$

Moreover, for $X \in dgCoCAlg_k$ and $\mathfrak{g} \in dgLieAlg_k$ then the adjoint [[hom sets]] are [[natural isomorphism|naturally isomorphic]]

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
  (dgCoCAlg_k)_{Quillen}
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
  (dgCoCAlg_k)_{Quillen}
  \,.
$$


=--

([Hinich 98, theorem 3.2](#Hinich98)) using ([Quillen 76 II 1.4](#Quillen76))





## Related concepts

* [[model structure on dg-comodules]]

* [[model structure for L-∞ algebras]]

* [[model structure on dg-Lie algebras]], [[model structure on simplicial Lie algebras]]

* [[model structure on coalgebras over a comonad]]

* [[rational homotopy theory]]

## References

In [[characteristic zero]] and in positive degrees the model structure is due to

* {#Quillen69} [[Dan Quillen]], section II.5 and appendix B of _Rational homotopy theory_, Annals of Math., 90(1969), 205&#8211;295 ([JSTOR](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf)) 

in non-negative degrees in

* [[Ezra Getzler]], [[Paul Goerss]], _A model category structure for differential graded coalgebras_ ([ps](http://www.math.northwestern.edu/~pgoerss/papers/model.ps), [[GetzlerGoerss99.pdf:file]])
 
and in unbounded degrees in

* {#Hinich98} [[Vladimir Hinich]], _DG coalgebras as formal stacks_, Journal of Pure and Applied Algebra Volume 162, Issues 2&#8211;3, 24 August 2001, Pages 209&#8211;250 ([arXiv:math/9812034](http://arxiv.org/abs/math/9812034))


* {#Pridham} [[Jonathan Pridham]], _Unifying derived deformation theories_, Adv. Math. 224 (2010), no.3, 772-826 ([arXiv:0705.0344](http://arxiv.org/abs/0705.0344))
 
See also

* {#Lurie} [[Jacob Lurie]], _[[Formal Moduli Problems]]_
 


Review with discussion of [[homotopy limits]] and [[homotopy colimits]] is in 

* {#Walter06} [[Ben Walter]], section 5 of _Rational Homotopy Calculus of Functors_ ([arXiv:math/0603336](http://arxiv.org/abs/math/0603336))


[[!redirects model stucture on dg-coalgebras]]




