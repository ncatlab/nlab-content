

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

A space of [[sections]] is like a [[mapping space]], but relative to a base. 

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
  \mathbb{B}
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
    & {}^{\mathllap{\sigma}}\nearrow & \downarrow^{\mathrlap{p}}
    \\
    U \times \Sigma
    &\underset{pr_2}{\longrightarrow}&
    \Sigma
  }
  \,,
$$

where the right and bottom morphisms are fixed, and where $\phi_U$ (and  the [[2-cell]] filling the diagram) is, manifestly, the $U$-parameterized family of [[sections]].


## Examples

* The space of section of an universal [[associated infinity-bundle]] is the space of [[homotopy coinvariants]] of the corresponding [[infinity-action]] (see there for more).

## Related concepts

* [[dependent product]]

* [[twisted cohomology]]

## References

Discussion of spaces of smooth sections is in

* {#BrunettiFredenhagenRibeiro12} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Pedro Ribeiro]], around remark 2.2.1 in _Algebraic Structure of Classical Field Theory I: Kinematics and Linearized Dynamics for Real Scalar Fields_ ([arXiv:1209.2148](https://arxiv.org/abs/1209.2148), [spire](http://inspirehep.net/record/1185123/))

[[!redirects spaces of sections]]

[[!redirects space of smooth sections]]
[[!redirects spaces of smooth sections]]


[[!redirects ∞-groupoid of sections]]
[[!redirects ∞-groupoids of sections]]
[[!redirects infinity-groupoid of sections]]
[[!redirects infinity-groupoids of sections]]