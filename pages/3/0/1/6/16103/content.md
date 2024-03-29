
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a [[symplectic vector space]] $(V,\omega)$, then its _affine symplectic group_ $ASp(V,\omega)$ (or _inhomogeneous sympelctic group_ $ISp(V,\omega)$) is equivalently

* the [[intersection]] $ASp(V,\omega) = Aff(V)\times_{Diff(V)} Sympl(X,\omega)$ of the [[affine group]] of the [[affine space]] $V$ and the [[symplectomorphism group]] of the [[symplectic manifold]] $(X,\omega)$, i.e.the  [[group]] of all those [[affine transformations]] which preserve the [[symplectic form]] $\omega$;

* the [[semidirect product]] $ASp(V,\omega) = V \rtimes Sp(V,\omega)$ of the [[symplectic group]] acting on $V$ regarded as the [[translation group]] over itself.

The further restriction to [[linear functions]] gives the [[symplectic group]] proper. 

## Properties

### Extensions

There is a [[circle group|circle]] [[group extension]] $ESp(V,\omega)$ of the affine symplectic group -- the _[[extended affine symplectic group]]_ -- given by restricting the [[quantomorphism group]] of $(V,\omega)$ to affine transformations. The further restriction of that to elements coming from [[translation group|translations]] is the [[Heisenberg group]]  $Heis(V,\omega)$.

$$
  \array{
     Heis(V,\omega)
     &\hookrightarrow&
     ESp(V,\omega) &\hookrightarrow& QuantMorph(V,\omega)
     \\
     \downarrow && \downarrow && \downarrow
     \\
     V
     &\hookrightarrow&
     ASp(V,\omega)
     &\hookrightarrow&
     HamSympl(V,\omega)
  }
$$

## Related concepts

* [[Poincare group]]

## References

Review includes

* {#Low12} Stephen G. Low, section 1 of _Maximal quantum mechanical symmetry: Projective representations of the inhomogenous symplectic group_, J. Math. Phys. 55, 022105 (2014) ([arXiv:1207.6787](http://arxiv.org/abs/1207.6787))


[[!redirects affine symplectic groups]]
