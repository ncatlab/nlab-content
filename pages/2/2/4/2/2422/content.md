##Idea ##

This page is a spin-off of the [[structural set theory]] described at [[SEAR]]. The aim is to define (individual) natural numbers in (a fragment of) SEAR without assuming the axiom of infinity. As a result, there should be a set with $n$ elements for all $n$, but we will not have a set of all natural numbers unless we assume the axiom of infinity.

The aim is to use as few axioms/results as possible, in particular, not the result that the category of SEAR sets is a topos. What we define in the first instance is along the lines of natural numbers a la von Neumann.


## Zero and One ##

Barring opinions whether zero should be a natural number, in SEAR we have sets $\empty$ and $\mathbf{1}$ with zero and one element respectively. These follow from axioms 0, 1 and 2 at [[SEAR]].

## Two and above ##

To define $\mathbf{2}$ we consider $P\mathbf{1}$. In a classical setting, this would be a two-element set, but not so for intuitionistic SEAR. We know that $\mathbf{1}$ has at least two subsets, namely $\empty$ and $\mathbf{1}$, so we let $\mathbf{2}$ be the subset of $P\mathbf{1}$ consisting of the corresponding elements. Continuing to higher numbers, we know that $\mathbf{n}$ has $n$ elements, so $n$ one-element subsets. Together with another \'obvious\' subset, this gives a set with $n+1$ elements.

More formally, let $\phi_2:\mathbf{1} \looparrowright P\mathbf{1}$ be the relation such that $\phi_2(*,empty)$ and $\phi_2(*,\mathbf{1})$. Then a tabulation $|\phi_2|$ has two elements. Let us fix one of these and call it $\mathbf{2}$.

Now assume we have defined a set $\mathbf{n}$ with $n$ elements, $1,\ldots,n$, where $n \geq 2$.  From axiom 3 we have a power set $P\mathbf{n}$. Let $\phi_{n+1}:\mathbf{1} \looparrowright P\mathbf{n}$ be a relation such that $\phi_{n+1}(*,u)$  whenever the subset $\{ i | \epsilon(i,u)\}$ of $\mathbf{n}$ has either exactly one element or is equal to all of $\mathbf{n}$.

+--{: .query}
[[Mike Shulman]]: I think it's fine, though AN might object.  A more formal thing to say would be that $\phi_{n+1}(*,u)$ whenever the subset $\{ i | \epsilon(i,u)\}$ of $\mathbf{n}$ has either exactly one element or is equal to all of $\mathbf{n}$. 

However, I don't think your definition works when $n=1$, since in that case, $\underline{1} = \mathbf{1}$!  Perhaps instead of $\phi(*,\mathbf{n})$ you want $\phi(*,\emptyset)$?

[[David Roberts]]: I've fixed the problem with $\mathbf{2}$, using Toby's original suggestion, incorporated the more formal suggestion you made for $\phi_{n+1}$ and added a new definition below.
=--

Then a tabulation of $\phi_{n+1}$ will have $n+1$ elements and we fix one of these as $\mathbf{n+1}$.

The construction on $\mathbf{1},\mathbf{2},\ldots$ only requires a fragment of SEAR, namely axioms 0,1,2 and 3, and even holds in the analogous fragment of bounded SEAR.

### Alternative definition ###

To avoid having to treat $\mathbf{2}$ as a special case, we can use another definition, again starting from $\mathbf{0},\mathbf{1}$ as before.

Assume we have defined $\mathbf{n}$ for $n \geq 1$. Then let $\psi_{n+1}:\mathbf{1} \looparrowright P\mathbf{n}$ be the relation such that $\psi_{n+1}(*,u)$ whenever the subset $\{ i | \epsilon(i,u)\}$ of $\mathbf{n}$ has either exactly one element or no elements. A tabulation $|\psi_{n+1}|$ has $n+1$ elements, and fixing one of these we denote it by $\mathbf{n+1}$.

This definition holds in the same fragment of (bounded) SEAR as described above.

+--{: .query}
[[David Roberts]]: Does this remark (about collection/power sets) belong here or in the next section? Certainly, I haven't gotten rid of power sets and I hope I haven't included collection.

[[Mike Shulman]]: I think it belongs in the next section.

_Toby_:  Sorry, I put my remarks in the wrong place!  It was late ...
=--

## Replacing the power set axiom by something else ##

As suggested by Toby, one could take as an axiom the existence of $\mathbf{2}$, together with axioms 0,1,2 and 5 (collection) of SEAR, instead of powersets (axiom 3). From Collection and $\mathbf{2}$, we get binary coproducts, so we could define $\mathbf{n}$ as $\mathbf{1}\coprod(\mathbf{1} \coprod ( \ldots\coprod \mathbf{1})\ldots)$ ($n$ times). (DR: this needs spelling out better, with tabulations, but that's the general idea).

This definition also holds in the bounded fragment of SEAR.


## With the axiom of infinity ##

> based on [this blog post](http://golem.ph.utexas.edu/category/2009/09/towards_a_computeraided_system.html#c027061) and its predecessors

To construe elements $n \in \mathbb{N}$ as giving actual finite sets, we construct a "family" $\phi\colon F \to \mathbb{N}$ where each fiber $F_n$ is a set of cardinality $n$. For example, consider the function
$$ \phi\colon \mathbb{N} \times \mathbb{N} \to \mathbb{N}\colon (m,n) \mapsto m + n + 1 $$
Then, for each $n \geq 0$, the fiber $\phi^{-1}(n)$ is a set of cardinality $n$.

If you use the Axiom of Collection, then it will do this for you automatically; you don\'t need to come up with an ad hoc representation of the family.


## Discussion ##
+--{: .query}
[[Mike Shulman]]: If you don't want to use powersets, then I'm pretty sure you'll need an axiom of coproducts.  Unless I'm mistaken, the collection of [[subsingleton]] sets satisfies Axioms 0, 1, and 2.

[[David Roberts]]: Actually what I probably mean is not use the result that $Set$ is a topos. I think you are correct on the subsingleton front, because it looks like we have no way of obtaining sets with more than one element without more axioms.

_Toby_:  If you want to be cute, you can make the existence of $\mathbf{2}$ an axiom and then get arbitrary binary coproducts using Collection.  On the other hand, if you\'re happy using power sets, then don\'t bother proving that $P\mathbf{1} = \mathbf{2}$ (which won\'t generalise to the intuitionistic case anyway); instead use Separation to carve out $\{ x \in P\mathbf{1} \;|\; x = \empty \;\vee\; x = \mathbf{1} \}$.  Then $\mathbf{3}$ is a subset of $P\mathbf{2}$, etc; or make $\mathbf{3}$ and $\mathbf{4}$ both subsets of $P\mathbf{2}$, with the general rule going logarithmically.
=--

