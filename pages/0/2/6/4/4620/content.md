
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Principles of omniscience
* table of contents
{: toc}

## Idea

In [[logic and foundations]], a __principle of omniscience__ is any principle of [[classical mathematics]] that is not valid in [[constructive mathematics]].  The idea behind the name (which is due to [Bishop (1967)](#Bishop)) is that, if we attempt to extend the [[computation|computational]] interpretation of constructive mathematics to incorporate one of these principles, we would have to know something that we cannot compute.  The main example is the law of [[excluded middle]] ($EM$); to apply $p \vee \neg{p}$ computationally, we must know which of these [[disjunction|disjuncts]] hold; to apply this in all situations, we would have to know everything (hence 'omniscience').

Bishop\'s principles of omniscience (stated below) may be seen as principles that extend classical logic from [[predicates]] (where $EM$ may happen to be valid, even constructively, for certain predicates) to their [[quantifications]] over infinite domains (where $EM$ is typically not constructively valid).


## The limited principle of omniscience

The __limited principle of omniscience__ ($LPO$) states that the [[existential quantification]] of any [[decidable proposition]] is again decidable.  That is,
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee \neg(\exists x, P(x)) ,$$
or equivalently
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee (\forall x, \neg{P(x)}) .$$

The __weak limited principle of omniscience__ ($WLPO$) states that the [[universal quantification]] of any [[decidable proposition]] is again decidable. That is,
$$(\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\forall x, P(x)) \vee \neg(\forall x, P(x)).$$

Note that $LPO$ implies $WLPO$: if $P(x)$ is a decidable proposition, then so is $\neg{P(x)}$, and so $LPO$ gives
$$(\exists x, \neg{P(x)}) \vee (\forall x, \neg{\neg{P(x)}}), $$
which implies
$$\neg(\forall x, P(x)) \vee (\forall x, P(x))$$
as $P$ is decidable.

We have not stated the domain of quantification of the variable $x$.  If you take it to be the [[subsingleton]] corresponding to a given [[truth value]] and apply this principle to the constantly [[true]] proposition, then $EM$ follows; conversely, $EM$ implies $LPO$ (over any domain).  However, Bishop\'s $LPO$ takes the domain to be the set of [[natural numbers]], giving a weaker principle than $EM$.  (It appears that a [[realizability topos]] based on infinite-time [[Turing machine]]s validates $LPO$ but not $EM$; see [Bauer (2011)](#Bauer).)  Note that propositions of the form $\exists x, P(x)$ when $P$ is decidable are the [[open truth values]] in the [[Rosolini dominance]].

We can also state the principle set-theoretically, with explicit reference to the domain of quantification.  Given a [[set]] $A$, the __limited principle of omniscience for $A$__ ($LPO_A$) states that, given any [[function]] $f$ from $A$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$.  Then Bishop\'s $LPO$ is $LPO_{\mathbb{N}}$, which applies to any [[infinite sequence]] of [[bits]].

While $LPO$ for $\mathbb{N}$ is a classic example of the difference between constructive and classical mathematics, $LPO$ holds for the set $\overline{\mathbb{N}}$ of [[extended natural number]]s; this is related to the fact that $\overline{\mathbb{N}}$ may constructively be given a [[compact space|compact]] topology.  See [Escard&#243; (2011)](#Escardo) for this and much more.


## The lesser limited principle of omniscience

The __lesser limited principle of omniscience__ ($LLPO$) states that, if the existential quantification of the [[conjunction]] of two [[decidable propositions]] is false, then one of their separate existential quantifications is false.  That is,
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x, P(x) \wedge \exists y, Q(y)) \Rightarrow \neg(\exists x, P(x)) \vee \neg(\exists y, Q(y)) ,$$
or equivalently
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x, P(x) \wedge \exists y, Q(y)) \Rightarrow (\forall x, \neg{P(x)}) \vee (\forall y, \neg{Q(y)}) .$$

If, as before, you take the domains of quantification to be subsingletons, you get [[de Morgan's law]] $\neg(p \wedge q) \Rightarrow \neg{p} \vee \neg{q}$ ($DM$), which is weaker than $EM$; conversely, $DM$ implies $LLPO$ (over any domain).  Again, Bishop\'s $LLPO$ takes the domain to be $\mathbb{N}$, giving a principle weaker than $DM$ (and also weaker than $LPO_{\mathbb{N}}$).

Stated set-theoretically, the __lesser limited principle of omniscience for $A$__ ($LLPO_A$) states that, given functions $f, g\colon A \to \{0,1\}$, if $1 \notin \im f \cap \im g$, then $1 \notin \im f$ or $1 \notin \im g$.  So Bishop\'s $LLPO$ is $LLPO_{\mathbb{N}}$.  Note that $LLPO_A$ follows from $LPO_A$, but not conversely.

## Analytic versions {#analytic}

Bishop introduced the above principles of omniscience to show that certain results in pointwise [[analysis]] could not be constructive, by showing that these results implied a principle of omniscience.  The principles of omniscience that appear directly in analysis are these:

*  The __analytic LPO__ states that the usual [[apartness relation]] on the set $\mathbb{R}$ of [[real numbers]] is [[decidable relation|decidable]] ($x \neq y$ or $x = y$), or equivalently __[[trichotomy]]__ for the real numbers ($x \lt y$ or $x = y$ or $x \gt y$), or equivalently, that the real numbers form a [[discrete field]].

* The __analytic WLPO__ states that $\mathbb{R}$ has [[decidable equality]].

*  The __analytic LLPO__ states that the usual order on $\mathbb{R}$ is a [[total order]] ($x \leq y$ or $x \geq y$), which (by analogy with trichotomy) may be called __dichotomy__ for the real numbers.

The analytic principles of omniscience imply the corresponding ones for natural numbers; the converses hold if we assume [[weak countable choice]] (as Bishop did).  In any case, if we use the [[modulated Cantor real numbers]] (sequential real numbers), then the sequential-analytic principles of omniscience are the same as those for natural numbers.

(Note that we need not accept $WCC$ to see that an analytic result implies a principle of omniscience and so cannot be constructively valid.)

## In the internal logic

In [[set theory]], there are actually two different notions of logic: there is the external predicate logic used to define the set theory itself, and there is the internal predicate logic induced by the set operations on [[subsingletons]] and [[injections]]. In particular, 

* An internal *[[proposition]]* is a set $P$ such that for all elements $x \in A$ and $y \in A$, $x = y$. 

* The internal proposition *[[true]]* is a [[singleton]] $\top$. 

* The internal proposition *[[false]]* is the [[empty set]]

* The internal conjunction of two internal propositions $P$ and $Q$ is the [[cartesian product]] $P \times Q$ of $P$ and $Q$. 

* The internal disjunction of two internal propositions $P$ and $Q$ is the [[image]] of the [[uniqueness quantifier|unique]] function $!_{P \uplus Q}:P \uplus Q \to 1$ from the [[disjoint union]] of $P$ and $Q$ to the [[singleton]] $\top$. 

$$P \vee Q = \mathrm{im}(!_{P \uplus Q})$$

* The internal implication of two internal propositions $P$ and $Q$ is the [[function set]] $P \to Q$ between $P$ and $Q$. 

* The internal negation of an internal proposition $P$ is the function set from $P$ to the [[empty set]]

$$\neg P = P \to \emptyset$$

* An internal proposition $P$ is a [[decidable proposition]] if it comes with a function $\chi_P:P \to 2$ from $P$ to the [[boolean domain]] $2$. 

* An *internal predicate* on a set $A$ is a [[set]] $P$ with [[injection]] $i:P \hookrightarrow A$, whose family of propositions indexed by $x \in A$ is represented by the [[preimages]] $i^*(x)$.

* The internal [[existential quantifier]] of an internal predicate $i:P \hookrightarrow A$ is the [[image]] of the [[uniqueness quantifier|unique]] function $!_P:P \to \top$ into the singleton $\top$.

$$\exists_A P = \im(!_P)$$

* The internal [[universal quantifier]] of an internal predicate $i:P \hookrightarrow A$ is the [[dependent product]] of the preimages
 
$$\forall_A P = \{f \in P^A \vert \forall x \in A, f(x) \in i^*(x) \}$$

* An internal predicate $i:P \hookrightarrow A$ is a [[decidable proposition]] if it comes with a function $\chi_P(x):i^*(x) \to 2$ into the [[boolean domain]] for all elements $x \in A$, or equivalently if it comes with a function $\chi_P:A \to 2$ from $A$ to the [[boolean domain]] $2$. 

Then the **internal LPO** for a [[family of sets]] $(A_z)_{z \in I}$ is the LPO for each $A_z$ stated in the internal logic of the set theory:

* For any internal predicate $i:P \hookrightarrow A_z$, if there is a function $\chi_P:A_z \to 2$, then the internal existential quantification of $P$, $\exists_{A_z} P = \im(!_P)$ has a function $(\exists_{A_z} P) \to 2$ into the boolean domain. 

or equivalently, as

* For any function $a:A_z \to 2$, the internal existential quantification of $P = \{x \in A_z \vert a(x) = 1\}$, $\exists_{A_z} P = \im(!_P)$ has a function $(\exists_{A_z} P) \to 2$ into the boolean domain. 

Similarly, the **internal WLPO** for a family of sets $(A_z)_{z \in I}$ is the WLPO for each $A_z$ stated in the internal logic of the set theory:

* For any internal predicate $i:P \hookrightarrow A_z$, if there is a function $\chi_P:A_z \to 2$, then the internal universal quantification of $P$, $\forall_{A_z} P = \{f \in P^{A_z} \vert \forall x \in A_z, f(x) \in i^*(x) \}$ has a function $(\forall_{A_z} P) \to 2$ into the boolean domain. 

or equivalently

* For any function $a:A_z \to 2$, the internal universal quantification of $P = \{x \in A_z \vert a(x) = 1\}$, $\forall_{A_z} P = \{f \in P^{A_z} \vert \forall x \in A_z, f(x) \in i^*(x) \}$ has a function $(\forall_{A_z} P) \to 2$ into the boolean domain. 

And finally, the **internal LLPO** for a family of sets $(A_z)_{z \in I}$ is the LLPO for each $A_z$ stated in the internal logic of the set theory:

* The internal LPO for a family of sets $(A_z)_{z \in I}$ holds only for the internal predicates $i:P \hookrightarrow A_z$ which comes with an internal predicate $j:Q \hookrightarrow A_z$ such that $i^*(x) = \neg j^*(x)$ for all $x \in A_z$. 

In particular, the internal LPO for the family of all [[subsingletons]] is internal excluded middle and the internal LLPO for the family of all [[subsingletons]] is internal [[weak excluded middle]]. 

The internal versions of the principles of omniscience, like all internal versions of axioms, are weaker than the external version of the principle of omniscience, since while [[bounded separation]] implies that one can convert any external predicate $x \in A \vdash P(x)$ on a set $A$ to an internal predicate $\{x \in A \vert P(x)\} \hookrightarrow A$, it is generally not possible to convert an internal predicate to an external predicate without a reflection rule which turns subsingletons in the set theory into propositions in the external logic. 

## Truncated and untruncated versions in homotopy type theory

In the context of [[homotopy type theory]], the various principles of omniscience can be translated in two ways, by interpreting "or" as [[propositional truncation|propositionally truncated]] ("merely or") or untruncated ("purely or"). The relationships between the truncated and untruncated principles of omniscience are as follows are:

* Truncated LPO and untruncated LPO are equivalent (due to [[Martin Escardo]], see [UFP](#UFP))

* Similarly, truncated WLPO and untruncated WLPO are equivalent.

* Untruncated LLPO is equivalent to WLPO (also due to Martin Escardo).

* In <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates WLPO from LLPO.

## Equivalent statements

There are various other results that are equivalent to or related to the principles of omniscience.  Here are a few:

* Every modulated Cantor real number has a [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) iff $LLPO_{\mathbf{N}}$ holds; every Dedekind real number has a radix expansion iff the analytic $LLPO$ holds.  At least in the presence of [[countable choice]] (which also implies that modulated Cantor reals and Dedekind reals agree), this is equivalent to the claim that the rings of radix expansions in any two bases are isomorphic. See Daniel Mehkeri\'s answer to [Feldman (2010)](#Mehkeri).

* Let $[0,1]/(0 \sim 1)$ be the [[quotient space|quotient]] of the unit [[interval]] that identifies the endpoints, and let $\mathbb{R}/\mathbb{Z}$ be the [[quotient ring]]; both are classically isomorphic to the [[circle]] $\mathbb{S}^1$. (Constructively, we take $\mathbb{S}^1$ to be $\mathbb{R}/\mathbb{Z}$, although $S^1$ can also be constructed as a [[uniform completion|completion]] of $[0,1]/(0 \sim 1)$.)  Constructively, there is an [[injection]] $[0,1]/(0 \sim 1) \hookrightarrow \mathbb{R}/\mathbb{Z}$, which is a [[bijection]] if and only if the $LLPO$ holds (for the appropriate kind of real number).

* Every [[semi-decidable proposition]] is a [[decidable proposition]] if $LPO_{\mathbf{N}}$ holds. 

* The [[boolean domain]] $\mathbb{2}$ is a [[sigma-frame|$\sigma$-frame]] iff the internal $LPO_{\mathbf{N}}$ holds. This implies that the classical notion of [[Dedekind real numbers]] can be constructed with respect to the $\sigma$-frame $\mathbb{2}$. However, in general the classical Dedekind real numbers does not coincide with the constructive notion of [[Dedekind real numbers]] constructed using the [[frame of truth values]] $\Omega$, though it does if [[excluded middle]] or [[countable choice]] holds. 

## Models

* Assuming that [[Set]] is a [[Boolean topos]], then $LPO_{\mathbb{N}}$ (the LPO for natural numbers) holds in any [[presheaf topos]] over $Set$ and indeed in any [[locally connected topos]] over $Set$, essentially since then $2^N$ is a constant object.

* The LPO for natural numbers fails in Johnstone's [[topological topos]], due to its internal continuity principle.  Hence, the analytic LPO also fails, since the modulated Cantor reals and Dedekind reals coincide in this topos.  However, the (analytic) LLPO holds, as a consequence of the preservation of finite closed unions by the inclusion of sequential spaces.

* The LPO for natural numbers can be stated in any $\Pi$-W-[[coherent category]] $\mathcal{E}$. This implies that the classical Dedekind real numbers can be constructed in $\mathcal{E}$, since the [[boolean domain object]] $2 \in \mathcal{E}$ is a $\sigma$-frame object if the LPO for natural numbers holds in $\mathcal{E}$, even though the modulated Cantor reals can only be constructed if $\mathcal{E}$ is also a [[pretopos]] and the constructive Dedekind reals can only be constructed if $\mathcal{E}$ is also an [[elementary topos]]. 

## References

* {#Bauer}  [[Andrej Bauer]] (2011) via constructivenews, [An Injection from $\mathbb{N}^{\mathbb{N}}$ to $\mathbb{N}$](http://math.andrej.com/wp-content/uploads/2011/06/injection.pdf) (pdf)

*  {#Bishop} [[Errett Bishop]] (1967), _[[Foundations of Constructive Analysis]]_ (in the introduction or chapter 1, I forget)

*  {#Escardo} [[Martín Escardó]] (2011) via constructivenews, [Infinite sets that satisfy the principle of omniscience in all varieties of constructive mathematics](http://www.cs.bham.ac.uk/~mhe/papers/omniscient-2011-07-06.pdf) (pdf)

* {#Mehkeri} David Feldman (2010) on Math.Overflow, [Radix notation and toposes](http://mathoverflow.net/questions/49775/radix-notation-and-toposes/)

* {#UFP} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* {#Booij} [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

The analytic WLPO and LLPO are mentioned in the following paper, although unfortunately it uses the phrase "analytic LPO" for what should really be the analytic *WLPO* (the reals have decidable equality):

* {#Shulman} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))


[[!redirects principle of omniscience]]
[[!redirects principles of omniscience]]

[[!redirects omniscience principle]]
[[!redirects omniscience principles]]

[[!redirects LPO]]
[[!redirects limited principle of omniscience]]
[[!redirects limited principles of omniscience]]

[[!redirects LLPO]]
[[!redirects lesser limited principle of omniscience]]
[[!redirects lesser limited principles of omniscience]]

[[!redirects WLPO]]
[[!redirects weak limited principle of omniscience]]
[[!redirects weak limited principles of omniscience]]

[[!redirects internal LPO]]
[[!redirects internal limited principle of omniscience]]
[[!redirects internal limited principles of omniscience]]

[[!redirects internal LLPO]]
[[!redirects internal lesser limited principle of omniscience]]
[[!redirects internal lesser limited principles of omniscience]]

[[!redirects internal WLPO]]
[[!redirects internal weak limited principle of omniscience]]
[[!redirects internal weak limited principles of omniscience]]

[[!redirects analytic LPO]]
[[!redirects analytic limited principle of omniscience]]
[[!redirects analytic limited principles of omniscience]]

[[!redirects analytic LLPO]]
[[!redirects analytic lesser limited principle of omniscience]]
[[!redirects analytic lesser limited principles of omniscience]]

[[!redirects analytic WLPO]]
[[!redirects analytic weak limited principle of omniscience]]
[[!redirects analytic weak limited principles of omniscience]]