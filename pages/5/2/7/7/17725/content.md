# Dominance

* table of contents
{: toc}

## Idea

In [[synthetic topology]] done as a branch of [[constructive mathematics]], a *dominance* is a set $\Sigma$ that functions as an analogue of the [[Sierpinski space]].  In particular, it allows us to define synthetically a notion of [[open subset]]: $\Sigma$ is a [[subset]] of the set of [[truth values]] $\Omega$, and a subset of a set $A$ is called "open" if its classifying map $A\to \Omega$ lands in $\Sigma$.

The name *dominance* is meant to evoke that the set is used to define the domains of a class of [[partial functions]]. I.e., in synthetic topology the partial functions whose domain is an open set and in [[synthetic computability theory]] the domains of [[computable functions|partial computable functions]]. 

## Definition

Let $\Omega$ be the set of [[truth values]].  A **dominance** is a subset $\Sigma\subseteq \Omega$ such that

1. $\top \in \Sigma$, and
1. If $U\in\Sigma$ and $P\in\Omega$ and $U\Rightarrow (P\in \Sigma)$, then $U\wedge P \in \Sigma$.

The second condition implies that $\Sigma$ is closed under binary [[meets]] $\wedge$, and hence is a sub-meet-[[semilattice]] of $\Omega$.  In [[type theory|type-theoretic]] language, the second condition says that $\Sigma$ is closed under [[dependent sums]].

The elements of $\Sigma$ are called **open** truth values.

### In dependent type theory

In [[dependent type theory]], every [[univalent]] [[type of propositions]] is a [[subtype]] of the [[type of all propositions]] $\Omega$. A **dominance** is a univalent type of propositions $(\Sigma, \mathrm{El}_\Sigma)$ with an element $\top:\Sigma$ such that

* $\mathrm{El}_\Sigma(\top)$ is a [[contractible type]]
* given a [[mere proposition]] $P$, for all elements $U:\Sigma$ with a function from $\mathrm{El}_\Sigma(U)$ to the type that $P$ is essentially $\Sigma$-small, the [[product type]] $\mathrm{El}_\Sigma(U) \times P$ is essentially $\Sigma$-small. 
$$\frac{\Gamma \vdash P \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(P)}{\Gamma, U:\Sigma \vdash q:\left(\mathrm{El}_\Sigma(U) \to \sum_{B:\Sigma} \mathrm{El}_\Sigma(B) \simeq P\right) \to \left(\sum_{C:\Sigma} \mathrm{El}_\Sigma(C) \simeq \mathrm{El}_\Sigma(U) \times P\right)}$$

## Open subsets

We define a subset $U\subseteq A$ of an arbitrary set $A$ to be **open** if for each $x\in A$, the proposition "$x\in U$" is an open truth value.  The second condition above is equivalent to saying that if $U\subseteq A$ is open and also $V\subseteq U$ is open, then $V\subseteq A$ is open.

Note that for any function $f:A\to B$, the preimage of any open set is open, since $(x\in f^{-1}(U))\iff (f(x) \in U)$.  Thus, any function is "[[continuous function|continuous]]" with respect to this "intrinsic topology."

## Overt sets

It is hard to get very far without an additional assumption that $\Sigma$ is closed under some [[joins]] as well.  However, if it were closed under *all* joins, then it would be all of $\Omega$, since any $P\in \Omega$ is the join $\bigvee_{i\in \{\star | P\}} \top$.

Given a dominance $\Sigma$, we say that a set $I$ is **overt** if $\Sigma$ is closed under $I$-indexed joins.  (This is related to, but not identical to, the notion of [[overt space]].)  In general it is reasonable to expect [[discrete object|discrete]] sets to be overt in this sense.  In some frameworks such as [[spatial type theory]] there is a formal notion of "discrete" and we can actually assert that all discrete sets are overt.   Otherwise we can assume that specific sets that we expect to be discrete are overt.  For instance, we might assume that:

* The [[empty set]] is overt, i.e. $\bot\in\Sigma$.
* The [[boolean domain]] is overt, i.e. $\Sigma$ is also a sub-join-semilattice of $\Omega$.
* The [[natural numbers]] are overt, i.e. $\Sigma$ is closed under countable joins in $\Omega$.

## Examples

* The singleton $\{\top\}$ is a dominance, for which only singletons are overt.

* The [[boolean domain]] $\{\bot,\top\}$ is a dominance.  This is the smallest dominance such that the empty set is overt and the smallest dominance such that the boolean domain is overt. (In [[classical mathematics]], of course, this and the previous example are the only two dominances, and the theory trivializes.)

* The [[initial object|initial]] [[sigma-frame|$\sigma$-frame]] $\Sigma$ is a dominance: the unique $\sigma$-frame [[homomorphism]] from $\Sigma$ to the [[frame of truth values]] $\Omega$ is an [[injection]], meaning that $\Sigma$ is a (structural) [[subset]] of $\Omega$. This is the smallest dominance such that the [[natural numbers]] $\mathbb{N}$ is overt. 

* The set of all truth values of the form $\exists n, f(n) = 1$ for some function $f:\mathbb{N}\to \mathbf{2}$ is often a dominance, though this may not be provable without further assumptions. For instance, this is the case if we assume [[countable choice]] or (perhaps) the [[propositional axiom of choice]]. When it is a dominance, this is the smallest dominance such that $\mathbb{N}$ is overt; it is called the **Rosolini dominance**.  Equivalently, it is the set of truth values of the form $x\gt 0$ for some [[Cauchy real number]] $x$.

* The set of all truth values of the form $x\gt 0$ for some [[Dedekind real number]] $x$ is also often a dominance, though this also may not be provable without further assumptions.

## See also

* [[streak]]

## References

*  [[Pino Rosolini]], *Continuity  and  Effectiveness  in  Topoi*, (PhD thesis, 1986), University of Oxford, ([pdf](https://www.researchgate.net/publication/35103849_Continuity_and_effectiveness_in_topoi))

* [[Martin Escardo]], *Topology via higher-order intuitionistic logic.*, unfinished paper, [pdf](http://www.cs.bham.ac.uk/~mhe/papers/pittsburgh.pdf)

* [[Martin Escardo]], *Synthetic  topology  of  data  types  and  classical  spaces.*  Electronic Notes in Theoretical Computer Science, 87:21--156, 2004.  [pdf](http://www.cs.bham.ac.uk/~mhe/papers/entcs87.pdf)

* [[Andrej Bauer]] and Davorin Lesnik, *Metric Spaces in Synthetic Topology*, [pdf](http://math.andrej.com/wp-content/uploads/2010/01/csms_in_synthtop.pdf)

* Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

[[!redirects dominance]]
[[!redirects dominances]]
[[!redirects Rosolini dominance]]
[[!redirects open truth value]]
[[!redirects open truth values]]
[[!redirects open proposition]]
[[!redirects open propositions]]
