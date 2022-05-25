
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of [[bimodule]] makes sense [[internalization|internal]] to a [[monoidal category]] or a [[monoidal (infinity,1)-category]].

## Definition 

### As a functor into a closed monoidal category

Let $V$ be a [[closed monoidal category]]. Recall that for $C$ a category [[enriched category|enriched over]] $V$, a $C$-[[module object]] in $V$ is a $V$-functor $\rho : C \to V$. We think of the objects $\rho(a)$ for $a \in Obj(C)$ as the objects on which $C$ acts, and of $\rho(C(a,b))$ as the action of $C$ on these objects.

In this language a $C$-$D$ _bimodule object_ in $V$ for $V$-enriched categories $C$ and $D$ is a $V$-functor

$$
  C^{op} \otimes D \to V
  \,.
$$

Such a functor is also called a profunctor or [[distributor]]. Bimodule objects in $V$ can be thought of as a kind of generalized hom, giving a set of morphisms (or object of $V$) between an object of $C$ and an object of $D$.

+--{.query}
Some points are in order. Strictly speaking, the construction of $C^{op}$ from a $V$-category $C$ requires that $V$ be symmetric (or at least braided) monoidal. It's possible to define $C$-$D$-bimodule objects in $V$ without recourse to $C^{op}$, but then either that should be spelled out, or one should include a symmetry. (If the former is chosen, then closedness one on side might not be the best choice of assumption, in view of the next remark; a more natural choice might be biclosed monoidal.) 

Second: bimodule objects are not that much good unless you can compose them; for that one should add some cocompleteness assumptions to $V$ (with $\otimes$ cocontinuous in both arguments; biclosedness would ensure that), and consider smallness assumptions on the objects $C$, $D$, etc. ---Todd. 
=--

## Examples

* Let $V = Set$ and let $C = D$.  Then the hom functor $C(-, -):C^{op} \times C \to Set$ is a bimodule. 

* Let $\hat{C} = Set^{C^{op}}$; the objects of $\hat{C}$ are "generating functions" that assign to each object of $C$ a set.  Every bimodule $f:D^op \times C \to Set$ can be curried to give a Kleisli arrow $\tilde{f}:C \to \hat{D}$.  Composition of these arrows corresponds to convolution of the generating functions. 

  +--{.query}
  [[Todd Trimble|Todd]]: I am not sure what is trying to be said with regard to "convolution". I know about Day convolution, but this is not the same thing. 

  Also, with regard to "Kleisli arrow": I understand the intent, but one should proceed with caution since there is no global monad $C \mapsto \hat{C}$ to which Kleisli would refer. Again there are size issues that need attending to.
  =--

* Let $V = Vect$ and let $C = \mathbf{B}A_1$ and $D = \mathbf{B}A_2$ be two one-object $Vect$-enriched categories, whose endomorphism vector spaces are hence [[algebra]]s. Then a $C$-$D$-bimodule is a vector space $V$ with an action of $A_1$ on the left and and action of $A_2$ on the right.

## See also

* [[bimodule]]
* [[biaction]]

[[!redirects bimodule objects]]