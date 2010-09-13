# Principles of omniscience
* table of contents
{: toc}

## Idea

In [[logic and foundations]], a __principle of omniscience__ is any principle of [[classical mathematics]] that is not valid in [[constructive mathematics]].  The idea beind the name (which is due to [[Errett Bishop]]) is that, if we attempt to extend the computational interpretation of constructive mathematics to incorporate one of these principles, we would have to know something that we cannot compute.  The main example is the law of [[excluded middle]] ($EM$); to apply $p \vee \neg{p}$ computationally, we must know which of these disjuncts hold; to apply this in all situations, we would have to know everything.

Bishop\'s principles of omnisicience (stated below) may be seen as principles that extend classicaly logic from [[predicates]] (where $EM$ may happen to be valid, even constructively, for certain predicates) to their [[quantifications]] over infinite domains (where $EM$ is typically not constructively valid).


## The limited principle of omniscience

The __limited principle of omniscience__ ($LPO$) states that the [[existential quantification]] of any [[decidable proposition]] is again decidable.  That is,
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee \neg(\exists x, P(x)) ,$$
or equivalently
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee (\forall x, \neg{P(x)}) .$$

We have not stated the domain of quantification of the variable $x$.  If you take it to be the [[subsingleton]] corresponding to a given [[truth value]] and apply this principle to the consantly [[true]] proposition, then $EM$ follows; conversely, $EM$ implies $LPO$.  However, Bishop\'s $LPO$ takes the domain to be the set of [[natural numbers]], giving a weaker principle than $EM$.

We can also state the principle set-theoretically, with explicit reference to the domain of quantification.  Given a [[set]] $A$, the __limited principle of omniscience for $A$__ ($LPO_A$) states that, given any [[function]] $f$ from $A$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$.  Then Bishop\'s $LPO$ is $LPO_{\mathbb{N}}$, which applies to any [[infinite sequence]] of [[bits]].


## The lesser limited principle of omniscience

The __lesser limited principle of omniscience__ ($LLPO$) states that, if the existential quantification of the [[conjunction]] of two [[decidable propositions]] is false, then one of their separate existential quantifications is false.  That is,
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x, P(x) \wedge \exists y, Q(y)) \Rightarrow \neg(\exists x, P(x)) \vee \neg(\exists y, Q(y)) ,$$
or equivalently
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x, P(x) \wedge \exists y, Q(y)) \Rightarrow (\forall x, \neg{P(x)}) \vee (\forall y, \neg{Q(y)}) .$$

If, as before, you take the domains of quantification to be subsingletons, you get [[de Morgan's law]] $\neg(p \wedge q) \Rightarrow \neg{p} \vee \neg{q}$ ($DM$), which is weaker than $EM$; converesely, $DM$ implies $LLPO$.  Again, Bishop\'s $LLPO$ takes the domain to be $\mathbb{N}$, giving a principle weaker than $DM$ (and also weaker than $LPO_{\mathbb{N}}$).

Stated set-theoretically, the __lesser limited principle of omniscience for $A$__ ($LLPO_A$) states that, given functions $f, g\colon A \to \{0,1\}$, if $1 \notin \im f \cap \im g$, then $1 \notin \im f$ or $1 \notin \im g$.  So Bishop\'s $LLPO$ is $LLPO_{\mathbb{N}}$.  Note that $LLPO_A$ follows from $LPO_A$, but not conversely.


## Usage in analysis

Bishop introduced the above principles of omniscience to show that certain results in pointwise [[analysis]] could not be constructive, by showing that these results implied a principle of omniscience.  For example:

*  If the set $\mathbb{R}$ of [[real numbers]] has [[decidable equality]] ($x = y$ or $x \neq y$), then $LPO_{\mathbb{N}}$ follows.
*  If the usual order on $\mathbb{R}$ is a [[total order]] ($x \leq y$ or $x \geq y$), then $LLPO_{\mathbb{N}}$ follows.

The converses hold if we assume [[weak countable choice]] (as Bishop did); or they hold in any case for the [[Cauchy real numbers]].


[[!redirects principle of omniscience]]
[[!redirects principles of omniscience]]

[[!redirects LPO]]
[[!redirects Limited Principle of Omniscience]]
[[!redirects limited principle of omniscience]]
[[!redirects limited principles of omniscience]]

[[!redirects LLPO]]
[[!redirects Lesser Limited Principle of Omniscience]]
[[!redirects lesser limited principle of omniscience]]
[[!redirects lesser limited principles of omniscience]]
