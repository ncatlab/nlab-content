# Contents # 
* table of contents 
{:toc} 

## Idea 

In [[material set theory]], especially versions of set theory that accept the [[axiom of foundation]] that the membership relation $\in$ is an extensional (but not necessarily [[transitive relation|transitive]]) [[well-founded relation]], there is a picture of sets as forming a _cumulative hierarchy_, hierarchically ordered by a rank function valued in the ordinals. The idea is that on Day 0 the empty set is born; on Day $n+1$ is born the power set of Day $n$. On limit Days all the sets born earlier are collected together into a single set which is their union. The cumulative hierarchy picture amounts to the assertion that every set belongs to some set produced by this iterative procedure. 

## In ZFC 

Suppose $V$ is a [[model]] of [[ZFC]]. Recall that in the theory ZFC, a set $x$ is defined to be *transitive* if $b \in x$ implies $b \subset x$; this is the same as saying that if $a \in b \in x$ then $a \in x$. Note this doesn't mean that the relation $\in$ on the set consisting of $x$ and the elements of its transitive closure is itself [[transitive relation|transitive]]: the condition concerns only chains $a \in b \in c$ where $c = x$. However, if that relation *is* transitive, then it is transitive, and extensional (by the extensionality axiom), and well-founded (by the axiom of foundation), and hence a well-order according to the argument [here](/nlab/show/well-order#wellorders_are_linear). In this case, $x$ is by definition an [[ordinal number]] (in the sense of von Neumann). 

Letting $On(V)$ be the class of ordinals (= ordinal numbers), one may define with the help of the replacement axiom a function 

$$R: On(V) \to V$$ 

by transfinite induction as follows: $R(0) = 0$, while 

* $R(\alpha + 1) = P(R(\alpha))$ (where $P$ denotes power set), 

* $R(\beta) = \bigcup_{\alpha \lt \beta} R(\alpha)$ when $\beta$ is a limit ordinal. 

+-- {: .num_prop} 
###### Proposition 
Each of the $R(\alpha)$ is transitive, and $\alpha \leq \beta$ implies $R(\alpha) \subseteq R(\beta)$. 
=-- 

+-- {: .proof} 
###### Proof 
First, if $X$ is a transitive set, then so is $P(X)$. For suppose $A \in P(X)$. Then $A \subseteq X$, and so if $x \in A$, we have $x \in X$ and thus $x \subset X$ since $X$ is transitive, so that $x \in P(X)$. We have thus shown $A \subset P(X)$. 

That each $R(\alpha)$ is transitive now follows by an easy induction. 

And so $R(\alpha) \subset R(\alpha + 1) = P(R(\alpha))$ since $R(\alpha) \in P(R(\alpha))$, and now $\alpha \leq \beta \Rightarrow R(\alpha) \subseteq R(\beta)$ follows by an easy induction. 
=-- 

If $x \in R(\gamma)$, then there is a least $\beta$ such that $x \in R(\beta)$, and this $\beta$ must be a successor ordinal, $\beta = \alpha + 1$. We define the _rank_ of $x$ to be that $\alpha$. Thus 

* $\emptyset$ has rank $0$, 

* $1 \coloneqq \{\emptyset\}$ has rank $1$, 

* $\{1\}$ and $2 \coloneqq \{0, 1\}$ have rank $2$, 

and so on. Each ordinal $\alpha$ has rank $\alpha$. 

+-- {: .num_theorem} 
###### Theorem 
For every element $x$ of $V$, there is some $\alpha \in On(V)$ such that $x \in R(\alpha)$. Thus every set $x$ appears as an element somewhere within the cumulative hierarchy 

$$R(0) \subset R(1) \subset \ldots \subset R(\omega) \subset R(\omega + 1) \subset \ldots \subset R(\omega + \omega) \subset \ldots$$ 
=-- 

The proof is essentially that $\bigcup_{\alpha \in On(V)} R(\alpha)$ is an $\in$-[[well-founded relation|inductive set]] of $V$, and so must be all of $V$ since $(V, \in)$ is well-founded (by the axiom of foundation). Details may be found in any reasonable text on ZFC set theory, for example [Kunen](#Kunen). 

+-- {: .num_remark} 
###### Remark 
The notation $V$ so widely seen in set theory texts and articles is a kind of visual pun that refers to the cumulative hierarchy: one imagines the V as outlining an angle, with a horizontal cross-section of the space inside the angle at height $\alpha$ suggesting a set $R(\alpha)$, which expands as $\alpha$ increases; the ordinals $\alpha$ themselves may be pictured as vertebrae of a spine or line therein. All sets in the cumulative hierarchy lie somewhere within the V. 
=-- 

## In algebraic set theory 

The idea of the cumulative hierarchy is realized in [[algebraic set theory]] via the construction of an initial "ZF-algebra". In broad-brush terms, there is a general connection between well-foundedness and initial algebras, as in Paul Taylor's theory of recursion where an initial $T$-algebra (for a [[taut functor]] $T$) is seen as a [[well-founded coalgebra]] $(X, \theta: X \to T X)$ for which $\theta$ is an isomorphism (i.e., a maximal well-founded coalgebra). Algebraic set theory can be seen as exploiting this connection and working out the details in cases specific to operations on "small sets", eventually enabling one to get at the cumulative hierarchy *per se*, i.e., the universe of *well-founded sets* (as well as the universe of ordinals, etc.). 

This deserves to be discussed at length, but let us try to give a few hints for now. One starts with a [[pretopos]] $\mathcal{C}$ (whose objects are regarded as "classes") equipped with a suitable notion of "smallness": to say a map $f: E \to X$ in the pretopos is "small" means intuitively that all its [[fibers]] are "small" (i.e., sets). Thus one assumes some reasonable axioms on the class of small maps in $\mathcal{C}$, including the existence of a universal small map "$el$": $E \to U$, with the elements $u$ of $U$ naming small sets and the fiber over $u$ the actual (small) set of its elements. The smallness axioms allow one to construct a small-[[power set]] functor $P_s: \mathcal{C} \to \mathcal{C}$; intuitively this sends a class $C$ to the class of small subsets of $C$. This carries a [[monad]] structure whose algebras $(X, \sup: P_s X \to X)$ are "small-complete" posets in $\mathcal{C}$. 

To get at the actual cumulative hierarchy (with attendant global membership relation $\in$), one defines a *ZF-algebra* to be a small-complete poset $(V, \leq)$ in $\mathcal{C}$, equipped with a function $s: V \to V$ satisfying suitable conditions; here one is to think of $\leq$ as "inclusion" and $s(x)$ as a singleton $\{x\}$. The relation $x \in y$ can then be interpreted as $s(x) \leq y$. The initial object in the category of ZF-algebras then captures the desired universe of well-founded sets. 

+-- {: .num_remark} 
###### Remark 
The details of the construction of the initial ZF-algebra should be examined with attention to connections with Taylor's theory of well-founded coalgebras; for example, systematic use is made of bisimulations which has a general meaning in coalgebra theory. 
=-- 

This program, initiated by [[André Joyal]] and [[Ieke Moerdijk]], permits a fine-grained analysis of *intuitionistic* ZF-set theory and intuitionistic ordinals. The reader is referred to their [monograph](#JM) for details, and to the [Algebraic Set Theory](http://www.phil.cmu.edu/projects/ast/) page for further pointers to the literature. 


## Related entries

* [[constructible universe]]

* [[reflection principle]]

* [[algebraic set theory]] 

## References 

* Kenneth Kunen, _Set Theory: An Introduction to Independence Proofs_, Studies in Logic and the Foundations of Mathematics Vol. 102 (2006), Elsevier. 
 {#Kunen} 

* Andr&#233; Joyal and Ieke Moerdijk, _Algebraic Set Theory_, London Math. Soc. Lecture Series Notes 220 (1995), Cambridge University Press. 
 {#JM} 
