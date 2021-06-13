[[!redirects Hartogs's number]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _Hartogs number_ of a [[cardinal number]] $\kappa$ is the number of ways to [[well-order]] a set of cardinality at most $\kappa$, up to isomorphism.[^term]

[^term]: The spelling _Hartogs' number_, or even _Hartog's number_, is also in use. The latter based presumably on a misapprehension since the concept was originally proposed by the German mathematician Friedrich Hartogs (1874-1943) in 1915.

Assuming the [[axiom of choice]], it is the smallest [[ordinal number]] whose cardinality is greater than $\kappa$ and therefore the [[successor]] of $\kappa$ as a cardinal number.  But even without the axiom of choice, it makes sense and is often an effective substitute for such a successor.


## Definition

We will define the Hartogs number as a [[functor|functorial]] operation from [[sets]] to [[well-ordered sets]].  The operation on numbers is just a round-about way of talking about the same thing.

So let $S$ be a set.  Without the axiom of choice (or more precisely, the [[well-ordering theorem]]), it may not be possible to well-order $S$ itself, but we can certainly well-order some [[subsets]] of $S$.  On the other hand, if we can well-order $S$ (or a subset), then there may be many different ways to do so, even non[[isomorphism|isomorphic]] ways.  So to begin with, let us form the collection of all well-ordered subsets of $S$, that is the subset of
$$ \coprod_{A: \mathcal{P}S} \mathcal{P}(A \times A) ,$$
where $\coprod$ indicates [[disjoint union]] and $\mathcal{P}$ indicates [[power set]], consisting of those pairs $(A,R)$ such that $R$ is a well-ordering.  Then form a [[quotient set]] by identifying all well-ordered subsets that are isomorphic as well-ordered sets.  This gives a set of well-order types, or [[ordinal numbers]], which can itself be well-ordered by the general theory of ordinal numbers.

The __Hartogs number__ of $S$ is this well-ordered set, the set of all order types of well-ordered subsets of $S$.  It is denoted $\aleph(S)$.  If $\kappa$ is the cardinality of $S$, then let $\kappa^+$ be the cardinality or ordinal rank (as desired) of the Hartogs number of $S$; this is called the __Hartogs number__ of $\kappa$.

There are other ways to encode $\aleph(S)$. A subset $A \subseteq S$ with a well-ordering can be specified through the collection of its initial segments or [[lower set|down-sets]], i.e., a suitable family of subsets of $S$ named by an [[element]] of $P P(S)$. Thus the set of well-orderings of subsets of $S$ can be defined as a suitable subset of $P P(S)$. Similarly, an equivalence class of such structures corresponding to a given order type is also definable as a subset of $P P(S)$, i.e., is named by a suitable element of $P P P(S)$, so $\aleph(S)$ which is the set of such equivalence classes is definable as a subset of $P P P(S)$. 

All of the defining formulas in this description involve only bounded quantification, i.e., can be expressed in the language of [[ZFC|BZC]] or in [[ETCS]]. The proof that $\aleph(S)$ is well-ordered (by existence of $P$-[coalgebra](https://ncatlab.org/nlab/show/well-founded+relation#coalgebraic_formulation) morphisms between representatives of order types) can be enacted in these theories without using the axiom of choice, hence the basic theory of $\aleph(S)$ can be carried out in BZ (bounded Zermelo set theory, without choice). 

## Properties

+-- {: .num_theorem} 
###### Theorem 
There is no [[injection]] $\aleph(S) \to S$. 
=--

This theorem is to [[Cantor's theorem]] as [[Burali-Forti's paradox]] is to [[Russell's paradox]]. This observation alone hints how the proof goes: 

+-- {: .proof} 
###### Proof 
As observed before, $\aleph(S)$ is well-ordered. Suppose there were an injection $i: \aleph(S) \to S$; then $i$ gives a bijection of $\aleph(S)$ onto its image $I$. By transport of structure, $I$ uniquely admits a well-ordering for which $i$ is an isomorphism of well-ordered sets. Using this well-ordering, there is an initial segment inclusion 

$$j: I \hookrightarrow \aleph(S)$$ 

which takes $x \in I$ to (the order type of) $\{y \in I: y \lt x\}$. Since there can be at most one initial segment inclusion between well-orders (cf. [simulation](https://ncatlab.org/nlab/show/well-founded+relation#simulations)), $j$ must coincide with the isomorphism $i^{-1}$, which is onto. This means $I$ itself, as an order type, must be of the form $I = \{y \in I: y \lt x\}$ for some $x \in I$, which in turn implies $x \lt x$, a contradiction. 
=-- 

According to this theorem, using the usual ordering of cardinal numbers, $\kappa^+ \nleq \kappa$.  So if this $\leq$ is a [[total order]] (a statement equivalent to the [[axiom of choice]]), we can say that $\kappa^+ \gt \kappa$.

Even without choice, however, we can say this:  If $\alpha$ is an ordinal number such that $|\alpha| \nleq \kappa$, then $\kappa^+ \leq \alpha$.  (Notice that we\'ve shifted our thinking of the Hartogs number from a cardinal to an ordinal.)  That is, $\kappa^+$ is the smallest ordinal number whose cardinal number is not at most $\kappa$.  This doesn\'t use any form of choice except for [[excluded middle]]; we only need choice to conclude that $|\kappa^+| \gt \kappa$.

The axiom of choice also implies the well-ordering theorem, that any set can be well-ordered.  Thus with choice, $\kappa^+$ is (now as a cardinal again) the smallest cardinal number greater than $\kappa$; this explains the notation $\kappa^+$. 

### GCH implies AC 

In [[ZF]] (without C, the [[axiom of choice]]), a set $X$ can be well-ordered if there is an injection $i: X \to \aleph(X)$, for any subset of a well-ordered set inherits a well-order. As an amusing illustration of this principle, we will prove an old result due to Sierpi&#324;ski, following [Gillman](#Gill): 

+-- {: .num_theorem} 
###### Theorem 
If the generalized [[continuum hypothesis]] holds, then the 
[[axiom of choice]] holds, i.e., ZF + GCH implies AC. 
=-- 

(Recall the GCH as formulated in ZF: for infinite sets $Y, Z$, if $|Y| \leq |Z| \leq |P(Y)|$, then $|Y| = |Z|$ or $|Z| = |P(Y)|$, letting $|Y|$ denote the cardinality as usual and where $|Y| \leq |Z|$ means there is a [[monomorphism]] $Y \to Z$.) 

+-- {: .proof} 
###### Proof 
In fact we will show that any set $Y$ can be well-ordered, which implies AC (see the article [[Zorn's lemma]]). We start with a technical trick: any $Y$ can be embedded in a set $X$ with the property $|X| = |X + X|$ (consider for example $X = P(\mathbb{N} + Y)$), and then it suffices to well-order such $X$, since we can then pull back the well-ordering along the embedding to well-order $Y$. Iterated power sets of $X$ also have that property. 

Now, the Hartogs number $\aleph(X)$ can be constructed explicitly in ZF as a subset of the triple power set $P^3(X) = P P P(X)$. We will show for $n \in \{1, 2, 3\}$ that under GCH, the hypothesis $|\aleph(X)| \leq |P^n(X)|$, true for $n = 3$, leads to one of two conclusions: 

1. $|X| \leq |\aleph(X)|$ (whence $X$ can be well-ordered), or 

1. $|\aleph(X)| \leq |P^{n-1}(X)|$. 

If we land in case 2, then we loop around and feed that conclusion back into the hypothesis and iterate. Iterating this, we cannot descend through case 2 all the way down to $|\aleph(X)| \leq |P^0(X)| = |X|$, so after a few iterations we wind up in case 1 anyway: $X$ can be well-ordered. 

To show this, we need a spot of cardinal arithmetic in ZF. First, we already observed that any $P = P^n(X)$ for $n \geq 0$ has the property $|P| = |2P|$. Second, we **claim** 

* If $P, A$ are sets such that $|P| = |2P|$ and $|A+P| = |2^P|$, then $|2^P| \leq |A|$  

whose ZF-proof we give in a moment. Granting the claim, let us continue. We have 

$$|P^{n-1}(X)| \leq |\aleph(X)| + |P^{n-1}(X)| \stackrel{hypoth}{\leq} |P^n(X)| + |P^{n-1}(X)| \leq 2|P^n(X)| = |P^n(X)|$$ 

or just 

$$|P^{n-1}(X)| \leq |\aleph(X)| + |P^{n-1}(X)| \leq |P^n(X)|.$$ 

By GCH, one of those two inequalities is an equality. If the first inequality is an equality, then we conclude $|\aleph(X)| \leq |P^{n-1}(X)|$, which lands us in case 2. If the second inequality is an equality, then the claim applies and we conclude $|P^n(X)| \leq |\aleph(X)|$, in which case $|X| \leq |P^n(X)| \leq |\aleph(X)|$ and we land in case 1. 

So we are done except for the claim. Given bijections $A + P \cong 2^P$, $P + P \cong P$, let $f$ be the evident composite 

$$P \stackrel{incl}{\to} A + P \cong 2^P \cong 2^{P + P} \cong 2^P \times 2^P \stackrel{\pi_1}{\to} 2^P$$ 

where $\pi_1$ denotes first projection. Let $C$ be an element not in the image of $f$, e.g., $C = \{x \in P: x \notin f(x)\}$ ([[Cantor's theorem]]). It follows that under the bijection $A + P \cong 2^P \times 2^P$, those elements of $A + P$ that map to elements of the fiber $\pi_1^{-1}(\{C\})$ can only belong to the summand $A$. Thus it is a subset of $A$ that maps bijectively onto $\pi_1^{-1}(\{C\}) \cong 2^P$, and this proves $|2^P| \leq |A|$. 
=-- 

### Equivalent forms of AC 

Methods somewhat similar to those used to prove GCH implies AC can be used to establish equivalent forms of AC. 

+-- {: .num_theorem} 
###### Theorem 
**(Tarski)** 
Over ZF (or ETCS without choice), the axiom of choice holds iff every infinite set $Y$ can be put into bijection with its square: $Y^2 \cong Y$. 
=-- 

+-- {: .proof} 
###### Proof 
The more interesting direction is the "if", so we assume every infinite set can be put into bijection with its square. 

It suffices to prove that every $X$ can be well-ordered. WLOG we prove this for (Dedekind) infinite $X$, since every $X$ embeds in a Dedekind infinite set (such as $X + \mathbb{N}$), and we can pull back a well-order on the latter along such an embedding to one on the former. 

For infinite $X$, let $Y$ be the disjoint union $X + \aleph(X)$, and let $\phi: Y \times Y \to Y$ be a bijection. We claim that for all $x \in X$, there exist $\alpha, \beta \in \aleph(X)$ such that $\phi(x, \alpha) = \beta$. If that were not true, then there would exist $x \in X$ such that for all $\alpha \in \aleph(X)$ we have $\phi(x, \alpha) \notin \aleph(X)$, or in other words for all $\alpha \in \aleph(X)$ we have $\phi(x, \alpha) \in X$, so that $\phi(x, -)$ defines an injection $\aleph(X) \rightarrowtail X$. This is impossible. 

By the claim, for each $x \in X$ there is a least pair $(\alpha_x, \beta_x) \in \aleph(X)^2$, considered in [[lexicographic order]], such that $\phi(x, \alpha_x) = \beta_x$. This assignment $x \mapsto (\alpha_x, \beta_x)$ defines an embedding $X \to \aleph(X)^2$ into a well-ordered set, so that $X$ inherits a well-order by restriction along the embedding, and we are done. 
=-- 

A very similar method establishes the following claim. 

+-- {: .num_prop} 
###### Proposition 
Over ZF, AC is equivalent to the statement that every inhabited set admits a group structure. 
=-- 

+-- {: .proof} 
###### Proof 
Every inhabited finite set admits a cyclic group structure, and under AC any infinite set can be put in bijection with the collection of its finite subsets, which forms a group under symmetric difference. 

Conversely, suppose $Y = X + \aleph(X)$ admits a group structure. Then for every $x \in X$, there exist $\alpha, \beta \in \aleph(X)$ such that $x\alpha = \beta$. For if that were not true, then there exists $x \in X$ such that for all $\alpha \in \aleph(X)$, we have $x \alpha \notin \aleph(X)$, i.e., for all $\alpha \in \aleph(X)$ we have $x\alpha \in X$, which implies left multiplication by $x$ defines an injection $\aleph(X) \rightarrowtail X$, contradiction. 

So for each $x \in X$, there exists a least $(\alpha_x, \beta_x) \in \aleph(X)^2$ in lexicographic order such that $x \alpha_x = \beta_x$. This again defines an embedding $x \mapsto (\alpha_x, \beta_x)$ into a well-ordered set $\aleph(X)^2$, and we are done. 
=-- 


## Examples

For $n$ a [[natural number]] regarded as the cardinal number of a [[finite set]], $n^+$ is the usual [[successor]] $n + 1$.  This result uses excluded middle; else we get the _plump_ successor of $n$, which may be rather larger.

For $\aleph_0$ the cardinality of the set of all [[natural number]]s, the Hartogs number $\aleph_0^+ = \omega_1$ is the smallest [[uncountable set|uncountable]] ordinal.  Assuming the axiom of choice ([[countable choice]] and excluded middle are enough), we have $\aleph_0^+ = \aleph_1$ as a cardinal.

In general, we get a sequence $\omega_\alpha$ of infinite cardinalities of well-orderable sets; assuming excluded middle, every infinite well-orderable cardinality shows up in this sequence.  Assuming the axiom of choice, every infinite cardinal shows up, and we have $|\omega_\alpha| = \aleph_\alpha$.  (Actually, there\'s no real need to begin with infinite cardinals; if we started with $\omega_0 = 0$ instead of $\omega_0 = \mathbf{N}$ and $\aleph_0 = 0$ instead of $\aleph_0 = |\mathbf{N}|$, then absolutely *every* cardinality or well-orderable cardinality would appear.)

## Related page

* [wikipedia entry](https://en.wikipedia.org/wiki/Hartogs_number)

## Related entries

* [[Lindenbaum number]]

* [[well-ordering theorem]]

* [[axiom of choice]]

* [[diagonal argument]]

## References

* Friedrich Hartogs, _&#220;ber das Problem der Wohlordnung_ , Math. Ann. **76** no.4 (1915) pp.438-443. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002266105))

* [[Radu Diaconescu]], _On Comparability in a Topos_ , Proc. AMS **98** no.3 (1986) pp.389-393. ([pdf](http://www.ams.org/journals/proc/1986-098-03/S0002-9939-1986-0857927-9/S0002-9939-1986-0857927-9.pdf)) 

* Leonard Gillman, _Two Classical Surprises Concerning the Axiom of Choice and the Continuum Hypothesis_, Amer. Math. Monthly 109 (June-July 2002), 544-553. ([pdf](https://www.maa.org/sites/default/files/pdf/upload_library/22/Ford/Gillman544-553.pdf)) 
 {#Gill} 

The last section of Gillman's paper is based on Sierpi&#324;ski's 1947 proof which may be found [here](http://matwbn.icm.edu.pl/ksiazki/fm/fm34/fm3411.pdf). 


[[!redirects Hartog's number]]
[[!redirects Hartogs number]]
[[!redirects Hartogs's number]]
[[!redirects Hartogs' number]]
[[!redirects Hartogg's number]]
[[!redirects Hartog's number]]

