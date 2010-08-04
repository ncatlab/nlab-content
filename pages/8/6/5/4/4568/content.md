# Infinitary Lawvere theories
* table of contents
{: toc}

## Idea

An infinitary Lawvere theory is a generalisation of a [[Lawvere theory]] to allow infinitary operations.  As a motivating example, consider the theory of [[suplattices]], where we have, for every [[cardinal number]] $n$, an operation to take the [[supremum]] of $n$ elements.

Size issues can be tricky for infinitary Lawvere theories.  Na&#239;vely, you would expect an infinitary Lawvere theory of [[complete lattices]] too, but there is none, because a smallness condition fails.  (This is connected to the nonexistence of [[free complete lattices]].)

In accordance with the [[red herring principle]], an infinitary Lawvere theory should not be thought of a special case of a [[Lawvere theory]].  To avoid this, one may call the latter a *finitary* Lawvere theory.

There are also many-sorted infinitary Lawvere theories, as well as $\kappa$-ary Lawvere theories for any [[regular cardinal]] $\kappa$.


## Definitions

A __many-sorted infinitary Lawvere theory__ is a [[locally small category]] $\mathcal{D}$ with all small [[products]] and equipped with a small family $\mathcal{R}$ of objects (called __sorts__) such that every object is a small product of these sorts.

Given a small [[set]] $S$, an __$S$-sorted infinitary Lawvere theory__ is a locally small category $\mathcal{D}$ with all small products and equipped with a [[functor]] from $S$ to $\mathcal{D}$.  Note than any many-sorted infinitary Lawvere theory $(\mathcal{D},\mathcal{R})$ may be interpreted as an $S$-sorted infinitary Lawvere theory, where $S$ is the index set of the family $\mathcal{R}$.

An __unsorted infinitary Lawvere theory__ is a locally small category $\mathcal{D}$ with all small products and equipped with an object $R$ (so that $(\mathcal{D},R)$ is a [[pointed category]]) such that every object is [[isomorphic]] to $R^n$ for some small cardinal number $n$.  An __infinitary Lawvere theory__ is by default an unsorted infinitary Lawvere theory, invoking the [[red herring principle]].  Note that an unsorted infinitary Lawvery theory is the same thing as a $1$-sorted infinitary Lawvere theory.

We will give the definitions of further special cases for unsorted infinitary Lawvere theories, but these definitions may also be generalised to the many-sorted case.

Given a [[regular cardinal]] $\kappa$, a __$\kappa$-ary Lawvere theory__ is a locally small pointed category $(\mathcal{D},R)$ with all $n$-ary products for $n \lt \kappa$ such that every object is isomorphic to $R^n$ for some $n \lt \kappa$.  Every $\kappa$-ary Lawvere theory may be interpreted as an infinitary Lawvere theory by using the free category with all small products on $\mathcal{D}$.  More generally, every $\kappa$-ary Lawvere theory may be interpreted as a $\lambda$-ary Lawvere theory if $\kappa \leq \lambda$.

A __bounded infinitary Lawvere theory__ is an infinitary Lawvere theory which is (under the interpretation above) [[equivalence of categories|equivalent]] to some $\kappa$-ary Lawvere theory.

A __finitary Lawvere theory__ is a locally small pointed category $(\mathcal{D},R)$ with all finitary products such that every object is isomorphic to $R^n$ for some [[natural number]] $n$.  A __[[Lawvere theory]]__ is by default a finitary Lawvere theory, invoking the [[red herring principle]].  Note that a finitary Lawvere theory is the same thing as an $\aleph_0$-ary Lawvere theory.


## Properties

See [the n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=1673) for preliminary results.
