##Idea ##

This page is a spin-off of the [[structural set theory]] described at [[SEAR]]. The aim is to define (individual) natural numbers in (a fragment of) SEAR without assuming the axiom of infinity. As a result, there should be a set with $n$ elements for all $n$, but we will not have a set of all natural numbers unless we assume the axiom of infinity.

The aim is to use as few axioms/results as possible, in particular, not the result that the category of SEAR sets is a topos. What we define in the first instance is along the lines of natural numbers a la von Neumann.


## Zero and One ##

Barring opinions whether zero should be a natural number, in SEAR we have sets $\empty$ and $\mathbf{1}$ with zero and one element respectively. These follow from axioms 0, 1 and 2 at [[SEAR]].

## Two and above ##

Now assume we have defined a set $\mathbf{n}$ with $n$ elements, $1,\ldots,n$. Denote by $\underline{1},\ldots,\underline{n}$ the corresponding subsets each with one element. From axiom 3 we have a power set $P\mathbf{n}$. Let $\phi_{n+1}:\mathbf{1} \looparrowright P\mathbf{n}$ be a relation such that $\phi_{n+1}(*,\underline{i})$ for $i=1,\ldots,n$ and $\phi(*,\mathbf{n})$ where are are blurring the line between subsets of $\mathbf{n}$ and elements of $P\mathbf{n}$ (DR: someone tell me either that this is ok, or how to phrase it better). Then a tabulation of $\phi_{n+1}$ will have $n+1$ elements and we fix one of these as $\mathbf{n+1}$.

The construction on $\mathbf{1},\mathbf{2},\ldots$ only requires a fragment of SEAR, namely axioms 0,1,2 and 3, and even holds in the analogous fragment of bounded SEAR.

## Alternative approach ##

As suggested by Toby one could take as an axiom the existence of $\mathbf{2}$, together with axioms 0,1 and 2 of SEAR, instead of powersets. Then Collection gives binary coproducts, so we could define $\mathbf{n}$ as $\mathbf{1}\coprod(\mathbf{1} \coprod ( \ldots\coprod \mathbf{1})\ldots)$ ($n$ times). (DR: this needs spelling out better, with tabulations, but that's the general idea).


## Discussion ##
+--{: .query}
[[Mike Shulman]]: If you don't want to use powersets, then I'm pretty sure you'll need an axiom of coproducts.  Unless I'm mistaken, the collection of [[subsingleton]] sets satisfies Axioms 0, 1, and 2.

[[David Roberts]]: Actually what I probably mean is not use the result that $Set$ is a topos. I think you are correct on the subsingleton front, because it looks like we have no way of obtaining sets with more than one element without more axioms.

_Toby_:  If you want to be cute, you can make the existence of $\mathbf{2}$ an axiom and then get arbitrary binary coproducts using Collection.  On the other hand, if you\'re happy using power sets, then don\'t bother proving that $P\mathbf{1} = \mathbf{2}$ (which won\'t generalise to the intuitionistic case anyway); instead use Separation to carve out $\{ x \in P\mathbf{1} \;|\; x = \empty \;\vee\; x = \mathbf{1} \}$.  Then $\mathbf{3}$ is a subset of $P\mathbf{2}$, etc; or make $\mathbf{3}$ and $\mathbf{4}$ both subsets of $P\mathbf{2}$, with the general rule going logarithmically.
=--

