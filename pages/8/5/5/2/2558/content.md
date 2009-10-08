# Idea

When $a$ and $b$ are elements of [[sets]], the __pairing__ of $a$ and $b$ is the [[ordered pair]] $(a,b)$.

It is natural to extend this to [[generalised elements]] in any [[category]] with binary [[products]].


# Definition

Let $X$ and $Y$ be [[objects]] of some [[category]] $C$, and suppose that [[the]] [[product]] $X \times Y$ exists in $C$.

Let $G$ be some object of $C$, and let $a\colon G \to X$ and $b\colon G \to Y$ be [[morphisms]] of $C$.  Then, by definition of [[product]], there exists a unique morphism $(a,b)\colon G \to X \times Y$ such that the obvious diagrams commute.

If we think of $a$ and $b$ as $G$-indexed elements of $X$ and $Y$, then $(a,b)$ is a $G$-indexed element of $X \times Y$.


# Examples

If $C$ is the [[Set|category of sets]] and $G$ is the [[point]], then $a$ and $b$ are simply elements, in the usual sense, of $X$ and $Y$; then $(a,b)$ is an element of $X \times Y$, the usual ordered pair $(a,b)$.

If $Y$ and $G$ are each $X$, with $a$ and $b$ each the [[identity morphism]] on $X$, then the pairing $(id_X,id_X)$ is the [[diagonal morphism]] $\Delta_X\colon X \to X^2$.


# Pairings versus products

Since taking the [[product]] is a [[functor]] (when defined), we can apply it to any two arbitrary morphisms.  That is, if $a\colon G \to X$ and $b\colon H \to Y$ are morphisms in a category $C$, and if the products $G \times H$ and $X \times Y$ exist, then we have a morphism $a \times b\colon G \times H \to X \times Y$.  This is *not* the pairing $(a,b)$, whose source is $G$.

A pairing is the composite of a product and a [[diagonal morphism]]:
$$ G \overset{\Delta_G}\to G \times G \overset{a \times b}\to X \times Y ;$$
conversely, a product is a pairing of two composites:
$$ \array {
   G \times H \to G \overset{a}\to X
,\\
   G \times H \to H \overset{b}\to Y
.} $$

If $G$ and $H$ are each [[terminal object|terminal]], however, then $(a,b)$ and $a \times b$ are the same [[global element]] of $X \times Y$.