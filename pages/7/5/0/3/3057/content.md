In SGA I.6 [[Grothendieck]] and [[Pierre Gabriel]] presented the formalism of [[Grothendieck fibration|fibered categories]] and descent; the exposition and the terminology emphasises on a version of [[relative point of view]] for categories. Thus they start with preliminaries over the [[overcategory|slice]] [[2-category]] $Cat/C$ of functors with fixed target category $C$. Objects in $Cat/C$ are thus called **categories over $C$** and the morphisms are called **functors over $C$**. Standard passages between different slice categories are via the [[base change]] and the cobase change 2-functors. 

An important sub-2-category of $Cat/C$ is the 2-category of [[fibered categories]] over $C$; this is not a [[full subcategory|full]] sub-2-category: one restricts only to **[[cartesian functor]]s** among fibered categories. The 2-categories $Cat/C$ are fibers in a [[codomain fibration|codomain 2-fibration]] $Cat^2$ over $Cat$.

+--{: .query}
[[Mike Shulman]]: Is that really a 2-fibration?  You can pull back along $Cat/C \to Cat/D$ along a functor $f\colon D\to C$, but can you do anything with a natural transformation $f\to f'$?
=--

Its restriction to the sub-2-category $Fib$ of fibered categories is then also a Grothendieck 2-fibration $Fib\to Cat$ which has been studied by [[Claudio Hermida]]. 

* A. Grothendieck, M. Raynaud et al. _Rev&#234;tements &#233;tales et groupe fondamental_ (SGA I), Lecture Notes in Mathematics __224__, Springer 1971 (retyped as [math.AG/0206203](http://arxiv.org/abs/math/0206203))

* C. Hermida, _Some properties of $Fib$ as a fibred 2-category_, Journal of Pure and Applied Algebra __134__ (1), 83--109, 1999 (earlier draft version can be found at [jpaa.ps.gz](http://maggie.cs.queensu.ca/chermida/papers/jpaa.ps.gz))


[[!redirects categories over a category]]
[[!redirects categories over categories]]