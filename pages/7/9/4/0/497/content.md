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

In [[logic]], the principle of **excluded middle** states that every [[truth value]] is either [[true]] or [[false]] ([Aristotle, MP1011b24](#AristotleMetaphysics)). (This is sometimes called the '[[axiom]]' or 'law' of excluded middle, either to emphasise that it is or is not optional; 'principle' is a relatively neutral term.) One of the many meanings of [[classical logic]] is to emphasise that this principle holds in the logic; in contrast, it fails in [[intuitionistic logic]].

The principle of excluded middle (hereafter, PEM), as a statement about truth values themselves, is accepted by nearly all mathematicians ([[classical mathematics]]); those who doubt or deny it are a distinct minority, the [[constructive mathematics|constructivists]]. However, when one [[internalization|internalises]] mathematics in [[categories]] other than [[Set|the category of sets]], there is no doubt that excluded middle often fails [[internal logic|internally]]. See the examples listed at [[internal logic]]. (Those categories in which excluded middle holds are called [[Boolean category|Boolean]]; in general, the adjective 'Boolean' is often used to indicate the applicability of PEM.)

Although the term 'excluded middle' (sometimes even _excluded third_) suggests that the principle does not apply in many-valued logics, that is not the point; many-valued logics are many-valued *externally* but may still be two-valued *internally*.  In the language of [[categorial logic]], whether a category has exactly two [[subterminal objects]] is in general independent of whether it is Boolean; instead, the category is Boolean iff the statement that it has exactly two subterminal objects holds in its [[internal logic]] (which is in general independent of whether that statement is true).

In fact, intuitionistic logic proves that there is no truth value that is neither true nor false; in this sense, the possibility of a 'middle' or 'third' truth value is still 'excluded'.  But since the relevant [[de Morgan law]] fails in intuitionistic logic, we may not conclude that every truth value is either true or false, which is the actual PEM.

## In set theory

In [[material set theory]], [Shulman 18](#Shulman18) makes the distinction between **full classical logic**, where the principle of excluded middle holds for all logical formulae in the [[material set theory]], and **$\Delta_0$-classical logic**, where the principle of excluded middle holds for only holds for $\Delta_0$-formulae. $\Delta_0$-formulae are logical formulae where every [[quantifier]] $Q$ has to be bounded by the membership relation; i.e. $Q x \in y.P(x) \coloneqq Q x.x \in y \wedge P(x)$. In [[structural set theory]], the above difference between full classical logic and $\Delta_0$-classical logic in [[material set theory]] is the difference between defining [[structural set theory]] as a [[well-pointed topos|well-pointed]] [[Boolean topos]] in [[classical logic]] and in [[intuitionistic logic]] respectively. 

## In type theory

In [[dependent type theory]], there are many statements of excluded middle. 

### Truncated excluded middle

The statement which directly corresponds to excluded middle in logic states that given a type $P$, if $P$ is a [[mere proposition]], then either $P$ or the negation of $P$ holds

$$\frac{\Gamma \vdash P \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_P:\mathrm{isProp}(P) \to (P \vee \neg P)}$$

where $\mathrm{isProp}$ is the [[isProp]] [[modality]] commonly defined as $\prod_{x:P} \prod_{y:P} \mathrm{Id}_P(x, y)$, negation $\neg P$ is simply the the function type $P \to \mathbb{0}$ into the [[empty type]] and [[disjunction]] $A \vee B$ is the [[bracket type]] of the [[sum type]] $[A + B]$. 

If one additionally has a [[Russell type of all propositions]] $\Omega$ or a [[Tarski type of all propositions]] $(\Omega, \mathrm{El}_\Omega)$, the law of truncated excluded middle could be expressed as an axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} P \vee \neg P}\mathrm{Russell} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} \mathrm{El}_\Omega(P) \vee \neg \mathrm{El}_\Omega(P)}\mathrm{Tarski}$$

If the type theory has a [[boolean domain]] $\mathrm{Bit}$ which is a [[univalent Tarski universe]] with [[type family]] $\mathrm{El}_\mathrm{Bit}$ and thus satisfies the extensionality principle, truncated excluded middle could be stated as given a type $P$, if $P$ is a [[mere proposition]], then there exists a boolean $Q$ such that $P$ is equivalent to the type reflection of $Q$:

$$\frac{\Gamma \vdash P \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_P:\mathrm{isProp}(P) \to \exists Q:\mathrm{Bit}.P \simeq \mathrm{El}_\mathrm{Bit}(Q)}$$

By definition, the only two booleans are $0$ representing false and $1$ representing true. 

### Untruncated excluded middle

There is also an untruncated version of excluded middle, which uses the sum type instead of the disjunciton:

$$\frac{\Gamma \vdash P \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_P:\mathrm{isProp}(P) \to (P + \neg P)}$$

In the untruncated case, the requirement that $P$ be an [[h-proposition]] is necessary; the untruncated law of excluded middle for [[h-sets]] is the [[set-theoretic choice operator]], which implies the [[set-theoretic axiom of choice]] in addition to [[excluded middle]], and the untruncated law of excluded middle for general [[types]] is the [[type-theoretic choice operator]], which implies [[UIP]] in addition to the set-theoretic axiom of choice and excluded middle. 

If one additionally has a [[Russell type of all propositions]] $\Omega$ or a [[Tarski type of all propositions]] $(\Omega, \mathrm{El}_\Omega)$, the law of untruncated excluded middle could be expressed as an axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} P + \neg P}\mathrm{Russell} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} \mathrm{El}_\Omega(P) + \neg \mathrm{El}_\Omega(P)}\mathrm{Tarski}$$

Similarly as above, if the type theory has a [[boolean domain]] $\mathrm{Bit}$ which is a [[univalent Tarski universe]] with [[type family]] $\mathrm{El}_\mathrm{Bit}$ and thus satisfies the extensionality principle, there is also an untruncated version of excluded middle using the [[boolean domain]] and [[dependent sum types]]:

$$\frac{\Gamma \vdash P \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_P:\mathrm{isProp}(P) \to \sum_{Q:\mathrm{Bit}} P \simeq \mathrm{El}_\mathrm{Bit}(Q)}$$

By definition, the only two booleans are $0$ representing false and $1$ representing true. 

### Contractible excluded middle

There is also a version of excluded middle, which uses [[contractible type|contractibility]] instead of [[pointed type|pointedness]] to express [[truth]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_A:\mathrm{isProp}(A) \to \mathrm{isContr}(A + \neg A)}$$

In [[dependent type theory]] as [[foundations of mathematics]], the requirement that $A$ be an [[h-proposition]] is also necessary. This alternate law of untruncated excluded middle for general types implies that every type is a [[h-proposition]] a la [[propositional logic as a dependent type theory]], because the only types $P$ such that $P + \neg P$ is equivalent to the unit type are the [[empty type]] and the [[unit type]], which are [[h-propositions]]: 

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_A:\mathrm{isContr}(A + \neg A)}$$

If one additionally has a [[Russell type of all propositions]] $\Omega$ or a [[Tarski type of all propositions]] $(\Omega, \mathrm{El}_\Omega)$, the law of excluded middle could be expressed as an axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} \mathrm{isContr}(P + \neg P)}\mathrm{Russell} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} \mathrm{isContr}(\mathrm{El}_\Omega(P) + \neg \mathrm{El}_\Omega(P))}\mathrm{Tarski}$$

Similarly as above, if the type theory has a [[boolean domain]] $\mathrm{Bit}$ which is a [[univalent Tarski universe]] with [[type family]] $\mathrm{El}_\mathrm{Bit}$ and thus satisfies the extensionality principle, there is also an contractible version of excluded middle using the [[boolean domain]] and [[dependent sum types]]:

$$\frac{\Gamma \vdash P \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_P:\mathrm{isProp}(P) \to \mathrm{isContr}\left(\sum_{Q:\mathrm{Bit}} P \simeq \mathrm{El}_\mathrm{Bit}(Q)\right)}$$

or equivalently, using the [[boolean domain]] and the [[uniqueness quantifier]]:

$$\frac{\Gamma \vdash P \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_P:\mathrm{isProp}(P) \to \exists!Q:\mathrm{Bit}.P \simeq \mathrm{El}_\mathrm{Bit}(Q)}$$

By definition, the only two booleans are $0$ representing false and $1$ representing true. 

### Relations between the notions of excluded middle


\begin{theorem}
The untruncated version of excluded middle implies the truncated version of excluded middle. 
\end{theorem}

\begin{proof}
By the [[introduction rule]] of [[propositional truncations]], there exists a function $\mathrm{isInhab}_{P + \neg P}:(P + \neg P) \to [P + \neg P]$, and the truncated version of excluded middle is simply the [[composition]] of functions 
$$\mathrm{isInhab}_{P + \neg P} \circ \mathrm{lem}_P:\mathrm{isProp}(P) \to (P \vee \neg P)$$
\end{proof}

\begin{theorem}
The contractible version of excluded middle implies the untruncated version of excluded middle
\end{theorem}

\begin{proof}
The type $\mathrm{isContr}(P + \neg P)$ is really the type 

$$\sum_{a:P + \neg P} \prod_{b:P + \neg P} a =_{P + \neg P} b$$

Thus, by the [[introduction rules]] of [[function types]] and the elimination rules of [[negative type|negative]] [[dependent sum types]], there is a function 
$$\lambda x:\mathrm{isProp}(P).\pi_1(\mathrm{lem}_P(x)):\mathrm{isProp}(P) \to (P + \neg P)$$
which is precisely the untruncated version of excluded middle
\end{proof}

## Relation to the axiom of choice
 {#RelationToTheAxiomOfChoice}

Excluded middle can be seen as a very weak form of the [[axiom of choice]] (a slightly more controversial principle, doubted or denied by a slightly larger minority, and true internally in even fewer categories).  In fact, the following are equivalent. (this is the [[Diaconescu-Goodman-Myhill theorem]] due to [Diaconescu 75](#Diaconescu75), see also [McLarty 96, theorem 19.7](#McLarty96), )

1. The principle of excluded middle.
1. [[finite set|Finitely indexed]] sets are [[projective object|projective]] (in fact, it suffices 2-indexed sets to be projective).
1. [[finite set|Finite sets]] are [[choice object|choice]] (in fact, it suffices for 2 to be choice).

(Here, a set $A$ is **finite** or **finitely-indexed** (respectively) if, for some natural number $n$, there is a bijection or surjection (respectively) $\{0, \ldots, n - 1\} \to A$.)

The proof is as follows.  If $p$ is a truth value, then divide $\{0,1\}$ by the equivalence relation where $0 \equiv 1$ iff $p$ holds.  Then we have a surjection $2\to A$, whose domain is $2$ (and in particular, finite), and whose codomain $A$ is 2-indexed (and thus finitely-indexed).  But this surjection splits iff $p$ is true or false, so if either $2$ is choice or $2$-indexed sets are projective, then PEM holds.

On the other hand, if PEM holds, then we can show by induction that if $A$ and $B$ are choice, so is $A\sqcup B$ (add details).  Thus, all finite sets are choice.  Now if $n\to A$ is a surjection, exhibiting $A$ as finitely indexed, it has a section $A\to n$.  Since a finite set is always projective, and any retract of a projective object is projective, this shows that $A$ is projective.

In particular, the axiom of choice implies PEM.  This argument, due originally to Diaconescu, can be internalized in any [[topos]]. However, other weak versions of choice such as [[countable choice]] (any surjection to a countable set (which for this purpose is any set isomorphic to the set of natural numbers) has a section), [[dependent choice]], or even [[COSHEP]] do not imply PEM. 

While is often claimed that axiom of choice is *true* in constructive mathematics (by the BHK or [[Brouwer-Heyting-Kolmogorov interpretation]] of predicate logic), the BHK interpretation of the "axiom of choice" is simply the always true statement that indexed [[cartesian products]] distribute over indexed [[disjoint unions]]

$$\left(\prod_{x \in A} \biguplus_{y \in B(x)} \{\top \vert P(x, y)\}\right) \to \left(\biguplus_{g \in \prod_{x \in A} B(x)} \{\top \vert P(x, g(x))\}\right)$$

or the always true statement that every [[split surjection]] splits. 

## Other equivalent statements

* Every set $A$ with a [[surjection]] from the [[boolean domain]] to $A$ is either a [[singleton]] or in [[bijection]] with the [[boolean domain]]. 

* The set of [[equivalence relations]] on the [[boolean domain]] is in [[bijection]] with the [[boolean domain]]. 

* Morgan Rogers showed [here](https://golem.ph.utexas.edu/category/2023/01/freedom.html#c062002) that the fact that the [[category of sets]] is a [[Boolean topos]] is equivalent to the fact that every [[pointed set]] is a [[free object|free]] pointed set. 

* [[compact spaces equivalently have converging subnets]]

* [[James Hanson]] showed [here](https://categorytheory.zulipchat.com/#narrow/stream/229136-theory.3A-category-theory/topic/One.20universe.20as.20a.20foundation.20.26.20friends/near/465219817) that every [[lower real number]] being a [[Dedekind real number]] is equivalent to LEM. Similarly, every [[upper real number]] being a [[Dedekind real number]] is equivalent to LEM. 

* Every [[subcountable set]] is a [[countable set]]. 

* The [[limited principle of omniscience]] holds for all [[subsingletons]]. 

* Sets with [[decidable tight apartness relations]] form a [[cartesian closed category]]. 

* Assuming [[function sets]], the [[tight apartness relation]] on an [[inequality space]] is [[decidable tight apartness relation|decidable]]. 

* The [[boolean domain]] $2$ is a [[frame]] iff the [[category of sets]] is a [[Boolean topos]]. This implies that one can do [[topology]] (using [[topological spaces]], [[locales]], [[formal topologies]], etc) directly using the boolean domain as the frame of open truth values. 

* The [[poset of truth values]] is an [[inequality space]].

* The [[partial function classifier]] of any [[singleton]] is the [[boolean domain]]. 

* Every [[ideal]] of a [[discrete integral domain|discrete]] [[Bézout domain|Bézout]] [[unique factorization domain]] is a [[principal ideal]]. 

## Double-negated PEM
 {#DoubleNegatedPEM}

While PEM is not valid in constructive mathematics, its double negation 

$$ \neg\neg(A\vee \neg A)$$

is valid.  One way to see this is to note that $\neg (A\vee B) = \neg A \wedge \neg B$ is one of [[de Morgan's laws]] that is constructively valid, and $\neg (\neg A \wedge \neg\neg A)$ is easy to prove (it is an instance of the [[law of non-contradiction]]).

However, a more direct argument makes the structure of the proof more clear.  When [[beta-reduced]], the [[proof term]] is $\lambda x. x(inr(\lambda a. x(inl(a))))$.   This means that we first assume $\neg (A\vee \neg A)$ for a contradiction, for which it suffices (by assumption) to prove $A\vee \neg A$.  We prove that by proving $\neg A$, which we prove by assuming $A$ for a contradiction.  But now we can reach a contradiction by invoking (again) our assumption of $\neg (A\vee \neg A)$ and proving $A\vee \neg A$ this time using our new assumption of $A$.  In other words, we start out claiming that $\neg A$, but whenever that "bluff gets called" by someone supplying an $A$ and asking us to yield a contradiction, we retroactively change our minds and claim that $A$ instead, using the $A$ that we were just given as evidence.

\begin{theorem}
In [[dependent type theory]], the double negation of untruncated excluded middle holds for all types $A$
\end{theorem}

\begin{proof}
The type $\neg \neg A \to \neg \neg A$ has an element, the [[identity function]] $\mathrm{id}_{\neg \neg A}$. Given types $A$, $B$, and $C$, there are equivalences

$$\mathrm{uncurry}_{A, B, C}:(A \to (B \to C)) \simeq ((A \times B) \to C)$$

$$\mathrm{expconv}^{A, B, C}:((A \to C) \times (B \to C)) \simeq ((A + B) \to C)$$

$$\mathrm{comm}_+^{A,B}:(A + B) \simeq (B + A)$$

Thus, there is an element 

$$\lambda z:\neg (A + \neg A).\lambda y:(\neg A + A).z(\mathrm{comm}_+^{\neg A,A}(\lambda x:(\neg \neg A \times \neg A).\mathrm{expconv}^{\neg A, A, \emptyset}(\mathrm{uncurry}_{\neg \neg A, \neg A, \emptyset}(\mathrm{id}_{\neg \neg A})(x))(y)):\neg \neg (A + \neg A)$$
\end{proof}

In particular, this shows how the [[double negation]] [[modality]] can be regarded computationally as a sort of [[continuation-passing]] transform.

However, there is another meaning of "double negated PEM" that is not valid.  The above argument shows that

$$ \forall A, \neg\neg(A\vee \neg A). $$

But a stronger statement is

$$ \neg\neg \forall A, (A \vee \neg A).$$

This is related to the above valid statement by a [[double-negation shift]]; and in fact, the truth of $ \neg\neg \forall A, (A \vee \neg A)$ is equivalent to the principle of double-negation shift.  In particular, it is *not* constructively provable.

## Sharp excluded middle

One could add to [[cohesive homotopy type theory]] a version of excluded middle called the **sharp law of excluded middle**, given by the following rule:

$$\frac{\Xi \vert \Gamma \vdash P \; \mathrm{type} \quad \Xi \vert \Gamma \vdash p:\mathrm{isProp}(P)}{\Xi \vert \Gamma \vdash \mathrm{lem}^\sharp:\sharp(P \vee \neg P)}$$

where $A \vee B \coloneqq \left[A + B\right]$ and $\neg A \coloneqq A \to \mathbb{0}$, and $\sharp A$ is the [[sharp modality]] of $A$, $\left[A\right]$ is the [[propositional truncation]] of $A$ and $\mathbb{0}$ is the [[empty type]]. 

## Related concepts

* [[axiom of choice]]

* [[law of double negation]]

* [[ex falso quodlibet]]

* [[proof by contradiction]]

* [[De Morgan law]]

* [[Cantor-Schroeder-Bernstein theorem]]

## References

### General

* {#McLarty96} [[Colin McLarty]], _Elementary Categories, Elementary Toposes_, Oxford University Press, 1996

* {#Shulman18} [[Mike Shulman]], *Comparing material and structural set theories*, Annals of Pure and Applied Logic, Volume 170, Issue 4, April 2019, Pages 465-504 ([doi:10.1016/j.apal.2018.11.002](https://doi.org/10.1016/j.apal.2018.11.002), [arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

### Relation to other axioms:

Relation to the [[axiom of choice]] ([[Diaconescu-Goodman-Myhill theorem]]):

* {#Diaconescu75} [[Radu Diaconescu]], _Axiom of choice and complementation_, Proceedings of the American Mathematical Society 51:176-178 (1975) ([doi:10.1090/S0002-9939-1975-0373893-X](https://doi.org/10.1090/S0002-9939-1975-0373893-X))

* {#GoodmanMyhill78} N. D. Goodman J. Myhill, _Choice Implies Excluded Middle_, Zeitschrift fuer Mathematische Logik und Grundlagen der Mathematik 24:461 (1978)

Relation to *[[ex falso quodlibet]]* and the *[[law of double negation]]*:

* Pedro Francisco, Valencia Vizcaíno, *Relations between ex falso, tertium non datur, and double negation elimination* &lbrack;[arXiv:1304.0272](https://arxiv.org/abs/1304.0272)&rbrack;



### In homotopy type theory
 {#ReferencesInHomotopyTypeTheory}


* {#AristotleMetaphysics} [[Aristotle]], _[[Metaphysics (Aristotle)|Metaphysics]]_, 1011b24: "Of any one subject, one thing must be either asserted or denied" 

In [[homotopy type theory]]:

* [[Univalent Foundations Project]], section 3.5 _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

In [[cohesive homotopy type theory]]:

* Mike Shulman, *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

category: foundational axiom, logic

[[!redirects Excluded Middle]]
[[!redirects excluded middle]]
[[!redirects law of excluded middle]]
[[!redirects the law of excluded middle]]
[[!redirects principle of excluded middle]]
[[!redirects the principle of excluded middle]]
[[!redirects axiom of excluded middle]]
[[!redirects the axiom of excluded middle]]

[[!redirects truncated excluded middle]]
[[!redirects truncated law of excluded middle]]
[[!redirects the truncated law of excluded middle]]
[[!redirects truncated principle of excluded middle]]
[[!redirects the truncated principle of excluded middle]]
[[!redirects truncated axiom of excluded middle]]
[[!redirects the truncated axiom of excluded middle]]

[[!redirects law of truncated excluded middle]]
[[!redirects the law of truncated excluded middle]]
[[!redirects principle of truncated excluded middle]]
[[!redirects the principle of truncated excluded middle]]
[[!redirects axiom of truncated excluded middle]]
[[!redirects the axiom of truncated excluded middle]]

[[!redirects untruncated excluded middle]]
[[!redirects untruncated law of excluded middle]]
[[!redirects the untruncated law of excluded middle]]
[[!redirects untruncated principle of excluded middle]]
[[!redirects the untruncated principle of excluded middle]]
[[!redirects untruncated axiom of excluded middle]]
[[!redirects the untruncated axiom of excluded middle]]

[[!redirects law of untruncated excluded middle]]
[[!redirects the law of untruncated excluded middle]]
[[!redirects principle of untruncated excluded middle]]
[[!redirects the principle of untruncated excluded middle]]
[[!redirects axiom of untruncated excluded middle]]
[[!redirects the axiom of untruncated excluded middle]]

[[!redirects contractible excluded middle]]
[[!redirects contractible law of excluded middle]]
[[!redirects the contractible law of excluded middle]]
[[!redirects contractible principle of excluded middle]]
[[!redirects the contractible principle of excluded middle]]
[[!redirects contractible axiom of excluded middle]]
[[!redirects the contractible axiom of excluded middle]]

[[!redirects law of contractible excluded middle]]
[[!redirects the law of contractible excluded middle]]
[[!redirects principle of contractible excluded middle]]
[[!redirects the principle of contractible excluded middle]]
[[!redirects axiom of contractible excluded middle]]
[[!redirects the axiom of contractible excluded middle]]

[[!redirects sharp excluded middle]]
[[!redirects sharp law of excluded middle]]
[[!redirects sharp principle of excluded middle]]
[[!redirects sharp axiom of excluded middle]]
