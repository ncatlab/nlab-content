A **(global) choice operator** is structure included in some [[foundations]] of [[mathematics]] which provides a uniform way to choose an element of every [[inhabited set|inhabited]] [[set]] or [[class]].

In [[David Hilbert|Hilbert]]'s original formulation, for any property $P(x)$ we can form a term $\varepsilon x.P(x)$ such that
$$\exists x.P(x) \;\Rightarrow\; P\big(\varepsilon x.P(x)\big).$$
In other words, if $P$ holds of anything at all, then it holds of the particular term $\varepsilon x.P(x)$.  A similar operator was used by [[Bourbaki]] and appears in [[FMathL]].

+--{: .query}
_Harry_: I think it should be noted that Hilbert and Bourbaki take the $\varepsilon$-operator, called $\tau$ in "Theory of Sets" to be a primitive symbol in a mathematical theory.  This has the advantage of also allowing the existential and universal quantifiers to be defined in terms of it, since $\exists x$ translates to $P(\varepsilon(P(x)))$.  The intuitive meaning behind the operator is that it returns a distinguished object for which the proposition is true, or if no such object exists, it returns a distinguished object for which it is not true.  Of course, the intuitive meaning can be misleading since the properties of the epsilon operator are governed by axioms stated in completely different terms.  Another wonderful usage of the global choice operator in Bourbaki is that we can easily show that paradoxical sets do not exist, since the definition of a set is given in terms of whether or not the relation defining the set is collectivizing.  It's quite powerful and makes a lot of set theory much easier to deal with.  
=--

One use of the choice operator is to eliminate undesirable details of implementation.  For example, if $P(x)$ is "$x$ is a Dedekind-complete totally ordered field," then we can define "the real numbers" to be $\varepsilon x.P(x)$.  Any of the numerous constructions of the [[real numbers]] can then be used to show that there exists an $x$ such that $P(x)$, after which point we can discard whichever explicit construction and work only with $\mathbb{R}=\varepsilon x.P(x)$.  This way we can no longer assert that real numbers (elements of $\mathbb{R}$) *are* Dedekind cuts, or equivalence classes of Cauchy sequences, or anything in particular, since the axioms provide no rules about how $\varepsilon x.P(x)$ must be chosen other than that it must satisfy $P$.  So $\mathbb{R}$ *might* consist of Cauchy sequences, or Dedekind cuts, or any other way to construct the reals, but we have no way of knowing, and thus we cannot make use of any such definition in a proof about $\mathbb{R}$; we are forced to use only its formal properties.

In many cases, the assumption of a global choice operator implies the [[axiom of choice]], since for any family $(A_u)$ of inhabited sets, a choice function is given by $u\mapsto (\varepsilon x.x\in A_u)$.  In fact, in the form given above it often implies the stronger *global* axiom of choice, which applies to proper classes as well as sets.

> "Here, moreover, we come upon a very remarkable circumstance, namely, that all of these transfinite axioms are derivable from a single axiom, one that also contains the core of one of the most attacked axioms in the literature of mathematics, namely, the axiom of choice: $A(a) \rightarrow A(\varepsilon(A))$, where $\varepsilon$ is the transfinite logical choice function."

> ---Hilbert (1925), "On the Infinite", excerpted in Jean van Heijenoort, _From Frege to G&#246;del_, p. 382.

However, in some [[foundations]] it seems to be possible to avoid this conclusion (if it is unwanted) by not requiring the choice operator to be extensional, i.e. it may not be the case that $A = B$ implies $\varepsilon x.A = \varepsilon x.B$.

+--{: .query}
[[Mike Shulman]]: Is there a formal statement in some formal system along the lines of "a non-extensional choice operator does not imply AC"?

_Toby_:  I don\'t know about a formal statement, but I can give you an example.

Recall:  In Per Martin-L&#246;f\'s Intuitionistic Type Theory (and many other systems along similar lines), the basic notion axiomatised is not really that of a set (even though it might be called 'set') but instead a [[preset]] (or 'type').  Often one hears that the axiom of choice *does* hold in these systems, which doesn\'t imply classical logic due to a lack of quotient (pre)sets.  However, if we define a set to be a preset equipped with an equivalence predicate, then the axiom of choice fails (although we have [[COSHEP]] if presets come with an identity predicate).

A lot of these systems (including Martin-L&#246;f\'s) use 'propositions as types', in which $\exists_{x:A} P(x)$ is represented as $\sum_{x:A} P(x)$, which comes equipped with an operation $\pi: \sum_{x:A} P(x) \to A$.  That is not going to get us our choice operator, but since a choice operator is constructively questionable anyway, then let\'s throw in excluded middle.  This is known to not imply choice, but we do have, for every preset $A$, an element $\varepsilon_A$ of $A \vee \neg{A}$, that is of $A \uplus \empty^A$.  It\'s not literally true that $\varepsilon_A$ is of type $A$, of course, but that would be unreasonable in a structural theory; what we do have is a fixed $\varepsilon_A$ such that, if $A$ is inhabited, then $\varepsilon_A = \iota_A(e)$ for some (necessarily unique) $e$ of type $A$ (where $\iota_A$ is the natural inclusion $A \to A \uplus \empty^A$), which I think should be considered good enough.  This is for presets (types), but every set has a type of elements, so that gets us our operator.

How is this nonextensional?  We do have $\varepsilon_A = \varepsilon_B$ if $A = B$ (which is a meaningful statement to Martin-L&#246;f, albeit not a proposition exactly), but if $A$ and $B$ are given as subsets of some $U$, then we may well have $A = B$ as subsets of $U$ without $A = B$ in the sense of identity of their underlying (pre)sets.  In particular, if $f: U \to V$ is a surjection and $A$ and $B$ are the preimages of elements $x$ and $y$ of $V$, then $x =_V y$ will not imply that $\varepsilon_A = \varepsilon_B$, and the proof of the axiom of choice does not go through.  It *will* go through if $x$ and $y$ are identical, that is if $x = y$ in the underlying preset of $V$, so again we do get choice for presets (again), but not for sets.

I\'m not *certain* that a nonextensional global choice operator won\'t imply excluded middle in some other way, but I don\'t see how it would.  You\'d want to do something with the idea that $\varepsilon_A$ always exists but belongs to $A$ if and only if $A$ is inhabited, but I don\'t see how to parse it (just by assuming that it exists) to decide the question.

[[Mike Shulman]]: That's a very nice explanation/example, and it did help me to understand better what's going on; thanks!  (Did you mean to say "excluded middle" and not "AC" in your final paragraph?)  What I would really like, though, is a statement like "the addition of a nonextensional global choice operator to ____ set theory is conservative" (i.e. doesn't enable the proving of any new theorems that doen't refer explicitly to the choice operator).  Of course I am coming from [this comment](http://golem.ph.utexas.edu/category/2009/09/towards_a_computeraided_system.html#c026817), wondering whether what you suggested really is a way to get a choice operator without implying the axiom of choice.

_Toby_:  Yeah, I really did mean to say 'excluded middle'; remembering that comment, I assume that the real question is whether the thing is OK for a constructivist.  I just argued $\mathbf{ITT} + EM \vDash CO$, and I know the result $\mathbf{ITT} + EM \not\vDash AC$, so I conclude $\mathbf{ITT} + CO \not\vDash AC$; but I don\'t know $\mathbf{ITT} + CO \not\vDash EM$ for certain.  I certainly don\'t have $\mathbf{ITT} + CO$ conservative over $\mathbf{ITT}$, nor with any other theory (other than those that already model $CO$, obviously).

[[Mike Shulman]]: Where should I look for a proof that $\mathbf{ITT} + EM$ doesn't imply AC?

_Toby_:  I\'m not sure, it\'s part of my folk knowledge now.  Probably Michael J. Beeson\'s _Foundations of Constructive Mathematics_ is the best bet.  I\'ll try to get a look in there myself next week; I can see that it\'s not exactly obvious, and perhaps my memory is wrong now that I think about it.

[[Mike Shulman]]: I'm trying to prove the sort of statement I want over at [[SEAR+?]].

_Toby_:  No, I can\'t get anything at all out of Beeson (or other references) about full AC (for types equipped with equivalence relations) in $\mathbf{ITT}$.
=--

Like the [[axiom of choice]], the existence of a global choice operator is consistent with the other axioms of most foundations.  For example, in ZF, the [[constructible universe]] (which models $ZF + (V=L)$, the [[axiom of constructibility]]) admits a natural classical [[well-ordering]] of the entire universe, giving rise to a naturally defined global choice operator (namely, $\varepsilon x.P$ = the smallest $x$ such that $P$ in the global well-ordering).

# Readings #

* [Hilbert's $\varepsilon$-Operator](http://planetmath.org/encyclopedia/HilbertsVarepsilonOperator.html), _PlanetMath_.

* See also Hilbert (1927), "The Foundations of Mathematics", pp. 464&#8211;479 in JvH.

category: foundational axiom
