
#Contents#
* automatic table of contents goes here
{:toc}

##Idea 

The notion of _twisting functions_ is an explicit [[simplicial set|simplicial]] formula for a [[cocycle]] with values in a [[simplicial group]]. The _twisted propduct_ induced from the twisting function is an explicit simplicial formula for the [[principal ∞-bundle]] classified by this cocycle.

In a fibre [[bundle]] or more generally in a fibration, the fibre 'twists' as one goes around a loop in the base space, (the standard simple example is the [[Möbius band]]). Such fibre bundles are usually restricted to being 'locally trivial', that is locally a product of an open set in the base with the fibre.


In the  setting of simplicial [[homotopy theory]], one can attempt to construct analogues of fibre bundles by starting with a base [[simplicial set]] $X_\bullet$ and a fibre $F_\bullet$ and trying to 'deform' the simplicial product $X_\bullet \times F_\bullet$ to get some non-trivial fibred object. In the Cartan seminars of the period 1956--57 ([numdam](http://www.numdam.org/numdam-bin/fitem?id=SHC_1956-1957__9__A1_0)), (about pages 1--10), a neat solution was described: by leaving all but one of the face maps of the product alone, and deforming the last. The result is a "twisted [[cartesian product]]" (see below). The deformation required a simplicial [[automorphism]] of the fibre of course, and the resulting twisting function went from the base $X_\bullet$ to the automorphisms of $F_\bullet$, completely mirroring the topological example. The simplicial identities force the twisting function to obey certain equations.


##Definition 

### Twisting function

Let $X_\bullet$ be a [[simplicial set]] and $G_\bullet$ a [[simplicial group]]. Then a __twisting function__ $\phi :X_\bullet\to G_\bullet$ is a family of maps $\phi=\{\phi_n : X_n\to G_{n-1}\}_{n\gt 1}$ such that

$$\array{
d_0 \phi(x) = (\phi(d_0 x))^{-1} \phi(d_1 x)\\
d_i \phi(x) = \phi(d_{i+1}x), i\gt 0,\\
s_i\phi(x) = \phi(s_{i+1}x), i\geq 0,\\
\phi(s_0 x) = 1_G.
}$$


### Twisted Cartesian products

Given a [[simplicial set]] $F_\bullet$ with left $G_\bullet$-[[action]], one then defines a __twisted Cartesian product__, (TCP),  $X_\bullet \times_\phi F_\bullet$ with
$(X_\bullet \times_\phi F_\bullet)_n = X_n\times F_n$ and
$$\array{
d_i(x,f) = (d_i x, d_i f), i\gt 0\\
d_0 (x,f) = (d_0 x, \phi(x)(d_0 f)),\\
s_i(x,y) = (s_i x,s_i y).
}$$

Thus the only difference from the usual Cartesian product of simplicial sets is in $d_0$. 


## Properties

* A twisting function $\phi :X_\bullet\to G_\bullet$ corresponds exactly to a simplicial map from $X$ to $\overline{W}(G_\bullet)$ [delooping of the simplicial group](http://ncatlab.org/nlab/show/simplicial+group#Delooping).  There is a universal twisting function $\overline{W}(G_\bullet)_\bullet\to G_\bullet$.  

* By the adjunction between $W$-bar and the [[Dwyer-Kan loop groupoid]] functor, a twisting function also corresponds to a morphism of simplicial groupoids $G(X_\bullet)\to G_\bullet$.

*  A twisting function is an analogue of a [[twisting cochain]] in the context of [[simplicial set]]s although historically the development went the other way, it seems as the basic theory of twisting cochains was explored by Ed Brown in his paper 

   * Edgar H. Brown Jr. _Twisted tensor products. I._  Ann. of Math. (2)  69  (1959) 223--246.

*  The link between Kan fibrations and simplicial fibre bundles, and thus TCPs is neatly summarised in Curtis 

   *  E. Curtis, _Simplicial Homotopy Theory_, Advances in Math., 6, (1971), 107 &#8211; 209.


[[!redirects twisting functions]]

[[!redirects twisted Cartesian product]]
[[!redirects twisted Cartesian products]]

[[!redirects twisted cartesian product]]
[[!redirects twisted cartesian products]]