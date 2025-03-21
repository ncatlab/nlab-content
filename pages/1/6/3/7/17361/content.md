* table of contents
{: toc}

## Idea

We can generalize the notion of [[club]] over a [[cartesian monad]] on $Cat$ to a cartesian monad $S$ on an object $C$ of any [[2-category]] $K$.

Note that the $Cat$ *on* which the cartesian monad lives does not generalize to the 2-category $K$; it generalizes to the [[object]] $C$.  The 2-category $K$ generalizes the [[large category|larger]] 2-category $CAT$ that contains $Cat$ as an object.

## Definition

### The context

Let $K$ be a 2-category and $C\in K$ an object that *has representable finite limits*, meaning that each [[hom-category]] $K(X,C)$ has [[finite limits]] and the precomposition functors $(-\circ f) : K(X,C) \to K(Y,C)$ [[preserved limit|preserve]] finite limits.

Given morphisms $f,g:X\to C$, a 2-cell $\alpha:f\to g$ is called **cartesian** if for any $h,k:Y\to X$ and 2-cell $\beta:h\to k$, the commutative square
$$ \array{ f h & \overset{f \beta}{\to} & f k\\
  ^{\alpha h}\downarrow && \downarrow^{\alpha k}\\
  g h & \underset{g\beta}{\to} & g k } $$
is a pullback in $K(Y,C)$.  (Note that this is a different notion of "cartesian 2-cell" than the one involved in the notion of [[fibration in a 2-category]].)

A [[monad]] $s$ on $C$ (that is, a 1-morphism $s:C\to C$ equipped with 2-morphisms $\mu : s s\to s$ and $\eta : id_C \to s$ that are associative and unital) is **cartesian** if $\mu$ and $\eta$ are cartesian 2-cells, in the above sense, and $s$ preserves pullbacks in the sense that each functor $(s\circ -):K(X,C) \to K(X,C)$ preserves pullbacks.

### The object of collections

Now suppose that $K$ is [[cartesian closed category|cartesian closed]] --- the weak [[bicategory|bicategorical]] sense suffices, i.e. we have [[equivalences]] $K(X\times Y,Z) \simeq K(X,[Y,Z])$.  Suppose further more that $K$ has a [[terminal object]] and [[comma objects]].  To avoid confusion, we will denote by $\mathbf{1}$ the terminal object of $K$, by $id$  the identity morphisms in $K$, and by $1\in K(X,C)$ the representable terminal object of $C$.

Now any monad $s$ transposes to a morphism $\mathbf{1}\to [C,C]$, and we can form the "slice object" $[C,C]/s$ by the following comma square:
$$ \array{ [C,C]/s & \to & [C,C] \\
  \downarrow & \swArrow & \downarrow \\
  \mathbf{1} & \underset{s}{\to} & [C,C] } $$
This has the representable property that $K(X,[C,C]/s) \simeq K(X\times C,C)/s_X$, where $s_X$ is the composite $X\times C \overset{\pi_2}{\to} C \overset{s}{\to} C$.

Similarly, we have $s 1 : \mathbf{1} \to C$ (meaning the composite $\mathbf{1} \overset{1}{\to} C \overset{s}{\to} C$, where $1:\mathbf{1}\to C$ is the representable terminal object of $C$), and we can form the slice $C/s1$.  Thus has the representable property $K(X,C/s1) \simeq K(X,C)/(s1)_X$, where $(s1)_X$ is the composite $X \overset{!}{\to} \mathbf{1} \overset{s1}{\to} C$.  Now "evaluate at 1" yields a morphism $ev_1:[C,C]/s \to C/s1$, which can be defined representably in a straightforward way.

Given the assumption that $C$ has representable pullbacks as well, we claim that the morphism $ev_1$ has a right adjoint.  This can be constructed representably as follows.  A morphism $X\to C/s1$ is a morphism $a:X\to C$ together with a 2-cell $a \to (s1)_X$, and we want a morphism $b:X\times C\to C$ together with a 2-cell $b \to s_X$.  We define $b$ to be the pullback
$$ \array{ b & \to & a \pi_1\\
  \downarrow && \downarrow\\
  s_X & \to & (s1)_{X\times C} = (s1)_X \pi_1 } $$
It is straightforward to check that this defines a right adjoint whose [[counit]] is fully faithful.  It commutes with precomposition (since the pullbacks in $S$ do), so it induces a right adjoint $C/s1 \to [C,C]/s$ whose counit is also fully faithful, i.e. $C/s1$ is a "reflective subobject" of $[C,C]/s$.

Moreover, by construction, a morphism $X\to [C,C]/s$ factors through $C/s1$ just when for the corresponding map $b:X\times C\to C$, the induced square
$$ \array{ b & \to & b (id\times 1) \pi_1\\
  \downarrow && \downarrow\\
  s_X & \to & (s1)_X \pi_1 } $$
is a pullback.  Now for any $h,k:Y\to X\times C$ and $\beta:h\to k$, consider the rectangle
$$ \array{b h &\to & b k & \to & b (id \times 1) \pi_1 h\\
  \downarrow && \downarrow && \downarrow\\
  s_X h & \to & s_X k & \to & (s1)_Y \pi_1 } $$
The factorization property above says that the right-hand square and the outer rectangle are pullbacks, which by the pasting law for pullbacks implies that the left-hand square is also a pullback, i.e. that $b\to s_X$ is a cartesian 2-cell as defined above.  On the other hand, if $b\to s_X$ is a cartesian 2-cell, then precomposing with the unique 2-cell $id_C \to 1$ yields the above square.  Hence, $C/s1$ as a subobject of $[C,C]/s$ can be said to be the "full subobject consisting of the cartesian transformations into $s$".  We may call it the object of *collections* over $S$.

### The substitution product

Now, $[C,C]$ is always a [[pseudomonoid]] in $K$, and since $s$ is a monoid therein, the comma object $[C,C]/s$ inherits a pseudomonoid structure.  We claim that if $s$ is cartesian, then $C/s1$ is closed under this pseudomonoid structure, i.e. $C/s1$ is a pseudomonoid and the inclusion is a pseudomonoid morphism.

Firstly, the unit of $[C,C]/s$ is the map $\mathbf{1} \to [C,C]/s$ corresponding to $id_C$ equipped with $\eta:id_C \to s$.  Since part of $s$ being cartesian means that $\eta$ is a cartesian 2-cell, this certainly factors through $C/s1$.

Secondly, for the tensor product we again argue representably.  Suppose given two maps $X\to [C,C]/s$, corresponding to $a,b:X\times C\to C$ equipped with cartetsian 2-cells to $s_X$.  Their "product" induced by the pseudomonoid structure on $[C,C]/s$ is the composite
$$ X\times C \overset{\Delta}{\to} X\times X\times C \overset{id\times b}{\to} X\times C \overset{a}{\to} C $$
equipped with the 2-cell
$$ a (id\times b) \Delta \to s_X(id\times b)\Delta \cong s b \to s s \overset{\mu}{\to} s. $$
Then we have the composite rectangle
$$ \array{
  a (id\times b) \Delta & \to &
  s_X(id\times b)\Delta & \cong &
  s b & \to &
  s s_X & \to &
  s_X \\
  \downarrow && \downarrow && \downarrow && \downarrow && \downarrow \\
  a (id\times b) \Delta (id\times 1) \pi_1 & \to &
  s_X(id\times b)\Delta(id\times 1)\pi_1 & \cong &
  s b (id\times 1) \pi_1 & \to &
  s s_X (id \times 1) \pi_1 & \to &
  s 1
} $$
The first square on the left is a pullback since $a\to s_X$ is cartesian.  The second is an isomorphism, hence automatically a pullback.  The third is a pullback since $b\to s_X$ is cartesian and $s$ preserves pullbacks.  And the last is a pullback since $\mu:s s \to s$ is cartesian.  Thus, the composite rectangle is also a pullback, showing that $a(id\times b)\Delta \to s_X$ is also cartesian.

Note that we did not actually need $C$ to have all representable pullbacks nor $s$ to preserve all of them: we only needed the existence of pullbacks of the form
$$ \array{ b & \to & a \pi_1\\
  \downarrow && \downarrow\\
  s_X & \to & (s1)_X \pi_1 } $$
and $s$ to preserve these.

## Examples

### Clubs on Cat

When $K=CAT$, we obtain the notion of club over a cartesian monad described at [[club]].  The usual subcase of interest is when $C=Cat$, and the simple case of clubs over $\mathbf{P}$ (the permutation category) is the further special case when $s$ is the free symmetric (strict) monoidal category monad.

### Double clubs

When $K=DBLCAT$ is the 2-category of (pseudo) [[double categories]], pseudo double functors, and vertical transformations, we obtain essentially the notion of *double club* from [(Garner)](#Garner).  Representable pullbacks in $DBLCAT$ can be constructed "levelwise", by taking pullbacks in the category of objects and vertical arrows, and also in the category of (all) horizontal arrows and cells; except that in general such a pullback may not define a pseudo double functor (it may not preserve identities and composition up to isomorphism).  The condition (hps) required by Garner ensures that the *specific* pullbacks needed above do exist as pseudo double functors.  Cartesianness of monads and transformations can also be tested levelwise.

### Virtual double clubs

When $K=VEQUIP$ is the 2-category of [[virtual equipments]] (or even just [[virtual double categories]] with units) and normal (unit-preserving) functors, we obtain a notion of *virtual double club*.  The units are necessary to have a cartesian closed 2-category (specifically, we need morphisms $\mathbf{1} \to C$, where $\mathbf{1}$ is the terminal object, to correspond to objects of $C$; and without units and normality such a morphism would instead be a monoid in $C$).  However, we can do without requiring composites to exist or be preserved by functors.

This means that it suffices to assume Garner's condition (hps2) on units, but not necessarily his condition (hps1) on composites.  This is nice because in many cases, such as the double category $Cat$ of categories, functors, and profunctors, (hps2) is automatically true for all monads $s$ by [(Garner, Proposition 48)](#Garner).

On the other hand, in this context we only get that the "inclusion" $C/s1 \to [C,C]/s$ is a normal functor of virtual double categories, i.e. lax in the horizontal direction; whereas in Garner's context it is a strong functor.

## References

* [[Richard Garner]], *Double clubs*, Cahiers de Topologie et Geometrie Differentielle Categoriques 47 (2006), no. 4, 261--317; [arXiv](http://arxiv.org/abs/math/0606733)

[[!redirects double club]]
[[!redirects double clubs]]
