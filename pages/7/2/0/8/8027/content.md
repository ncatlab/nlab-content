
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### Functorial Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _AGT correspondence_ ([AGT 09](#AGT09)) is a relation between 

1. the [[instanton]]-[[partition function]] of $SU(2)^{n+3g-3}$-[[N=2 D=4 super Yang-Mills theory]] (Nekrasov's partition function, e.g. [Szabo 15 (2.1)](#Szabo15))

1. the [[conformal blocks]] of [[Liouville theory]] on an $n$-punctured [[Riemann surface]] $C_{g,n}$ of [[genus]] $g$  

Here the idea is that $C_{g,n}$  is the [[super Yang-Mills theory]] obtained by [[Kaluza-Klein mechanism|compactifying]] the worldvolume [[6d (2,0)-supersymmetric QFT]] of two [[M5-branes]], see at [[N=2 D=4 super Yang-Mills theory]], the section [Construction by compactification](N%3D2+D%3D4+super+Yang-Mills+theory#ConstructionByCompactificationOf5Branes)).

In particular, the [[N=2 D=4 super Yang-Mills theory]] is a [[quiver gauge theory]] and the correspondence matches the shape of its [[quiver]]-diagram to the [[genus of a surface|genus]] and punctures of the [[Riemann surface]]:


<center>
<img src="https://ncatlab.org/nlab/files/AGTQuiver.jpg" width="400">
</center>

More generally, this construction yields something like a decomposition of the [[6d (2,0)-superconformal QFT]] into a [[2d SCFT]] "with values in [[super Yang-Mills theory|4d SYM field theory]]" (e.g. [Tachikawa 10, slide 25 (33 of 54)](#Tachikawa10)). Hence composition with any kind of suitable invariant of the 4d field theories yields an actual [[2d SCFT]], for instance taking the superconformal index in 4d yields a [[2d TQFT]] ([GPRR 10](#GPRR10)). In this picture of "4d-SYM field theory-valued [[2d SCFT]]" one has the following correspondences:

* the [[complex structure]] in 2d is the [[coupling constants]] and [[theta angles]] etc in the 4d [[super Yang-Mills theory]];

* the [[mapping class group]] (large [[conformal transformations]]) in 2d is the (generalized) [[S-duality]] of the 4d theory.

## Related concepts

* [[M5-brane elliptic genus]]

* [[duality in physics]], [[duality in string theory]]

* [[Nekrasov function]]

Wrapping the [[M5-brane]] on a [[3-manifold]] instead yields: [[3d-3d correspondence]].

## References

A [[2d SCFT]] argued to describe the  [[KK-compactification]] of the [[M5-brane]] on a [[4-manifold]] (specifically: a [[complex surface]]) originates with

* [[Juan Maldacena]], [[Andrew Strominger]], [[Edward Witten]], _Black Hole Entropy in M-Theory_, JHEP 9712:002, 1997 ([arXiv:hep-th/9711053](https://arxiv.org/abs/hep-th/9711053))

The origin of the AGT correspondence is:

* {#Gaiotto09} [[Davide Gaiotto]], _$N=2$ dualities_, JHEP08(2012)034 ([arXiv:0904.2715](http://arxiv.org/abs/0904.2715))

* {#AGT09} Luis F. Alday, [[Davide Gaiotto]], [[Yuji Tachikawa]], _Liouville Correlation Functions from Four-dimensional Gauge Theories_, Lett.Math.Phys.91:167-197, 2010 ([arXiv:0906.3219](http://arxiv.org/abs/0906.3219))

* [[Davide Gaiotto]], [[Gregory Moore]], [[Andrew Neitzke]], _Wall-crossing, Hitchin Systems, and the WKB Approximation_ ([arXiv:0907.3987](https://arxiv.org/abs/0907.3987))

The [[2d TQFT]] obtained from this by forming the 4d index is discussed in 

* {#GPRR10} Abhijit Gadde, Elli Pomoni, Leonardo Rastelli, Shlomo S. Razamat, _S-duality and 2d Topological QFT_, JHEP 1003:032, 2010 ([arXiv:0910.2225](http://arxiv.org/abs/0910.2225))

Relation of the [[AGT-correspondence]] to the [[D=6 N=(2,0) SCFT]]

* Benjamin Assel, [[Sakura Schafer-Nameki]], Jin-Mann Wong, _M5-branes on $S^2 \times M_4$: Nahm's Equations and 4d Topological Sigma-models_, J. High Energ. Phys. (2016) 2016: 120 ([arxiv:1604.03606](https://arxiv.org/abs/1604.03606))

  (relating to the [[moduli space of monopoles]])



and to the [[3d-3d correspondence]]:

* [[Clay Cordova]], [[Daniel Jafferis]], _Toda Theory From Six Dimensions_, J. High Energ. Phys. (2017) 2017: 106 ([arxiv:1605.03997](https://arxiv.org/abs/1605.03997))

* Sam van Leuven, Gerben Oling, _Generalized Toda Theory from Six Dimensions and the Conifold_, J. High Energ. Phys. (2017) 2017: 50 ([arxiv:1708.07840](https://arxiv.org/abs/1708.07840))

Brief surveys include

* {#Tachikawa10} [[Yuji Tachikawa]], _M5-branes, 4d gauge theory and 2d CFT_, 2010 ([pdf](http://member.ipmu.jp/yuji.tachikawa/transp/4d-2d-caltech.pdf))

* Abhijit Gadde, _$\mathcal{N}= 2$ Dualities and 2d TQFT_ 2012 ([[Gadde2dTQFT.pdf:file]])

* Nikolay Bovev, _New SCFTs from wrapped branes_, 2013 ([pdf](http://ipht.cea.fr/Meetings/Itzykson2013/Talks/bobev-Itzykson-july2013.pdf))

* Giulio Bonelli, _Variations on AGT Correspondence_, 2013 ([pdf](https://indico.cern.ch/event/217384/attachments/348854/486363/Bonelli.pdf))

* {#Taki16} Masato Taki, _String Theory as an Attempt of PolyMathematics_, talk at 2016.4/28 iTHES-AIMR-IIS  ([pdf](https://indico2.riken.jp/event/2215/attachments/4106/4775/Taki_invited.pdf))

More detailed review is in

* Rober Rodger, _A pedagogical introduction to the AGT conjecture_, Master Thesis Utrecht (2013) ([pdf](http://testweb.science.uu.nl/ITF/teaching/2013/R.J.Rodger.pdf))

* {#Szabo15} [[Richard Szabo]], _$N=2$ gauge theories, instanton moduli spaces and geometric representation theory_, Journal of Geometry and Physics Volume 109, November 2016, Pages 83-121 ([arXiv:1507.00685](https://arxiv.org/abs/1507.00685))

* Bruno Le Floch, _A slow review of the AGT correspondence_ ([arXiv:2006.14025](https://arxiv.org/abs/2006.14025))


See also

* [[Alexander Belavin]], M. A. Bershtein, B. L. Feigin, A. V. Litvinov, G. M. Tarnopolsky, _Instanton moduli spaces and bases in coset conformal field theory_ ([arxiv/1111.2803](http://arxiv.org/abs/1111.2803))

* [[Volker Schomerus]], Paulina Suchanek, _Liouville's imaginary shadow_ ([arxiv/1210.1856](http://arxiv.org/abs/1210.1856))

* A.Mironov, A.Morozov, _The power of Nekrasov functions_ ([arxiv/0908.2190](http://arxiv.org/abs/0908.2190))

* D. Galakhov, A. Mironov, A. Morozov, _S-duality as a beta-deformed Fourier transform_ ([arxiv/1205.4998](http://arxiv.org/abs/1205.4998))

* A. Mironov, _Spectral duality in integrable systems from AGT conjecture_ ([arxiv/1204.0913](http://arxiv.org/abs/1204.0913))

* A. Belavin, V. Belavin, _AGT conjecture and integrable structure of conformal field theory for $c=1$_, Nucl.Phys.B850:199-213 (2011) ([arxiv/1102.0343](http://arxiv.org/abs/1102.0343))

* A. Belavin, V. Belavin, M. Bershtein, _Instantons and 2d Superconformal field theory_ ([arxiv/1106.4001](http://arxiv.org/abs/1106.4001))

* Kazunobu Maruyoshi, _Quantum integrable systems, matrix models, and AGT correspondence_, seminar ([slides pdf](http://db.ipmu.jp/seminar/sysimg/seminar/428.pdf))

* Giulio Bonelli, Alessandro Tanzini, _Hitchin systems, N=2 gauge theories and W-gravity_ ([arxiv/0909.4031](http://arxiv.org/abs/0909.4031))

* Giulio Bonelli, Kazunobu Maruyoshi, Alessandro Tanzini, _Quantum Hitchin systems via beta-deformed matrix models_ ([arxiv/1104.4016](http://arxiv.org/abs/1104.4016))

* {#ChacaltanaDistler10} [[Oscar Chacaltana]], [[Jacques Distler]], _Tinkertoys for Gaiotto Duality_, JHEP 1011:099,2010, ([arXiv:1008.5203](http://arxiv.org/abs/arXiv:1008.5203))

* Satoshi Nawata, _Givental J-functions, Quantum integrable systems, AGT relation with surface operator_ ([arXiv/1408.4132](http://arxiv.org/abs/1408.4132))

The AGT correspondence is treated with the help of a [[Riemann-Hilbert problem]] in 

* G. Vartanov, [[Jörg Teschner]], _Supersymmetric gauge theories, quantization of moduli spaces of flat connections, and conformal field theory_ ([arxiv/1302.3778](http://arxiv.org/abs/1302.3778))




 

category: physics

[[!redirects AGT-correspondence]]

[[!redirects AGT conjecture]]
[[!redirects Class S]]