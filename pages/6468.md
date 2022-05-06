
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **K3 surface** is a [[Calabi-Yau variety]] of [[dimension]] $2$ (a Calabi-Yau [[algebraic surface]]). This means that the [[canonical bundle]] $\omega_X=\wedge^2\Omega_X\simeq \mathcal{O}_X$ is trivial and $H^1(X, \mathcal{O}_X)=0$.

The term "K3" is 

> in honor of Kummer, K&#228;hler, Kodaira, and the beautiful K2 mountain in Kashmir

([Weil 79, p. 546](#Weil79))

## Examples

* A cyclic cover of $\mathbb{P}^2$ branched over a curve of degree $6$.

* A nonsingular degree $4$ hypersurface in $\mathbb{P}^3$, such as the [[Fermat hypersurface|Fermat quartic]] $\{[w,x,y,z] \in \mathbb{P}^3 | w^4 + x^4 + y^4 + z^4 = 0\}$ (in fact every K3 surface over $\mathbb{C}$ is [[diffeomorphism|diffeomorphic]] to this example).


## Properties

### Basic properties

* All K3 surfaces are [[simply connected]]. 

* Over the [[complex numbers]] they are all [[Kähler manifold|Kähler]], and even [[hyperkähler manifold|hyperkähler]].

### Cohomology

+-- {: .num_prop #IntegralCohomology}
###### Proposition
**([[integral cohomology]] of [[K3-surface]])**

The [[integral cohomology]] of a K3-surface $X$ is 

$$
  H^n(X,\mathbb{Z})
  \;\simeq\;
  \left\{
  \array{
    \mathbb{Z} &\vert& n = 0
    \\
    0 &\vert& n = 1
    \\
    \mathbb{Z}^{22} &\vert& n = 2
    \\
    0 &\vert& n = 3
    \\
    \mathbb{Z} &\vert& n = 4
  }
  \right.
$$

=--

(e.g. [Barth-Peters-Van den Ven 84, VIII Prop. 3.2](#BarthPetersVandenVen84))

+-- {: .num_prop #BettiNumbers}
###### Proposition
**([[Betti numbers]] of a [[K3-surface]])**


The [[Hodge diamond]] is completely determined (even in positive [[characteristic]]) and hence the  [[Hodge-de Rham spectral sequence]] degenerates at $E_1$. This also implies that the [[Betti numbers]] are completely determined as $1, 0, 22, 0, 1$:

$$
  \array{
    && h^{0,0}
    \\
    & h^{1,0} && h^{0,1}
    \\
    h^{2,0} & & h^{1,1} & & h^{0,2}
    \\
    & h^{2,1} & & h^{1,2}
    \\
    && h^{2,2}
  }
  \;\;\;=\;\;\;
  \array{
    && 1
    \\
    & 0 && 0
    \\
    1 & & 20 & & 1
    \\
    & 0 & & 0
    \\
    && 
    1
  }
$$

=--

(e.g. [Barth-Peters-Van den Ven 84, VIII Prop. 3.3](#BarthPetersVandenVen84))


### Moduli of higher line bundles and deformation theory
 {#ModuliOfHigherLineBundles}

In [[positive number|positive]] [[characteristic]] $p$:

The [[Néron-Severi group]] of a K3 is a [[free abelian group]]

The [[formal Brauer group]] is

* either the formal [[additive group]], in which case it has [[height of a formal group|height]] $h = \infty$, by definition;

* or its [[height of a formal group|height]] is $1 \leq h \leq 10$, and every value may occur

([Artin 74](#Artin74)), see also ([Artin-Mazur 77, p. 5 (of 46)](#ArtinMazur77))

[[!include moduli of higher lines -- table]]

## Related concepts

* [[formal Brauer group]]

* [[K3-cohomology]]

* [[F-theory]],

* [[elliptic fibration]]

## References

### General

Original sources include

* {#Artin74} [[Michael Artin]], _Supersingular K3 Surfaces_, Annal. Sc. d, l'&#201;c Norm. Sup.  4e  s&#233;ries, T. 7, fasc.  4, 1974, pp. 543-568

* {#Weil79} [[Andre Weil]], Final report on contract AF 18 (603)-57. In Scientific works. Collected papers. Vol. II (1951-1964). 1979.

Textbook accounts include

* {#BarthPetersVandenVen84} W. Barth, C. Peters, A. Van den Ven, chapter VII of _Compact complex surfaces_, Springer 1984

Lecture notes include

* [[Daniel Huybrechts]], _Lectures on K3-surfaces_ ([pdf](http://www.math.uni-bonn.de/people/huybrech/K3Global.pdf))

* [[Claire Voisin]], _<a href="http://www.ams.org/mathscinet-getitem?mr=2487743">Geometry of the Moduli Space of K3 surfaces</a>_ 

* [[David Morrison]], _[The geometry of K3 surfaces](http://www.cgtp.duke.edu/ITP99/morrison/cortona.pdf)_ Lecture notes (1988)

* Viacheslav Nikulin, _Elliptic fibrations on K3 surfaces_ ([arXiv:1010.3904](http://arxiv.org/abs/1010.3904))

Discussion of the [[deformation theory]] of K3-surfaces (of their [[Picard schemes]]) is (see also at _[[Artin-Mazur formal group]]_) in 

* {#ArtinMazur77} [[Michael Artin]], [[Barry Mazur]], _Formal Groups Arising from Algebraic Varieties_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 10 no. 1 (1977), p. 87-131  [numdam](http://www.numdam.org/item?id=ASENS_1977_4_10_1_87_0), [MR56:15663](http://www.ams.org/mathscinet-getitem?mr=56:15663)

### In string theory
  {#InStringTheory}

In [[string theory]], the [[KK-compactification]] of [[type IIA string theory]]/[[M-theory]]/[[F-theory]] on K3-[[fibers]] is supposed to exhibit te [[duality between M/F-theory and heterotic string theory]], originally due to

* [[Chris Hull]], [[Paul Townsend]], section 6 of _Unity of Superstring Dualities_, Nucl.Phys.B438:109-137,1995 ([arXiv:hep-th/9410167](http://arxiv.org/abs/hep-th/9410167))

* {#Witten95} [[Edward Witten]], section 4 of _[[String Theory Dynamics In Various Dimensions]]_, Nucl.Phys.B443:85-126,1995 ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))

Review includes

* {#Aspinwall96} [[Paul Aspinwall]], _K3 Surfaces and String Duality_, in  [[Shing-Tung Yau]] (ed.): _Differential geometry inspired by string theory_ 1-95 ([arXiv:9611137](https://arxiv.org/abs/hep-th/9611137), [spire:426102](http://inspirehep.net/record/426102))

Further discussion includes

* [[Paul Aspinwall]], [[David Morrison]], _String Theory on K3 Surfaces_, in [[Brian Greene]], [[Shing-Tung Yau]] (eds.), _Mirror Symmetry II_, International Press, Cambridge, 1997, pp. 703-716 ([arXiv:hep-th/9404151](https://arxiv.org/abs/hep-th/9404151))

* [[Paul Aspinwall]], _Enhanced Gauge Symmetries and K3 Surfaces_, Phys.Lett. B357 (1995) 329-334 ([arXiv:hep-th/9507012](http://arxiv.org/abs/hep-th/9507012))

Specifically in relation to the putative [[K-theory]]-classification of [[D-brane charge]]:

* {#GarciaUranga05} Inaki Garcia-Etxebarria, [[Angel Uranga]], _From F/M-theory to K-theory and back_, JHEP 0602:008,2006 ([arXiv:hep-th/0510073](https://arxiv.org/abs/hep-th/0510073))


Specifically in [[M-theory on G2-manifolds]]:

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] section 6.4 of _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

Specifically in relation to [[Moonshine]]:

* [[Miranda Cheng]], Sarah M. Harrison, Roberto Volpato, Max Zimet, _K3 String Theory, Lattices and Moonshine_ ([arXiv:1612.04404](https://arxiv.org/abs/1612.04404))
 

[[!redirects K3 surfaces]]

[[!redirects K3]]

[[!redirects K3-surface]]
[[!redirects K3-surfaces]]
