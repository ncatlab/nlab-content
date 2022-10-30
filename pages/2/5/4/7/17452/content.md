# Multiplicative disjunction

* table of contents
{: toc}

## Idea

In [[linear logic]]/[[linear type theory]], and also sometimes in other [[substructural logics]] such as [[relevance logic]], the **multiplicative disjunction** (also called **negative disjunction**, **intensional disjunction**, or **fission**) is a [[logical connective]] that is [[dual]] to the [[multiplicative conjunction]].  In linear logic it is often written following Girard as $A\invamp B$, but a multitude of other symbols have also been used for it, including $\oplus,\bullet,\odot,\Box,\sharp,*,\parallel$.

It is probably the rarest of the binary connectives of linear logic to appear semantically.  The additive conjunction and additive disjunction are categorically [[products]] and [[coproducts]], while the [[multiplicative conjunction]] is the [[tensor product]] of a [[monoidal category]] and the [[linear implication]] is the [[internal-hom]] of a [[closed category]]; but the multiplicative disjunction only appears nontrivially (i.e. without coinciding with one of the others) in a [[star-autonomous category]] (or more generally a [[linearly distributive category]]) that is not [[compact closed category|compact]].  Syntactically, this means that it mainly appears when the multiplicative connectives are "classical", i.e. the multiplicative [[negation]] is involutive.

It is probably also the hardest to understand intuitively of any of the linear logic connectives.  We include several intuitive explanations below.

## Definition

In terms of the [[multiplicative conjunction]] $\otimes$ and an involutive multiplicative [[negation]] $\neg$, the multiplicative disjunction can be defined as

$$ A \invamp B \coloneqq \neg (\neg A \otimes \neg B) $$

Categorically, this means that it is obtained from the tensor product in a [[star-autonomous category]] by applying the self-duality.

When classical linear logic is expressed with multiple-conclusion [[sequent calculus]], its left and right rules are

$$ \frac{\Gamma \vdash \Delta,A,B}{\Gamma \vdash \Delta, A\invamp B}  \qquad 
\frac{\Gamma,A \vdash \Delta \quad \Gamma',B\vdash \Delta'}{\Gamma,\Gamma',A\invamp B \vdash \Delta,\Delta'}$$

## Explanations

Here we collect some possible ways to understand $\invamp$ intuitively.

### In terms of resources

When linear logic is interpreted as tracking the usage of resources, we can interpret $A\invamp B$ as saying that only one of $A$ or $B$ will happen, but we don't know which, so we have to allocate enough resources to deal with each of them separately.  For example, a military general who knows that he will be attacked from either the east or the north must divide his forces between both fronts, even if the attack will only come from one direction; thus what he has is "attack from east $\invamp$ attack from north".  (If he had spies out that would be able to inform him in advance where the attack was coming from so that he could concentrate his forces there, then he would instead have an additive disjunction "attack from east $\oplus$ attack from north".)

### As a delayed or nondeterministic choice

Relatedly, we can interpret $A\invamp B$ as a "delayed choice" $A$ and $B$.  That is, if I give you $A\invamp B$, then it might appear at first that what I gave you is $A$, but as you proceed to make use of $A$ I might change my mind and decide that really I wanted to give you $B$ instead.  This can also be regarded as a "nondeterministic" choice, so that your responses to being given $A$ or $B$ have to proceed in parallel.

In particular, note that in classical linear logic it is the multiplicative disjunction, not the additive one, that is "classical" in the sense that it satisfies [[excluded middle]]:

$$ \vdash A \invamp \neg A$$

We don't have $A\oplus \neg A$ because, as in [[constructive mathematics]], we can't decide which of $A$ or $\neg A$ might hold.  But we can say $A \invamp \neg A$ because that allows us to delay making a choice until we have enough information.  This is similar to how constructively we can say $\neg\neg(A\vee \neg A)$ by a "continuation-passing" argument (see [[excluded middle]] for details).

### In game semantics

Imagine we play two parallel games of chess, where person A is playing white in one game and black in the other.  If both players play the "copycat strategy", i.e. wait for the other one to open in one game and "copy" their moves to the other game, then we have a deadlock.  In order for two simultaneous games to proceed, one player has to play

$$ Chess \otimes \neg Chess$$

and the other

$$ Chess \invamp \neg Chess$$

Here $Chess$ is the game from the perspective of white, so that the negation $\neg Chess$ is the perspective of black, and $\otimes$ denotes the [[multiplicative conjunction]].  Note that both players are playing both games --- although $\invamp$ is a disjunction, it has certain "conjunctive properties".  But the person playing $ Chess \invamp \neg Chess$  is in the stronger position, because they can play copycat in this situation, i.e. they can wait for the other to move, whereas the person playing $Chess \otimes \neg Chess$ has to play as soon as it's their turn in one of the games.  

Another, stronger interpretation is that in $A\otimes B$ we can not use any information from A to play B, and vice versa, so A and B are played by two non-communicating threads.  So in a sense, linear logic is a type system for concurrent processes that allows to avoid dead-locks.

### Disentangling additivity from disjunctive syllogism

The basic rules for proving and using a disjunction $A\vee B$ in [[intuitionistic logic]] are *additivity* and *proof by cases*.

* If we can prove $A$, we can prove $A\vee B$.  Dually, if we can prove $B$, we can prove $A\vee B$.
* If we have $A\vee B$, then we can split any proof into two cases, assuming $A$ in one and $B$ in the other.

These are also a correct set of rules for disjunction in [[classical logic]], but an equivalent pair of rules is based instead on the [[disjunctive syllogism]]:

* If assuming $\neg A$ we can prove $B$, then we can prove $A\vee B$.  Dually, if assuming $\neg B$ we can prove $A$, we can prove $A\vee B$.
* If we have $A\vee B$ and also $\neg A$, then we can conclude $B$.  Dually, if we have $A\vee B$ and also $\neg B$, then we can conclude $A$.

In linear logic, these two sets of rules are no longer equivalent: additivity and proof by cases characterize the [[additive disjunction]], while the disjunctive syllogism rules characterize the multiplicative disjunction.

In particular, note that the traditional argument for [[ex contradictione quodlibet]] depends fundamentally on having a single disjunction that obeys both additivity and the disjunctive syllogism.  (More simply, linear logic also distinguishes between the additive [[falsity]] --- the unit for the additive disjunction --- which satisfies [[ex falso quodlibet]], and the multiplicative falsity --- the unit for the multiplicative disjunction --- which doesn't.)  Thus, one might expect linear logic to be a [[paraconsistent logic]], and indeed it is (in an appropriate sense).  

## Related concepts

[[!include logic symbols -- table]]

[[!redirects multiplicative disjunction]]
[[!redirects multiplicative disjunctions]]
[[!redirects intensional disjunction]]
[[!redirects intensional disjunctions]]
[[!redirects negative disjunction]]
[[!redirects negative disjunctions]]
[[!redirects fission]]
