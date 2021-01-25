
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



#Contents#
* table of contents
{:toc}

## Idea

A _tensor triangulated category_ is a [[category]] that carries the structure of a [[symmetric monoidal category]] and of a [[triangulated category]] in a compatible way.

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


This is ([Hovey-Palmieri-Strickland 97, def. A.2.1](#HoveyPalmieriStrickland97)) except for statements concerning possible further [[closed monoidal category]] structure. There this is called "symmetric monoidal structure compatible with the triangulation".

Finally, one can ask for the existence of additional compatibility commutative diagrams, for instance representing a "derived shadow" of the [[pushout product]] axiom of a [[monoidal model category]].  These can be found as (TC3), (TC4), and (TC5) in ([May](#May01)).


## Examples

* The archetypical example is the [[stable homotopy category]] equipped with the [[smash product of spectra]]. For details see at _[[model structure on orthogonal spectra]]_ the section _[The monoidal stable homotopy category](model+structure+on+orthogonal+spectra#TheMonoidalStableHomotopyCategory)_.

## Related concepts

* [[spectrum of a tensor triangulated category]]

* [[tensor category]], [[triangulated category]]

* [[tensor (∞,1)-category]]


## References

* {#HoveyPalmieriStrickland97} [[Mark Hovey]], [[John Palmieri]], [[Neil Strickland]], _Axiomatic stable homotopy theory_, Memoirs of the AMS 610 (1997) ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/axiomatic.pdf), [doi:10.1090/memo/0610](http://dx.doi.org/10.1090/memo/0610))

* {#Balmer05} [[Paul Balmer]], _The spectrum of prime ideals in tensor triangulated categories, J. Reine Angew. Math., 588:149&#8211;168, 2005 ([arXiv:0409360](http://arxiv.org/abs/math/0409360), [doi:10.1515/crll.2005.2005.588.149](https://doi.org/10.1515/crll.2005.2005.588.149))

* {#May01} [[Peter May]], _The Additivity of Traces in Triangulated Categories_, Advances in Mathematics, Volume 163, Issue 1, 2001, Pages 34-73 ([doi:10.1006/aima.2001.1995](https://doi.org/10.1006/aima.2001.1995))

Review:

* {#Stevenson11} [[Greg Stevenson]], _Tensor actions and locally complete intersection_ PhD thesis 2011 ([pdf](http://www.math.uni-bielefeld.de/~gstevens/Stevenson_thesis.pdf))

* [[Paul Balmer]], _A guide to tensor-triangular classification_, in: [[Haynes Miller]] (ed.) _[[Handbook of Homotopy Theory]]_ ([arXiv:1912.08963](https://arxiv.org/abs/1912.08963))


[[!redirects tensor triangulated categories]]
