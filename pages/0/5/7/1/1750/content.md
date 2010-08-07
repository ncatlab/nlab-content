<div class="rightHandSide toc">
[[!include 2-category theory - contents]]
</div>

## Idea

Recall the notion of a [[Grothendieck fibration]]: it is given by a [[functor]] $p \colon E \to B$ whose fibres $E_b$ are functorial in $b \in B$.

This idea may be generalized to work in any suitable [[2-category]], in any of several equivalent ways, the most straightforward being the 'representable' definition given at [[Grothendieck fibration]].  The definitions are justified by the fact that:

+-- {: .standout #ElemFibSpecializesToCat }

When $\mathcal{K}$ is [[Cat]], fibrations in this sense are precisely [[Grothendieck fibration|Grothendieck fibrations]].

=--

## Definition

Fix a 2-category $\mathcal{K}$.  Recall that for any two morphisms $f: A \to C$ and $g: B \to C$, $f/g$ denotes their [[comma object]].  Let $f/_=g$ be their [[pullback]].

A morphism $p \colon E \to B$ in $\mathcal{K}$ is a **fibration** when any of the following holds:

* $p_* = \mathcal{K}(X,p) \colon \mathcal{K}(X,E) \to \mathcal{K}(X,B)$ is a fibration in $Cat$ for each $X \in \mathcal{K}$, and for all $f \colon Y \to X$ in $\mathcal{K}$
$$
\array{
  \mathcal{K}(X,E) & \overset{f^*}{\to} & \mathcal{K}(Y,E) \\
  \mathllap{p_*} \downarrow & & \downarrow \mathrlap{p_*} \\
  \mathcal{K}(X,B) & \overset{f^*}{\to} & \mathcal{K}(Y,B)  
}
$$
is a morphism of fibrations.

* For every morphism $f: X \to B$, the canonical map $i: f/_=p \to f/p$ has a [[right adjoint]] in the [[slice category]] $\mathcal{K} / X$.

* The canonical map $i \colon p \to B/p$ has a right adjoint in $\mathcal{K} / B$.

* $p \colon E \to B$ is an algebra for the [[2-monad]] $L$ on $\mathcal{K}/B$ given by $L p = A/p$.


## Details

Spelling out the first definition, we have that a 2-cell $\eta \colon b \to b' \colon X \to E$ is $p$-cartesian if $f^*\eta = \eta f$ is $p_*$-cartesian for every $f \colon Y \to X$. Then $p$ is a fibration in $\mathcal{K}$ if for every 2-cell $\beta \colon a \to p b$ there is a cartesian $\hat\beta \colon b' \to b$ such that $p b' = a$ and $p \hat\beta = \beta$.

The third definition is perhaps the simplest.  Of course, it is implied by the second, but the converse is also true by the pasting lemma for comma objects.

**Proposition.** _A functor $p \colon E \to B$ is a cloven fibration if and only if the canonical functor $i \colon B \to E/p$ has a right adjoint $r$ in $Cat / B$._

+-- {: .proof }
_Proof._
First, recall that the 2-category $Cat/X$ has objects the functors $C \to X$, as morphisms the commuting triangles
$$\array{C & \stackrel{h}{\to} & C' \\ & f \searrow \swarrow g &  \\  & X,  & }$$
and as 2-cells the natural transformations $\alpha : h_1 \to h_2$ such that $g\alpha = id_f$.

Next, recall that the [[comma category]] $B/p$ has objects the triples $(x, e, k)$, with $k \colon x \to p e$.  Let $\pi \colon B/p \to B$ denote the projection $(x, e, k) \mapsto x$.

The canonical morphism $p \to B/p$ is simply the inclusion functor of identity maps $i b = 1 \colon p b \to p b$.

Somewhat imprecisely, seeing both categories $E$ and $B/p$ as sitting over $B$ means that functors between those should be the identity on the $b$ component, and natural transformations should have the identity as their $b$ component.

To give an adjunction $i \dashv r$ it suffices to give, for each $k \colon x \to p e$ in $B/p$, an object $r k$ in $E$ such that $p r k = x$ and an arrow $i r k = 1_x \to k$ in $B/p$ that is [[universal arrow|universal]] from $i$ to $k$.  For the adjunction to live in $Cat/B$ we must have that $\pi \circ i r k = 1_{p r k} = 1_x$, so the universal arrow must be of the form
$$
\array{
  x & \overset{1}{\to} & x \\
  \mathllap{1} \downarrow & & \downarrow \mathrlap{p \epsilon_k} \\
  x & \underset{k}{\to} & p e
}
$$
and thus amounts to a choice of $\epsilon_k \colon r k \to e$ in $E$ such that $p \epsilon_k = k$.

The universal property of $\epsilon_k$ tells us that for any other morphism in $B/p$ from some $i y$ to $k$, i.e., for any $y$ and any pair $(f,g)$ making the square
$$
\array{
  p y & \stackrel{1}{\to} & p y \\
  \mathllap{f} \downarrow & & \downarrow \mathrlap{p g} \\
  x & \underset{k}{\to} & p e
}
$$
commute, there is a unique map $h \colon y \to r k$ in $B$ such that the above square factors in $B/p$ as
$$
\array{
  p y & \stackrel{1}{\to} & p y \\
  \mathllap{p h} \downarrow &  & \downarrow \mathrlap{p h} \\
  \mathllap{p r k =} x & \stackrel{1}{\to} & x \mathrlap{= p r k}\\
  \mathllap{1} \downarrow & & \downarrow \mathrlap{p \epsilon_k} \\
  x & \underset{k}{\to} & p e.
}
$$

In other words, the universal property provides a unique $h$ such that $\epsilon_k h = g$ and $p h = f$, which exactly asserts that $\epsilon_k$ is a [[Grothendieck fibration|cartesian]] lift of $k$.

So the existence of a right adjoint to $i$ means precisely that for each morphism $k \colon x \to p e$ a choice is given of a cartesian lift of $k$, which means in turn that $p$ is a cloven fibration.

=--

## References

* [[Ross Street]], Fibrations in bicategories. _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_, 21 no. 2 (1980), p. 111--160 ([numdam](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1980__21_2_111_0)).

*  Mark Weber, Yoneda structure from 2-toposes.  _Applied Categorical Structures_ 15:259--323 (2007).

