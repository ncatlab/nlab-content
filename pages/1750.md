+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Fibrations in a 2-category

* table of contents
{: toc}

## Idea

Recall the notion of a [[Grothendieck fibration]]: a [[functor]] $p \colon E \to B$ whose fibres $E_b$ are (contravariantly) functorial in $b \in B$.

This idea may be generalized to work in any suitable [[2-category]] $K$, although if the 2-category is not [[strict 2-category|strict]], then one has to generalize instead the non-strict notion of [[Street fibration]].  The generalized definition can be given in any of several equivalent ways, in such a way that

+-- {: .standout #ElemFibSpecializesToCat }

When $K$ is [[Cat]], strict fibrations in this sense are precisely [[Grothendieck fibration|Grothendieck fibrations]], while non-strict ones are precisely [[Street fibrations]].

=--

## Definition

Fix a [[2-limit|finitely complete]] (non-strict) 2-category $K$.  Recall that for any two morphisms $f: A \to C$ and $g: B \to C$, $f/g$ denotes their [[comma object]].  Let $f/_{\cong} g$ be their [[2-pullback]].

A morphism $p \colon E \to B$ in $K$ is a (non-strict) **fibration** when the following equivalent conditions hold:

* $p_* = K(X,p) \colon K(X,E) \to K(X,B)$ is a Street fibration in $Cat$ for each $X \in K$, and for all $f \colon Y \to X$ in $K$
$$
\array{
  K(X,E) & \overset{f^*}{\to} & K(Y,E) \\
  \mathllap{p_*} \downarrow & & \downarrow \mathrlap{p_*} \\
  K(X,B) & \overset{f^*}{\to} & K(Y,B)  
}
$$
is a [[morphism of fibrations]].

* For every morphism $f: X \to B$, the canonical map $i: f/_{\cong} p \to f/p$ has a [[right adjoint]] in the [[slice 2-category]] $K / X$.

* The canonical map $i \colon p \to B/p$ has a right adjoint in $K / B$.

* $p \colon E \to B$ is an algebra for the [[2-monad]] $L$ on $K/B$ given by $L p = B/p$.

* The induced [[F-functor]] $\Sigma_p : K\swarrow E \to K\swarrow B$ between the [[lax slice 2-category|oplax slice]] [[F-categories]] has a [[lax F-adjunction|right semi-lax F-adjoint]].  (See [Johnstone](#JohnstonePP).)

If $K$ is a [[strict 2-category]] with finite strict 2-limits, then we say that $p \colon E \to B$ is a **strict fibration** when the corresponding conditions hold where "Street fibration" is replaced by "Grothendieck fibration", slice 2-categories are replaced by strict-slice 2-categories, comma objects are replaced by strict comma objects, and 2-pullbacks are replaced by strict 2-pullbacks.  In this case the 2-monad $L$ is in fact a strict 2-monad, but we do *not* require $p$ to be a *strict* algebra, only a [[pseudoalgebra]]; strict algebras for $L$ would instead be [[split fibrations]].

Note also that the *first* definition makes perfect sense regardless of whether $K$ has any limits, although this is not true of the others.

## Details

By way of spelling out the first definition, we may define a 2-cell $\eta \colon e \to e' \colon X \to E$ to be **$p$-cartesian** if $f^*\eta = \eta f$ is $p_*$-cartesian for every $f \colon Y \to X$.  Since this definition already incorporates stability under pullback, we can then say that $p$ is a fibration in $K$ if for every 2-cell $\beta \colon b \to p e$ there is a cartesian $\hat\beta \colon e' \to e$ such that $p e' = b$ and $p \hat\beta = \beta$.

The third definition is perhaps the simplest.  Of course, it is implied by the second (take $f = 1$), but the converse is also true by the pasting lemma for [[comma object|comma]] and [[pullback]] squares.

We can show that the first and third definitions are equivalent by using the representability of fibrations and adjunctions, plus the following lemma, whose proof can be found at [[Street fibration]].

+--{: .un_lemma}
###### Lemma
A functor $p \colon E \to B$ is a [[cleavage|cloven]] Street fibration if and only if the canonical functor $i \colon B \to E/p$ has a right adjoint $r$ in $Cat / B$.
=--

It follows that a morphism $p \colon E \to B$ in any 2-category $K$ is representably a fibration (i.e. satisfies the first definition) if and only if the adjunction $i \dashv r$ exists in $K/B$ (i.e. it satisfies the third condition).

Now we connect the first three conditions with the fourth.  Because $K$ is finitely complete, we may form the [[tricategory]] $Span(K)$ of [[spans]] in $K$.  In particular, $K/B$ is equivalent to the hom-2-category $Span(K)(B,1)$.  Now [[comma object|recall]] that $B/p$ can be expressed as a pullback or span composite
$$
\array{
  & & & & B/p & & & & \\
  & & & \swarrow & & \searrow & & & \\
  & & B^{\mathbf{2}} & & & & E & & \\
  & \swarrow & & \searrow &
  & \swarrow & & \searrow & \\
  B & & & & B & & & & 1
}
$$
Write $\Phi B = B^{\mathbf{2}}\rightrightarrows B$.  The functor $L \colon p \mapsto B/p$ is then given by composition: $L p =\Phi B \circ p$.  To show that $p$ is a fibration iff it is an $L$-algebra, it suffices to show

**Lemma.** _$\Phi B$ is a [[colax-idempotent monad]] in $Span(K)$ with unit $i \colon B \to B^{\mathbf{2}} = B/B$._

+-- {: .proof}
_Proof_.  Write $\mathbf{\Delta}$ for the monoidal 2-category whose underlying 1-category is the [[augmented simplex category]] (q.v.) $\Delta_a$.  Recall that for $n \geq 1$ each $[n] \in \mathbf{\Delta}$ is given by the $(n-1)$-fold composite of the cospan $[1] \to [2] \leftarrow [1]$ with itself, where we take a 0-fold composite to denote the identity $[1] \to [1] \leftarrow [1]$. Recall also that the monoidal structure $[n] \oplus [m]$ on $\mathbf{\Delta}$ is generated by composing the cospans $[n],[m] \colon [1] &#8696; [1]$ (together with the fact that $[0],[1]$ are the initial and terminal objects).

Thus for each $n \geq 1$, there is a span $B^{[n]} \colon B &#8696; B$, which is canonically equivalent to the $(n-1)$-fold composite $B^{[2]} \circ B^{[2]} \circ \cdots \circ B^{[2]} \colon B &#8696; B$, because cotensor preserves finite limits.  For the same reason, $B^- \colon Cat^{op}_{fp} \to K$ almost restricts to a monoidal 2-functor $\mathbf{\Delta}^{op} \to Span(K)(B,B)$, except that $[0]$ does not yield a span from $B$ to $B$.  Precomposing $B^-$ with the functor $\mathbf{\Delta}^{co} \to \mathbf{\Delta}^{op}$ that sends $[n]$ to $[n+1]$, while $\delta_i \mapsto \sigma_i$ and $\sigma_i \mapsto \delta_{i+1}$ does yield a monoidal 2-functor $\mathbf{\Delta}^{co} \to Span(K)(B,B)$, which by the universal property of $\mathbf{\Delta}$ corresponds to a unique colax-idempotent monad in $Span(K)(B,B)$.

In detail, the monoid object $[0] \to [1] \leftarrow [2]$ in $\mathbf{\Delta}$ is sent to the monad $\Phi B = B^{[2]}$ in $Span(K)$, with structure maps $i = (\sigma^1_0)^* \colon B \to \Phi B$ and $c = (\delta^2_1)^* \colon \Phi B \circ \Phi B \to \Phi B$.  Moreover, because of the adjunction $\delta^2_1 \dashv \sigma^2_0 = \sigma^1_0 \oplus [1]$ in $\mathbf{\Delta}$, we have $i \circ \Phi B \dashv c$ in $Span(K)(B,B)$ with identity unit.
=--

It follows that $L = \Phi B \circ -$ is a monad, and is colax-idempotent because, for a span $H \colon B &#8696; A$, we have $\eta_H = i \circ H$, $\mu_H = c \circ H$, and
$$
  \eta_{L H} = i \circ \Phi B \circ H \dashv c \circ H
$$
with identity unit.  It is clear, too, that the morphism $i \colon p \to B/p$ as above is given by $\eta_{p^\circ} = i \circ p^\circ$, where $p^\circ$ denotes the obvious span $B &#8696; 1$.  Thus, by the definition of a [[colax-idempotent monad]], a morphism $p \colon E \to B$ carries the structure of an $L$-algebra if and only if the unit $i = \eta_{p^\circ} \colon p \to B/p$ has a right adjoint.

## Properties

### The 2-fibration of fibrations

For a [[strict 2-category]] $K$, let $Fib_K$ be the 2-category of strict fibrations in $K$, morphisms of fibrations, and 2-cells between them.  Then the codomain functor $cod : Fib_K \to K$ is a strict [[2-fibration]].  (This is arguably an instance of the [[microcosm principle]].)

Similarly, for any [[bicategory]] $K$, the bicategory $Fib_K$ of weak fibrations in $K$, morphisms of fibrations, and 2-cells admits a weak 2-fibration $cod : Fib_K \to K$.

### Iterated fibrations

It is easy to show that a composite of fibrations is a fibration.  Moreover, if $Fib(X)= Fib_K(X)$ denotes the 2-category of fibrations over $X\in K$, then we have:

+--{: .num_theorem}
###### Theorem
A morphism in $Fib(X)$ is a fibration in the 2-category $Fib(X)$ iff its underlying morphism in $K$ is a fibration.
=--

This is a standard result, at least in the case $K=Cat$, and is apparently due to Benabou.  References include ([Bénabou 1985](#Benabou85)), ([Hermida 1999](#Hermida99)) and ([Jacobs 1999, Chapter 9](#Jacobs)). Therefore, for any fibration $A\to X$ in $K$ we have $Fib_K(A) \simeq Fib_{Fib_K(X)}(A\to X)$, and similarly for opfibrations.  This is a fibrational 2-categorical analogue of the standard equivalence $K/A \simeq (K/X)/(A\to X)$ for ordinary [[slice categories]].


## Related concepts

* [[Grothendieck fibration]], [[Street fibration]], [[discrete fibration]], [[two-sided fibration]]

* [[Cartesian fibration]]


## References

* [[Ross Street]], _Fibrations in bicategories_, [[Cahiers de Topologie et Géométrie Différentielle Catégoriques]], 21 no. 2 (1980), p. 111--160 ([numdam](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1980__21_2_111_0)).

*  [[Mark Weber]], _Yoneda structure from 2-toposes_,  Applied Categorical Structures **15** (2007) pp259-323. doi:[10.1007/s10485-007-9079-2](https://doi.org/10.1007/s10485-007-9079-2) ([author's page](https://sites.google.com/site/markwebersmaths/home/yoneda-structures-from-2-toposes))

* {#JohnstonePP} [[Peter Johnstone]], _Fibrations and partial products in a 2-category_, Applied Categorical Structures **1** (1993) pp141-179 doi:[10.1007/BF00880041](https://doi.org/10.1007/BF00880041)

* {#Benabou85} [[Jean Bénabou]], _Fibered categories and the foundations of naive category theory_, Journal of Symbolic Logic, **50**(1) (1985) pp10-37. doi:[10.2307/2273784](https://doi.org/10.2307/2273784), ([JSTOR](http://www.jstor.org/stable/2273784))

* {#Jacobs} [[Bart Jacobs]], _Categorical Logic and Type Theory_, Studies in Logic and the Foundations of Mathematics, 141. North-Holland Publishing Co., Amsterdam, 1999. xviii+760 pp. ISBN: 0-444-50170-3 ([pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)) ([contents](http://www.cs.ru.nl/B.Jacobs/CLT/bookinfo.html))

* {#Hermida99} [[Claudio Hermida]], _Some properties of Fib as a fibred 2-category_, Journal of Pure and Applied Algebra **134** Issue 1 (1999) pp83-109 doi:[10.1016/S0022-4049(97)00129-1](https://doi.org/10.1016/S0022-4049%2897%2900129-1), ([Core](https://core.ac.uk/display/82656524))




[[!redirects fibrations in a 2-category]]
[[!redirects fibrations in 2-categories]]
[[!redirects internal fibration]]
[[!redirects internal fibrations]]
[[!redirects opfibration in a 2-category]]
[[!redirects opfibrations in a 2-category]]
[[!redirects opfibrations in 2-categories]]
[[!redirects internal opfibration]]
[[!redirects internal opfibrations]]
