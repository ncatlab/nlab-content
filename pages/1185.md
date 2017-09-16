# Idea #

Cardinals are one generalization of [[natural numbers object|natural numbers]] to non-finite numbers.


# Definition ##

In naive [[set theory]], the  **cardinals** or **cardinal numbers** are the [[isomorphism]] classes in the [[category]] [[Set]].  The cardinality of a [[finite set]] is a **finite cardinal**, that of a non-finite set is a **infinite** or **transfinite** cardinal.

This naive definition is unpleasant because each cardinal is then a [[proper class]] (and one could not make further sets using them as elements).  For this reason, in axiomatic (material) [[set theory]] one usually chooses the canonical representatives of cardinals among [[ordinal]]s.  According to this approach, a **cardinal** is an ordinal (a [[transitive set]] which is [[well-order|well-ordered]] by the membership relation $\in$) which is not equipotent ([[bijection|bijective]]) to any smaller (with respect to the total order $\in$ on the class $\mathbf{Ord}$ of ordinals) ordinal.  The **cardinality** of a set $X$ is defined to be the unique cardinal number to which it is bijective.

This definition relies on the [[axiom of choice]] to ensure that any set can be well-ordered (so that is is bijective to some ordinal).  In the absence of choice, various other tricks can be used to define cardinalities.  For instance, in the presence of the [[axiom of foundation]], every set appears somewhere in the [[von Neumann hierarchy]], and this hierarchy is indexed by the ordinals.  We can therefore consider, instead of the proper class of _all_ sets of a given cardinality, the set of all sets of a given cardinality of least rank.

On the other hand, in structural [[set theory]] it is [[evil]] to care about distinguishing isomorphic objects (which is the case of sets just means bijective ones), and silly to want to have a canonical choice of representative for isomorphism classes.  Thus, from this approach it is natural to simply define a cardinal to _be_ a set (that is, an object of [[Set]]).


# Cardinal arithmetic #

For $S$ a [[set]], write $|S|$ for its cardinality. Then the standard operations in the [[cartesian closed category]] [[Set]] induced arithmetic operations on cardinals:

For $S_1$ and $S_2$ two sets, the **sum** of their cardinalities is the cardinality of their [[coproduct]] in [[Set]]
$$
  |S_1| + |S_2| := | S_1 \sqcup S_2|
  \,.
$$

Likewise, , the  **product** of their cardinalities is the cardinality of their [[product]] in [[Set]]
$$
  |S_1| \cdot |S_2| := | S_1 \times S_2|
  \,.
$$

In so far as the [[hom-set]] $S_1^{S_2}$ exists (as a set),
the exponentiation of $|S_1|$ by $|S_2|$ is its cardinality
$$
  |S_1|^{|S_2|} := | Set(S_1,S_2)  |
  \,.
$$

In particular, we have $2^{|S|}$, which (assuming the law of [[excluded middle]]) is the cardinality of the [[power set]] $P(S)$.

A cardinal $|S_1|$ is said to be **smaller than or equal to** another cardinal $|S_2|$ precisely if there exists an [[injection]] of the corresponding sets
$$
  (|S_1| \leq |S_2|)
  \Leftrightarrow
  (\exist (S_1 \hookrightarrow S_2))
  \,.
$$
This is equivalent to the existence of a [[surjection]] $S_2 \to S_1$.  The Schroeder-Bernstein Theorem asserts that if $|S_1|\le |S_2|$ and $|S_2|\le |S_1|$, then $|S_1|=|S_2|$ (that is, $S_1$ and $S_2$ are bijective).


# Properties #

* With the [[order]]ing as above, cardinals are [[well-order|well-ordered]] (assuming the axiom of choice).  In particular, every cardinal has a [[successor]] cardinal (the next smallest one), sometimes written $\pi^+$.

* It is traditional to write $\aleph_0$ for the first infinite cardinal (the cardinality of the natural numbers), $\aleph_1$ for the next (the first uncountable cardinality), and so on.  In this way every cardinal (assuming choice) is labeled $\aleph_\mu$ for a unique [[ordinal]] $\mu$, with $(\aleph_\mu))^+ = \aleph_{\mu+1}$.

* For every cardinal $\pi$, we have $2^\pi \gt \pi$ (this is sometimes called "Cantor's theorem").  The question of whether $2^{\aleph_n} = \aleph_{n+1}$ is called the [[continuum hypothesis]].

* For every transfinite cardinal $\pi$ we have $\pi+\pi = \pi$ and $\pi \cdot \pi = \pi$.


# Properties of cardinals #

A transfinite cardinal $\pi$ is **regular** if no set of cardinality $\pi$ is the union of fewer than $\pi$ sets of cardinality less than $\pi$.  Equivalently, $\pi$ is regular if given a function $P \to X$ (regarded as a family $\{P_x\}_{x\in X}$) such that $|X| \lt \pi$ and $|P_x| \lt \pi$ for all $x \in X$, then $|P| \lt \pi$.  Again equivalently, $\pi$ is regular if the category $\Set_{\lt\pi}$ of sets of cardinality $\lt\pi$ has all [[colimit]]s of size $\lt\pi$.  The [[successor]] of any infinite cardinal, such as $\aleph_1$, is a regular cardinal.

A cardinal is called **singular** if it is not regular.  For instance, $\aleph_\omega = \bigcup_{n\in \mathbb{N}} \aleph_n$ is singular, more or less by definition, since $\aleph_n\lt\aleph_\omega$ and $|\mathbb{N}| = \aleph_0 \lt\aleph_\omega$.

A **limit cardinal** is one which is not a successor of any other cardinal.  Note that _every_ cardinal is a limit [[ordinal]] (in the picture where cardinals are identified with certain ordinals).

A **strong limit cardinal** is a cardinal $\pi$ such that if $\lambda\lt \pi$, then $2^\lambda\lt\pi$, for any cardinal $\lambda$. Since $\lambda^+ \le 2^\lambda$, any strong limit is a limit. Conversely, assuming the [[continuum hypothesis]], every limit is a strong limit.  Since $2^\lambda$ is the cardinality of the [[power set]] $P(\lambda)$, a cardinal $\pi$ is a strong limit iff the category $\Set_{\lt\pi}$ is an elementary [[topos]].

An [[inaccessible cardinal]] is any (usually uncountable) regular strong limit cardinal.  A **weakly inaccessible cardinal** is a regular limit cardinal.


#References#

For a generalization of cardinality from sets to [[groupoid]]s see [[groupoid cardinality]].
