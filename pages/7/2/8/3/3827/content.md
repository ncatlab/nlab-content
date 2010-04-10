+--{: .standout}
Original research alert.
=--

## Idea

An **autonomous double category** is a (usually pseudo) [[double category]] which is [[monoidal double category|symmetric monoidal]], and in which every object has an assigned [[dualizable object|dual]] in the "proarrow" direction.  The basic example is the double category $\underline{Cat}$ of categories, functors, and [[profunctors]], in which the dual of a category is its [[opposite category]].

On this page, we will draw the "functor" direction horizontally and the "profunctor" direction vertically.  Thus, in an autonomous double category, every object has a vertical dual.

Note that if an autonomous double category is a [[proarrow equipment]], then its [[vertical bicategory]] is a [[symmetric monoidal bicategory]], which is moreover an [[autonomous bicategory]].  However, saying that a double category is autonomous says more than this: it says that the vertical duals are assigned in a horizontally functorial way.  Just as duals in a monoidal category are characterized up to isomorphism, duals in an autonomous bicategory are characterized up to equivalence, which in this case would mean *vertical* equivalence.  But equivalence in the bicategory $Prof$ of categories and profunctors is a weaker notion than [[equivalence of categories]], so just saying that $C^{op}$ is a dual of $C$ in $Prof$ does not characterize $C^{op}$ up to equivalence, only up to [[Morita equivalence]] (i.e. equivalence of [[Cauchy completion]]s).  The extra structure (not merely extra properties) of the autonomous double category $\underline{Cat}$ includes the specification of $C^{op}$ up to equivalence (i.e., horizontal equivalence), along with all the attendant structure.

Likewise, an **autonomous virtual double category** is a [[virtual double category]] which is autonomous in a similar sense: it has a monoidal structure and functorially assigned duals.  Note that in order to match with our conventions on this page, the role of vertical and horizontal cells in a virtual double category is flipped from the choices made at [[virtual double category]], and the cells must be transposed and have their multi-sources on the left, rather than the top.

By contrast, in a **virtually autonomous virtual double category**, the monoidal and autonomous structure has also been "virtualized": rather than coming equipped with a horizontally functorial tensor product, in such a virtual double category there are also horizontal arrows with multi-sources that are finite lists of objects with variance, such as $(A,B^{op},C)$.  We can also have a **virtually autonomous double category** which is an honest double category, but whose monoidal and autonomous structure is only virtual.

A virtually autonomous double category containing only identity vertical arrows is called an **extraordinary 2-multicategory**.  It is in some sense the "minimal" generalization of a [[2-category]] in which one can study [[extraordinary natural transformations]].  These can also be defined in any of the more algebraic structures considered above, but in general those also contain much more information than necessary merely to define extranaturals.

Finally, if an autonomous double category or virtual category is a [[proarrow equipment]] or a [[virtual equipment]], we of course call it an **autonomous (virtual) proarrow equipment**.

## Definition

Let $T$ be the "free category" monad on the [[virtual equipment]] $Span(Quiv)$ of [[spans]] in the category of [[quivers]], and let $T' = Mod(T)$ be the resulting monad on the virtual equipment $Mod(Span(Quiv)) = Cat(Quiv)$ whose objects are internal quivers in $Cat$, or equivalently internal categories in $Quiv$.  Then a (pseudo) $T'$-algebra is precisely a (pseudo) double category, while a [[virtual T-algebra]] is precisely a virtual double category.  In particular, the virtual equipment $Vdc = nKMod(Cat(Quiv),T')$ consists of virtual double categories, functors, and profunctors between them.

Let $G$ be the [[pseudomonad]] on $Cat(Quiv)$ defined as follows.  We may consider an object of $Cat(Quiv)$ as like a double category, but with only horizontal composition: there are no vertical composites or identities.  If $C$ is such, then:

* The objects of $G(C)$ are finite ordered lists of objects of $C$ with variance, such as $(x,y^{op},z,x^{op})$.  Of course, we include the empty list.

* There can exist a horizontal arrow of $G(C)$ from one list $\vec{x}$ to another $\vec{y}$ only if the two lists have the same length, say $n$.  In this case, such an arrow is given by a permutation $\sigma \in S_n$ such that the variance of $x_i$ matches the variance of $y_{\sigma (i)}$, together with for each $i$ a horizontal arrow $x_i \to y_{\sigma(i)}$ in $C$.  Composition of these is defined in the evident way using composition in $C$ and multiplying permutations.

* A vertical arrow from $\vec{x}$ to $\vec{y}$ in $G(C)$ is given by a "graph" from $\vec{x}$ to $\vec{y}$ labeled by vertical arrows of $C$, together with an ordered list of endo-vertical-arrows of $C$ (called "loops").  To be precise, by such a "graph" we mean a fixed-point-free involution of $\vec{x} \sqcup \vec{y}^{op}$ which reverses variance.  Here $\vec{y}^{op}$ means reverse the variance all through $\vec{y}$; thus if $x_i$ is matched with $y_j$, they must have the *same* variance, while if $x_i$ is matched with $x_j$, or $y_i$ with $y_j$, they must have opposite variances.

  To define a vertical arrow in $G(C)$, together with such a graph we also require, for each matched pair, a vertical arrow in $C$, according to the following rules.  If $x_i$ is matched with $y_j$ and neither is "opped," then we require a vertical arrow $x_i\to y_j$, while if both are "opped," we require instead a vertical arrow $y_j\to x_i$.  And if $x_i$ is matched with $x_j^{op}$, we require a vertical arrow $x_i\to x_j$, while if $y_i$ is matched with $y_j^{op}$, we require a vertical arrow $y_j\to y_i$.  (And, in addition to all this, we also require an ordered list of loops.)

* The squares in $G(C)$ are defined in a straightforward way, incorporating two graphs which are related by a pair of permutations, and a collection of labeling squares from $C$ with appropriately chosen boundaries.

With this definition, $G$ is evidently an endofunctor of the category of $Cat$-quivers.  We can extend it to the virtual equipment $Cat(Quiv)$ in a straightforward way, mimicking the definition above for horizontal arrows and squares to define it on the proarrows (which are like [[double profunctors]] but, again, without vertical composites).

Note that the action of $G$ on vertical arrows is very much like that of the monad on $Cat$ whose algebras are [[autonomous categories]].  The main difference is that in the latter, rather than an *ordered* list of loops (an element of the [[free monoid]] on endomorphims), we have an element of the free *commutative* monoid on the endomorphisms.  This change is what will make $G$ be only a pseudomonad, rather than a monad, but it is also crucial for the applications.

We next extend $G$ to a pseudomonad in the [[Gray-category]] of [[virtual equipments]].  The unit $C\to G(C)$ is easy to define and strictly natural: an object $x$ goes to the unary list $(x)$, horizontal arrows are labeled with the unique permutation of one element, and vertical arrows are labeled with the unique graph between two such unary lists.

The multiplication is somewhat trickier....

The multiplication defined in this way is still strictly natural, and it satisfies the laws relating it to the unit transformation strictly, but its "associativity" law is only satisfied up to isomorphism, making $G$ into a fairly strict sort of pseudomonad.

We now claim that there is a [[distributive law]] relating $T'$ to $G$, and therefore $G$ has the structure of a pseudomonad on the object $(Cat(Quiv),T')$ in the category of monads-on-virtual-equipments....

It follows by the functoriality of the construction of [[generalized multicategories]] that $G$ induces a pseudomonad $G' = nKMod(G,T')$  on the virtual equipment $Vdc = nKMod(Cat(Quiv),T')$ of virtual double categories.  Moreover, we can verify that $G'$ preserves pseudo double categories, and induces a monad $G''$ on the virtual equipment of double categories and [[double profunctors]].  Finally, we can define:

* An **autonomous double category** is a pseudo $G''$-algebra.  By general nonsense about distributive laws, this should be the same as a pseudo $G T'$-algebra, where $G T'$ is the composite pseudomonad on $Cat(Quiv)$ resulting from the distributive law.

* An **autonomous virtual double category** is a pseudo $G'$-algebra.

* A **virtually autonomous virtual double category** is a virtual $G T'$-algebra (in $Cat(Quiv)$).  I *don't* think this is quite the same as a virtual $G'$-algebra in $Vdc$.

* A **virtually autonomous double category** is a virtual $G''$-algebra.

In each of the above cases, we can replace "double category" by [[proarrow equipment]] if the (virtual) double category in question is additional a ([[virtual equipment|virtual]]) equipment.

* An **extraordinary club** is a virtually autonomous double category containing only identity vertical arrows.


## Examples

The basic example is $\underline{Cat}$, in which the objects are categories, the horizontal arrows are functors, and the vertical arrows are profunctors.  This is an autonomous proarrow equipment.  There are similar examples $V \underline{Prof}$ for any Benabou [[cosmos]] $V$.  In fact, as long as $V$ is any symmetric [[multicategory]], we can define a virtually autonomous virtual equipment $V \underline{Prof}$.

Any virtually autonomous virtual equipment has an underlying extraordinary club obtained by discarding all the non-identity vertical arrows.


## Extraordinary 2-cells

Let $C$ be a virtually autonomous virtual double category with units (it could be an equipment, or it could be an extraordinary club).  Note that the source of a general 2-cell in $C$ is a graph whose edges are labeled by composable strings of vertical arrows in $C$.  Suppose also that $f\colon \vec{x} \to z$ and $g\colon \vec{y}\to z$ are horizontal arrows in $C$.  An **extraordinary 2-cell** in $C$ is defined to be a 2-cell whose target is the unit/identity $U_z$, and whose source is a loop-free graph whose edges are all labeled by empty strings (or, equivalently, by identities).  One can verify that in $\underline{Cat}$, this reproduces the usual notion of [[extraordinary natural transformation]].


## Structures in an autonomous double category

In a (possibly virtual) autonomous double category, we can define internal notions of "closed category," "closed monoidal category," and so on.

...


## Representability

...


## References

* [Blog post](http://golem.ph.utexas.edu/category/2010/03/extraordinary_2multicategories.html) about extraordinary 2-multicategories and their ilk.

[[!redirects autonomous virtual double category]]
[[!redirects virtually autonomous double category]]
[[!redirects virtually autonomous virtual double category]]
[[!redirects autonomous double categories]]
[[!redirects autonomous virtual double categories]]
[[!redirects virtually autonomous double categories]]
[[!redirects virtually autonomous virtual double categories]]
[[!redirects compact closed double category]]
[[!redirects compact closed double categories]]
[[!redirects extraordinary club]]
[[!redirects extraordinary clubs]]
[[!redirects autonomous equipment]]
[[!redirects autonomous proarrow equipment]]
[[!redirects autonomous virtual equipment]]
[[!redirects virtually autonomous equipment]]
[[!redirects virtually autonomous proarrow equipment]]
[[!redirects virtually autonomous virtual equipment]]
