# Contents #
* table of contents 
{: toc}

## Idea 

The concept of *matroid*, due to Hassler Whitney, is fundamental to combinatorics, giving several different ways of encoding/defining and presenting a general notion of "independence", e.g., linear independence in a vector space, algebraic independence in a field extension, etc. 

There is also a similar concept of an [[oriented matroid]]; every oriented matroid has an underlying matroid. 

## Definitions 

+-- {: .num_defn} 
###### Definition 
A **matroid** on a set $X$ is a [[Moore closure|closure operator]] $\mathbf{C}: P(X) \to P(X)$ satisfying the _exchange axiom_: if $a \in \mathbf{C}(S \cup\{b\}) \cap \neg \mathbf{C}(S)$, then $b \in \mathbf{C}(S \cup\{a\}) \cap \neg \mathbf{C}(S)$. 
=-- 

Usually when combinatorialists speak of matroids as such, $X$ is taken to be a finite set. A typical example is $X$ some finite subset of a vector space $V$, taking $\mathbf{C}(S) \coloneqq X \cap Span(S)$ for any $S \subseteq X$. 

Under this definition, a subset $S \subseteq X$ is _independent_ if there is a strict inclusion $\mathbf{C}(T) \subset \mathbf{C}(S)$ for every strict inclusion $T \subset S$ (this is the same as requiring $x \notin \mathbf{C}(S\backslash \{x\})$ for every $x \in S$). Again under this definition, $S$ is a _basis_ if $\mathbf{C}(S) = X$ and $S$ is independent. A _hyperplane_ is a closed subset $S$ (meaning $\mathbf{C}(S) = S$) that is maximal among proper closed subsets of $X$. It is possible to axiomatize the notion of matroid by taking bases as the primitive notion, or independent sets as the primitive notion, or hyperplanes as the primitive notion, etc. -- Rota (after Birkhoff) speaks of _cryptomorphism_ between these differing definitions. Much of the power and utility of matroid theory comes from this multiplicity of definitions and the possibility of moving seamlessly between them; for example, a matroid structure might be easy to detect from the viewpoint of one definition, but not from another. 

+-- {: .num_proposition} 
###### Proposition 
Any two bases of a finite matroid $X$ have the same cardinality, the _dimension_ of the matroid. 
=-- 

+-- {: .proof} 
###### Proof 
First, suppose $A$ is an independent set and $B$ is a basis, and suppose there are subsets $A_0 \subseteq A, B_0 \subseteq B$ such that $A_0 \cup B_0$ is a basis. We claim that for each $a \in A \backslash A_0$, there exists $b \in B_0$ such that $A_0 \cup \{a\} \cup (B_0 \backslash \{b\})$ is a basis. For, let $C \subseteq B_0$ be of minimum cardinality such that $a \in \mathbf{C}(A_0 \cup C)$; we know $C$ must be inhabited since $a \notin \mathbf{C}(A \backslash \{a\}) \supseteq \mathbf{C}(A_0)$; clearly $C \cap A_0 = \emptyset$. So let $b$ be an element of $C$. Since by minimality of $C$ we have  

$$a \in \mathbf{C}(A_0 \cup (C \backslash \{b\}) \cup \{b\}) \cap \neg \mathbf{C}(A_0 \cup (C \backslash \{b\})),$$ 

it follows from the exchange axiom that $b \in \mathbf{C}(A_0 \cup (C \backslash \{b\}) \cup \{a\})$. Thus $b \in \mathbf{C}(A_0 \cup (B_0 \backslash \{b\}) \cup \{a\})$, whence 

$$\mathbf{C}(A_0 \cup (B_0 \backslash \{b\}) \cup \{a\}) = \mathbf{C}(A_0 \cup B_0 \cup \{a\}) = X$$ 

so that $D \coloneqq A_0 \cup (B_0 \backslash \{b\}) \cup \{a\}$ "spans" $X$. Also $D$ is independent: if $x \in D$ and $x \neq a$, then 

$$\mathbf{C}(D \backslash \{x\}) \subseteq \mathbf{C}((A_0 \cup B_0) \backslash \{x\})$$ 

with neither side containing $x$ since $A_0 \cup B_0$ is independent; whereas if $x = a$ and supposing to the contrary that $a \in \mathbf{C}(D \backslash \{a\}) = \mathbf{C}((A_0 \cup (B_0 \backslash \{b\}))$, we conclude $A_0 \cup (B \backslash \{b\})$ has the same span as $D$. Since $D$ already spans, $b \in \mathbf{C}(A_0 \cup (B_0 \backslash \{b\}))$, again impossible since $A_0 \cup B_0$ is independent. This proves the claim. 

Again assuming $A$ independent and $B$ a basis, now we show that $card(A) \leq card(B)$, which will finish the proof. Let $n = card(B)$, and suppose on the contrary that there are distinct elements $a_1, \ldots, a_{n+1} \in A$. Set $A_0 = \emptyset$ and $B_0 = B$. Applying the claim above inductively, we have that $\{a_1, \ldots, a_i\} \cup (B \backslash \{b_1, \ldots, b_i\})$ is a basis for $1 \leq i \leq n$, so in particular $\{a_1, \ldots, a_n\}$ spans $X$. Hence $a_{n+1} \in \mathbf{C}(\{a_1, \ldots, a_{n}\})$, contradicting the independence of $A$. 
=-- 

## Examples 

Vector spaces, algebraic closures, graphs, restrictions, localizations, ... 

## Model-theoretic geometry 

Essentially the very same notion arises in model theory, except instead of being called a matroid it is called a "geometry". It arises in the study of geometry of strongly minimal sets, with applications to stability theory (i.e., Shelah's classification theory). 

+-- {: .num_defn} 
###### Definition 
A _pregeometry_ is a (possibly infinite) matroid (given by a set $X$ equipped with a closure operator $C$) such that for all $S \subseteq X$, if $x \in C(S)$ then $x \in C(S_0)$ for some finite subset $S_0 \subseteq S$. A **geometry** is a pregeometry such that $C(\emptyset) = \emptyset$ and $C(\{x\}) = \{x\}$ for every $x \in X$. 
=-- 

The language of independence, spanning, and basis carry over as before. A maximal independent set spans (i.e., is a basis), and maximal independent sets exist according to [[axiom of choice|Zorn's lemma]]. Again we have a notion of dimension by the following proposition. 

+-- {: .num_proposition} 
###### Proposition 
In a pregeometry, any two maximal independent sets have the same cardinality. 
=-- 

+-- {: .proof} 
###### Proof 

=-- 


## Combinatorial optimization 


## Mnev's theorem 

Mn&#235;v's universality theorem says that any [[semialgebraic set]] in $\mathbb{R}^n$ defined over integers is stably equivalent to the realization space of some oriented matroid.

* wikipedia [matroid](http://en.wikipedia.org/wiki/Matroid), [Mn&#235;v's universality theorem](http://en.wikipedia.org/wiki/Mnev%27s_universality_theorem), [oriented matroid](http://en.wikipedia.org/wiki/Oriented_matroid)
* Hassler Whitney, _On the abstract properties of linear dependence_, American Journal of Mathematics (The Johns Hopkins University Press) 57 (3): 509&#8211;533, 1935, [jstor](http://jstor.org/stable/2371182), [MR1507091](http://www.ams.org/mathscinet-getitem?mr=1507091)
* J. Oxley, _What is a matroid_, [pdf](http://www.math.lsu.edu/~oxley/survey4.pdf)
* James G. Oxley, _Matroid theory_, Oxford Grad. Texts in Math. 1992, 2010
* some papers on Coxeter matroids [html](http://www.math.ufl.edu/~white/cox.html)
* MathOverflow question [Mn&#235;v's universality corollaries, quantitative versions](http://mathoverflow.net/questions/72154/mnevs-universality-corollaries-quantitative-versions) 
* Eric Katz, Sam Payne, _Realization space for [[tropical geometry|tropical]] fans_, [pdf](http://users.math.yale.edu/~sp547/pdf/Realization-spaces.pdf)
* Nikolai E. Mnev, _The universality theorems on the classification problem of configuration varieties and convex polytopes varieties_, pp. 527-543, in "Topology and geometry: Rohlin Seminar." Edited by O. Ya. Viro. Lecture Notes in Mathematics, __1346__, Springer 1988; _A lecture on universality theorem_ (in Russian) [pdf](http://club.pdmi.ras.ru/~panina/9.pdf)
* Talal Ali Al-Hawary, _Free objects in the category of geometries_, [pdf](http://www.emis.de/journals/HOA/IJMMS/Volume26_12/770.pdf)
* Talal Ali Al-Hawary, D. George McRae, _Toward an elementary axiomatic theory of the category of LP-matroids_, Applied Categorical Structures __11__: 157&#8211;169, 2003, [doi](http://dx.doi.org/10.1023/A:1023557229668)
* Hirokazu Nishimura, Susumu Kuroda, _A lost mathematician, Takeo Nakasawa: the forgotten father of matroid theory_ 1996, 2009
* William H. Cunningham, _Matching, matroids, and extensions_, Math. Program., Ser. B __91__: 515&#8211;542 (2002) [doi](http://dx.doi.org/10.1007/s101070100256)
* L. Lov&#225;sz, _Matroid matching and some applications_, J. Combinatorial Theory B __28__, 208&#8211;236 (1980)
* A. Bj&#246;rner, M. Las Vergnas, B. Sturmfels, N. White, G.M. Ziegler,  _Oriented matroids_, Cambridge Univ. Press 1993, 2000, [view at reslib.com](http://reslib.com/book/Oriented_Matroids)
[[!redirects matroids]]