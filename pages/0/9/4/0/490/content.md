
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In the [[foundations]] of [[mathematics]], it\'s interesting to consider the axiom that the [[Set|Category Of Sets]] Has [[projective object|Enough Projectives]]; in short: **COSHEP** (pronounced /ko:-shep/).  This is also known as the **presentation axiom** "PAx."   It is a weak form of the [[axiom of choice]].

In elementary terms, COSHEP states that for every set $A$, there exists a set $P$ and a [[surjection]] $P \to A$, such that every surjection $X \twoheadrightarrow P$ has a [[section]]. (Note that the full axiom of choice states that every surjection $X \to A$ has a section; that is, you may take $P$ to be $A$ itself.) In analogy with [[algebra]] (see below), we may call $P$ (or more precisely, the surjection $P \to A$) a _projective resolution_ of $A$. Or borrowing from the philosophy of [[constructive mathematics|constructivism]], we may call $P$ (or again, $P \to A$) a _complete presentation_ of $A$.

As in [[homological algebra]], an [[object]] $P$ in a [[category]] $C$ is (externally) projective iff the [[hom-functor]] 

$$C(P, -): C \to Set$$ 

takes [[epimorphism|epis]] to epis. This is the same as saying: given an epi $p: B \to A$ and a map $f: P \to A$, there exists a lift $g: P \to B$ in the sense that $f = p \circ g$. 


## Consequences

As an axiom, this has important consequences for algebra; there, one often uses the axiom of choice to prove that categories of [[module]]s have enough projectives, on the grounds that the [[free functor|free]] modules are projective. But COSHEP is sufficient; while not every free module will be projective, one can still use COSHEP to find a [[projective resolution]] for every free module (and thus for every module).

+-- {: .un_prop}
######Proposition
In the presence of COSHEP (and the base assumption that $Set$ forms a [[W-pretopos]]), the following three axioms on [[Set]] are equivalent: 

1. The axiom of [[dependent choice]] (DC), 

2. The axiom of [[countable choice]] (CC), 

3. Projectivity of the [[singleton]] (the [[terminal object]]) $1$. 
=-- 

Note that we normally assume (3), which is always true *[[internalization|internally]]* in any pretopos, so one normally says that DC and CC simply follow from COSHEP.  (Equivalently, internal DC and internal CC follow from internal COSHEP.)

+-- {: .proof}
######Proof 
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

(An example of a topos in which COSHEP holds but $1$ is not projective is $Set^C$, where $C$ is the category with three objects and exactly two non-identity arrows $a \to b \leftarrow c$. For if $U: C \to Set$ is a functor with $U(a) = \{a_0\}$, $U(b) = \{b_0, b_1\}$, and $U(c) = \{c_0\}$, with $U(a \to b)(a_0) = b_0$ and $U(c \to b)(c_0) = b_1$, then the map $U \to 1$ is epi but has no section, so $1$ is not projective. On the other hand, as noted below, every presheaf topos satisfies COSHEP.) 

COSHEP also implies several weaker forms of choice, such as the [[axiom of multiple choice]] and [[WISC]].  In [[predicative mathematics]], it can be combined with the existence of [[function sets]] to show the [[subset collection]] axiom.


## Justification

Although perhaps not well known in the literature of [[constructive mathematics]], this axiom may be justified by the sort of reasoning usually accepted (except in the school of Fred Richman) to justify the axioms of countable choice and dependent choice (which it implies, as above). To be explicit, every set $A$ should have a 'completely presented' set of 'canonical' elements, that is elements given directly as they are constructed without regard for the [[equality relation]] imposed upon them. For canonical elements, equality is identity, so the BHK interpretation of logic justifies the axiom of choice for a completely presented set. This set is $P$, and $A$ is obtained from it as a [[quotient set|quotient]] by the relation of equality on $A$. This argument can be made precise in many forms of [[type theory]] (including those of Martin-L&#246;f and Thierry Coquand), which thus justify COSHEP, much as they are widely known to justify dependent choice.


## In topos theory
{#topos}

When working in the [[internal logic]] of a [[topos]], the "internal" meaning of COSHEP is "every object is covered by an [[internally projective object]]."  (Compare with the internal axiom of choice: every object is internally projective.)  Since every projective object is internally projective, if the topos itself has enough projectives, then it must satisfy internal COSHEP.

For example, any [[presheaf]] topos has enough projectives, since any coproduct of representables is projective, and therefore it validates internal COSHEP.  In contrast, any topos that violates countable choice, of which there are plenty, must also violate internal COSHEP.  (Note that the terminal object of any topos is *internally* projective, so the proof above that COSHEP implies CC goes through.)

An interesting example of a topos that has enough projectives and thus does satisfy internal COSHEP (at least, assuming the axiom of choice in [[Set]]), although it violates the full (internal) axiom of choice, is the [[effective topos]].  The reason for this is quite similar to the intuitive justification for COSHEP given above.


## Remarks 

* The dual axiom that $Set$ has enough [[injective object|injectives]] (that is, every set admits an injection into an injective set) is always true.  In fact, any topos has enough injectives: every power object is injective and every object $X$ embeds in its power object $P X$ via the "singleton" map $\{\cdot\}:X\hookrightarrow P X$.

* Since $Set$ is (essentially regardless of foundations) an [[exact category]], if it has enough projectives then it must be the _free_ exact category $PSet_{ex/lex}$ generated by its subcategory $PSet$ of projective objects.  By the construction of $PSet_{ex/lex}$, it follows that every set is the quotient of some "pseudo-equivalence relation" in $PSet$; i.e., the result of imposing an equality relation on some completely presented set.  See [[SEAR+ε]] for an application of this idea.


## References

When [[Peter Aczel]] was developing $\mathbf{CZF}$ (a constructive predicative version of [[ZFC]]), he considered this axiom, under the name of the _presentation axiom_, but ultimately rejected in favour of its weaker consequence, [[dependent choice]].

* Peter Aczel. _The type theoretic interpretation of constructive set theory_. Logic Colloquium '77 (Proc. Conf., Wroclaw, 1977), pp. 55--66, Stud. Logic Foundations Math., 96, North-Holland, Amsterdam-New York, 1978.  Cited in Palmgren, below.

The presentation axiom was, however, adopted by [[Erik Palmgren]] in $\mathbf{CETCS}$ (a constructive predicative version of [[ETCS]]):

*  Erik Palmgren.  _Constructivist and Structuralist Foundations: Bishop's and Lawvere's Theories of Sets_.  [pdf](http://www.math.uu.se/~palmgren/cetcs.pdf).

Its relationship to some other weak axioms of choice is studied in

* Michael Rathjen.  _Choice principles in constructive and classical set theories_.


[[!redirects presentation axiom]]
[[!redirects PAx]]

category: foundational axiom
