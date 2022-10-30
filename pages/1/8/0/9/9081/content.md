

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _extended Lagrangian_ is the notion of [[Lagrangian]] refined to [[extended quantum field theory]] (or "localized" or "multi-tiered" quantum field theory). At the same time is is the [[prequantum n-bundle]] of the theory in its [[higher geometric quantization]] in top codimension, hence over the point.

## Definition

Let $\mathbf{H}$ be an ambient [[(∞,1)-topos]], typically a [[cohesive (∞,1)-topos]] such as [[Smooth∞Grpd]] or one of its [[slice (∞,1)-topos|slices]]. For $n \in \mathbb{N}$ let $\mathbf{B}^n U(1)_{conn} \in \mathbf{H}$ be the [[moduli ∞-stack]] of [[circle n-bundles with connection]]. Let moreover $\mathbf{Fields} \in \mathbf{H}$ be the given [[moduli ∞-stack]] of field configurations, so tha for $\Sigma$ some [[worldvolume]] [[manifold]] a field configuration on $\Sigma$ is a map in $\mathbf{H}$ of the form

$$
  \phi \colon \Sigma \to \mathbf{Fields}
$$

a [[gauge transformation]] $\phi \Rightarrow \phi'$ is a [[homotopy]] between two such maps, and a [[higher gauge transformation]] is a higher homotopy.

Then an **extended Lagrangian** or [[prequantum n-bundle]] for an $n$-dimensional [[quantum field theory]] with fields classified by $\mathbf{Fields}$ is a map in $\mathbf{H}$ of the form

$$
  \mathbf{L}
  \;\colon\;
  \mathbf{Fields}
  \to 
  \mathbf{B}^n U(1)_{conn}
  \,.
$$

By post-[[composition]] this sends a field $\pho \colon \Sigma_n \to \mathbf{Fields}$ to the [[circle n-bundle with connection]] on $\Sigma_n$ modulated by

$$
  \mathbf{L}(\phi)
  \;\colon\;
  \Sigma_n 
  \stackrel{\phi}{\to}
  \mathbf{Fields}
  \stackrel{\mathbf{L}}{\to}
  \mathbf{B}^n U(1)_{conn}
  \,.
$$

This is locally  -- restricted to some [[good cover]] $U \to \Sigma_n$ of $\Sigma_b$) given by a [[differential n-form]] 

$$
  L(\phi) \omega \in \Omega^n(U)
  \,,
$$

where $L(\phi) \in C^\infty(U)$ is a [[smooth function]] and where $\omega \in \Omega^n(U)$ is some [[volume form]] or some other prespecified [[measure]]. This function $L(\phi)$ is the ordinary [[Lagrangian]]. 

Over an [[orientation|oriented]] [[closed manifold]] $\Sigma_n$ of [[dimension]] $n$ the corresponding [[action functional]] is the [[transgression]] of $\mathbf{L}$ to the mapping stack/[[internal hom]] out of $\Sigma_n$, hence the composite

$$
  \exp\left(
    2\pi i \int_{\Sigma_n} [\Sigma_n, \mathbf{L}]
  \right)
  \;\colon\;
  [\Sigma_n, \mathbf{Fields}]
  \stackrel{[\Sigma_n, \mathbf{L}]}{\to}
  [\Sigma_n, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi in \int_{\Sigma_n})(-) }{\to}
  U(1)
  \,,
$$

where the first map is the [[internal hom]] on morphisms and the second is the [[higher holonomy]] map of a [[circle n-bundle with connection]] over $\Sigma_n$, hence the [[fiber integration in ordinary differential cohomology]]. 

For $\phi : \Sigma_n \to \mathbf{Fields}$ a field such that the [[circle n-group|circle (n-1)-group]] [[principal ∞-bundle]] underlying $\mathbf{L}(\phi)$ is trivializable and trivialized, the differential form $L(\phi)\omega$ discussed above descends to $X$ itself and the [[action functional]] is simply the [[integration of differential forms]]

$$
  \phi \mapsto \exp\left(2 \pi i \int_{\Sigma_n} L(\phi) \omega \right)
  \,.
$$

This special case is the relation between [[Lagrangians]] and [[action functionals]] as traditionally considered.

Generally, for $0 \leq k \leq n$ and $\Sigma_{k}$ an oriented [[closed manifold]] of [[dimension]] $k$, transgression as above yields a map in $\mathbf{H}$ of the form

$$
  \exp\left(
    2\pi i \int_{\Sigma_k} [\Sigma_n, \mathbf{L}]
  \right)
  \;\colon\;
  [\Sigma_k, \mathbf{Fields}]
  \stackrel{[\Sigma_n, \mathbf{L}]}{\to}
  [\Sigma_l, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi in \int_{\Sigma_k})(-) }{\to}
  \mathbf{B}^{n-k}U(1)
$$

which modulates a [[circle n-bundle with connection|circle (n-k)-bundle with connection]] on the [[moduli infinity-stack]] of fields on $\Sigma_k$. At least for large classes of theories, this is the (off-shell) [[prequantum n-bundle|prequantum (n-k)-bundle]] of the theory.

## Examples

### Higher gauge theory

If $G \in Grp(\mathbf{H})$ is an [[∞-group]] (a [[smooth ∞-group]] if $\mathbf{H}$ is [[Smooth∞Grpd]]) and 

$$
  \mathbf{Fields}  
  \simeq
  \mathbf{B}G_{conn}
$$

is a [[moduli ∞-stack]] of $G$-[[principal ∞-bundle|principal]] [[connection on an ∞-bundle|∞-connections]], then the theory in question is a ([[higher gauge theory|higher]]) [[gauge theory]]. In this case the map

$$
  \mathbf{c} \;\colon\; \mathbf{B}G \to \mathbf{B}^n U(1)
$$

underlying the extended Lagrangian is a [[cocycle]] that induces an [[extension of ∞-groups]], fitting a [[homotopy fiber sequence]]

$$
  \mathbf{B}^{n-1}U(1) \to \mathbf{B}\hat G
\stackrel{}{\to} \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^n U(1)
  \,.
$$

In this case the extended Lagrangian also plays the role as the universal differential refinement of the [[obstruction]] class to [[lift of structure groups]] through $\hat G \to G$. More generally, its [[homotopy fiber products]] are [[moduli ∞-stacks]] of [[twisted differential c-structures]]. See there for more examples.

### Higher Chern-Simons theory

Various examples are discussed at 

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[AKSZ sigma-models]]

  * [[string field theory]]

  * [[infinite-dimensional Chern-Simons theory]]

## Related concepts

[[!include extended prequantum field theory - table]]
  


## References

Expositions, examples and further pointers are in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_

Lecture notes are in _[[geometry of physics]]_, and section 1.2 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

A general abstract discussion is in section 3 there, further discussion of examples in section 5.



[[!redirects extended Lagrangians]]

