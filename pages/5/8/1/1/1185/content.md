

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

The _cardinal numbers_ (or just _cardinals_) constitute a generalisation of [[natural number|natural numbers]] to [[numbers]] of possibly infinite magnitudes.  Specifically, cardinal numbers generalise the concept of 'the number of ...'.  In particular, the number of natural numbers is the first infinite cardinal number.

## Definition 

Na&#239;vely, a **cardinal number** should be an [[isomorphism]] class of [[sets]], and the **cardinality** of a set $S$ would be its isomorphism class.  That is:

1. every set has a unique cardinal number as its cardinality;
2. every cardinal number is the cardinality of some set;
3. two sets have the same cardinality if and only if they are isomorphic as sets.

Then a **finite cardinal** is the cardinality of a [[finite set]], while an **infinite cardinal** or **transfinite cardinal** is the cardinality of an [[infinite set]].  (If you interpret both terms in the strictest sense, then there may be cardinals that are neither finite nor infinite, without some form of the [[axiom of choice]]).

Taking this definition literally in material [[set theory]], each cardinal is then a [[proper class]] (so one could not make further sets using them as elements).  For this reason, in axiomatic set theory one usually defines a cardinal number as a particular representative of this [[equivalence class]].  There are several ways to do this:

* The __cardinality__ of a set $S$ is the smallest possible ordinal rank of any [[well-order]] on $S$.  In other words, it is the smallest [[ordinal number]] (usually defined following von Neumann) which can be put in bijection with $S$.  A __cardinal number__ is then any cardinality, i.e. any ordinal which is not in bijection with any smaller ordinal.

  * On well-orderable sets, this cardinality function satisfies (1--3), but one needs the [[axiom of choice]] (precisely, the [[well-ordering theorem]]) to prove that every set is well-orderable.  This approach is probably the most common one in the presence of the axiom of choice.

  * In the absence of [[excluded middle]], when the "correct" definition of well-order is different from the usual one (and so "the least ordinal such that ..." may not exist), a better definition of the cardinality of $S$ is as the set of all [[ordinal numbers]] less than the ordinal rank of every [[well-order]] on $S$.

* Alternatively, we can define the __cardinality__ of a set $X$ to be the set of all well-founded [[pure sets]] that are isomorphic as sets to $X$ and such that no pure set of smaller hereditary rank (that is, which occurs earlier in the [[von Neumann hierarchy]]) is isomorphic to $X$.

  * On those sets that are isomorphic to some well-founded set, this cardinality function satisfies (1--3), but one needs some assumption to prove that every set is isomorphic to a well-founded set.  (This will follow directly from the [[axiom of foundation]]; it will also follow from the [[axiom of choice]], since then every set is isomorphic to a von Neumann ordinal.)

In the absence of the appropriate axioms, the definitions above can still be used to define __well-ordered cardinals__ and __well-founded cardinals__, respectively.

From the perspective of structural [[set theory]], caring about distinctions between isomorphic objects is at odds with the [[principle of equivalence]], and it is unnecessary to insist on a canonical choice of representatives for isomorphism classes.  Therefore, from this point of view it is natural to simply say:

* A __cardinal__ is a [[set]] (that is, an object of [[Set]]).

However, one still may need sets of cardinals, that is sets that serve as the target of a cardinality function satisfying (1--3) on any (small) collection of sets.  One can construct this as a [[quotient set]] of that collection.

Lowercase Greek letters starting from $\kappa$ are often used for cardinal numbers.

### In homotopy type theory

A **cardinal** in [[homotopy type theory]] is an element of the type of cardinals $\kappa \colon Card_\mathcal{U}$ relative to a universe $\mathcal{U}$. The type of cardinals is defined as the set-truncation of the type of sets $Set_\mathcal{U}$ relative to $\mathcal{U}$, $Card_\mathcal{U} \coloneqq \left| Set_\mathcal{U} \right|_0$ with $Set_\mathcal{U}$ defined as 

$$Set_\mathcal{U} \coloneqq \sum_{A:\mathcal{U}} \prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} \prod_{q:a =_A b} p =_{a =_A b} q$$

## Cardinal arithmetic 

### Definition

For $S$ a [[set]], write ${|S|}$ for its cardinality. Then the standard operations in the [[category]] [[Set]] induce [[arithmetic]] operations on cardinal numbers ("[[cardinal arithmetic]]"):

For $S_1$ and $S_2$ two sets, the **sum** of their cardinalities is the cardinality of their [[disjoint union]], the [[coproduct]] in $Set$:
$$
  {|S_1|} + {|S_2|} \coloneqq {|S_1 \amalg S_2|}
  \,.
$$

More generally, given any family $(S_i)_{i: I}$ of sets indexed by a set $I$, the **sum** of their cardinalities is the cardinality of their disjoint union:
$$
  \sum_{i: I} {|S_i|} \coloneqq {|\coprod_{i: I} S_i|}
  \,.
$$

Likewise, the **product** of their cardinalities is the cardinality of their [[cartesian product]], the [[product]] in $Set$:
$$
  {|S_1|} \, {|S_2|} \coloneqq {|S_1 \times S_2|}
  \,.
$$

More generally again, given any family $(S_i)_{i: I}$ of sets indexed by a set $I$, the **product** of their cardinalities is the cardinality of their cartesian product:
$$
  \prod_{i: I} {|S_i|} \coloneqq {|\prod_{i: I} S_i|}
  \,.
$$

Also, the **exponential** of one cardinality raised to the power of the other is the cardinality of their [[function set]], the [[exponential object]] in $Set$:
$$
  {|S_1|}^{|S_2|} \coloneqq {|Set(S_2,S_1)|}
  \,.
$$

In particular, we have $2^{|S|}$, which (assuming the law of [[excluded middle]]) is the cardinality of the [[power set]] $P(S)$.  In [[constructive mathematics|constructive]] (but not [[predicative mathematics|predicative]]) mathematics, the cardinality of the power set is $\Omega^{|S|}$, where $\Omega$ is the cardinality of the set of [[truth values]].

The usual way to define an ordering on cardinal numbers is that ${|S_1|} \leq {|S_2|}$ if there exists an [[injection]] from $S_1$ to $S_2$:
$$
  ({|S_1|} \leq {|S_2|})
  \;:\Leftrightarrow\;
  (\exists (S_1 \hookrightarrow S_2))
  \,.
$$
Classically, this is almost equivalent to the existence of a [[surjection]] $S_2 \to S_1$, except when $S_1$ is [[empty set|empty]].  Even restricting to [[inhabited sets]], these are not equivalent conditions in [[constructive mathematics]], so one may instead define that ${|S_1|} \leq {|S_2|}$ if there exists a [[subset]] $X$ of $S_2$ and a surjection $X \to S_1$.  Another alternative is to require that $S_1$ (or $X$) be a [[decidable subset]] of $S_2$.  All of these definitions are equivalent using [[excluded middle]].

This order relation is [[antisymmetric relation|antisymmetric]] (and therefore a [[partial order]]) by the [[Cantor–Schroeder–Bernstein theorem]] (proved by Cantor using the [[well-ordering theorem]], then proved by Schroeder and Bernstein without it).  That is, if $S_1 \hookrightarrow S_2$ and $S_2 \hookrightarrow S_1$ exist, then a bijection $S_1 \cong S_2$ exists.  This theorem is not constructively valid, however.

The well-ordered cardinals are [[well-order|well-ordered]] by the ordering $\lt$ on [[ordinal numbers]].  Assuming the [[axiom of choice]], this agrees with the previous order in the sense that $\kappa \leq \lambda$ iff $\kappa \lt \lambda$ or $\kappa = \lambda$.  Another definition is to define that $\kappa \lt \lambda$ if $\kappa^+ \leq \lambda$, using the successor operation below.

The __[[successor]]__ of a well-ordered cardinal $\kappa$ is the smallest well-ordered cardinal larger than $\kappa$.  Note that (except for finite cardinals), this is different from $\kappa$\'s successor as an [[ordinal number]].  We can also take successors of arbitrary cardinals using the operation of [[Hartog's number]], although this won\'t quite have the properties that we want of a successor without the axiom of choice.


### Properties 

* It is traditional to write [[ℵ]]${}_0$ for the first infinite cardinal (the cardinality of the [[natural numbers]]), $\aleph_1$ for the next (the first uncountable cardinality), and so on.  In this way every cardinal (assuming choice) is labeled $\aleph_\mu$ for a unique [[ordinal number]] $\mu$, with $(\aleph_\mu))^+ = \aleph_{\mu^+}$.

* For every cardinal $\pi$, we have $2^\pi \gt \pi$ (this is sometimes called [[Cantor's theorem]]).  The question of whether $2^{\aleph_0} = \aleph_{1}$ (or more generally whether $2^{\aleph_\mu} = \aleph_{\mu^+}$) is called Cantor's continuum problem; the assertion that this is the case is called the (generalized) [[continuum hypothesis]]. It is known that the continuum hypothesis is undecidable in [[ZFC]]. 

* For every transfinite cardinal $\pi$ we have (using the axiom of choice) $\pi + \pi = \pi$ and $\pi \cdot \pi = \pi$, so addition and multiplication are [[idempotent]].


## Properties of cardinals

* A transfinite cardinal $\pi$ is a **[[regular cardinal]]** if no set of cardinality $\pi$ is the union of fewer than $\pi$ sets of cardinality less than $\pi$.  Equivalently, $\pi$ is regular if given a function $P \to X$ (regarded as a family $\{P_x\}_{x\in X}$) such that ${|X|} \lt \pi$ and ${|P_x|} \lt \pi$ for all $x \in X$, then ${|P|} \lt \pi$.  Again equivalently, $\pi$ is regular if the category $\Set_{\lt\pi}$ of sets of cardinality $\lt\pi$ has all [[colimits]] of size $\lt\pi$.  The [[successor]] of any infinite cardinal, such as $\aleph_1$, is a regular cardinal.

* A cardinal is called **singular** if it is not regular.  For instance, $\aleph_\omega = \bigcup_{n\in \mathbb{N}} \aleph_n$ is singular, more or less by definition, since $\aleph_n \lt \aleph_\omega$ and ${|\mathbb{N}|} = \aleph_0 \lt \aleph_\omega$.

* A **limit cardinal** is one which is not a successor of any other cardinal.  Note that _every_ infinite cardinal is a limit [[ordinal number|ordinal]] (in the picture where cardinals are identified with certain ordinals).

* A **strong limit cardinal** is a cardinal $\pi$ such that if $\lambda \lt \pi$, then $2^\lambda \lt \pi$, for any cardinal $\lambda$. Since $\lambda^+ \le 2^\lambda$, any strong limit is a limit. Conversely, assuming the [[continuum hypothesis]], every limit is a strong limit.  Since $2^\lambda$ is the cardinality of the [[power set]] $P(\lambda)$, a cardinal $\pi$ is a strong limit iff the category $\Set_{\lt\pi}$ is an elementary [[topos]].

* An **[[inaccessible cardinal]]** is any (usually uncountable) regular strong limit cardinal.  A **weakly inaccessible cardinal** is a regular limit cardinal.

* A cardinal $\kappa$ is a **[[measurable cardinal]]** if some (hence any) set of cardinality $\kappa$ admits a two-valued [[measure]] which is $\kappa$-additive, or equivalently an [[ultrafilter]] which is $\kappa$-complete.



## Related concepts

* [[groupoid cardinality]]

* [[counting measure]]

* [[ordinal number]]


## References

The original article is

* {#Cantor1895} [[Georg Cantor]], _[[Beiträge zur Begründung der transfiniten Mengenlehre]]_, Math. Ann. 46 (1895) pp.481-512, reprinted from p. 282 on in [[Ernst Zermelo]] (ed.), _Georg Cantor -- Gesammelte Abhandlungen mathematischen und philosophischen Inhalts_, Springer Berlin 1932 ([online English translation](https://archive.org/details/contributionstof00cant))


The book

* Peter J Cameron, _Sets, Logic and Categories_  (ISBN: 1-85233-056-2 )

contains a very readable account of ZFC and the definitions of both ordinal and cardinal numbers.  

Any serious reference on set theory should cover cardinal numbers.  The long-established respected tome is 

* Thomas Jech _[Set Theory](http://books.google.com/books?id=pLxq0myANiEC)_; 

there are also some references listed at 

* [MathWorld](http://mathworld.wolfram.com/CardinalNumber.html) and 

* [the English Wikipedia](http://en.wikipedia.org/wiki/Cardinal_number).

A good introduction to infinite cardinals is:

* Frank R. Drake, _Set Theory: An Introduction to Large Cardinals_, Studies in Logic and the Foundations of Mathematics, vol. 76, Elsevier, 1974.

For a much deeper treatment, which assumes most of the material in Drake as a prerequisite, see:

* Akihiro Kanamori, _The Higher Infinite: Large Cardinals in Set Theory from Their Beginning, Springer, 2003.

This is a very readable and freely available historical introduction:

* Akihiro Kanamori and M. Magidor, The evolution of large cardinal axioms in set theory, in _Higher Set Theory_, Springer Lecture Notes in Mathematics 669, 1978.  ([pdf](http://math.bu.edu/people/aki/e.pdf))

*Standard* approaches start with a [[material set theory]], such as ZFC, whereas the approach here uses [[structural set theory]] as emphasized above.  Since cardinality is isomorphism-invariant, it is easy to interpret the standard material structurally, although the basic definitions will be different.  There does not seem to be a standard account of cardinality from within structural set theory.

For cardinal numbers in [[homotopy type theory]], see chapter 10 of

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

For a critical discussion of the history of the meaning of Cantor's "Kardinalen", see 

* [[William Lawvere]], _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_,

which argues that Cantor's original meaning of _set_ was more like what today is _[[cohesive]] set_ and that his _Kardinalen_ refer to the _underlying set_ (see at _[[flat modality]]_).

[[!redirects cardinal number]]
[[!redirects cardinal numbers]]
[[!redirects cardinal]]
[[!redirects cardinals]]
[[!redirects cardinality]]
[[!redirects cardinalities]]

[[!redirects limit cardinal]]
[[!redirects limit cardinals]]

[[!redirects strong limit cardinal]]
[[!redirects strong limit cardinals]]



