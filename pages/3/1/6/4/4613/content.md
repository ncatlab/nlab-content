
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

In its most refined form, a _secondary characteristic class_ is a [[characteristic class]] in [[ordinary differential cohomology]]. The term "secondary" refers to the fact that such a differential cohomology class in degree $n$ not only encodes a degree-$n$ class in [[integral cohomology]], but in addition [[connection on an infinity-bundle|higher connection data]] in degree $(n+1)$: the data of a [[circle n-bundle with connection]].

The refined [[Chern-Weil homomorphism]] takes values in such "secondary characteristic classes".

But the precise meaning of the term _secondary characteristic class_ varies a little in the literature, as follows. Historically it was first understood in more restricted senses.

1. In the strict sense of the word, a _secondary characteristic class_ is a characteristic of a situation where an ordinary [[characteristic class]] vanishes ([PetersonStein1962](#PetersonStein)).

1. More specifically, a special case of this situation in [[differential geometry]] arises where the [[characteristic class]] is represented in [[de Rham cohomology]] by a [[curvature characteristic form]]. If that curvature form happens to vanish, the corresponding [[Chern-Simons form]] itself becomes closed, and now itself represents a cohomology class, in one degree lower. This is often called the corresponding _Chern-Simons secondary characteristic class_ . Sometimes the term "secondary geometric invariants" is used for [[Chern-Simons form]]s (see for instance the review ([FreedII](#FreedCSII))).

1. Using refined [[Chern-Weil theory]] the notions of [[curvature characteristic form]]s and their [[Chern-Simons form]]s are unified into the notion of cocycles in [[ordinary differential cohomology]]. The notion of [[Cheeger-Simons differential character]] was introduced to describe this unification, and it is has become tradition to call these differential characters themselves _secondary characteristic classes_ independently of whether the corresponding ordinary [[characteristic class]]/[[curvature characteristic form]] vanishes or not (for instance ([DupontKamber](#Kamber), [Karlsson](#Karlsson)). More descriptively, this case is maybe better referred to as a _[[differential characteristic class]]_ . See there for more details.

## Higher order invariants and boundary field theory
 {#HigherOrderInvariantsAndBoundaryFieldTheory}

The statement that secondary invariants are indeed secondary to primary invariants can be formalized in the language of [[prequantum field theory|prequantum]] [[boundary field theory]] by saying that (higher) [[topological Yang-Mills theory]] (which is controled by differential [[Chern classes]]) has as [[boundary field theory]] ([[higher dimensional Chern-Simons theory|higher]]) [[Chern-Simons theory]]. 

As explained at _[[boundary field theory]]_, this statement is reflected by the existence of a universal [[correspondence]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)}$, where $\mathbf{H}$ is [[Smooth∞Grpd]], $\flat$ is the [[flat modality]] and $\mathbf{B}^{n+1}U(1)$ is the [[circle n-group|circle (n+2)-group]]:

$$
  \array{
    && X
    \\
    & \swarrow &\downarrow^\nabla& \searrow^{\mathrlap{F_{(\nabla)}}}
    \\
    \ast &\leftarrow& \mathbf{B}^n U(1)_{conn} &\stackrel{F_{(-)}}{\to}& \Omega^{n+1}_{cl}
    \\
    & \searrow &\swArrow& \swarrow_{\mathrlap{}}
    \\
    && \flat \mathbf{B}^{n+1}U(1)
  }
  \,,
$$

where the bottom right map is the canonical one in the context of [[differential cohesion]], the outer diagram is any specified one and the factorization through the

This exhibits a secondary invariant $\nabla$ (a [[cocycle]] in [[ordinary differential cohomology]]) of degree (n+1) as a boundary condition for the theory of closed characteristic forms.

In this picture, one obtains further "higher order invariants" by successively further [[transgression|transgrssing]] and forming higher order boundaries. 

If we view here, as we may $\nabla$ as the [[local Lagrangian]] of an [[schreiber:infinity-Chern-Simons theory]], then the ternary invariants are _[[WZW terms]]_; the quaternary invariants are _[[Wilson loop]]_ terms.
([lpqft](#lpqft))



## Related concepts

* [[Chern-Simons invariant]]

* [[Cheeger-Simons class]], [[complex volume]]


## References

The notion in its general cohomological sense appears in

* {#PetersonStein} Franklin P. Peterson, Norman Stein, _Secondary characteristic classes_, Annals of mathematics, Vol 76, No. 3 (1962)


The notion of [[Chern-Simons forms]] originates in 

* [[Shiing-shen Chern]], [[James Simons]], _[[Characteristic forms and geometric invariants]]_, The Annals of Mathematics, Second Series, Vol. 99, No. 1 (1974) ([jstor](http://www.jstor.org/stable/1971013)).



The special meaning in the context of [[Chern-Weil theory]] in [[differential geometry]] was established by the introduction of [[Cheeger-Simons differential character]] in

* {#CheegerSimons} [[Jeff Cheeger]],  [[James Simons]], _Differential characters and geometric invariants_, pages 50&#8211;80 in: _Geometry and Topology_, Lecture Notes in Mathematics, vol 1167. Springer (1985)  ([pdf](http://numr.wdfiles.com/local--files/differential-cohomology/cheeger-simons.pdf), [doi:10.1007/BFb0075212](https://doi.org/10.1007/BFb0075212))
 
Review:

* {#FreedCSII} [[Dan Freed]], _Classical Chern-Simons theory II_ ([pdf](http://www.ma.utexas.edu/users/dafr/cs2.pdf))


* {#Kamber} [[Johan Dupont]], Franz Kamber, _Gerbes, Simplicial forms and Invariants for Families of Foliated Bundles_ ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.152.1375&rep=rep1&type=pdf))


* {#Karlsson} Michelle Karlsson, _Characteristic classes and bounded cohomology_ ([pdf](http://www.math.ethz.ch/u/burger/karlsson.pdf))

Lecture notes on secondary cohomology classes in [[differential cohomology]] for flat connections is presented in

* {#Bunke12} [[Ulrich Bunke]], _Differential cohomology_ ([arXiv:1208.3961](https://arxiv.org/abs/1208.3961))

Discussion in complex [[algebraic geometry]] is in 

* {#BlochEsnault97} [[Spencer Bloch]], [[Hélène Esnault]], _Algebraic Chern-Simons theory_, American Journal of Mathematics, Volume 119, Number 4, August 1997, pp. 903-952 ([pdf](http://www.mi.fu-berlin.de/users/esnault/preprints/helene/39-algebraic-chern-simons.pdf))

Discussion of secondary classes being [[torsion elements]]:

* [[Alexander Reznikov]], _All regulators of flat bundles are torsion_, Annals of Mathematics Second Series, Vol. 141, No. 2 (Mar., 1995), pp. 373-386 (14 pages) ([arXiv:dg-ga/9407006](https://arxiv.org/abs/dg-ga/9407006), [jstor:2118525](https://www.jstor.org/stable/2118525))

* [[Alexander Reznikov]], _Rationality of secondary classes_, J. Differential Geom., Volume 43, Number 3 (1996), 674-692. ([arXiv:dg-ga/9407007](https://arxiv.org/abs/dg-ga/9407007), [euclid:jdg/1214458328](https://projecteuclid.org/euclid.jdg/1214458328))


* Jaya N. Iyer, [[Carlos Simpson]], _Regulators of canonical extensions are torsion: the smooth divisor case_ ([arXiv:0707.0372](https://arxiv.org/abs/0707.0372))

* [[Hélène Esnault]],  _Algebraic Differential Characters of Flat Connections with Nilpotent Residues_,  In: Baas N., Friedlander E., Jahren B., Østvær P. (eds.) _Algebraic Topology_, Abel Symposia, vol 4. Springer 2009 ([doi:10.1007/978-3-642-01200-6_5](https://doi.org/10.1007/978-3-642-01200-6_5))

Discussion of secondary characteristic classes in [[string cobordism cohomology theory]] and in [[tmf]]:

* [[Ulrich Bunke]], [[Niko Naumann]], _Secondary Invariants for String Bordism and tmf_, Bulletin des Sciences Mathématiques, Volume 138, Issue 8, 2014, Pages 912-970 
([arXiv:0912.4875](https://arxiv.org/abs/0912.4875), 
[doi:10.1016/j.bulsci.2014.05.002](https://doi.org/10.1016/j.bulsci.2014.05.002))


Discussion of secondary and higher order invariant as higher order [[boundary field theories]] to higher [[topological Yang-Mills theory|topological Yang-Mills]] prequantum field theory is in

* {#lpqft} [[Urs Schreiber]] et al., _[[schreiber:Local prequantum field theory]]_
  

Specifically the secondary Chern-Simons and quaternary WZW invariants in this context are discussed in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_, in Damien Calaque et al. (eds.)
_Mathematical Aspects of Quantum Field Theories_, Springer 2014



[[!redirects secondary characteristic class]]
[[!redirects secondary characteristic classes]]

[[!redirects secondary characteristic form]]
[[!redirects secondary characteristic forms]]

[[!redirects secondary invariant]]
[[!redirects secondary invariants]]