

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

_Zorn\'s lemma_ is a [[proposition]] in [[set theory]] and [[order theory]]. It says that: _A [[preorder]] in which every sub-[[total order]] has an [[upper bound]] has a [[maximal element]]._ 

Depending on the chosen perspective on [[foundations]]
this is either an [[axiom]] or a [[deduction|consequence]] of the [[axiom of choice]]; or neither if neither the axiom of choice nor Zorn's lemma is assumed as an axiom.
Conversely, Zorn\'s lemma and the [[axiom of excluded middle]] together imply the [[axiom of choice]].  Although it doesn\'t imply excluded middle itself, Zorn\'s lemma is not generally accepted in [[constructive mathematics]] as an [[axiom]].  

> (Say something about how one can systematically get around this in many situations ....)


In as far as it holds or is assumed to hold, Zorn's lemma is a standard method for constructing (or at least, [[proof|proving]] the [[existence]] of) objects that are 'maximal' in an appropriate sense.  It is commonly used in [[algebra]] and named after the algebraist [[Max Zorn]].



## Statement and proofs

+-- {: .num_defn }
###### Definition

* Given a [[preorder|preordered]] set $(S, \leq)$, an element $x$ of $S$ is _[[maximal element|maximal]]_ if $y \leq x$ whenever $x \leq y$.  

* A _[[chain]]_ in $S$ is a [[subset]] $A \hookrightarrow S$ such that $\leq$ is a [[total order]] on $A$.  

* An _[[upper bound]]_ of a subset $A$ of $S$ is an element $x$ of $S$ such that $y \leq x$ whenever $y \in A$.  
=--

+-- {: .num_defn}
###### Definition

The [[proposition]] __Zorn\'s Lemma__ states that each preordered set $S$ has a maximal element if every chain in $S$ has an upper bound.
=--

+-- {: .num_theorem #TheLemma}
###### Theorem

Suppose the [[axiom of choice]] holds. Then Zorn\'s Lemma holds.
=--

+-- {: .proof}
###### Proof
By contradiction. (A direct proof of the existence of a maximal element is not possible, so we freely use the [[axiom of excluded middle]], which in any case follows from AC, the axiom of choice. The one use made of AC is noted below.) 

Suppose $S$ has no maximal element. Then every chain $C \subseteq S$ has a *strict* upper bound: an element $x$ such that $c \lt x$ for all $c \in C$. (Take an upper bound $y$ of $C$, then $y$ is not maximal by supposition, so any $x$ with $y \lt x$ will serve.) For each $W \subseteq S$ that is well-ordered by $\leq$, use AC to choose a strict upper bound $f(W)$ of $W$. Given a such a function $f: Well(S) \to S$ from well-ordered subsets of $S$ to $S$, let us say $W \in Well(S)$ is *$f$-inductive* if for every $x \in W$, we have $x = f(\{y \in W: y \lt x\})$. 

Let $Y, Z \in Well(S)$ be $f$-inductive sets; we will show one is an initial segment of the other. Let $I$ be the maximal initial segment common to both ($I$ may be empty), and suppose for a contradiction that $I$ is properly contained in both; let $y$ be the least element of $Y \setminus I$, and $z$ the least element of $Z \setminus I$. Then $\{x \in Y: x \lt y\} = I = \{x' \in Z: x' \lt z\}$, so by $f$-inductivity of $Y, Z$, we have $y = f(I) = z$. Thus $I$ extends to initial segments $I \cup \{y\} = I \cup \{z\}$, contradicting maximality of $I$. Hence $I = Y$ or $I = Z$, making one of $Y, Z$ an initial segment of the other.  

So the collection of $f$-inductive sets is totally ordered by inclusion of initial segments, making their union $U$ the maximal $f$-inductive set. Appending its strict upper bound $f(U)$, the chain $U \cup \{f(U)\}$ is a larger $f$-inductive set, contradiction. The proof is complete. 
=--

+-- {: .num_remark }
###### Remark

The [[empty set]] is not an exception to Zorn\'s lemma, as the chain $\emptyset$ does not have an upper bound.
=-- 

+-- {: .num_remark} 
###### Remark 
The proof above (does anyone know where it appears in the literature?) can be seen as an application of general recursion theory &#224; la Paul Taylor's [[Practical Foundations of Mathematics|book]], which in turn follows Osius. In particular, initial segments are the same as $P$-coalgebra maps between [[well-founded coalgebras]], and the maximal $U$ constructed is a maximal attempt with respect to a partial algebra structure $f: P(S) \rightharpoonup S$, following Taylor's formulation of the recursion scheme. For a slightly different arrangement of the facts, one very commonly found in the literature, see the account of the Bourbaki-Witt theorem below. 
=-- 


+-- {: .num_theorem}
###### Theorem 

If Zorn\'s Lemma and the [[principle of excluded middle]] hold, then so do the [[well-ordering principle]] and the [[axiom of choice]].
=--

+-- {: .proof}
###### Proof

We first show that Zorn's lemma implies the classical [[well-ordering principle]]. The [[axiom of choice]] easily follows from the well-ordering principle. 

1. Let $A$ be a set, and consider the [[poset]] whose elements are pairs $(X, R)$, where $X \subseteq A$ and $R$ is a (classical) [[well-order]]ing on $X$, ordered by $(X, R) \leq (Y, S)$ if $X$ as a well-ordered set is an initial segment of $Y$. The hypothesis of Zorn's lemma is easily established: given a chain $(X_t, R_t)_{t \in T}$, put $X = \bigcup_t X_t$ and define the relation $R$ on $X$ by $x R y$ if $x R_t y$ for any (hence all) $X_t$ containing both $x, y$. Then $R$ is a well-ordering: if $U \subseteq X$ is any nonempty set, then $U \cap X_t$ is nonempty for some $t$, and the minimal element of $U$ with respect to $R$ will also be the minimal element of $U \cap X_t$ with respect to $R_t$ (crucially using here the initial segment condition). 

2. By Zorn's lemma, the poset above contains a maximal element $(X, R)$, where $X \subseteq A$. We claim $X = A$; suppose not (here is where we need [[excluded middle]]), and let $x$ be a member of the complement $\neg X$. Well-order $X \cup \{x\}$, extending $R$ by deeming $x$ to be the final element. This shows $(X, R)$ was not maximal, contradiction. Hence any set $A$ may be well-ordered. 

3. The [[axiom of choice]] follows: suppose given a [[surjection]] $p: E \to B$, so that every [[fiber]] $p^{-1}(b)$ is [[inhabited set|inhabited]]. Consider any well-ordering of $E$, and define $s: B \to E$ by letting $s(b)$ be the least element in $p^{-1}(b)$ with respect to the well-ordering. This gives a section $s$ of $p$. 
=--

### Bourbaki-Witt theorem 

Many accounts of the proof of Zorn's lemma start by establishing first the so-called Bourbaki-Witt theorem, which does not require AC and is of interest in its own right. (However, it too does not admit a constructive proof; see Bauer-Lumsdaine for a demonstration that it is not valid in the [[effective topos]]. That said, the issue is subtle enough that the Bourbaki-Witt theorem nonetheless holds in any [[Grothendieck topos]].) 

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
the elements of $M$ are $0, f(0), f f(0), \ldots f^n(0), \ldots$, where we may continue by transfinite induction: at limit ordinals $\alpha$ define $f^\alpha(0)$ to be the sup of $\{f^\beta(0): \beta \lt \alpha\}$, and at successors define $f^{\alpha + 1}(0) = f(f^\alpha(0))$. We cannot have a strictly increasing chain that goes on forever, by cardinality considerations, so at some point we hit an $\alpha$ such that $f^{\alpha + 1}(0) = f^\alpha(0)$, which provides a fixed point. (What could be nonconstructive about that? See this [comment](https://golem.ph.utexas.edu/category/2012/10/the_zorn_identity.html#c042428) by Lumsdaine.) In any case, once we prove $M$ is totally ordered, our fixed point will be the sup of $M$. 

=-- 

## Usage/applications 

It is very common, when starting with a preordered set $S$, to apply Zorn\'s lemma not to $S$ itself but to an [[up-set]] (an [[under category]]) in $S$.  That is, one starts with an element $x$ of $S$ and proves the existence of a maximal element comparable to $x$.

Zorn\'s lemma may be used to prove all of the following:

* The [[Hausdorff maximal principle]]: Every chain in $S$ is contained in a maximal chain.
* The [[ultrafilter theorem]]: Every proper [[filter]] on a set may be extended to an [[ultrafilter]].
* The [[maximal ideal theorem]]: Every [[ideal]] in a [[ring]] may be extended to a [[maximal ideal]].
* The [[basis theorem]]: Every [[vector space]] (over a [[field]]) has a basis.
* etc ...

Some of these are equivalent to Zorn\'s lemma, while some are weaker; conversely, some additionally require excluded middle.


[[!redirects Zorn lemma]]
[[!redirects Zorn's lemma]]
[[!redirects Zorn\'s lemma]]
[[!redirects Zorn's lemma]]
[[!redirects Zorn's Lemma]]
