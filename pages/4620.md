
# Principles of omniscience
* table of contents
{: toc}

## Idea

In [[logic and foundations]], a __principle of omniscience__ is any principle of [[classical mathematics]] that is not valid in [[constructive mathematics]].  The idea behind the name (which is due to [Bishop (1967)](#Bishop)) is that, if we attempt to extend the computational interpretation of constructive mathematics to incorporate one of these principles, we would have to know something that we cannot compute.  The main example is the law of [[excluded middle]] ($EM$); to apply $p \vee \neg{p}$ computationally, we must know which of these disjuncts hold; to apply this in all situations, we would have to know everything (hence 'omniscience').

Bishop\'s principles of omniscience (stated below) may be seen as principles that extend classical logic from [[predicates]] (where $EM$ may happen to be valid, even constructively, for certain predicates) to their [[quantifications]] over infinite domains (where $EM$ is typically not constructively valid).


## The limited principle of omniscience

The __limited principle of omniscience__ ($LPO$) states that the [[existential quantification]] of any [[decidable proposition]] is again decidable.  That is,
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee \neg(\exists x, P(x)) ,$$
or equivalently
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee (\forall x, \neg{P(x)}) .$$

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

*  The __analytic LPO__ states that the usual [[apartness relation]] on the set $\mathbb{R}$ of [[real numbers]] is [[decidable relation|decidable]] ($x \neq y$ or $x = y$), or equivalently __[[trichotomy]]__ for the real numbers ($x \lt y$ or $x = y$ or $x \gt y$).
*  The __analytic LLPO__ states that the usual order on $\mathbb{R}$ is a [[total order]] ($x \leq y$ or $x \geq y$), which (by analogy with trichotomy) may be called __dichotomy__ for the real numbers.

The analytic (L)LPO implies the (L)LPO for natural numbers; the converses hold if we assume [[weak countable choice]] (as Bishop did).  In any case, if we use the [[Cauchy real numbers]] (sequential real numbers), then the sequential-analytic (L)LPO is the same as the (L)LPO for natural numbers.

(Note that we need not accept $WCC$ to see that an analytic result implies the (L)LPO and so cannot be constructively valid.)

That the real numbers have [[decidable equality]] is weaker than the analytic LPO (and decidable equality for the Cauchy reals in weaker than $LPO_{\mathbf{N}}$), unless we also assume [[Markov's principle]] (over $\mathbf{N}$ for the Cauchy reals, an analytic version for the Dedekind reals).

## Truncated and untrumcated versions in homotopy type theory

In the context of [[homotopy type theory]], the various principles of omniscience can be translated in two ways, by interpreting "or" as [[propositional truncation|propositionally truncated]] ("merely or") or untruncated ("purely or"). The relationships between the truncated and untruncated principles of omniscience are as follows are:

* Truncated LPO and untruncated LPO are equivalent (due to [[Martin Escardo]], see [UFP](#UFP))

* Similarly, truncated WLPO and untruncated WLPO are equivalent.

* Untruncated LLPO is equivalent to WLPO (also due to Martin Escardo).

* In <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates WLPO from LLPO.

## Equivalent statements

There are various other results that are equivalent to or related to the principles of omniscience.  Here are a few:

* Every Cauchy real number has a [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) iff $LLPO_{\mathbf{N}}$ holds; every Dedekind real number has a radix expansion iff the analytic $LLPO$ holds.  At least in the presence of [[countable choice]] (which also implies that Cauchy and Dedekind reals agree), this is equivalent to the claim that the rings of radix expansions in any two bases are isomorphic.  See Daniel Mehkeri\'s answer to [Feldman (2010)](#Mehkeri).

* Let $[0,1]/(0 \sim 1)$ be the [[quotient space|quotient]] of the unit [[interval]] that identifies the endpoints, and let $\mathbb{R}/\mathbb{Z}$ be the [[quotient ring]]; both are classically isomorphic to the [[circle]] $S^1$.  (Constructively, we take $S^1$ to be $\mathbb{R}/\mathbb{Z}$, although $S^1$ can also be constructed as a [[uniform completion|completion]] of $[0,1]/(0 \sim 1)$.)  Constructively, there is an [[injection]] $[0,1]/(0 \sim 1) \hookrightarrow \mathbb{R}/\mathbb{Z}$, which is a [[bijection]] if and only if the $LLPO$ holds (for the appropriate kind of real number).


## Models

* Assuming that [[Set]] is a [[Boolean topos]], then $LPO_{\mathbb{N}}$ (the LPO for natural numbers) holds in any [[presheaf topos]] over $Set$ and indeed in any [[locally connected topos]] over $Set$, essentially since then $2^N$ is a constant object.

* The LPO for natural numbers fails in Johnstone's [[topological topos]], due to its internal continuity principle.  Hence, the analytic LPO also fails, since the Cauchy and Dedekind reals coincide in this topos.  However, the (analytic) LLPO holds, as a consequence of the preservation of finite closed unions by the inclusion of sequential spaces.

## References

* {#Bauer}  [[Andrej Bauer]] (2011) via constructivenews, [An Injection from $\mathbb{N}^{\mathbb{N}}$ to $\mathbb{N}$](http://math.andrej.com/wp-content/uploads/2011/06/injection.pdf) (pdf)

*  {#Bishop} [[Errett Bishop]] (1967), _[[Foundations of Constructive Analysis]]_ (in the introduction or chapter 1, I forget)

*  {#Escardo} [[Martín Escardó]] (2011) via constructivenews, [Infinite sets that satisfy the principle of omniscience in all varieties of constructive mathematics](http://www.cs.bham.ac.uk/~mhe/papers/omniscient-2011-07-06.pdf) (pdf)

* {#Mehkeri} David Feldman (2010) on Math.Overflow, [Radix notation and toposes](http://mathoverflow.net/questions/49775/radix-notation-and-toposes/)

* {#UFP} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)


[[!redirects principle of omniscience]]
[[!redirects principles of omniscience]]

[[!redirects omniscience principle]]
[[!redirects omniscience principles]]

[[!redirects LPO]]
[[!redirects Limited Principle of Omniscience]]
[[!redirects limited principle of omniscience]]
[[!redirects limited principles of omniscience]]

[[!redirects LLPO]]
[[!redirects Lesser Limited Principle of Omniscience]]
[[!redirects lesser limited principle of omniscience]]
[[!redirects lesser limited principles of omniscience]]
