
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--



\tableofcontents

## Idea

A _tensor triangulated category_ is a [[triangulated category]] that also carries the structure of a [[symmetric monoidal category]] in a compatible way.

(For a compatible non-[[symmetric monoidal category|symmetric]] [[monoidal category]] [[structure]] on a [[triangulated categories]], some authors speak of *monoidal triangulated categories*, cf. [Rowe 2024](#Rowe2024).)

## Definition

+-- {: .num_defn}
###### Definition

There are different variants of the definition in the literature, asking for successively more structure.

To start with, a **tensor triangulated category** must be at least a [[category]] $Ho$ equipped with 

1. the structure of a [[symmetric monoidal category]] $(Ho, \otimes, 1, \tau)$ ("[[tensor category]]");

1. the structure of a [[triangulated category]] $(Ho, \Sigma, CofSeq)$

1. for all objects $X,Y\in Ho$ [[natural isomorphisms]]

   $$
     e_{X,Y}
       \;\colon\;
     (\Sigma X) \otimes Y 
       \overset{\simeq}{\longrightarrow} 
     \Sigma(X \otimes Y)
   $$

   
such that

1. (tensor product is additive) for each object $V$ the functor $V \otimes (-) \simeq (-) \otimes V$ is an [[additive functor]];

1. (tensor product is exact) for each object $V \in Ho$ the functor $V \otimes (-) \simeq (-)\otimes V$ preserves distinguished triangles in that for 

   $$
     X 
       \overset{f}{\longrightarrow}
     Y
       \overset{g}{\longrightarrow}
     Y/X
       \overset{h}{\longrightarrow}
     \Sigma X
   $$

   in $CofSeq$, then also

   $$
     V \otimes X 
       \overset{id_V \otimes f}{\longrightarrow}
     V\otimes Y
       \overset{id_V \otimes g}{\longrightarrow}
     V \otimes Y/X
       \overset{id_V \otimes h}{\longrightarrow}
     V \otimes (\Sigma X)
       \simeq
     \Sigma(V \otimes X)
   $$

   in $CofSeq$, where the equivalence at the end is $e_{X,V}\circ \tau_{V, \Sigma X}$.

Jointly this says that the isomorphisms $e$ give $V \otimes (-)$ the structure of a [[triangulated functor]], for all $V$.

=--

([Balmer 05, def. 1.1](#Balmer05))

In addition one may ask that

1. (coherence) for all $X, Y, Z \in Ho$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       ( \Sigma(X) \otimes Y) \otimes Z
         &\overset{e_{X,Y} \otimes id}{\longrightarrow}&
       (\Sigma (X \otimes Y)) \otimes Z
         &\overset{e_{X \otimes Y, Z}}{\longrightarrow}& 
       \Sigma( (X \otimes Y) \otimes Z )
       \\
       {}^{\mathllap{\alpha_{\Sigma X, Y, Z}}}\downarrow
         &&
         &&
       \downarrow^{\mathrlap{\Sigma \alpha_{X,Y,Z}}}
       \\
       \Sigma (X) \otimes (Y \otimes Z)
         &&
         \underset{e_{X, Y \otimes Z }}{\longrightarrow} 
         &&
      \Sigma( X \otimes (Y \otimes Z) )
     }
   $$

   is in $CofSeq$, where $\alpha$ is the [[associator]] of $(Ho, \otimes, 1)$.


1. (graded commutativity) for all $n_1, n_2 \in \mathbb{Z}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (\Sigma^{n_1} 1) \otimes (\Sigma^{n_2} 1)
       &\overset{\simeq}{\longrightarrow}&
       \Sigma^{n_1 + n_2} 1
       \\
       {}^{\mathllap{\tau_{\Sigma^{n_1}1, \Sigma^{n_2}1}}}\downarrow
         &&
       \downarrow^{\mathrlap{(-1)^{n_1 \cdot n_2}}}
       \\
       (\Sigma^{n_2} 1) \otimes (\Sigma^{n_1} 1)
       &\underset{\simeq}{\longrightarrow}&
       \Sigma^{n_1 + n_2} 1
     }
     \,,
   $$

   where the horizontal isomorphisms are composites of the $e_{\cdot,\cdot}$ and the braidings.


This is [Hovey, Palmieri & Strickland 1997, def. A.2.1](#HoveyPalmieriStrickland97), except for statements concerning possible further [[closed monoidal category]] structure. There this is called "symmetric monoidal structure compatible with the triangulation".

Finally, one can ask for the existence of additional compatibility commutative diagrams, for instance representing a "derived shadow" of the [[pushout product]] axiom of a [[monoidal model category]].  These can be found as (TC3), (TC4), and (TC5) in [May 2001](#May01).


## Examples

* The archetypical example is the [[stable homotopy category]] equipped with the [[smash product of spectra]]. For details see at _[[model structure on orthogonal spectra]]_ the section _[The monoidal stable homotopy category](model+structure+on+orthogonal+spectra#TheMonoidalStableHomotopyCategory)_.

## Related concepts

* [[spectrum of a tensor triangulated category]]

* [[tensor category]], [[triangulated category]]

* [[tensor (∞,1)-category]]


## References

### Tensor triangulated categories
 {#ReferencesTensorTriangulatedCategories}

* {#HoveyPalmieriStrickland97} [[Mark Hovey]], [[John Palmieri]], [[Neil Strickland]], _Axiomatic stable homotopy theory_, Memoirs of the AMS 610 (1997) ([pdf](https://www.sas.rochester.edu/mth/sites/doug-ravenel/otherpapers/axiomatic.pdf), [doi:10.1090/memo/0610](http://dx.doi.org/10.1090/memo/0610))

* {#Balmer05} [[Paul Balmer]], _The spectrum of prime ideals in tensor triangulated categories, J. Reine Angew. Math., 588:149&#8211;168, 2005 ([arXiv:0409360](http://arxiv.org/abs/math/0409360), [doi:10.1515/crll.2005.2005.588.149](https://doi.org/10.1515/crll.2005.2005.588.149))

* {#May01} [[Peter May]], _The Additivity of Traces in Triangulated Categories_, Advances in Mathematics, Volume 163, Issue 1, 2001, Pages 34-73 ([doi:10.1006/aima.2001.1995](https://doi.org/10.1006/aima.2001.1995))

Review:

* {#Stevenson11} [[Greg Stevenson]], _Tensor actions and locally complete intersection_ PhD thesis 2011 ([pdf](http://www.math.uni-bielefeld.de/~gstevens/Stevenson_thesis.pdf))

* [[Paul Balmer]], _A guide to tensor-triangular classification_, in: [[Haynes Miller]] (ed.) _[[Handbook of Homotopy Theory]]_ ([arXiv:1912.08963](https://arxiv.org/abs/1912.08963))



### Monoidal triangulated categories
 {#ReferencesMonoidalTriangulatedCategories}

On non-[[symmetric monoidal category|symmetric]] [[monoidal category]] [[structure]] on [[triangulated categories]] ("monoidal triangulated (mt) categories" in the terminology of [Rowe 2024](#Rowe2024)), just asing the [[tensor product]] to be an [[exact functor]] in each variable:

* Daniel K Nakano, Kent B Vashaw, Milen T Yakimov; §2.1 in: *Noncommutative Tensor Triangular Geometry and the Tensor Product Property for Support Maps Free*, International Mathematics Research Notices, Volume 2022, Issue 22, (2022) 17766--17796 \[<a href="https://doi.org/10.1093/imrn/rnab221">doi:10.1093/imrn/rnab221</a>\]

* Daniel K. Nakano: *Monoidal Triangular Geometry with Applications to Representation Theory*, talk slides \[<a href="https://www.crmath.ca/wp-content/uploads/2023/09/canmex-dan-nakano.pdf">pdf</a>\]

* Hongdi Huang, Kent B. Vashaw: *Group actions on monoidal triangulated categories and Balmer spectra*, Documenta Mathematica, **30** 5 (2025) 1055--1083 \[<a href="http://doi.org/10.4171/DM/1016">doi:10.4171/DM/1016</a>, [arXiv:2311.18638](https://arxiv.org/abs/2311.18638)\]

 
* {#Rowe2024} James Rowe; §2 in: *Noncommutative tensor triangular geometry: classification via Noetherian spectra*, Pacific Journal of Mathematics, **330** (2024) 355--371 \[<a href="https://doi.org/10.2140/pjm.2024.330.355">doi:10.2140/pjm.2024.330.355</a>\]

* Daniel K. Nakano, Kent B. Vashaw, Milen T. Yakimov: *The homological spectrum for monoidal triangulated categories* \[<a href="https://arxiv.org/abs/2506.19946">arXiv:2506.19946</a>\]

In these articles, asking the tensor product just to be biexact appears to be sufficient for the intended application to nonsymmetric *[[spectra of tensor triangulated categories]]*. 
But beyond that it would seem natural to demand more [[coherence]], for instance asking the tensor product to be a *triangulated bifunctor* in the sense of:

* [[Masaki Kashiwara]], [[Pierre Schapira]]; Def. 10.3.6, 10.1.1(v) in: _[[Categories and Sheaves]]_, Grundlehren der Mathematischen Wissenschaften **332**, Springer (2006) \[<a href="https://link.springer.com/book/10.1007/3-540-27950-4">doi:10.1007/3-540-27950-4</a>, [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)\]




[[!redirects tensor triangulated categories]]

[[!redirects monoidal triangulated category]]
[[!redirects monoidal triangulated categories]]

