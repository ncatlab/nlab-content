
# Inner product spaces
* table of contents
{: toc}

## Idea

An __inner product space__ is a [[vector space]] $V$ equipped with a __bilinear__ or __sesquilinear form__: a linear map from $V \otimes V$ or $\bar{V} \otimes V$ to the [[ground field]] $k$.

One often studies _positive-definite_ inner product spaces; for these, see [[Hilbert space]].  Here we do not assume positivity or definiteness.


## Definitions

Let $V$ be a [[vector space]] over the [[field]] $k$.  Suppose that $k$ is equipped with an [[involution]] $r \mapsto \bar{r}$, called _conjugation_; in many examples, this will simply be the [[identity function]], but not always.  An __inner product__ on $V$ is a function
$$ \langle {-},{-} \rangle: V \times V \to k $$
that is (1--3) _sesquilinear_ (or _bilinear_ when the involution is the identity) and (4) _conjugate-symmetric_ (or _symmetric_ when the involution is the identity).  That is:

1.  $ \langle 0, x \rangle = 0 $ and $ \langle x, 0 \rangle = 0 $;
1.  $ \langle x + y, z \rangle = \langle x, z \rangle + \langle y, z \rangle $ and $ \langle x, y + z \rangle = \langle x, y \rangle + \langle x, z \rangle $;
1.  $ \langle c x, y \rangle = \bar{c} \langle x, y \rangle $ and $ \langle x, c y \rangle = c \langle x, y \rangle $;
1.  $ \langle x, y \rangle = \overline{\langle y, x \rangle} $.

Here we use the _physicist\'s convention_ that the inner product is conjugate-linear in the first variable rather than in the second, rather than the _mathematician\'s convention_, which is the reverse.  The physicist\'s convention fits in a little better with $2$-[[2-Hilbert space|Hilbert space]]s.  Note that we use the same field as values of the inner product as for [[scalars]].

(The axiom list above is rather redundant.  First of all, (1) follows from (3) by setting $c = 0$; besides that, (1--3) come in pairs, only one of which is needed, since each half follows from the other using (4).  It is even possible to derive (3) from (2) under some circumstances.)

An __inner product space__ is simply a vector space equipped with an inner product.


## Conditions on inner products

We define a function ${\|{-}\|^2}\colon V \to k$ by ${\|x\|^2} = \langle x, x \rangle$; this is called the __norm__ of $x$.  As the notation suggests, it is common to take the norm of $x$ to be the square root of this expression in contexts where that makes sense, but for us ${\|{-}\|^2}$ is an atomic symbol.  Note that the norm of $x$ is __real__ in that it equals its own conjugate, by (4).  Then we can consider some conditions on the inner product:

*  Notice that (by 1), ${\|x\|^2} = 0$ if $x = 0$; the inner product is __definite__ if the converse holds.
*  More generally, the inner product is __semidefinite__ if ...
*  On the other hand, the inner product is __indefinite__ if ...

Semidefinite inner products behave very much like definite ones; you can mod out by the elements with norm $0$ to get a [[quotient object|quotient space]] with a definite inner product.


Now suppose that $k$ (or at least, its subfield of real values) is an [[ordered field]].  Then we can consider other conditions on the inner product:

*  The inner product is __positive semidefinite__, or simply __positive__, if ${\|x\|^2} \geq 0$ always.
*  The inner product is __positive definite__ if it is both positive and definite, in other words if ${|x|^2} \gt 0$ whenever $x \ne 0$.
*  The inner product is __negative semidefinite__, or simply __negative__, if ${\|x\|^2} \leq 0$ always.
*  The inner product is __negative definite__ if it is both positive and definite, in other words if ${|x|^2} \lt 0$ whenever $x \ne 0$.

In this case, we have these theorems:

*  A semidefinite inner product is either positive or negative.
*  A definite inner product is either positive or negative definite.
*  An inner product is indefinite if and only if some norms are positive and some are negative.

Negative (semi)definite inner products behave very much like positive (semi)definite ones; you can turn one into the other by multiplying all inner products by $-1$.


The study of positive definite inner product spaces (hence essentially of all semidefinite inner product spaces over ordered fields) is essentially the study of [[Hilbert spaces]].  (For Hilbert spaces, one usually uses a [[topological field]], typically $\mathbb{C}$, and requires a completeness condition, but this does not effect the algebraic properties much.)  The study of indefinite inner product spaces is very different; see the [English Wikipedia article](http://secure.wikimedia.org/wikipedia/en/wiki/Krein_space) on [[Krein space]]s for some of it.


[[!redirects inner product]]
[[!redirects inner products]]
[[!redirects inner product space]]
[[!redirects inner product spaces]]
