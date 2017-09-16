Zorn\'s lemma is a standard trick for constructing (or at least, proving the existence of) objects that are 'maximal' in an appropriate sense.  It is commonly used in [[algebra]] and named after the algebraist Max Zorn.

Zorn\'s lemma and the principle of [[excluded middle]] together imply the [[axiom of choice]].  Although it doesn\'t imply excluded middle itself, Zorn\'s lemma is not generally accepted in [[constructive mathematics]].  (Say something about how one can systematically get around this in many situations ....)

## Statement and proofs

Given a [[preorder]]ed set $(S, \leq)$, an element $x$ of $S$ is _maximal_ if $y \leq x$ whenever $x \leq y$.  A _chain_ in $S$ is a subset $A$ of $S$ such that $\leq$ is a [[total order]] on $A$.  An _upper bound_ of a subset $A$ of $S$ is an element $x$ of $S$ such that $y \leq x$ whenever $y \in A$.  In these terms, we have:

+-- {: .un_theorem}
###### Theorem (Zorn\'s lemma)

A nonempty preordered set $S$ has a maximal element if every chain has an upper bound.
=--

+-- {: .un_proof}
###### Proof

The proof may be arranged in the following steps: 
* For each subset of $A \subseteq S$ which is well-ordered under the preorder it inherits from $S$, choose a _strict_ upper bound $f(A) \in S$ [if it has one]. 
* Say a well-ordered subset $A$ is $f$-_inductive_ if for all $x \in A$, $x = f(\{y \in A: y \lt x\})$. Thus $A_0 = \emptyset$ is inductive, as is $A_1 = \{f(A_0)\}$, $A_2 = A_1 \cup \{f(A_1)\}$, $A_3 = A_2 \cup \{f(A_2)\}$ and so on. Intuitively, using the chain hypothesis, one can [by transfinite induction] define $A_\alpha$ for ordinals $\alpha$ by appending strict upper bounds in this way, until at some point $\alpha$, one has run out of further strict upper bounds to choose from. But by hypothesis, $A_\alpha$ does have an upper bound $x$. This element is necessarily maximal. 
* More precisely, $f$-inductive sets are well-ordered by inclusion. For if $A$ and $B$ are distinct (well-ordered and) $f$-inductive sets, then there is a smallest element contained in one but not the other, say $x \in A$ but $\neg(x \in B)$. But then $\{y \in A: y \lt x\}$ is a down-closed subset of $B$, i.e., is an initial segment of $B$. If it were a _proper_ subset of $B$, then for the least $z \in B$ in its complement we would have 
$$\{y \in A: y \lt x\} = \{y' \in B: y' \lt z\}$$ 
whence by applying $f$ to both sides, we infer $x = z$ by $f$-inductivity of $A$ and $B$, contradiction. In that case, $B = \{y \in A: y \lt x\}$. In other words, one of $A$, $B$ is an initial segment of the other. 
* Therefore the union of all $f$-inductive sets is also $f$-inductive. Being the maximal $f$-inductive set $M$, it contains any upper bound (in fact there is only one up to isomorphism), and this element is necessarily maximal in $S$.
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