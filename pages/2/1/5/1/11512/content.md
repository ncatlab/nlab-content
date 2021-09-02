

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn} 
###### Definition

The [[profinite completion of a group|profinite completion]] of the [[integers]] is the [[inverse limit]]

$$
  \widehat{\mathbb{Z}} 
    \coloneqq 
  \underset{\leftarrow}{\lim}_{n \in \mathbb{N}} (\mathbb{Z}/n\mathbb{Z})
$$

of all the [[cyclic groups]] over their canonical [[filtered diagram]].

=--

+-- {: .num_prop #AsProductOverAlsoPAdicIntegers} 
###### Proposition

This is [[isomorphism|isomorphic]] to the [[product]] of the [[p-adic integers]] for all [[prime numbers]] $p$

$$
  \widehat{\mathbb{Z}} \simeq \underset{p\; prime}{\prod} \mathbb{Z}_p
  \,.
$$

=--

+-- {: .num_remark} 
###### Remark

From this perspective the concept of the [[ring of adeles]] is natural, see there for more.

=--

## Properties

### Pontryagin duality

Under [[Pontryagin duality]], $\hat \mathbb{Z}$ maps to $\mathbb{Q}/\mathbb{Z}$, see at _[[Pontryagin duality for torsion abelian groups]]_.

$$
  \array{
     &\mathbb{Z}[p^{-1}]/\mathbb{Z}
     &\hookrightarrow&
     \mathbb{Q}/\mathbb{Z}
     &\hookrightarrow&
     \mathbb{R}/\mathbb{Z}
     \\
     {}^{\mathllap{hom(-,\mathbb{R}/\mathbb{Z})}}\downarrow
     \\
     &\mathbb{Z}_p
     &\leftarrow&
     \hat \mathbb{Z}
     &\leftarrow&
     \mathbb{Z}
  }
$$

## Related concepts

* the [[modular group]]/[[general linear group]] with profinite integer coefficients $GL_2(\widehat{\mathbb{Z}})$ appears as the symmetry group in [[modular equivariant elliptic cohomology]].

## References

* {#Lenstra} [[Hendrik Lenstra]], example 2.2 in _Profinite groups_ ([pdf](http://websites.math.leidenuniv.nl/algebra/Lenstra-Profinite.pdf))
 
* [[Groupprops]], _[Profinite completion of the integers](http://groupprops.subwiki.org/wiki/Profinite_completion_of_the_integers)_


[[!redirects profinite integers]]