
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[equations of motion]] of [[supergravity]] typically imply -- or are even equivalent to ([Candiello-Lechner 93](#CandielloLechner93), [Howe 97](#Howe97)), that the [[supertorsion|super-]][[torsion of a Cartan connection|torsion]] of the super-[[vielbein fields]] vanishes. At least in some cases these _supergravity torsion constraints_ may naturally be understood as saying that supergravity solutions are ([[higher Cartan geometry|higher]]) [[super-Cartan geometry]] modeled on [[extended super Minkowski spacetime]] _with_ its canonical [[torsion of a G-structure]], due to the fact that the [[left invariant 1-forms]] on super-Minkowski space are not closed.



### From the canonical torsion of super-Minkowski spacetime
 {#CanonicalTorsionOfSuperMinkowskiSpacetime}

The torsion constraint is naturally understood by regarding [[supergravity]] as [[Cartan geometry]] for the inclusion of the [[orthogonal group]] into a [[super Poincare group]] and by noticing that the corresponding local model space, which is [[super-Minkowski spacetime]] $\mathbb{R}^{d|N}$, canonically has non-vanishing torsion.

Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[supermanifold]] $\mathbb{R}^{d|N}$ underlying the [[super translation group]]. Then the [[left-invariant 1-forms]] are

* $\psi^\alpha = d \theta^\alpha$.

* $e^a = d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta$.

Here the extra summand in the equation for $e^a$ (necessary to make it left-invariant) causes it to be non-closed:

$$ 
  \begin{aligned}
    d e^a & = d (d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta)
    \\
    & = \frac{i}{2} d \overline{\theta}\Gamma^a d \theta
    \\
    & = \frac{i}{2} \overline{\psi}\Gamma^a \psi
  \end{aligned}
  \,.
$$

Taking the [[spin connection]] $(\omega^a{}_b)$ on $\mathbb{R}^{d|N}$ to vanish, as usual, this means that there is non-vanishing [[torsion]]:

$$
  \begin{aligned}
    \tau^a & = \mathbf{d} e^a + \omega^a{}_b \wedge e^b 
    \\
    & = \mathbf{d} e^a
    \\
    & = \frac{i}{2} \overline{\psi}\Gamma^a \psi
  \end{aligned}
$$

Depending on perspective one might say that it is the [[supertorsion]] that vanishes (see at _[[super-Minkowski spacetime]]_ and at _[[D'Auria-Fre formulation of supergravity]]_ for this perspective), or, alternatively, that one is dealing with [[Cartan geometry]]/[[G-structure]] whose local model space carries non-vanishing torsion, see [below](#InTermsOfTorsionTwistedGStructure). 

Notice that the torison-full but left-invariant forms are of course obtained from the torsion-free but non-left-invartiant forms by a $GL(\mathbb{R}^{d|N})$-valued function:

$$
  \left(   
     \array{
        e^a
        \\
        \psi^\alpha
     }
  \right)
  =
  \left(
    \array{
      id & \tfrac{i}{2}\Gamma^a{}_{\alpha \beta} \theta^\alpha
      \\
      0 & id
    }
  \right)
  \left(  
    \array{
      \mathbf{d}x^a
      \\
      \mathbf{d}\theta^\alpha
    }
  \right)
$$

$$
  \left(  
    \array{
      \mathbf{d}x^a
      \\
      \mathbf{d}\theta^\alpha
    }
  \right)
  =
  \left(
    \array{
      id & -\tfrac{i}{2}\Gamma^a{}_{\alpha \beta} \theta^\alpha
      \\
      0 & id
    }
  \right)
  \left(   
     \array{
        e^a
        \\
        \psi^\alpha
     }
  \right)
$$

This shows that regarding

$$
  (E^A) \coloneqq (E^a, E^\alpha) \coloneqq (e^a, \Psi^\alpha)
$$

as a [[super-vielbein]] is consistent: this is indeed a [[homotopy]] in

$$
  \array{
     \mathbb{R}^{d|N} &\to& \ast &\to& \mathbf{B}O(\mathbb{R}^{d|N})
     \\
     & 
     {}_{\mathllap{\tau_{\mathbb{R}^{d|N}}}}\searrow 
     &
     \swArrow_{E}
     & 
     \swarrow_{\mathrlap{O(\mathbb{R}^{d|N})\mathbf{Struc}}}
     \\
     && \mathbf{B}GL(\mathbb{R}^{d|N})
  }
$$

but not the tautological one given by

$$
  \array{
     \mathbb{R}^{d|N} &\to& \ast &\to& \mathbf{B}O(\mathbb{R}^{d|N})
     \\
     & 
     \searrow 
     &
     \downarrow
     & 
     \swarrow
     \\
     && \mathbf{B}GL(\mathbb{R}^{d|N})
  }
$$

where the left triangle is that which exhibits the canonical trivialization of the [[frame bundle]] of $\mathbb{R}^{d|N}$.



### In terms of torsion-twisted $G$-structure
 {#InTermsOfTorsionTwistedGStructure}

Given a [[subgroup]] $G\hookrightarrow GL(V)$ of the [[general linear group]] of a linear model space $V$ (e.g. [[super-Minkowski spacetime]] $\mathbb{R}^{d|N}$), then a [[G-structure]] is [[integrability of G-structure|first-order integrable]] if on the first-order [[infinitesimal neighbourhoods]] of any point it is equal to the canonical (trivial) $G$-structure on $V$. Ordinarily the standard [[torsion]] on $V$ vanishs, and if so then so does that of any first-order integrable $G$-structire, which is the reason why for these the [[torsion of a G-structure]] vanishes.

But in the situation of $V$ being [[super-Minkowski spacetime]] as [above](#CanonicalTorsionOfSuperMinkowskiSpacetime), the torsion of the local model space does not vanish, and so accordingly neither does that of a first-order integrable $G$-structure in this case.

This perspective on the torsion constraints in supergravity is adopted in ([Lott 01](#Lott01)), see there around (38) of the original article or section 4 of the review on the arXiv.

## Properties

### Relation to supergravity equations of motion

The [[supergravity]] [[equations of motion]] typically imply the torsion constraints. See at [super p-brane -- On curved spacetimes](Green-Schwarz+action+functional#OnCurvedSpacetime) for more.

With enough [[supersymmetry]], the torsion constraints (always together with the [[Bianchi identities]] on the superfields, see at _[[D'Auria-Fre formulation of supergravity]]_) may even become equivalent to the supergravity equations of motion. This is so for [[11-dimensional supergravity]] ([Candiello-Lechner 93](#CandielloLechner93), [Howe 97](#Howe97)) and maybe its maximally supersymmetric [[KK-compactifications]]. See at _[Examples -- 11d SuGra](#Examples11dSuGra)_.


### Relation to CR-geometry

A close [[analogy]] between [[CR geometry]] and [[supergravity]] [[superspacetimes]] (as both being [[torsion of a G-structure|torsion-ful]] [[integrable G-structures]]) is pointed out in ([Lott 01 exposition (4.2)](Lott01)).

## Examples

In accord with the [above](#CanonicalTorsionOfSuperMinkowskiSpacetime), typically the [[equations of motion]] of a [[supergravity]] theory constrain the spinorial part of the torsion to have components $(\Gamma^a)_{\alpha \beta}$.


### 11d supergravity
 {#Examples11dSuGra}

For instance in [[11-dimensional supergravity]] this is ([Bergshoeff-Sezgin-Townsend 87, equation (14)](#BergshoeffSezginTownsend87)).

More in detail, ([Candiello-Lechner 93 (5.6)](#CandielloLechner93), [Howe 97](#Howe97)) show that imposing (on some chart) $\mathbf{d} E^a + \omega^{a}{}_b \wedge E^b - \bar \psi \Gamma^a \psi  = 0$ as well as $(\mathbf{d} \Psi +\tfrac{1}{4}\omega^{a b} \Gamma_{a b}\Psi)_{\theta \theta} = 0$ implies the equations of motion of [[11d supergravity]]. 

Moreover, setting $\mathbf{d} \Psi +\tfrac{1}{4}\omega^{a b} \Gamma_{a b}\Psi = 0$ generally (not just the component proportional to the wedge product of two fermionic 1-forms, hence requiring the full supertorsion tensor to be that of super-Minkowski spacetime)) then ([Candiello-Lechner 93, (5.8) with (6.5)](#CandielloLechner93))  this in addition puts the [[field strength]] of the [[supergravity C-field]] to 0. Hence this implies solutions to the ordinary vacuum [[Einstein equations]] in 11d. Such solutions are considered notably in the context of [[M-theory on G2-manifolds]] (e.g. [Acharya 02, p. 9](M-theory+on+G2-manifolds#Acharya02)). See also at _[M-theory on G2-manifolds -- Details -- Vacuum solution and torsion constraints](M-theory+on+G2-manifolds#VacuumSolutionsAndTorsion)_.


## Related concepts

* [[CR manifold]]

* [[D'Auria-Fre formulation of supergravity]]

## References

### General

The formulation of supergravity equations of motion in terms of constraints on the torsion tensor goes back to 

* [[Julius Wess]] [[Bruno Zumino]], _Superspace formulation of supergravity_, Phys. Lett. B66 (1977), 361&#8211;364.

A mathematical formulation in terms of [[torsion of a G-structure|torsion-full]] [[first-order integrable G-structure|first-order integrable]] [[G-structures]] on [[supermanifolds]] (for low dimensional supergravity theories) is given in

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

which is followed up in

* [[Michel Egeileh]], [[Fida El Chami]], _Some remarks on the geometry of superspace supergravity_, J.Geom.Phys. 62 (2012) 53-60 ([spire](http://inspirehep.net/record/1333125))


### For 11d supergravity

Discussion of torsion constrains for [[11-dimensional supergravity]] from the point of view of consistency of the [[membrane]] [[Green-Schwarz action functional]] is in

* {#BergshoeffSezginTownsend87}  [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[Mike Duff]],  (ed.), _[[The World in Eleven Dimensions]]_ 69-72 ([pdf](http://streaming.ictp.trieste.it/preprints/P/87/010.pdf), [spire](http://inspirehep.net/record/248230?ln=en))


The claim that this torsion constraint in  [[11-dimensional supergravity]] is already equivalent to all of the [[equations of motion]] is due to

*  {#CandielloLechner93} A. Candiello, K. Lechner, _Duality in Supergravity Theories_, Nucl.Phys. B412 (1994) 479-501 ([arXiv:hep-th/9309143](http://arxiv.org/abs/hep-th/9309143))


* {#Howe97} [[Paul Howe]], _Weyl Superspace_, Physics Letters B
Volume 415, Issue 2, 11 December 1997, Pages 149&#8211;155 ([arXiv:hep-th/9707184](http://arxiv.org/abs/hep-th/9707184))



For commentary see also ([Nilsson 00, section 2](#Nilsson00)) and

* {#CGNN00} [[Martin Cederwall]], [[Ulf Gran]], Mikkel Nielsen, [[Bengt Nilsson]], _Manifestly supersymmetric M-theory_, JHEP 0010 (2000) 041 ([arXiv:hep-th/0007035](http://arxiv.org/abs/hep-th/0007035))

Discussion of possible deformations of the torsion constraint ([[M-theory]] corrections) includes

* [[Martin Cederwall]], [[Ulf Gran]], Mikkel Nielsen, [[Bengt Nilsson]], _Generalised 11-dimensional supergravity_, in A. Semikhatov, M. Vasiliev and V. Zaikin (eds.) Proceedings of "Quantization, Gauge Theory & Strings", Moscow 2000 ([arXiv:hep-th/0010042](http://arxiv.org/abs/hep-th/0010042))


* [[Paul Howe]], [[Dimitrios Tsimpis]], _On higher-order corrections in M theory_, JHEP 0309 (2003) 038 ([arXiv:hep-th/0305129](http://arxiv.org/abs/hep-th/0305129))

### For 10d heterotic supergravity

Discussion of torsion constraints for [[heterotic supergravity]] goes back to ([Nilsson 81](Green-Schwarz+action+functional#Nilsson81)) and includes

* [[Paul Howe]], A. Umerski, _On superspace supergravity in ten dimensions_, Phys. Lett. B 177 (1986) 163.

* [[Paul Howe]], _Heterotic supergeometry revisited_ ([arXiv:0805.2893](http://arxiv.org/abs/0805.2893))

* {#Nilsson00} [[Bengt Nilsson]], _A superspace approach to branes and supergravity_ ([arXiv:hep-th/0007017](http://arxiv.org/abs/hep-th/0007017))

### For 4d supergravity
 {#ReferencesFor4d}

For [[d=4 N=1 supergravity]] the torsion is again constrained to be equal to the left-invariant torsion of super-Minkowski spacetime, see for instance


* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], volume 2, (III.2.28a), (III.3.66a) of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* Daniel Patrick Butter, section 2.2.5 of _On conformal superspace and the One-Loop Effective Action in Supergravity_, 2010 ([pdf](http://digitalassets.lib.berkeley.edu/etd/ucb/text/Butter_berkeley_0028E_10582.pdf))

### For 2d supergravity / superstring worldsheets / super Riemann surfaces

* [[Suresh Govindarajan]], [[Burt Ovrut]], _A geometric interpretation for the torsion constrains of $(2,0)$-heterotic worldhseet supergravity_, Mod. Phys. Lett. A6(1991), 3341. ([pdf](http://www.physics.iitm.ac.in/~suresh/sgtalk/talk_html/torsion.pdf))


[[!redirects supergravity torsion constraint]]
[[!redirects supergravity torsion constraints]]

[[!redirects torsion constraint of supergravity]]
[[!redirects torsion constraints of supergravity]]