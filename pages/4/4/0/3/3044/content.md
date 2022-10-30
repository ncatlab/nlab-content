+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
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
   \stackrel{\overset{\mathcal{L}}{\leftarrow}}{\underset{\mathcal{C}}{\to}}
  dgCoCAlg_k
$$

between the category of [[dg-Lie algebras]] (on unbounded [[chain complexes]]) and that of dg [[cocommutative coalgebras]], where the [[right adjoint]] sends a dg-Lie algebra $(\mathfrak{g}_\bullet, [-,-])$ to its "Chevalley-Eilenberg coalgebra", whose underlying coalgebra is the [[free graded co-commutative coalgebra]] on $\mathfrak{g}_\bullet$ and whose differential is given on the tensor product of two generators by the Lie bracket $[-,-]$.

=--


+-- {: .num_theorem }
###### Theorem

There exists a [[model category]] structure on $dgCoCAlg_k$ for which

* the cofibrations are the (degreewise) [[injections]];

* the weak equivalences are those morphisms that become [[quasi-isomorphisms]] under the functor $\mathcal{L}$ from prop. \ref{TheCETangentAdjunction}.

Moreover, this is naturally a [[simplicial model category]] structure.  

=--

This is ([Hinich98, theorem, 3.1](#Hinich98)). More details on this are in the relevant sections at _[[model structure for L-infinity algebras]]_.

## Properties



### Relation to the model structure on dg-Lie algebras

+-- {: .num_prop }
###### Proposition

The functor $\mathcal{C}$ from prop. \ref{TheCETangentAdjunction} is a [[right Quillen functor]].

=--

([Hinich98, lemma 5.3.2](#Hinich98))

Hence $(\mathcal{L} \dashv \mathcal{C})$ is a [[Quillen adjunction]] to the [[model structure on dg-algebras]].

+-- {: .num_prop }
###### Proposition

The [[adjunction]] of prop. \ref{TheCETangentAdjunction} constitutes a  [[Quillen equivalence]] to the [[model structure on dg-Lie algebras]].

=--

This is ([Hinich98, theorem 3.2](#Hinich98)).



## Related concepts

* [[rational homotopy theory]]

* [[model structure for L-∞ algebras]]

* [[model structure on dg-Lie algebras]]

* [[model structure on coalgebras over a comonad]]

## References


* {#Quillen69} [[Dan Quillen]], section II.5 and appendix B of _Rational homotopy theory_, Annals of Math., 90(1969), 205&#8211;295 ([JSTOR](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf)) 


* [[Ezra Getzler]], [[Paul Goerss]], _A model category structure for differential graded coalgebras_ ([ps](http://www.math.northwestern.edu/~pgoerss/papers/model.ps), [[GetzlerGoerss99.pdf:file]])

* {#Hinich97} [[Vladimir Hinich]], _Homological algebra of homotopy algebras_ , Comm. in algebra, 25(10)(1997), 3291&#8211;3323.
 

* {#Hinich98} [[Vladimir Hinich]], _DG coalgebras as formal stacks_ ([arXiv:math/9812034](http://arxiv.org/abs/math/9812034))
 


* {#Pridham} [[Jonathan Pridham]], _Unifying derived deformation theories_, Adv. Math. 224 (2010), no.3, 772-826 ([arXiv:0705.0344](http://arxiv.org/abs/0705.0344))
 

* {#Lurie} [[Jacob Lurie]], _[[Formal Moduli Problems]]_
 


Review with discussion of [[homotopy limits]] and [[homotopy colimits]] is in 

* {#Walter06} [[Ben Walter]], section 5 of _Rational Homotopy Calculus of Functors_ ([arXiv:math/0603336](http://arxiv.org/abs/math/0603336))


[[!redirects model stucture on dg-coalgebras]]




