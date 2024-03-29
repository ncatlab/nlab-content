+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In the [[foundations]] of [[mathematics]], it\'s interesting to consider the axiom that the [[Set|Category of Sets]] Has [[projective object|Enough Projectives]]; in short: **CoSHEP** (pronounced /ko:-shep/).  This is more commonly known as the **presentation axiom**: PAx.   It is a weak form of the [[axiom of choice]].

## Statement
 {#Statement}

In elementary terms, CoSHEP states 

+-- {: .num_defn}
###### Axiom (CoSHEP)

For every [[set]] $A$, there exists a set $P$ and a [[surjection]] $P \to A$, such that every surjection $X \twoheadrightarrow P$ has a [[section]].
=--

\begin{remark}
The full axiom of choice states that every surjection $X \to A$ has a section; hence in the above $P$ may be chosen to be $A$ itself.
\end{remark}

This should be read in view of the definition of _[[projective objects]]_:

\begin{definition}
An [[object]] $P$ in a [[category]] $C$ is (externally) [[projective object|projective]] iff the [[hom-functor]] $C(P, -): C \to Set$
takes [[epimorphism|epis]] to epis. This is the same as saying: given an epi $p: B \to A$ and a map $f: P \to A$, there exists a lift $g: P \to B$ in the sense that $f = p \circ g$. 
\end{definition}

Accordingly, in a [[topos]] the CoSHEP axiom says equivalently

+-- {: .num_defn}
###### Axiom (CoSHEP)

Every object has a [[projective presentation]]. Hence: There are [enough projectives](projective+object#EnoughProjectives).
=--

Borrowing from the philosophy of [[constructive mathematics|constructivism]], we may also call this a _complete presentation_.

\begin{remark}
The [[duality|dual]] axiom,  that $Set$ has [enough injectives](injective+object#EnoughInjectives) (that is, every set admits an injection into an injective set) is [[true]] in every [[topos]]: every [[power object]] is an [[injective object]], and every object $X$ embeds in its power object $P X$ via the [[singleton subset|singleton]] map $\{\cdot\}:X\hookrightarrow P X$.
\end{remark}

## Consequences

The existence of sufficiently many [[projective presentations]] plays a central role in [[homological algebra]] as a means to construct [[projective resolutions]] of objects. Tradtionally one often uses the [[axiom of choice]] to prove that [[categories of modules]] have [enough projectives](projective+object#EnoughProjectives), on the grounds that the [[free modules]] are projective. 

But the weaker assumption of CoSHEP is already sufficient for this purpose: while not every free module will be projective, one can still use CoSHEP to find a [[projective presentation]] for every free module (and thus for every module). This is discussed in more detail [here](projective+object#EnoughWithCOSHEP).

+-- {: .num_prop #ImpliesDependentAndCountableChoice}
###### Proposition

The following three conditions on a [[W-pretopos]] with [enough projectives](projective+object#EnoughProjectives) are equivalent: 

1. The axiom of [[dependent choice]] (DC), 

2. The axiom of [[countable choice]] (CC), 

3. Projectivity of the [[singleton]] (the [[terminal object]]) $1$. 
=-- 

Note that we normally assume (3) for [[the category of sets]], which is true in any (constructively) [[well-pointed pretopos]] and true *[[internalization|internally]]* in any pretopos whatsoever, so one normally says that DC and CC simply follow from the existence of enough projectives (CoSHEP).  Equivalently, internal DC and internal CC follow from internal CoSHEP.

+-- {: .proof}
###### Proof 
Condition 1 easily implies 2. Condition 2 says precisely that the [[natural numbers object]] $\mathbb{N}$ is externally projective, and since $1$ is a retract of $\mathbb{N}$, it is projective under condition 2, so 2 implies 3. It remains to show 3 implies 1. 

Let $X$ be inhabited, so there exists an [[entire relation]] given by a jointly monic span 

$$1 \stackrel{epi}{\leftarrow} U \stackrel{f}{\to} X,$$ 

and similarly let 

$$X \stackrel{epi \pi_1}{\leftarrow} R \stackrel{\pi_2}{\to} X$$ 

be an [[entire relation|entire binary relation]]. Let $p: P \to X$ be a projective cover. Since $1$ is assumed projective, the cover $U \to 1$ admits a section $\sigma: 1 \to U$, and the element $f \sigma: 1 \to X$ lifts through $p$ to an element $x_0: 1 \to P$. Next, in the diagram below, $p$ lifts through the epi $\pi_1$ to a map $q: P \to R$, and then $\pi_2 q$ lifts through $p$ to a map $\phi$ (since $P$ is projective): 

$$\array{
 & & P  & \stackrel{\phi}{\to} & P \\
 & \swarrow p & \downarrow q & & \downarrow p \\
X & \underset{\pi_1}{\leftarrow} & R & \underset{\pi_2}{\to} & X
}$$

By the universal property of $\mathbb{N}$ (see [[recursion]]), there exists a unique map $h: \mathbb{N} \to P$ rendering commutative the diagram 

$$\array{
1 & \stackrel{0}{\to} & \mathbb{N} & \stackrel{s}{\to} & \mathbb{N} \\
id \downarrow & & \downarrow h & & \downarrow h \\
1 & \underset{x_0}{\to} & P & \underset{\phi}{\to} & P \\
 & \swarrow p & \downarrow q & & \downarrow p \\
X & \underset{\pi_1}{\leftarrow} & R & \underset{\pi_2}{\to} & X
}$$

Clearly $\langle p h, p h s \rangle : \mathbb{N} \to X \times X$ factors through $\langle \pi_1, \pi_2 \rangle : R \to X \times X$, i.e., $\forall_{n: \mathbb{N}} (p h(n), p h(n+1)) \in R$, thus proving that dependent choice holds under CoSHEP. 
=-- 


+-- {: .num_example}
###### Example

A topos in which CoSHEP holds but $1$ is not projective is $Set^C$, where $C$ is the category with three objects and exactly two non-identity arrows $a \to b \leftarrow c$. For if $U: C \to Set$ is a functor with $U(a) = \{a_0\}$, $U(b) = \{b_0, b_1\}$, and $U(c) = \{c_0\}$, with $U(a \to b)(a_0) = b_0$ and $U(c \to b)(c_0) = b_1$, then the map $U \to 1$ is epi but has no section, so $1$ is not projective. On the other hand, as noted below, every presheaf topos satisfies CoSHEP, assuming that $Set$ itself does.
=--

CoSHEP also implies several weaker forms of choice, such as the [[axiom of multiple choice]] and [[WISC]].  In weakly [[predicative mathematics]], it can be combined with the existence of [[function sets]] to show the [[subset collection]] axiom.

## Variants of the presentation axiom
{#Variants}

### Split surjections

In the absence of the full [[axiom of choice]], there are actually two notions of surjections: [[surjections]], and [[split surjections]]. Hence, we get four possible different statements of the presentation axiom, depending on whether one uses surjections or split surjections:

1. For every [[set]] $A$, there exists a set $P$ and a [[surjection]] $P \to A$, such that every surjection $X \twoheadrightarrow P$ has a [[section]].

2. For every [[set]] $A$, there exists a set $P$ and a [[split surjection]] $P \to A$, such that every surjection $X \twoheadrightarrow P$ has a [[section]].

3. For every [[set]] $A$, there exists a set $P$ and a [[surjection]] $P \to A$, such that every split surjection $X \twoheadrightarrow P$ has a [[section]]. 

4. For every [[set]] $A$, there exists a set $P$ and a [[split surjection]] $P \to A$, such that every split surjection $X \twoheadrightarrow P$ has a [[section]].

By definition of split surjection, every split surjection has a section, so the third and fourth versions of the presentation axioms are simply:

* For every [[set]] $A$, there exists a set $P$ and a [[surjection]] $P \to A$. 

* For every [[set]] $A$, there exists a set $P$ and a [[split surjection]] $P \to A$.

These two versions of the presentation axiom are always true: take the set $P$ to be $A$ and the (split) surjection $P \to A$ to be the [[identity function]] on $A$. 

This leaves the first and second version of the presentation axiom as non-trivial axioms that one can add to the [[foundations]]. In general, the version using a split surjection into $A$ is stronger than the version using a surjection into $A$, because not every surjection is a split surjection unless the full [[axiom of choice]] holds. And then the usual [[axiom of choice]] is simply the presentation axiom where the surjection is required to be a [[bijection]]. 

### External and internal versions

In addition, every [[set theory]] has an [[internal logic]] defined on its [[subsingletons]]:

* Any [[subsingleton]] represents a proposition

* The [[empty set]] represents [[falsehood]]

* Any [[singleton]] represents [[truth]]

* The binary cartesian product of two subsingletons is [[conjunction]] of propositions

* The function set between two subsingletons is [[implication]] of propositions

* The function set from a subsingleton to the empty set is [[negation]] of propositions

* Given a family of subsingletons, the indexed [[cartesian product]] of the family of subsingletons is [[universal quantification]]

* One can turn any set into a subsingleton by taking the [[image]] of the unique function into a [[singleton]]. This is useful for constructing the internal disjunction and existential quantifier:

* The image of the unique function from the [[disjoint union]] of two subsingletons to any singleton is the [[disjunction]] of propositions

* The image of the unique function from the indexed [[disjoint union]] of a family of subsingletons to any singleton is the [[existential quantifier]]

* Equality is given by the [[diagonal subset]]

Then there also exist internal versions of the presentation axiom, which states that the presentation axiom is true when expressed internally in the set theory, that a particular subsingleton defined using the set theoretic operations above is a singleton. 

### BHK interpretation of the presentation axiom

In addition, there are two different ways to interpret predicate logic in the internal logic of a set theory:

* There is the traditional way of interpreting the internal logic, which takes [[propositions as subsingletons]], and uses the [[disjunction]] for "or" and the [[existential quantifier]] for "there exists, suitably defined in the internal logic.

* There is the [[BHK interpretation]] of the internal logic, which takes [[propositions as sets]] and directly uses binary [[disjoint unions]] for "or" instead of the disjunction, as well as indexed disjoint unions for "there exist" instead of the existential quantifier. 

This means that we get even more versions of the presentation axiom in set theory, depending on where one uses the traditional interpretation of predicate logic and where one uses the BHK interpretation of predicate logic in the internal logic: 

* For surjections, whether the fibers of the function $f:P \to A$ are internally inhabited or pointed

* For split surjections, whether given a function $f:P \to A$ there exists a section $g:A \to P$, or whether one has a section-retraction pair $(f, g):(P \to A) \times (A \to P)$

All of these combine together to form a huge number of possible axioms of the presentation axiom, ranging from the provable to stronger than the usual presentation axiom. 

### In dependent type theory

In dependent type theory, not all types are sets, and sets (and other types) are usually elements of types called universes, so there are even more versions of the presentation axiom, depending on 

* Whether given a set $A:U$ there exists a set $P:U$ or whether one has a pair of sets $(A, P):U \times U$,

* Whether one uses sets or types in defining the presentation axiom. 

## In a topos
 {#topos}

When working in the [[internal logic]] of a [[topos]], the "internal" meaning of CoSHEP is "every object is covered by an [[internally projective object]]."  (Compare with the internal axiom of choice: every object is internally projective.)  As regards foundational axioms for toposes (in the sort of sense that the axiom of choice is regarded as "foundational"), the internal version of the presentation axiom should be taken as the default version. 

+-- {: .num_prop}
###### Proposition
 
Suppose that $1$ is (externally) projective in $E$. Then $E$ satisfies PAx whenever it satisfies internal PAx. 
=-- 

Internal PAx does not follows from external PAx; see Counterexample 5.3. However, if _every_ object is projective (AC), then every object is internally projective (IAC). 

A stronger version of PAx may be worth considering. Say that an object is **stably projective** if its [[pullback]] to any [[slice category]] is projective. Then stably projective objects are internally projective (proof?). Similarly, if we say that a topos $E$ satisfies stable PAx if every object is covered by a stably projective object, then a topos satisfies internal PAx if it satisfies stable PAx. 


+-- {: .num_example}
###### Example

Every [[presheaf topos]] $Set^{C^{op}}$ has enough projectives, since any coproduct of representables is projective. If in addition $C$ has binary products, then by [this result](/nlab/show/internally+projective+object#presheaf), $Set^{C^{op}}$ validates internal PAx.  
=--

+-- {: .num_example #counter} 
###### Counterexample

However, not every presheaf topos validates internal PAx, even though every presheaf topos validates external PAx. As an example, let $C$ be the category where $Ob(C)$ is the disjoint sum $\mathbb{N} \cup \{a, b\}$, and preordered by taking the reflexive transitive closure of relations $n \leq n+1$, $n \leq a$, $n \leq b$. The claim is that neither $C(-, a)$, nor any presheaf $P$ that maps epimorphically onto $C(-, a)$, can be internally projective. Indeed, consider the presheaf $F$ defined by $F(a) = F(b) = \emptyset$ and $F(n) = [n,\infty)$, with $F(n+1 \to n)$ the evident inclusion. Let $G$ be the [[subterminal object|support]] of $F$, so that we have an epi $e: F \to G$. 

The objects $C(-, a), C(-, b)$, and $G$ are [[subterminal object|subterminal]] and $G \cong C(-, a) \cap C(-, b) \cong C(-, a) \times C(-, b)$. The set $F^{C(-, a)}(b)$ is empty because there is no $C(-, a) \times C(-, b) \to F$ (it would give a section $G \to F$ of $e: F \to G$, but none exists), whereas $G^{C(-, a)}(b)$ is inhabited by $C(-, a) \times C(-, b) \cong G$. For any $P$ covering $C(-, a)$, the set $F^P(b)$ is empty (because any section $s: C(-, a) \to P$ of $P \to C(-, a)$ induces a function $F^P(b) \to F^{C(-, a)}(b) = 0$), and the set $G^P(b)$ is inhabited (the map $P \to C(-, a)$ induces a map $1 \cong G^{C(-, a)}(b) \to G^P(b)$). Thus the map $e^P \colon F^P \to G^P$ cannot be epic. 
=-- 

+-- {: .num_example}
###### Counterexample 

Any topos that violates countable choice, of which there are plenty, must also violate internal PAx.
=-- 

+-- {: .num_example}
###### Example

An interesting example of a topos that has enough projectives and satisfies internal CoSHEP (at least, assuming the axiom of choice in [[Set]]), although it violates the full (internal) axiom of choice, is the [[effective topos]], and more generally any [[realizability topos]]. The reason for this is quite similar to the intuitive justification for CoSHEP given above. Technically, it results from the fact that realizability toposes are [[exact completions]]; an explanation is given in [this remark](/nlab/show/realizability+topos#pax). 
=--

For a Grothendieck topos example, the sheaves on the interval $[0,1]$ with its usual topology give a topos in which the internal axiom of countable choice fails, hence internal PAx must also fail.

## In categories which are not topoi

+-- {: .num_example}
###### Example

According to Peter Scholze in [this comment on the nCafé](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057798), an example of a category that satisfies external CoSHEP is the category of [[condensed sets]], assuming that [[Set]] satisfies the axiom of choice. The category of condensed sets do not form a topos, only an [[infinitary pretopos]]. 

However, internal CoSHEP fails in condensed sets. 
=--

## Further properties

Since [[Set]] is (essentially regardless of foundations) an [[exact category]], if it has [enough projectives](projective+object#EnoughProjectives) then it must be the _free_ [[exact category]] $PSet_{ex/lex}$ generated by its [[subcategory]] $PSet$ of [[projective objects]].  By the construction of the [ex/lex completion](regular+and+exact+completions#TheExLexCompletion) $PSet_{ex/lex}$, it follows that every set is the quotient of some "pseudo-equivalence relation" in $PSet$; i.e., the result of imposing an equality relation on some completely presented set.  See [[SEAR plus epsilon|SEAR+ε]] for an application of this idea.


+-- {: .num_prop}
###### Proposition

CoSHEP as a choice principle added to [[ZF]] implies a [[proper class]] of [[regular cardinals]].
=--

+-- {: .proof}
###### Proof 

Since CoSHEP implies [[WISC]], and WISC has this implication (a result of [[Benno van den Berg|van den Berg]]).
=--

## In higher category theory

In [[higher category theory]], there are different versions of CoSHEP: 

* For every [[0-groupoid]] $A$, there exists 0-groupoid $P$ and [[effective epimorphism]] $P \to A$, such that for all 0-groupoids $X$ there exists effective epimorphism $X \to P$ with [[section]]. 

* For every [[infinity-groupoid]] $A$, there exists 0-groupoid $P$ and [[effective epimorphism]] $P \to A$, such that for all 0-groupoids $X$ there exists effective epimorphism $X \to P$ with [[section]]. 

The difference between these versions of CoSHEP is that [[sets cover]]. 

## Justification

Although perhaps not well known in the literature of [[constructive mathematics]], the CoSHEP axiom may be justified by the sort of reasoning usually accepted to justify the [[axiom of countable choice|axioms of countable choice]] and [[axiom of dependent choice|dependent choice]], which it implies, by Proposition \ref{ImpliesDependentAndCountableChoice} above. 

To be explicit, every set $A$ should have a 'completely presented' set of 'canonical' [[elements]], that is elements given directly as they are constructed without regard for the [[equality relation]] imposed upon them. For canonical elements, [[equality]] is identity, so the [[BHK interpretation]] of logic justifies the axiom of choice for a completely presented set. This set is $P$, and $A$ is obtained from it as a [[quotient set|quotient]] by the relation of equality on $A$. This argument can be made precise in some forms of [[type theory]], which thus justify CoSHEP, much as they are widely known to justify dependent choice.

## Related concepts

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

  * [[projective module]]

  * [[internally projective object]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]


## References

When [[Peter Aczel]] was developing $CZF$ (a constructive predicative version of [[ZFC]]), he considered this axiom, under the name of the _presentation axiom_, but ultimately rejected it.

* [[Peter Aczel]], _The type theoretic interpretation of constructive set theory_. Logic Colloquium '77 (Proc. Conf., Wroclaw, 1977), pp. 55--66, Stud. Logic Foundations Math., 96, North-Holland, Amsterdam-New York, 1978. doi:[10.1016/S0049-237X(08)71989-X](https://doi.org/10.1016/S0049-237X%2808%2971989-X)

The presentation axiom was, however, adopted by [[Erik Palmgren]] in $CETCS$ (a constructive predicative version of [[ETCS]]):

*  [[Erik Palmgren]],  _Constructivist and Structuralist Foundations: Bishop's and Lawvere's Theories of Sets_, Annals of Pure and Applied Logic
 **163** Issue 10 (2012) 1384–1399, doi:[10.1016/j.apal.2012.01.011](https://doi.org/10.1016/j.apal.2012.01.011) arXiv:[1201.6272](https://arxiv.org/abs/1201.6272),  [author pdf](http://www.math.uu.se/~palmgren/cetcs.pdf).

Its relationship to some other weak axioms of choice is studied in

* [[Michael Rathjen]], _Choice principles in constructive and classical set theories_, In: Z. Chatzidakis, P. Koepke, & W. Pohlers (Eds.), Logic Colloquium '02 (Lecture Notes in Logic, pp. 299-326) (2006). Cambridge: Cambridge University Press. doi:[10.1017/9781316755723.014](https://doi.org/10.1017/9781316755723.014). [author pdf](http://www1.maths.leeds.ac.uk/~rathjen/acend.pdf).


category: foundational axiom

[[!redirects presentation axiom]]
[[!redirects PAX]]
[[!redirects PAx]]
[[!redirects pax]]
[[!redirects COSHEP]]
[[!redirects CoSHEP]]
[[!redirects coshep]]
[[!redirects completely presented set]]
[[!redirects completely presented sets]]