A lax natural transformation is a transformation (i.e.
indexed collection of 1-cells) that commutes up to a
coherent 2-cell.

## Definition ##

Given bicategories $C,D$ and (possibly [[lax functor|lax]]) 2-functors
$F,G:C\to D$, a _lax natural transformation_ $\alpha:F\Rightarrow G$
is given by

* for each $A\in C$ a 1-cell $\alpha_A:FA\to GA$ in $D$,
as usual

* for each $f:A\to B$ in $C$ a 2-cell $\alpha_f: Gf \circ
\alpha_A \Rightarrow \alpha_B \circ Ff$

such that

* for each $A,B$, the $\alpha_f$ are the components of a
(strict) natural transformation $\alpha_{A,B}:
(\alpha_A)^* \circ G_{A,B} \dot{\to} (\alpha_B)_* \circ
F_{A,B}$

* the assignment $f\mapsto \alpha_f$ behaves sensibly with
respect to identities and composition (see the
references).

The word 'natural' is often dropped for brevity.

$\alpha$ is a _pseudo-natural_ transformation if each
$\alpha_f$ is invertible, a _strict_ one if they are
identities.  An _oplax_ transformation is as above, only
with all 2-cells reversed.  As usual, nothing significant
changes if the definitions of _lax_ and _oplax_ are
swapped.


## The Yoneda Lemma ##

Given a bicategory $C$, a lax functor $F:C\to Cat$ and $A\in C$, there
are functors

\[ I : Lax(y A,F) \stackrel{\to}{\leftarrow} F A : J \]

such that $J \dashv I$.  Here $y:C^{op} \to [C,Cat]$ is the
bicategorical Yoneda embedding, and $Lax$ denotes a 1-category of lax
transformations and [[modification]]s between them.

_Proof sketch to follow, or see Gray for the strict 2-category and
-functor case_.

## References ##

* Gray, [[Gray-adjointness-for-2-categories|Adjointness For
2-Categories]]

* Leinster, _Basic bicategories_,
[arXiv](http://arxiv.org/abs/math/9810017).

Note that both of these use somewhat outdated terminology.
