
> Not to be confused with *[[nilpotent ideal]]*, which is a [[nilpotent element]] in the [[lattice]] of [[ideals]] of a [[ring]]. 

---

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $R$ a [[commutative ring]], its **nilradical** $I \subset R$ is the [[ideal]] of [[nilpotent elements]]: the collection of those elements $a \in R$ such that there is $n \in \mathbb{N}$ with $a^n = 0$.

The [[quotient]] $R/I$ is also called the _[[reduced object|reduced]]_ part of $R$.

(If $R$ is not [[commutative ring|commutative]] there are different generalization of the notion of nilradical. See Wikipedia, for the moment.) 

## Examples

Every [[local Artinian ring]] is a commutative ring whose set of non-invertible elements is a [[nilradical]]. 

With rings regarded as [[Isbell duality|formal dual]]s of [[affine scheme]]s, the canonical inclusion

$$
  Spec R/I \to Spec R
$$

is to be thought of as exhibiting the inclusion of $Spec R/I$ into an [[infinitesimal object|infinitesimal thickening]] of itself.

For $X : CRing \to Set$ a [[presheaf]] on the [[category]] of [[commutative rings]], the presheaf

$$
  X_{dR} : Spec R \mapsto X(Spec R/I)
$$

is called the [[de Rham space]] of $X$.

## Related concepts

* [[infinitesimal extension]]

* [[reduced ring]]

* [[Artinian local ring]]

## References

See also:

* Wikipedia, *[Nilradical](https://en.m.wikipedia.org/wiki/Nilradical_of_a_ring)*

[[!redirects nilradical]]
[[!redirects nilradicals]]

