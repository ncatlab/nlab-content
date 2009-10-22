
#Contents#
* automatic table of contents goes here
{:toc}

#Definition#

Let $V$ be a [[closed monoidal category]]. Recall that for $C$ a category [[enriched category|enriched over]] $V$, a $V$-[[module]] is a $V$-functor $\rho : C \to V$. We think of the object $\rho(a)$ for $a \in Obj(C)$ as the objects on which $C$ acts, and of $\rho(C(a,b))$ as the action of $C$ on these objects.

In this language a $C$-$D$ _bimodule_ for $V$-categories $C$ and $D$ is a $V$-functor

$$
  C^{op} \otimes D \to V
  \,.
$$

Such a functor is also called a profunctor or [[distributor]].

+--{.query}
Some points are in order. Strictly speaking, the construction of $C^{op}$ from a $V$-category $C$ requires that $V$ be symmetric (or at least braided) monoidal. It's possible to define $C$-$D$ bimodules without recourse to $C^{op}$, but then either that should be spelled out, or one should include a symmetry. (If the former is chosen, then closedness one on side might not be the best choice of assumption, in view of the next remark; a more natural choice might be biclosed monoidal.) 

Second: bimodules are not that much good unless you can compose them; for that one should add some cocompleteness assumptions to $V$ (with $\otimes$ cocontinuous in both arguments; biclosedness would ensure that), and consider smallness assumptions on the objects $C$, $D$, etc. ---Todd. 
=--

#Examples#

* Let $V = Set$ and let $C = D$.  Then the hom functor $C(-, -):C^{op} \times C \to Set$ is a bimodule.  Bimodules can be thought of as a kind of generalized hom, giving a set of morphisms (or object of $V$) between an object of $C$ and an object of $D$.

* Let $\hat{C} = Set^{C^{op}}$; the objects of $\hat{C}$ are "generating functions" that assign to each object of $C$ a set.  Every bimodule $f:D^op \times C \to Set$ can be curried to give a Kleisli arrow $\tilde{f}:C \to \hat{D}$.  Composition of these arrows corresponds to convolution of the generating functions. 

  +--{.query}
  [[Todd Trimble|Todd]]: I am not sure what is trying to be said with regard to "convolution". I know about Day convolution, but this is not the same thing. 

  Also, with regard to "Kleisli arrow": I understand the intent, but one should proceed with caution since there is no global monad $C \mapsto \hat{C}$ to which Kleisli would refer. Again there are size issues that need attending to.
  =--

* Let $V = Vect$ and let $C = \mathbf{B}A_1$ and $D = \mathbf{B}A_2$ be two one-object $Vect$-enriched categories, whose endomorphism vector spaces are hence [[algebra]]s. Then a $C$-$D$ bimodule is a vector space $V$ with an action of $A_1$ on the left and and action of $A_2$ on the right.

[[!redirects bimodules]]