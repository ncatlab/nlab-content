
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[constructive mathematics]], the [[law of double negation]] doesn't hold, which means that the notion of [[negation]] doesn't have the same properties as that in [[classical mathematics]]. The usual notion of negation of a [[proposition]] $P$ says that $P$ is *negated* or *false* if and only if $P$ implies [[falsehood]], $\neg P \iff P \Rightarrow \bot$. But there is also a stronger notion of negation: The **strong negation** of $P$, if it exists, is a proposition $Q$ such that $P$ holds if and only if $Q$ is negated $P \iff (Q \Rightarrow \bot)$. $P$ is **strongly negated** or **strongly false** if the strong negation $Q$ holds ($Q \iff \top$). Since every propostion $P$ still implies its [[double negation]], $P$ being strongly negated still implies $P$ being negated in the usual sense. 

For example, there are two different notions of [[inequality]] in the [[real numbers]] in [[constructive analysis]]: there is the usual [[denial inequality]] $\neq$ defined by the usual constructive [[negation]] of [[equality]] $x \neq y \iff (x = y) \Rightarrow \bot$, and then there is a strong inequality $\#$ defined by the [[disjunction]] of the order relations $x \lt y$ and $y \lt x$, $x \# y \iff (x \lt y) \vee (y \lt x)$, which is a strong negation of equality in the sense that $x = y$ if and only if $x \# y$ is false. As a result, there are two ways to define, for instance, an [[irrational number]]: a weak version which uses the usual [[denial inequality]] with every [[rational number]], and a strong version which uses the strong inequality with every rational number. 

### The antithesis interpretation

In the [[antithesis interpretation]] of [[intuitionistic logic]], the strong negation of a proposition correspond to the negation of a [[refutative proposition]] in [[affine logic]]. Compare with the usual notion of [[negation]] of a proposition, which correspond to the negation of an [[affirmative proposition]] in [[affine logic]]. 

The notion of [[strong negation]] is also important in giving examples of the [[antithesis interpretation]] of [[intuitionistic logic]]. In much of constructive mathematics, statements of interest seem to come in pairs, a statement $P^+$ that amounts to a constructive version of a well-known statement $P^{\mathrm{C}}$ from [[classical mathematics]], and a statement $P^-$ that amounts to a constructive version of $\neg{P^{\mathrm{C}}}$, and which is equivalent to $\neg{P^+}$ in [[classical logic]], but which is not the same as $\neg{P^+}$ in [[intuitionistic logic]], and similarly for $P^+$ vis-a-vis $\neg{P^-}$.

For example, suppose there are predicates $P_0$ and $P_1$ each with strong negations $Q_0$ and $Q_1$. In the antithesis interpretation, there are two statements $P^+$ and $P^-$ one can make about these: 

* $P^+$ states that $P_0$ holds or $P_1$ holds, $P_0 \vee P_1$

* $P^-$ states that $Q_0$ holds and $Q_1$ holds, $Q_0 \wedge Q_1$

These two statements are [[de Morgan duality|de Morgan dual]] to each other, and thus are classically the [[negations]] of each other, but neither is the negation of the other in [[intuitionistic logic]]. 

Similarly, suppose there is a predicate $P$ indexed by elements $x$ of a [[set]] $A$, such that each $P(x)$ has a strong negation $Q(x)$. In the antithesis interpretation, there are two statements $P^+$ and $P^-$ one can make about these: 

* $P^+$ states that there exists an element $x$ in $A$ such that $P(x)$ holds

$$\exists x \in A.P(x)$$

* $P^-$ states that for all elements $x$ in $A$, the strong negation $Q(x)$ holds

$$\forall x \in A.Q(x)$$

These statements are [[de Morgan duality|de Morgan dual]] to each other, and thus are classically the [[negations]] of each other, but neither is the negation of the other in [[intuitionistic logic]]. 

## Related concepts

* [[negation]]

* [[inequality]], [[tight apartness relation]]

* [[antithesis interpretation]]

[[!redirects strong negation]]
[[!redirects strongly negated]]

[[!redirects strong falsehood]]
[[!redirects strongly false]]