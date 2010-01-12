<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In every [[smooth topos]] there is a notion of [[infinitesimal object]]. In some special smooth toposes, there is in addition a notion of _invertible infinitesimal object_ and an object of _smooth natural numbers_ that contains [[generalized element]]s which are _infinite natural numbers_  that model at least parts of the axioms of [[nonstandard analysis]].

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

Therefore for domain of definition the set $\mathbb{N}$ regarded as an object of $\mathcal{T}$, a [[generalized element]] $n \in \Delta(\mathbb{N})$  is a _bounded_ sequence of intergers, whereas a [[generalized element]] $\nu \in N$ is a possibly _unbounded_ sequence of integers.

Compare this to [[nonstandard analysis]], where infinite numbers are represented by unbounded sequences of numbers.


## References

Chapter VI in,

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_

especially section 1.6 and section 2 of this chapter.