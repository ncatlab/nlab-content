<div class="rightHandSide toc">
[[!include 2-category theory - contents]]
</div>

## Idea

Recall the notion of a [[Grothendieck fibration]]: a [[functor]] $p \colon E \to B$ whose fibres $E_b$ are (contravariantly) functorial in $b \in B$.

This idea may be generalized to work in any suitable [[2-category]], although if the 2-category is not [[strict 2-category|strict]], then one has to generalize instead the non-strict notion of [[Street fibration]].  The generalized definition can be given in any of several equivalent ways, in such a way that

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

* $p \colon E \to B$ is an algebra for the [[2-monad]] $L$ on $K/B$ given by $L p = A/p$.

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

Now we connect the first three conditions with the third.  Because $K$ is finitely complete, we may form the [[tricategory]] $Span(K)$ of [[spans]] in $K$.  In particular, $K/B$ is equivalent to the hom-2-category $Span(K)(B,1)$.  Now [[comma object|recall]] that $B/p$ can be expressed as a pullback or span composite
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
_Proof_.  Write $\mathbf{\Delta}$ for the monoidal 2-category whose underlying 1-category is the [[augmented simplex category]] (q.v.) $\Delta_a$.  Recall that for $n \geq 1$ each $[n] \in \mathbf{\Delta}$ is given by the $(n-1)$-fold composite of the cospan $[1] \to [2] \leftarrow [1]$ with itself, where we take a 0-fold composite to denote the identity $[1] \to [1] \leftarrow [1]$. Recall also that the monoidal structure $[n] \oplus [m]$ on $\mathbf{\Delta}$ is generated by composing the cospans $[n],[m] \colon [1] &#x21f8; [1]$ (together with the fact that $[0],[1]$ are the initial and terminal objects).

Thus for each $n \geq 1$, there is a span $B^{[n]} \colon B &#x21f8; B$, which is canonically equivalent to the $(n-1)$-fold composite $B^{[2]} \circ B^{[2]} \circ \cdots \circ B^{[2]} \colon B &#x21f8; B$, because cotensor preserves finite limits.  For the same reason, $B^- \colon Cat^{op}_{fp} \to K$ almost restricts to a monoidal 2-functor $\mathbf{\Delta}^{op} \to Span(K)(B,B)$, except that $[0]$ does not yield a span from $B$ to $B$.  Precomposing $B^-$ with the functor $\mathbf{\Delta}^{co} \to \mathbf{\Delta}^{op}$ that sends $[n]$ to $[n+1]$, while $\delta_i \mapsto \sigma_i$ and $\sigma_i \mapsto \delta_{i+1}$ does yield a monoidal 2-functor $\mathbf{\Delta}^{co} \to Span(K)(B,B)$, which by the universal property of $\mathbf{\Delta}$ corresponds to a unique colax-idempotent monad in $Span(K)(B,B)$.

In detail, the monoid object $[0] \to [1] \leftarrow [2]$ in $\mathbf{\Delta}$ is sent to the monad $\Phi B = B^{[2]}$ in $Span(K)$, with structure maps $i = (\sigma^1_0)^* \colon B \to \Phi B$ and $c = (\delta^2_1)^* \colon \Phi B \circ \Phi B \to \Phi B$.  Moreover, because of the adjunction $\delta^2_1 \dashv \sigma^2_0 = \sigma^1_0 \oplus [1]$ in $\mathbf{\Delta}$, we have $i \circ \Phi B \dashv c$ in $Span(K)(B,B)$ with identity unit.
=--

It follows that $L = \Phi B \circ -$ is a monad, and is colax-idempotent because, for a span $H \colon B &#x21f8; A$, we have $\eta_H = i \circ H$, $\mu_H = c \circ H$, and
$$
  \eta_{L H} = i \circ \Phi B \circ H \dashv c \circ H
$$
with identity unit.  It is clear, too, that the morphism $i \colon p \to B/p$ as above is given by $\eta_{p^\circ} = i \circ p^\circ$, where $p^\circ$ denotes the obvious span $B &#x21f8; 1$.  Thus, by the definition of a [[colax-idempotent monad]], a morphism $p \colon E \to B$ carries the structure of an $L$-algebra if and only if the unit $i = \eta_{p^\circ} \colon p \to B/p$ has a right adjoint.


## References

* [[Ross Street]], Fibrations in bicategories. _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_, 21 no. 2 (1980), p. 111--160 ([numdam](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1980__21_2_111_0)).

*  Mark Weber, Yoneda structure from 2-toposes.  _Applied Categorical Structures_ 15:259--323 (2007).

[[!redirects fibrations in a 2-category]]
[[!redirects fibrations in 2-categories]]
[[!redirects internal fibration]]
[[!redirects internal fibrations]]
[[!redirects opfibration in a 2-category]]
[[!redirects opfibrations in a 2-category]]
[[!redirects opfibrations in 2-categories]]
[[!redirects internal opfibration]]
[[!redirects internal opfibrations]]
