
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


This result is named after [[Sergio Doplicher]] and [[John Roberts]], who conceived of it in the context of [[algebraic quantum field theory]] as an intrinsic characterization of the [[superselection sectors]] of a [[quantum field theory]]. See at _[[DHR superselection theory]]_ for more on this aspect.
A simplified and self-contained proof was given in [Müger 06](#Mueger06).

In brief, the DR reconstruction theorem says that every [[symmetric monoidal category|symmetric]] [[tensor category|tensor]] [[star-category]] with conjugates, [[direct sums]], [[subobjects]] and [[endomorphism ring]] of the [[tensor unit]] [[isomorphism|isomorphic]] to the [[complex numbers]], $End(1)= \mathbb{C}$,  is [[equivalence of categories|equivalent]] to the category of [[finite dimensional vector space|finite dimensional]] [[unitary group|unitary]] [[linear representations]] of a [[compact topological group|compact]] [[supergroup]], which is unique up to [[isomorphism]].  For definitions of these terms, see [Müger 06](#Mueger06).

Beware that there are non-isomorphic finite groups whose [[categories of representations]] are equivalent considered merely as [[tensor categories]], ignoring the [[symmetric monoidal category|symmetric]] [[mathematical structure|structure]] (e.g. [Etingof-Gelaki 00](#EtingofGelaki00)).



## Related concepts

* [[DHR superselection theory]]

* [[Deligne's theorem on tensor categories]]

* [[Wigner classification]]

  * [[unitary representation of the Poincaré group]]

  * [[unitary representation of the super Poincaré group]]


## References

Original statement and proof in the context of [[AQFT]]:

* {#DoplicherRoberts89} [[Sergio Doplicher]], [[John Roberts]], _A new duality theory for compact groups_, Inventiones mathematicae **98** 1 (1989) 157-218 &lbrack;[dml:143725](https://eudml.org/doc/143725)&rbrack;

Generalization to supergroups and streamlined proof:

* {#Mueger06} [[Michael Müger]]: *Abstract duality theory for symmetric tensor $ast$-categories* ([pdf](https://www.math.ru.nl/~mueger/PDF/16.pdf)), appendix to: [[Hans Halvorson]], *Algebraic Quantum Field Theory*, in *Philosophy of Physics*, Handbook of the Philosophy of Science (2007) 731-864 &lbrack;[doi:10.1016/B978-044451560-5/50011-7](https://doi.org/10.1016/B978-044451560-5/50011-7), [arXiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036)&rbrack;

Review:

* [[Garth Warner]]: *Reconstruction Theory*, EPrint Collection, University of Washington (2011) &lbrack;[hdl:1773/16351](http://hdl.handle.net/1773/16351), [pdf](https://sites.math.washington.edu//~warner/ReconTh_Warner.pdf), [[Warner-ReconstructionTheory.pdf:file]]&rbrack;

See also:

* {#EtingofGelaki00} [[Pavel Etingof]], [[Shlomo Gelaki]], _Isocategorical groups_ &lbrack;[arXiv:math/0007196](https://arxiv.org/abs/math/0007196)&rbrack;


[[!redirects Doplicher-Roberts reconstruction]]
[[!redirects Doplicher-Roberts duality]]