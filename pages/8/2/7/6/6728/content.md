
\tableofcontents

## Idea ##

Category of descent data is a particular presentation of a [[2-limit|2-categorical limit]] in [[Cat]], i.e. the [[descent object]], intended to solve the [[descent]] problem. It can be defined in several setups: in a formulation of descent via [[fibered categories]] and [[Grothendieck topologies]], as well as in the (co)[[monadic descent]]. In the first case, the descent category appears as a presentation of the [[descent object]], while in the (co)monadic descent the descent category is given by the [[Eilenberg-Moore category]] of the ([[comonad|co]])[[monad]]. In a particular setup, the two approaches give the same result, see [[Bénabou-Roubaud theorem]].

## Descent along a cover ##

+--{.query}
This kind of descent is described in the article [[stack]] using the bar construction to write a [[sieve]] as a [[colimit]] of representables.
=--

Let $C$ be a site, $p:D\to C$ a fibration, $x\in C_0$, $U_x$ a cover of $x$. $h_x\hookrightarrow C/x$ the full subcategory of arrows, that factor through some $u\rightarrow x$ of the cover; the corresponding functor $C^{op}\rightarrow \Cat$ is then a sieve.
The **category of descent data** (sometimes shortcut to **descent category**) of $p$ along $U_x$ is defined to be the functor category $[h_x,D]$.

## See also ##

* [[descent]]

* [[descent object]]

* [[stack]]

## References ##

* [[Angelo Vistoli]], _Notes on Grothendieck topologies, fibered categories and descent theory_ ([arXiv](http://arxiv.org/abs/math/0412512)) (p.74)

* [[Stacks Project]], ([Tag 02ZC](https://stacks.math.columbia.edu/tag/02ZC))


[[!redirects Descent category]]
[[!redirects descent category]]
[[!redirects the category of descent data]]
