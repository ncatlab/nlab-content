A lax natural transformation is a transformation (i.e.
$0$-cell indexed collection of $1$-cells, like a [[natural transformation]]) that commutes up to a
coherent $2$-cell.


## Definitions ##

Given [[bicategories]] $C,D$ and (possibly [[lax functor|lax]]) $2$-[[2-functor|functors]]
$F,G:C\to D$, a _lax natural transformation_ $\alpha:F\Rightarrow G$
is given by

* for each $A\in C$ a $1$-cell $\alpha_A:F(A)\to G(A)$ in $D$,
as usual

* for each $f:A\to B$ in $C$ a 2-cell $\alpha_f: G(f) \circ
\alpha_A \Rightarrow \alpha_B \circ F(f)$

such that

* for each $A,B$, the $\alpha_f$ are the components of a
(strict) [[natural transformation]] $\alpha_{A,B}:
(\alpha_A)^* \circ G_{A,B} \dot{\to} (\alpha_B)_* \circ
F_{A,B}$

* the assignment $f\mapsto \alpha_f$ behaves sensibly with
respect to identities and composition (see the
references for details).

The word 'natural' is often dropped for brevity.

$\alpha$ is a _pseudo-natural_ transformation if each
$\alpha_f$ is [[isomorphism|invertible]], a _strict_ one if each is
an [[identity morphism|identity]].  An _oplax_ transformation is as above, only
with all 2-cells reversed.  As usual, nothing significant
changes if the definitions of _lax_ and _oplax_ are
swapped; it is a matter of convention.

+-- {: .query}
How consistent are different authors in this convention?  Should we include a warning ---or for that matter, a reassurance?  ---Toby
=--

The [[category]] $Lax(F,G)$ consists of lax transformations from $F$ to $G$ and [[modification]]s between them.


## The Yoneda Lemma ##

Given a bicategory $C$, a lax functor $F:C\to Cat$ and a $0$-cell $A\in C$, there
are [[adjoint functor]]s

\[ I : Lax(y A,F) \stackrel{\to}{\leftarrow} F(A) : J \]

such that $J \dashv I$.  Here $y A:C \to Cat$ is the image of $A$ under the
bicategorical [[Yoneda embedding]].

+-- {: .proof}
###### Proof

Sketch to follow, or see Gray for the case [[strict 2-categories]] and
strict 2-functors.
=--


## References ##

* Gray, [[Gray-adjointness-for-2-categories|Adjointness For
2-Categories]]

* Leinster, _Basic bicategories_,
[arXiv](http://arxiv.org/abs/math/9810017).

Note that both of these use somewhat outdated terminology.
