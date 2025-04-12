
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


The aim of _Homological Perturbation Theory_ is to construct small [[chain complex]]es from large ones. It was originally developed for the calculation of chain models of the total spaces of [[fiber bundles]], but has since developed into a useful general computational tool. 

## Homological perturbation lemma

Let $(X,d), (Y,d)$ be [[chain complexes]] over a [[commutative ring]] $R$ and let $f: X \to Y, \nabla: Y \to X$ be [[chain maps]], and $\Phi: X \to X$ be a [[chain homotopy]] such that 

$$ f \nabla=1, \quad \nabla f= 1 + d\Phi + \Phi d, $$ 

 $$ f\Phi = 0, \Phi \nabla=0, \Phi^2=0, \Phi d \Phi= - \Phi. $$

Let $X,Y$ have [[filtrations]] $F^*$ bounded below by $0$ and preserved by $\nabla,f, \Phi$ and the [[differentials]] on $X,Y$. Suppose $X$ has another differential $d^\tau$ with the property that 

$$ (d^\tau -d)F^p X \subseteq F^{p-1} X $$ 

for all $p \geq 0$. The **Homological Perturbation Lemma** states that $Y$ can be given a new differential $d^\tau$ such that there is a [[quasi-isomorphism]] $(Y, d^\tau) \to (X, d^\tau)$. 

The main point is that there is an explicit formula for the new chain homotopy as 

$$\Phi^\tau= \sum _{r=0}^\infty \Phi (1+ d^\tau \Phi)^r.$$

There is considerable interest in describing the new differential in terms of a [[twisting cochain]]. 

This result derived from earlier work of G. Hirsch, E.H. Brown, Weishu Shih, and has been widely developed into a useful theoretical and computational tool by Guggenheim, Lambe, Stasheff and others.  

## Applications

### BV-complexes and Wick's lemma
 {#BVComplexesAndWickLemma}

Homological perturbation theory is a key tool in the construction of [[BRST-BV complexes]], where the [[quantum BV complex]] is a perturbation of a [[classical BV-complex]]. See ([Gwilliam, section 2.5](#Gwilliam)). In this context [[Wick's lemma]] in [[quantum field theory]] is a direct consequence of the homological perturbation lemma ([Gwilliam, section 2.5.2](#Gwilliam)).




## References

Review includes

* [[Marius Crainic]], _On the perturbation lemma, and deformations_ ([arXiv:math/0403266](http://arxiv.org/abs/math/0403266))

* [[Johannes Huebschmann]], _A survey on homological perturbation theory_ ([pdf](http://math.univ-lille1.fr/~huebschm/data/talks/courant.pdf))


Other references include

* [[Ronnie Brown]], _The twisted Eilenberg-Zilber Theorem_,  Simposio di Topologia (Messina, 1964)  pp. 33--37 Edizioni Oderisi, Gubbio. ([pdf] (http://pages.bangor.ac.uk/~mas010/pdffiles/twistedez.pdf))

* {#BarnesLambe91} Donald W. Barnes, [[Larry Lambe|Larry A. Lambe]], _A fixed point approach to homological perturbation theory_, Proc. Amer. Math. Soc. 112 (1991), no. 3, 881--892. 

* V Gugenheim, LA Lambe, JD Stasheff, _Perturbation theory in differential homological algebra II_, Illinois Journal of Mathematics 35:3 (1991) 357--373 [euclid](https://projecteuclid.org/journals/illinois-journal-of-mathematics/volume-35/issue-3/Perturbation-theory-in-differential-homological-algebra-II/10.1215/ijm/1255987784.full)

For applications to  "make computable" a bicategory of isolated hypersurface singularities and matrix factorisations comp that has been studied in the context of [[topological field theory]], using the formulation in ([Barnes-Lambe 91](#BarnesLambe91))  is in 

* [[Daniel Murfet]], _Computing with cut systems_, ([arXiv:1402.4541](http://arxiv.org/abs/1402.4541))

See also _[[linear logic]]_.


Discussion with an eye towards [[Hochschild cohomology]] and [[cyclic cohomology]] is in

* [[Larry Lambe|Larry A. Lambe]], _Homological perturbation theory, Hochschild homology and formal groups_ Contemp. Math. __189__, AMS, 1992 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.64.8783&rep=rep1&type=pdf))


* V. &#193;lvarez, J.A. Armario, P. Real, B. Silva, _Homological perturbation theory and computability Of Hochschild and cyclic homologies of cdgas_ ([pdf](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.47.6955))

Discussion in the context of [[BV-quantization]] is in section 2.5 of 

* [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis ([pdf](https://people.math.umass.edu/~gwilliam/thesis.pdf))
 {#Gwilliam}




[[!redirects homological perturbation lemma]]
