
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *strict total order* or *strict linear order* is the irreflexive version of a [[total order]]. This is sometimes called *linear order*, but [[linear order]] is also used to refer to the non-strict [[total order]]. 

A **strictly totally ordered set** or **strictly linearly ordered set** is a [[set]] equipped with a strict total order.

In [[classical mathematics]], the distinction between strict total orders and total orders is merely a terminological technicality, which is not always observed; more precisely, there is a [[natural isomorphism|natural bijection]] between the set of total orders on a given set $S$ and the set of strict total orders on $S$, and one distinguishes them by the notation $\lt$ (for the strict total orders) and $\leq$ (for the total order). In [[constructive mathematics]], however, there exist total orders whose negation is not a strict total order. 

## Definition

A **strict total order** or **strict linear order** or **decidable pseudo-order** on a set is a [[pseudo-order]] $\lt$ which additionally is [[decidable relation|decidable]] in that $x \lt y$ or $\neg (x \lt y)$. Rewriting $\neg (y \lt x)$ as the [[partial order]] $x \leq y$, the decidability condition is equivalent to the linearity condition $x \lt y \vee y \leq x$, hence the name *strict linear order* or *linear order*. 

Equivalently, a strict total order or a strict linear order is a [[strict weak order]] which satisfies [[trichotomy]]: $x \lt y$ or $y \lt x$ or $x = y$. 

Since $x \lt y$ is a [[decidable proposition]], the proposition $x \lt y \underline{\vee} y \lt x$ is also a [[decidable proposition]] due to asymmetry. An alternate way of writing the 
connectedness axiom of a pseudo-order is 
* if not ($x \lt y$ [[xor]] $y \lt x$), then $x = y$.
which the decidability of the exclusive disjunction implies that ($x \lt y$ [[xor]] $y \lt x$) [[xor]] $x = y$.  

## Properties

\begin{theorem}
The negation of every strict linear order is a [[total order]]
\end{theorem}

\begin{proof}
This follows from trichotomy and linearity. We have $x \lt y$ or $x = y$ or $y \lt x$ and $x \lt y$ or $y \leq x$, which implies that $x = y$ or $y \lt x$ if and only if $y \leq x$. Then, since disjunction is idempotent and equality is symmetric, we have $x \lt y$ or $x = y$ or $y = x$ or $y \lt x$, which is logically equivalent to totality $x \leq y$ or $y \leq x$. 
\end{proof}

\begin{theorem}
Assuming [[excluded middle]], the negation of every total order is a strict linear order.
\end{theorem}

\begin{proof}
...
\end{proof}

Given a proposition $P$, $P$ can be made into a [[subsingleton]] [[set]] by considering the subset $\{\top \vert P\} \coloneqq \{p \in \{\top\} \vert (p = \top) \wedge P\}$ of the [[singleton]] $\{\top\}$. Let $A \uplus B$ denote the [[disjoint union]] of sets $A$ and $B$, and let $B^A$ denote the function set with domain $A$ and codomain $B$.  

\begin{theorem}
Every strict total order on a set $A$ is [[purely cotransitive]]: Given elements $x$, $y$, and $z$ in $A$, one can construct an element of the function set

$$\mathrm{cotransitive}(x, y, z) \in \left(\{\top \vert x \lt y\} \uplus \{\top \vert y \lt z\}\right)^{\{\top \vert x \lt z\}}$$
\end{theorem}

\begin{proof}
We prove this by case analysis. 

Suppose that $x \lt y$. Then one can construct the element $\top \in \{\top \vert x \lt y\}$ and by definition of [[disjoint union]] an element $(0, \top) \in \{\top \vert x \lt y\} \uplus \{\top \vert y \lt z\}$. $\mathrm{cotransitive}(x, y, z)$ is given by the constant function $t \mapsto (0, \top)$. 

Now suppose that $\neg (x \lt y)$. This means that $y \leq x \lt z$, and one can construct the element $\top \in \{\top \vert y \lt z\}$. By definition of [[disjoint union]] one can construct an element $(1, \top) \in \{\top \vert x \lt y\} \uplus \{\top \vert y \lt z\}$. $\mathrm{cotransitive}(x, y, z)$ is given by the constant function $t \mapsto (1, \top)$.

Since $x \lt y$ is decidable this covers every possible case. Thus, every decidable pseudo-order is purely cotransitive. 
\end{proof}

The above proof first appeared for the pseudo-order of the [[real numbers]] in theorem 11.4.3 of the [[HoTT book]] in the context of [[dependent type theory]]. 

\begin{corollary}
Suppose that the [[rational numbers]] are a [[subset]] of the decidably pseudo-ordered set $A$, and the canonical injection $i:\mathbb{Q} \to A$ is strictly monotonic. Then for every element $x$ of $A$ one can construct a [[locator]] for $x$.  
\end{corollary}

\begin{proof}
The locator is given by the [[dependent function]]

$$(q, r) \mapsto \mathrm{cotransitive}(i(q), x, i(r)) \in \prod_{q, r \in \mathbb{Q}} \left(\{\top \vert q \lt x\} \uplus \{\top \vert x \lt r\}\right)^{\{\top \vert q \lt r\}}$$

which always exists by the previous theorem and by the fact that the rational numbers are a subset of $A$ which preserves the pseudo-order. 
\end{proof}

## Related concepts

* [[pseudo-order]]

* [[classical set]]

* [[dense linear order]]

## References

The definition of linearity for an order relation is given on page 377 of 

* {#UFP13} [[Univalent Foundations Project]], Section 11.2 of: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

For a proof that the strict linear order on the real numbers is purely cotransitive, see theorem 11.4.3 of:

* {#UFP13} [[Univalent Foundations Project]], Section 11.4 of: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

[[!redirects strict linear order]]
[[!redirects strict linear orders]]
[[!redirects strict linear ordering]]
[[!redirects strict linear orderings]]
[[!redirects strictly linearly ordered]]
[[!redirects strictly linearly ordered set]]
[[!redirects strictly linearly ordered sets]]

[[!redirects strict total order]]
[[!redirects strict total orders]]
[[!redirects strict total ordering]]
[[!redirects strict total orderings]]
[[!redirects strictly totally ordered]]
[[!redirects strictly totally ordered set]]
[[!redirects strictly totally ordered sets]]

[[!redirects decidable pseudo-order]]
[[!redirects decidable pseudo-orders]]
[[!redirects decidable pseudo-ordering]]
[[!redirects decidable pseudo-orderings]]
[[!redirects decidably pseudo-ordered]]
[[!redirects decidably pseudo-ordered set]]
[[!redirects decidably pseudo-ordered sets]]