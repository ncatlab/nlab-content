+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

An __initial [[algebra for an endofunctor|algebra]]__ for an [[endofunctor]] $F$ on a [[category]] $C$ is an [[initial object]] in the category of [[algebra over an endofunctor|algebras]] of $F$. These play a role in particular as the [[categorical semantics]] for [[inductive types]].


## Properties

### Relation to algebras over a monad

The concept of an [[algebra of an endofunctor]] is arguably somewhat odd, a more natural concept being that of an [[algebra over a monad]].  However, the former can often be reduced to the latter.

+-- {: .num_prop}
###### Proposition
If $\mathcal{C}$ is a [[complete category]], then the [[category]] of [[algebras of an endofunctor]] $F : \mathcal{C} \to \mathcal{C}$ is [[equivalence of categories|equivalent]] to the category of [[algebras over a monad]] of the [[free monad]] on $F$, if the latter exists.
=--

The proof is fairly straightforward, see for instance ([Maciej](#Maciej)) or at [[free monad]].

The existence of free monads, on the other hand, can be a tricky question.  One general technique is the [[transfinite construction of free algebras]].


### Lambek's theorem
 {#LambeksTheorem}

+-- {: .num_theorem}
###### Theorem

If $F$ has an initial algebra $\alpha: F(X) \to X$, then $X$ is [[isomorphism|isomorphic]] to $F(X)$ via $\alpha$. 
=--


+-- {: .num_remark}
###### Remark

In this sense, $X$ is a fixed point of $F$.  Being initial, $X$ is the *smallest* fixed point of $F$ in that there is a map from $X$ to any other fixed point (indeed, any other algebra), and this map is an [[injection]] if $C$ is [[Set]]. 
=--

+-- {: .num_remark}
###### Remark

The dual concept is [[terminal coalgebra]], which is the *largest* fixed point of $F$.
=--

+-- {: .proof}
###### Proof

Given an initial algebra structure $\alpha: F(X) \to X$, define an algebra structure on $F(X)$ to be $F(\alpha): F(F(X)) \to F(X)$. By initiality, there exists an $F$-algebra map $i: X \to F(X)$, so that 

$$\array{
F(X) & \overset{F(i)}{\to} & F(F(X)) \\
\alpha \downarrow & & \downarrow F(\alpha) \\
X & \underset{i}{\to} & F(X)
}$$ 

commutes. Now it is trivial, in fact tautological that $\alpha$ is itself an $F$-algebra map $F(X) \to X$. Thus $\alpha \circ i = 1_X$, since both sides of the equation are $F$-algebra maps $X \to X$ and $X$ is initial. As a result, $F(\alpha) \circ F(i) = 1_{F(X)}$, so that $i \circ \alpha = 1_{F(X)}$ according to the commutative square. Hence $\alpha$ is an isomorphism, with inverse $i$.
=--


### Ad&#225;mek's theorem
 {#AdameksTheorem-sec}

In many cases, initial algebras can be constructed in a [[recursion|recursive]] fashion, using the following special case of a theorem due to Ad&#225;mek (although, the same construction for set-functors already appeared in ([Pohlova,1973](#Pohlova))).

+-- {: .num_theorem #AdameksTheorem }
######Theorem (Ad&#225;mek)

Let $C$ be a category with an [[initial object]] $0$ and [[transfinite composition]] of length $\omega$, hence [[colimits]] of sequences $\omega \to C$ (where $\omega$ is the first infinite [[ordinal]]), and suppose $F: C \to C$ preserves colimits of $\omega$-chains. Then the colimit $\gamma$ of the chain 

$$0 \overset{i}{\to} F(0) \overset{F(i)}{\to} \ldots \to F^{(n)}(0) \overset{F^{(n)}(i)}{\to} F^{(n+1)}(0) \to \ldots$$ 

carries a structure of initial $F$-algebra. 
=-- 

+-- {: .proof}
###### Proof

The $F$-algebra structure $F\gamma \to \gamma$ is inverse to the canonical map $\gamma \to F\gamma$ out of the colimit (which is invertible by the hypothesis on $F$). The proof of initiality may be extracted by dualizing the corresponding proof given at [[terminal coalgebra]]. 
=--

This approach can be generalized to the [[transfinite construction of free algebras]].


### Semantics for inductive types

Initial algebras of endofunctors provide [[categorical semantics]] for [[extensional type theory|extensional]] [[inductive types]].
The generalization to [[weak initial]] algebras captures the notion in [[intensional type theory]] and [[homotopy type theory]]. 


## Examples

### Natural numbers
 {#NaturalNumbers}

The archetypical example of an initial algebra is the set of [[natural numbers]].  

+-- {: .num_prop}
###### Proposition

Let $\mathcal{T}$ be  [[topos]] and let $F : \mathcal{T} \to \mathcal{T}$ the functor given by

$$
  F : X \mapsto * \coprod X
$$

(i.e. the functor underlying the "[[maybe monad]]").
Then an initial algebra over $F$ is precisely a [[natural number object]] $\mathbb{N}$ in $\mathcal{T}$. 
=--

+-- {: .proof}
###### Proof

By definition, an $F$-algebra is an object $X$ equipped with a morphism

$$
  (0,s) :  * \coprod X \to X
  \,,
$$

hence equivalently with a [[pointed object|point]] $0 : * \to X$ and an [[endomorphism]] $s : X \to X$. Initiality means that for any other $F$-algebra $(0_Y, s_Y) : * \coprod Y \to Y$, there is a unique morphism $f : X \to Y$ such that the [[diagram]]

$$
  \array{
    * &\stackrel{0}{\to}& X &\stackrel{s}{\to}& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{f}}
    \\
    * &\stackrel{0}{\to}& Y &\stackrel{s}{\to}& Y  
  }
$$

commutes. This is the very definition of [[natural number object]] $X = \mathbb{N}$.
=--

### Bi-pointed sets

Another example of an initial algebra is the [[bi-pointed set]] $\mathbf{2}$.  

+-- {: .num_prop}
###### Proposition

Let $\mathcal{T}$ be  [[topos]] and let $F : \mathcal{T} \to \mathcal{T}$ the functor given by

$$
  F : X \mapsto * \coprod *
$$


Then an initial algebra over $F$ is precisely a [[bi-pointed object]] $\mathbf{2}$ in $\mathcal{T}$. 
=--

### More examples

Theorem \ref{AdameksTheorem} applies (in particular) to any functor $F: Set \to Set$ which is a [[colimit]] of finitely [[representable functors]] $hom(n, -): X \mapsto X^n$, as in the following examples. 
 

* Let $A$ be a set, and let $F: Set \to Set$ be the functor $F(X) = 1 + A \times X$. Then the initial $F$-algebra is $A^*$, the [[free monoid]] on $A$. The $F$-algebra structure is 
  $$(e, m| ): 1 + A \times A^* \to A^*$$ 
  where $e: 1 \to A^*$ is the identity and $m|: A \times A^* \to A^*$ is the restriction of the monoid multiplication along the evident inclusion $i \times 1: A \times A^* \to A^* \times A^*$. 

  This "fixed point" of $F$ can be thought of as the result of the (slightly nonsensical) calculation 
  $$1 + A \times X = X \Rightarrow X = \frac1{1 - A} = 1 + A + A^2 + \ldots = A^*$$ 
  which can be made rigorous by interpreting the initial equality as defining the solution $X$ by recursion, and applying the theorem above. 

* Let $F: Set \to Set$ be the functor $F(X) = 1 + X^2$. Then the initial $F$-algebra is the set $T$ of isomorphism classes of finite (planar, rooted) binary [[trees]]. The $F$-algebra structure is 
  $$(r, j): 1 + T^2 \to T$$ 
  where $r: 1 \to T$ names the tree consisting of just a root vertex, and $j: T^2 \to T$ creates a tree $t \vee t'$ from two trees $t$, $t'$ by joining their roots to a new root, so that the root of $t$ becomes the left child and the root of $t'$ the right child of the new root. 

  The recursive equation 
  $$T = 1 + T^2$$ 
  would seem to imply that the structure $T$ behaves something like a structural "sixth root of unity", and indeed the structural isomorphism $T \cong F(T)$ allows one to exhibit an isomorphism 
  $$T = T^7$$ 
  constructively, as famously explored by Andreas Blass in the paper "[[Seven trees in one]]". 


* Let $F: Set \to Set$ be the functor $F(X) = X^*$ (the free monoid from an earlier example). Then the initial $F$-algebra is the set of isomorphism classes of finite planar rooted [[trees]] (not necessarily binary as in the previous example). 

* Let $C$ be the [[coslice category]] $\mathbb{Z} \downarrow Ab$, and let $F: C \to C$ be the functor which pushes out along the multiplication-by-$p$ map $p \cdot -: \mathbb{Z} \to \mathbb{Z}$. Then the initial $F$-algebra is the [[Pruefer group]] $\mathbb{Z}[p^{-1}]/\mathbb{Z}$. See the discussion at the n-Category Caf&#233;, starting [here](http://golem.ph.utexas.edu/category/2008/11/coalgebraically_thinking.html#c020660). 

* Let $Ban$ be the category of complex [[Banach spaces]] and maps of [[norm]] bounded above by $1$, and let $F: \mathbb{C} \downarrow Ban \to \mathbb{C} \downarrow Ban$ be the squaring functor $X \mapsto X \times X$. Then the initial $F$-algebra is $L^1([0, 1])$ (with respect to the usual [[Lebesgue measure]]). This result is due to [[Tom Leinster]]; see this [MathOverflow discussion](http://mathoverflow.net/questions/23143/what-theorem-constructs-an-initial-object-for-this-category-formerly-integrabi/78262#78262). 


## Related entries

* [[inductive type]]

* [[inductive-recursive type]],  [[algebraically compact category]]

* [[higher inductive type]], [[initial algebra of a presentable ∞-monad]]


## References

A textbook account of the basic theory is in [Chapter 10](http://www.andrew.cmu.edu/course/80-413-713/notes/chap10.pdf) of

* [[Steve Awodey]], _Category theory_ lecture notes (2011) ([web](http://www.andrew.cmu.edu/course/80-413-713/))

A brief review of some basics, with an eye towards [[inductive types]], is in Section 2 of

* {#AwodeyGambinoSojakova} [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], *Inductive types in homotopy type theory* ([arXiv:1201.3898](http://arxiv.org/abs/1201.3898))
 

The relation to [[homotopy type theory]] is discussed in

* [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], _Homotopy-initial algebras in type theory_ ([arXiv:1504.05531](http://arxiv.org/abs/1504.05531))

The relation to [[free monads]] is discussed in 

* {#Maciej} [Maciej](http://maciejcs.wordpress.com/), _[Free monads and their algebras](http://maciejcs.wordpress.com/2012/04/17/free-monads-and-their-algebras/)_

Original references on initial algebras include

* {#Pohlova} Věra Pohlová. "On sums in generalized algebraic categories." Czechoslovak Mathematical Journal 23.2 (1973): 235-251. <http://eudml.org/doc/12718>.
* Jiří Adámek. "Free algebras and automata realizations in the language of categories." Commentationes Mathematicae Universitatis Carolinae 15.4 (1974): 589-602.
* Jiří Adámek, Věra Trnková. Automata and algebras in categories. Vol. 37. Springer Science & Business Media, 1990.


[[!redirects initial algebras of an endofunctor]]
[[!redirects initial algebras of endofunctors]]

[[!redirects initial algebra for an endofunctor]]
[[!redirects initial algebras for an endofunctor]]
[[!redirects initial algebras for endofunctors]]

[[!redirects initial algebra over an endofunctor]]
[[!redirects initial algebras over an endofunctor]]
[[!redirects initial algebras over endofunctors]]