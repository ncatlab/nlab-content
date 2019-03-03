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

If these equivalent conditions hold, we write $\lambda\unlhd \mu$.  If $\lambda \unlhd \mu$ and $\lambda\lt\mu$, we write $\lambda\lhd \mu$ and say that $\lambda$ is **sharply smaller** than $\mu$.

### Examples

* For any uncountable regular cardinal $\lambda$ we have $\aleph_0\lhd \lambda$.  (In fact $\aleph_0$ is the only infinite regular cardinal with this property; see [this question](https://mathoverflow.net/q/150305).)

* For any regular cardinal $\lambda$ we have $\lambda\lhd \lambda^+$ (its [[successor cardinal]]).

* If $\lambda\le\mu$ then $\lambda \lhd (2^\mu)^+$.  Thus, for any set $S$ of regular cardinals there is a regular cardinal $\mu$ such that $\lambda\lhd \mu$ for all $\lambda\in S$.

* We write $\lambda\ll\mu$ if for every $\lambda'\lt\lambda$ and $\mu'\lt\mu$ we have $(\mu')^{\lambda'} \lt\mu$.  (This is [[Higher Topos Theory]], Definition A.2.6.3.)  Then if $\lambda\ll\mu$, then $\lambda\lhd \mu$.

  The converse claim ($\lambda \lhd \mu$ implies $\lambda\ll\mu$) is independent of [[ZFC]].  On one hand it implies the [[generalized continuum hypothesis]] (GCH) for regular cardinals (and in particular the ordinary [[continuum hypothesis]] (CH)), since if $\lambda^+ \lt 2^\lambda$ then we have $\lambda^+ \lhd \lambda^{++}$ but not $\lambda^+ \ll \lambda^{++}$.  Thus it is unprovable in ZFC (if ZFC is consistent), since CH is unprovable.  On the other hand, it is implied by the full GCH, as explained by [Goldberg](#Goldberg19), and is thus consistent with ZFC since GCH is.

* If $\kappa$ is an [[inaccessible cardinal]], then every $\lambda\lt\kappa$ satisfies $\lambda\lhd \kappa$.

* $\aleph_1 \lhd \aleph_{\omega+1}$ does not hold.

## References

* {#MP}  [[Michael Makkai]], [[Robert Paré]], _Accessible categories: The foundations of categorical model theory_ Contemporary Mathematics 104. American Mathematical Society, Rhode Island, 1989.1989. 
{#MakkaiPare}

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AR}

* [[Jacob Lurie]], [[Higher Topos Theory]]

* {#Goldberg19} Gabe Goldberg, answer to MathOverflow question _Raising the index of accessibility_,  <https://mathoverflow.net/q/324492>
