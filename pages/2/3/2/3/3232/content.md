
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Just as the notion of a [[monad]] in a [[bicategory]] $K$ generalizes that of a [[monoid]] in a [[monoidal category]], [[module|modules]] over monoids generalize easily to modules over monads.

Modules over monads, especially in [[Cat]], are also often called *algebras* for the monad; see below.

The [[formal dual|formally dual]] concept is that of _[[coalgebra over a comonad]]_.

## Definition

Let $K$ be a bicategory and $t \colon a \to a$ a monad in $K$ with structure 2-cells $\mu \colon t t \Rightarrow t$ and $\eta \colon 1_a \Rightarrow t$.  Then a **left $t$-module** is given by a 1-cell $x \colon b \to a$ and a 2-cell $\lambda \colon t x \Rightarrow x$, where
$$
\array{
  t t x & \overset{\mu x}{\to} & t x \\
  t\lambda\downarrow & & \downarrow \lambda \\
  t x & \underset{\lambda}{\to} & x
}
\qquad \qquad
\array{
  x & \overset{\eta x}{\to} & t x \\
  & 1\searrow & \downarrow \lambda \\
  & & x
}
$$
commute.  Similarly, a **right $t$-module** is given by a 1-cell $y \colon a \to c$ and a 2-cell $\rho \colon y t \Rightarrow y$, with commuting diagrams as above with $y$ on the left instead of $x$ on the right.

Clearly, a right $t$-module in $K$ is the same thing as a left $t$-module in $K^{\mathrm{op}}$.  A **left $t$-comodule** or **coalgebra** is then a left $t$-module in $K^{\mathrm{co}}$, and a **right $t$-comodule** is a left $t$-module in $K^{\mathrm{coop}}$.

A $t$-module of any of these sorts is _a fortiori_ an [[algebra over an endomorphism|algebra over the underlying endomorphism]] $t$.

### Bimodules

Given monads $s$ on $b$ and $t$ on $a$, an **$s,t$-bimodule** is given by a 1-cell $x\colon b \to a$, together with the structures of a right $s$-module $\rho \colon x s \Rightarrow x$ and a left $t$-module $\lambda \colon t x \Rightarrow x$ that are compatible in the sense that the diagram
$$
\array{
  t x s & \overset{t\rho}{\to} & t x \\
  \lambda s \downarrow & & \downarrow \lambda \\
  x s & \underset{\rho}{\to} & x
}
$$
commutes.  Such a bimodule may be written as $x \colon s &#8696; t$.

A **morphism** of left $t$-modules $(x,\lambda) \to (x',\lambda')$ is given by a 2-cell $\alpha \colon x \Rightarrow x'$ such that $\lambda' \circ t\alpha = \alpha \circ \lambda$.  Similarly, a morphism of right $t$-modules $(y,\rho) \to (y',\rho')$ is $\beta \colon y \Rightarrow y'$ such that $\rho' \circ \alpha s = \alpha \circ \rho$.  A morphism of bimodules $(x,\lambda,\rho) \to (x',\lambda',\rho')$ is given by $\alpha \colon x \Rightarrow x'$ that is a morphism of both left and right modules.

More abstractly, the monads $s$ and $t$ in $K$ give rise to ordinary monads $s^*$ and $t_*$ on the hom-category $K(b,a)$, by pre- and post-composition.  The associativity isomorphism of $K$ then gives rise to an invertible [[distributive law]] between these, so that the composite $s^* t_* \cong t_* s^* \colon x \mapsto t x s$ is again a monad.  Then the category $Mod_K(s,t)$ of bimodules from $s$ to $t$ is the ordinary [[Eilenberg--Moore category]] $K(b,a)^{s^* t_*}$.


### Algebras for monads in Cat

If $K = Cat$ and $(T,\eta,\mu)$ is a monad on a category $C$, then a left $T$-module $A \colon C \to 1 \to C$, where $1$ is the [[terminal category]], is usually called a **$T$-algebra**: it is given by an object $A \in C$ together with a morphism $\alpha \colon T A \to A$, such that
$$ \array {
  T(T(A))              & \stackrel{\mu_A}\rightarrow  & T(A) \\
  T(\alpha) \downarrow &                              & \downarrow \alpha \\
  T(A)                 & \stackrel{\alpha}\rightarrow & A
}
$$
and
$$ \array {
  A & \stackrel{\eta_A}\rightarrow  & T(A) \\
    & id_A \searrow & \downarrow \alpha \\
    &               & A
}
$$
commute.

In particular, every algebra over a monad $(T,\eta,\mu)$ in $Cat$ has the structure of an [[algebra over an endofunctor|algebra over the underlying endofunctor]] $T$.

$T$-algebras can also be defined as left [[modules]] over $T$ _qua_ monoid in $End(C)$.  There the object $A$ is represented by the constant endofunctor at $A$.

The [[Eilenberg-Moore category]] of $T$ is the category of these algebras.  It has a universal property that allows the notion of
[[Eilenberg-Moore object]] to be defined in any bicategory.


## Tensor product

Given bimodules $x' \colon r &#8696; s$ and $x \colon s &#8696; t$, where $r,s,t$ are monads on $c,b,a$ respectively, we may be able to form the **tensor product** $x \otimes_s x' \colon r &#8696; t$ just as in the case of bimodules over rings.  If the hom-categories of the bicategory $K$ have [[reflexive coequalizer]]s that are preserved by composition on both sides, then the tensor product is given by the reflexive coequalizer in $K(c,a)$
$$
\array{
  x s x' & \overset{\to}{\to} & x x' & \to x \otimes_s x'
}
$$
where the parallel arrows are the two induced actions $\rho x'$ and $x \lambda$ on $s$.  Indeed, under the hypothesis on $K$ the forgetful functor $Mod_K(r,t) = K(c,a)^{r^* t_*} \to K(c,a)$ [[colimits in categories of algebras|reflects reflexive coequalizers]], because the monad $r^* t_*$ preserves them, and so $x \otimes_s x'$ is an $r,t$-bimodule.

If $K$ satisfies the above conditions then there is a bicategory $Mod(K)$ consisting of monads, bimodules and bimodule morphisms in $K$.  The identity module on a monad $t$ is $t$ itself, and the unit and associativity conditions follow from the [[universal property]] of the above coequalizer.  There is a [[lax functor|lax]] forgetful functor $Mod(K) \to K$, with comparison morphisms $1_a \to t$ the unit of $t$, and $x x' \to x \otimes_s x'$ the coequalizer map.

## Examples

If $K = Span(Set)$, the bicategory of [[span]]s of sets, then a monad in $K$ is precisely a small category.  Then $Mod(K) = Prof$, the category of small categories, [[profunctor]]s and natural transformations.

More generally, $Mod(Span(C))$, for $C$ any category with coequalizers and pullbacks that preserve them, consists of [[internal category|internal categories]] in $C$, together with [[internal profunctor|internal profunctors]] between them and transformations between those.


## Related concepts

* **algebra over a monad**, [[algebra over an endofunctor]], [[coalgebra over an endofunctor]], [[algebra over a profunctor]]

  [[∞-algebra over an (∞,1)-monad]] 

  * [[model structure on algebras over a monad]]

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]] / [[model structure on simplicial T-algebras]]

* [[algebra over an operad]] 

   [[∞-algebra over an (∞,1)-operad]]

   * [[model structure on algebras over an operad]]

## References

* [[John Isbell]], _Generic algebras_ Transactions of the AMS, vol 275, number 2 ([pdf](http://www.ams.org/journals/tran/1983-275-02/S0002-9947-1983-0682715-8/S0002-9947-1983-0682715-8.pdf))

* H. Lindner, _Commutative monads_ in _Deuxi&#233;me colloque sur l'alg&#233;bre des cat&#233;gories_. Amiens-1975. R&#233;sum&#233;s des conf&#233;rences, pages 283-288. Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle cat&#233;goriques, tome 16, nr. 3, 1975.

* R. Guitart, _Tenseurs et machines_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 21(1):5-62, 1980.

* A. Kock. _Closed categories generated by commutative monads_, Journal of the Australian Mathematical Society, 12(04):405-424, 1971.

* G. J. Seal. _Tensors, monads and actions_, Theory Appl. Categ., 28:No. 15, 403-433, 2013.

Discussion of [[model category]] structures on categories of [[coalgebras]] over [[comonads]] is in 

* [[Kathryn Hess]], [[Brooke Shipley]], _The homotopy theory of coalgebras over a comonad_ ([arXiv:1205.3979](http://arxiv.org/abs/1205.3979))


[[!redirects module of a monad]]
[[!redirects module for a monad]]
[[!redirects modules of a monad]]
[[!redirects modules for a monad]]
[[!redirects modules over a monad]]
[[!redirects modules for monads]]
[[!redirects modules over monads]]
[[!redirects algebra of a monad]]
[[!redirects algebra for a monad]]
[[!redirects algebra over a monad]]
[[!redirects algebras of a monad]]
[[!redirects algebras for a monad]]
[[!redirects algebras over a monad]]
[[!redirects algebras for monads]]
[[!redirects algebras over monads]]

[[!redirects Eilenberg-Moore algebra]]
[[!redirects Eilenberg-Moore algebras]]
