
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Just as the notion of a [[monad]] in a [[bicategory]] $K$ generalizes that of a [[monoid]] in a [[monoidal category]], [[module|modules]] over monoids generalize easily to modules over monads.

A special case of this (see below) is often called an _algebra_ for a monad.

## Definition

Let $K$ be a bicategory and $t \colon a \to a$ a monad in $K$ with structure 2-cells $\mu \colon t t \Rightarrow t$ and $\eta \colon 1_a \Rightarrow t$.  Then a **left $t$-module** is given by a 1-cell $x \colon b \to a$ and a 2-cell $\lambda \colon t x \Rightarrow x$, where
$$
\array{
  t t x & \overset{\mu x}{\to} & t x \\
  t\lambda\downarrow & & \downarrow \lambda \\
  t x & \underset{\lambda}{\to} & x
}
\qquad \qquad
\array{
  x & \overset{\eta x}{\to} & t x \\
  & 1\searrow & \downarrow \lambda \\
  & & x
}
$$
commute.  Similarly, a **right $t$-module** is given by a 1-cell $y \colon a \to c$ and a 2-cell $\rho \colon y t \Rightarrow y$, with commuting diagrams as above with $y$ on the left instead of $x$ on the right.

Clearly, a right $t$-module in $K$ is the same thing as a left $t$-module in $K^{\mathrm{op}}$.  A **left $t$-comodule** or **coalgebra** is then a left $t$-module in $K^{\mathrm{co}}$, and a **right $t$-comodule** is a left $t$-module in $K^{\mathrm{coop}}$.

Given monads $s$ on $b$ and $t$ on $a$, an **$s,t$-bimodule** is given by a 1-cell $x\colon b \to a$, together with the structures of a right $s$-module $\rho \colon x s \Rightarrow x$ and a left $t$-module $\lambda \colon t x \Rightarrow x$ that are compatible in the sense that the diagram
$$
\array{
  t x s & \overset{t\rho}{\to} & t x \\
  \lambda s \downarrow & & \downarrow \lambda \\
  x s & \underset{\rho}{\to} & x
}
$$
commutes.  Such a bimodule may be written as $x \colon s &#8696; t$.

Every $t$-module of any of the sorts above is _a fortiori_ an [[algebra over an endomorphism|algebra over the underlying endomorphism]] $t$.

A **morphism** of left $t$-modules $(x,\lambda) \to (x',\lambda')$ is given by a 2-cell $\alpha \colon x \Rightarrow x'$ such that $\lambda' \circ t\alpha = \alpha \circ \lambda$.  Similarly, a morphism of right $t$-modules $(y,\rho) \to (y',\rho')$ is $\beta \colon y \Rightarrow y'$ such that $\rho' \circ \alpha s = \alpha \circ \rho$.  A morphism of bimodules $(x,\lambda,\rho) \to (x',\lambda',\rho')$ is given by $\alpha \colon x \Rightarrow x'$ that is a morphism of both left and right modules.

### Algebras for monads in Cat

If $K = Cat$ and $(T,\eta,\mu)$ is a monad on a category $C$, then a left $T$-module $A \colon 1 \to C$, where $1$ is the [[terminal category]], is usually called a **$T$-algebra**: it is given by an object $A \in C$ together with a morphism $\alpha \colon T A \to A$, such that
$$ \array {
  T(T(A))              & \stackrel{\mu_A}\rightarrow  & T(A) \\
  T(\alpha) \downarrow &                              & \downarrow \alpha \\
  T(A)                 & \stackrel{\alpha}\rightarrow & A
}
$$
and
$$ \array {
  A & \stackrel{\eta_A}\rightarrow  & T(A) \\
    & id_A \searrow & \downarrow \alpha \\
    &               & A
}
$$
commute.

In particular, every algebra over a monad $(T,\eta,\mu)$ in $Cat$ has the structure of an [[algebra over an endofunctor|algebra over the underlying endofunctor]] $T$.

$T$-algebras can also be defined as left [[modules]] over $T$ _qua_ monoid in $End(C)$.  There the object $A$ is represented by the constant endofunctor at $A$.

The [[Eilenberg-Moore category]] of $T$ is the category of these algebras.  It has a universal property that allows the notion of
[[Eilenberg-Moore object]] to be defined in any bicategory.


## Tensor product

Given bimodules $x' \colon r &#8696; s$ and $x \colon s &#8696; t$, where $r,s,t$ are monads on $c,b,a$ respectively, we may be able to form the **tensor product** $x \otimes_s x' \colon r &#8696; t$ just as in the case of bimodules over rings.  If the hom-categories of the bicategory $K$ have [[reflexive coequalizer]]s that are preserved by composition on both sides, then the tensor product is given by the reflexive coequalizer in $K(c,a)$
$$
\array{
  x s x' & \overset{\to}{\to} & x x' & \to x \otimes_s x'
}
$$
where the parallel arrows are the two induced actions $\rho x'$ and $x \lambda$ on $s$.  It is straightforward, though a little tedious, to show that this is an $r,t$-bimodule, the conditions following from those on $x,x'$ together with the fact that coequalizers are [[epimorphism]]s and that (because of the condition on $K$) [[whiskering]] one reflexive coequalizer diagram on either side results in another.

If $K$ satisfies the above conditions then there is a bicategory $Mod(K)$ consisting of monads, bimodules and bimodule morphisms in $K$.

## Examples

If $K = Span(Set)$, the bicategory of [[span]]s of sets, then a monad in $K$ is precisely a small category.  Then $Mod(K) = Prof$, the category of small categories, [[profunctor]]s and natural transformations.

More generally, $Mod(Span(C))$, for $C$ any category with coequalizers and pullbacks that preserve them, consists of [[internal category|internal categories]] in $C$, together with [[internal profunctor|internal profunctors]] between them and transformations between those.


## Related concepts

* **algebra over a monad**

  [[∞-algebra over an (∞,1)-monad]] 

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]] / [[model structure on simplicial T-algebras]]

* [[algebra over an operad]] 

   [[∞-algebra over an (∞,1)-operad]]

   * [[model structure on algebras over an operad]]


[[!redirects module of a monad]]
[[!redirects module for a monad]]
[[!redirects modules of a monad]]
[[!redirects modules for a monad]]
[[!redirects modules over a monad]]
[[!redirects modules for monads]]
[[!redirects modules over monads]]
[[!redirects algebra of a monad]]
[[!redirects algebra for a monad]]
[[!redirects algebra over a monad]]
[[!redirects algebras of a monad]]
[[!redirects algebras for a monad]]
[[!redirects algebras over a monad]]
[[!redirects algebras for monads]]
[[!redirects algebras over monads]]
