
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

## Properties

### Relation to prime ideals 

\begin{theorem} Assuming the [[axiom of choice]], if $R$ is a commutative ring, then the nilradical equals the intersection of all [[prime ideals]] of $R$. \end{theorem} 

\begin{proof} In one direction, it it elementary that if $x$ is nilpotent, then $x$ belongs to any prime $\mathfrak{p}$. 

For the other direction, we assume the [[axiom of choice]], or slightly more sharply, the [[ultrafilter principle]], which implies that any non-trivial ring $R$ has a proper prime ideal $\mathfrak{p}$: see [[prime ideal theorem]]. We must show that if $x$ is not nilpotent, then there is some prime ideal $\mathfrak{p}$ that does not contain $x$. But if $x$ is not nilpotent, then the set $1, x, x^2, \ldots$ is a multiplicative set that does not contain $0$. It follows that the [[localization]] $R[x, \frac1{x}]$ with respect to this multiplicative set is a non-trivial ring, and hence has a prime ideal $\mathfrak{q}$. The image of $x$ under the canonical map $\phi: R \to R[x, \frac1{x}]$ is invertible, hence is not contained in $\mathfrak{q}$. Then the inverse image $\mathfrak{p} = \phi^{-1}(\mathfrak{q})$ is a prime ideal that does not contain $x$. \end{proof} 


## Related concepts

* [[infinitesimal extension]]

* [[reduced ring]]

* [[Artinian local ring]]

## References

See also:

* Wikipedia, *[Nilradical](https://en.m.wikipedia.org/wiki/Nilradical_of_a_ring)*

[[!redirects nilradical]]
[[!redirects nilradicals]]

