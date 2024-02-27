
# Finite mathematics
* table of contents
{: toc}

## Idea

__Finite mathematics__ is the [[mathematics]] of [[finite sets]].  The term is sometimes used more broadly for *[[discrete mathematics]]*.

We may say that finite mathematics is mathematics done [[internalization|internal]] to the category [[FinSet]] of finite sets or the mathematics of $\Fin\Set$ itself. The latter (but not the former) includes the basic arithmetic of [[natural numbers]], since these are the [[cardinal numbers|cardinalities]] of finite sets; we can go as far as [[rational numbers]] this way, but not [[real numbers]]. 

Finite mathematics also includes a great deal of [[combinatorics]], basic [[algebra]], and elementary [[formal logic]], although not many advanced topics.

## Finitism

In the [[foundations]] of mathematics and in [[philosophy of mathematics]], __finitism__ is the [[philosophy|philosophical]] sentiment that one "should" do only finite mathematics.  In a weak sense, one should not assume the [[axiom of infinity]]; in a strong sense, one should even deny it by an axiom of finiteness.  This makes it impossible to do [[analysis]] as we normally understand it.

Finitism (in the weak sense of not accepting an axiom of infinity) is essentially the mathematics that can be done internal to an arbitrary [[boolean topos]] (at least if one is not also being [[predicative mathematics|predicative]] or [[constructive mathematics|constructive]]).  For [[constructive mathematics]] as usually practised, one goes beyond finitism by positing a [[natural numbers object]].

Although often considered an extreme form of constructivism, finitism in the strong sense (actually denying the axiom of infinity) can make [[excluded middle]] and even the [[axiom of choice]] constructively acceptable (and similarly make [[power sets]] predicatively acceptable).  This is because even constructivists agree that these are true in $\Fin\Set$; it\'s the extension of them to [[infinite set]]s that the first constructivists objected to.

__Ultrafinitism__ is an even more extreme form of finitism, in which one doubts the existence of certain very large natural numbers. The theory of ultrafinite mathematics is most well developed by [[Edward Nelson]] in [[Nelson arithmetic]]. Foundational systems such as [[soft linear logic]] can also be argued to have an ultrafinitist flavor. 

This is also true of foundational systems using [[paraconsistent logic]], where [[paraconsistent arithmetics]] can have only a finite number of natural numbers. In particular, there is a paraconsistent version of the [[Löwenheim-Skolem theorem]], which states: 

> Any mathematical theory presented in first order logic has a finite paraconsistent model.

For the opinionated espousal of finitism (and much else), one can hardly do better than the [Opinions](http://www.math.rutgers.edu/~zeilberg/OPINIONS.html) of [[Doron Zeilberger]].

### The mathematics of FinSet

One definition of finite mathematics is as the mathematics of [[FinSet]]. This includes the basic arithmetic of [[natural numbers]], since these are the [[cardinal numbers|cardinalities]] of finite sets. This may seem contradictory to the entire conception of "finite mathematics", since the [[natural numbers]] form an infinite set. The way out is to state that the natural numbers don't form a set (or class) at all; instead, they are formally defined outside of the [[set theory]] via an auxiliary theory like [[primitive recursive arithmetic]]. This phenomenon is similar to defining the [[universe hierarchy]] of [[Russell universes]] or [[Coquand universes]] in [[dependent type theory]] without a separate [[type]] [[judgment]], where the natural numbers used in the universe indices are not elements of a type, but rather formally defined outside of the type theory using some other theory. 

### Neutral finite mathematics

An alternative definition of finite mathematics is **neutral finite mathematics**; i.e. mathematics done internally to an [[elementary topos]] (constructively) or [[Boolean topos]] (classically), but which does not assume either the [[axiom of infinity]] or the [[axiom of finiteness]]. There are no [[natural numbers]]; instead one works directly with the [[finite sets]] in neutral finite mathematics in neutral finite mathematics. 

Alternatively, one can attempt to approximate arithmetic in the natural numbers by considering increasing long [[tuples]] of digits - elements of a [[finite set]] $D$, via the inclusions

$$\mathbb{1} \hookrightarrow D \hookrightarrow D \times D \hookrightarrow D \times D \times D \hookrightarrow \ldots$$

In particular, in the [[internal logic|internal]] [[type theory]] of neutral finite mathematics, since types in the internal type theory aren't [[free variables]], one cannot quantify over finite sets, which means that many concepts in elementary number theory cannot be internally defined in neutral finite mathematics for finite sets. Examples include: 

* Unlike the case for division of [[natural numbers]], which can be defined via [[induction]] or [[recursion]] on the [[natural numbers]], the [[division]] of two [[finite sets]] cannot be defined via the usual set-theoretic operations on [[finite sets]] in neutral finite mathematics. Instead, one needs to add additional set constructors to neutral finite mathematics which state that given finite set $A$ and finite [[pointed set]] $B$ with an element $p:B$, one can construct finite sets $A \div B$ and $A\ \%\ B$ with bijections
$$A \simeq ((B \times (A \div B)) + (A\ \%\ B)) \qquad (B \hookrightarrow A\ \%\ B) \simeq \emptyset$$
meaning that it is no longer neutral finite mathematics. 

* As a result, the analogues of the notions of [[divisibility relation]], [[divisor]], [[greatest common divisor]], [[least common multiple]], [[prime number]], [[prime factorization]], and so forth, cannot be internally defined for finite sets in neutral finite mathematics. 

* Furthermore, the definition of [[prime number]] requires quantification over finite sets, which is impossible in the internal logic since there are no finite set free variables. (The collection of finite sets are infinite, and so internally quantifying over that collection implies that one has an infinite collection in the foundations, contrary to finitism.) From this internal perspective, [[Doron Zeilberger]], despite his [Opinions](http://www.math.rutgers.edu/~zeilberg/OPINIONS.html), is not finitist since he is able to define prime numbers and work with them (cf. [Zeilberger 01](#Zeilberger01)), which requires some notion of quantification over finite sets to define finite sets with prime number [[cardinality]], or otherwise the infinite set of natural numbers so that one can internally quantify over them for the definition of prime number. 

* One can prove that given individual finite sets $A$ and $B$ that there is a bijection $A + B \simeq B + A$, but one cannot prove that there is a bijection $A + B \simeq B + A$ for all $A$ and $B$, because there are no finite set free variables in the internal logic. The same goes for any arithmetic or order-theoretic property for the set-theoretic operations on finite sets. Syntactically, the properties for finite sets are given by [[inference rules]] with at least one [[hypothesis]], rather than [[axioms]] as would be for the [[natural numbers]]: 
$$\frac{A \; \mathrm{set} \quad p:\mathrm{isFinite}(A) \quad B \; \mathrm{set} \quad q:\mathrm{isFinite}(A)}{\mathrm{comm}_{A + B}(p, q):A + B \simeq B + A}$$

* In [[predicative mathematics|predicative]] [[constructive mathematics|constructive]] neutral finite mathematics; i.e. internal to a [[Pi-pretopos|$\Pi$-pretopos]] without the [[natural numbers]] or a [[set of truth values]], one can't even define when a [[set]] is a [[finite set]], and thus one cannot do any natural numbers arithmetic in the guise of finite set arithmetic at all. Even basic arithmetic properties of the natural numbers like the [[cancellative monoid|cancellativity of multiplication]] don't apply to arbitrary sets in the absence of [[excluded middle]] (cf. [Swan 18](https://arxiv.org/abs/1804.04490)), and arbitrary sets only form a [[preorder]], rather than a [[total preorder]]. 

### $\pi$-finite mathematics

In [[homotopy type theory]], another possibility is available: $\pi$-finite mathematics, which can be said to be the study of only the $n$-[[truncated]] [[pi-finite types]] for $n:\mathbb{N}$, which have finite homotopy groups, and type operations that preserve finiteness. Finite sets are just finite 0-truncated tame homotopy types in homotopy type theory. Certain type operations do not preserve tameness, such as [[suspensions]] and [[homotopy pushouts]], and so wouldn't be part of finite mathematics. This extends traditional finite mathematics based in set theoretic foundations to more modern fields such as [[higher category theory]] and [[homotopy theory]]. Just as the cardinalities of finite sets are [[natural numbers]] (finite set cardinalities), the [[groupoid cardinality|cardinalities]] of these $n$-truncated homotopy types are positive [[rational numbers]]. 

## See also

* [[predicative mathematics]]

* [[constructive mathematics]]

* [[paraconsistent mathematics]]

* [[Nelson arithmetic]]

## References

* {#Zeilberger01} [[Doron Zeilberger]], *“Real” Analysis is a Degenerate Case of Discrete Analysis*, Transcript of a plenary talk delivered at the International Conference on Difference Equations and Applications (ICDEA 2001), Augsburg, Germany, Aug. 1, 2001. &lbrack;[pdf](https://sites.math.rutgers.edu/~zeilberg/mamarim/mamarimPDF/hersh90.pdf)&rbrack;

* [[Edward Nelson]], _Warning Signs of a Possible Collapse of Contemporary Mathematics_ (~2011) &lbrack;[pdf](https://web.math.princeton.edu/~nelson/papers/warn.pdf), [[Nelson-WarningSigns.pdf:file]]&rbrack;

* Manuel Bremer, *Inconsistent Mathematics*, ([slides](https://www.mbph.de/Logic/Para/InconsistentMathematics.pdf))

[[!redirects finite mathematics]]

[[!redirects neutral finite mathematics]]

[[!redirects finitist mathematics]]
[[!redirects finitism]]
[[!redirects ultrafinitism]]