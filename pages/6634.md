
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Lax morphisms
* table of contents
{:toc}

## Idea

In general, if $A$ and $B$ are [[categories]] (or, more generally, any category-like things, such as [[objects]] of some [[2-category]]) equipped with [[algebraic structure]], a *lax morphism* $f\colon A\to B$ is one which "preserves" the algebraic structure only up to a not-necessarily invertible transformation.

Of course, this transformation goes in one particular direction; a *colax morphism* is one where the transformation goes in the other direction.  The case of 2-monads, below, provides an almost universally applicable way to decide which direction is "lax" and which is "colax".

## Definition

### For algebras of 2-monads

Let $T$ be a [[2-monad]] on a 2-category $K$, and let $A$ and $B$ be (strict, pseudo, or even lax or colax) $T$-algebras.  A **lax $T$-morphism** $f\colon A\to B$ is a morphism in $K$ together with a [[2-cell]]

$$\array{ T A & \overset{T f}{\to} & T B\\
^{a} \downarrow & \swArrow & \downarrow^{b}\\
A & \underset{f}{\to} & B}$$

satisfying some axioms.

If the 2-cell goes in the other direction, then we say $f$ is a **colax $T$-morphism** (or **oplax $T$-morphism**).  Equivalently, a colax $T$-morphism is a lax $T^{co}$-morphism, where $T^{co}$ is the induced 2-monad on the 2-cell dual $K^{co}$ (see [[opposite 2-category]]).

If the 2-cell is invertible, we call $f$ a **pseudo** or **strong** $T$-morphism.

### For coalgebras of 2-comonads

Let $W$ be a 2-comonad on $K$, i.e. a 2-monad on the 1-cell dual $K^{op}$, and let $C$ and $D$ be $W$-coalgebras.  A **lax $W$-morphism** $f\colon C\to D$ is a morphism in $K$ together with a 2-cell

$$\array{ C & \overset{T f}{\to} & D\\
^{c} \downarrow & \swArrow & \downarrow^{d}\\
W C & \underset{f}{\to} & W D}$$

satisfying some axioms.

Note that a lax morphism of algebras for the 2-comonad $W$ is a *colax* morphism of algebras for the 2-monad $W^{op}$.  The reason we choose to call this direction for coalgebras "lax" is that if $T$ is a 2-monad with a right [[adjoint functor|adjoint]] $T^*$, then $T^*$ automatically becomes a 2-comonad such that $T^*$-coalgebras are the same as $T$-algebras, and with the above definition, lax $T$-morphisms coincide with lax $T^*$-morphisms.

## Examples

* A [[lax monoidal functor]] is a lax morphism for the 2-monad on [[Cat]] whose algebras are [[monoidal categories]].  Similarly, an [[oplax monoidal functor]] is a colax morphism for this 2-monad.

* A [[lax natural transformation]] between [[2-functors]] $C\to D$ is a lax morphism for the 2-monad on $[ob(C),D]$ whose algebras are 2-functors (which exists if $D$ is cocomplete and $C$ is small).  Similarly, an oplax natural transformation is a colax morphism for this 2-monad.  If $D$ is also complete, then this 2-monad has a right adjoint, which then as usual becomes a 2-comonad whose coalgebras are also 2-functors.  The above conventions for lax morphisms between coalgebras mean that a lax natural transformation is unambiguously "lax" rather than "colax", whether we regard the 2-functors as algebras for a 2-monad or coalgebras for a 2-comonad.

  Some authors have tried to change the traditional meanings of "lax" and "colax" in this case, but the general framework of 2-monads gives a good argument for keeping it this way (even if in this particular case, oplax transformations are more common or useful).

* A [[lax functor]] between 2-categories is a lax morphism for the 2-monad on Cat-graphs whose algebras are 2-categories.

* A [[lax algebra for a 2-monad]] $T$ is a lax morphism $T\to \langle A,A\rangle$ for the 2-monad whose algebras are 2-monads, where $\langle A,A\rangle$ is the [[codensity monad]] of the object $A$.

* If $T$ is a [[lax-idempotent 2-monad]], then (by definition) *every* morphism in the underlying 2-category $K$ between (the objects underlying) $T$-algebras has a unique structure of lax $T$-morphism.  For instance, every functor between categories with (some class of) [[colimits]] is a lax morphism for the 2-monad which assigns those colimits; the unique lax structure map is the canonical comparison $colim (F\circ D) \to F(colim D)$.  Such a morphism is strong/pseudo exactly when it preserves the colimits in question.

* For [[probability monads]] on a [[locally posetal 2-category]], such as the [[Radon monad#the_ordered_case|ordered Radon monad]], the lax morphisms of algebras corresponds to [[concave maps]] or a suitable generalization thereof.


## Categories of lax morphisms

For any 2-monad $T$, there are a 2-categories:

* $T Alg_l$ of $T$-algebras and lax morphisms
* $T Alg_c$ of $T$-algebras and colax morphisms
* $T Alg_p$ (frequently written just $T Alg$) of $T$-algebras and pseudo morphisms
* (if $T$ is strict) $T Alg_s$ of $T$-algebras and strict morphisms

We have obvious 2-functors

$$ \array{ & & & & T Alg_l \\
  & & & \nearrow\\
  T Alg_s & \to & T Alg_p\\
  & & & \searrow\\
 & & & & T Alg_c }$$

which are [[bijective on objects functor|bijective on objects]], [[faithful functor|faithful]] on 1-cells, and [[locally fully faithful 2-functor|locally fully faithful]].

Therefore, we can also assemble a number of [[F-categories]] of $T$-algebras and any suitable pair of types of $T$-morphism: strict+pseudo, strict+lax, strict+colax, pseudo+lax, or pseudo+colax.

If we want to consider both lax and colax $T$-morphisms together, the natural structure is a [[double category]]: there is a straightforward definition of the squares in a double category whose vertical arrows are colax $T$-morphisms and whose horizontal arrows are lax ones.  We could then, if we wish, add some "F-ness" to incorporate pseudo and/or strict morphisms as well.

The 2-category $T Alg_p$ is fairly well-behaved; for strict $T$, it admits all strict [[PIE-limits]] (if the base 2-category does), and therefore all [[2-limits]] (i.e. bilimits).  When $T$ is [[accessible functor|accessible]], $T Alg_p$ admits all 2-colimits as well (but not, in general, many strict 2-colimits).

However, the 2-categories $T Alg_l$ and $T Alg_c$ are not so well-behaved; they do not have many limits or colimits.  But once we enhance them to [[F-categories]], they admit all [[rigged limits]].  All three 2-categories also admit [[lax morphism classifier|morphism classifiers]]; that is, the inclusions $T Alg_s \to T Alg_*$ have left 2-adjoints.


## Related pages

* [[2-monad]]

* [[lax morphism classifier]]


## References

* R. Blackwell, [[Max Kelly]], [[John Power]], _2-dimensional monad theory_, ([doi](https://doi.org/10.1016/0022-4049%2889%2990160-6))

[[!redirects lax morphisms]]
[[!redirects colax morphism]]
[[!redirects colax morphisms]]
[[!redirects oplax morphism]]
[[!redirects oplax morphisms]]
[[!redirects pseudo morphism]]
[[!redirects pseudo morphisms]]

