
> This entry is about domains in [[ring theory]]. For other uses, see at _[[domain]]_. 

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Some authors call a domain an [[integral domain]]. However, we maintain a distinction between domains and integral domains, and reserve "integral domain" for the commutative domains. 

### By the cancellative property

A unital [[ring]] $R$ is a __domain__ if it is nontrivial and the multiplicative submonoid $R \backslash \{0\}$ is a [[cancellative monoid]] (i.e., $1 \neq 0$ and left and right multiplication by $c$ is injective if $c \neq 0$, which may be combined as left and right multiplication by $c$ is injective if and only if $c \neq 0$) 

### By zero divisors

A unital [[ring]] $R$ is an __domain__ if it is nontrivial and has no non-zero [[zero divisors]] (i.e., $1 \ne 0$ and $a b = 0$ implies $a = 0$ or $b = 0$). 

In this definition, the [[trivial ring]] is [[too simple to be simple|too simple]] to be an integral domain. You can see this by phrasing this definition without [[bias]] as: any product of (finitely many) nonzero elements of $R$ (which includes the empty product $1$) must be nonzero.

## Properties

A domain $R$ is an __[[Ore domain]]__ if the set of all nonzero elements is an [[Ore set]] in $R$. In that case the Ore localized ring is called the _[[Ore quotient ring]]_ of $R$. 

## Examples

For example, the ring of [[integers]], any [[skewfield]], the ring of global sections of the structure sheaf of any [[integral scheme]], an [[Ore extension]] of any other domain.

## Generalizations

In principle, one could just as easily consider a [[rig]] or [[semiring]] $R$.  In that case, however, only the definition involving the cancellative property extends to rigs and semirings. Furthermore, we should add the additional requirement that addition in $R$ is cancellable (that is, addition by any element is injective), to make the analogue of the previous paragraph correct. These could be called a *domain rig* or *domain semiring*. One could also relax the requirement that the domain be associative or unital, this could be called a *domain $\mathbb{Z}$-algebra*, in the context where $R$-algebras are usually not assumed to be [[associative unital algebras]]. 

## See also

* [[integral domain]]

## External links

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Domain_(ring_theory)">Domain (ring theory)</a>*

[[!redirects domain ring]]
[[!redirects domain rings]]

[[!redirects domain rig]]
[[!redirects domain rigs]]
[[!redirects domain semiring]]
[[!redirects domain semirings]]

[[!redirects domain Z-algebra]]
[[!redirects domain Z-algebras]]
[[!redirects domain unital Z-algebra]]
[[!redirects domain unital Z-algebras]]
