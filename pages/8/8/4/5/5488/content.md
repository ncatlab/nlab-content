
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
=--
=--

# The axiom of pairing
* table of contents
{: toc}

## Idea

In [[material set theory]] as a [[foundation of mathematics]], the axiom of pairing is an important axiom needed to get the foundations off the ground (to mix metaphors).  It states that [[pair sets]] exist.

## Statement

### Pairing

The __axiom of pairing__ (or __axiom of pairs__) states the following:

**Axiom of pairing**: _If $x$ and $y$ are (material) sets, then there exists a set $P$ such that $x \in P$ and $y \in P$._

Using the axiom of separation ([[bounded separation]] is enough), we can prove the existence of a particular set $P$ such that $x$ and $y$ are the *only* members of $P$.  Using the [[axiom of extensionality]], we can then prove that this set $P$ is unique; it is usually denoted $\{x,y\}$ and called the __[[pair set]]__ of $x$ and $y$.  Note that $\{x,x\}$ may also be denoted simply $\{x\}$.

One could also assume that the [[material set theory]] has a primitive binary operation $P$ which takes of a material set $x$ and $y$ and returns a material set $P(x, y)$. Then the axiom of pairing becomes

**Axiom of pairing**: _If $x$ and $y$ are (material) sets, then $x \in P(x, y)$ and $y \in P(x, y)$._

### Unordered pairing

The __axiom of unordered pairing__ (or __axiom of unordered pairs__) states the following:

**Axiom of unordered pairing**: If $x$ and $y$ are (material) sets, then there exists a set $P$ such that $x \in P$ and $y \in P$ and for all sets $z$, $z \in P$ implies that $z = x$ or $z = y$.

Using the [[axiom of extensionality]], we can then prove that this set $P$ is unique; it is usually denoted $\{x,y\}$ and called the __[[pair set]]__ of $x$ and $y$.  Note that $\{x,x\}$ may also be denoted simply $\{x\}$.

One could also assume that the [[material set theory]] has a primitive binary operation $\{-,-\}$ which takes of a material set $x$ and $y$ and returns a material set $\{x, y\}$. Then the axiom of pairing becomes

**Axiom of unordered pairing**: If $x$ and $y$ are (material) sets, then $x \in \{x, y\}$, $y \in \{x, y\}$, and for all sets $z$, $z \in \{x, y\}$ implies that $z = x$ or $z = y$.

### Ordered pairing

Let us assume that the [[material set theory]] has a primitive binary operation $(-,-)$ which takes of a material set $x$ and $y$ and returns a material set $(x, y)$. 

The __axiom of ordered pairing__ (or __axiom of ordered pairs__) states the following:

**Axiom of ordered pairing**: _If $x$ and $y$ are (material) sets, then $x \in (x, y)$, $y \in (x, y)$, and for all sets $a$ and $b$, $(a, b) = (x, y)$ if and only if $a = x$ and $b = y$._

$$\forall a.\forall b.\{a, b\} = \{x, y\} \iff (a = x \wedge b = y)$$

### With sets and elements different

In set theories where sets and elements are not the same thing, pairing becomes an operation on both the sets and the elements. One has to add a primitive ternary relation $p(X, Y, P)$ which says that $P$ is the [[Cartesian product]] of $X$ and $Y$, as well as primitive quaternary relations $\pi_1(X, P, c, a)$ and $\pi_2(Y, P, c, b)$ which says that element $a \in X$ is the left element of the pair $c \in P$ and element $b \in Y$ is the right element of the pair $c \in P$, and the following axiom:

**Axiom of ordered pairing**: _If $X$ and $Y$ are sets, then there exists a set $P$ such that $p(X, Y, P)$ and for every object $a$ and $b$, $a \in X$ and $b \in Y$ implies that there exists an object $c$ such that $c \in P$, $\pi_1(X, P, c, a)$, and $\pi_2(Y, P, c, b)$_

$P$ is usually denoted $X \times Y$ and called the __[[Cartesian product]]__ of $X$ and $Y$, while $c$ is usually denoted $(a, b)$ and called the __[[ordered pair]] of $a$ and $b$.

### In dependent type theory

In [[dependent type theory]], it is possible to define a [[Tarski universe]] $(V, \in)$ of [[pure sets]] which behaves as a [[material set theory]]. The universal type family of the Tarski universe is given by the type family $x:V \vdash \sum_{y:V} y \in x$. The **axiom of pairing** is given by the following [[inference rule]]:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{pairing}_V:\prod_{x:V} \prod_{y:V} \sum_{P:V} (x \in P) \times (y \in P)}$$

## Generalisation

The axiom of pairing is the binary part of a [[binary/nullary pair]] whose nullary part is the axiom stating the existence of the [[empty set]].  We can use these axioms and the [[axiom of union]] to prove every instance of the following __axiom__ (or rather theorem) __schema of finite sets__:

\begin{theorem}
If $x_1, \ldots, x_n$ are sets, then there exists a set $P$ such that $x_1, \ldots, x_n \in P$.
\end{theorem}

Again, we can prove the existence of specific $P$ such that $x_1, \ldots, x_n$ are the *only* members of $P$ and prove that this $P$ is unique; it is denoted $\{x_1, \ldots, x_n\}$ and is called the __[[finite set]]__ consisting of $x_1, \ldots, x_n$.

Note that this is a _schema_, with one instance for every (metalogical) [[natural number]].  Within axiomatic set theory, this is very different from the single statement that begins with a [[universal quantification]] over the (internal) set of natural numbers.  In particular, each instance of this schema can be stated and proved without the [[axiom of infinity]]. Of course, there is one proof for each natural number.

*  For $n = 0$, this is simply the axiom of the empty set.
*  For $n = 1$, we use the axiom of pairing with $x \coloneqq x_1$ and $y \coloneqq x_1$ to construct $\{x_1\}$.
*  For $n = 2$, we use the axiom of pairing with $x \coloneqq x_1$ and $y \coloneqq x_2$ to construct $\{x_1, x_2\}$.
*  For $n = 3$, we first use the axiom of pairing twice to construct $\{x_1, x_2\}$ and $\{x_3\}$, then use pairing again to construct $\big\{\{x_1, x_2\}, \{x_3\}\big\}$, then use the axiom of union to construct $\{x_1, x_2, x_3\}$.
*  In general, once we have $\{x_1, \ldots, x_{n-1}\}$, we use pairing to construct $\{x_n\}$, use pairing again to construct $\big\{\{x_1, \ldots, x_{n-1}\}, \{x_n\}\big\}$, then use the axiom of union to construct $\{x_1, \ldots, x_n\}$.  (A direct proof of a single statement for $n \gt 3$ can actually go faster than this; the length of the shortest proof is [[logarithmic]] in $n$ rather than linear in $n$.)

Note that these 'finite sets' are precisely the [[Kuratowski-finite sets]] in a [[constructive mathematics|constructive]] treatment.


## Related notions

* [[pairing structure]]

In the $n$Lab, the term '[[pairing]]' usually refers to *[[ordered pair|ordered]]* pairs.

## References

For the axiom of ordered pairing see:

* [[Håkon Robbestad Gylterud]], [[Elisabeth Stenholm]], [[Niccolò Veltri]], *Terminal Coalgebras and Non-wellfounded Sets in Homotopy Type Theory* &lbrack;[arXiv:2001.06696](https://arxiv.org/abs/2001.06696)&rbrack;

[[!redirects axiom of pairing]]
[[!redirects axiom of pairs]]
[[!redirects axiom of pair sets]]

[[!redirects axiom of unordered pairing]]
[[!redirects axiom of unordered pairs]]
[[!redirects axiom of unordered pair sets]]

[[!redirects axiom of ordered pairing]]
[[!redirects axiom of ordered pairs]]
[[!redirects axiom of ordered pair sets]]

[[!redirects axiom of finite sets]]
[[!redirects axiom scheme of finite sets]]
[[!redirects axiom schema of finite sets]]

category: foundational axiom
