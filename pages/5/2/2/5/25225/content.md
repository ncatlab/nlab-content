
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Marked extensional well-founded orders are important in constructing the [[sets]] of the [[cumulative hierarchy]] $V$ in a model of set theory, in the same way that [[well-orders]] or sets with [[transitive relation|transitive]] [[extensional relation|extensional]] [[well-founded relations]] are important in constructing the [[ordinals]] of $V$. These become important in [[constructive mathematics]] where one cannot in general show that the set of [[cardinals]] in $V$ and the set of ordinals in $V$ are in bijection with each other. 

## Definition

A **marked extensional well-founded order** or **mewo** is a set $S$ with an [[extensional relation|extensional]] [[well-founded relation]] $a \prec b$ on a set $S$ and a [[predicate]] $m(a)$ on $S$. 

## Properties

### Marked elements

An element $x \in S$ is **marked** if $m(x)$ is true. By the [[axiom schema of bounded separation]], one can construct the subset of marked elements in $S$:

$$M_S \coloneqq \{x \in S \vert m(x)\}$$

### Marked extensional well-founded order homomorphisms

A **marked extensional well-founded order homomorphism** between two marked extensional well-founded order $S$ and $T$ is a function $f:S \to T$ such that

* $f$ preserves the marking predicate: for all $x \in S$, $m(x)$ implies that $m(f(x))$ 

* $f$ preserves the well-founded relation: for all $x \in S$ and $y \in S$, $x \prec y$ implies that $f(x) \prec f(y)$

A **marked extensional well-founded order isomorphism** is a marked extensional well-founded order homomorphism $f:S \to T$ with a marked extensional well-founded order homomorphism $g:T \to S$ such that for all elements $s \in S$, $g(f(s)) = s$ and for all elements $t \in T$ $f(g(t)) = t$.  

The category of marked extensional well-founded order homomorphisms is the [[concrete category]] $\mathrm{MEWO}$ whose [[objects]] are marked extensional well-founded orders and whose [[morphisms]] are marked extensional well-founded order homomorphisms. 

### Trivialization

There is a [[forgetful functor]] $U:\mathrm{MEWO} \to \mathrm{EWO}$ which takes a marked extensional well-founded order $(S, \prec, m)$ to its underlying extensional well-founded order $(S, \prec)$. There is also a [[functor]] $F:\mathrm{EWO} \to \mathrm{MEWO}$ which takes an extensional well-founded order $(S, \prec)$ to the marked extensional well-founded order $(S, \prec, \top_S)$, where $\top_S$ is the always true predicate on $S$. The **trivialization** of a marked extensional well-founded order is defined as the composite of the two functors above $\overline{S} \coloneqq F(U(S))$. 

### Simulations

A [[simulation]] between marked extensional well-founded orders $S$ and $T$ is a marked extensional well-founded order homomorphism $f:S \to T$ such that its [[image]] is downwards closed: for all $x \in S$ and $y \in T$, if $y \prec f(x)$, then there exists $z \in S$ such that $z \prec x$ and $f(z) \prec y$. 

We denote the set of simulations between marked extensional well-founded orders $S$ and $T$ by $S \sqsubseteq T$. 

The category $\mathrm{MEWO}_\mathrm{Sim}$ is the [[subcategory]] of $\mathrm{MEWO}$ whose objects are marked extensional well-founded orders and whose [[morphisms]] are simulations. We show that the above category is a [[poset]]:

Since the relation $\prec$ is extensional and well-founded, the following is true of simulations: 

* Every simulation $f:S \to T$ is an [[injection]]. 

* Given marked extensional well-founded orders $S$ and $T$, the set of simulations $S \sqsubseteq T$ has at most one element. 

As a result, one could define the relation $S \leq T$ on marked extensional well-founded orders by $\exists x.x \in S \sqsubseteq T$. The relation $S \leq T$ between marked extensional well-founded orders is a [[partial order]]

* for all marked extensional well-founded orders $S$, $S \leq S$
* for all marked extensional well-founded orders $S$, $T$, and $U$, $S \leq T \wedge T \leq U \implies S \leq U$
* for all marked extensional well-founded orders $S$ and $T$, $S \leq T \wedge T \leq S \implies S = T$

### Covered elements and initial segments

An element $x \in S$ is **covered** if there exists a marked element $y \in S$ such that $x \prec y$ is true. Given a marked extensional well-founded order $S$ and an element $x \in S$, the **initial segment** of $S$ is the set of all elements covered by $x \in S$

$$S \downarrow^+ x \coloneqq \{t \in S \vert t \prec x\}$$

The initial segment $S \downarrow^+ x$ is a marked extensional well-founded order, with the well-founded relation defined as $y \prec z$ for elements $y \in S \downarrow^+ x$ and $z \in S \downarrow^+ x$, and the marking relation defined as $m_x(y) \coloneqq y \prec x$ for elements $y \in S \downarrow^+ x$. 

A marked extensional well-founded order is **covered** if every element $x \in S$ is covered; i.e. 

$$\forall x \in S.\exists y \in S.m(y) \wedge (x \prec y)$$

It follows by well-founded induction that $S \downarrow^+ x$ is a covered marked extensional well-founded order. 

\begin{theorem}
Given a marked extensional well-founded order $S$, the function $f:S \downarrow^+ x \to \overline{S}$, defined by the composite of the canonical subset injection $i:S \downarrow^+ x \to S$ and the canonical function $j:S \to \overline{S}$ given by the identity function on the carrier set, is a simulation. 
\end{theorem}

\begin{theorem}
Given a marked extensional well-founded order $S$ and elements $x \in S$ and $y \in S$, $S \downarrow^+ x = S \downarrow^+ y$ implies that $x = y$. 
\end{theorem}

\begin{theorem}
Given marked extensional well-founded orders $S$ and $T$ and a function $f:S \to T$ which preserves the marking predicate; i.e. $m(x)$ implies that $m(f(x))$ for all $x \in S$, then $f$ is a simulation if and only if $S \downarrow^+ x = T \downarrow^+ f(x)$. 
\end{theorem}

### Bounded simulations

A bounded simulation between marked extensional well-founded orders $S$ and $T$ consists of a marked element $y \in M_T$ and a simulation $f:S \to T$ such that the [[image]] of $f$ is equal to the initial segment at $y$, $\mathrm{im}(f) = T \downarrow^+ y$. We denote the set of bounded simulations between marked extensional well-founded orders $S$ and $T$ by $S \sqsubset T$. 

\begin{theorem}
Given marked extensional well-founded orders $S$ and $T$, the set of bounded simulations $S \sqsubset T$ has at most one element. 
\end{theorem}

As a result, one could define the relation $S \lt T$ on marked extensional well-founded orders by $\exists x.x \in S \sqsubset T$. The relation satisfies the following properties

* for all marked extensional well-founded orders $S$ and $T$, $S \lt T$ implies that $S \leq \overline{T}$

* for all marked extensional well-founded orders $S$ and $T$ and $U$, $S \lt T$ and $T \lt U$ implies that $S \leq \overline{U}$

* for all marked extensional well-founded orders $S$ and $T$ and $U$, $S \lt T$ and $T \leq U$ implies that $S \lt U$ 

## Related concepts

* [[well-order]]

* [[extensional relation]]

* [[well-founded relation]]

## References

* {#deJongEtAl23} [[Tom de Jong]], [[Nicolai Kraus]], [[Fredrik Nordvall Forsberg]], [[Chuangjie Xu]], *Set-Theoretic and Type-Theoretic Ordinals Coincide* ([arXiv:2301.10696](https://arxiv.org/abs/2301.10696))

[[!redirects marked extensional well-founded order]]
[[!redirects marked extensional well-founded orders]]

[[!redirects mewo]]
[[!redirects mewos]]

[[!redirects MEWO]]
[[!redirects MEWOs]]

[[!redirects covered marked extensional well-founded order]]
[[!redirects covered marked extensional well-founded orders]]

[[!redirects covered mewo]]
[[!redirects covered mewos]]

[[!redirects covered MEWO]]
[[!redirects covered MEWOs]]

[[!redirects marked extensional well-founded relation]]
[[!redirects marked extensional well-founded relations]]

[[!redirects covered marked extensional well-founded relation]]
[[!redirects covered marked extensional well-founded relations]]

[[!redirects marked element]]
[[!redirects marked elements]]

[[!redirects subset of marked elements]]
[[!redirects subsets of marked elements]]

[[!redirects covered element]]
[[!redirects covered elements]]