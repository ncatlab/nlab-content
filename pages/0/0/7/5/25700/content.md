+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

\tableofcontents

\section{Definition}

A **[[pointed set|pointed]] [[commutative semigroup|commutative]] [[invertible semigroup]]** is a [[commutative semigroup]] $(A, +)$ which comes with an element $1 \in A$ and a function $-:A \to A$ such that for all elements $a \in A$ and $b \in A$, $a + b + (-b) = a$. From commutativity and associativity one could derive the other three invertibility properties for an [[invertible semigroup]]: $a + (-b) + b = a$, $b + (-b) + a = a$, and $(-b) + b + a = a$. 

\section{Properties}

Every pointed commutative invertible semigroup $(A, +, -, 1)$ is an [[abelian group]]. The element $1 + (-1)$ is both left unital and right unital with respect to the binary operation $+$. Since $1$ is usually not the same as $1 + (-1)$, these are also **pointed abelian groups**. Similarly, every [[abelian group]] is a pointed commutative invertible semigroup by taking the point to be the [[neutral element]] $0$. 

However, despite the above relation between pointed commutative invertible semigroup and abelian groups, the [[category]] of pointed commutative invertible semigroups is different from the [[category of abelian groups]] ($\mathrm{Ab}$). In [[Ab]], the initial object and terminal objects are the same, the [[trivial group]]. However, in the category of pointed commutative invertible semigroups, while the [[terminal object]] is still the [[trivial group]], the [[initial object]] is the [[integers]]. In this, the category of pointed commutative invertible semigroups has more in common with the categories [[Ring]] and [[CRing]] of rings and commutative rings respectively. 

\section{Related concepts}

* [[commutative invertible semigroup]]
* [[abelian group]]
* [[Tarski group]]

[[!redirects pointed commutative invertible semigroup]]
[[!redirects pointed commutative invertible semigroups]]

[[!redirects category of pointed commutative invertible semigroups]]

[[!redirects pointed abelian group]]
[[!redirects pointed abelian groups]]

[[!redirects category of pointed abelian groups]]