
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

## Definition

+-- {: .num_defn}
###### Definition


A **tensor triangulated category** is a [[category]] $Ho$ equipped with 

1. the structure of a [[symmetric monoidal category]] $(Ho, \otimes, 1, \tau)$;

1. the structure of a [[triangulated category]] $(Ho, \Sigma, CofSeq)$

1. for all objects $X,Y\in Ho$ [[natural isomorphisms]]

   $$
     e_{X,Y}
       \;\colon\;
     (\Sigma X) \wedge Y 
       \overset{\simeq}{\longrightarrow} 
     \Sigma(X \wedge Y)
   $$

such that

1. for all $X, Y, Z \in Ho$ the following [[commuting diagram|diagram commutes]]

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

1. (tensor product is exact) for each object $V \in Ho$ the functors $V \otimes (-) \simeq (-)\otimes V$ preserves distinguished triangles in that for 

   $$
     X 
       \overset{f}{\longrightarrow}
     X
       \overset{g}{\longrightarrow}
     Y
       \overset{h}{\longrightarrow}
     \Sigma X
   $$

   in $CofSeq$, then also

   $$
     V \otimes X 
       \overset{id_V \otimes f}{\longrightarrow}
     V\otimes X
       \overset{id_V \otimes g}{\longrightarrow}
     V \otimes Y
       \overset{id_V \otimes h}{\longrightarrow}
     V \otimes (\Sigma X)
     \simeq
     \Sigma(V \otimes X)
     \,,
   $$

   where the equivalence at the end is $e_{X,V}\circ \tau_{V, \Sigma Y}$.

1. for all $n_1, n_2 \in \mathbb{Z}$ the following [[commuting diagram|diagram commutes]]

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


=--

This is ([Hovey-Palmieri-Strickland 97, def. A.2.1](#HoveyPalmieriStrickland97)) except for statemens concerning possible further [[closed monoidal category]] structure. There this is called "symmetric monoidal structure compatible with the triangulation".

In ([Balmer 05, def. 1.1](#Balmer05)) the terminology "tensor triangulated category" is said to refer to a symmetric monoidal triangulated category such that "tensor product is exact in each variable", without further specification. Similarly for instance in ([Stevenson 11, Introduction](#Stevenson11)). But ([Balmer 05, p. 2](#Balmer05)) cites ([Hovey-Palmieri-Strickland 97](#HoveyPalmieriStrickland97)) as "dealing with tensor triangulated categories". In sources like ([Stevenson 11](#Stevenson11)) furthermore $ V \otimes (-)$ is required to preserve [[direct sums]]. 



## Related concepts

* [[spectrum of a tensor triangulated category]]

## References

* {#HoveyPalmieriStrickland97} [[Mark Hovey]], [[John Palmieri]], [[Neil Strickland]], _Axiomatic stable homotopy theory_, Memoirs of the AMS 610 (1997) ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/axiomatic.pdf))

* {#Balmer05} [[Paul Balmer]], _The spectrum of prime ideals in tensor triangulated categories, J. Reine Angew. Math., 588:149&#8211;168, 2005 ([arXiv:0409360](http://arxiv.org/abs/math/0409360))

Review is for instance in 

* {#Stevenson11} [[Greg Stevenson]], _Tensor actions and locally complete intersection_ PhD thesis 2011 ([pdf](http://www.math.uni-bielefeld.de/~gstevens/Stevenson_thesis.pdf))

[[!redirects tensor triangulated categories]]
