Zorn\'s lemma is a standard trick for constructing (or at least, proving the existence of) objects that are 'maximal' in an appropriate sense.  It is commonly used in [[algebra]] and named after the algebraist Max Zorn.

Zorn\'s lemma and the principle of [[excluded middle]] together imply the [[axiom of choice]].  Although it doesn\'t imply excluded middle itself, Zorn\'s lemma is not generally accepted in [[constructive mathematics]].  (Say something about how one can systematically get around this in many situations ....)

## Statement and proofs

Given a [[preorder]]ed set $(S, \leq)$, an element $x$ of $S$ is _maximal_ if $y \leq x$ whenever $x \leq y$.  A _chain_ in $S$ is a subset $A$ of $S$ such that $\leq$ is a [[total order]] on $A$.  An _upper bound_ of a subset $A$ of $S$ is an element $x$ of $S$ such that $y \leq x$ whenever $y \in A$.  In these terms, we have:

+-- {: .un_theorem}
###### Theorem (Zorn\'s lemma)

A preordered set $S$ has a maximal element if every chain has an upper bound.
=--

+-- {: .un_proof}
###### Proof

(Insert standard proof here; note usage of the axiom of choice.)
=--

+-- {: .un_proof}
###### Proof of converse

(Insert standard proof of AC from Zorn here; note usage of excluded middle.)
=--

## Usage

It is very common, when starting with a preordered set $S$, to apply Zorn\'s lemma not to $S$ itself but to an [[up-set]] (an [[under category]]) in $S$.  That is, one starts with an element $x$ of $S$ and proves the existence of a maximal element comparable to $x$.

Zorn\'s lemma may be used to prove all of the following:

* The [[Hausdorff maximal principle]]: Every chain in $S$ is contained in a maximal chain.
* The [[ultrafilter theorem]]: Every proper [[filter]] on a set may be extended to an [[ultrafilter]].
* The [[maximal ideal theorem]]: Every [[ideal]] in a [[ring]] may be extended to a [[maximal ideal]].
* The [[basis theorem]]: Every [[vector space]] (over a [[field]]) has a basis.
* etc ...

Some of these are equivalent to Zorn\'s lemma, while some are weaker; conversely, some additionally require excluded middle.