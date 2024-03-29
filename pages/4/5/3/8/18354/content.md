+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition {#sec:orgcc9169c}

An
[[imaginary element]] of a (finitary)
[[first-order theory]] is an equivalence
class $X/E$ of a (finitary first-order) [[definable
set]] $X$ quotiented by a (finitary first-order)
[[definable groupoid|definable equivalence
relation]] $E$. A **hyperimaginary** is an equivalence
class $X/E$ of a [[definable set#type-definable-set |
type-definable]] $X$ quotiented by a
[[definable set#type-definable-set | type-definable]] equivalence relation $E$.

## Examples {#sec:orgdc24af7}

The prototypical example of a hyperimaginary is an equivalence class of
the quotient of the [[hyperreal numbers]] by
the equivalence relation "$x$ is infinitesimally close to $y$", which is
definable by the countable conjunction
$\left( \left| x - y \right| &lt; \frac{1}{n} \right)_{n \in \mathbb{N}}$.

## Elimination of hyperimaginaries {#sec:org59c5525}

Let $X/E$ be a hyperimaginary. $T$ is said to **eliminate** the
hyperimaginary $X/E$ (c.f. [[elimination of
imaginaries]]) if $X/E$ is interdefinable with a sequence
of imaginaries, i.e. if every type-definable equivalence relation is, in
fact, a conjunction of definable equivalence relations.

[[stable theory|Stable theories]] eliminate
hyperimaginaries. This is related to a result of Hrushovski's that in a stable theory, (pro-definable) groupoids are pro-(definable groupoids).

## Properties {#sec:org623f6fa}

-   In the same way that the [[automorphism
    group]] $\operatorname{Aut}(M)$ of a model acts on
    [[imaginary element|imaginaries]],
    $\operatorname{Aut}(M)$ acts on hyperimaginaries.

-   Any hyperimaginary $X/E$ in the sense of
    the previous paragraph can be extended to a quotient of the entire
    model $M^{\alpha}$ (in the (possibly infinitary)
    [[type|sort]] $\alpha$ of $E$) by a
    type-definable equivalence relation $E'$ obtained by preserving $E$ on $X$ and extending it to be the discrete equivalence relation on $M^{\alpha} \backslash X$. In symbols, $E' \overset{\operatorname{df}}{=} (E(x,y) \wedge (x,y) \in X \times X) \vee (x = y)$. (This is a special case of the fact that finite disjunctions of type-definable sets are again type-definable. It is not true that arbitrary disjunctions of type-definable sets are again type-definable, since $\operatorname{Aut}(\mathbb{M})$-invariant subsets of $\mathbb{M}$ the [[monster model]] have this form.)

-   The process of taking points of hyperimaginaries in models
    ($M \mapsto M(X/E)$) does not commute
    with [[ultraproducts]]. For example, if
    $E$ is the equivalence relation in the reals of being
    infinitesimally close together, it's easy to see that
    $\mathbb{R}^{\mathcal{U}}/E \not \simeq \left(\mathbb{R}/E \right)^{\mathcal{U}}$,
    since $\mathbb{R}/E \simeq \mathbb{R}$ (after all, the real numbers
    are Hausdorff) so that the right hand side is the nonstandard reals
    $^* \mathbb{R}$ again (so every number has a [[halo|cloud]] of infinitesimals
    around it) while the left hand side has no points which are
    infinitesimally close together.

+-- {: .num_remark}
###### Remark

This is actually an excellent example of why we shouldn't expect in
general the process of taking points of hyperimaginaries in a model to
commute with ultraproducts: on one hand, if $E$ is a type-definable
equivalence relation on $X$, and $\mathcal{U}$ an
[[ultrafilter]], then computing
$\left(\prod_{i \in I} M_i/\mathcal{U} \right)(X/E)$ yields
$E$-equivalence classes of [[germs]]
$[m_i]_{\mathcal{U}}$. That is, for every condition $\varphi(x_1, x_2)$
in $E$ that needs to be checked to conclude that two tuples are
$E$-equivalent, every pair of $E$-equivalent germs
$[m_i]_{\mathcal{U}}$ and $[n_i]_{\mathcal{U}}$ agree on $\varphi$ on
some subset $P \subseteq I$ for $P$ in $\mathcal{U}$.But these $P$s
depend on $\varphi$. They aren't uniform, and there's possibly no set
$P'$ in the ultrafilter (the intersection of all the $P$'s might be
empty) on which one could decide if $[m_i]$ and $[n_i]$ are
$E$-equivalent for every condition $\varphi \in E$.

On the other hand, one could try computing
$\left( \prod_{i \in I} M_i(X/E) \right) /\mathcal{U}$. One ends up
instead with germs of hyperimaginaries, as in
$[[m_i]_E]_{\mathcal{U}}$, but this is a tighter
equivalence relation: $([x_i]_E)_i$ and $([y_i]_E)_i)$ are
$\mathcal{U}$-equivalent if and only if there is a single $P \in \mathcal{U}$,
uniform for every $i \in P$ and for every $\varphi \in E$ so that
$M_i \models \varphi(x_i, y_i)$. This means that the commutation of
these two procedures should fail precisely when the $P$'s on the left
hand side intersect to something outside of the ultrafilter.

Indeed, in the example we first mentioned, consider the sequences
$(1, 2, 3, \dots)$ and $(1 + 1/2, 2 + 1/3, 3 + 1/4, \dots)$. If we take
them mod-$\mathcal{U}$, then mod-$E$, then they are equivalent as
hyperimaginaries in $^*\mathbb{R}$, since for each condition "x is less
than $1/n$ away from y", these two sequences agree cofinitely many times
(and every ultrafilter contains the cofinite filter). But these cofinite
sets of indices are getting smaller and smaller and intersect to
$\emptyset$. And if we take them mod-$E$, then mod-$\mathcal{U}$, they
remain distinct.

=--

## Related concepts {#sec:org1bb2b22}

-   [[imaginary element]]

-   [[infinitesimal]]

-   [[simple theory]]

## References {#sec:org00f5b3c}

-   Frank Wagner, *Simple Theories* (2000)

-   Byunghan Kim, *Simplicity Theory* (2014)

-   Enrique Casanovas, *Simple theories and hyperimaginaries* (2011)

[[!redirects hyperimaginary]]
[[!redirects hyperimaginaries]]
[[!redirects hyperimaginary elements]]
[[!redirects elimination of
hyperimaginaries]]