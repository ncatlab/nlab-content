
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


\tableofcontents


### Idea

An *Ore extension* of a [[unital ring]] $R$ is certain generalization of the ring $R[T]$ of [[polynomials]] in one [[variable]] $T$ with [[coefficients]] in $R$. 

While keeping the left $R$-[[module]]-[[structure]] intact, unlike in the polynomial ring, the coefficients in $R$ and the indeterminate $T$ do not need to commute, but rather commute up to a skew-derivation. A skew-polynomial ring is a special case. 

### Definition

Given an endomorphism $\sigma: R\to R$, a __$\sigma$-derivation__ $d: R\to R$ is an additive map satisfying the $\sigma$-twisted Leibniz rule

$$
d(r s) = d(r) s + \sigma(r) d(s),\,\,\,\,\,\forall r,s\in R.  
$$

If $\sigma$ is an injective endomorphism of $R$, and $d$ a $\sigma$-derivation $d$ then the free left $R$-module underlying the ring of polynomials in one variable $R[T]$ is equipped with the unique multiplication rule which is making it into a unital ring, extends $R = R 1\subset R[T]$ and such that 
$$
T \cdot r = \sigma(r) T + d(r), \,\,\,\,\forall r\in R. 
$$
$R[T]$ with this ring structure is called the Ore extension of $R$ and denoted $R[T;\sigma,d]$. 
If $d = 0$ identically, then we say that $R[T]$ is a __skew polynomial ring__. 

An Ore extension of an Ore extension of...(finitely many times) is called an iterated Ore extension. See [[quantum nilpotent algebra]] for an example.

### Literature

* [[K. R. Goodearl]], R. B. Warfield, _An introduction to noncommutative Noetherian rings_, London Math. Society Student Texts __61__, Camb. Univ. Press. 
* Louis H. Rowen, _Ring theory_, student edition, Acad. Press 1991, sec. 1.6
* wikipedia [Ore extension](http://en.wikipedia.org/wiki/Ore_extension) 

[[!redirects skew-polynomial ring]]
[[!redirects Ore extensions]]
 