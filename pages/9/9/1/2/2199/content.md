
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

The boolean domain is in [[bijection]] to the set of [[decidable propositions]]. 

$$\mathrm{Bool} \cong \{P \in \Omega \vert P \vee \neg P\}$$

As a result, sometimes the type of booleans is called a __decidable subtype classifier__. 

### Boolean logic

One could recursively define the logical functions on $\mathrm{Bool}$ as follows

* For negation $\neg$
  * $\neg 0 := 1$
  * $\neg 1 := 0$
* For conjunction $\wedge$
  * $0 \wedge a := 0$
  * $1 \wedge a := a$
* For disjunction $\vee$
  * $0 \vee a := a$
  * $1 \vee a := 1$
* For implication $\implies$
  * $0 \implies a := 1$
  * $1 \implies a := a$
* For the biconditional $\iff$
  * $0 \iff a := \neg a$
  * $1 \iff a := a$

One could prove that $(\mathrm{Bool}, 0, 1, \neg, \wedge, \vee, \implies)$ form a [[total order|total]] [[Boolean algebra]]. The [[poset]] structure is given by implication.

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
