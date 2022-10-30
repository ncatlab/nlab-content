
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

$N=1$ [[supergravity]] in $d = 11$.

> for the moment see the respective section at [[D'Auria-Fre formulation of supergravity]]

## The action functional

(...)

### Kinetic terms

(...)

### The higher Chern-Simons term

> under construction

$$
  \int_X
  \left(
  \frac{1}{6} 
  \left(
    C \wedge G \wedge G
    -
    C \wedge
    \frac{1}{8}
    \left(
      p_2 + (\frac{1}{2}p_1)^2 
    \right)
  \right)
  \right)
$$

where $p_i$ is the $i$th [[Pontryagin class]].

$$
  \lambda := \frac{1}{2}p_1
  \,.
$$

Concerning the integrality of

$$
  I_8 := \frac{1}{48}(p_2 + (\lambda)^2)
$$

on a [[spin structure|spin manifold]] $X$.
([Witten96, p.9](#Witten96))

First, the [[index]] of a [[Dirac operator]] on $X$ is

$$
  I = \frac{1}{1440}(7 (\frac{1}{2}p_1)^2 - p_2) \in \mathbb{Z}
  \,.
$$

Notice that $1440 = 6 x 8 x 30$. So

$$
  p_2 - (\frac{1}{2}p_2)^2 = 6 ( (\frac{1}{2}p_1)^2 - 30 x 8 I) 
$$

is divisble by 6. 

Assume that $(\frac{1}{2}p_1)$ is further divisble by 2 (see the relevant discussion at _[[M5-brane]]_).

$$
  (\frac{1}{2}p_1) = 2 x
  \,.
$$

Then the above becomes

$$
  p_2 - (\frac{1}{2}p_2)^2 = 24 ( x^2 - 30 x 2 I) 
$$

and hence then $p_2 + (\frac{1}{2}p_1)^2$ is divisible at least by 24.

But moreover, on a [[spin structure|Spin manifold]]
the [[first fractional Pontryagin class]] $\frac{1}{2}p_1$ is 
the [[Wu class]] $\nu_4$ (see there). By definition this means that

$$
  x^2 = x (\frac{1}{2}p_1) \; mod \; 2
$$

and so when $(\frac{1}{2}p_1)^2$ is further divisible by 2 we have that 
$p_2 - (\frac{1}{2}p_1)^2$ is divisible by 48. Hence $I_8$ is integral.


### The hidden deformation

There is in fact a hidden 1-parameter deformation of the Lagrangian of 11d sugra.
Mathematically this was maybe first noticed in ([D'Auria-Fre 82 ](#DAuriaFre)) around equation (4.25). This shows that there is a topological term which may be expressed as 

$$
  \propto \int_{X_11} G_4 \wedge G_7
$$

where $G_4$ is the [[curvature]] 3-form of the [[supergravity C-field]] and $G_7$ that of the [[electric-magnetic duality|magnetically dual]] [[C6-field]]. However, ([D'Auria-Fre 82 ](#DAuriaFre)) consider only topologically trivial (trivial [[instanton sector]]) configurations of the  [[supergravity C-field]], and since on them this term is a total derivative, the authors "drop" it. 

The term then re-appears in the literatur in ([Bandos-Berkovits-Sorokin 97, equation (4.13)](#BandosBerkovitsSorokin97)).
And it seems that this is the same term later also redicovered around equation (4.2) in ([Tsimpis 04](#Tsimpis04)).



### BPS states

The basic [[BPS spates]] of 11d SuGra are

* the [[M2-brane]]

* the [[M5-brane]]

* the [[M-wave]]

* the [[Kaluza-Klein monopole]]

(e.g. [EHKNT 07](#EHKNT07))


## Related concepts

* [[supergravity]]

* 10-dimensional [[type II supergravity]], [[heterotic supergravity]]

* [[7-dimensional supergravity]]

* [[5-dimensional supergravity]]

* [[4-dimensional supergravity]]

  * [[M-theory on G2-manifolds]], [[G2-MSSM]]

  * [[Freund-Rubin compactification]]

* [[3-dimensional supergravity]]

* [[supergravity C-field]], [[supergravity Lie 3-algebra]], [[supergravity Lie 6-algebra]]

* [[Ho?ava-Witten theory]]

* [[M-theory]]

* [string theory FAQ -- Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)


[[!include table of branes]]

## References

### General

That there is a maximal dimension $d = 11$ in which supergravity may exist was found in 

* {#Nahm78} [[Werner Nahm]], _[[Supersymmetries and their Representations]]_, Nucl.Phys. B135 (1978) 149 ([spire](https://inspirehep.net/record/120988/), [pdf](http://cds.cern.ch/record/132743/files/197709213.pdf))

The theory was then actually constructed in

* E. Cremmer, [[Bernard Julia]], [[Joël Scherk]], _Supergravity in theory in 11 dimensions_ Phys. Lett. 76B (1978) 409

Formulation in terms of [[supergeometry]] ("superspace formulation") is in 

* {#Cremmerferrara80} E. Cremmer, S. Ferrara, _Formulation of Eleven-Dimensional Supergravity in Superspace_, Phys.Lett. B91 (1980) 61

* [[Lars Brink]], [[Paul Howe]], _Eleven-Dimensional Supergravity on the Mass-Shell in Superspace_, Phys.Lett. B91 (1980) 384


The description of 11d supergravity in terms of the [[D'Auria-Fre formulation of supergravity]] originates in 

* {#DAuriaFre} [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140
 

of which a textbook account is in 

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapters III.8 and V.4-V.11 in _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific, 1991


The topological deformation (almost) noticed in equation (4.25) of [D'Auria-Fre 82](#DAuriaFre82) later reappears in (4.13) of

* {#BandosBerkovitsSorokin97} [[Igor Bandos]], [[Nathan Berkovits]], [[Dmitri Sorokin]], _Duality-Symmetric Eleven-Dimensional Supergravity and its Coupling to M-Branes_, Nucl. Phys. B522 (1998) 214-233 ([arXiv:hep-th/9711055](http://arxiv.org/abs/hep-th/9711055))
 

and around (4.2) of
 
* {#Tsimpis04} Dimitrios Tsimpis, _11D supergravity at $\mathcal{O}(l^3)$_,  	JHEP0410:046,2004 ([arXiv:hep-th/0407271](http://arxiv.org/abs/hep-th/0407271))

More recent textbook accounts include

* [[Antoine Van Proeyen]], [[Daniel Freedman]], section 10 of _Supergravity_, Cambridge University Press, 2012 

Discussion of the equivalence of the 11d SuGra [[equations of motion]] with the [[supergravity torsion constraints]] is in 

* {#Howe97} [[Paul Howe]], _Weyl Superspace_, Physics Letters B
Volume 415, Issue 2, 11 December 1997, Pages 149&#8211;155 ([arXiv:hep-th/9707184](http://arxiv.org/abs/hep-th/9707184))

following 

*  A. Candiello, K. Lechner, _Duality in Supergravity Theories_, Nucl.Phys. B412 (1994) 479-501 ([arXiv:hep-th/9309143](http://arxiv.org/abs/hep-th/9309143))

Much computational detail is displayed in

* A. Miemiec, I. Schnakenburg, _Basics of M-Theory_, Fortsch.Phys. 54 (2006) 5-72 ([arXiv:hep-th/0509137](http://arxiv.org/abs/hep-th/0509137))

### Classical solutions and BPS states
	
Bosonic solutions of eleven-dimensional supergravity were studied in the 1980s in the context of [[Kaluza-Klein mechanism|Kaluza-Klein]] supergravity. The topic received renewed attention in the mid-to-late 1990s as a result of the [[branes]] and duality paradigm and the [[AdS/CFT correspondence]].

One of the earliest solutions of eleven-dimensional supergravity is the maximally supersymmetric Freund-Rubin background with geometry $AdS_4 \times S^7$ and 4-form [[flux]] proportional to the [[volume form]] on $AdS_4$. 

* Peter Freund, Mark Rubin, _Dynamics of Dimensional Reduction_ Phys.Lett. B97 (1980) 233-235 ([inSpire](http://inspirehep.net/record/154579?ln=en))

The radii of curvatures of the two factors are furthermore in a ratio of 1:2. The modern avatar of this solution is as the near-horizon limit of coincident [[M2-branes]].

* [[Mike Duff]], [[Kellogg Stelle]], _Multimembrane solutions of D = 11 supergravity_ , Phys.Lett. B253 (1991) 113-118 ([web](http://adsabs.harvard.edu/abs/1991PhLB..253..113D))

Shortly after the original Freund-Rubin solution was discovered, Englert discovered a deformation of this solution where one could turn on [[flux]] on the $S^7$; namely, singling out one of the [[Killing spinors]] of the solution, a suitable multiple of the 4-form one constructs by squaring the [[spinor]] can be added to the [[volume form]] in $AdS_4$ and the resulting 4-form still obeys the supergravity [[Euler-Lagrange equations|field equations]], albeit with a different relation between the radii of [[curvature]] of the two factors. The flux breaks the [[special orthogonal group|SO(8)]] symmetry of the [[sphere]] to an $SO(7)$ subgroup.

* [[Francois Englert]], _Spontaneous Compactification of Eleven-Dimensional Supergravity_ Phys.Lett. B119 (1982) 339 ([inSPIRE](http://inspirehep.net/record/180130))

Some of the above is taken from [this TP.SE thread](http://theoreticalphysics.stackexchange.com/questions/329/modern-avatar-of-englerts-solution).

A classification of symmetric solutions is discussed in

* [[José Figueroa-O'Farrill]], _Symmetric M-Theory Backgrounds_ ([arXiv:1112.4967](http://arxiv.org/abs/1112.4967))

Discussion of [[black branes]] and [[BPS states]] includes

* {#Stelle98} [[Kellogg Stelle]], section 3 of _BPS Branes in Supergravity_ ([arXiv:hep-th/9803116](http://arxiv.org/abs/hep-th/9803116))

* {#EHKNT07} [[Francois Englert]], Laurent Houart, [[Axel Kleinschmidt]], [[Hermann Nicolai]], Nassiba Tabti, _An $E_9$ multiplet of BPS states_, JHEP 0705:065,2007 ([arXiv:hep-th/0703285](http://arxiv.org/abs/hep-th/0703285))

* Andrew Callister, [[Douglas Smith]], _Topological BPS charges in 10 and 11-dimensional supergravity_, Phys. Rev. D78:065042,2008 ([arXiv:0712.3235](http://arxiv.org/abs/0712.3235))

* Andrew Callister, [[Douglas Smith]], _Topological charges in $SL(2,\mathbb{R})$ covariant massive 11-dimensional and Type IIB SUGRA_, Phys.Rev.D80:125035,2009 ([arXiv:0907.3614](http://arxiv.org/abs/0907.3614))

* Andrew Callister, _Topological BPS charges in 10- and 11-dimensional supergravity_, thesis 2010 ([spire](http://inspirehep.net/record/1221591?ln=en))


* A. A. Golubtsova, V.D. Ivashchuk, _BPS branes in 10 and 11 dimensional supergravity_, talk at DIAS 2013 ([pdf slides](http://theor.jinr.ru/~diastp/summer13/lectures/Golubtsova.pdf))

* Cristine N. Ferreira, _BPS solution for eleven-dimensional supergravity with a conical defect configuration_ ([arXiv:1312.0578](http://arxiv.org/abs/1312.0578))


### Truncations and compactifications

* [[Hermann Nicolai]], Krzysztof Pilch, _Consistent truncation of $d = 11$ supergravity on $AdS_4 x S^7$_ ([arXiv:1112.6131](http://arxiv.org/abs/1112.6131))

### Topology and anomaly cancellation

Discussion of [[quantum anomaly]] cancellation and [[Green-Schwarz mechanism]] in 11D supergravity includes the following articles.

* [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_ ([arXiv:hep-th/9609122](http://arxiv.org/abs/hep-th/9609122))
 {#Witten96}

See also the relevant references at _[[M5-brane]]_.

* [[Daniel Freed]], _Two nontrivial index theorems in odd dimensions_ ([arXiv:dg-ga/9601005](http://arxiv.org/abs/dg-ga/9601005))

* Adel Bilal, Steffen Metzger, _Anomaly cancellation in M-theory: a critical review_ ([arXiv:hep-th/0307152](http://arxiv.org/abs/hep-th/0307152))



### Description by exceptional generalized geometry

* Paulo Pires Pacheco, [[Daniel Waldram]], _M-theory, exceptional generalised geometry and superpotentials_ ([arXiv:0804.1362](http://arxiv.org/abs/0804.1362))

[[!redirects 11d supergravity]]