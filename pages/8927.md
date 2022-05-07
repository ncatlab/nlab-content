

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition 

Let $K$ be a [[Grothendieck 2-topos]].  We say that $K$ is **$n$-truncated** if it has a small [[eso-generator]] consisting of $(n-1)$-[[truncated object|truncated objects]].  It is easy to see that if a coproduct of $(n-1)$-truncated objects is $(n-1)$-truncated (as is the case for all $n\ge 1$), then this is equivalent to saying that $K$ has _enough $(n-1)$-truncated objects_ (i.e. every object admits an eso from an $(n-1)$-truncated one).  In particular:

* $K$ is always **2-truncated**.
* $K$ is **(2,1)-truncated** if it has [[core|enough groupoids]].
* $K$ is **1-truncated** if it has enough discretes.
* $K$ is **(0,1)-truncated** if the subterminal objects are eso-generating.
* $K$ is **(-1)-truncated** if the terminal object is an eso-generator.


## $n$-sites and $n$-sheaves

By the [[2-Giraud theorem]], small eso-generating sets of objects correspond to small [[2-site|2-sites]] of definition for $K$.  Thus, if we define an $n$-site to be a 2-site which is an $n$-category (where $n\le 2$ as usual), we have:

+--{: .num_theorem}
###### Theorem
A Grothendieck 2-topos is $n$-truncated iff it is equivalent to the 2-category of 2-sheaves on some $n$-site.
=--

Note that a 1-site is the same as the usual notion of [[site]], and a [[(0,1)-site]] is sometimes called a _[[posite]]_. In particular, any [[frame]] is a (0,1)-site with its [[canonical coverage]] (the covering families are given by [[unions]]).

Particular cases include:

* $K$ is 1-truncated iff it is equivalent to the 2-category of 2-sheaves (stacks) on an ordinary small (1-)site, and therefore to the 2-category of stacks for the canonical coverage on some Grothendieck 1-topos.

* $K$ is (0,1)-truncated iff it is equivalent to the 2-category of stacks on a posite, and therefore also to the 2-category of stacks on some [[nlab:locale|locale]].  We call such a $K$ _localic_.

* If $K$ is (-1)-truncated, then it is in particular localic, and its terminal object is a (strong) generator.  It is not hard to see that this is equivalent to saying that the corresponding locale $X$ is a sublocale of the terminal locale $1$.  Thus, just as [[nlab:(-1)-category|(-1)-categories]] are sub*sets* of $1$, (-1)-toposes are sub*locales* of $1$.  If $Cat$ has classical logic, this implies that either $X\cong 0$ or $X\cong 1$; and hence that either $K\simeq 1$ or $K\simeq Cat$.  However, constructively there may be many other sublocales of $1$.

* It would be nice if the only (-2)-truncated Grothendieck 2-topos were $Cat$.  However, I don't see a way to make this happen except by fiat.


## Grothendieck $n$-toposes

Now, if $C$ is an $n$-site, it is also reasonable to consider **$n$-sheaves** on $C$, by which we mean 2-sheaves taking values in $(n-1)$-categories.  Thus, a 1-sheaf on a 1-site is precisely the usual notion of [[nlab:sheaf|sheaf]] on a site.  And a (0,1)-sheaf on a (0,1)-site is easily seen to be a lower set that is an "ideal" for the coverage.

We define a **Grothendieck $n$-topos** to be an $n$-category equivalent to the $n$-category of $n$-sheaves on an $n$-site.  The case $n=1$ gives classical [[nlab:Grothendieck topos|Grothendieck toposes]]; the case $n=(0,1)$ gives [[nlab:locale|locales]].  Note the distinction between a Grothendieck $n$-topos and an $n$-truncated Grothendieck 2-topos.  The relationship is that

1. The 2-category of 2-sheaves for the canonical coverage on a Grothendieck $n$-topos is an $n$-truncated Grothendieck 2-topos, and
1. Any $n$-truncated Grothendieck 2-topos arises in this way from the Grothendieck $n$-topos which is its full subcategory of $(n-1)$-truncated objects.

This relationship is completely analogous to the classical relationship between locales and localic toposes.  In fact, if $Gr n Top$ denotes the $(n+1)$-category of Grothendieck $n$-toposes (that is, $n$-categories of $n$-sheaves on an $n$-site), we have inclusions
$$\array{
  &&&&&& Gr(1,2)Top\\
  &&&&& \nearrow && \searrow\\
  Gr (-1) Top &\to&
  Gr(0,1)Top &\to &
  Gr1Top &&&&
  Gr2Top\\
  &&&&& \searrow && \nearrow\\
  &&&&&& Gr(2,1)Top
}$$
where the inclusion from $Gr n Top$ to $Gr (n+1) Top$ is given by taking the $(n+1)$-category of $(n+1)$-sheaves for the canonical coverage.  (See [[2-geometric morphism]] for the morphisms in these categories.)

## Related concepts

* [[n-localic (∞,1)-topos]]

[[!include flavors of higher toposes -- list]]


## References

The material on this page is taken from

* [[Mike Shulman]], _[[michaelshulman:truncated 2-topos]]_


[[!redirects n-site]]
[[!redirects n-sheaf]]
[[!redirects n-sites]]
[[!redirects n-sheaves]]
[[!redirects Grothendieck n-topos]]
[[!redirects n-truncated 2-topos]]
