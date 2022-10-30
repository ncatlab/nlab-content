#Idea#

An __$A_\infty$-operad__ is an [[operad]] over some enriching category $C$ which is a (free) [[homological resolution|resolution]] of the standard associative operad enriched over $C$ (that is, the operad whose algebras are monoids).

Important examples, to be discussed below, include:

* The topological operad of Stasheff associahedra.

* The little-1-cubes operad.

* The standard dg-$A_\infty$-operad.

* The standard categorical $A_\infty$-operad.

An $A_\infty$-operad, like the standard associative operad, can be defined to be either a _symmetric_ or a _non-symmetric_ operad.  On this page we assume the non-symmetric version.  When regarded as a symmetric operad, an $A_\infty$-operad may also be called an $E_1$-operad.

An [[algebra over an operad|algebra]] over an $A_\infty$-operad is called an __$A_\infty$-object__, where -object is often replaced with an appropriate noun; thus we have the notions of **$A_\infty$-[[A-infinity-space|space]]**, **$A_\infty$-[[A-infinity-algebra|algebra]]**, and so on.  In general, $A_\infty$-objects can be regarded as 'monoids up to coherent homotopy.'  Likewise, a [[category over an operad|category]] over an $A_\infty$-operad is called an $A_\infty$-[[A-infinity-category|category]].

Some authors use the term '$A_\infty$-operad' only for a _particular_ chosen $A_\infty$-operad in their chosen ambient category, and thus use '$A_\infty$-object' and '$A_\infty$-category' for algebras and categories over this particular operad.  The $A_\infty$-operads discussed below are common choices for this 'standard' $A_\infty$-operad.


#The topological Stasheff associahedra operad#

Let $\{K(n)\}$ be the sequence of [[associahedron|Stasheff associahedra]].  This is naturally equipped with the structure of a (non-symmetric) operad $K$ enriched over [[Top]] called the **topological Stasheff associahedra operad** or simply the **Stasheff operad**.  Since each $K(n)$ is [[contractible space|contractible]], $K$ is an $A_\infty$-operad.

The original article that defines associahedra, and in which the operad $K$ is used implicitly to define $A_\infty$-topological spaces, is

* Stasheff, _Homotopy associative H-spaces I_, _II_, Trans. Amerk. Math. Soc. 108 (1963), 275-312

A textbook discussion (slightly modified) is in section 1.6 of the book

* Martin Markl, Steve Shnider, Jim Stasheff, _Operads in Algebra, Topology and Physics_ ([web](http://books.google.de/books?id=fMhZjT9lQo0C&pg=PA56&lpg=PA56&dq=Stasheff+associahedra&source=bl&ots=ZuGXjT4zbp&sig=V-taGG2LHS0msHK-PTxmUXXCvEY&hl=de#PPP1,M1))


# The little 1-cubes operad #

Let $\mathcal{C}_1(n)$ denote the configuration space of $n$ disjoint intervals linearly embedded in $[0,1]$.  Substitution gives the sequence $\{\mathcal{C}_1(n)\}$ an operad structure, called the **little 1-cubes operad**; it is again an $A_\infty$-operad.  This is a special case of the [[little n-cubes operad]] $\mathcal{C}_n$, which is in general an $E_n$-[[E-n-operad|operad]].

The little $n$-cubes operads (in their symmetric version) were among the first operads to be explicitly defined, in the book that first explicitly defined operads:

* May, _The Geometry of Iterated Loop Spaces_


#The standard dg-$A_\infty$-operad#

The **standard dg-$A_\infty$-operad** is the dg-operad (that is, operad enriched in [[cochain complex]]es $Ch^\bullet(Vect)$)

* freely generated from one $n$-ary operation $f_n$ for each $n \geq 1$, taken to be in degree
$2 - n$;

* with the differential of the $n$th generator given by
$$ -
\sum_{j+p+q = n}^{1 \lt p \lt n} (-1)^{j p + q} a_{p,j,n} ,$$
where $a_{p,j,n}$ is $f_p$ attachched to the $(j+1)$st input of $f_{n}$.

This can be shown to be a standard free resolution of the linear associative operad in the context of dg-operads; see [Markl 94](http://arxiv.org/abs/hep-th/9411208), [proposition 3.3](http://arxiv.org/PS_cache/hep-th/pdf/9411/9411208v1.pdf#page=13); therefore it is an $A_\infty$-operad.

It can also be shown to be _isomorphic_ to the operad of top-dimensional (cellular) chains on the topological Stsheff associahedra operad.  This is discussed on [pages 26-27](http://arxiv.org/PS_cache/hep-th/pdf/9411/9411208v1.pdf#page=26) of [Markl 94](http://arxiv.org/abs/hep-th/9411208)

In the dg-context it is especially common to say '$A_\infty$-algebra' and '$A_\infty$-category' to mean specifically algebras and categories over _this_ operad.  The explicit description of this operad given above means that such $A_\infty$-algebras and categories can be given a fairly direct description without explicit reference to operads.

In addition to

* Martin Markl, _Models for operads_ ([arXiv](http://arxiv.org/abs/hep-th/9411208))

another reference is section 1.18 of

* Yu. Bespalov, V. Lyubashenko, O. Manzyuk, _Pretriangulated $A_\infty$-categories_, Proceedings of the Institute of Mathematics of NAS of Ukraine, vol. 76, Institute of Mathematics of NAS of Ukraine, Kyiv, 2008, 598 ([ps.gz](http://www.math.ksu.edu/~lub/cmcMonad.gz))

A relation of the linear dg-$A_\infty$-operad to the Stasheff associahedra is in the proof of proposition 1.19 in Bespalov et al.



# The standard categorical $A_\infty$-operad #

Let $O$ be the operad in [[Set]] freely generated by a single binary operation and a single nullary operation.  Thus, the elements of $O(n)$ are ways to associate, and add units to, a product of $n$ things.  Let $B(n)$ be the [[indiscrete category]] on the set $O(n)$; then $B$ is an $A_\infty$-operad in [[Cat]].  $B$-algebras are precisely (non-strict, biased) [[monoidal category|monoidal categories]], and $B$-categories are precisely (biased) [[bicategory|bicategories]].

If instead of $O$ we use the $Set$-operad freely generated by a single $n$-ary operation for every $n$, we obtain a $Cat$-operad whose algebras and categories are _unbiased_ monoidal categories and bicategories.


***

### Discussion ###

A previous version of this entry started the following discussion:

+--{: .query}
[[Mike Shulman|Mike]]: Evidently some people use the terminology this way, but for many people there is no 'the' $A_\infty$-operad.  Rather _an_ $A_\infty$-operad is any operad equivalent to the associative operad (in whatever enrichment we are working).  Likewise, an $A_\infty$-algebra is an algebra for _some_ $A_\infty$-operad.

If we want a page about this particular operad, could we call it maybe [[standard linear A-infinity-operad]]?  Or [[linear Stasheff operad]] since, as Jim Stasheff pointed out at the cafe, it is the operad of cellular chains on the standard topological $A_\infty$-operad of associahedra?

[[Urs Schreiber|Urs]]: i have tried to expand on this now (was in a haste yesterday) -- would it make sense to keep all the examples listed here on one page, the way I have it now?

[[Mike Shulman|Mike]]: Yes, I think that is a good idea.  I have added a couple more 'standard' examples and tried to uniformize the description of each.  This meant deleting a little that I thought was extraneous from the standard dg-$A_\infty$-operad.  What do you think?

=--
