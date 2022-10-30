
# Relational $\beta$-modules
* table of contents
{: toc}

## Idea

>One of my early Honours students at [[Macquarie University]] baffled his proposed Queensland graduate studies supervisor who asked whether the student knew the definition of a [[topological space]]. The aspiring researcher on [[dynamical system]]s answered positively: "Yes, it is a relational $\beta$-module!"  I received quite a bit of flak from colleagues concerning that one; but the student [[Peter Kloeden]] went on to become a full professor of mathematics in Australia then Germany.
---[[Ross Street]], in _[[An Australian conspectus of higher categories]]_

In 1970, [[Michael Barr]] gave an abstract definition of [[topological space]] based on a notion of [[convergence]] between [[ultrafilters]] (building on work by [[Ernest Manes]] on [[compact Hausdorff spaces]]).   Succinctly, Barr defined topological spaces as 'relational $\beta$-modules'.  Here we unpack this definition and examine its properties.

The correctness of this definition (in the sense of matching [[Bourbaki]]\'s definition) is equivalent to the [[ultrafilter principle]] ($UP$).  However, the definition can be treated on its own, even in a context without $UP$.  So we also consider the properties of relational $\beta$-modules when these might not match Bourbaki spaces.


## Definitions

### Abstract

If $S$ is a [[set]], let $\beta{S}$ be the set of [[ultrafilters]] on $S$.  This operation $\beta$ extends to a [[functor]] on [[Set]] and even on [[Rel]] as follows:

...

This functor $\beta$ becomes a [[monad]] on $Rel$ and even on $Set$ as follows:

...

Then a __relational $\beta$-module is a [[lax algebra]] (module) of $\beta$ on the [[2-poset]] $Rel$.


### Concrete

A __relational $\beta$-module__ is a [[set]] $S$ and a [[binary relation]] $\to$ between [[ultrafilters]] on $S$ and [[elements]] of $S$ that satisfies a certain rule.

To explain this rule, we first define a [[subset]] $A$ of $S$ to be __[[open subset|open]]__ if $A \in \mathcal{U}$ whenever $\mathcal{U} \to x \in A$.  Then the requirement on $\to$ is a converse:

*  $\mathcal{U} \to x$ if $A \in \mathcal{U}$ whenever $A$ is open and $x \in A$.

...


## Properties

We say that $\mathcal{U}$ __converges__ to $x$ if $\mathcal{U} \to x$.

As above, a [[subset]] $A$ of $S$ is __[[open subset|open]]__ if $A \in \mathcal{U}$ whenever $\mathcal{U} \to x \in A$.  On the other hand, $A$ is __[[closed subset|closed]]__ if $x \in A$ whenever $A \in \mathcal{U} \to x$.

A relational $\beta$-module is __[[compact space|compact]]__ if every ultrafilter converges to at least one point.  It is __[[Hausdorff space|Hausdorff]]__ if every ultrafilter converges to at most one point.  Thus, a __[[compactum]]__ is (assuming $UF$) precisely a relational $\beta$-module in which every ultrafilter converges to exactly one point, that is in which the action of the monad $\beta$ lives in $Set$ rather than in $Rel$.

...


## Relation to nonstandard analysis

In [[nonstandard analysis]] (which implicitly relies throughout on $UF$), one may define a topological space using a relation between hyperpoints (elements of $S^*$) and points (elements of $S$).  If $u$ is a hyperpoint and $x$ is a point, then we write $u \approx x$ or $st(u) = x$ and say that $x$ is a __[[standard part]]__ of $u$.  This relation must satisfy a condition analogous to the condition in the definition of a relational $\beta$-module.  The nonstandard defintions of open set, compact space, etc are also analogous.  (Accordingly, one can speak of *the* standard part of $u$ and use the notation $st(u)$ without difficulty only for Hausdorff spaces.)

So ultrafilters behave very much like hyperpoints.  This is not to say that ultrafilters *are* (or even can be) hyperpoints, as they don't obey the [[transfer principle]].  Nevertheless, one does use ultrafilters to construct the [[model]]s of nonstandard analysis in which hyperpoints actually live.  Intuitions developed for nonstandard analysis can profitably be applied to ultrafilters, but the transfer principle is not valid in proofs.


## Relation to other topological concepts

If $\beta$ is treated as a monad on $Set$ instead of on $Rel$, then its algebras are the [[compacta]] (the compact Hausdorff spaces), again assuming $UF$.

There should be an analogous treatment of [[uniform spaces]] based on an [[equivalence relation]] between ultrafilters.  (In nonstandard analysis, this becomes a relation $\approx$ of infinite closeness between hyperpoints.)


[[!redirects relational beta-module]]
[[!redirects relational beta-modules]]
[[!redirects relational ∞-module]]
[[!redirects relational ∞-modules]]
