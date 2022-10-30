
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $L$ be a first order language and $T$ a [[theory]] over $L$. One can consider the [[category]] $\mathcal{M}_{el}(L)$ of [[structure in model theory|structures]] over $L$ and [[elementary monomorphisms]]. Define $\mathcal{M}_{el}(T)$ as a [[full subcategory]] of $\mathcal{M}_{el}(L)$, whose [[objects]] are [[models]] of $T$. 

### Groupoids and categories
 
A __definable groupoid__ over a theory $T$ is an [[internal groupoid]] in the category of [[definable sets]] and definable functions, i.e. the internal groupoid in the [[category of functors]] $\mathcal{M}_{el}(T)\to Set$.  Similarly, for more general notion of a __definable category__ over $T$. 


### Groups

In particular, there is much studied case of __definable groups__, cf. e.g. ([Peterzil-Pillay](#PeterzilPillay))

## Properties


+-- {: .num_defn}
###### Theorem

There is a [[bijection|bijective]] correspondence between internal imaginary sorts of $T$ and definable concrete groupoids with a single isomorphism class (both up to equivalence.)

=--

This is ([Hrushovski 2006, Th.3.2](#Hrushovski)).


## Related concepts

* [[definability]]

## References

* Y. Peterzil, A. Pillay, _Generic sets in definably compact groups_, Fundamenta Mathematicae __193__ (2007), pp. 153--170, [MR2282713](http://www.ams.org/mathscinet-getitem?mr=2282713), [doi](http://dx.doi.org/10.4064/fm193-2-4)
 {#PeterzilPillay}

* Y. Peterzil, A. Pillay, S. Starchenko, _Linear groups definable in o-minimal structures_, J. Algebra __247__ (2002), no. 1, pp. 1--23, [MR1873380](http://www.ams.org/mathscinet-getitem?mr=1873380), [doi](http://dx.doi.org/10.1006/jabr.2001.8861)

* Alessandro Berarducci, _Definable groups in o-minimal structures_, [pdf](http://www.dm.unipi.it/~dinasso/marian2004/berarducci.pdf); _Cohomology of groups in o-minimal structures: acyclicity of the infinitesimal subgroup_, J. Symbolic Logic __74__:3 (2009), 891-900, [MR2548466](http://www.ams.org/mathscinet-getitem?mr=2548466), [euclid](http://projecteuclid.org/euclid.jsl/1245158089), [doi](http://dx.doi.org/10.2178/jsl/1245158089), _O-minimal spectra, infinitesimal subgroups and cohomology_, J. Symbolic Logic __72__ (2007), no. 4, pp. 1177--1193, [MR2371198](http://www.ams.org/mathscinet-getitem?mr=2371198), [euclid](http://projecteuclid.org/euclid.jsl/1203350779 ), [doi](http://dx.doi.org/10.2178/jsl/1203350779)

* Margarita Otero, _A survey on groups definable in o-minimal structures_, in: Model theory with applications to algebra and analysis. Vol. 2, 177&#8211;206, London Math. Soc. Lecture Note Ser. __350__, Cambridge Univ. Press 2008, [MR2010b:03042](http://www.ams.org/mathscinet-getitem?mr=2436142), [doi](http://dx.doi.org/10.1017/CBO9780511735219.006)

* [[Ehud Hrushovski]], _Groupoids, imaginaries and internal covers_ (2006), [arxiv/math.LO/0603413](http://arxiv.org/abs/math/0603413) 
 {#Hrushovski06}

* [[Ehud Hrushovski]], _On finite imaginaries_, [arxiv/0902.0842](http://arxiv.org/abs/0902.0842)


[[!redirects definable groupoids]]
[[!redirects definable category]]
[[!redirects definable categories]]
[[!redirects definable group]]
[[!redirects definable groups]]
