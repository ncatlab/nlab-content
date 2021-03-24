
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The *Doplicher-Roberts reconstruction theorem* allows one to [[reconstruction theorem|reconstruct]] a [[compact topological group]] or "[[supergroup]]" (here essentially: $\mathbb{Z}/2$-graded group) from its [[category of representations]], given enough [[extra structure]] on this [[category]].  Unlike some other versions of [[Tannaka duality]], such as [[Deligne's theorem on tensor categories]], it does not require knowledge of the [[forgetful functor]] ("[[fiber functor]]") from the category of representations to [[VectorSpaces]]. 


This result is named after [[Sergio Doplicher]] and [[John Roberts]], who conveived of it in the context of [[algebraic quantum field theory]] as an intrinsic characterization of the [[superselection sectors]] of a [[quantum field theory]]. See at _[[DHR superselection theory]]_ for more on this aspect.
A simplified and self-contained proof was given in [Müger 06](#Mueger06).

In brief, the DR reconstruction theorem says that every [[symmetric monoidal category|symmetric]] [[tensor category|tensor]] [[star-category]] with conjugates, [[direct sums]], [[subobjects]] and [[endomorphism ring]] of the [[tensor unit]] [[isomorphism|isomorphic]] to the [[complex numbers]], $End(1)= \mathbb{C}$,  is [[equivalence of categories|equivalent]] to the category of [[finite dimensional vector space|finite dimensional]] [[unitary group|unitary]] [[linear representations]] of a [[compact topological group|compact]] [[supergroup]], which is unique up to [[isomorphism]].  For definitions of these terms, see [Müger 06](#Mueger06).

Beware that there are non-isomorphic finite groups whose [[categories of representations]] are equivalent considered merely as [[tensor categories]], ignoring the [[symmetric monoidal category|symmetric]] [[mathematical structure|structure]] (e.g. [Etingof-Gelaki 00](#EtingofGelaki00)).



## Related concepts

* [[Deligne's theorem on tensor categories]]

* [[Wigner classification]]

  * [[unitary representation of the Poincaré group]]

  * [[unitary representation of the super Poincaré group]]


## References

Original statement and proof in the context of [[AQFT]]:

* [[Sergio Doplicher]], [[John Roberts]], ...

Generalization to supergroups and streamlined proof:

* {#Mueger06} [[Michael Müger]], _Abstract duality theory for symmetric tensor $\ast$-categories_ appendix ([pdf](http://www.math.ru.nl/~mueger/PDF/16.pdf)), in [[Hans Halvorson]],  _Algebraic quantum field theory_ ([arXiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036)), in J. Butterfield & J. Earman (eds.) _Handbook of Philosophy and Physics_ 


See also:

* {#EtingofGelaki00} [[Pavel Etingof]], [[Shlomo Gelaki]], _Isocategorical groups_ ([arXiv:math/0007196](https://arxiv.org/abs/math/0007196))


[[!redirects Doplicher-Roberts reconstruction]]
[[!redirects Doplicher-Roberts duality]]