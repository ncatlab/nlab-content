# Sharply smaller cardinals

* table of contents
{: toc}

## Definition

+--{: .un_theorem}
###### Theorem
For [[regular cardinals]] $\lambda\le\mu$, the following are equivalent:

* Every $\lambda$-[[accessible category]] is $\mu$-accessible.
* For every $\mu'\lt\mu$, the set $P_\lambda(\mu')$ of subsets of $\mu'$ of [[cardinality]] $\lt\lambda$ has a [[cofinal subset]] of cardinality $\lt\mu$.
=--

For a proof, see Theorem 2.11 of [Adamek-Rosicky](#AR) or section 2.3 of [Makkai-Pare](#MP).

If these equivalent conditions hold, we write $\lambda\unlhd \mu$.  If $\lambda \lhd \mu$ and $\lambda\lt\mu$, we write $\lambda\lhd \mu$ and say that $\lambda$ is **sharply smaller** than $\mu$.

### Examples

* For any uncountable regular cardinal $\lambda$ we have $\omega\lhd \lambda$.

* For any regular cardinal $\lambda$ we have $\lambda\lhd \lambda^+$ (its [[successor cardinal]]).

* If $\lambda\le\mu$ then $\lambda \lhd (2^\mu)^+$.  Thus, for any set $S$ of regular cardinals there is a regular cardinal $\mu$ such that $\lambda\lhd \mu$ for all $\lambda\in S$.

* We write $\lambda\ll\mu$ if for every $\lambda'\lt\lambda$ and $\mu'\lt\mu$ we have $(\mu')^{\lambda'} \lt\mu$.  (This is [[Higher Topos Theory]], Definition A.2.6.3.)  Then if $\lambda\ll\mu$, then $\lambda\lhd \mu$.

* $\aleph_1 \lhd \aleph_{\omega+1}$ does not hold.

## References

* {#MP}  [[Michael Makkai]], [[Robert Paré]], _Accessible categories: The foundations of categorical model theory_ Contemporary Mathematics 104. American Mathematical Society, Rhode Island, 1989.1989. 
{#MakkaiPare}

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AR}

* [[Jacob Lurie]], [[Higher Topos Theory]]
