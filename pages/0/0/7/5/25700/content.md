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

A **[[pointed object|pointed]] [[abelian group]]** is an abelian group $(A, +, 0, -)$ with an additional point $1 \in A$. 

\begin{remark}
The neutral element $0$ is not needed in the definition of a pointed abelian group. Pointed abelian groups could equally be defined as [[pointed set|pointed]] [[commutative semigroup|commutative]] [[invertible semigroups]], a [[commutative semigroup]] $(A, +)$ which comes with an element $1 \in A$ and a function $-:A \to A$ such that for all elements $a \in A$ and $b \in A$, $a + b + (-b) = a$. From commutativity and associativity one could derive the other three invertibility properties for an [[invertible semigroup]]: $a + (-b) + b = a$, $b + (-b) + a = a$, and $(-b) + b + a = a$. The element $1 + (-1)$ is both left unital and right unital with respect to the binary operation $+$, so by defining $0 \coloneqq 1 + (-1)$, $A$ becomes an [[abelian group]] $(A, +, 0, -)$ with an additional point $1 \in A$; hence a pointed abelian group. 
\end{remark}

\section{Properties}

Every [[abelian group]] is a pointed abelian group by taking the point to be the [[neutral element]] $0$. 

However, despite the above relation between pointed abelian groups and abelian groups, the [[category]] of pointed abelian groups is different from the [[category of abelian groups]] ($\mathrm{Ab}$). In [[Ab]], the initial object and terminal objects are the same, the [[trivial group]]. However, in the category of pointed abelian groups, while the [[terminal object]] is still the [[trivial group]], the [[initial object]] is the [[integers]]. In this, the category of pointed abelian groups has more in common with the categories [[Ring]] and [[CRing]] of rings and commutative rings respectively. 

\section{Related concepts}

* [[pointed module]]
* [[pointed object in a monoidal category]]
* [[commutative invertible semigroup]]
* [[abelian group]]
* [[Tarski group]]

[[!redirects pointed abelian group]]
[[!redirects pointed abelian groups]]

[[!redirects category of pointed abelian groups]]

[[!redirects pointed commutative invertible semigroup]]
[[!redirects pointed commutative invertible semigroups]]

[[!redirects category of pointed commutative invertible semigroups]]