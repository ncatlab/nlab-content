
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Zorn\'s Lemma
* table of contents
{: toc}

## Idea

_Zorn\'s lemma_, also known as Kuratowski-Zorn lemma, is a [[proposition]] in [[set theory]] and [[order theory]]. It says that: _A [[preorder]] in which every sub-[[total order]] has an [[upper bound]] has a [[maximal element]]._ 

Depending on the chosen perspective on [[foundations]]
this is either an [[axiom]] or a [[deduction|consequence]] of the [[axiom of choice]]; or neither if neither the axiom of choice nor Zorn's lemma is assumed as an axiom.
Conversely, Zorn\'s lemma and the [[axiom of excluded middle]] together imply the [[axiom of choice]].  Although it doesn\'t imply excluded middle itself, Zorn\'s lemma is not generally accepted in [[constructive mathematics]] as an [[axiom]].  Sometimes the maximal element is only a convenience, and it's enough to use the entire poset or perhaps the collection of all chains instead; sometimes, the use of Zorn's Lemma is essential.

In as far as it holds or is assumed to hold, Zorn's lemma is a standard method for constructing (or at least, [[proof|proving]] the [[existence]] of) objects that are 'maximal' in an appropriate sense.  It is commonly used in [[algebra]] and named after the algebraist [[Max Zorn]] (although he himself protested the naming after him).



## Statement and proofs

+-- {: .num_defn #ChainAndUpperBound}
###### Definition

* Given a [[preorder|preordered]] set $(S, \leq)$, an element $x$ of $S$ is _[[maximal element|maximal]]_ if $y \leq x$ whenever $x \leq y$.  

* A _[[chain]]_ in $S$ is a [[subset]] $A \hookrightarrow S$ such that $\leq$ is a [[total order]] on $A$.  

* An _[[upper bound]]_ of a subset $A$ of $S$ is an element $x$ of $S$ such that $y \leq x$ whenever $y \in A$.  
=--

+-- {: .num_defn #statement}
###### Definition

The [[proposition]] __Zorn\'s Lemma__ states that a preordered set $S$ has a maximal element if every chain in $S$ has an upper bound.
=--

+-- {: .num_theorem #TheLemma}
###### Theorem

Suppose the [[axiom of choice]] holds. Then Zorn\'s Lemma holds.
=--

+-- {: .proof}
###### Proof
By contradiction. (We freely use the [[axiom of excluded middle]], which in any case follows from AC, the axiom of choice. The one use made of AC is noted below. WLOG we prove the result for [[posets]].) 

Suppose $S$ has no maximal element. Then every chain $C \subseteq S$ has a *strict* upper bound: an element $x$ such that $c \lt x$ for all $c \in C$. (Take an upper bound $y$ of $C$, then $y$ is not maximal by supposition, so any $x$ with $y \lt x$ will serve.) For each $W \subseteq S$ that is well-ordered by $\leq$, use AC to choose a strict upper bound $f(W)$ of $W$. Given a such a function $f: Well(S) \to S$ from well-ordered subsets of $S$ to $S$, let us say $W \in Well(S)$ is *$f$-inductive* if for every $x \in W$, we have $x = f(\{y \in W: y \lt x\})$. 

Let $Y, Z \in Well(S)$ be $f$-inductive sets; we will show one is an [[lower set|initial segment]] of the other. Let $I$ be the union of all subsets of $S$ that are initial segments of both $Y$ and $Z$; then $I$ is maximal among such initial segments of both. Suppose $I$ is *properly* contained in both; let $y$ be the least element of $Y \setminus I$, and $z$ the least element of $Z \setminus I$. Then $\{x \in Y: x \lt y\} = I = \{x' \in Z: x' \lt z\}$, so by $f$-inductivity of $Y, Z$, we have $y = f(I) = z$. Thus $I$ extends to an initial segment $I \cup \{y\} = I \cup \{z\}$, contradicting maximality of $I$. Therefore we must have $I = Y$ or $I = Z$, so one of $Y, Z$ is an initial segment of the other.  

So the collection of $f$-inductive sets is totally ordered by inclusion of initial segments, making their union $U$ the maximal $f$-inductive set (Lemma \ref{wo} below). Appending its strict upper bound $f(U)$, the chain $U \cup \{f(U)\}$ is a larger $f$-inductive set, contradiction. The proof is complete. 
=--

+-- {: .num_remark }
###### Remark

The [[empty set]] (with its unique structure as preordered set) is not an exception to Zorn\'s lemma, as the chain $\emptyset$ does not have an upper bound.
=-- 

+-- {: .num_remark} 
###### Remark 
The proof above (originally by [Kneser](#Kneser)) can be seen as an application of general recursion theory &#224; la Paul Taylor's [[Practical Foundations of Mathematics|book]], which in turn is inspired in large part by [Osius](#Osius). In particular, initial segments are the same as $P$-coalgebra maps between [[well-founded coalgebras]], and the maximal $U$ constructed is a maximal attempt with respect to a partial algebra structure $f: P(S) \rightharpoonup S$, following Taylor's formulation of the recursion scheme. For a slightly different arrangement of the facts, one very commonly found in the literature, see the account of the Bourbaki-Witt theorem below. 
=-- 

+-- {: .num_lemma #wo} 
###### Lemma 
Let $P_\alpha$ be a collection of subsets of a set $S$, each equipped with a well-ordering $\leq_\alpha$, such that for any $\alpha, \beta$, one of $P_\alpha, P_\beta$ (each with their orderings) is an [[lower set|initial segment]] of the other. Let $P$ be the union $\cup_\alpha P_\alpha$, equipped with the ordering $x \leq y$ if $x \leq_\alpha y$ in some $P_\alpha$ containing them both. Then $P$ is well-ordered by $\leq$, with each $P_\alpha$ an initial segment of $P$. 
=-- 

+-- {: .proof} 
###### Proof 
Observe that $\leq$ is well-defined, and is a [[total order]]: if $x, y \in P$, then $x \in P_\alpha$ and $y \in P_\beta$ for some $\alpha, \beta$, where one of $P_\alpha, P_\beta$ contains the other, say $P_\alpha \subseteq P_\beta$, whence $x, y$ are comparable in $P_\beta$. If $T$ is an inhabited subset of $P$, then $T \cap P_\alpha$ is inhabited for some $\alpha$, so there is a minimal element $t \in T \cap P_\alpha$ with respect to $\leq_\alpha$. This $t$ is minimal in $T$ with respect to $\leq$, for if $s \in T$, $s \leq t$, then $s \in P_\alpha$ by the initial segment condition, and then $t \leq s$ by definition of $t$. 
=-- 

+-- {: .num_theorem}
###### Theorem 

If Zorn\'s Lemma and the [[principle of excluded middle]] hold, then so do the [[well-ordering principle]] and the [[axiom of choice]].
=--

+-- {: .proof}
###### Proof

We first show that Zorn's lemma implies the classical [[well-ordering principle]]. The [[axiom of choice]] easily follows from the well-ordering principle. 

1. Let $A$ be a set, and consider the [[poset]] whose elements are pairs $(X, R)$, where $X \in P A$ and $R$ is a (classical) [[well-order]]ing on $X$, ordered by $(X, R) \leq (Y, S)$ if $X$ as a well-ordered set is an initial segment of $Y$. If $C$ is a chain in the poset consisting of subsets $X_\alpha$, then their union $X$ is a well-order by Lemma \ref{wo}, and so the hypothesis of Zorn's lemma is satisfied. 

2. By Zorn's lemma, conclude that the poset above contains a maximal element $(X, R)$, where $X \subseteq A$. We claim $X = A$; suppose not (here is where we need [[excluded middle]]), and let $x$ be a member of the complement $\neg X$. Well-order $X \cup \{x\}$, extending $R$ by deeming $x$ to be the final element. This shows $(X, R)$ was not maximal, contradiction. Hence any set $A$ may be well-ordered. 

3. The [[axiom of choice]] follows: suppose given a [[surjection]] $p: E \to B$, so that every [[fiber]] $p^{-1}(b)$ is [[inhabited set|inhabited]]. Consider any well-ordering of $E$, and define $s: B \to E$ by letting $s(b)$ be the least element in $p^{-1}(b)$ with respect to the well-ordering. This gives a section $s$ of $p$. 
=--


## Bourbaki-Witt theorem 

Many accounts of the proof of Zorn's lemma start by establishing first the so-called Bourbaki-Witt theorem, which does not require AC and is of interest in its own right. However, it too does not admit a constructive proof; see [Bauer](#Bauer) for a demonstration that it is not valid in the [[effective topos]]. That said, the issue is subtle enough that the Bourbaki-Witt theorem nonetheless holds in topos with a [[geometric morphism]] to $Set$, for instance any [[Grothendieck topos]], assuming B-W holds in $Set$ ([Bauer-Lumsdaine 2013](#Bauer-Lumsdaine_13)).

+-- {: .num_theorem} 
###### Theorem 
**(Bourbaki-Witt)** 
Let $P$ be an inhabited [[poset]] such that every chain has a [[supremum|least upper bound]], and $s: P \to P$ a function that is *inflationary*: satisfies $x \leq s(x)$ for all $x$. Then $s$ has a [[fixed point]]: an $x$ such that $s(x) = x$. 
=-- 

+-- {: .proof} 
###### Proof 
Without loss of generality, assume $P$ has a bottom element $0$; otherwise just pick an element $a \in P$ and replace $P$ with the upward set $\uparrow a$. 

Say that a subset $I \subseteq P$ is *$s$-inductive* if: $0 \in I$, $I$ is closed under $s$ ($s(I) \subseteq I$), and $I$ contains the sup of any chain in $I$. The intersection of any family of $s$-inductive sets is also $s$-inductive, so the intersection $M$ of all $s$-inductive sets is $s$-inductive. 

The idea is that $M$ is totally ordered (is a chain) by the following intuition: 
the elements of $M$ are $0, s(0), s s(0), \ldots s^n(0), \ldots$, where we continue by transfinite induction: at limit ordinals $\alpha$ define $s^\alpha(0)$ to be the sup of $\{s^\beta(0): \beta \lt \alpha\}$, and at successors define $s^{\alpha + 1}(0) = s(s^\alpha(0))$. We cannot have a strictly increasing chain that goes on forever, by cardinality considerations, so at some point we hit an $\alpha$ such that $s^{\alpha + 1}(0) = s^\alpha(0)$, which provides a fixed point. (What could be nonconstructive about that? See this [comment](https://golem.ph.utexas.edu/category/2012/10/the_zorn_identity.html#c042428) by Lumsdaine.) In any case, once we prove $M$ is totally ordered, the sup of $M$ is obviously a fixed point. 

Without getting into ordinals, one may prove $M$ is totally ordered as follows. 
Call an element $c \in M$ a *cap* if $x \lt c$ for $x\in M$ implies $s(x) \leq c$. For each $c \in M$, put $M_c = \{x \in M: x \leq c \vee s(c) \leq x\}$. A routine verification shows $M_c$ is $s$-inductive if $c$ is a cap, so in fact $M_c = M$ by minimality of $M$. Then, show that the set of caps is $s$-inductive. This is also routine if we avail ourselves of the just-proven fact that $M_c = M$ for any cap (but consult Appendix 2 in Lang's Algebra if you get stuck). So again by minimality of $M$, every element of $M$ is a cap. Finally, if $c, d \in M$, use the fact that $c$ is a cap to conclude either that $d \leq c$ or $s(c) \leq d$, whence $c \leq s(c) \leq d$; thus we see any two elements are comparable.  
=-- 

For a discussion of how to get from Bourbaki-Witt to Zorn, see either Lang or this $n$-Category Caf&#233; [post](https://golem.ph.utexas.edu/category/2012/10/the_zorn_identity.html) by [[Tom Leinster]], especially the main post which gives three very closely related results bearing on Zorn's lemma, and a follow-up comment [here](https://golem.ph.utexas.edu/category/2012/10/the_zorn_identity.html#c042422) which brings in Bourbaki-Witt. 

+-- {: .num_remark} 
###### Remark 
An alternative proof of Bourbaki-Witt would be along lines similar to those used to show AC implies Zorn's lemma. Given the inflationary function $s$, consider the function $f: Well(S) \to S$ which takes a well-ordered subset $W$ to $s(\sup W)$. If $s$ has no fixed points, then $f(W)$ will always be a strict upper bound of $W$, and from there one derives a contradiction exactly as in the proof of Zorn's lemma. 
=-- 

+-- {: .num_remark} 
###### Remark 
The Bourbaki-Witt theorem is an example of a fixed-point theorem. We should point out its kinship with the quite remarkable fixed-point theorem due to Pataraia, who observed that the conclusion of the Bourbaki-Witt theorem may be strengthened quite considerably, and proved constructively (!), if we change the hypothesis to say that $s$ is a monotone operator (preserves the order $\leq$) on an inhabited [[dcpo]]. See [[fixed point]] for a brief account, and this [blog post](https://topology.lmf.cnrs.fr/bourbaki-witt-and-dito-pataraia/) for some appreciative commentary. 
=-- 


## Well-ordered formulation

[[Terry Tao]]  [points out](https://terrytao.wordpress.com/2009/01/28/245b-notes-7-well-ordered-sets-ordinals-and-zorns-lemma-optional/) (Remark 14) that the proof of Zorn's Lemma uses only the well-ordered chains, allowing a weakened hypothesis.  This is most naturally stated in the context of [[quosets]] rather than [[posets]]:

+-- {: .num_defn #WellChainAndStrictUpperBound}
###### Definition

* Given a [[quasiordered set]] $(S, \lt)$, an element $x$ of $S$ is _[[maximal element|maximal]]_ if $x \lt y$ never holds.

* A _[[well-ordered set|well-ordered]] chain_ (or a _well-ordered subset_ or simply a _well-chain_) in $S$ is a [[subset]] $A \hookrightarrow S$ such that $\lt$ is a [[well order]] on $A$.  

* A _[[strict upper bound]]_ of a subset $A$ of $S$ is an element $x$ of $S$ such that $y \lt x$ whenever $y \in A$.  
=--

The change to *strict* upper bounds is natural in a quasiordered context; it makes no difference in the presence of excluded middle, since we wish to conclude that a maximal element exists; if there is no maximal element, then any set with an upper bound immediately gets a strict upper bound along with it.

+-- {: .num_defn #wellStatement}
###### Definition

The well-ordered __Zorn\'s Lemma__ states that any quasiordered set $S$ has a maximal element if every well-chain in $S$ has a strict upper bound, or more simply that it is not possible in a quasiordered set that every well-chain has a strict upper bound.  Or from another perspective, if every well-ordered subset of a quasiordered [[class]] $S$ has a strict upper bound, then $S$ is a [[proper class]].
=--

The &#8216;more simply&#8217; formulation is equivalent (even constructively) because, on the one hand, if $m$ is a maximal element, then ${m}$ is a well-chain with no strict upper bound, contradicting the hypothesis; while on the other hand, anything whatsoever is true of a nonexistent quoset $S$.  The &#8216;another perspective&#8217; is then immediate if by a &#8216;proper class&#8217; one simply means a class that is not a set.

Assuming excluded middle, this is (a priori) stronger than the usual Zorn's Lemma, since only well-ordered chains are required to have upper bounds.  (Of course, once all the proofs are in, they are both simply equivalent to the Axiom of Choice.)  In [[constructive mathematics]], however, it is not stronger, for two reasons: just because $S$ has no maximal element, that doesn't mean that every upper bound has a strict upper bound; and even if this could be fixed, we would only conclude that $S$ does [[not not]] have a maximal element.  However, I intend to argue that this version of Zorn's Lemma should be regarded as more constructively acceptable; some relativized versions are flat-out true.


## Usage/applications 

It is very common, when starting with a preordered set $S$, to apply Zorn\'s lemma not to $S$ itself but to an [[up-set]] (an [[under category]]) in $S$.  That is, one starts with an element $x$ of $S$ and proves the existence of a maximal element comparable to $x$.

Zorn\'s lemma may be used to prove all of the following:

* The [[Hausdorff maximal principle]]: Every chain in $S$ is contained in a maximal chain.
* The [[ultrafilter theorem]]: Every proper [[filter]] on a set may be extended to an [[ultrafilter]].
* The [[maximal ideal theorem]]: Every [[ideal]] in a [[ring]] may be extended to a [[maximal ideal]].
* The [[basis theorem]]: Every [[vector space]] (over a [[field]]) has a basis.
* etc ...

Some of these are equivalent to Zorn\'s lemma, while some are weaker; conversely, some additionally require excluded middle. 


## References 

Due Kuratowski and, independently later, Zorn:

* Casimir Kuratowski, _Une méthode d'élimination des nombres transfinis des raisonnements mathématiques_, Fundamenta Mathematicae __3__ (1922) 76--108 [doi](https://doi.org/10.4064/fm-3-1-76-108)
* Max Zorn, _A remark on method in transfinite algebra_, Bull. Amer. Math. Soc. __41__ (10): 667--670 (1935)[doi](https://doi.org/10.1090/S0002-9904-1935-06166-X)

* Serge Lang, _Algebra_ (third edition), Addison-Wesley 1993. 

* {#Osius} Gerhard Osius, _Categorical set theory: a characterization of the category of sets_, Jour. Pure Appl. Alg. 4 (1974), 79--119. doi:[10.1016/0022-4049(74)90032-2](https://doi.org/10.1016/0022-4049%2874%2990032-2) 

* {#Bauer} [[Andrej Bauer]], _On the Failure of Fixed-Point Theorems for Chain-complete Lattices in the Effective Topos_, Electronic Notes in Theoretical Computer Science, **249** (2009) 157--167, doi:[10.1016/j.entcs.2009.07.089](https://doi.org/10.1016/j.entcs.2009.07.089) _and_
Theoretical Computer Science, **430** (2012) 43--50, doi:[10.1016/j.tcs.2011.12.005](https://doi.org/10.1016/j.tcs.2011.12.005).
arXiv:[0911.0068](https://arxiv.org/abs/0911.0068).

* {#Bauer-Lumsdaine_13} [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], _On the Bourbaki-Witt Principle in Toposes_, Math. Proc. Cam. Phil. Soc. 155 (2013), no. 1, 87--99 doi:[10.1017/S0305004113000108](https://doi.org/10.1017/S0305004113000108), arXiv:[1201.0340](https://arxiv.org/abs/1201.0340).

* {#Kneser} Hellmuth Kneser, *Das Auswahlaxiom und das Lemma von Zorn*, Mathematische Zeitschrift, 96:62--63, 1967; available [here](http://resolver.sub.uni-goettingen.de/purl?PPN266833020_0096)

On Zorn's lemma and [[Boolean algebra]] in [[intuitionistic type theories]]:

* {#Bell} [[John Lane Bell]], *Zorn’s lemma and complete Boolean algebras in intuitionistic type theories*, The Journal of Symbolic Logic, 62(4):1265--1279, 1997 ([doi:10.2307/2275642](https://doi.org/10.2307/2275642))


[[!redirects Zorn lemma]]
[[!redirects Zorn's lemma]]
[[!redirects Zorn\'s lemma]]
[[!redirects Zorn's lemma]]
[[!redirects Zorn's Lemma]]
