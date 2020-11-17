
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _volume conjectures_ are a class of [[conjectures]] (slightly differing in generality and assumptions), saying that on a suitable (in particular: [[hyperbolic 3-manifold|hyperbolic]]) [[3-manifold]] $X$ a [[large N limit]] of [[SU(n)]]-[[Chern-Simons theory]] [[quantum observables]] ($N$-[[colored Jones polynomials]] or more generally [[RT-invariants]], [[TV-invariants]]) is [[equality|equal]] to the [[volume]] or [[complex volume]] of $X$.

For a few special cases of 3-manifolds there are explicit [[proofs]] of the volume conjecture(s). Besides this there is an abundance of [[computer experiment|numerical evidence]] for the volume conjectures, using computer algebra such as [[SnapPy]] (see also [Zickert 07](#Zickert07)). In fact experimentation with these numerics is what has been driving the formulation of further variants of the volume conjecture. 

Hence [[experimental mathematics]] strongly suggests that the volume conjectures are true. But a conceptual explanation (let alone [[proof]]) in terms of [[quantum field theory]] has remained open ([Witten 14, bottom of p. 4](#Witten14)).

But an explanation via [[duality in string theory]], combining [[AdS/CFT duality]] with the [[3d/3d correspondence]] for [[wrapped brane|wrapped]] [[M5-branes]], is argued for in [Gang-Kim-Lee 14, 3.2](#GangKimLee14), [Gang-Kim 18 (21)](#GangKim18), see [below](#AsAdSCFTPlus3d3dDuality).


### For $SU(2)$ on knot complements

The original _volume conjecture_ (also "Kashaev's conjecture", due to [Kashaev 95](#Kashaev95), and understood in terms of the $N$-[[colored Jones polynomial]] by [Murakami-Murakami 01](#MurakamiMurakami01)) states that the [[large N limit]] of the $N$-[[colored Jones polynomial]] (for [[gauge group]] [[SU(2)]]) of a [[knot]] $K$ gives the simplicial [[volume]] of its [[complement]] in the [[3-sphere]] (for [[hyperbolic knots]] this is the volume of the complementary [[hyperbolic 3-manifold]])

\[
  \label{KashaevConjecture}
  lim_{N \to \infty}
  \left(
    \frac{
       2 \pi log
    }
    {N}
      \left\vert
        V_N(K; q = e^{\frac{2 \pi i}{N}})
      \right\vert     
  \right) 
  \;=\; 
  vol(K).
\]

Here $V_N(K; q)$ is the ratio of the values of the $N$-[[colored Jones polynomial]] of $K$ and of the [[unknot]]

$$
  V_N(K; q) = \frac{J_N(K; q)}{J_N(\bigcirc; q)}.
$$

The simplicial volume of a knot complement can be found via its unique **torus** decomposition  into hyperbolic pieces and Seifert fibered pieces by a system of tori. The simplicial volume is then the sum of the hyperbolic volumes of the hyperbolic pieces of the decomposition.

If one omits the [[absolute value]] in (eq:KashaevConjecture) then the volume conjecture instead involves the [[complex volume]] ([MMOTY 02, Conjecture 1.2](#MMOTY02)).

### For $SU(2)$ on general 3-manifolds
 {#IdeaGenerally}

More generally, volume conjectures state [[convergence of a sequence|convergence]] of the [[Turaev-Viro invariants]] or [[Reshetikhin-Turaev invariants]] on general [[hyperbolic 3-manifolds]] to the [[volume]] or [[complex volume]], respectively.

See ([Chen-Yang 15](#ChenYang15))

### For $SU(n)$

Generalization from [[gauge group]] [[SU(2)]] to [[SU(n)]]: [Chen-Liu-Zhu 15](#ChenLiuZhu15)


## Proof strategies

### As combined AdS/CFT + 3d/3d duality for wrapped M5-branes
 {#AsAdSCFTPlus3d3dDuality}

In [Gang-Kim-Lee 14b, 3.2](#GangKimLee14b), [Gang-Kim 18 (21)](#GangKim18) it is argued that the [[volume conjecture]] for [[Chern-Simons theory]] on [[hyperbolic 3-manifolds]] $\Sigma^3$ is the combined statement of two [[dualities in string theory]]:

1. [[AdS/CFT duality]]

1. [[3d-3d correspondence]]

for the situation of [[M5-branes]] [[wrapped brane|wrapped on]] $\Sigma^3$ ([DGKV 10](3d-3d+correspondence#DGKV10)):

<center>
<img src="https://ncatlab.org/nlab/files/VolumeConjectureAsAdSCFTPlus3d3dDuality.jpg" width="660">
</center>

For review of the literature see also [Dimofte 16, Section 4.1](#Dimofte16).

## Related concepts

* [[hyperbolic manifold]]

* [[analytically continued Chern-Simons theory]]

* [[Borel regulator]]

* [[membrane instanton]]

## References

### General

Original articles include

* {#Kashaev95} [[Rinat Kashaev]], _A Link Invariant from Quantum Dilogarithm_,  Modern Physics Letters AVol. 10, No. 19, pp. 1409-1418 (1995) ([arXiv:q-alg/9504020](https://arxiv.org/abs/q-alg/9504020))

* {#Kashaev95} [[Rinat Kashaev]], _The Hyperbolic Volume Of Knots From The Quantum Dilogarithm_ Lett. Math. Phys. 39 (1997) 269-275 ([arXiv:q-alg/9601025](https://arxiv.org/abs/q-alg/9601025))

* {#KashaevTirkkonen99} [[Rinat Kashaev]], O. Tirkkonen, _Proof of the volume conjecture for torus knots_, Journal of Mathematical Sciences (2003) 115: 2033 ([arXiv:math/9912210](http://arxiv.org/abs/math/9912210))


* {#MurakamiMurakami01} [[Hitoshi Murakami]], [[Jun Murakami]], _The Colored Jones Polynomial And The Simplicial Volume Of A Knot_, Acta Math. 186 (2001) 85-104 ([euclid.acta/1485891370](https://projecteuclid.org/euclid.acta/1485891370))

* {#MMOTY02} [[Hitoshi Murakami]], [[Jun Murakami]], M. Okamoto, T. Takata, and Y. Yokota, _Kashaev's Conjecture And The Chern-Simons Invariants Of Knots And Links_, Experiment. Math. 11 (2002) 427-435 ([arXiv:math/0203119](https://arxiv.org/abs/math/0203119))

* {#Murakami04} [[Hitoshi Murakami]], _Asymptotic Behaviors Of The Colored Jones Polynomials Of A Torus Knot_, Internat. J. Math. 15 (2004) 547-555.

Generalization to [[Reshetikhin-Turaev construction]] on closed manifold, to the  [[Turaev-Viro construction]] on [[manifolds with boundary]], and to more general [[roots of unity]] than considered before is in 

* {#ChenYang15} [[Qingtao Chen]], [[Tian Yang]], _A volume conjecture for a family of Turaev-Viro type invariants of 3-manifolds with boundary_ ([arXiv:1503.02547](http://arxiv.org/abs/1503.02547))

* Dongmin Gang, Mauricio Romo, Masahito Yamazaki, _All-Order Volume Conjecture for Closed 3-Manifolds from Complex Chern-Simons Theory_,     Commun. Math. Phys. (2018) 359: 915. ([arXiv:1704.00918](https://arxiv.org/abs/1704.00918), [doi:10.1007/s00220-018-3115-y](https://doi.org/10.1007/s00220-018-3115-y))

Generalization to [[SU(n)]]:

* {#ChenLiuZhu15} [[Qingtao Chen]], [[Kefeng Liu]], Shengmao Zhu, _Volume conjecture for $SU(n)$-invariants_ ([arXiv:1511.00658](https://arxiv.org/abs/1511.00658))


Review includes

* {#Murakami11} [[Hitoshi Murakami]], _An Introduction to the Volume Conjecture_ ([arXiv:1002.0126](https://arxiv.org/abs/1002.0126)) In: _Interactions Between Hyperbolic Geometry, Quantum Topology and Number Theory_, Contemporary Mathematics Volume 541, AMS 2011  ([doi:10.1090/conm/541](http://dx.doi.org/10.1090/conm/541))

* {#Witten14} [[Edward Witten]], pp. 4 of _Two Lectures On The Jones Polynomial And Khovanov Homology_ ([arXiv:1401.6996](http://arxiv.org/abs/1401.6996))

* Wikipedia, _[Volume conjecture](http://en.wikipedia.org/wiki/Volume_conjecture)


See also

* {#Neumann03} [[Walter Neumann]], _Extended Bloch group and the Cheeger-Chern-Simons class_, Geom. Topol. 8 (2004) 413-474 ([arXiv:math/0307092](http://arxiv.org/abs/math/0307092))

* {#Zickert07} [[Christian Zickert]], _The volume and Chern-Simons invariant of a representation_, Duke Math. J., 150 (3):489-532, 2009 ([arXiv:0710.2049](http://arxiv.org/abs/0710.2049))

* {#Neumann11} [[Walter Neumann]], _Realizing arithmetic invariants of hyperbolic 3-manifolds_, Contemporary Math 541 (Amer. Math. Soc. 2011), 233--246 ([arXiv:1108.0062](http://arxiv.org/abs/1108.0062))

* {#GaroufalidisThurstonZickert11} [[Stavros Garoufalidis]], [[Dylan Thurston]], [[Christian Zickert]], _The complex volume of $SL(n,\mathbb{C})$-representations of 3-manifolds_ ([arXiv:1111.2828](http://arxiv.org/abs/1111.2828), [Euclid](http://projecteuclid.org/euclid.dmj/1259332507))

### Via string theory

#### General

Speculative discussion in terms of [[quantum field theory]] or [[string theory]] includes

* {#Gukov03} [[Sergei Gukov]], _Three-Dimensional Quantum Gravity, Chern-Simons Theory, And The A-Polynomial_, Commun. Math. Phys. 255 (2005) 577-627 ([arXiv:hep-th/0306165](https://arxiv.org/abs/hep-th/0306165))


* {#DijkgraafFuji09} [[Robbert Dijkgraaf]], Hiroyuki Fuji, _The Volume Conjecture and Topological Strings_ ([arXiv:0903.2084](http://arxiv.org/abs/0903.2084))

* {#DimofteGukov10} [[Tudor Dimofte]], [[Sergei Gukov]], _Quantum Field Theory and the Volume Conjecture_, Contemporary Mathematics 541 (2011), p.41-67 ([arxiv:1003.4808](http://arxiv.org/abs/1003.4808))

* {#Dimofte16} [[Tudor Dimofte]], Section 4.1 of:  _Perturbative and nonperturbative aspects of complex Chern-Simons Theory_, Journal of Physics A: Mathematical and Theoretical, Volume 50, Number 44 ([arXiv:1608.02961](https://arxiv.org/abs/1608.02961))

A conceptual explanation of the volume conjecture via [[analytically continued Chern-Simons theory]] was proposed in

* {#Witten10} [[Edward Witten]], _Analytic Continuation Of Chern-Simons Theory_, AMS/IP Stud. Adv. Math 50 (2011): 347 ([arXiv:1001.2933](https://arxiv.org/abs/1001.2933))

(but it seems that as a sketch or strategy for a rigorous proof, it didn't catch on).


#### As AdS/CFT + 3d/3d duality for wrapped M5-branes


Suggestion that the statement of the [[volume conjecture]] is really [[AdS-CFT duality]] combined with the [[3d-3d correspondence]] for [[M5-branes]] [[wrapped brane|wrapped]] on [[hyperbolic 3-manifolds]]:


* {#GangKimLee14b} [[Dongmin Gang]], [[Nakwoo Kim]], Sangmin Lee, Section 3.2 of: _Holography of 3d-3d correspondence at Large $N$_, JHEP 04 (2015) 091 ([arXiv:1409.6206](https://arxiv.org/abs/1409.6206))


* {#GangKim18} [[Dongmin Gang]], [[Nakwoo Kim]], around (21) of: _Large $N$ twisted partition functions in 3d-3d correspondence and Holography_, Phys. Rev. D 99, 021901 (2019) ([arXiv:1808.02797](https://arxiv.org/abs/1808.02797))



[[!redirects volume conjectures]]
