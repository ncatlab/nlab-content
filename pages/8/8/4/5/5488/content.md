
# The axiom of pairing
* table of contents
{: toc}

## Idea

In [[material set theory]] as a [[foundation of mathematics]], the axiom of pairing is an important axiom needed to get the foundations off the ground (to mix metaphors).


## Statement

The __axiom of pairing__ states the following:

+-- {: .un_axiom}
###### Axiom (pairing)

If $x$ and $y$ are (material) sets, then there exists a set $P$ such that, for every set $a$, $a \in P$ if and only if $a = x$ or $a = y$.
=--

Using the [[axiom of extensionality]], one can prove that the set $P$ above is unique; it is usually denoted $\{x,y\}$ and called the __unordered pair__ of $x$ and $y$.  Note that $\{x,x\}$ may also be denoted simply $\{x\}$.


## Generalisation

The axiom of pairing is the binary part of a [[binary/nullary pair]] whose nullary part is the axiom stating the existence of the [[empty set]].  We can use these axioms and the [[axiom of union]] to prove every instance of the following __axiom__ (or rather theorem) __schema of finite sets__:

+-- {: .un_theorem}
###### Theorem (finite sets)

If $x_1, \ldots, x_n$ are sets, then there exists a set $P$ such that, for every set $a$, $a \in P$ if and only if $a = x_1$ or ... or $a = x_n$.
=--

Again, we can prove that $P$ is unique; it is denoted $\{x_1, \ldots, x_n\}$ and called the __finite set__ consisting of $x_1, \ldots, x_n$.

Note that this is a _schema_, with one instance for every (metalogical) [[natural number]].  Within axiomatic set theory, this is very different from the single statement that begins with a [[universal quantification]] over the (internal) set of natural numbers.  In particular, each instance of this schema can be stated and proved without the [[axiom of infinity]].

+-- {: .proof}
###### Proof

Of course, there is one proof for each natural number.

*  For $n = 0$, this is simply the axiom of the empty set.
*  For $n = 1$, we use the axiom of pairing with $x \coloneqq x_1$ and $y \coloneqq x_1$ to construct $\{x_1\}$.
*  For $n = 2$, we use the axiom of pairing with $x \coloneqq x_1$ and $y \coloneqq x_2$ to construct $\{x_1, x_2\}$.
*  For $n = 3$, we first use the axiom of pairing twice to construct $\{x_1, x_2\}$ and $\{x_3\}$, then use pairing again to construct $\big\{\{x_1, x_2\}, \{x_3\}\big\}$, then use the axiom of union to construct $\{x_1, x_2, x_3\}$.
*  In general, once we have $\{x_1, \ldots, x_{n-1}\}$, we use pairing to construct $\{x_n\}$, use pairing again to construct $\big\{\{x_1, \ldots, x_{n-1}\}, \{x_n\}\big\}$, then use the axiom of union to construct $\{x_1, \ldots, x_n\}$.  (A direct proof of a single statement for $n \gt 3$ can actually go faster than this; the length of the shortest proof is [[logarithmic]] in $n$ rather than linear in $n$.)
=--

Note that these 'finite sets' are precisely the [[Kuratowski-finite sets]] in a [[constructive mathematics|constructive]] treatment.


## Relation to ordered pairs

The unordered pair $\{x,y\}$ should not be confused with the [[ordered pair]] $(x,y)$.  In particular, $\{x,y\} = \{y,x\}$, while $(x,y) \neq (y,x)$ (if $x \neq y$).  While $\{x,y\}$ has a direct definition as a [[pure set]] (if $x$ and $y$ are pure sets), $(x,y)$ must be coded in a complicated way (traditionally as $\big\{\{x\}, \{x,y\}\big\}$).  However, the two are somewhat related:

*  As just seen, the usual encoding of an ordered pair of pure sets as a pair set (due again to Kuratowski) involves unordered pairs.  (But in fact pairing is needed to get *anywhere* in material set theory.)
*  Just as the axiom of pairing is needed to get anywhere in material set theory, so some axiom related to ordered pairs is needed to get anywhere in [[structural set theory]].  (In [[ETCS]], this is the axiom of the ([[Cartesian product|Cartesian]]) [[product]]; in [[SEAR]], this is the axiom of tabulations.)

Since we usually take a structural approach in the $n$Lab, the term '[[pairing]]' here usually refers to *ordered* pairs.

Note that unordered pairs also exist in structural set theory in this way:  If $A$ is a set and $x$ and $y$ are elements of $A$, then $\{x,y\}$ is a [[subset]] of $A$ (and an element of the [[power set]] of $A$).  The set of all unordered pairs of elements of $A$ may be denoted $\big(A \atop 2\big)$.


[[!redirects axiom of pairing]]

[[!redirects unordered pair]]
[[!redirects unordered pairs]]

[[!redirects axiom of finite sets]]
[[!redirects axiom scheme of finite sets]]
[[!redirects axiom schema of finite sets]]
