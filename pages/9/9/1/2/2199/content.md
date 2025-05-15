
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
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

The boolean domain is in [[bijection]] with the set of [[decidable propositions]]. 

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

Using the recursion principle of the boolean domain, one can recursively define the logical functions on $\mathrm{Bool}$ as follows

* For negation $b \mapsto \neg b$
$$\neg 0 \coloneqq 1 \qquad \neg 1 \coloneqq 0$$
* For conjunction $b \mapsto b \wedge a$, given a boolean $a$
$$0 \wedge a \coloneqq 0 \qquad 1 \wedge a \coloneqq a$$
* For disjunction $b \mapsto b \vee a$, given a boolean $a$
$$0 \vee a \coloneqq a \qquad 1 \vee a \coloneqq 1$$
* For implication $b \mapsto b \implies a$, given a boolean $a$
$$0 \implies a \coloneqq 1 \qquad 1 \implies a \coloneqq a$$
* For the biconditional $b \mapsto b \iff a$, given a boolean $a$
$$0 \iff a \coloneqq \neg a \qquad 1 \iff a \coloneqq a$$

One could prove that $(\mathrm{Bool}, 0, 1, \neg, \wedge, \vee, \implies, \leq)$ form a [[Boolean algebra]] with respect to the inductively defined partial order above. 

A _boolean predicate_ valued in a type $T$ is a function $P: T \rightarrow \mathrm{Bool}$, and the type $T \to \mathrm{Bool}$ is a boolean [[function algebra]] for all types $T$. 

## Related concepts

* [[decidable equality]]

* [[set of truth values]]

* [[boolean domain object]]

* [[type of booleans]]

* [[two-valued logic]]

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

[[!redirects two-valued type]]
[[!redirects two-valued types]]
