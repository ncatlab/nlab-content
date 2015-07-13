# Contents # 
* table of contents 
{:toc}

## Idea 

Engeler's lemma is one of a number of set-theoretic propositions connected with [[axiom of choice|choice principles]] and [[prime ideal theorem|prime ideal]]/[[maximal ideal theorem|maximal ideal]] theorems. A key phrase for such set-theoretic propositions is "systems of finite character"; related results include the [[Teichmüller-Tukey lemma]]. 

## Statement and proof 

+-- {: .num_theorem} 
###### Theorem 
**(Engeler's lemma)** 
Let $X$ be a [[set]], and let $F$ be a collection of [[partial functions]] $f: X \rightharpoonup 2 = \{0, 1\}$: 

$$X \hookleftarrow A \stackrel{f}{\to} 2$$ 

where $A = \dom(f)$ is the [[domain]] of $f$. Suppose the following 3 conditions are satisfied: 

1. For every $f: \dom(f) \to 2$ in $F$ and finite subset $S \subseteq \dom(f)$, the restriction $Res_S(f): S \to 2$ belongs to $F$; 

2. If $f: X \rightharpoonup 2$ is any partial function such that $Res_S(f)$ belongs to $F$ for every [[finite set|finite]] subset $S \subseteq \dom(f)$, then $f$ belongs to $F$; 

3. Every finite subset $S \subseteq X$ is the domain of some $f \in F$. 

Then, assuming the [[ultrafilter theorem|ultrafilter principle]] (UP), there exists a [[total function]] $f \in F$. 
=-- 

+-- {: .proof} 
###### Proof 
We abuse notation by identifying partial functions $f: X \rightharpoonup \{0, 1\}$ with total functions $X \to 3 = \{0, 1, 2\}$, defining $\dom(f)$ for $f: X \to 3$ in terms of the corresponding partial function: $\dom(f) = \{x \in X: f(x) \neq 2\}$. For $f: X \to 3$, the notation $Res_S(f)$ means we regard $f$ as a partial function, obtain another partial function by restriction, and consider this a function $X \to 3$. 

Thus $F$ defines a subspace $F \subseteq 3^X$. Under [[Tychonoff theorem|UP]], the [[product]] space $3^X$ is [[compact Hausdorff space|compact Hausdorff]]. We claim $F$ is [[closed subset|closed]]. For suppose $f: X \to 3$ is in the closure of $F$. This means that for any finite $A \subseteq X$ there exists $g \in F$ with $f|_A = g|_A$. In particular, for any finite $B \subseteq \dom(f)$ there exists $g \in F$ such that $f|_B = g|_B$. In particular $g(x) \neq 2$ for all $x \in B$, so $B \subseteq \dom(g)$, and so $Res_B(f) = Res_B(g)$ belongs to $F$ by condition 1. Since $Res_B(f)$ belongs to $F$ for all finite $B \subseteq \dom(f)$, we have that $f \in F$ by condition 2. Thus $F$ is closed, and therefore compact. 

Now we claim that the set $T = \{f \in F: \forall_{x \in X} f(x) \neq 2\}$ is [[inhabited set|inhabited]], which in the partial function interpretation means $F$ contains a total function. For, the family of closed sets $C_x = F \cap \{f \in 3^X: f(x) \neq 2\}$ satisfies the finite intersection property, by condition 3. Thus $T = \bigcap_{x \in X} C_x$ is inhabited by compactness of $F$. 
=-- 

## References 

* Marcel Ern&#233;, _Prime Ideal Theorems and systems of finite character_, Commentationes Mathematicae Universitatis Carolinae, Vol. 38, No. 3 (1997), 513-536. ([web](http://dml.cz/dmlcz/118949)) 