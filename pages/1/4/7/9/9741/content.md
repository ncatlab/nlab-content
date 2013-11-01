
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[moduli space]] of ([[flat connection|flat]]) [[connections on bundles]] over some prescribed [[space]].

## Properties

### Compactness

If $\Sigma$ is a [[compact topological space|compact]] [[smooth manifold]], then the moduli psace of flat connections over $\Sigma$ is compact. 

### Complex structure

 The _[[Narasimhan–Seshadri theorem]]_ identifies [[moduli spaces of flat connections]] over a [[Riemann surface]] with that of certain [[complex manifold|complex]] spaces of [[stable vector bundles]].  This space appears as the [[phase space]] for [[Chern-Simons theory]] over that surface. See there for more.

## Examples

### Flat connections over a torus
  {#FlatConnectionsOverATorus}

Let $G$ be a [[compact Lie group]].

The moduli space of $G$ [[flat connections]] on a 2-dimensional [[torus]] $A \simeq S^1 \times S^1$ (e.g. underlying a complex [[elliptic curve]]) has the following description:

first, the [[moduli stack]] of flat connections is

$$
  [\Pi(A), \mathbf{B}G] \simeq Hom_{Grp}(\mathbb{Z} \times \mathbb{Z}, G)//_{ad} G
$$

Here a single flat connection is just a choice of pair of of two commuting elements in $G$, and $G$ acts on that by [[conjugation]]. Now any two commuting elements can be taken to sit in a [[maximal torus]] $T \hookrightarrow G$, and up to [[conjugation]] we can take this to be one fixed maximal torus. This means that the moduli space is actually

$$
  \pi_0 \left(
    Hom_{Grp}(\mathbb{Z} \times \mathbb{Z}, G)//_{ad} G
  \right)
  \simeq
  Hom_{Grp}(\mathbb{Z} \times \mathbb{Z}, T)/W
  \,,
$$

where $W$ is the [[Weyl group]] $W = N_G(T)/T$. 

Moreover, by [[Pontryagin duality]] this may be re-expressed as

$$
  \cdots \simeq Hom_{Grp}([T,S^1], A)/W
  \,.
$$

where $[T,S^1]$ is the [[character group]] of the maximal torus.

In this form the moduli space of flat connections appears prominently for instance in the discussion of [[equivariant elliptic cohomology]].


## Related concepts

* [[Tamagawa numbers]]

## References

* [[Michael Atiyah]], [[Raoul Bott]], _The Yang-Mills equations over Riemann surfaces_ ([jstor](http://www.jstor.org/stable/37156), [lighning summary](http://math.stackexchange.com/a/295505/58526))

* _Moduli space of connections on a Riemann surface_ ([pdf](http://www.mat.ucm.es/~vmunozve/Moduli.pdf&#8206;))

For more references see at _[[Hitchin connection]]_.

[[!redirects moduli spaces of connections]]

[[!redirects moduli space of flat connections]]
[[!redirects moduli spaces of flat connections]]