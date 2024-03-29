
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### Monoidal prederivators

Let $Dia$ be a suitable [[2-category]] of [[diagram]] shapes, as used to define [[derivators]].  The 2-category $PDer$ of prederivators is the [[functor category|functor]] 2-category $[Dia^{op},CAT]$.  As such, it is a naturally [[cartesian monoidal category|cartesian]] [[monoidal 2-category]].

A **monoidal prederivator** is simply a [[pseudomonoid]] in $PDer$.  This is equivalent to saying that it is a pseudofunctor $Dia^{op} \to MonCat$, where $MonCat$ consists of [[monoidal categories]], strong [[monoidal functors]], and [[monoidal natural transformations]].  We may similarly define [[braided monoidal category|braided]] and [[symmetric monoidal category|symmetric]] monoidal prederivators.

A **monoidal semiderivator** is a monoidal prederivator which is a semiderivator.

### Monoidal derivators

We could define a monoidal derivator to be simply a monoidal prederivator which is a derivator.  This is what Groth does.  However, we might also want to ask that the tensor product be well-behaved with respect to homotopy Kan extensions, and the natural requirement is that it preserve homotopy colimits in each variable.

Precisely, let $D$ be a monoidal prederivator which is a derivator; we say that its tensor product **preserves homotopy colimits in each variable separately** if for any $A\in Dia$, the adjunction $r_! \colon D(A) \leftrightarrows D(*) : r^*$ is a [[Hopf adjunction]], where $r\colon A\to *$ is the unique functor to the [[terminal category]].  (Note that this is automatically a [[comonoidal adjunction]], since $r^*$ is strong monoidal.

Explicitly, this means that for any diagram $X\in D(A)$ and any object $Y\in D(*)$, the canonical transformations

$$ hocolim^A (X \otimes r^* Y) \to (hocolim^A X) \otimes Y $$
$$ hocolim^A (r^* Y\otimes X) \to Y\otimes (hocolim^A X) $$

are isomorphisms.  In this case we say that $D$ is a **monoidal derivator**.

## Properties

### Preservation of certain homotopy Kan extensions

The above preservation condition, though stated only for colimits, also applies to certain homotopy Kan extensions.  If $p\colon B\to A$ is any [[opfibration]], then we can conclude that $p_! \dashv p^*$ is also a Hopf adjunction as follows.  It suffices to show that for any $a\in A$, $X\in D(B)$, and $Y\in D(A)$, the induced transformation

$$ a^* p_! (X\otimes p^* Y) \to a^* (p_! X \otimes Y) $$

is an isomorphism (and dually).  But since $p$ is an opfibration, the square

$$ \array{ p^{-1}(a) & \overset{g}{\to} & B \\
  ^q\downarrow & & \downarrow^p \\
  * & \underset{a}{\to} & A } $$

is [[homotopy exact square|homotopy exact]].  Therefore, $a^* p_! \cong q_! g^*$, and (since the square commutes) $g^* p^* \cong q^* a^*$, so using the fact that $q_! \dashv q^*$ is Hopf, we have

$$ a^* p_! (X\otimes p^* Y)
\cong q_! g^* (X \otimes p^* Y)
\cong q_! (g^* X \otimes g^* p^* Y)
\cong q_! (g^* X \otimes q^* a^* Y)
\cong q_! g^* X \otimes a^* Y
\cong a^* p_! X \otimes a^* Y
\cong a^* (p_! X \otimes Y).
$$
We leave it to the reader to verify that this composite isomorphism is, in fact, the transformation in question.


## Examples

* Any representable prederivator represented by a monoidal category is a monoidal prederivator.  If the monoidal category is complete and cocomplete, and its tensor product preserves colimits on each side, then this is a monoidal derivator.

* The homotopy derivator of any [[monoidal model category]] is a monoidal derivator.

## References

* [[Moritz Groth]], Derivators, pointed derivators, and stable derivators ([pdf](http://www.math.uni-bonn.de/~mgroth/groth_derivators.pdf))
