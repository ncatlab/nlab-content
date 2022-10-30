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

[[Finn Lawler|Finn]]:  I meant terminology and/or an explanation for arbitrary $n$ (which Urs gives below).

Actually I was thinking of functions rather than functors, as they are the 1-cells in $0-Cat$.  But of course functions are just functors between discrete categories, and thinking of them as the latter probably makes more sense when moving to higher dimensions.

_Toby_:  Now, I would either have said 'functors are indexed collections of objects' or 'functions are indexed collections of elements'; your mixture confused me!  (^_^)

_Finn_:  Ah!  Point taken.  In any case, I should have said '0-cell' instead of 'object'.  But I think 'functor' is better anyway, as I said.

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

It may be helpful to realize the same pattern in the globular context of, for instance, [[strict omega-category]]. These are certain presheaves not on the [[simplex category]] but on the [[globe category]], but the pattern is the same: the [[internal hom]] strict $\omega$-category of morphisms between strict $\omega$-categories $X$ and $Y$ is
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

[[Finn Lawler|Finn]]:  Cool!  Thanks, Urs.  I might move this section to an article on $n$-[[n-transformation|transformations]] (if that's what they're called) once I get my head around it properly.

_Toby_:  Unfortunately, '$n$-transformation' already (following '$n$-functor') means a transformation between functors between $n$-categories.  See [Cheng--Gurski](http://cheng.staff.shef.ac.uk/degeneracy/cheng-gurski-degeneracy.pdf) for this, along with '$n$-modification' and even '$n$-perturbation' (gee, that doesn\'t conflict with anything else, does it?), along with the claim that there is 'no existing terminology' thereafter.

I would probably say '$n$-morphism in $n Cat$' (possibly with two different values of $n$); you can use '$n$-cell' in place of '$n$-morphism' if you like.  But it would be nice to find something more specific that\'s not already taken.  Or we could just throw out the Cheng--Gurski meaning of '$n$-transformation'; although it\'s not unique to them, it may not be too entrenched yet.

(But please let a transformation be a $1$-transformation, even though it is a $2$-morphism.)

[[Todd Trimble|Todd]]: I think what Urs and Crans both may be suggesting is that, at least in the context of strict $n$- and $\omega$-categories, there is a uniform notion of "transformation of depth k between n-functors", or just $(n, k)$-transformations, where $(n, 1)$-transformations are usual transformations between $n$-functors, $(n, 2)$-transformations are modifications, and so on. Surely this usage won't conflict with Cheng-Gurski. 

_Toby_:  Yeah, that would work, so we could write [[(n,k)-transformation]].  My only disgruntlement is that the $n$ is superfluous; the problem is all those other people that are already using it and preventing us from unambiguously saying simply '$k$-transformation'!

_Finn_: Probably tiros like me shouldn't have a say in this sort of thing, but I would tend to agree with Toby here, that the $k$ is at least more interesting than the $n$, in that you're more likely to vary the values of $k$ than those of $n$.  However, typing the few extra characters does seem a small price to pay to avoid horrible confusion.  I slightly reluctantly vote for $(n,k)$. 

_Todd_: I'm not crazy about it either, but I agree it's a small price. I'll note (in case it helps) that in the general theory of Crans-Gray tensor products, both variations in $n$ and $k$ come up, about equally often (e.g., the tensor of a 1-category and an $n$-category is an $(n+1)$-category). 

=--


## References ##

Leinster, _Basic bicategories_,
[arXiv](http://arxiv.org/abs/math/9810017).
