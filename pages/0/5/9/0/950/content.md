
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

An alternative definition of finite mathematics is as the mathematics of [[FinSet]]. This includes the basic arithmetic of [[natural numbers]], since these are the [[cardinal numbers|cardinalities]] of finite sets. This may seem contradictory to the entire conception of "finite mathematics", since the [[natural numbers]] form an infinite set. The way out is to state that the natural numbers don't form a set (or class) at all; instead, they are formally defined outside of the [[set theory]] via an auxiliary theory like [[primitive recursive arithmetic]]. This phenomenon is similar to defining the [[universe hierarchy]] of [[Russell universes]] or [[Coquand universes]] in [[dependent type theory]] without a separate [[type]] [[judgment]], where the natural numbers used in the universe indices are not elements of a type, but rather formally defined outside of the type theory using some other theory. 

### $\pi$-finite mathematics

In [[homotopy type theory]], another possibility is available: $\pi$-finite mathematics, which can be said to be the study of only the $n$-[[truncated]] [[pi-finite types]] for $n:\mathbb{N}$, which have finite homotopy groups, and type operations that preserve finiteness. Finite sets are just finite 0-truncated tame homotopy types in homotopy type theory. Certain type operations do not preserve tameness, such as [[suspensions]] and [[homotopy pushouts]], and so wouldn't be part of finite mathematics. This extends traditional finite mathematics based in set theoretic foundations to more modern fields such as [[higher category theory]] and [[homotopy theory]]. Just as the cardinalities of finite sets are [[natural numbers]] (finite set cardinalities), the [[groupoid cardinality|cardinalities]] of these $n$-truncated homotopy types are positive [[rational numbers]]. 

### Neutral finite mathematics

One definition of finite mathematics is **neutral finite mathematics**; i.e. mathematics done internally to an [[elementary topos]] (constructively) or [[Boolean topos]] (classically), but which does not assume either the [[axiom of infinity]] or the [[axiom of finiteness]]. There are no [[natural numbers]]; instead one works directly with the [[finite sets]] in neutral finite mathematics in neutral finite mathematics. 

In particular, in the [[internal logic|internal]] [[type theory]] of neutral finite mathematics, while one can show that arithmetic statements of individual finite sets is true, such as $\mathbb{2} + \mathbb{2} \simeq \mathbb{2} \times \mathbb{2}$ given the [[boolean domain]] $\mathbb{2}$, one cannot show that $A + \emptyset \simeq A$ for all finite sets $A$ - because types in the internal type theory aren't [[free variables]]. 

Alternatively, one can attempt to approximate arithmetic in the natural numbers by considering increasing long [[tuples]] of digits - elements of a finite set $D$, via the inclusions

$$\mathbb{1} \hookrightarrow D \hookrightarrow D \times D \hookrightarrow D \times D \times D \hookrightarrow \ldots$$

The non-negative [[rational numbers]] do not exist in neutral finite mathematics. However, given a [[finite group]] $G$ as an [[action]] on a set $X$, one can assume as a separate axiom the existence of the [[action groupoid]] of $G // X$, which corresponds to the [[fraction]] $m/n$ where $m$ is the cardinality of $G$ and $n$ is the cardinality of $X$. This means one can instead work with action groupoids for rational arithmetic. Externally, this requires moving from an [[elementary topos]] or [[Boolean topos]] to an [[(infinity,1)-category|$(\infty, 1)$-category]] which has [[finite limits]], [[power sets]], and action groupoids, since in general groupoids are not sets unless they are [[discrete groupoids|discrete]]. 

Unfortunately, trying to encode the negative [[integers]] directly as set-like objects seems to require infinity, since infinity is inherent in the [[sphere spectrum]] $\lim_{n \to \infty} \Omega^n S^n$ (which is kind of like [[FinSet]] but with negative [[cardinalities]]) from the fact that the [[sphere spectrum]] is not $\pi$-finite. Furthermore, any attempt to axiomatize the sphere spectrum as the initial [[E-infinity ring]] will result in [[coherence law|coherence issues]] from the fact that the syntax cannot handle infinite structure without the natural numbers. 

However, one can attempt to approximate arithmetic in the integers by considering increasing long [[tuples]] of digits - elements of a finite set $D$ - with a sign bit at the beginning of the tuple, via the inclusions

$$\mathbb{2} \hookrightarrow \mathbb{2} \times D \hookrightarrow \mathbb{2} \times D \times D \hookrightarrow \mathbb{2} \times D \times D \times D \hookrightarrow \ldots$$

## See also

* [[predicative mathematics]]

* [[constructive mathematics]]

* [[paraconsistent mathematics]]

* [[Nelson arithmetic]]

## References

* [[Edward Nelson]], _Warning Signs of a Possible Collapse of Contemporary Mathematics_ (~2011) &lbrack;[pdf](https://web.math.princeton.edu/~nelson/papers/warn.pdf), [[Nelson-WarningSigns.pdf:file]]&rbrack;

* Manuel Bremer, *Inconsistent Mathematics*, ([slides](https://www.mbph.de/Logic/Para/InconsistentMathematics.pdf))

[[!redirects finite mathematics]]

[[!redirects finitist mathematics]]
[[!redirects finitism]]
[[!redirects ultrafinitism]]