
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[field]] $K$ and an [[algebraic group]] $G$ over $K$, and given a [[field extension]] $k \hookrightarrow K$, then a _$k$-form_ of $G$ is an algebraic group $G_k$ over $k$ such that its [[base change]] to $K$ yields $G$:

$$
  Spec(K)\times_{Spec (k)} G_k \simeq G
  \,.
$$

Typically one requires that $G$ is also defined over $k$, hence one considers $k$-forms of the $K$-ification of a given $k$-form.

## Examples

### Multiplicative group and circle group
 {#MultiplicativeAndCircleGroup}

Consider the inclusion $\mathbb{R} \hookrightarrow \mathbb{C}$ of the [[real numbers]] into the [[complex numbers]] and let $G = \mathbb{G}_m = \mathbb{C}^\times$ be the [[multiplicative group]] hence the [[group of units]] of $\mathbb{C}$.

Then one $\mathbb{R}$-form, hence a [[real form]] of $\mathbb{G}_m$ is given by $\mathbb{R}^\times$, and another is given by the [[circle group]] $S^1 = U(1)$.

To see this, realize $\mathbb{C}^\times$ as the group of 2x2 [[matrices]] with entries in the [[complex numbers]] which are diagonal and of unit [[determinant]]:

$$
  \left(
    \array{
       x & 0
       \\
       0 & y
    }
  \right)
  \;\;\; with
  \;
  x y = 1
  \,.
$$

The same prescription over the real numbers yields $\mathbb{R}^\times$ and exhibits it as a real form of $\mathbb{C}^\times$.

On the other hand, realize the circle group as the group of 2x2 real matrices of the form

$$
  \left(
    \array{
       x & y
       \\
       -y & x
    }
 \right)
  \;\;\;\;\;
  with 
  \;
  x^2 + y^2 = 1
  \,.
$$

One checks that over the complex numbers this is isomorphic to the previous group of diagonal matrices, with the [[isomorphism]] being given by

$$
  \left(
    \array{
       x & y
       \\
       -y & x
    }
 \right)
  \mapsto
  \left(
    \array{
       x + i y & 0
       \\
       0 & x- i y
    }
  \right)
  \,.
$$

(e.g. [eom](#eom))

## Related concepts

* [[relation between compact Lie groups and reductive algebraic groups]]

## References


* David Herzog, _Forms of algebraic groups_, Proceedings of the American Mathematical Society Vol. 12, No. 4 (Aug., 1961), pp. 657-660 ([JSTOR](http://www.jstor.org/stable/2034264), [[BuzzardForms.pdf:file]])

* {#eom} [[eom]], _[Form of an algebraic group](http://www.encyclopediaofmath.org/index.php/Form_of_an_algebraic_group)_


[[!redirects forms of an algebraic group]]

[[!redirects form of a reductive algebraic group]]
[[!redirects forms of a reductive algebraic group]]