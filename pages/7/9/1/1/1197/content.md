
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea 

The notion of _twisting functions_ is an explicit [[simplicial set|simplicial]] formula for a [[cocycle]] with values in a [[simplicial group]]. The _twisted product_ induced from the twisting function is an explicit simplicial formula for a [[simplicial principal bundle]], a model for a [[discrete ∞-groupoid|discrete]] [[principal ∞-bundle]] classified by this cocycle.

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

* A twisting function $\phi :X_\bullet\to G_\bullet$ corresponds exactly to a simplicial map from $X$ to $\overline{W}(G_\bullet)$ [delooping of the simplicial group](http://ncatlab.org/nlab/show/simplicial+group#Delooping).  There is a universal twisting function $\overline{W}(G_\bullet)_\bullet\to G_\bullet$.  See [[simplicial principal bundle]] for more.

* By the adjunction between $W$-bar and the [[Dwyer-Kan loop groupoid]] functor, a twisting function also corresponds to a morphism of simplicial groupoids $G(X_\bullet)\to G_\bullet$.

\begin{remark}\label{RelationToTwistingCochains}
Twisting functions are the analogue of [[twisting cochains]] in the context of [[simplicial sets]]; but twisting cochains were introduced by [Brown 1959](#Brown59), whilst twisting functions were discussed already in [Cartan 1956](#Cartan56).
\end{remark}

## Literature

* {#Cartan56} [[Henri Cartan]], *Sur la théorie de Kan*, Séminaire Henri Cartan **9** (1956-1957) talk no. 1 &lbrack;[numdam:SHC_1956-1957__9__A1_0](http://www.numdam.org/item?id=SHC_1956-1957__9__A1_0)&rbrack;

* {#Brown59} [[Edgar H. Brown]] Jr. _Twisted tensor products. I._  Ann. of Math. **69** 2  (1959) 223-246 &lbrack;[doi:10.2307/1970101](https://doi.org/10.2307/1970101), [jstor:1970101](https://www.jstor.org/stable/1970101)&rbrack;

* [[Michael G. Barratt]], [[Victor K.A.M. Gugenheim]], [[John C. Moore]], _On semisimplicial fibre-bundles_, Amer. J. Math. __81__ (1959) 639-657 &lbrack;[doi:10.2307/2372920](https://doi.org/10.2307/2372920), [jstor:2372920](https://www.jstor.org/stable/2372920), MR0111028&rbrack;


The link between Kan fibrations and simplicial fibre bundles, and thus TCPs is neatly summarised in:

*  [[Edward Curtis]], _Simplicial Homotopy Theory_, Advances in Math. __6__ (1971) 107-209 &lbrack;[MR279808](http://www.ams.org/mathscinet-getitem?mr=279808) <a href="http://dx.doi.org/10.1016/0001-8708(71)90015-6">doi</a>&rbrack;


Review:

* [[Peter May]], §IV in: _Simplicial objects in algebraic topology_, University of Chicago Press (1967) &lbrack;[ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]]&rbrack;



[[!redirects twisting functions]]

[[!redirects twisted Cartesian product]]
[[!redirects twisted Cartesian products]]

[[!redirects twisted cartesian product]]
[[!redirects twisted cartesian products]]