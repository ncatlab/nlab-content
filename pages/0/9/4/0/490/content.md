
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

In the [[foundations]] of [[mathematics]], it\'s interesting to consider the axiom that the [[Set|Category Of Sets]] Has [[projective object|Enough Projectives]]; in short: **COSHEP** (pronounced /ko:-shep/).  This is more commonly known as the **presentation axiom**: PAx.   It is a weak form of the [[axiom of choice]].

## Statement
 {#Statement}

In elementary terms, COSHEP states 

**Axiom (COSHEP).** _For every [[set]] $A$, there exists a set $P$ and a [[surjection]] $P \to A$, such that every surjection $X \twoheadrightarrow P$ has a [[section]]._ 

+-- {: .num_remark}
###### Remark

The full axiom of choice states that every surjection $X \to A$ has a section; hence that in the above $P$ may be chosen to be $A$ itself.

=--

This should be read in view of the definition of _[[projective objects]]_:

+-- {: .num_defn}
###### Definition

An [[object]] $P$ in a [[category]] $C$ is (externally) [[projective object|projective]] iff the [[hom-functor]] $C(P, -): C \to Set$
takes [[epimorphism|epis]] to epis. This is the same as saying: given an epi $p: B \to A$ and a map $f: P \to A$, there exists a lift $g: P \to B$ in the sense that $f = p \circ g$. 

=--

Accordingly, in a [[topos]] the COSHEP axiom says equivalently

**Axiom (COSHEP)** _Every object has a [[projective presentation]]._ Hence: _There are [enough projectives](projective+object#EnoughProjectives)._

Borrowing from the philosophy of [[constructive mathematics|constructivism]], we may also call this a _complete presentation_.


+-- {: .num_remark}
###### Remark

The [[duality|dual]] axiom,  that $Set$ has [enough injectives](injective+object#EnoughInjectives) (that is, every set admits an [injection into an injective set) is [[true]] in every [[topos]],  every topos has enough injectives: every [[power object]] is an [[injective object]] and every object $X$ embeds in its power object $P X$ via the "singleton" map $\{\cdot\}:X\hookrightarrow P X$.

=--

## Justification

Although perhaps not well known in the literature of [[constructive mathematics]], the COSHEP axiom may be justified by the sort of reasoning usually accepted (except in the school of Fred Richman) to justify the [[axiom of countable choice|axioms of countable choice]] and [[axiom of dependent choice|dependent choice]] (which it implies, by prop. \ref{ImpliesDependentAndCountableChoice} below). 

To be explicit, every set $A$ should have a 'completely presented' set of 'canonical' [[elements]], that is elements given directly as they are constructed without regard for the [[equality relation]] imposed upon them. For canonical elements, [[equality]] is identity, so the [[BHK interpretation]] of logic justifies the axiom of choice for a completely presented set. This set is $P$, and $A$ is obtained from it as a [[quotient set|quotient]] by the relation of equality on $A$. This argument can be made precise in many forms of [[type theory]] (including those of Martin-L&#246;f and Thierry Coquand), which thus justify COSHEP, much as they are widely known to justify dependent choice.


## Consequences

+-- {: .num_remark}
###### Remark

The existence of sufficiently many [[projective presentations]] plays a central role in [[homological algebra]] as a means to construct [[projective resolutions]] of objects.
Tradtionally one often uses the [[axiom of choice]] to prove that [[categories of modules]] have [enough projectives](projective+object#EnoughProjectives), on the grounds that the [[free modules]] are projective. 

But the weaker assumption of COSHEP is already sufficient for this purpose: while not every free module will be projective, one can still use COSHEP to find a [[projective presentation]] for every free module (and thus for every module). This is discussed in more detail [here](projective+object#EnoughWithCOSHEP).

=--

+-- {: .num_prop #ImpliesDependentAndCountableChoice}
###### Proposition

The following three conditions on a [[W-pretopos]] with [enough projectives](projective+object#EnoughProjectives) are equivalent: 

1. The axiom of [[dependent choice]] (DC), 

2. The axiom of [[countable choice]] (CC), 

3. Projectivity of the [[singleton]] (the [[terminal object]]) $1$. 
=-- 

Note that we normally assume (3) for [[the category of sets]], which is always true *[[internalization|internally]]* in any pretopos, so one normally says that DC and CC simply follow from the existence of enough projectives (COSHEP).  Equivalently, internal DC and internal CC follow from internal COSHEP.

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

Clearly $\langle p h, p h s \rangle : \mathbb{N} \to X \times X$ factors through $\langle \pi_1, \pi_2 \rangle : R \to X \times X$, i.e., $\forall_{n: \mathbb{N}} (p h(n), p h(n+1)) \in R$, thus proving that dependent choice holds under COSHEP. 
=-- 


+-- {: .num_example}
###### Example

A topos in which COSHEP holds but $1$ is not projective is $Set^C$, where $C$ is the category with three objects and exactly two non-identity arrows $a \to b \leftarrow c$. For if $U: C \to Set$ is a functor with $U(a) = \{a_0\}$, $U(b) = \{b_0, b_1\}$, and $U(c) = \{c_0\}$, with $U(a \to b)(a_0) = b_0$ and $U(c \to b)(c_0) = b_1$, then the map $U \to 1$ is epi but has no section, so $1$ is not projective. On the other hand, as noted below, every presheaf topos satisfies COSHEP, assuming that $Set$ itself does.

=--

+-- {: .num_remark}
###### Remark

COSHEP also implies several weaker forms of choice, such as the [[axiom of multiple choice]] and [[WISC]].  In [[predicative mathematics]], it can be combined with the existence of [[function sets]] to show the [[subset collection]] axiom.

=--

## In a topos
 {#topos}

When working in the [[internal logic]] of a [[topos]], the "internal" meaning of COSHEP is "every object is covered by an [[internally projective object]]."  (Compare with the internal axiom of choice: every object is internally projective.)  As regards foundational axioms for toposes (in the sort of sense that the axiom of choice is regarded as "foundational"), the internal version of the presentation axiom should be taken as the default version. 

+-- {: .num_remark}
###### Remark 
Suppose that $1$ is (externally) projective in $E$. Then $E$ satisfies PAx whenever it satisfies internal PAx. 
=-- 

+-- {: .num_remark} 
###### Remark 
Internal PAx does not follows from external PAx; see Example \ref{counter}. However, if _every_ object is projective (AC), then every object is internally projective (IAC). 

A stronger version of PAx may be worth considering. Say that an object is **stably projective** if its pullback to any slice category is projective. Then stably projective objects are internally projective (proof?). Similarly, if we say that a topos $E$ satisfies stable PAx if every object is covered by a stably projective object, then a topos satisfies internal PAx if it satisfies stable PAx. 
=--


+-- {: .num_example}
###### Example

Every [[presheaf topos]] $Set^{C^{op}}$ has enough projectives, since any coproduct of representables is projective. If in addition $C$ has binary products, then by [this result](/nlab/show/internally+projective+object#presheaf), $Set^{C^{op}}$ validates internal PAx.  

=--

+-- {: .num_example #counter} 
###### Example 
However, not every presheaf topos validates internal PAx, even though every presheaf topos validates external PAx. As an example, let $C$ be the category where $Ob(C)$ is the disjoint sum $\mathbb{N} \cup \{a, b\}$, and preordered by taking the reflexive transitive closure of relations $n \leq n+1$, $n \leq a$, $n \leq b$. The claim is that neither $C(-, a)$, nor any presheaf $P$ that maps epimorphically onto $C(-, a)$, can be internally projective. Indeed, consider the presheaf $F$ defined by $F(a) = F(b) = \emptyset$ and $F(n) = (-\infty, -n]$, with $F(n+1 \to n)$ the evident inclusion. Let $G$ be the support of $F$, so that we have an epi $e \colon F \to G$. Then it may be shown that for any $P$ covering $C(-, a)$, the set $F^P(b)$ is empty and the set $G^P(b)$ is nonempty, so that the map $e^P \colon F^P \to G^P$ cannot be epic. 
=-- 

+-- {: .num_example}
###### Example 
Any topos that violates countable choice, of which there are plenty, must also violate internal PAx.  (Note that the terminal object of any topos is *internally* projective, so the proof above that PAx implies CC goes through.) 
=-- 

+-- {: .num_example}
###### Example
An interesting example of a topos that has enough projectives and satisfies internal COSHEP (at least, assuming the axiom of choice in [[Set]]), although it violates the full (internal) axiom of choice, is the [[effective topos]], and more generally any [[realizability topos]]. The reason for this is quite similar to the intuitive justification for COSHEP given above. Technically, it results from the fact that realizability toposes are [[exact completions]]; an explanation is given in [this remark](/nlab/show/realizability+topos#pax). 
=--


## Further properties


Since [[Set]] is (essentially regardless of foundations) an [[exact category]], if it has [enough projectives](projective+object#EnoughProjectives) then it must be the _free_ 
[[exact category]] $PSet_{ex/lex}$ generated by its [[subcategory]] $PSet$ of [[projective objects]].  By the construction of the [ex/lex completion](regular+and+exact+completions#TheExLexCompletion) $PSet_{ex/lex}$, it follows that every set is the quotient of some "pseudo-equivalence relation" in $PSet$; i.e., the result of imposing an equality relation on some completely presented set.  See [[SEAR+ε]] for an application of this idea.


+-- {: .num_prop}
###### Proposition

COSHEP as a choice principle added to [[ZF]] implies a [[proper class]] of [[regular cardinals]].

=--

+-- {: .proof}
###### Proof 

Since COSHEP implies [[WISC]], and WISC has this implication.

=--

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

When [[Peter Aczel]] was developing $\mathbf{CZF}$ (a constructive predicative version of [[ZFC]]), he considered this axiom, under the name of the _presentation axiom_, but ultimately rejected it.

* Peter Aczel. _The type theoretic interpretation of constructive set theory_. Logic Colloquium '77 (Proc. Conf., Wroclaw, 1977), pp. 55--66, Stud. Logic Foundations Math., 96, North-Holland, Amsterdam-New York, 1978.  Cited in Palmgren, below.

The presentation axiom was, however, adopted by [[Erik Palmgren]] in $\mathbf{CETCS}$ (a constructive predicative version of [[ETCS]]):

*  Erik Palmgren.  _Constructivist and Structuralist Foundations: Bishop's and Lawvere's Theories of Sets_.  [pdf](http://www.math.uu.se/~palmgren/cetcs.pdf).

Its relationship to some other weak axioms of choice is studied in

* Michael Rathjen.  _Choice principles in constructive and classical set theories_.


category: foundational axiom

[[!redirects presentation axiom]]
[[!redirects PAx]]
[[!redirects COSHEP]]
[[!redirects coshep]]
