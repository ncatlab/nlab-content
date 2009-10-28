# Idea #

The _cardinal numbers_ (or just _cardinals_) constitute a generalisation of a [[natural number|natural numbers]] to possibly infinite magnitudes.  Specifically, cardinal numbers generalise the concept of 'the number of ...'.  In particular, the number of natural numbers is the first infinite cardinal number.

# Definition #

Na&#239;vely, a **cardinal number** should be an [[isomorphism]] class of [[sets]], and the **cardinality** of a set $S$ would be its isomorphism class.  That is:
1. every set has a unique cardinal number as its cardinality;
1. every cardinal number is the cardinality of some set;
1. two sets have the same cardinality if and only if they are isomorphic as sets.

Then a **finite cardinal** is the cardinality of a [[finite set]], while an **infinite cardinal** or **transfinite cardinal** is the cardinality of an [[infinite set]].  (If you interpret both terms in the strictest sense, then there may be cardinals that are neither finite nor infinite, without some form of the [[axiom of choice]]).

Taking this definition literally in material [[set theory]], each cardinal is then a [[proper class]] (so one could not make further sets using them as elements).  For this reason, in axiomatic set theory one usually defines a cardinal number as a particular representative of this equivalence class.  There are several ways to do this:

* The __cardinality__ of a set $S$ is the smallest possible ordinal rank of any [[well-order]] on $S$.  In other words, it is the smallest [[ordinal number]] (usually defined following von Neumann) which can be put in bijection with $S$.  A __cardinal number__ is then any cardinality, i.e. any ordinal which is not in bijection with any smaller ordinal.

  * On well-orderable sets, this cardinality function satisfies (1--3), but one needs the [[axiom of choice]] (precisely, the [[well-ordering theorem]]) to prove that every set is well-orderable.  This approach is probably the most common one in the presence of the axiom of choice.

  * In the absence of [[excluded middle]], when the "correct" definition of well-order is different from the usual one (and so "the least ordinal such that ..." may not exist), a better definition of the cardinality of $S$ is as the set of all [[ordinal numbers]] less than the ordinal rank of every [[well-order]] on $S$.

* Alternatively, we can define the __cardinality__ of a set $X$ to be the set of all well-founded [[pure sets]] that are isomorphic as sets to $X$ and such that no pure set of smaller hereditary rank (that is, which occurs earlier in the [[von Neumann hierarchy]]) is isomorphic to $X$.

  * On those sets that are isomorphic to some well-founded set, this cardinality function satisfies (1--3), but one needs some assumption to prove that every set is isomorphic to a well-founded set.  (This will follow directly from the [[axiom of foundation]]; it will also follow from the [[axiom of choice]], since then every set is isomoprhic to a von Neumann ordinal.)

In the absence of the appropriate axioms, the definitions above can still be used to define __well-ordered cardinals__ and __well-founded cardinals__, respectively.

From the perspective of structural [[set theory]], it is [[evil]] to care about distinctions between isomorphic objects, and unnecessary to insist on a canonical choice of representatives for isomorphism classes.  Therefore, from this point of view it is natural to simply say:

* A __cardinal__ is a [[set]] (that is, an object of [[Set]]).

However, one still may need sets of cardinals, that is sets that serve as the target of a cardinality function satisfying (1--3) on any (small) collection of sets.  One can construct this as a [[quotient set]] of that collection.

+--{: .query}
_Mike_: I don't understand that last paragraph.

_Toby_:  The reason why material set theorists go to all this trouble to define cardinal numbers as sets rather than proper classes is so that they can make them elements of sets.  This isn\'t just for fun; if you have a small collection of sets, then you want to form the set of their cardinalities.  Fortunately, this is easy to do up to isomorphism, which is all that we need.

I think that my wording was a bit confusing, so perhaps it\'s clearer now.

_Roger Witte_
First of all sorry if I am posting in the wrong place

While thinking about graphs, I wanted to define them as subobjects of naive cardinal **2** and this got me thinking about the behaviour of the full subcategories of **Set** defined by isomorphism classes.  These categories turned out to be more interesting than I had expected.

If the background set theory is ZFC or similar, these are all large but locally small categories with all hom sets being isomorphic.  They all contain the same number of objects (except **0**, which contains one object and no non-identity morphisms) and are equinumerous with **Set**.  Each hom Set contains 2^N arrows.  In the finite case N! of the morphisms in a particular hom set are isomorphisms.  In particular, only **0** and **1** are groupoids.  I haven't worked out how this extends to infinite cardinalities, yet.

If the background theory is NF, then they are set and **1** is smaller than **Set**.  I haven't yet worked out how **2** compares to **1**.  I need to brush up on my NF to see how NF and category theory interact.

I am acutely aware that NF/NFU is regarded as career suicide by proffesional mathematicians, but, fortunately, I am a proffesional transport planner, not a mathematician.
=--

Lowercase Greek letters starting from $\kappa$ are often used for cardinal numbers.

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

In particular, we have $2^{|S|}$, which (assuming the law of [[excluded middle]]) is the cardinality of the [[power set]] $P(S)$.  In [[constructive mathematics|constructive]] (but not [[predicative mathematics|predicative]]) mathematics, the cardinality of the power set is $\Omega^{|S|}$, where $\Omega$ is the cardinality of the set of [[truth values]].

The usual way to define an ordering on cardinal numbers is that $|S_1| \leq |S_2|$ if there exists an [[injection]] from $S_1$ to $S_2$:
$$
  (|S_1| \leq |S_2|)
  \;:\Leftrightarrow\;
  (\exists (S_1 \hookrightarrow S_2))
  \,.
$$
Classically, this is almost equivalent to the existence of a [[surjection]] $S_2 \to S_1$, except when $S_1$ is [[empty set|empty]].  Even restricting to [[inhabited sets]], these are not equivalent conditions in [[constructive mathematics]], so one may instead define that $|S_1| \leq |S_2|$ if there exists a [[subset]] $X$ of $S_2$ and a surjection $X \to S_1$.  Another alternative is to require that $S_1$ (or $X$) be a [[decidable subset]] of $S_2$.  All of these definitions are equivalent using [[excluded middle]].

This order relation is [[antisymmetric relation|antisymmetric]] (and therefore a [[partial order]]) by the (Cantor--)Schroeder--Bernstein Theorem (proved by Cantor using the [[well-ordering theorem]], then proved by Schroeder and Bernstein without it).  That is, if $S_1 \hookrightarrow S_2$ and $S_2 \hookrightarrow S_1$ exist, then a bijection $S_1 \cong S_2$ exists.  This theorem is not constructively valid, however.

The well-ordered cardinals are [[well-order|well-ordered]] by the ordering $\lt$ on [[ordinal numbers]].  Assuming the [[axiom of choice]], this agrees with the previous order in the sense that $\kappa \leq \lambda$ iff $\kappa \lt \lambda$ or $\kappa = \lambda$.  Another definition is to define that $\kappa \lt \lambda$ if $\kappa^+ \leq \lambda$, using the successor operation below.

The __[[successor]]__ of a well-ordered cardinal $\kappa$ is the smallest well-ordered cardinal larger than $\kappa$.  Note that (except for finite cardinals), this is different from $\kappa$\'s successor as an [[ordinal number]].  We can also take successors of arbitrary cardinals using the operation of [[Hartog's number]], although this won\'t quite have the properties that we want of a successor without the axiom of choice.


# Properties #

* It is traditional to write $\aleph_0$ for the first infinite cardinal (the cardinality of the natural numbers), $\aleph_1$ for the next (the first uncountable cardinality), and so on.  In this way every cardinal (assuming choice) is labeled $\aleph_\mu$ for a unique [[ordinal number]] $\mu$, with $(\aleph_\mu))^+ = \aleph_{\mu+1}$.

* For every cardinal $\pi$, we have $2^\pi \gt \pi$ (this is sometimes called [[Cantor's theorem]]).  The question of whether $2^{\aleph_n} = \aleph_{n+1}$ is called the [[continuum hypothesis]].

* For every transfinite cardinal $\pi$ we have $\pi+\pi = \pi$ and $\pi \cdot \pi = \pi$.


# Properties of cardinals #

A transfinite cardinal $\pi$ is **regular** if no set of cardinality $\pi$ is the union of fewer than $\pi$ sets of cardinality less than $\pi$.  Equivalently, $\pi$ is regular if given a function $P \to X$ (regarded as a family $\{P_x\}_{x\in X}$) such that $|X| \lt \pi$ and $|P_x| \lt \pi$ for all $x \in X$, then $|P| \lt \pi$.  Again equivalently, $\pi$ is regular if the category $\Set_{\lt\pi}$ of sets of cardinality $\lt\pi$ has all [[colimits]] of size $\lt\pi$.  The [[successor]] of any infinite cardinal, such as $\aleph_1$, is a regular cardinal.

A cardinal is called **singular** if it is not regular.  For instance, $\aleph_\omega = \bigcup_{n\in \mathbb{N}} \aleph_n$ is singular, more or less by definition, since $\aleph_n\lt\aleph_\omega$ and $|\mathbb{N}| = \aleph_0 \lt\aleph_\omega$.

A **limit cardinal** is one which is not a successor of any other cardinal.  Note that _every_ cardinal is a limit [[ordinal number|ordinal]] (in the picture where cardinals are identified with certain ordinals).

A **strong limit cardinal** is a cardinal $\pi$ such that if $\lambda\lt \pi$, then $2^\lambda\lt\pi$, for any cardinal $\lambda$. Since $\lambda^+ \le 2^\lambda$, any strong limit is a limit. Conversely, assuming the [[continuum hypothesis]], every limit is a strong limit.  Since $2^\lambda$ is the cardinality of the [[power set]] $P(\lambda)$, a cardinal $\pi$ is a strong limit iff the category $\Set_{\lt\pi}$ is an elementary [[topos]].

An [[inaccessible cardinal]] is any (usually uncountable) regular strong limit cardinal.  A **weakly inaccessible cardinal** is a regular limit cardinal.


#References#

For a generalization of cardinality from sets to [[groupoids]] see [[groupoid cardinality]].

+-- {: .query}
_Stephen_: What is a _good standard_ references on this topic?

I have found

* _Sets, Logic and Categories_ by Peter J Cameron (ISBN: 1-85233-056-2 )

a very readable account of ZFC and the definitions of both Ordinal and Cardinal numbers.  However, I am not convinced this reference would be the most respected in this area. 

_Toby_:  It looks like you\'re asking about cardinal numbers in general rather than groupoid cardinality.

Any serious reference on set theory should cover cardinal numbers.  The long-established respected tome is Thomas Jech\'s _[Set Theory](; there are also some references listed at [MathWorld]() and [the English Wikipedia]().

Any *standard* approach will start from a material set theory, such as ZFC; we tend to prefer structural set theory here.  (See [[set theory]].)  Since cardinality is isomorphism invariant (which is kind of the whole point), it\'s easy to interpret the standard material structurally, but the basic definitions will be different.  If you\'re looking for a standard reference on cardinality from a structural foundation, I can\'t help you; there may not be any.

By the way, if you want to be sure that people see your questions in a timely manner, then it\'s best if you make a note of it [here](); I just did that (which you can find by looking for your name).  You did *ask* the question in the right place, but now it\'s possible that more people will come to *read* it!
=--


[[!redirects cardinality]]
[[!redirects cardinal numbers]]
[[!redirects cardinal]]
[[!redirects cardinals]]
[[!redirects cardinalities]]
[[!redirects regular cardinal]]