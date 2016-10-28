[[!redirects super Minkowski space]]
[[!redirects super Minkowski space]]
[[!redirects super Minkowski space]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
=--
=--

#Contents#
* table of contents
{: toc}

## Idea

Super-Minkowski spacetime is a [[super spacetime]] which is an analog in [[supergeometry]] of ordinary [[Minkowski spacetime]]. It is a [[super Cartesian space]] whose odd coordinates form a real [[spinor representation]].

## Definition 

Ordinary $(d+1)$-dimensional [[Minkowski space]] may be understood as the  quotient $Iso(\mathbb{R}^{d-1,1})/(SO(d,1))$ of the [[Poincare group]] by the [[Lorentz group]] -- the [[translation group]].

Analogously, the for each real irreducible [[spin representation]] $N$ the
$dim(N)$-extended [[supermanifold]] **Minkowski superspace** or **super Minkowski space** is the quotient of [[supergroups]] of the [[super Poincaré group]] by the corresponding [[spin group]]

The _[[super-translation group]]_. See there for more details.

Alternatively, regarded as a [[super Lie algebra]] this is the quotient of the [[super Poincaré Lie algebra]] by the relevant [[Lorentz Lie algebra]].

## Properties

### Canonical coordinates
 {#CanonicalCoordinates}

We briefly review some basics of the canonical [[coordinates]] and the super [[Lie algebra cohomology]] of the [[super Poincaré Lie algebra]] and [[super Minkowski space]] (see also at _[[super Cartesian space]]_ and at _[[signs in supergeometry]]_).

By the general discussion at [[Chevalley-Eilenberg algebra]], we may characterize the [[super Poincaré Lie algebra]] $\mathfrak{Iso}(\mathbb{R}^{d-1,1|N})$ by its CE-algebra $CE(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$ "of [[left-invariant 1-forms]]" on its group manifold.

Let $d \in \mathbb{N}$ and let $N$ be a real [[spin representation]] of $Spin(d-1,1)$. See at _[[Majorana representation]]_ for details.

+-- {: .num_defn #CEAlgebraOfSuperPoincare}
###### Definition

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$ is generated on 

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

where $a \in \{0,1, \cdots, d-1\}$ is a spacetime index, and where $\alpha$ is an index ranging over a basis of the chosen [[Majorana spinor]] representation $N$.

The CE-differential defined as follows

$$
  d_{CE} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

and

$$
  d_{CE} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
  \,.
$$

(which is the differential for the [[semidirect product]] of the [[Poincaré Lie algebra]] [[action|acting]] on the given [[Majorana spinor]] representation)

and

$$
  d_{CE} \, e^{a } = \omega^a{}_b \wedge e^b + \overline{\psi} \Gamma^a \psi
$$

where on the right we have the spinor-to-vector pairing in $N$ ([def.](Majorana+spinor#SpinorToVectorBilinearPairing)).

This defines the [[super Poincaré super Lie algebra]]. After discarding the terms involving $\omega$ this becomes the CE algebra of the [[super translation algebra]] underlying super Minkowski spacetime.

=--

In this way the [[super-Poincaré Lie algebra]] and its extensions is usefully discussed for instance in ([D'Auria-Fr&#233; 82](#DAuriaFre82)) and in ([Azc&#225;rraga-Townsend 89](AzcarragaTownsend89), [CAIB 99](#CAIB99)). In much of the literature instead the following equivalent notation is popular, which more explicitly involves the [[coordinates]] on [[super Minkowski space]].

+-- {: .num_remark }
###### Remark

The abstract generators in def. \ref{CEAlgebraOfSuperPoincare} are identified with [[left invariant 1-forms]] on the [[super-translation group]] (= [[super Minkowski space]]) as follows.

Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[supermanifold]] $\mathbb{R}^{d|N}$ underlying the super translation group. Then the identification is 

* $\psi^\alpha = d \theta^\alpha$.

* $e^a = d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta$.

Notice that this then gives the above formula for the differential of the [[super-vielbein]] in def. \ref{CEAlgebraOfSuperPoincare} as

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


=--


+-- {: .num_remark #Supertorsion}
###### Remark

The term $\frac{i}{2}\bar \psi \Gamma^a \psi$ is sometimes called the *[[supertorsion]]* of the [[super-vielbein]] $e$, because the defining equation

$$
  d_{CE} e^{a } -\omega^a{}_b \wedge e^b = \frac{i}{2}\bar \psi \Gamma^a \psi
$$

may be read as saying that $e$ is [[torsion]]-free except for that term. Notice that this term is the only one that appears when the differential is applied to "Lorentz scalars", hence to object in $CE(\mathfrak{siso})$ which have "all indices contracted". See also at _[[torsion constraints in supergravity]]_.

Notably we have 

$$
  d \left( 
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \right)
  \propto
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
  \,.
$$

This remaining operation "$e \mapsto \Psi^2$" of the differential acting on Loretz scalars is sometimes denoted "$t_0$", e.g. in ([Bossard-Howe-Stelle 09, equation (8)](#BossardHoweStelle09)).

This relation is what govers all of the exceptional super Lie algebra cocycles that appear as WZW terms for the Green-Schwarz action below: for some combinations of $(D,p)$ a [[Fierz identity]] implies that the term

$$
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
$$

vanishes identically, and hence in these dimensions the term

$$
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
$$

is a [[cocycle]]. See also the [brane scan](#BraneScan) table below.

=--

### Cohomology and super $p$-branes

As opposed to ordinary [[Minkowski space]], the [[de Rham cohomology]] of [[left invariant forms]] of super-Minkowski space contains nontrivial exceptional [[cocycles]] (the _[[brane scan]]_). These serve as the [[Wess-Zumino-Witten model|WZW terms]] for the [[Green-Schwarz action functional]] (see there for more) of super-$p$-[[branes]] propagating on super-Minkowski space ([FSS 13](#FSS13)).

The corresponding $L_\infty$-extensions are _[[extended superspacetime]]_.

### As a central extension of the superpoint
 {#AsCentralExtensionOfTheSuperpoint}

Regarded as a [[super Lie algebra]], super Minkowski spacetime $\mathbb{R}^{d-1,1|N}$ has the single nontrivial super-Lie bracket given by the spinor bilinear pairing

$$
  \overline{(-)}\Gamma (-)
  \colon
  S \otimes S \longrightarrow V
$$

discussed in detail at _[[spin representation]]_.

Notice that this means that if one regards the [[superpoint]] $\mathbb{R}^{0|dim(N)}$ as an [[abelian super Lie algebra]], then super Minkowski spacetime is the [[Lie algebra extension]] of that by this bilinear pairing regarded as a super-[[Lie algebra cohomology|Lie algebra cocycle]] with [[coefficients]] in $\mathbb{R}^{d}$.

$$
  \array{
    \mathbb{R}^{d} &\longrightarrow& \mathbb{R}^{d-1,1|N}
    \\
    && \downarrow 
    \\
    && \mathbb{R}^{0|dim(N)}
  }
$$




## Related concepts

* [[super anti de Sitter spacetime]]



[[!include local and global geometry - table]]

## References 

* _Super spacetimes and super Poincar&#233;-group_ ([pdf](http://www.math.ucla.edu/~vsv/papers/ch6.pdf))

* [[Daniel Freed]], _Lecture 4 of [[Five lectures on supersymmetry]]_

* [[Veeravalli Varadarajan]], section 7 of _Supersymmetry for mathematicians: An introduction_


page 370, part II section II.3.3 of

* [[Leonardo Castellani]], [[Riccardo D'Auria]], _[[Pietro Fre]], [[Supergravity and Superstrings - A Geometric Perspective]]_

Discussion of how [[super L-infinity algebra]] [[L-infinity cocycle|extensions]] of super Minkowski spacetime yield all the [[brane scan]] of [[string theory]]/[[M-theory]] is in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet]]_ (2013)
  {#FSS13}

[[!redirects super Minkowski spacetime]]
[[!redirects super-Minkowski spacetime]]

[[!redirects super Minkowski spacetimes]]
[[!redirects super-Minkowski spacetimes]]