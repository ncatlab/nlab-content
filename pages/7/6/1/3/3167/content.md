
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In every [[smooth topos]] there is a notion of [[infinitesimal object]] and of [[infinitesimal number]].  The most common such infinitesimal numbers are [[nilpotent]], but in some special smooth toposes, there is in addition a notion of _invertible infinitesimal_.  In these toposes there is likewise an object of _smooth natural numbers_, which contains _infinite_ or _[[nonstandard number|nonstandard natural numbers]]_ (and whose inverses are invertible infinitesimals).

Some examples of such smooth toposes are discussed at [[Models for Smooth Infinitesimal Analysis]].


## The central mechanism

The phenomenon of "smooth" nonstandard natural numbers in a [[Grothendieck topos]] arises from the following simple general principle:

Consider any [[Grothendieck topos|sheaf topos]] $\mathcal{T} = Sh(C)$ such that

1. the category [[Set]] embeds [[full and faithful functor|full and faithfully]] into $\mathcal{T}$. 

   (For [[smooth topos]]es we have, if they are "well adapted", even a full and faithful inclusion of [[Diff]] and then the one of [[Set]] is the one induced by the inclusion $Set \hookrightarrow Diff$.)

1. the [[Grothendieck topology]] on $C$ is on each object given by _finite_ covering families.

In such a case there are two objects in $\mathcal{T}$ that both look like they should qualify as the [[internalization|internal object]] of [[natural number]], but that are different:

1. The image $N$ of the set $\mathbb{N}$ under the given full and faithful embedding. 

   This yields, trivially, a sheaf such that morphisms from any other set into it are given by arbitrary $\mathbb{N}$-valued functions on this set.

1. The abstractly defined [[natural numbers object]] $\Delta(\mathbb{N})$: 

   this is the [[sheafification]] of the [[presheaf]] that is constant on the set $\mathbb{N}$. A morphism into this presheaf is a _constant_ $\mathbb{N}$-valued function. And since we are sheafifying, by assumption, with respect to _finite_ covers, a morphism from a set into its sheafification is a function into $\mathbb{N}$ that is constant on each patch of a _finite_ cover of that set and hence is a _bounded_ $\mathbb{N}$-valued function.

The unbounded functions thus represent [[infinite number|infinite]] or [[nonstandard number|non-standard]] "smooth natural numbers."  In particular, a [[generalized element]] $n \in \Delta(\mathbb{N})$ with domain of definition $\mathbb{N}$ (regarded as an object of $\mathcal{T}$) is a _bounded_ sequence of integers, whereas a similarly defined [[generalized element]] $\nu \in N$ is a possibly _unbounded_ sequence of integers.  This is intuitively similar to the unbounded sequences of numbers that represent infinitely large numbers in the ultrafilter approach to [[nonstandard analysis]] (a different way of making [[infinitesimal numbers]] precise).


## The generic nonstandard number

The _generic non-standard natural number_ is the [[generalized element]] of $N$ on the domain of definition $\ell C^\infty(\mathbb{N})/{NullTail}$ given by the canonical injection $\ell C^\infty(\mathbb{N})/NullTail \to N$ that is dual to the canonical projection of the ring onto its quotient.  Here $NullTail$ is the ideal of sequences of real numbers that vanish above some integer.

The ring $C^\infty(\mathbb{N})/NullTail$ here is a quotient ring of sequences as above, where two sequences are identified if they agree above some integer. So $\ell C^\infty(\mathbb{N})/NullTail$ is the [[smooth locus]] whose function algebra is similar to a nonstandard extension of $\mathbb{R}$.

The generic non-standard natural number is discussed on page 252 of the Moerdijk-Reyes book below.


## References

See in 

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_

chapter VI -- there section 1.6 section 2 -- and chapter VII.

[[!redirects smooth natural number]]
