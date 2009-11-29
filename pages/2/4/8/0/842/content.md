#Idea#

The notion of [[limit]] generalizes to [[quasi-category|quasi-categories]] straightforwardly using the generalization of [[over category]] and [[terminal object]] to [[over quasi-category]] and [[terminal object in a quasi-category]].


#Definition#

For $K$ and $C$ two [[quasi-category|quasi-categories]] and $F : K \to C$ a morphism of [[quasi-category|quasi-categories]], the **limit** over $F$ is, if it exists, the [[terminal object in a quasi-category|quasi-categorical terminal object]] in the [[over quasi-category|over quasi-categories]] $C_{/F}$:

$$
  lim F := TerminalObj(C_{/F})
  \,.
$$

The definition of [[colimit]] in this context is the obvious analogue.

#Examples#

## Homotopy limits in Kan-enriched categories ##

Let $K$ and $C$ be categories [[enriched category|enriched]] in [[Kan complex|Kan complexes]] and $F : K \to C$ a morphism of Kan-enriched categories (i.e. an [[SimpSet]]-functor). Then the [[homotopy limit]] of $F$ (computed for instance as described at [[weighted limit]]) coincides with the quasi-categorical limit of $F$ under the embedding of simplicial categories into quasi-categories.

This is [theorem 4.2.4.1, p. 214](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf#page=214) in Lurie's book (see below).


# Properties # 

## Limits and colimits with values in $\infty Grpd$ ##

Limits and colimits over a [[(∞,1)-functor]] with values in the [[(∞,1)-category]] [[∞-Grpd]] of [[∞-groupoids]] may be reformulation in terms of the  [[universal fibration of (infinity,1)-categories]].

Let [[∞-Grpd]] be the [[(∞,1)-category]] of [[∞-groupoid]]s. Let the [[(∞,1)-functor]] $Z|_{Grpd} \to \infty Grpd^{op}$ be the [[universal fibration of (infinity,1)-categories|universal ∞-groupoid fibration]] whose fiber over the object denoting some $\infty$-groupoid is that very $\infty$-groupoid.

Then let $X$ be any [[∞-groupoid]] and

$$
  F : X \to \infty Grpd
$$

an [[(∞,1)-functor]]. Recall that the [[Cartesian fibration|coCartesian fibration]] $E_F \to X$ classified by $F$ is the pullback of the [[universal fibration of (∞,1)-categories]] $Z$ along F:

$$
  \array{
    E_F &\to& Z|_{Grpd}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{F}{\to}& \infty Grpd
  }
$$

+-- {: .un_prop }
###### Proposition

Let the assumptions be as above. Then:

* The colimit of $F$ is equivalent to $E_F$:

  $$
    E_F \simeq colim F
  $$

* The limit of $F$ is equivalent to the [[(infinity,1)-category of cartesian section|(∞,1)-groupoid of sections]] of $E_F \to X$

  $$
    \Gamma_X(E_F) \simeq lim F
    \,.
  $$

=-- 

+-- {: .proof}
###### Proof

The statement for the colimit is corollary 3.3.4.6 in [[Higher Topos Theory|HTT]]. The statement for the limit is corollary 3.3.3.4.

=--

If instead of [[∞-Grpd]] the target is the [[(∞,1)-category of (∞,1)-categories]] then the latter statement is true with the $(\infty,1)$-category of all sections replaced by [[(∞,1)-category of cartesian sections]].

#References#

The definition of limit in quasi-categories is due to

* A. Joyal, _Quasi-categories and Kan complexes_ Journal of Pure and Applied Algebra 175 (2002), 207-222.

It appears as [definition 1.2.13.4, p. 48](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=48) in 

* [[Jacob Lurie]], [[Higher Topos Theory]] 

[[!redirects colimit in a quasi-category]]
[[!redirects limit in quasi-categories]]
[[!redirects limits in quasi-categories]]
[[!redirects colimit in quasi-categories]]
[[!redirects colimits in quasi-categories]]
[[!redirects (infinity,1)-limit]]
[[!redirects (infinity,1)-colimit]]