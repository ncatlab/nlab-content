
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


# Derived elliptic curve#
* table of contents
{:toc}

## Idea ##

A _derived elliptic curve_ is an object in [[higher geometry]] that is to an [[E-∞ ring]] as an ordinary [[elliptic curve]] is to an ordinary [[ring]].

## Definition ##

For the notation and terminology of the following definition, see (for the time being)


Let $A$ be an [[E-∞ ring]]. A **derived elliptic curve** over $A$ is [[derived group scheme]] $E \to Spec A$ with the property that the underlying morphism $\bar E \to Spec \pi_0 A$ is an ordinary [[elliptic curve]].

## Properties

### Moduli stack of derived elliptic curves

By the [[Goerss-Hopkins-Miller theorem]] the [[structure sheaf]] $\mathcal{O}$ of the [[moduli stack of elliptic curves]] (ordinary [[elliptic curves]]) lifts to a sheaf $\mathcal{O}^{top}$ of [[E-∞ rings]] which over a given [[elliptic curve]] is the corresponding [[elliptic spectrum]].
 
By ([[A Survey of Elliptic Cohomology|Lurie (Survey), theorem 4.1]]), this yields a  [[spectral Deligne-Mumford stack]] refinement $(\mathcal{M}_{ell}, \mathcal{O}^{top})$ which is the moduli stack of derived elliptic curves, in that there is a [[natural equivalence]] in [[E-∞ rings]] $A$ of the form

$$
  Hom(Spec(A), (\mathcal{M}_{ell},\mathcal{O}^{top}))
  \simeq
  E(A)
  \,,
$$

where on the left we have maps of [[structured (∞,1)-toposes]] and on the right the [[∞-groupoid]] of derived elliptic curves over $A$.

This is based on the representability theorem ([[A Survey of Elliptic Cohomology|Lurie (Survey), prop. 4.1]], [[Representability Theorems|Lurie (Representability)]]).


## References

* [[Jacob Lurie]], [[A Survey of Elliptic Cohomology]]

[[!redirects derived elliptic curves]]