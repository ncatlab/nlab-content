Just as a [[natural transformation]] between [[functor]]s is a
collection of $1$-cells indexed by $0$-cells, a _modification_ between
transformations is an indexed collection of 2-cells.


## Definitions ##

To be most general, start with [[lax natural transformation|lax transformations]]
$\alpha, \beta : F \dot{\to} G : C \to D$. Given those, a modification
$m : \alpha \ddot{\to} \beta$ assigns to each $0$-cell $A\in
C$ a $2$-cell $m_A : \alpha_A \Rightarrow \beta_A$ in $D$
that commutes suitably with the $2$-cell components of
$\alpha$ and $\beta$ (see Leinster for details).

If $\alpha,\beta$ are strict transformations, then the
complicated-looking modification condition becomes simply
a naturality square with globs $m_A : \alpha_A \Rightarrow
\beta_A$ where the $1$-cells $\alpha_A$ would normally be.


## Discussion ##

+-- {: .query}

[[Finn Lawler|Finn]]: There is a pattern here: functors
are indexed collections of objects, natural
transformations are i.c.s of 1-cells, modifications i.c.s
of 2-cells; and these are what make the collection of all
$n$-categories into an $n+1$-category, for $0 \leq n \leq
2$ anyway.  Any references for the pattern in higher
dimensions?

_Toby_:  Do you mean for the terminology or for the appropriate coherence laws? (the details that you\'ve been leaving out).  Not that I have either ...

Incidentally, I corrected 'function' to 'functor' in you question above; I hope that\'s OK.

[[Urs Schreiber|Urs]]: the pattern that Finn is looking for is that embodied in the nature of the [[internal hom]] of the [[closed monoidal structure on presheaves]].

In its most general form, consider an [[infinity-category]] modeled as a [[simplicial set]] with certain properties. Being a simplicial set, this is a presheaf on the [[simplex category]]. Hence for $X$ and $Y$ such $\infty$-categories, the $\infty$-category of morphisms between them corresponds to the internal hom simplicial set
$$
  [X,Y] = Hom_{SSet}(X \times \Delta^\bullet, Y)
  \,.
$$

This simple formula encodes that pattern that Finn observed. It says that:

* [[functor]]s (the 0-cells in $[X,Y]$) are just maps $X \to Y$ from cells to cells;

* [[natural transformation]]s (the 1-cells in $[X,Y]$) are maps $X \times \Delta^1 \to Y$. Notice that $\Delta^1$ is the [[interval object]] in $SSet$ (or at least its Kanification is, but never mind that for the moment). Such maps send $n$-cells in $X$ to $(n+1)$-cells in $Y$.

* modifications are maps $X \times \Delta^2 \to Y$, that map $n$-cells in $X$ to $(n+2)$-cells in $Y$.

It may be helpful to realize the same pattern in the globular context of, for instance, [[strict omega-catgeory]]. These are certain presheaves not on the [[simplex category]] but on the [[globe category]], but the pattern is the same: the [[internal hom]] strict $\omega$-category of morphisms between strict $\omega$-categories $X$ and $Y$ is
$$
  [X,Y] = Hom_{\omega Cat}(X \otimes G^\bullet , Y)
  \,,
$$
where now the tensor product appearing is no longer the cartesian one but the [[Crans-Gray tensor product]] and where $G^n$ is the standard globular $n$-globe. Again $G^1$ is a model for the [[interval object]] and we see that

* functors are morphisms $X \to Y$;

* transformations are morphisms $X \otimes G^1 \to Y$

* modifications are morphisms $X \otimes G^2 \to Y$

etc. Same logic as before.

When thinking about this, it may be useful to explicitly apply the hom-adjunction everywhere and think for instance of a natural transformation as a morphism

$$
  X \to [I,Y]
$$

from $X$ into the "category of cylinders in $Y$". This is maybe the most intuitive way: if for instance $Y$ happens to be just a 2-category, then this says that a transformation between functors between 2-categories is a 1-functor from the 1-category underlying $X$ to the category of cylinders in $Y$ (satisfying some property). Which is exactly what it is, in components.

When in a certain mood, I like to think of this basic fact, that $n$-fold transformations between $k$-functors are essentially (in components) $(k-n)$-functors with values in $n$-cylinders as the "holographic principle" in category theory. That may sound a bit silly, but it is true that in the case the $k$-functors in questions are $k$-functors on $Bord_k$ respresenting $k$-dimensional [[quantum field theory]], then teir transformations, being $(k-1)$-functors, represent $(k-1)$-dim QFT, and this relation between higher and lower dim QFT is called "holography" in phyiscs.

=--

## References ##

Leinster, _Basic bicategories_,
[arXiv](http://arxiv.org/abs/math/9810017).
