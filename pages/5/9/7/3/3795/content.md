
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### In mathematics

Consider a complex projective [[Calabi-Yau manifold|Calabi-Yau 3-manifold]] $X$ with volume form $vol_X$. R. Thomas considered in his 1997 thesis a holomorphic version of the [[Casson invariant]] which may be defined using the holomorphic [[Chern-Simons theory|Chern-Simons functional]]. 

For a holomorphic connection $A = A_0 +\alpha$, the holomorphic Chern-Simons functional is given by 

$$CS(A) = \int_X Tr(\bar\nabla_{A_0} \alpha\wedge\alpha +\frac{1}{2}\alpha\wedge\alpha\wedge\alpha) vol_X $$

Its critical points are holomorphically flat connections: $F^{0,2}_A = 0$. One would like to count the critical points in appropriate sense, which means the integration over the suitable compactified moduli space of solutions. These solutions may be viewed as Hermitean Yang-Mills connections or as [[BPS state]]s in physical interpretation. The issues of compactification involve stability conditions which depend on the underlying [[Kähler manifold|Kähler form]]; as the K&#228;hler form varies there are discontinuous jumps at the places of [[wall crossing]]. 

Under the [[mirror symmetry]], the holomorphic bundles correspond to the [[Lagrangian submanifold]]s in the mirror, and the stability condition restricts the attention to the [[special Lagrangian submanifold]]s in the mirror. 

### In physics

for the moment see [this comment](http://mathoverflow.net/questions/75482/donaldson-thomas-invariants-in-physics/75493#75493)

### Motivic DT invariants {#Motivic}

A more general setup of [[motive|motivic]] Donaldson-Thomas invariants is given by [[Dominic Joyce]] and by [[Maxim Kontsevich]] and [[Yan Soibelman]], see the references below. 

## References

### General

* [[Simon Donaldson]], ...

### Motivic Donaldson-Thomas invariants

The original articles are

* [[Dominic Joyce]], Yinan Song, _A theory of generalized Donaldson-Thomas invariants_ ([arxiv/0810.5645](http://arxiv.org/abs/0810.5645))

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_, ([arXiv:0811.2435](http://arxiv.org/abs/0811.2435)); 

summarized in 

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Motivic Donaldson-Thomas invariants: summary of results_, ([0910.4315](http://arxiv.org/abs/0910.4315)); 

and with lecture notes in

* [[Yan Soibelman]], _Motivic Donaldson-Thomas invariants and wall-crossing formulas_,  [Chern-Simons Research Lectures](http://math.berkeley.edu/~reshetik/CSR-Lectures.html) 2010 ([pdf](http://math.berkeley.edu/~reshetik/CSRL/Yan-Berkeley-2010-2.pdf))

See also

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Cohomological [[Hall algebra]], exponential Hodge structures and motivic Donaldson-Thomas invariants_ ([arxiv/1006.2706](http://arxiv.org/abs/1006.2706))


### Relation to wall crossing

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Wall-crossing structures in Donaldson-Thomas invariants, integrable systems and Mirror Symmetry_, ([arxiv/1303.3253](http://arxiv.org/abs/1303.3253))


* S. Cecotti, [[Cumrun Vafa|C. Vafa]], _[[BPS state|BPS]] wall crossing and topological strings_, 
[arXiv/0910.2615](http://arxiv.org/abs/0910.2615)

* [[Davide Gaiotto]], [[Greg Moore|Gregory W. Moore]], [[Andrew Neitzke]], _[[wall crossing|Wall-crossing]], [[Hitchin system]]s, and the [[WKB approximation]], [arxiv/0907.3987](http://arxiv.org/abs/0907.3987)

* sbseminar blog: [Hall algebras and Donaldson-Thomas invariants-i](http://sbseminar.wordpress.com/2009/03/25/hall-algebras-and-donaldson-thomas-invariants-i)

[[!redirects Donaldson-Thomas invariants]]

[[!redirects motivic Donaldson-Thomas invariant]]
