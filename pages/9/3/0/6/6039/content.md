
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

In the context of [[string theory]], the [[background gauge field]] for the [[open string]] [[sigma-model]] over a [[D-brane]] in [[bosonic string theory]] or [[type II string theory]] is a unitary [[principal bundle]] [[connection on a bundle|with connection]], or rather, by the Kapustin-part of the [[Freed-Witten-Kapustin anomaly cancellation]] mechanism, a [[twisted bundle|twisted unitary bundle]], whose twist is the restriction of the ambient [[B-field]] to the [[D-brane]]. 

The first hint for the existence of such [[background gauge fields]] for the [[open string]] 2d-[[sigma-model]] comes from the fact that the open string's endpoint can naturally be taken to carry labels $i \in \{1, \cdots n\}$. Further analysis then shows that the lowest excitations of these $(i,j)$-strings behave as the quanta of a $U(n)$-[[gauge field]], the $(i,j)$-excitation being the given [[matrix]] element of a $U(n)$-valued connection 1-form $A$.

This original argument goes back work by Chan and Paton. Accordingly one speaks of _Chan-Paton factors_ and _Chan-Paton bundles_ . 

## Definition

We discuss the Chan-Paton gauge field and its [[quantum anomaly cancellation]] in [[extended prequantum field theory]].

Throughout we write $\mathbf{H} = $ [[Smooth∞Grpd]] for the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoids]].

### The $B$-field as a prequantum 2-bundle

For $X$ a [[type II supergravity]] [[spacetime]], the [[B-field]] is a map

$$
  \nabla_B \;\colon\; X \to \mathbf{B}^2 U(1)
  \,.
$$

If $X = G$ is a [[Lie group]], this is the [[prequantum 2-bundle]] of $G$-[[Chern-Simons theory]]. Viewed as such we are to find a canonical [[∞-action]] of the [[circle 2-group]] $\mathbf{B}U(1)$ on some $V \in \mathbf{H}$, form the corresponding [[associated ∞-bundle]] and regard the [[sections]] of that as the [[prequantum 2-states]] of the theory.

The Chan-Paton gauge field is such a prequantum 2-state.

### The Chan-Paton gauge field

We discuss the [[Chan-Paton gauge fields]] over [[D-branes]]
in [[bosonic string theory]] and over $Spin^c$-D-branes in [[type II string theory]].

We fix throughout a natural number $n \in \mathbb{N}$, the _[[rank]]_ of the Chan-Paton gauge field.

+-- {: .num_prop #TheLongSequenceOfTheProjectiveUnitaryExtension}
###### Proposition

The [[extension of groups|extension]] of [[Lie groups]]  

$$
  U(1) \to U(n) \to PU(n)
$$ 

exhibiting the [[unitary group]] as a [[circle group]]-extension of the [[projective unitary group]] sits in a long [[homotopy fiber sequence]] of [[smooth ∞-groupoids]] of the form

$$
  U(1) \to U(n) \to PU(n) \to \mathbf{B}U(1)
  \to \mathbf{B}U(n) \to \mathbf{B}PU(n) \stackrel{\mathbf{dd}_n}{\to}
  \mathbf{B}^2 U(1)
  \,,
$$

where for $G$ a [[Lie group]] $\mathbf{B}G$ is its [[delooping]] [[Lie groupoid]], hence the [[moduli stack]] of $G$-[[principal bundles]], and where similarly $\mathbf{B}^2 U(1)$ is the [[moduli ∞-stack|moduli 2-stack]] of [[circle 2-group]] [[principal 2-bundles]] ([[bundle gerbes]]).

=--

+-- {: .num_prop}
###### Proposition

Here 

$$
  \mathbf{dd}_n \;\colon\; \mathbf{B} PU(n) \to \mathbf{B}^2 U(1)
$$

is a smooth refinement of the universal [[Dixmier-Douady class]]

$$
  dd_n \;\colon\; B PU(n) \to K(\mathbb{Z}, 3)
$$

in that under [[geometric realization of cohesive ∞-groupoids]] ${\vert- \vert} \colon$ [[Smooth∞Grpd]] $\to$ [[∞Grpd]] we have

$$
  {\vert \mathbf{dd}_n \vert}
  \simeq
  dd_n
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

By the discussion at _[[∞-action]]_ the [[homotopy fiber sequence]] in prop. \ref{TheLongSequenceOfTheProjectiveUnitaryExtension}

$$
  \array{
    \mathbf{B} U(n)
    &\to&
    \mathbf{B} PU(n)
    \\
    && \downarrow
    \\
    && \mathbf{B}^2 U(1)
  }
$$

in $\mathbf{H}$
exhibits a smooth[[∞-action]] of the [[circle 2-group]] on the [[moduli stack]] $\mathbf{B}U(n)$ and it exhibits an equivalence

$$
  \mathbf{B} PU(n) \simeq (\mathbf{B}U(n))//(\mathbf{B} U(1))
$$

of the moduli stack of projective unitary bundles with the [[∞-quotient]] of this [[∞-action]].

=--

+-- {: .num_prop }
###### Proposition

For $X \in \mathbf{H}$ a [[smooth manifold]] and $\mathbf{c} \;\colon\; X \to \mathbf{B}^2 U(1)$ modulating a [[circle 2-group]]-[[principal 2-bundle]], maps

$$
  \mathbf{c} \to \mathbf{dd}_n
$$

in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}^2 U(1)}$, hence [[diagrams]] of the form

$$
  \array{
    X &&\stackrel{}{\to}&& \mathbf{B} PU(n)
    \\
    & {}_{\mathllap{\mathbf{c}}}\searrow 
    &\swArrow& 
    \swarrow_{\mathrlap{\mathbf{dd}_n}}
    \\
    && \mathbf{B}^2 U(1)
  }
$$

in $\mathbf{H}$ are equivalently rank-$n$ unitary [[twisted bundles]] on $X$, with the twist being the class $[\mathbf{c}] \in H^3(X, \mathbb{Z})$.

=--

+-- {: .num_prop #DifferentialRefinementOfSMoothDDClass}
###### Proposition

There is a further differential refinement

$$
  \array{
     (\mathbf{B}U(n))//(\mathbf{B}U(1))_{conn}
     &\stackrel{\widehat \mathbf{dd}_n}{\to}&
     \mathbf{B}^2 U(1)_{conn}
     \\
     \downarrow && \downarrow
     \\
     (\mathbf{B}U(n))//(\mathbf{B}U(1))
     &\stackrel{\widehat \mathbf{dd}_n}{\to}&
     \mathbf{B}^2 U(1)
  }
  \,,
$$

where $\mathbf{B}^2 U(1)_{conn}$ is the universal moduli 2-stack of [[circle n-bundle with connection|circle 2-bundles with connection]] ([[bundle gerbes]] with connection).

=--


+-- {: .num_defn}
###### Definition

Write

$$
  \left(
  \left(\mathbf{B}U\left(n\right)//\mathbf{B}U\left(1\right)\right)_{conn}
   \stackrel{\mathbf{Fields}}{\to} 
  \mathbf{B}^2 U\left(1\right)_{conn}
  \right)
  \;\;
  \in \mathbf{H}_{/\mathbf{B}^2 U(1)_{conn}}
$$

for the differential smooth universal Dixmier-Douady class of prop. \ref{DifferentialRefinementOfSMoothDDClass}, regarded as an object in the [[slice (∞,1)-topos]] over $\mathbf{B}^2 U(1)_{conn}$.

=--

+-- {: .num_defn}
###### Definition

Let 

$$
  \iota_X   
    \;\colon\;
  Q \hookrightarrow X 
$$

be an inclusion of [[smooth manifolds]] or of [[orbifolds]], to be thought of as a [[D-brane]] [[worldvolume]] $Q$ inside an ambient [[spacetime]] $X$.

Then a **field configuration** of a _[[B-field]]_ on $X$ together with a compatible rank-$n$ **Chan-Paton gauge field** on the [[D-brane]] is a map

$$
  \phi 
   \;\colon\;
  \iota_X \to \mathbf{Fields}
$$

in the [[arrow (∞,1)-topos]] $\mathbf{H}^{(\Delta^1)}$, hence a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    Q &\stackrel{\nabla_{gauge}}{\to}& (\mathbf{B}U(n)//\mathbf{B}U(1))
    \\
    {}^{\iota_X}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\hat \mathbf{dd}_n}}
    \\
    X &\stackrel{\nabla_B}{\to}& \mathbf{B}^2 U(1)_{conn}
  }
$$

=--

This identifies a  [[twisted bundle]] with connection on the D-brane whose twist is the class in $H^3(X, \mathbb{Z})$ of the bulk [[B-field]]. 

This relation is the Kapustin-part of the [[Freed-Witten-Kapustin anomaly]] cancellation for the [[bosonic string]] or else for the [[type II string]] on $Spin^c$ D-branes. ([FSS](#FSS))


+-- {: .num_remark }
###### Remark

If we regard the [[B-field]] as a [[background field]] for the [[Chan-Paton gauge field]], then remark \ref{PullbackAlongGeneralizedLocalDiffeomorphisms} determines along which maps of the B-field the Chan-Paton gauge field may be transformed. 

$$
  \array{
    Y &\stackrel{}{\to}& X &\stackrel{}{\to}& (\mathbf{B}U(n)//\mathbf{B}U(1))_{conn}
    \\
    & \searrow & \downarrow & \swarrow
    \\
    &&\mathbf{B}^2 U(1)_{conn}
  }
  \,.
$$

On the local connection forms this acts as

$$
  A \mapsto A + \alpha
  \,.
$$

$$
  B \mapsto B + d \alpha
$$

This is the famous gauge transformation law known from the string theory literature.

=--

### The open string sigma-model

+-- {: .num_remark}
###### Remark

The [[D-brane]] inclusion $Q \stackrel{\iota_X}{\to} X$ is the [[target space]] for an [[open string]] with [[worldsheet]] $\partial \Sigma \stackrel{\iota_\Sigma}{\hookrightarrow} \Sigma$: a [[field (physics)|field]] configuration of the open string [[sigma-model]] is a map

$$
  \phi \;\colon\; \iota_\Sigma \to \iota_X
$$

in $\mathbf{H}^{\Delta^1}$, hence a [[diagram]] of the form

$$
  \array{
    \partial \Sigma &\stackrel{\phi_{bdr}}{\to}& Q
    \\
    \downarrow^{\mathrlap{\iota_\Sigma}} 
     &\swArrow& 
    \downarrow^{\mathrlap{\iota_X}}
    \\
    \Sigma &\stackrel{\phi_{bulk}}{\to}& X
  }
  \,.
$$

For $X$ and $Q$ ordinary [[manifolds]] just says that a field configuration is a map $\phi_{bulk} \;\colon\; \Sigma \to X$ subject to the constraint that it takes the [[boundary]] of $\Sigma$ to $Q$. This means that this is a [[trajectory]] of an [[open string]] in $X$ whose endpoints are constrained to sit on the [[D-brane]] $Q \hookrightarrow X$.

If however $X$ is more generally an [[orbifold]], then the [[homotopy]] filling the above diagram imposes this constraint only up to orbifold transformations, hence exhibits what in the physics literature are called "orbifold twisted sectors" of open string configurations.

=--

+-- {: .num_prop #TheTypeIIOpenStringSigmaModelModuliStackOfFields}
###### Proposition

The [[moduli stack]] $[\iota_\Sigma, \iota_X]$ of such field configurations is the [[homotopy pullback]] 

$$
  \array{
    [\iota_{\Sigma}, \iota_X]
    &\to&
    [\Sigma, X]
    \\
    \downarrow &\swArrow& \downarrow
    \\
    [S^1, Q]
    &\to&
    [S^1, X]
  }
  \,.
$$

=--

### The anomaly-free open string coupling to the Chan-Paton gauge field

+-- {: .num_prop }
###### Proposition

For $\Sigma$ a [[smooth manifold]] with [[boundary]] $\partial \Sigma$ of [[dimension]] $n$ and for $\nabla \;\colon \; X \to \mathbf{B}^n U(1)_{conn}$ a [[circle n-bundle with connection]] on some $X \in \mathbf{H}$, then the [[transgression]] of $\nabla$ to the [[mapping space]] $[\Sigma, X]$ yields a [[section]] of the [[complex line bundle]] [[associated bundle|associated]] to the pullback of the ordinary transgression over the mapping space out of the boundary: we have a diagram

$$  
  \array{  
    [\Sigma, X]
      &\stackrel{\exp(2 \pi i \int_{\Sigma})}{\to}& 
    \mathbb{C}//U(1)_{conn}
    \\
    \downarrow^{\mathrlap{[\partial \Sigma, X]}} 
    && 
    \downarrow^{\mathrlap{\overline{\rho}}_{conn}}
    \\
    [\partial \Sigma, X]
    &\stackrel{\exp(2 \pi i \int_{\partial \Sigma})}{\to}&
    \mathbf{B} U(1)_{conn}
  }
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

This is the _[[higher parallel transport]]_ of the $n$-connection $\nabla$ over maps $\Sigma \to X$.

=--


+-- {: .num_prop #TheTwistedHolonomyMapOnTwistedUnitaryBundles}
###### Proposition

The operation of forming the [[holonomy]] of a twisted unitary connection around a curve fits into a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    [S^1, (\mathbf{B}U(n))//(\mathbf{B}U(1))_{conn}]
    &\stackrel{hol_{S^1}}{\to}&
    \mathbb{C}//U(1)_{conn}
    \\
    \downarrow^{\mathrlap{[S^1, \widehat\mathbf{dd}_n]}} 
     &\swArrow_{\simeq}& 
    \downarrow^{\mathrlap{\overline{\rho}_{conn}}}
    \\
    [S^1, \mathbf{B}^2 U(1)_{conn}]
    &\stackrel{\exp(2 \pi i \int_{S^1})}{\to}&
    \mathbf{B}U(1)_{conn}
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

By the discussion at _[[∞-action]]_ the diagram in prop. \ref{TheTwistedHolonomyMapOnTwistedUnitaryBundles} says in particular that forming traced [[holonomy]] of twisted unitary bundles constitutes a [[section]] of the [[complex line bundle]] on the [[moduli stack]] of twisted unitary connection on the circle which is the [[associated bundle]] to the [[transgression]] $\exp(2 \pi i \int_{S^1} [S^1, \widehat\mathbf{dd}_n])$ of the universal differential [[Dixmier-Douady class]]. 

=--


It follows that on the moduli space of the open string [[sigma-model]] of prop. \ref{TheTypeIIOpenStringSigmaModelModuliStackOfFields} above there are two $\mathbb{C}//U(1)$-valued [[action functionals]] coming from the bulk field and the boundary field

$$
  \array{
    [\iota_{\Sigma}, \iota_X]
    &\to&
    [\Sigma, X]
    &\stackrel{exp(2 \pi i \int_{\Sigma}[\Sigma, \nabla_B]  ) }{\to}&
    \mathbb{C}//U(1)_{conn}
    \\
    \downarrow &\swArrow& \downarrow
    \\
    [S^1, Q]
    &\to&
    [S^1, X]
    \\
    \downarrow^{\mathrlap{hol_{S^1}([S^1, \nabla_{gauge}])}}
    \\
    \mathbb{C}//U(1)_{conn}
  }
  \,.
$$

Neither is a well-defined $\mathbb{C}$-valued function by itself. But by [[pasting]] the above diagrams, we see that both these constitute [[sections]] of the same [[complex line bundle]] on the moduli stack of fields:

$$
  \array{
    [\iota_{\Sigma}, \iota_X]
    &\to&
    [\Sigma, X]
    &\stackrel{[\Sigma, \nabla_B]}{\to}&
    [S^1, \mathbf{B}^2 U(1)_{conn}]
    &\stackrel{\exp(2 \pi i \int_{\Sigma})}{\to}&
    \mathbb{C}//U(1)_{conn}
    \\
    \downarrow &\swArrow& \downarrow
    && && \downarrow
    \\
    [S^1, Q]
    &\to&
    [S^1, X]
    \\
    \downarrow^{\mathrlap{[S^1, \nabla_{gauge}]}} &&  & \searrow^{\mathrlap{[S^1, \nabla_B]}}
    & && \downarrow
    \\
    [S^1, (\mathbf{B}U(n))//(\mathbf{B}U(1))_{conn}] & &\stackrel{[S^1, \widehat \mathbf{dd}_n]}{\to}& & [S^1, \mathbf{B}^2 U(1)_{conn}]
    \\
    \downarrow^{\mathrlap{hol_{S^1}}} 
      && && &  \searrow^{\mathrlap{\exp(2 \pi i \int_{S^1}(-))}}
    \\
    \mathbb{C}//U(1)_{conn} &\to& &\to& &\to&  \mathbf{B}U(1)_{conn}
  }
  \,.
$$

Therefore the product action functional is a well-defined function

$$
  [\iota_\Sigma, \iota_X]
  \stackrel{
    \exp(2 \pi i \int_{\Sigma} [\Sigma, \nabla_b] )
    \cdot
    hol_{S^1}( [S^1, \widehat {\mathbf{dd}}_n] )^{-1}
  }{\to}
  U(1)
  \,.
$$

This is the [[Freed-Witten-Kapustin anomaly|Kapustin anomaly]]-free [[action functional]] of the [[open string]].


## Related concepts

* [[B-field]]

* [[twisted K-theory]]

* [[Freed-Witten anomaly cancellation]]

* [[Dirac-Born-Infeld action]]

## References

In the traditional physicist's string theory introductions one finds Chan-Paton bundles discussed for instance 


* [[Clifford Johnson]], section 2.4 of _D-Brane primer_ ([arXiv:hep-th/0007170](http://arxiv.org/abs/hep-th/0007170))


* David Tong, around p. 66 of _Lectures on string theory_ ([arxiv/0908.0333](http://front.math.ucdavis.edu/0908.0333))

These lectures tend to ignore most of the global subtleties though. For traditional discussion of the  _[[Freed-Witten-Kapustin anomaly]]_, see there. The above account in terms of [[higher geometry]] and [[extended prequantum field theory]] is due to  section 5.4 of

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_ .

Lecture notes along these lines are at

* _[[geometry of physics]]_ 

Discussion of the derivation of the  [[Yang-Mills theory]] on the D-brane from open [[string scattering amplitudes]]/[[string field theory]] includes

* [[David Gross]], [[Edward Witten]], _Superstring modifications of Einstein's equations_,  Nuclear Physics B Volume 277, 1986, Pages 1-10

and for the non-abelian case:

* Semyon Klevtsov, _Yang-Mills theory from String field theory on D-branes_ ([pdf](http://www.mi.uni-koeln.de/~klevtsov/cargese02.pdf))



[[!redirects Chan-Paton bundles]]

[[!redirects Chan-Paton vector bundle]]
[[!redirects Chan-Paton vector bundles]]

[[!redirects Chan-Paton gauge field]]
[[!redirects Chan-Paton gauge fields]]

[[!redirects Chan-Paton gauge bundle]]
[[!redirects Chan-Paton gauge bundles]]
