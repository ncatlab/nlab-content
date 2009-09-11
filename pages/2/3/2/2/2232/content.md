In general, the _center_ (or _centre_) of an object $X$ is the collection of things which "commute with all elements of $X$."  This has a number of specific incarnations.

The original example is the __center__ $Z(G)$ of a [[group]] $G$, which is defined to be the [[subgroup]] consisting of all elements $g\in G$ such that for all elements $h\in H$ the equality $g h=h g$ holds.  The center is an [[abelian group|abelian]] subgroup, but not every abelian subgroup is in the center.  See also [[centralizer]].

The center of a group can be generalized to the center of a [[monoid]] in an obvious way.

The __center of a Lie algebra__ $L$ is an abelian Lie subalgebra $Z(L)$, consisting of all elements $ z\in L$ such that $[l,z]=0$ for all $z\in L$. There are generalizations for some other kinds of algebras.


## Centers of categories and higher categories

The centre of a monoid can be [[horizontal categorification|horizontally categorified]] to the center of a [[category]].  Specifically, the center of a category $C$ is defined to be the commutative monoid $[C,C](Id_C,Id_C)$ of [[natural transformation|endo-natural-transformations]] of the [[identity functor]] of $C$.  It is straightforward to check that this reduces to the usual definition if $C$ is a monoid, considered as a one-object category.

The notion of center can also be [[vertical categorification|vertically categorified]].  It is easy to categorify the notion of center of a category as defined above: if $C$ is an [[n-category]], then its _center_ is the monoidal $(n-1)$-category $[C,C](Id_C,Id_C)$ of endo-transformations of its identity functor.  One expects that in general, this center will actually admit a natural structure of *braided* monoidal $(n-1)$-category, just as the center of a category is actually a commutative monoid, not merely a monoid.

We can now obtain a notion of the center of a monoidal $n$-category by regarding it as a one-object $(n+1)$-category, according to the [[delooping hypothesis]].  It follows that the center of a monoidal $n$-category should naturally be a braided monoidal $n$-category.  This is known to be true when $n=0$ (the center of a monoid is a commutative monoid) and also for $n=1$ and $n=2$.

Note that a monoidal $n$-category has two different centers: if we regard it as a one-object $(n+1)$-category, then its center is a braided monoidal $n$-category, but if we regard it merely as an $n$-category, then its center is a braided monoidal $(n-1)$-category. The latter construction makes no reference to the monoidal structure. Likewise, a braided monoidal $n$-category has three different centers, depending on whether we regard it as an $n$-category, a connected $(n+1)$-category, or a 2-connected $(n+2)$-category, and so on (a $k$-tuply monoidal $n$-category has $k+1$ different centers).

It seems that in applications, however, one is usually most interested in the sort of center of a monoidal $n$-category $C$ obtained by regarding it as a one-object $(n+1)$-category, thereby obtaining a braided monoidal $n$-category.  It is in this case, and seemingly this case only, that the center comes with a natural forgetful functor to $C$, corresponding to the classical inclusion of the center of a monoid.  (For $n\gt 0$, however, this functor will not be an inclusion; the objects of the center of $C$ are objects of $C$ equipped with additional [[stuff, structure, property|structure]].)

Moreover, one expects that if we perform this "canonical" operation on a [[k-tuply monoidal n-category]] (for $k\ge 1$), the resulting braided monoidal $n$-category will actually be $(k+1)$-tuply monoidal.  This is known to be true in the cases $n\le 4$: the center of a braided monoidal category is symmetric monoidal, the center of a braided monoidal 2-category is sylleptic, and the center of a sylleptic monoidal 2-category is symmetric.

Finally, if we decategorify further, we find that the center of a [[set]] (i.e. a [[0-category]]) is a monoidal [[(-1)-category]], i.e. the [[truth value]] "true."  This is what we ought to expect, since when $C$ is a set, there is precisely one endo-transformation of its identity endofunction (namely, the identity).

+--{: .query}
[[Mike Shulman]]: It seems to me that the monoid of endofunctions of a set would be the decategorification of $[C,C]$, not $[C,C](Id_C,Id_C)$.  The center of a set should be the endotransformations _of_ the identity endofunction (of which there is only one, the identity).  Moreover, since the center of a category is a commutative monoid, and the center of a bicategory is a braided monoidal category (horizontally categorifying the center of a monoidal category), the center construction acts like a knights-move on the periodic table; thus it makes sense that the center of a set should be a symmetric monoidal $(-1)$-category, i.e. "True."

_Toby_:  I didn\'t look closely enough at your centre of a category then!  What you say here contradicts what you wrote below ---that the centre of a $k$-tuply monoidal $n$-category is a $(k+1)$-tuply monoidal $n$-category, which is my understanding--- and contradicts what [[John Baez]] writes in Section 1.1 (page 5) of [HDA1](http://math.ucr.edu/home/baez/bm2cat.ps).

[[Mike Shulman]]: I expanded it a lot; let me know if this is any better.  It's even more confusing than I realized at first.

_Toby_:  I understand it, but it still doesn\'t actually include the centre of a set (or more generally of an $n$-category) that I learnt about from HDA1.  Now, maybe that\'s not a very useful concept ... except that it fits in so well with the centre of a $k$-tuply monoidal $n$-category for $k \gt 0$!  How many of these $k + 1$ different centres that a $k$-tuply monoidal $n$-category has are used?

[[Mike Shulman]]: Hmm, that appears to be a different notion of center than the one I was used to.  (I didn't make this one up, but I don't remember where I learned it; has anyone else seen it?)  Perhaps that one is better; it also has the advantage that it gives automatically that the center of a $k$-tuply monoidal $n$-category is $(k+1)$-tuply monoidal.

_Toby_:  I\'ll try to get John\'s attention.

[[Mike Shulman]]: The HDA1 definition also leaves me wondering: why make only that particular choice of what level to stop at?  Is there anything interesting to say about other choices?

_Toby_:  H\'m, John is 'too busy' until September 22.  ('_')
=--


[[!redirects centre]]
