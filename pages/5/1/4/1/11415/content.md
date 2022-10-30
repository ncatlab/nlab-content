
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Typically, if one has a generalized [[topological space|topology]] $\mathcal{T}$ and one has an object $M$ "over" that topology (e.g. a [[sheaf]], [[bundle]] or [[stack]]) one can ask about other objects over $\mathcal{T}$ which are [[local isomorphism|locally isomorphic]] to $M$. Here, all of these terms (e.g. topology, equivalent, over) depend on the situation at hand. However, we often say than an object $M'$ which is locally isomorphic to $M$ is a _twisted form of $M$_. For some authors, the notion of being _locally isomorphic_ is only for a chosen [[cover]] $U\to X$ of an object $X$. At least for the extent of this wiki, discussion of such twisted forms will always reference the cover. In other words, to say that $M'$ is a _twisted form of $M$ over $X$_ is to say that $M$ and $M'$ are locally isomorphic for all covers. However, to say that $M'$ is a _twisted form of $M$ for $U\to X$_ would indicate that $M$ and $M'$ are only isomorphic when [[base change|pulled back]] along the given cover. 

The notion of a twisted form is very general, and has manifestations in [[differential geometry]], [[commutative algebra]], [[category theory]], [[algebraic geometry]], and more recently in [[homotopy theory]]. However, one unifying property in all of these cases is that such forms should be classified by an appropriate [[cohomology]]. Typically, this will be a sort of [[sheaf cohomology]] or [[Čech cohomology]] with coefficients in a sheaf of [[automorphisms]] of the object of interest. Moreover, computations of such cohomologies can often be simplified by identifying them as [[Galois cohomology]] or [[Hopf-Galois cohomology]]. In many cases, twisted forms are in bijection with some relevant notion of [[torsor]] for the automorphism object and when a specific cover is referenced, twisted forms are equivalent to [[descent data]] for the object along that cover.


## History

Probably the most famous twisted form computation is [[Hilbert's Theorem 90]]. That theorem can be reinterpreted as saying that for a [[Galois extension]] of fields $K\to L$, and an $L$-[[vector space]] $W$, there is exactly one $K$-vector space $V$ such that $W\cong V\otimes_K L$. In that case, the relevant [[nonabelian cohomology]] has been reinterpreted to look like [[Galois cohomology]]. [[Serre]] discussed twisted forms at some length (though he just called them "forms") in his book _Corps Locaux_. 


## Twisted forms in differential geometry

In [[differential geometry]], one often twists [[differential forms]] by a [[line bundle]]; see [differential form#twisted](differential+form#twisted).


## Twisted forms in commutative algebra

Given a [[homomorphism]] of [[commutative rings]] $\phi:R\to S$, we have an [[extension of scalars]] [[functor]] $-\otimes_R S:Mod_R\to Mod_S$. For a given $R$-[[module]] $M$, a _twisted form_ of $M$ is another $R$-module $M'$ such that $M\otimes_R S$ is [[isomorphism|isomorphic]] to $M'\otimes_R S$.  It turns out that if $\phi$ is of [[descent morphism|effective descent]] for modules, then isomorphism classes of twisted forms of a given $S$-module $N\cong M\otimes_R S$ are in [[bijection]] with the set of [[descent]] data on $N$! What's more, this set can be computed using [[nonabelian cohomology]]. 


[[!redirects twisted form]]
[[!redirects twisted forms]]
[[!redirects forme tordue]]
[[!redirects formes tordues]]
