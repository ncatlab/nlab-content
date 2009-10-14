[[!redirects n-localic (∞,1)-topos]]

# Idea #

Recall that a [[topos]] may be thought of as a generalized [[topological space]]. A [[localic topos]] is one that essentially behaves  like an ordinary [[topological space]] after all.

In [[higher topos theory]] one realizes that an ordinary [[topos]] that is a [[localic topos]] may be thought of as a [[(1,1)-topos]] that _effectively behaves_ like a [[(0,1)-topos]]. And a (Grothendieck) [[(0,1)-topos]] is effectily a [[locale]] which is essentially a [[topological space]].

This is the beginning of a pattern: a $k$-localic [[(n,1)-topos]] for $0 \leq k \leq n \leq \infty$ is a [[(n,1)-topos]] that effectively behaves like a $(k,1)$-topos.

In other words, when we embed $(k,1)$-toposes in the larger context of $(n,1)$-toposes for $k \leq n$ then we can remember those $(n,1)$-toposes that came from $(k,1)$-toposes by noticing that these are $k$-localic.

# Definition (raw material at the moment) #



recall from [[n-truncated object of an (infinity,1)-category]] that for $X$ an [[(infinity,1)-topos]]
the symbols $\tau_{n-1} X$ denote the essential image of the truncation
functor $\tau_{n-1} : X \to X$. Recall from the warning remark
6.4.5.10 and the discussion above it that this should really be thought of
as $\tau_n X$ if we think of $X$ as a [[topological space]].

Definition (n-localic $(\infinity,1)$-topos)

def 6.4.5.8 in [[Higher Topos Theory]]

For $X,Y$ $(\infty,1)$-toposes, 
let $Geom(X,Y) \subset Fun(X,Y)$ denote the subcategory of the [[(infinity,1)-category of (infinity,1)-functors]] $X \to Y$
that are [[geometric morphism]]s of $(\infty,1)$-toposes.

An [[(infinity,1)-topos]] $X$ is $n$-localic if for any other
$(\infty,1)$-topos $Y$ the canonical map

$$
  Geom(X,Y) \to Geom(\tau_{n-1}X, \tau_{n-1}Y)
$$

is an equivalence.



#References#

section 6.4.5 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[!redirects localic (∞,1)-topos]]