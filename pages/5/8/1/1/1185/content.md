# Idea #

The _cardinal numbers_ (or just _cardinals_) constitute a generalisation of a [[natural number|natural numbers]]s to possibly infinite magnitudes.  Specifically, cardinal numbers generalise the concept of 'the number of ...'.  In particular, the number of natural numbers is the first infinite cardinal number.

# Definition #

Na&#239;vely, a **cardinal number** should be an [[isomorphism]] class of [[set]]s, and the **cardinality** of a set $S$ would be its isomorphism class.  That is:
1. every set has a unique cardinal number as its cardinality;
1. every cardinal number is the cardinality of some set;
1. two sets have the same cardinality if and only if they are isomorphic as sets.

Then a **finite cardinal** is the cardinality of a [[finite set]], while an **infinite cardinal** or **transfinite cardinal** is the cardinality of an [[infinite set]].  (If you interpret both terms in the strictest sense, then there may be cardinals that are neither finite nor infinite, without some form of the [[axiom of choice]]).

Taking this definition literally in material [[set theory]], each cardinal is then a [[proper class]] (so one could not make further sets using them as elements).  For this reason, in axiomatic set theory one usually defines a cardinal number as a particular representative of this equivalence class.  There are two ways to do this:

* The __cardinality__ of a set $S$ is the set of all [[ordinal number]]s (themselves usually defined following von Neumann) less than the ordinal rank of every [[well-order]] on $S$; then a __cardinal number__ is any cardinality.  On well-orderable sets, this cardinality function satisfies (1--3), but one needs the [[axiom of choice]] (or at least the [[well-ordering theorem]]) to prove that every set is well-orderable.
* Alternatively, the __cardinality__ of a set $X$ is the set of all well-founded [[pure set]]s that are isomorphic as sets to $X$ and such that no pure set of smaller hereditary rank is isomoprhic to $X$.  On those sets that are isomorphic to some well-founded set in the [[von Neumann hierarchy]], this cardinality function satisfies (1--3), but one needs the [[axiom of foundation]] to prove that every set is isomorphic to a well-founded set.

In the absence of the appropriate axioms, the definitions above can still be used to define __well-ordered cardinals__ and __well-founded cardinals__, respectively.

From the perspective of structural [[set theory]], it is [[evil]] to care about distinctions between isomorphic objects, and unnecessary to insist on a canonical choice of representatives for isomorphism classes.  Therefore, from this point of view it is natural to simply say:

* A __cardinal__ is a [[set]] (that is, an object of [[Set]]).

However, one still may need sets of cardinals, that is sets that serve as the target of a cardinality function satisfying (1--3) on any small class of sets.  One defines this as a [[quotient set]] of the set of those sets under consideration.

# Cardinal arithmetic #

For $S$ a [[set]], write $|S|$ for its cardinality. Then the standard operations in the [[category]] [[Set]] induce arithmetic operations on cardinal numbers:

For $S_1$ and $S_2$ two sets, the **sum** of their cardinalities is the cardinality of their [[disjoint union]], the [[coproduct]] in $Set$:
$$
  |S_1| + |S_2| := |S_1 \amalg S_2|
  \,.
$$

More generally, given any family $(S_i)_{i: I}$ of sets indexed by a set $I$, the **sum** of their cardinalities is the cardinality of their disjoint union:
$$
  \sum_{i: I} |S_i| := |\coprod_{i: I} S_i|
  \,.
$$

Likewise, the **product** of their cardinalities is the cardinality of their [[cartesian product]], the [[product]] in $Set$:
$$
  |S_1| \, |S_2| := |S_1 \times S_2|
  \,.
$$

More generally again, given any family $(S_i)_{i: I}$ of sets indexed by a set $I$, the **product** of their cardinalities is the cardinality of their cartesian product:
$$
  \prod_{i: I} |S_i| := |\prod_{i: I} S_i|
  \,.
$$

Also, the **exponential** of one cardinality raised to the power of the other is the cardinality of their [[function set]], the [[exponential object]] in $Set$:
$$
  |S_1|^{|S_2|} := |Set(S_2,S_1)|
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
