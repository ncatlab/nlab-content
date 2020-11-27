
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _complex Hopf fibration_ (named after [[Heinz Hopf]]) is a canonical nontrivial  [[circle principal bundle]] over the [[2-sphere]] whose total space is the [[3-sphere]].

$$
  S^1 \hookrightarrow S^3 \to S^2 
  \,.
$$

Its canonically [[associated bundle|associated]] [[complex line bundle]] is the [[basic line bundle on the 2-sphere]].

This we discuss below in 

* _[On the 3-sphere](#DefinitionFor3Sphere)_

More generally, there are four Hopf fibrations, on the 1-sphere, the 3-sphere, the 7-sphere and the 15-sphere, respectively. This we discuss in 

* _[On the 1-sphere, 3-sphere, 7-sphere and 15-sphere](#OnAllFourSpheres)_.

## On the 3-sphere
 {#DefinitionFor3Sphere}

### Homotopy-theoretic characterization
 {#HomotopyTheoreticCharacterization}

The [[Eilenberg-MacLane space]] $K(\mathbb{Z},2) \simeq B S^1$ is the [[classifying space]] for [[circle group]] [[principal bundles]]. By its very nature, it has a single nontrivial [[homotopy group]], the second, and this is isomorphic to the group of [[integers]]

$$
  \pi_2(K(\mathbb{Z},2)) \simeq \mathbb{Z}
  \,.
$$

This means that there is, up to [[homotopy]], a canonical (up to sign), continuous map from the 2-sphere 

$$
  \phi : S^2 \to K(\mathbb{Z},2)
  \,,
$$

such that $[\phi] \in \pi_2(K(\mathbb{Z},2)) = \pm 1 \in \mathbb{Z}$.

As any map into $K(\mathbb{Z},2)$ this classifies a [[circle group]] [[principal bundle]] over its [[domain]]. This is the Hopf fibration, fitting into the long [[fiber sequence]]

$$
  \array{
    S^1 &\hookrightarrow& S^3
    \\  
    && \downarrow
    \\
    && S^2
    &\stackrel{\phi}{\to}&
    B S^1 \simeq K(\mathbb{Z},2)
  }
  \,.
$$

In other words, the Hopf fibration is the $U(1)$-bundle with unit first [[Chern class]] on $S^2$.

### Realization via the complex numbers

An explicit [[topological space]] presenting the Hopf fibration may be obtained as follows. Identify

$$ 
  S^3 \simeq \{(z_0, z_1) \in \mathbb{C}\times \mathbb{C} \,|\, {|z_0|}^2 + {|z_1|}^2 = 1\}
$$

and

$$S^2 \simeq \mathbb{C P}^1 \simeq \mathbb{C} \sqcup \{\infty\}$$ 

Then the [[continuous function]] $S^3 \to S^2$ defined by  

$$(z_0, z_1) \mapsto \frac{z_0}{z_1}$$ 

gives the Hopf fibration. (Thus, the Hopf fibration is a circle bundle naturally associated with the canonical [[line bundle]].) Alternatively, if we use 

$$
  S^2 \simeq \{(z, x) \in \mathbb{C} \times \mathbb{R} 
  \,|\,
  {|z|}^2 + x^2 = 1\}
  \,.
$$

and identify this presentation of the 2-sphere with the complex projective line via [[stereographic projection]], the Hopf fibration is identified with the map  $S^3 \to S^2$ given by sending

$$
  (z_0, z_1) \mapsto (2 z_0 z_1^* , {|z_0|}^2 - {|z_1|}^2).
$$

### Realization via quaternions
 {#RealizationViaQuaternions}

Alternatively, we may regard $S^3 \simeq S(\mathbb{H})$ as the [[unit sphere]] in the [[quaternions]] and $S^2 \simeq S\left( \mathbb{H}_{\mathrm{im}}\right)$ as the unit sphere in the [[imaginary part|imaginary]] [[quaternions]]. Under this identification, the complex Hopf fibration is equivalently represented by

$$
  \array{
    S(\mathbb{H})
    &\longrightarrow&
    S\left( \mathbb{H}_{\mathrm{im}}\right)
    \\
    q 
      &\mapsto&
    q \cdot \mathbf{i} \cdot \overline{q}
  }
$$

where $\mathbf{i} \in S\left( \mathbb{H}_{\mathrm{im}}\right)$ is any unit imaginary quaternion.



### Realization via the Hopf construction

Regard $S^1 = U(1)$ as equipped with its [[circle group]] structure. This makes $S^1$ in particular an [[H-space]]. The Hopf fibration $S^1 \to S^3 \to S^2$  is the [[Hopf construction]] applied to this H-space.


### [[Spin(3)]]-[[action|equivariance]]

Consider 

1. the [[Spin(3)]]-[[action]] on the [[2-sphere]] $S^2$ which is induced by the defining action on $\mathbb{R}^3$ under the identification $S^2 \simeq S(\mathbb{R}^3)$;

1. the [[Spin(3)]]-action on the [[3-sphere]] $S^3$ which is induced under the exceptional [[isomorphism]] $Spin(3) \simeq Sp(1) = U(1,\mathbb{H})$ by the canonical left action of $U(1,\mathbb{H})$ on $\mathbb{H}$ via $S^3 \simeq S(\mathbb{H})$.

Then the complex Hopf fibration $S^3 \overset{h_{\mathbb{C}}}{\longrightarrow} S^2$ is [[equivariant]] with respect to these [[actions]].

A way to make the $Spin(3)$-equivariance of the complex Hopf fibration fully explicit is to observe that it is equivalently the following map of [[coset spaces]]:

$$
  \array{
    S^1 
      &\overset{fib(h_{\mathbb{C}})}{\longrightarrow}& 
    S^{3}
      &\overset{h_{\mathbb{C}}}{\longrightarrow}& 
    S^2
    \\
     = && = && =
    \\
    \frac{Spin(2)}{Spin(1)}
    &\longrightarrow&
    \frac{Spin(3)}{Spin(1)}
    &\longrightarrow&
    \frac{Spin(3)}{Spin(2)}  
  }
$$

## On the 1-sphere, 3-sphere, 7-sphere and 15-sphere
 {#OnAllFourSpheres}


### Via norms and projections

For each of the [[normed division algebra|normed division algebras]] over $\mathbb{R}$, the [[real numbers]], [[complex numbers]], [[quaternions]], [[octonions]]

$$A = \mathbb{R}, \mathbb{C}, \mathbb{H}, \mathbb{O},$$ 

there is a corresponding Hopf fibration of [[Hopf invariant one]]. 


The total space of the fibration is the space of pairs $(\alpha, \beta) \in A^2$ of unit norm: ${|\alpha|}^2 + {|\beta|}^2 = 1$. This gives [[spheres]] of dimension 1, [[3-sphere|3]], [[7-sphere|7]], and 15 respectively. The base space of the fibration is [[projective space|projective]] 1-space $\mathbb{P}^1(A)$, giving spheres of dimension 1, 2, 4, and 8, respectively. In each case, the Hopf fibration is the map 

$$S^{2^n - 1} \to S^{2^{n-1}}$$ 

($n = 1, 2, 3, 4$) which sends the pair $(\alpha, \beta)$ to $\alpha/\beta$. 

### Via the Hopf construction

When $X$ is a [[sphere]] that is an $H$-space, namely, one of the [[groups]] $S^0 = 1$ the [[trivial group]], $S^1 = \mathbb{Z}/2$ the [[group of order 2]], the [[3-sphere]] [[special unitary group]] $S^3 = SU(2)$;  or the [[7-sphere]] $S^7$ with its [[Moufang loop]] structure, then the Hopf construction produces the above four Hopf fibrations:

1. $S^0 \hookrightarrow S^1 \to S^1 $ -- [[real Hopf fibration]]
1. $ S^1 \hookrightarrow S^3 \to S^2 $ -- [[complex Hopf fibration]]
1. $ S^3 \hookrightarrow S^7 \to S^4 $ -- [[quaternionic Hopf fibration]]
1. $ S^7 \hookrightarrow S^{15} \to S^8 $ -- [[octonionic Hopf fibration]]

## Properties

### Relation to stable homotopy groups of spheres
 {#RelationToStableHomotopyGroupsOfSpheres}

Let 

$H_{\mathbb{C}} \in \pi_3(S^2)$,

$H_{\mathbb{H}} \in \pi_7(S^4)$

$H_{\mathbb{O}} \in \pi_{15}(S^8)$

be the [[homotopy class]] of the [[complex Hopf fibration]], the [[quaternionic Hopf fibration]] and the [[octonionic Hopf fibration]], respectively. Then their [[suspensions]] are the generators of the corresponding [[stable homotopy groups of spheres]]:

$$
  \begin{aligned}
  \Sigma H_{\mathbb{C}}
  & =
  \pm 1
    \in 
  \mathbb{Z}_2
  \simeq
  \pi_1^{st}
  \\
  \Sigma H_{\mathbb{H}}
  & =
  \pm 1
    \in 
  \mathbb{Z}_{24} 
    \simeq
  \pi_3^{st}
  \\
  \Sigma H_{\mathbb{O}}
  & =
  \pm 1
    \in 
  \mathbb{Z}_{240} 
    \simeq
  \pi_7^{st}
  \end{aligned}
$$

see [this MO comment](https://mathoverflow.net/a/224082/381)



## Applications

### Magnetic monopoles 

When [[line bundles]] are regarded as models for the topological structure underlying the [[electromagnetic field]] the Hopf fibration is often called "the [[magnetic monopole]]". We may think of the $S^2$ homotopically as being the 3-dimensional [[Cartesian space]] with origin removed $\mathbb{R}^3 - \{0\}$ and think of this as being 3-dimensional physical space with a unit point [[magnetic charge]] at the origin removed. The corresponding [[electromagnetic field]] away from the origin is given by a [[connection on a bundle|connection]] on the corresponding Hopf fibration bundle.

### K-theory

In complex [[K-theory]], the Hopf fibration represents a class $H$ which generates the [[cohomology ring]] $K_U(S^2)$, and satisfying the relation $H^2 = 2 \cdot H - 1$, or $(H-1)^2 = 0$. (So in particular $H$ has an [[inverse]] $H^{-1} = 2- H $, see at [[Bott generator]].) 

A succinct formulation of [[Bott periodicity]] for [[complex K-theory]] is that for a space $X$ whose [[homotopy type]] is that of a [[CW-complex]], we have 

$$K(S^2 \times X) \cong K(S^2) \otimes K(X)$$ 

(It would be interesting to see whether this can be proved by internalizing the (classically easy) calculation for $K(S^2)$ to the topos of sheaves over $X$.)

The Hopf fibrations over other [[normed division algebras]] also figure in the more complicated case of [[real K-theory]] $K_O$: they can be used to provide generators for the non-zero [[homotopy groups]] $\pi_n(B O)$ for the [[classifying space]] of the [[stable orthogonal group]], which are periodic of period 8 (not coincidentally, 8 is the dimension of the largest normed division algebra $\mathbb{O}$). [To be followed up on.] 

## Related concepts

* [[Hopf construction]]

* [[Hopf invariant one]]

* [[real Hopf fibration]], [[quaternionic Hopf fibration]], [[octonionic Hopf fibration]]

* [[complex projective space]]

## References
  {#References}

Exposition:

* Saifuddin Syed, _Group structure on spheres and the Hopf fibration_ ([[SyedHopfFibration.pdf:file]])

Review:

* [[Herman Gluck]], [[Frank Warner]], [[Chung Tao Yang]], Section 6 of: _Division algebras, fibrations of spheres by great spheres and the topological determination of space by the gross behavior of its geodesics_, Duke Math. J. Volume 50, Number 4 (1983), 1041-1076 ([euclid:dmj/1077303489](https://projecteuclid.org/euclid.dmj/1077303489))

* {#GluckWarnerZiller86} [[Herman Gluck]], [[Frank Warner]], [[Wolfgang Ziller]], _The geometry of the Hopf fibrations_, L'Enseignement Math&eacute;matique, t.32 (1986), p. 173-198 ([doi:10.5169/seals-55085](http://doi.org/10.5169/seals-55085))


* _[Third homotopy group of the sphere and Hopf fibration](https://chiasme.wordpress.com/2014/01/04/third-homotopy-group-of-the-sphere-and-hopf-fibration/)_

Formulation in [[homotopy type theory]]:

* [HoTT Wiki](https://ncatlab.org/homotopytypetheory/show/HomePage), _[[homotopytypetheory:Hopf fibration]]_

Relation to [[skyrmions]]:


* [[Sven Bjarke Gudnason]], [[Muneto Nitta]], _Linking number of vortices as baryon number_ ([arXiv:2002.01762](https://arxiv.org/abs/2002.01762))

Discussion of [[supersymmetry|supersymmetric]] Hopf fibrations:

* [[A. P. Balachandran]], G. Marmo, B.-S. Skagerstam and A. Stern, section 9.3 of _Gauge Symmetries and Fibre Bundles_, Lect. Notes in Physics 188, Springer-Verlag, Berlin, 1983 ([arXiv:1702.08910](https://arxiv.org/abs/1702.08910))

* Simon Davis, section 3 of _Supersymmetry and the Hopf fibration_ ([doi:10.4995/agt.2012.1623](https://doi.org/10.4995/agt.2012.1623))

[[!redirects Hopf fibrations]]

[[!redirects complex Hopf fibration]]