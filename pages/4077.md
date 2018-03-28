
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

### Standard definition

A **simple group** is a [[group]] $G$ with exactly two [[quotient group]]s: the [[trivial quotient group]] $\{1\} \cong G/G$ and the group $G \cong G/\{1\}$ itself. 

Equivalently, a simple group is a group possessing exactly two [[normal subgroup|normal subgroups]]: the [[trivial subgroup]] $\{1\}$ and the group $G$ itself. One can also say that a normal subgroup is trivial iff it is not $G$, or trivial iff proper (compare the definition in constructive mathematics below).

Note that the [[trivial group]] does not itself count as simple, on the grounds that it has only *one* quotient group (or only one normal subgroup).  It may be possible to find authors that use "at most" in place of "exactly", thereby allowing the trivial group to be simple.  (Compare [[too simple to be simple]].)


### In constructive algebra

In [[constructive mathematics]], we consider a group $G$ equipped with a [[tight apartness]] $\ne$ such that the group operations are [[strongly extensional function|strongly extensional]] and use the theory of [[antisubgroups]] (which classically are the complements of subgroups).  Then $G$ is __simple__ if, given any [[normal antisubgroup]] $N$ of $G$, $N$ is trivial iff it is proper.  Explicitly, this says $N$ owns every nonidentity element (every $x$ such that $x \ne 1$) iff $N$ is [[inhabited subset|inhabited]] (with some $x$ such that necessarily $x \ne 1$).  Replacing 'iff' with 'if' here would allow the trival group to be simple.


## Examples

### Finite simple groups

Simple groups are most commonly encountered in the theory of [[finite group]]s. Every finite group $G$ admits a [[composition series]], i.e., a finite filtration of subgroups 

$$1 = G_0 \subseteq G_1 \subseteq \ldots \subseteq G_n = G$$ 

where each inclusion $G_i \subseteq G_{i+1}$ is a [[normal subgroup]] and the quotient $G_{i+1}/G_i$ (called a **composition factor**) is simple. The condition of simplicity means that that the filtration cannot be further refined by addition of strict inclusions of normal subgroups. Furthermore, the [[Jordan-Hölder theorem]] ensures that any two composition series have the same length and the same composition factors (up to permutation). 

Thus finite simple groups are in some sense the primitive building blocks of finite groups generally. The massive program of classifying all finite simple groups was announced as completed by Daniel Gorenstein in 1983, although some doubts remained because there were some gaps in proofs. Most if not all the gaps are considered by experts in the area to have been filled, but there remain some notable skeptics, including for example [[Jean-Pierre Serre]], who said in an interview 

> Whenever I asked the specialists, they replied something like: "Oh no, 
  it is not a gap; it is just something which has not been written, but 
  there is an incomplete unpublished 800-page manuscript on it."  For me, 
  it was just the same as a "gap," and I could not understand why it was 
  not acknowledged as such. ([Source](https://cs.nyu.edu/pipermail/fom/2008-November/013181.html))

and possibly also [[John H. Conway]], although according to [Joe Shipman](https://cs.nyu.edu/pipermail/fom/2008-November/013178.html), 

> A few months ago I was discussing the COFSG with John Conway and he was still pessimistic. (Meaning of course that he was confident the classification was correct, "optimistic" in his case means there are previously undiscovered finite simple groups, because they're beautiful and interesting objects and it would be disappointing to have no more.)

See [[classification of finite simple groups]]. 


### Directed colimits 

+-- {: .num_prop #directed} 
###### Proposition 
Let $S_\alpha$ be a directed system of simple groups and monomorphisms between them. Then $colim_\alpha S_\alpha$ is also simple. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose $N$ is a normal subgroup of $colim_\alpha S_\alpha$ with a non-identity element. Then $N_\alpha = N \cap S_\alpha$ is normal in $S_\alpha$ (if $x \in S_\alpha$ and $y \in N \cap S_\alpha$, then clearly $x y x^{-1}$ belongs to both $N$ and $S_\alpha$). As soon as $\alpha$ is large enough that $S_\alpha$ contains a non-identity element of $N$, it follows from simplicity of $S_\alpha$ that $N_\alpha = S_\alpha$. By directedness, this shows $N_\alpha = S_\alpha$ for all $\alpha$, and since for any $s \in S$ there is $\alpha$ such that $s \in S_\alpha$, we conclude $s \in S_\alpha = N_\alpha \subseteq N$, i.e., $N$ contains any $s \in S$. 
=-- 

### Infinite simple groups

There are simple groups of any infinite [[cardinality]] $\kappa$; take for example the smallest normal subgroup of the [[automorphism group]] $Aut(\kappa)$ containing all 3-cycles (this is the infinite version of the [[alternating group]]).

To see that $Alt(\kappa)$ is simple, it is enough to observe that it is a directed colimit of $Alt(X)$ where $X$ ranges over finite subsets of $\kappa$ of cardinality at least $5$; then simplicity of $A_n$ for integers $n \geq 0$, coupled with Proposition \ref{directed}, yields the desired result. 

A rather deeper set of examples is afforded by the following result, which follows from a theorem named after [Baer, Ulam, and Schreier](https://groupprops.subwiki.org/wiki/Baer-Schreier-Ulam_theorem). 

+-- {: .num_theorem} 
###### Theorem 
For an infinite set $X$, every proper normal subgroup of the permutation group $Sym(X)$ is contained in a maximal such normal subgroup $N_X$, consisting of all permutations that move fewer than ${|X|}$ many elements of $X$, where ${|X|}$ is the cardinality of $X$. 
=-- 

It follows that the quotient group $Q_X = Sym(X)/N_X$ is simple, and we have the following corollary. 

+-- {: .num_cor} 
###### Corollary 
Every group embeds into a simple group. 
=-- 

+-- {: .proof} 
###### Proof 
For finite groups $G$ (WLOG, of cardinality at least $3$), we have the Cayley embedding $G \hookrightarrow Sym(G)$ into the permutation group of the underlying set, and there is an embedding $Sym(G) \hookrightarrow Alt(G + 2)$ which carries an even permutation on $G$ to the obvious even permutation on $G + 2$ that fixes the elements $a, b$ of $2$, and an odd permutation $\pi$ on $G$ to the even permutation $\pi (a\; b)$. Hence $G$ embeds in a simple group $Alt(G + 2)$. 

An infinite group $G$ embeds in $Q_G$ via the Cayley embedding 

$$G \hookrightarrow Sym(G) \to Sym(G)/N_G = Q_G$$ 

noting that for any non-identity $g \in G$, the permutation $Cayley(g) = (h \mapsto g h)$ has no fixed points, hence does not belong to $N_G$, so that $G \to Q_G$ is indeed monic. 
=-- 

#### Tarski monsters 

Among the infinite simple groups, there are curious examples called "Tarski monsters" for primes $p$, infinite groups with the property that every subgroup is either trivial, of prime order $p$, or the entire group. Their existence (for all primes $p \gt 10^{75}$, according to [Wikipedia](https://en.wikipedia.org/wiki/Tarski_monster_group)) was established only in 1979, by Olshanskii. It may be shown that all such groups must be simple, and generated by two elements, and also that for each prime $p \gt 10^{75}$ there are continuum many monsters for $p$ that are distinct up to isomorphism. 

[[!redirects simple group]]
[[!redirects simple groups]]
