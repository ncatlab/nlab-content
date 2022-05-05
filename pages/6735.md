
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The BLG model is a 3-dimensional [[SCFT]] involving a [[Chern-Simons theory]] coupled to matter. It is argued to be the [[worldvolume]] theory of 2 coincident [[black brane|black]] [[M2-branes]] with 16 manifest [[supersymmetries]]. The generalization to an arbitrary number of M2-branes is supposed to be given by the [[ABJM model]].


[[!include 7d spherical space forms -- table]]


## Properties

### The Lagrangian

(...)

### Boundary conditions 

Discussion of [[boundary conditions]] of the BLG model, leading to [[brane intersection]] with [[M-wave]], [[M5-brane]] and [[MO9-brane]] is in ([Chu-Smith 09](#ChuSmith09), [BPST 09](#BPST09)).



### The "$3$-algebra" structure
 {#3AlgebraStructure}

The BLG model Lagrangian involves a trilinear operation on the scalar fields $\phi \in V$

$$
 [-,-,-] : V^{\otimes 3} \to V
  \,.
$$

Moreover, the [[supersymmetry]] of the Lagrangian hinges on the fact that this map satisfies a condition that has some similarity to a [[Jacobi identity]] for the binary operation on a [[Lie algebra]]. 

Therefore, superficially, it looks like this might be the trinary bracket on an _[[L-∞ algebra]]_ structure on the space $V$. 

On the one hand, indeed, by the discussion at _[[supergravity C-field]]_ , the M2-brane is charged under a [[circle n-bundle with connection|circle 3-bundle with connection]] whose [[higher gauge theory]] is controled by [[Lie n-algebra|Lie 3-algebra]]s in direct analogy to how the [[higher gauge theory]] of the [[string]] is controled by [[gerbes]]/[[principal 2-bundles]] and their [[Lie 2-algebra]]s and that of charged [[particles]] by ordinary [[Lie algebra]]s.


Apparantly motivated by an intuition along these lines, ([BaggerLambert](#BaggerLambert)) named $(V,[-,-,-])$ a **3-algebra**. This terminology was picked up by many authors In the process, it transmuted sometimes to "3-Lie algebra" and sometimes even to "Lie 3-algebra".

Unfortunately, the Bagger-Lambert "3-algebra" is **not** a _[[Lie n-algebra|Lie 3-algebra]]_ in the established sense of an [[L-∞ algebra]] structure on a [[graded vector space]] $V$ concentrated in the lowest three degrees. At least not without some modifications in the interpretation of the map $[-,-,-]$. 

The reason is that for the notion of an [[L-∞ algebra]] (as discussed there) it is crucial that $V$ is a $\mathbb{N}$-graded (or $\mathbb{Z}$-graded) vector space and that the $n$-ary brackets respect the degree in a certain way. 
But in the [BaggerLambert](#BaggerLamber)-proposal, $V$ is all concentrated in a single degree (is regarded as ungraded). One immediately finds that in this case the $L_\infty$-respect of $[-,-,-]$ for the grading would imply that $V$ is taken to be in degree $1/2$. Since this is not in $\mathbb{N}$, it does not yield an $L_\infty$-algebra.

Notice that the $\mathbb{N}$-grading (or $\mathbb{Z}$-grading) of $L_\infty$-algebras is crucial for the [[homotopy theory|homotopy theoretic]] interpretation of [[L-∞ algebra]]s as higher Lie algebras. None of the good theory of $L_\infty$-algebras survives when this grading is dropped. This grading has its origin in the [[Dold-Kan correspondence]], which establishes integral graded homological structures as models for structures in [[higher category theory]]. Notably, a higher Lie algebra is supposed to have a [[Lie integration]] to a [[smooth ∞-groupoid|smooth $n$-groupoid]]. Under this process, the elements in degree $k$ of the higher Lie algebra become tangents to the space of [[k-morphisms]] of this smooth $n$-groupoid. Clearly, here only integer $k$ do make sense.

On the other hand, it is of course possible to consider the structure on "$L_\infty$-algebras without grading", even if these will not have a good theory. This notion has once been introduced by Filippov (Sib. Math. Zh. No 6 126&#8211;140 (195)) under the term _[[n-Lie algebra]]_ .

Beware, therefore, that the innocent-looking difference between the terms

* [[Lie n-algebra]]

* [[n-Lie algebra]]

corresponds, unfortunately, to a major difference in the behaviour of the concepts behind these terms.

In conclusion, it is clear that 2-brane physics is governed by Lie 3-algebraic structures, but it is not yet clear how the trinary operation highlighted by [BaggerLambert](#BaggerLambert) would be an example.

In view of this it might be noteworthy that the equivalent reformulation and generalization of the BLG model by the [[ABJM model]] does not involve any "3-algebras" at all. In fact at least most of the "3-algebras" appearing in the membrane literature may be understood as being data of a plain [[Lie algebra]] with an invariant product and a representation ([MFMR 08](#MFMR)). These authors summarize the state of affiars on p. 3 as 

> All this prompts one to question whether the 3-algebras appearing in the constructions [1&#8211;3,10,11] play a fundamental role in M-theory or, at least insofar as the effective field theory is concerned, are largely superfluous. The equivalence of [10] and [6] and the abundance of new theories (dual to known M-theory backgrounds) which seem not to involve a 3-algebra might suggest the latter. Nonetheless, given our lack of understanding of how to incorporate in Lie-algebraic terms the expected properties of M-theoretic degrees of freedom, like the entropy scaling laws for M2- and M5-brane condensates, it may be useful to understand the precise relation between the 3-algebras appearing in the recent literature on superconformal Chern&#8211;Simons theory and Lie algebras.

The article ([MFMR 08](#MFMR)) provides this relation and under this relation the "3-algebraic" BLG model has then been understood as a special case of the ordinary Lie algebraic [[ABJM theory]]. A review is in ([Bagger-Lambert 12](#BaggerLambert12)).

It has also been suggested that "3-algebras" are to be interpreted in **[[n-plectic geometry|2-plectic structure]]** ([Saemann-Szabo](#SaemannSzabo)).


## Related concepts

* [[ABJM theory]]

* [[membrane matrix model]]

[[!include table of branes]]

## References

The original articles are

* {#BaggerLambert06} [[Jonathan Bagger]], [[Neil Lambert]], _Modeling Multiple M2's_, Phys. Rev. D75, 045020 (2007). ([hep-th/0611108](http://arxiv.org/abs/hep-th/0611108)). 

* [[Jonathan Bagger]], [[Neil Lambert]], Phys. Rev. D77, 065008 (2008). ([arXiv:0711.0955](http://arXiv.org/abs/0711.0955)). 

and concerning the "3-algebra"-structure also

* [[Andreas Gustavsson]], Nucl. Phys. B811, 66-76 (2009). [arXiv:0709.1260].

The interpretation in terms of branes at a $\mathbb{Z}/2$-[[ADE-singularities]] with [[discrete torsion]] in the [[supergravity C-field]] is due to

* [[Neil Lambert]], [[David Tong]], _Membranes on an Orbifold_, Phys.Rev.Lett.101:041602, 2008 ([arXiv:0804.1114](https://arxiv.org/abs/0804.1114))

* [[Jacques Distler]], [[Sunil Mukhi]], [[Constantinos Papageorgakis]], [[Mark Van Raamsdonk]], _M2-branes on M-folds_, JHEP 0805:038,2008 ([arXiv:0804.1256](https://arxiv.org/abs/0804.1256))

A comprehensive review is in 

* {#BaggerLambert12} [[Jonathan Bagger]], [[Neil Lambert]], Sunil Mukhi, Constantinos Papageorgakis, _Multiple Membranes in M-theory_ ([arXiv:1203.3546](http://arxiv.org/abs/1203.3546))

and a review talk is

* {#Lambert18} [[Neil Lambert]], _M-Branes: Lessons from M2’s and Hopes for M5’s_,  talk at _[Higher Structures in M-Theory, Durham, August 2018](http://www.maths.dur.ac.uk/lms/109/index.html)_ ([pdf slides](http://www.maths.dur.ac.uk/lms/109/talks/1877lambert.pdf), [video recording](http://www.maths.dur.ac.uk/lms/109/movies/1877lamb.mp4))

Discussion of [[boundary conditions]] leading to [[brane intersection]] with [[M-wave]], [[M5-brane]] and [[MO9-brane]] is in

* {#ChuSmith09} Chong-Sun Chu, Douglas J. Smith, _Multiple Self-Dual Strings on M5-Branes_, JHEP 1001:001, 2010 ([arXiv:0909.2333](https://arxiv.org/abs/0909.2333))

* {#BPST09} [[David Berman]], Malcolm J. Perry, [[Ergin Sezgin]], Daniel C. Thompson, _Boundary Conditions for Interacting Membranes_, JHEP 1004:025, 2010 ([arXiv:0912.3504](https://arxiv.org/abs/0912.3504))


Discussion in [[Horava-Witten theory]] reducing M2-branes to [[heterotic strings]] is in

* {#Lambert15} [[Neil Lambert]], _Heterotic M2-branes_ ([arXiv:1507.07931](http://arxiv.org/abs/1507.07931))
 

The interpretation of at least most of the "3-algebra" appearing in the membrane literature in terms of plain [[Lie algebras]] is due to

* {#MFMR} Paul de Medeiros, [[José Figueroa-O'Farrill]], Elena M&#233;ndez-Escobar, Patricia Ritter, _On the Lie-algebraic origin of metric 3-algebras_, Commun.Math.Phys.290:871-902,2009 ([arXiv:0809.1086](http://arxiv.org/abs/0809.1086))
 
See also

* [[José Figueroa-O'Farrill]], section _Triple systems and Lie superalgebras_ in _M2-branes, ADE and Lie superalgebras_, talk at IPMU 2009 ([pdf](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/Hongo.pdf))


The suggestion that BGL "3-algebras" are to be interpreted in [[2-plectic geometry]] appears in

* {#SaemannSzabo} [[Christian Saemann]], [[Richard Szabo]], _Quantization of 2-Plectic Manifolds_ ([arXiv:1106.1890](http://arxiv.org/abs/1106.1890))
 
[[!redirects BLG-model]]
