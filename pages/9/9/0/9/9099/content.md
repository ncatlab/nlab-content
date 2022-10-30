
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

The case of [[higher dimensional Chern-Simons theory]] in [[dimension]] 7.

## Examples

We discuss

1. [Abelian 7d CS theory](#AbelianTheory) of an abelian 3-form connection;

1. [7d p2 theory on String 2-connections](#OnString2Connections)

1. [2-species cup-product theory on a G2 manifold](#TwoSpeciesCupProductTheoryOnG2Manifold)

### Abelian theory
 {#AbelianTheory}

A basic 7d [[higher dimensional Chern-Simons theory]] is the abelian theory, whose [[extended Lagrangian]] $\mathbf{L}$ is the [[diagonal]] of the [[cup product in ordinary differential cohomology]] 

$$
  \mathbf{L}_{\mathbf{DD}\cup \mathbf{DD}}
  \colon
  \mathbf{B}^3 U(1)_{conn}
  \stackrel{\Delta}{\to}
  \mathbf{B}^3 U(1)_{conn}
  \times
  \mathbf{B}^3 U(1)_{conn}
  \stackrel{\widehat {\cup}}{\to}
  \mathbf{B}^7 U(1)_{conn}
  \,.
$$

The [[transgression]] of this to [[codimension]] 0 hence for $\Sigma_7$ a [[closed manifold]] of [[dimension]] 7 is the [[action functional]]

$$
  \exp\left(  
    2 \pi i \int_{\Sigma_7}
    [\Sigma_7, \mathbf{L}_{\mathbf{DD}\cup \mathbf{DD}}]
  \right)
  \;\colon\;
  [\Sigma_7, \mathbf{B}^3 U(1)_{conn}]
  \to 
  U(1)
  \,.
$$

A [[gauge field]] configuration 

$$
  \phi \;\colon\; \Sigma_7 \to \mathbf{B}^3 U(1)_{conn}
$$

here is a [[circle n-bundle with connection|circle 3-bundle with connection]]. In the special case that the underlying [[circle 3-group]] [[principal 3-bundle]] is trivializable and trivialized, this is equivalently a [[differential 3-form]] $C \in \Omega^3(\Sigma_7)$ and the above [[action functional]] takes this to the simple expression

$$
  C 
   \mapsto 
  \exp\left(
     2 \pi i \int_{\Sigma_7}  C \wedge d C
  \right)
  \in U(1)
  \,,
$$

where in the [[exponent]] we have the [[integration of differential forms]] over the [[wedge product]] of $C$ with its [[de Rham differential]]. On general field configurations the action functional is the suitable globalization of this expression.


In ([Witten 96](#WittenI)), ([Witten 98](#Witten98)) a slight refinement of this construction (a  [[quadratic refinement]] induced by an [[integral Wu structure]]) was argued to be the [[holographic principle|holographic dual]] to the [[self-dual higher gauge theory]] of the abelian self-dual 2-form gauge field in the [[6d (2,0)-superconformal QFT]] on the [[worldvolume]] of the [[M5-brane]]. The issue of the quadratic refinement was discussed in more detail in ([HopkinsSinger](#HopkinsSinger)). A refinement to [[extended Lagrangians]] as above is discussed in ([FSSII](#FSSII)).

By the argument in ([Witten98](#Witten98)) the above relation holds when we interpret the fields $\phi \colon : \Sigma_7 \to \mathbf{B}^3 U(1)_{conn}$ as the [[supergravity C-field]] after [[Kaluza-Klein mechanism|compactification]] on a 4-[[sphere]] in the [[AdS-CFT|AdS7-CFT6]] setup. By the discussion at [[11-dimensional supergravity]] this field is in general not simply a 3-connection as above but receives corrections by a [[Green-Schwarz mechanism]] and "flux quantization" which give it non-abelian components. This, and the resulting non-abelian generalization of the above extended Lagrangian is discussed in ([FSSI](#FSSI), [FSSII](#FSSII)).

The nonabelian 7d action functional this obtained contains the following two examples as summands.

### Nonabelian $p_2$ theory on String 2-connections 
 {#OnString2Connections}

The [[second fractional Pontryagin class]] 

$$
  [\tfrac{1}{6}p_2] \in H^8(B String, \mathbb{Z})
$$
 
has a smooth and differential refinement (see at _[[twisted differential fivebrane structure]]_) to an [[extended Lagrangian]]

$$
  \tfrac{1}{2}\hat \mathbf{p}_2
  \;\colon\;
  \mathbf{B}String_{conn}
  \to 
  \mathbf{B}^7 U(1)_{conn}
  \,.
$$

where the domain is the [[smooth infinity-groupoid|smooth]] [[moduli infinity-stack|moduli 2-stack]] of [[String 2-group]] [[connection on a 2-bundle|principal 2-connections]] (see at _[[differential string structure]]_ for more). This modulates the [[Chern-Simons circle 7-bundle]] with connection on $\mathbf{B}String_{conn}$.

The [[transgression]] of this to codimension 0 yields an [[action functional]]

$$
  \exp\left(
    2 \pi i \int_{\Sigma_7}
    [\Sigma_7, \tfrac{1}{6}\hat \mathbf{p}_2]
  \right)
  \;\colon\;
  [\Sigma_7, \mathbf{B}String_{conn}]
  \to 
  U(1)
$$

on string 2-connection fields. This is part of the quantum-corrected and flux-quantized extended action functional of the [[supergravity C-field]] in [[11-dimensional supergravity]] by the analysis in ([FSSII](#FSSII)).



### Two-species cup-product theory on a $G_2$ manifold
 {#TwoSpeciesCupProductTheoryOnG2Manifold}

For $X$ a [[G2-manifold]] with characteristic [[differential forms]] 

$$
  \omega_3 \in \Omega^3(X)
$$ 

and 

$$
  \omega_4 = \star \omega_3\in \Omega^4(X)
$$

and for $G$ a simply connected compact [[semisimple Lie group]] with [[invariant polynomial]] $\langle -,-\rangle$, consider the [[action functional]] on the space of $\mathfrak{g}$-[[Lie algebra valued 1-forms]] $A$ given by the [[integration of differential forms]]

$$
  A 
    \mapsto 
  \exp\left(
    2 \pi i\int_{X} \omega_4 \wedge CS\left(A\right)
  \right)
  \,,
$$

where $CS(A) \in \Omega^3(X)$ is the [[Chern-Simons form]] of $A$. This, or some suitable globalization of this, has been considered as an [[action functional]] for 7-dimensional Chern-Simons-type theory in ([Donaldson-Thomas](#DonaldsonThomas)) and ([Baulieu-Losev-Nekrasov](#BaulieuLosevNekrasov)). This appears as an action functional in [[topological M-theory]] ([deBoer et al](#deBoerEtAl)).

To refine this to an [[extended Lagrangian]] and then fully globalize the action functional we can ask for a [[higher geometric quantization|higher geometric prequantization]] of $\omega_4$, regarded as a [[n-plectic structure|3-plectic structure]], by a [[prequantum n-bundle|prequantum 3-bundle]] $\hat \mathbf{G}_2$

$$
  \array{
   && \mathbf{B}^3 U(1)_{\mathrm{conn}}
   \\
   & {}^{\mathllap{\hat \mathbf{G}_2}}\nearrow & \downarrow^{\mathrlap{F_{(-)}}}
   \\
    X
   &\stackrel{\omega_4}{\to}&
   \Omega^4_{cl}
  }
  \,,
$$ 

where $\mathbf{B}^3 U(1)_{conn} \in $ [[Smooth∞Grpd]] is the smooth [[moduli ∞-stack]] of [[circle n-bundle with connection|circle 3-bundles with connection]]. 

If moreover we write

$$
  \hat \mathbf{c} \;:\;
  \mathbf{B}G_{conn}
  \to 
  \mathbf{B}^3 U(1)_{conn} 
$$

for the universal differential characteristic map which is the [[Lie integration]] of $\langle-,-\rangle$ (as discussed at _[[differential string structure]]_), hence the [[extended Lagrangian]] for ordinary [[3d Chern-Simons theory|3d]] $G$-[[Chern-Simons theory]], then an [[extended Lagrangian]] for the above [[action functional]] is given by the [[cup product in ordinary differential cohomology]]

$$
  \exp\left( 
   2 \pi i \int_{\Sigma_7} [\Sigma_7, \hat {\mathbf{G}}_4 \hat \cup \hat \mathbf{S}]
  \right)
  \;\colon\;
  X 
  \times
  \mathbf{B}G_{conn}
  \stackrel{(\hat \mathbf{G}_2, \hat \mathbf{c})}{\to}
  \mathbf{B}^3 U(1)_{conn}
  \times
  \mathbf{B}^3 U(1)_{conn}
  \stackrel{\hat \cup}{\to}
  \mathbf{B}^7 U(1)_{conn}
  \,.
$$

(This is an cup product extended Lagrangian of the kind considered in ([FSSIII](#FSSIII)).)


Notice that the prequantization lift to [[differential cohomology]] is entirely demanded by the interpretation of $\omega_4$ as the [[field strength]] of the [[supergravity C-field]] in interpretations of this setup in [[M-theory on G2-manifolds]].

Moreover, the above considerations do not really need $X$ to be a [[G2-manifold]] to go through, a manifold with [[weak G2 holonomy]] is just as well, hence equipped with $\phi \in \Omega^3(X)$ such that 

$$
  \omega_4 = \lambda \star \phi
$$

and

$$
 d \phi = \omega_4
 \,.
$$

This arises from [[Freund-Rubin compactifications]] with [[cosmological constant]] $\lambda$ ([Bilal-Derendinger-Sfetsos](#BilalDerendingerSfetsos)). 


## Related concepts

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[2d Chern-Simons theory]]

  * [[3d Chern-Simons theory]]

  * [[4d Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[6d Chern-Simons theory]]

  * **7d Chern-Simons theory**

  * [[AKSZ sigma-models]]

  * [[string field theory]]

  * [[infinite-dimensional Chern-Simons theory]]

* [[M-theory on G2-manifolds]], [[topological M-theory]]

* [[Hitchin functional]]


## References

### Abelian theory

The abelian 7d [[higher dimensional Chern-Simons theory]] of a [[circle n-bundle with connection|circle 3-bundle with connection]] was considered in 

* [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ J. Geom. Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 {#WittenI}

* [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 
 {#Witten98}

and argued to be the [[holographic principle|holographic dual]] to the [[self-dual higher gauge theory]] of an abelian 2-form connection on a _single_ [[M5-brane]] in its [[6d (2,0)-supersymmetric QFT]] on the worldvolume.

The precise formulation of this functional in terms of [[differential cohomology]] and [[integral Wu structure]] was given in 

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_
 {#HopkinsSinger}

### Nonabelian theories
 {#ReferencesNonabelianTheories}

In 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_
 {#FSSI}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field]]_ 
 {#FSSII}

the 7d Chern-Simons action obtained by [[Kaluza-Klein reduction|compactifying]] [[11-dimensional supergravity]] including the quantum corrections of the [[supergravity C-field]] on a 4-sphere (the [[AdS-CFT|AdS7/CFT6]] setup) is considered and refined to an [[extended Lagrangian]]. It contains the [Donaldson-Thomas](#DonaldsonThomas)-functional $\int_X CS(A) \wedge G_4$ as one summand and the [Witten](#WittenI)-functional as another.

Further discussion of [[extended Lagrangians]] for 7d CS theories is in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_
 {#FSSIII}




### On $G_2$-manifolds

The Chern-Simons type action functionals $A \mapsto \int_X CS(A) \wedge \omega_4$ on a 7d [[G2-manifold]] $(X, \omega_3)$ was first considered in 

* [[S. Donaldson]], [[R. Thomas]], _Gauge theory in higher dimensions_ ([pdf](http://www2.imperial.ac.uk/~rpwt/skd.pdf))
 {#DonaldsonThomas}

and around (3.23) of

* L. Baulieu, A. Losev, [[Nikita Nekrasov]], _Chern-Simons and Twisted Supersymmetry in Higher Dimensions_, Nucl.Phys. B522 (1998) 82-104 ([arXiv:hep-th/9707174](http://arxiv.org/abs/hep-th/9707174))
 {#BaulieuLosevNekrasov}



In 

* [[Jan de Boer]], Paul de Medeiros, Sheer El-Showk, Annamaria Sinkovics, _Open $G_2$ Strings_ ([arXiv:hep-th/0611080](http://arxiv.org/abs/hep-th/0611080))
 {#deBoerEtAl}

this is put into the context of [[topological M-theory]] (see around equation (2) in the introduction).


Discussion for [[weak G2-holonomy]] is in 

* A. Bilal, J.-P. Derendinger, K. Sfetsos, _(Weak) $G_2$ Holonomy from Self-duality, Flux and Supersymmetry_, Nucl.Phys. B628 (2002) 112-132 ([arXiv:hep-th/0111274](http://arxiv.org/abs/hep-th/0111274))
 {#BilalDerendingerSfetsos}


### Formulation in extended TQFT

Formulation in [[extended TQFT]] is discussed in

* [[Dan Freed]], _[[4-3-2 8-7-6]]_, talk at _[ASPECTS of Topology](https://people.maths.ox.ac.uk/tillmann/ASPECTS.html)_ Dec 2012




[[!redirects 7-dimensional Chern-Simons theory]]
[[!redirects 7d Chern-Simons theories]]
[[!redirects 7-dimensional Chern-Simons theories]]
