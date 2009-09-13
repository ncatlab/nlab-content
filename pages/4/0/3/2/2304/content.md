+-- {: .un_remark}
###### Note
This page records the basic definitions of graph theory that have some degree of prevalence in the field that goes by that name.  Many directions of abstraction and augmentation are no doubt obvious, but it is useful to start from these.
=--

## Graph ##

Frank Harary's classical _Graph Theory_ defines the concept of a graph --- and much of its conceptual neighborhood --- in the following manner:

: A _graph_ $G$ consists of a finite nonempty set $V = V(G)$ of $p$ _points_ together with a prescribed set $X$ of $q$ unordered pairs of distinct points of $V$.  Each pair $x = \{ u, v \}$ of points in $X$ is a _line_ of $G$, and $x$ is said to _join_ $u$ and $v$.  We write $x = u v$ and say that $u$ and $v$ are _adjacent points_ (sometimes denoted $u \:\mathop{adj} v$);  point $u$ and line $x$ are _incident_ with each other, as are $v$ and $x$.  If two distinct lines $x$ and $y$ are incident with a common point, then they are _adjacent lines_.  A graph with $p$ points and $q$ lines is called a _$(p, q)$ graph_.  The (1,0) graph is _trivial_.  (Harary, 1969, p.&#160;9).

See [[graph]] for other kinds of graphs in the same vein; do not confuse this with the [[graph of a relation]], in particular, the [[graph of a function]].

## References ##

* Harary, F. (1969), _Graph Theory_, Addison-Wesley.

* Harary, F. and Palmer, E.M. (1973), _Graphical Enumeration_, Academic Press.

* Lambek, J. and Scott, P.J. (1986), _Introduction to Higher Order Categorical Logic_, Cambridge University Press.

## External links ##

* [Glossary of terms in combinatorics](http://www.math.uiuc.edu/~west/openp/gloss.html)

* [Data on dialectical immaterialism](http://www.math.uiuc.edu/~west/igt/)

## Discussion ##

### Re: Note ###

+--{: .query}
At [[latest changes]], [[Jon Awbrey]] introduced this page with:

> The page on [[graph]] has become too baroque to fix, but there needs to be a place to record the basic definitions of graph theory that are actually used by the larger schools of math folks who actually dare to call themselves graph theorists.

[[Mike Shulman]]: I don't think starting a new page that duplicates the intent of a previous one because one doesn't like the organization or approach of the previous one is a good idea.  Instead, let's have a discussion -- at [[graph]], where it belongs -- about what (you think) is wrong with it and how we can fix it.

I think the page called "graph theory" should be about the field in general, like the pages called [[category theory]] and [[topology]].  Definitions of individual concepts should be on their respective pages.

[[Jon Awbrey]]: Mike, all punny business aside, I don't think there's anything _wrong_ with the page on [[graph]] that can be fixed.  I'm a pragmatist about language, and if there's a community of people who use the terms that way, then it's pointless for me to try and reform their usage.  All I can do is observe that there are communities who use the words another way.  That usually happens because different people have different objectives and senses of what works to those ends.  So I don't see any duplication of intent here, though I might on further examination, I don't know.

_Toby_:  It turns out that I wrote an opinion about this back on [[graph]].

_Todd_: Although I agree with Mike, I have a possible compromise. We on the nLab have been known to write entries on individual books (like Stone Spaces by Johnstone). Why not simply rename this entry "Graph Theory" (caps) and start talking about this book by Harary, which is being quoted with approval here? That way you could definitely have your fixed anchor -- this is how Harary defines the notion of 'graph', and this is what he does with it -- and you could begin talking about an important book at the same time. 

An entry 'graph theory' (lower-case) would then be about the field at large, as Mike suggests. 

_Toby_:  While a page about Haray\'s book could be cool, I\'m still not convinced that there will be any real conflict between Jon and Mike, as this page develops.
=--
