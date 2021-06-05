
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[axioms]] of traditional [[algebraic quantum field theory]] or [[locally covariant perturbative quantum field theory]], where one assigns a plain [[algebra]] (e.g. a [[C*-algebra]] or [[formal power series algebra]]) of [[observables]] to a [[spacetime]] region, fail when one considers [[gauge theory]] on [[spacetimes]] more general than [[Minkowski spacetime]] ([[AQFT on curved spacetimes]]): 

The nature of [[gauge fields]] implies that to re-construct their global configuration (including non-trivial topology as in [[instanton sectors]]) one needs to locally remember the [[groupoid]] of [[gauge transformations]] (see [Eggertsson 14](https://ncatlab.org/schreiber/show/bachelor+thesis+Eggertsson), [Schenkel 14](#Schenkel14), [Schreiber 14](https://ncatlab.org/schreiber/show/Higher+field+bundles+for+gauge+fields) for exposition), and hence, after [[quantization]], some [[higher algebra]] of observables. 

The program of _homotopical algebraic quantum field theory_ ([Benini-Schenkel 16](#BeniniSchenkel16), see [Schenkel 17](#Schenkel17) for survey) is to lift the axioms of [[AQFT on curved spacetimes]] to certain [[local nets]] of [[homotopical algebra|homotopical algebras]] such as to properly capture [[gauge theory]] with topologically non-trivial [[gauge field]] configurations.

The axioms as considered in [Schenkel 17](#Schenkel17) have some  similarity with that of [[factorization homology]], but also do take into account the [[causality]] condition for [[quantum fields]] on [[Lorentzian manifolds]].

## Related concepts

* [[higher structures]]

* [[locally covariant perturbative algebraic quantum field theory]]

## References
 {#References}

For review and exposition see

* {#Schenkel17} [[Alexander Schenkel]], _Towards Homotopical Algebraic Quantum Field Theory_, talk at _[Foundational and Structural Aspects of Gauge Theories](https://indico.mitp.uni-mainz.de/event/76/overview)_, Mainz Institute for Theoretical Physics, 29 May &#8211; 2 June 2017. ([pdf](http://aschenkel.eu/Mainz17.pdf))

* {#Schenkel14} [[Alexander Schenkel]], _On the problem of gauge theories in locally covariant QFT_, talk at _[Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html)_ Trento, 2014 ([[SchenkelTrento2014.pdf:file]]) (with further emphasis on this point in the companion talk [Schreiber 14](field+bundle#Schreiber14)) 

* {#Schenkel17b} [[Alexander Schenkel]], _From Fredenhagen's universal algebra to homotopy theory and operads_, talk at _Quantum Physics meets Mathematics_, Hamburg, December 2017 ([pdf slides](http://aschenkel.eu/Hamburg17.pdf))

* {#BeniniSchenkel19} [[Marco Benini]], [[Alexander Schenkel]], _Higher Structures in Algebraic Quantum Field Theory_,  Proceedings of LMS/EPSRC Symposium _[[Higher Structures in M-Theory 2018]]_, Fortschritte der Physik 2019  ([arXiv:1903.02878](https://arxiv.org/abs/1903.02878), [doi:10.1002/prop.201910015]( https://doi.org/10.1002/prop.201910015))

* [[Simen Bruinsma]], _Coloring Operads for Algebraic Field Theory_, in: Proceedings of _[[Higher Structures in M-Theory 2018]]_ Fortschritte der Physik, Special Issue Volume 67, Issue 8-9 ([arXiv:1903.02863](https://arxiv.org/abs/1903.02863) [doi:10.1002/prop.201910004](https://doi.org/10.1002/prop.201910004))


Construction and axiomatization of gauge field AQFT via [[homotopy theory]] and [[homotopical algebra]] is being developed in

* {#BDS} [[Marco Benini]], [[Claudio Dappiaggi]], [[Alexander Schenkel]], _Quantized Abelian principal connections on Lorentzian manifolds_, Communications in Mathematical Physics 2013 ([arXiv:1303.2515](http://arxiv.org/abs/1303.2515))

* {#BeniniSchenkelSzabo15} [[Marco Benini]], [[Alexander Schenkel]], [[Richard Szabo]], _Homotopy colimits and global observables in Abelian gauge theory_ ([arXiv:1503.08839](http://arxiv.org/abs/1503.08839))


* {#BeniniSchenkel16} [[Marco Benini]], [[Alexander Schenkel]], _Quantum field theories on categories fibered in groupoids_, Communications in Mathematical Physics November 2017, Volume 356, Issue 1, pp 19&#8211;64 ([arXiv:1610.06071](https://arxiv.org/abs/1610.06071))

The [[stack]] of [[Yang-Mills theory|Yang-Mills]] [[gauge fields]] is discussed in

* {#BeniniSchenkelSchreiber17} [[Marco Benini]], [[Alexander Schenkel]], [[Urs Schreiber]], _The stack of Yang-Mills fields on Lorentzian manifolds_, Commun. Math. Phys. 359, 765–820 (2018) ([arXiv:1704.01378](https://arxiv.org/abs/1704.01378), [doi:10.1007/s00220-018-3120-1](https://doi.org/10.1007/s00220-018-3120-1))


An [[operad]] for [[local nets of observables]] in [[AQFT]] is considered in

* {#BeniniSchenkelWoike17} [[Marco Benini]], [[Alexander Schenkel]], [[Lukas Woike]], _Operads for algebraic quantum field theory_ ([arXiv:1709.08657](https://arxiv.org/abs/1709.08657))

and its [[model structure on algebras over an operad]] (with respect to the [[model structure on chain complexes]]) is discussed in

* {#BeniniSchenkelWoike18} [[Marco Benini]], [[Alexander Schenkel]], [[Lukas Woike]], _Homotopy theory of algebraic quantum field theories_, Lett. Math. Phys. 109, 1487-1532 (2019) ([arXiv:1805.08795](https://arxiv.org/abs/1805.08795), [doi:10.1007/s11005-018-01151-x](https://doi.org/10.1007/s11005-018-01151-x))


The [[Boardman-Vogt resolution]] of the [[operad]] for [[local nets of observables]] ([Benini-Schenkel-Woike 17](#BeniniSchenkelWoike17)), lifting it to homotopy AQFT, is considered in

* {#Yau18} [[Donald Yau]], _Homotopical Quantum Field Theory_, World Scientific 2019 ([arXiv:1802.08101](https://arxiv.org/abs/1802.08101), [doi:10.1142/11626](https://doi.org/10.1142/11626))

Assignment of [[BV-BRST complexes]] as a homotopy AQFT is discussed in

* {#BeniniBruinsmaSchenkel19} [[Marco Benini]], [[Simen Bruinsma]], [[Alexander Schenkel]], _Linear Yang-Mills theory as a homotopy AQFT_, Commun. Math. Phys. 378, 185–218 (2020) ([arXiv:1906.00999](https://arxiv.org/abs/1906.00999), [doi:10.1007/s00220-019-03640-z](https://doi.org/10.1007/s00220-019-03640-z))

Discussion of [[orbifold|orbifolding]] via [[categorification]]:

* [[Marco Benini]], [[Marco Perin]], [[Alexander Schenkel]], [[Lukas Woike]], _Categorification of algebraic quantum field theories_, Lett. Math. Phys. 2021 ([h)arXiv:2003.13713](https://arxiv.org/abs/2003.13713))


Application to [[semi-topological 4d Chern-Simons theory]]:

* [[Marco Benini]], [[Alexander Schenkel]], Benoit Vicedo, _Homotopical analysis of 4d Chern-Simons theory and integrable field theories_ ([arXiv:2008.01829](https://arxiv.org/abs/2008.01829))



[[!redirects homotopical algebraic quantum field theories]]

[[!redirects homotopical AQFT]]

[[!redirects homotopy AQFT]]
[[!redirects homotopy algebraic quantum field theory]]
