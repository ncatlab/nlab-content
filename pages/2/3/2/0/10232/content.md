

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given a [[bundle]] $E \overset{}{\to} \Sigma$, then its _space of [[sections]]_ is like a [[mapping space]], but relative to the base space $\Sigma$. 

Formally this is given by the _[[dependent product]]_ construction. See at _[section -- In terms of dependent product](section#InTermsOfDependentProduct)_ and at _[dependent product -- In terms of spaces of sections](dependent%20product#RelationToSpacesOfSections)_.

## Definition

Let $\mathbf{H}$ be a [[topos]] (for instance $\mathbf{H} =$[[SmoothSet]]) or [[(∞,1)-topos]] (for instance $\mathbf{H} = $ [[Smooth∞Grpd]]) and consider 

$$
  \left[
    \,\,
    \array{
       E 
       \\
       {}^{\mathllap{p}}\downarrow
       \\
       \Sigma
    }
  \right]
  \;\colon\;
  \mathbf{H}_{/\Sigma}
$$

a [[bundle]] in $\mathbf{H}$, regarded as an object in the [[slice topos]]/[[slice (∞,1)-topos]].

Then the _space of sections_ $\Gamma_\Sigma(E)$ of this bundle is the [[dependent product]]

$$
  \Gamma_\Sigma E 
    \coloneqq 
  \prod_{\Sigma} E
  \;\in\; \mathbf{H}
$$

hence the image of the bundle under the [[right adjoint]] $\Sigma_\ast$ in the [[base change]] [[adjoint triple]]

$$
  \mathbf{H}_{/\Sigma} 
    \underoverset
      {\underset{\Sigma_\ast}{\longrightarrow}}
      {\overset{\Sigma_!}{\longrightarrow}}
      {\overset{\Sigma^\ast}{\longleftarrow}}
  \mathbf{H}
  ,.
$$

By [[adjunction]] this means that for $U \in \mathbf{H}$ a test object, then a $U$-parameterized family of sections of $E$, hence a morphism in $\mathbf{H}$ of the form

$$
  U \longrightarrow \Gamma_\Sigma(E)
$$

is equivalently a morphism in $\mathbf{H}_{/\Sigma}$ of the form

$$
  \Sigma \times U = \Sigma^\ast U \longrightarrow E
  \,.
$$

This is equivalently a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    && E
    \\
    & {}^{\mathllap{\phi_U}}\nearrow & \downarrow^{\mathrlap{p}}
    \\
    U \times \Sigma
    &\underset{pr_2}{\longrightarrow}&
    \Sigma
  }
  \,,
$$

where the right and bottom morphisms are fixed, and where $\phi_U$ (and  the [[2-cell]] filling the diagram) is, manifestly, the $U$-parameterized family of [[sections]].

## Properties

### Topological vector space structure


+-- {: .num_defn #TVSStructureOnSpacesOfSmoothSections}
###### Definition
**([[Fréchet space|Fréchet]] [[topological vector space]] on spaces of smooth sections of a [[smooth vector bundle]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]]. On its [[real vector space]] $\Gamma_\Sigma(E)$ [[space of sections|of smooth sections]] consider the [[seminorms]] indexed by a [[compact subset]] $K \subset \Sigma$ and a [[natural number]] $N \in \mathbb{N}$ and given by

$$
  \array{
    \Gamma_\Sigma(E) &\overset{p_K^N}{\longrightarrow}&
    [0,\infty)
    \\
    \Phi &\mapsto&  \underset{n \leq N}{max} \left( \underset{x \in K}{sup} {\vert \nabla^n \Phi(x)\vert}\right) \,,
  }
$$

where on the right we have the [[absolute values]] of the [[covariant derivatives]] of $\Phi$ for any fixed choice of [[connection on a bundle|connection]] on $E$ and [[norm]] on the [[tensor product of vector bundles]] $(T^\ast \Sigma)^{\otimes_\Sigma^n} \otimes_\Sigma E $.

This makes $\Gamma_\Sigma(E)$ a [[Fréchet space|Fréchet]] [[topological vector space]].

For $K \subset \Sigma$ any [[closed subset]] then the sub-space of sections

$$
  \Gamma_{\Sigma,K}(E) \hookrightarrow \Gamma_\Sigma(E)
$$ 

of sections whose [[support]] is inside $K$ becomes a [[Fréchet space|Fréchet]] [[topological vector spaces]] with the induced [[subspace topology]], which makes these be [[closed subspaces]].

=--

([B&#228;r 14, 2.1, 2.2](#Baer14))


## Examples

* The space of section of an universal [[associated infinity-bundle]] is the space of [[homotopy coinvariants]] of the corresponding [[infinity-action]] (see there for more).

## Related concepts

* [[dependent product]]

* [[twisted cohomology]]

* [[space of states (in geometric quantization)]]

## References

The [[topological vector space]] on spaces of smooth sections is discussed in

* {#BrunettiFredenhagenRibeiro12} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Pedro Ribeiro]], around remark 2.2.1 in _Algebraic Structure of Classical Field Theory I: Kinematics and Linearized Dynamics for Real Scalar Fields_ ([arXiv:1209.2148](https://arxiv.org/abs/1209.2148), [spire](http://inspirehep.net/record/1185123/))

* {#Baer14} [[Christian Bär]], _Green-hyperbolic operators on globally hyperbolic spacetimes_, Communications in Mathematical Physics 333, 1585-1615 (2014) ([doi](http://dx.doi.org/10.1007/s00220-014-2097-7), [arXiv:1310.0738](https://arxiv.org/abs/1310.0738))


[[!redirects spaces of sections]]

[[!redirects space of smooth sections]]
[[!redirects spaces of smooth sections]]


[[!redirects ∞-groupoid of sections]]
[[!redirects ∞-groupoids of sections]]
[[!redirects infinity-groupoid of sections]]
[[!redirects infinity-groupoids of sections]]