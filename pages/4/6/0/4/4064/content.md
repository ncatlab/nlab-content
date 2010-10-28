## Definition

In a (weak) [[2-category]], the appropriate notion of an [[orthogonal factorization system]] is suitably weakened up to isomorphism.  Specifically, a factorization system in a 2-category $K$ consists of two classes $(E,M)$ of 1-morphisms in $K$ such that:

1. Every 1-morphism $f:x\to y$ in $K$ is *isomorphic* to a composite $e\circ m$ where $e\in E$ and $m\in M$, and

1. For any $e:a\to b$ in $E$ and $m:x\to y$ in $M$, the following square
   $$\array{ K(b,x) & \to & K(b,y) \\
   \downarrow & \cong & \downarrow \\
   K(a,x) & \to & K(a,y)}$$
   (which commutes up to isomorphism) is a [[2-pullback]] in $Cat$.

This second property is a "2-categorical orthogonality."  In particular, it implies that any square
$$\array{a & \to & x \\
^e\downarrow & \cong & \downarrow^m \\
b & \to & y}$$
which commutes up to specified isomorphism, where $e\in E$ and $m\in M$, has a diagonal filler $b\to x$ making both triangles commute up to isomorphisms that are coherent with the given one.  It also implies an additional factorization property for 2-cells.

## Examples

The following are all factorization systems in the 2-category $Cat$.  Many of them have analogues in more general 2-categories.

* $E=$ [[essentially surjective functors]], $M=$ [[fully faithful functors]].  This is the "ur-example," and it generalizes to [[enriched category theory]], [[internal category]] theory, etc.

* $E=$ functors $e:a\to b$ such that every object of $b$ is a [[retract]] of an object in the image of $a$, and $M=$ fully faithful functors whose image is closed under retracts.

* $E=$ essentially surjective and [[full functors]], $M=$ [[faithful functors]].

* $E=$ (possibly [[transfinite compositions|transfinite]]) composites of [[localizations]], $M=$ [[conservative functors]].

## Cat-enriched factorization systems

If instead $K$ is a [[strict 2-category]] and we require that

1. Every 1-morphism in $K$ is *equal* to a composite of a morphism in $E$ and a morphism in $M$, and

1. The above square (which commutes strictly when $K$ is a strict 2-category) is a strict 2-pullback (i.e. a $Cat$-enriched pullback).

then we obtain the notion of a $Cat$-enriched, or strict 2-categorical, factorization system.

It is important to note that in general, the strict and weak notions of 2-categorical factorization system are incomparable; neither is a special case of the other.  For example, on $Cat$ there is a weak 2-categorical factorization system where $E=$ [[essentially surjective functors]] and $M=$ [[fully faithful functors]], and a strict 2-categorical factorization system where $E=$ [[bijective on objects functors]]
and $M=$ [[fully faithful functors]].

## Related pages

* Factorization systems in a 2-category play an important role in the construction of a [[proarrow equipment]] out of [[codiscrete cofibrations]].

* Combining the (eso,ff) and (eso+full, faithful) factorization systems into a [[ternary factorization system]] has connections with the theory of [[stuff, structure, property]].

[[!redirects factorization system on a 2-category]]
[[!redirects factorization systems in a 2-category]]
[[!redirects factorization systems on a 2-category]]
[[!redirects factorization systems in 2-categories]]
[[!redirects factorization systems on 2-categories]]
[[!redirects 2-categorical factorization system]]
[[!redirects 2-categorical factorization systems]]
