
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The __boolean domain__ or __boolean field__ (often just: $Bool$) is a $2$-element [[set]], say $\mathbb{B} = \{ 0, 1 \}$ ("[[bits]]") or $\mathbb{B} = \{ \bot, \top \}$ ("[[bottom]]", "[[top]]"), whose [[elements]] may be interpreted as [[truth values]]. 

Note that $\mathbb{B}$ is the set of *all* [[truth values]] in [[classical logic]], but this cannot be assumed in non-classical logic such as [[intuitionistic logic]].  

The Boolean domain plays the role of the [[subobject classifier]] in the [[Boolean topos]] of [[Sets]].

If we think of the classical $\mathbb{B}$ as a [[pointed set]] equipped with the true element, then there is an [[generalized the|effectively unique]] boolean domain.

A __boolean variable__ $x$ is a variable that takes its value in a boolean domain, as $x \in \mathbb{B}$.  If this variable depends on parameters, then it is (or defines) a [[Boolean-valued function]], that is a [[function]] whose target is $\mathbb{B}$.

An [[element]] of $\mathbb{B}$ is a __[[binary digit]]__, or __bit__.

The boolean domain is the initial set with two elements. It is also the initial set with an element and an [[involution]]. It is also the [[tensor unit]] for the [[smash product]] in the [[monoidal category]] of [[pointed sets]]. 

\begin{remark}
**(relation to boolean algebra)**
\linebreak
The term 'boolean field' (or just 'field', depending on the context) is sometimes used more generally for any *[[boolean algebra]]*. In fact, the boolean domain is the [[initial object|initial]] boolean algebra.  If we interpret a boolean algebra as a [[boolean ring]], then the boolean domain is the [[finite field]] with $2$ elements.
\end{remark}

In [[dependent type theory]] the boolean domain is called the __[[type of booleans]]__. 

## Properties

The boolean domain is in [[bijection]] with the set of [[decidable propositions|decidable]] [[truth values]]. 

$$\mathrm{Bool} \cong \{P \in \Omega \vert P \vee \neg P\}$$

As a result, sometimes the boolean domain is called a __decidable subset classifier__. 

### Induction and recursion on the boolean domain

Like the natural numbers, the boolean domain has an induction principle, which states that to prove a statement $P(n)$ true for every bit, it suffices to prove it for falsehood $P(0)$ and truth $P(1)$. 

Similarly, the boolean domain also has a recursion principle, which states that to define a function $f:\mathrm{Bool} \to A$ from the boolean domain to a set $A$, it suffices to define the function when evaluated at falsehood $f(0)$ and truth $f(1)$. 

### Equality and inequality

\begin{definition}
By the induction principle of the boolean domain, we can define an [[equality]] [[relation]] on the boolean domain $x = y$, inductively defined by 

$$0 = 0 \; \mathrm{is} \; \mathrm{true} \qquad 0 = 1 \; \mathrm{is} \; \mathrm{false} \qquad 1 = 0 \; \mathrm{is} \; \mathrm{false} \qquad 1 = 1 \; \mathrm{is} \; \mathrm{true}$$
\end{definition}

\begin{definition}
Similarly, we can define an [[inequality]] relation on the boolean domain $x \neq y$, inductively defined by

$$0 \neq 0 \; \mathrm{is} \; \mathrm{false} \qquad 0 \neq 1 \; \mathrm{is} \; \mathrm{true} \qquad 1 \neq 0 \; \mathrm{is} \; \mathrm{true} \qquad 1 \neq 1 \; \mathrm{is} \; \mathrm{false}$$
\end{definition}

We can show that equality is an [[equivalence relation]] and the inequality relation is a [[apartness relation]], and that equality and inequality are mutually [[decidable]] $x = y \vee x \neq y$. 

If the ambient [[foundations]] already has an [[equality]] [[relation]] for all [[sets]] that satisfy the [[principle of substitution]], then one can show that $x = y$ [[if and only if]] $x =_\mathrm{Bool} y$ for the predefined equality relation $x =_\mathrm{Bool} y$ on the boolean domain. 

### Order structure

In addition, we can define various order structures on the boolean domain.

\begin{definition}
The order relation $x \leq y$ is inductively defined by 
$$0 \leq 0 \; \mathrm{is} \; \mathrm{true} \qquad 0 \leq 1 \; \mathrm{is} \; \mathrm{true} \qquad 1 \leq 0 \; \mathrm{is} \; \mathrm{false} \qquad 1 \leq 1 \; \mathrm{is} \; \mathrm{true}$$
\end{definition}

\begin{definition}
The order relation $x \geq y$ is inductively defined by 
$$0 \geq 0 \; \mathrm{is} \; \mathrm{true} \qquad 0 \geq 1 \; \mathrm{is} \; \mathrm{false} \qquad 1 \geq 0 \; \mathrm{is} \; \mathrm{true} \qquad 1 \geq 1 \; \mathrm{is} \; \mathrm{true}$$
\end{definition}

\begin{definition}
The order relation $x \lt y$ is inductively defined by 
$$0 \lt 0 \; \mathrm{is} \; \mathrm{false} \qquad 0 \lt 1 \; \mathrm{is} \; \mathrm{true} \qquad 1 \lt 0 \; \mathrm{is} \; \mathrm{false} \qquad 1 \lt 1 \; \mathrm{is} \; \mathrm{false}$$
\end{definition}

\begin{definition}
The order relation $x \gt y$ is inductively defined by 
$$0 \gt 0 \; \mathrm{is} \; \mathrm{false} \qquad 0 \gt 1 \; \mathrm{is} \; \mathrm{false} \qquad 1 \gt 0 \; \mathrm{is} \; \mathrm{true} \qquad 1 \gt 1 \; \mathrm{is} \; \mathrm{false}$$
\end{definition}

We can show that 

* the relations $\leq$ and $\geq$ are [[total orders]] with respect to the equality relation defined above and [[opposite relation|opposite]] of each other

* the relations $\lt$ and $\lt$ are [[pseudo-orders]] with respect to the equality relation defined above and [[opposite relation|opposite]] of each other

* the relations $\leq$ and $\gt$ are mutually [[decidable]] $x \leq y \vee x \gt y$. 

* the relation $\lt$ and $\geq$ are mutually [[decidable]] $x \lt y \vee x \geq y$. 

### Boolean algebra structure

We can also define the logical functions on $\mathrm{Bool}$ using the recursion principle of the boolean domain.

\begin{definition}
The [[negation]] of a boolean $x \mapsto \neg x$ is recursively defined by 
$$\neg 0 \coloneqq 1 \qquad \neg 1 \coloneqq 0$$
\end{definition}

\begin{definition}
The [[conjunction]] of two booleans $x, y \mapsto x \wedge y$ is recursively defined by 
$$0 \wedge 0 \coloneqq 0 \qquad 0 \wedge 1 \coloneqq 0 \qquad 1 \wedge 0 \coloneqq 0 \qquad 1 \wedge 1 \coloneqq 1$$
\end{definition}

\begin{definition}
The [[disjunction]] of two booleans $x, y \mapsto x \vee y$ is recursively defined by 
$$0 \vee 0 \coloneqq 0 \qquad 0 \vee 1 \coloneqq 1 \qquad 1 \vee 0 \coloneqq 1 \qquad 1 \vee 1 \coloneqq 1$$
\end{definition}

\begin{definition}
The [[exclusive disjunction]] of two booleans $x, y \mapsto x \underline{\vee} y$ is recursively defined by 
$$0 \underline{\vee} 0 \coloneqq 0 \qquad 0 \underline{\vee} 1 \coloneqq 1 \qquad 1 \underline{\vee} 0 \coloneqq 1 \qquad 1 \underline{\vee} 1 \coloneqq 0$$
\end{definition}

\begin{definition}
The implication of two booleans $x, y \mapsto x \rightarrow y$ is recursively defined by 
$$0 \rightarrow 0 \coloneqq 1 \qquad 0 \rightarrow 1 \coloneqq 1 \qquad 1 \rightarrow 0 \coloneqq 0 \qquad 1 \rightarrow 1 \coloneqq 1$$
\end{definition}

\begin{definition}
The abjunction of two booleans $x, y \mapsto x \nrightarrow y$ is recursively defined by 
$$0 \nrightarrow 0 \coloneqq 0 \qquad 0 \nrightarrow 1 \coloneqq 0 \qquad 1 \nrightarrow 0 \coloneqq 1 \qquad 1 \nrightarrow 1 \coloneqq 0$$
\end{definition}

\begin{definition}
The converse implication of two booleans $x, y \mapsto x \leftarrow y$ is recursively defined by 
$$0 \leftarrow 0 \coloneqq 1 \qquad 0 \leftarrow 1 \coloneqq 0 \qquad 1 \leftarrow 0 \coloneqq 1 \qquad 1 \leftarrow 1 \coloneqq 1$$
\end{definition}

\begin{definition}
The converse abjunction of two booleans $x, y \mapsto x \nleftarrow y$ is recursively defined by 
$$0 \nleftarrow 0 \coloneqq 0 \qquad 0 \nleftarrow 1 \coloneqq 1 \qquad 1 \nleftarrow 0 \coloneqq 1 \qquad 0 \nleftarrow 1 \coloneqq 0$$
\end{definition}

\begin{definition}
The biconditional of two booleans $x, y \mapsto x \iff y$ is recursively defined by 
$$0 \iff 0 \coloneqq 1 \qquad 0 \iff 1 \coloneqq 0 \qquad 1 \iff 0 \coloneqq 0 \qquad 1 \iff 1 \coloneqq 1$$
\end{definition}

We can prove that 

* $(\mathrm{Bool}, 0, 1, \neg, \wedge, \vee, \leq)$ forms a [[Boolean algebra]] with respect to the inductively defined total order above,

* $(\mathrm{Bool}, 0, 1, \wedge, \vee, \rightarrow, \leftarrow, \leq)$ forms a [[bi-Heyting algebra]] with respect to the inductively defined total order above,

* $(\mathrm{Bool}, 0, 1, \neg, \wedge, \underline{\vee})$ and $(\mathrm{Bool}, 1, 0, \neg, \vee, \underline{\vee})$ both form a [[Boolean ring]]

* For all booleans $x$ and $y$, 
$$x \iff y = 1 \;\mathrm{iff}\; x = y \qquad x \underline{\vee} y = 1 \;\mathrm{iff}\; x \neq y$$
$$x \rightarrow y = 1 \;\mathrm{iff}\; x \leq y \qquad x \nrightarrow y = 1 \;\mathrm{iff}\; x \gt y \qquad x \leftarrow y = 1 \;\mathrm{iff}\; x \geq y \qquad x \nleftarrow y = 1 \;\mathrm{iff}\; x \lt y$$

## In category theory

In [[category theory]], the boolean domain is the [[discrete category]] $\mathbb{2}$ with two objects $0, 1 \in \mathbb{2}$. Pairs of [[objects]] in a [[category]] $C$ are equivalently [[functors]] $F:\mathbb{2} \to C$ from the boolean domain to $C$ by the recursion principle of the boolean domain. As a result, the boolean domain can be called the **[[walking]] pair of objects** or **[[free-standing]] pair of objects** or **[[free-living]] pair of objects**. 

In addition, the boolean domain is the [[groupoid]] [[core]] of a number of categories, including the [[interval category]] and the [[walking parallel pair]]. 

## Related concepts

* [[decidable equality]]

* [[set of truth values]]

* [[boolean domain object]]

* [[type of booleans]]

* [[classical logic]], [[two-valued logic]]

* [[walking structure]]

  * **walking pair of objects**

  * [[walking morphism]]

  * [[walking parallel pair]]

  * [[walking isomorphism]]

  * [[walking equivalence]]

## References

See also:

* Wikipedia, *[Boolean domain](https://en.wikipedia.org/wiki/Boolean_domain)*

[[!redirects boolean domain]]
[[!redirects Boolean domain]]

[[!redirects boolean variable]]
[[!redirects Boolean variable]]
[[!redirects Boolean field]]
[[!redirects boolean field]]
[[!redirects Boolean fields]]
[[!redirects boolean fields]]

[[!redirects boolean]]
[[!redirects booleans]]

[[!redirects Boolean]]
[[!redirects Booleans]]

[[!redirects Bit]]

[[!redirects decidable subset classifier]]

[[!redirects set of decidable truth values]]
[[!redirects proset of decidable truth values]]
[[!redirects poset of decidable truth values]]
[[!redirects toset of decidable truth values]]
[[!redirects semilattice of decidable truth values]]
[[!redirects lattice of decidable truth values]]
[[!redirects Boolean algebra of decidable truth values]]
[[!redirects algebra of decidable truth values]]
[[!redirects Boolean ring of decidable truth values]]
[[!redirects ring of decidable truth values]]

[[!redirects set of decidable propositions]]
[[!redirects proset of decidable propositions]]
[[!redirects poset of decidable propositions]]
[[!redirects toset of decidable propositions]]
[[!redirects semilattice of decidable propositions]]
[[!redirects lattice of decidable propositions]]
[[!redirects Boolean algebra of decidable propositions]]
[[!redirects algebra of decidable propositions]]
[[!redirects Boolean ring of decidable propositions]]
[[!redirects ring of decidable propositions]]

[[!redirects walking pair of objects]]
[[!redirects walking pairs of objects]]

[[!redirects free-standing pair of objects]]
[[!redirects free-standing pairs of objects]]

[[!redirects free-living pair of objects]]
[[!redirects free-living pairs of objects]]

[[!redirects two-valued type]]
[[!redirects two-valued types]]
