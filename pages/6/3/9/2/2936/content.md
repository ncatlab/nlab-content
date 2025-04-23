
# Contents
* table of contents 
{: toc}

## Introduction 

A **Polish space** is a [[topological space]] that's [[homeomorphism|homeomorphic]] to a [[separable space|separable]] [[complete space|complete]] [[metric space]]. Every [[second countable space|second countable]] [[locally compact space|locally compact]] [[Hausdorff space]] is a Polish space, among others.

Polish spaces, or the [[measurable spaces]] that they define ([[standard Borel spaces]]) provide a useful framework for doing [[measure theory]].  As with any topological space, we can take a Polish space and regard it as a [[measurable space]] with its [[sigma-algebra]] of [[Borel set]]s.  Then, there is a very nice classification of Polish spaces up to measurable bijection: there is one for each [[countable set|countable]] [[cardinality]], one whose cardinality is that of the [[continuum]], and no others.

Why are Polish spaces 'not very big'?  In other words, why are there none with cardinality exceeding the continuum?  As with any separable metric space, it's because any Polish space has a countable dense subset and you can write any point as a limit of a sequence of points in this subset.  So, you only need a [[sequence]] of integers to specify any point in a Polish space. More sharply, see Lemma \ref{baire} below. 

+-- {: .num_example} 
###### Example 
The primordial example (and in practice, one of the most convenient) is [[set-theoretic Baire space|Baire space]] $B$, viz. the space of irrational real numbers between $0$ and $1$, with the [[subspace topology]] inherited from the [[real number|real line]]. This is obviously not complete with respect to the metric induced from the real line, but it is homeomorphic to the product space $\mathbb{N}^\mathbb{N}$ via regular [[continued fraction]] expansions, and the latter is metrizable by a complete metric where the distance between two sequences $a = (a_1, a_2, \ldots)$ and $b = (b_1, b_2, \ldots)$ of positive integers is given by the formula $d(a, b) = 1/2^n$ where $n$ is the least integer such that $a_n \neq b_n$. A countable dense subset is given by continued fractions that eventually repeat (quadratic surds). 
=-- 

The convenience of Baire space is attested to by the fact that in [[descriptive set theory]], a "real number" is often taken to mean just a point of Baire space. See also Theorem \ref{Borel} below. 

## Properties 

Much of the material here is adapted from [Marker](#Marker), who in turn cites the text by [Kechris](#Kechris) as a main source. 

* A countable product $X = \prod_n X_n$ of Polish spaces is Polish. Indeed, each $X_n$ is metrizable by a complete metric $d_n$ that takes values in $[0, 1]$, and then we may define another such complete metric on $X$ by 
$$d(f, g) = \sum_n \frac1{2^{n+1}} d_n(f(n), g(n)).$$ 
The metric topology on $X$ coincides with the product topology. 

In particular, the [[Hilbert cube]] $[0, 1]^\mathbb{N}$ is Polish. 

* A subspace of a Polish space $X$ is Polish iff it is a [[G-delta set]] of $X$. See [Marker](#Marker), Theorem 1.33. 

* If $X, Y$ are Polish and $X$ is locally compact, then the [[exponentiable space|exponential]] $Y^X$ (the space of continuous maps with the [[compact-open topology]]) is also Polish.  See A.10 of [Kerr and Li](#KerrLi2016).

### "Universal" Polish spaces 

+-- {: .num_prop #hilbert} 
###### Proposition 
Any Polish space is homeomorphic to a subspace of the Hilbert cube. 
=-- 

In fact, this is true of any [[separable space|separable metrizable space]]. Note that mere separability does not suffice, as there are separable spaces that are not first-countable, such as the Stone-&#268;ech compactification of $\N$, and hence cannot be subspaces of any metrizable space. What distinguishes Polish spaces is that they are, up to homeomorphism, precisely the _$G_\delta$ subsets_ of the Hilbert cube. 

+-- {: .num_lemma #baire} 
###### Lemma 
Every [[inhabited]] Polish space $X$ admits a continuous surjection from Baire space. 
=-- 

+-- {: .proof} 
###### Proof (sketch) 
Construct by induction a collection of closed sets (balls) $C_s$ indexed over _finite_ sequences $s$ of positive integers, with the following properties: 

* For the empty sequence $e$, $C_e = X$; 

* For nonempty sequences $s$, $diam(C_s) \leq 1/n$ where $n = length(s)$; 

* Letting $(s, k)$ denote the extension of $s$ obtained by appending to $s$ the final element $k$, 
$$C_s = \bigcup_{k=0}^\infty C_{(s, k)};$$ 

* If $t$ extends $s$, then $center(C_t) \in C_s$. 

Then define $f: B \to X$ where for each infinite sequence $a \in \mathbb{N}^\mathbb{N}$, 

$$f(a) = \bigcap \{C_s: a\; extends\; s\}.$$ 

One may check that $f$ is continuous and surjective. 
=-- 

### Cantor-Bendixson rank 

Let $C \subseteq X$ be a closed subset of a Polish space $X$. The following operation traces back to Cantor's work in Fourier analysis, which in turn led to his study of [[countable ordinal|countable ordinals]] and [[ordinal]] analysis. 

For a subset $A \subseteq X$, recall that $x \in A$ is a [[limit point]] if $x \in Cl(A \setminus \{x\})$. A point $x \in A$ that is not a limit point of $A$ is called an _isolated point_ of $A$. Clearly each isolated point is open relative to $A$, as is therefore the set of isolated points. 

+-- {: .num_defn} 
###### Definition 
The **Cantor-Bendixson derivative** of $C$ is the set $C' \subseteq C$ of limit points relative to $C$. For each ordinal $\alpha$ the iterated derivative $C^\alpha$ is defined by recursion: $C^0 = C$, $C^{\alpha + 1} = (C^\alpha)'$, and $C^\alpha = \bigcap_{\beta \lt \alpha} C^\beta$ if $\alpha$ is a limit ordinal. 
=-- 

Since $\beta \lt \alpha$ implies $C^\beta \supseteq C^\alpha$, it is clear that there is a least ordinal $\alpha$ for which $C^\alpha = C^{\alpha + 1}$. This ordinal is called the _Cantor-Bendixson rank_ of $C$. A _[[perfect set]]_ is a closed set $C$ such that $C = C'$. (Some people insist that a perfect set also be nonempty; we do not.) 

+-- {: .num_prop #cantor} 
###### Proposition 
For each nonempty perfect set $P$ in a Polish space $X$, there is a continuous injection $i: \mathbf{2}^\mathbb{N} \to P$ from [[Cantor space]]. In particular, the cardinality of $P$ is the [[continuum]] $c$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $T$ be the complete infinite binary tree, whose infinite paths from the root correspond to points in Cantor space $\mathbf{2}^\mathbb{N}$. To each node $s$ in $T$ (a finite sequence of $0$'s and $1$'s) we construct by induction an open set $U_s$ with the following properties: 

* $U_e = X$ for the empty sequence $e$, 

* $\widebar{U_t} \subseteq U_s$ if $s$ is an initial segment of $t$, 

* For the two children $(s, 0)$ and $(s, 1)$ of $s$, the sets $U_{(s, 0)}$ and $U_{(s, 1)}$ are disjoint, 

* $diam(U_s) \leq 1/n$ where $n$ is the length of (nonempty) $s$, 

* $U_s \cap P \neq \emptyset$ for each $s$. 

Indeed, if $U_s$ has been constructed, and given $x \in U_s \cap P$, there are (at least!) two points $x_0, x_1 \in U_s \cap P$ since $P$ is perfect. We can easily find disjoint neighborhoods $U_{(s, 0)}, U_{(s, 1)}$ of these points respectively with the required properties. 

Then for each path $p = (a_0, a_1, \ldots) \in \mathbf{2}^\mathbb{N}$, define 

$$i(p) = \bigcap_{s \preceq p} U_s$$ 

where $s \preceq p$ means $s$ is an initial segment of $p$. The intersection consists of a single point because it equals the intersection of a decreasing chain of closed sets with shrinking diameter (thus closing in on a limit of a [[Cauchy sequence]]). The map $i$ is clearly injective by the disjointness of open sets of children, and it is easy to see $i$ is continuous. 
=-- 


+-- {: .num_theorem} 
###### Theorem 
For $C$ a closed subset of a Polish space $X$, the Cantor-Bendixson rank is a countable ordinal $\alpha$. The complement $C \setminus C^\alpha$ is at most countable.  
=-- 

+-- {: .proof} 
###### Proof 
Let $U_i$ be a countable basis of $X$. For each $\beta \lt \alpha$, each point $x \in C^\beta \setminus C^{\beta + 1}$ is an isolated point, so we can find an $U_{i(x)}$ in the basis such that $U_{i(x)} \cap (C^\beta \setminus C^{\beta + 1}) = \{x\}$. It is then clear that $x \mapsto i(x)$ is injective, so each $C^\beta \setminus C^{\beta + 1}$ is countable. Similarly, whenever $C^\beta \setminus C^{\beta + 1}$ is nonempty, we can find a basis element $U_{j(\beta)}$ that isolates one of its points (say $x$), and this same $U_j$ cannot isolate any point of an earlier $C^\gamma \setminus C^{\gamma + 1}$ since $x$ is a limit point of $C^\gamma$. It follows that $\beta \mapsto j(\beta)$ is an injective map, so that $\alpha$ must be a countable ordinal, and the collection $F \coloneqq C \setminus C^\alpha = \bigcup_{\beta \lt \alpha} C^\beta \setminus C^{\beta + 1}$ is (at most) countable. 
=-- 

+-- {: .num_cor #CH} 
###### Corollary 
A closed set in a Polish space is the disjoint union $P \cup F$ of a perfect set $P$ and a finite or countable set $F$. Hence an infinite closed subset in a Polish space has cardinality either $\aleph_0$ or the continuum $c = 2^{\aleph_0}$ ([[continuum hypothesis]] for closed sets). 
=-- 

### Borel isomorphism between Polish spaces 

Recall that a function $f: X \to Y$ between topological spaces is _Borel_ if $f^{-1}(V)$ is a Borel set in $X$ for every open $V$ in $Y$. Topological spaces and Borel functions form a category. 

+-- {: .num_lemma} 
###### Lemma 
If $A, B$ are countably infinite $T_1$-[[separation axiom|spaces]], then any bijection $f: A \to B$ is a Borel isomorphism. 
=-- 

For, the inverse image $f^{-1}(U)$ of an open set, being countable, is an $F_\sigma$ set. In particular, any two denumerable Polish spaces are Borel isomorphic. 

+-- {: .num_lemma} 
###### Lemma 
The unit interval $[0, 1]$ and Cantor space $2^\mathbb{N}$ are Borel isomorphic. 
=-- 

+-- {: .proof} 
###### Proof 
Let $E \subseteq \mathbf{2}^\mathbb{N}$ be the set of $(0, 1)$-sequences that are eventually constant. Then 

$$f(a_1, a_2, \ldots) = \sum_n \frac{a_n}{2^n}$$ 

maps $2^\mathbb{N} \setminus E$ homeomorphically onto the space of non-(dyadic rational) numbers in $[0, 1]$. Pick any bijection $g: E \to \{dyadic\; rationals\}$. Then the union of $f$ and $g$ defines a Borel isomorphism $h: \mathbf{2}^\mathbb{N} \to [0, 1]$. 
=-- 

+-- {: .num_prop #subset} 
###### Proposition 
Any Polish space $X$ is Borel isomorphic to a Borel subset of Cantor space. 
=-- 

+-- {: .proof} 
###### Proof 
There is a sequence of maps 

$$X \hookrightarrow [0, 1]^\mathbb{N} \stackrel{h^\mathbb{N}}{\to} (\mathbf{2}^{\mathbb{N}})^\mathbb{N} \stackrel{j}{\to} \mathbf{2}^\mathbb{N}$$ 

where the first map is an inclusion of a $G_\delta$ set, the second is induced from a Borel isomorphism $h$, and the third is a homeomorphism. 
=-- 

+-- {: .num_theorem #Borel} 
###### Theorem 
Any two Polish spaces of the same cardinality are Borel isomorphic. 
=-- 

+-- {: .proof} 
###### Proof 
It suffices to prove this for uncountable Polish spaces (which have continuum cardinality, as we saw in Corollary \ref{CH}). We show that any such $X$ is Borel isomorphic to Cantor space. By Proposition \ref{subset}, we have an inclusion $i: X \to \mathbf{2}^{\mathbb{N}}$ that maps $X$ Borel isomorphically onto its image, and by Proposition \ref{cantor}, we have an inclusion $j: \mathbf{2}^{\mathbb{N}} \to X$ that maps Cantor space Borel isomorphically (even homeomorphically) onto its image. The rest is just a matter of checking that at least one of the proofs of the [[Cantor-Schroeder-Bernstein theorem]] applies to this Borel context. 

Indeed, as explained [here](https://ncatlab.org/nlab/show/Cantor-Schroeder-Bernstein+theorem#alt), we may consider 

$$S = \bigcap_{n \geq 0} (\neg \exists_j \neg \exists_i)^n(X)$$ 

Each of the direct image maps $\exists_i$ and $\exists_j$ takes Borel sets to Borel sets, since their inverses $i^{-1}, j^{-1}$ are Borel functions on their domains. So each of the iterates $(\neg \exists_j \neg \exists_i)^n(X)$ is a Borel set and so is their countable intersection $S$. The set $S$ is a fixed point of $\neg \exists_j \neg \exists_i$ and so we construct a Borel isomorphism $h: X \to \mathbf{2}^{\mathbb{N}}$ as 

$$\array{
x & \mapsto & i(x) & if\; x \in S \\ 
 & \mapsto & j^{-1}(x) & if\; x \in \neg S
}$$ 

following the proof of the [[Cantor-Schroeder-Bernstein theorem]]. 
=-- 

For another proof, see theorem 3.1.1 of [Berberian](#Ber). 


## Further examples 

* The classical $L^p$-[[Lebesgue space|spaces]] for $p \lt \infty$ are Polish spaces. 

* For a metric space $X$, let $K(X)$ be the set of nonempty [[compact space|compact]] subsets of $X$, equipped with the [[Hausdorff metric]]. If $X$ is a separable complete metric space, then so is $K(X)$. 

* A [[local compactum|locally compact Hausdorff space]] is Polish iff it is second-countable. 
 
* If $X$ is Polish, then the space $P(X)$ of Borel probability measures $\mu$ equipped with the Prokhorov metric is also Polish. Definitions: for $x \in X$ and $A \subset X$ nonempty, put $d(x, A) = \inf \{d(x, a): a \in A\}$, and for $\alpha \gt 0$ define $A_\alpha = \{x \in X: d(x, A) \lt \alpha\}$ and $\emptyset_\alpha = \emptyset$. Define the *Prokhorov metric* $d_P$ by 
$$d_P(\mu, \nu) = \inf \{\alpha \gt 0: \forall_{Borel\; A} \mu(A) \lt \nu(A_\alpha) + \alpha \; and \; \nu(A) \lt \mu(A_\alpha) + \alpha\}.$$ 
Then the map $u_X: X \to P(X)$ sending $x$ to the [[Dirac measure]] $\delta_x$ is continuous. If $x_n$ is a countable dense set of $X$, then the set of rational convex combinations $\sum_{i=1}^n q_n \delta_{x_n}$ (with $0 \leq q_n \leq 1$ and $\sum_i q_i = 1$) is a countable dense subset of $P(X)$. More at [[Giry monad]]. 

* Spaces of [[structure in model theory|structures]] and [[models]] (in the [[model theory]] sense), and spaces of $n$-[[n-type (model theory)|types]] (again in the model theory sense), quite often provide examples of Polish spaces. For example, if $L$ is a countable language (a countable [[signature (in logic)|signature]]), then the collection of possible $L$-structures $M$ on the countable universe $\mathbb{N}$, topologized by taking as basic opens 
$$U_\phi = \{M \in Struct(L): M \models \phi\}$$ 
where $\phi$ is a quantifier-free sentence, is a Polish space homeomorphic to the product space 
$$\prod_{relations\; R} \mathbf{2}^{\mathbb{N}^{arity(R)}} \times \prod_{functions\; f} \mathbb{N}^{\mathbb{N}^{arity(f)}}$$ 
(taking constants to be functions of arity $0$ in the signature). 

As an example of the last principle, we have a kind of continuum hypothesis for substructures: 

+-- {: .num_prop} 
###### Proposition 
Let $X$ be a countable structure of a language; then the number of substructures of $X$ is either countable or the continuum. 
=-- 

+-- {: .proof} 
###### Proof 
A subset of $X$ is specified by its [[characteristic function]] $\chi \in 2^X$, where $2^X$ is regarded as a Polish space. In order for the subset *not* to support a substructure, then must be some function symbol $f$ of the language, say of arity $n$, and elements $a_1, \ldots, a_n$ such that $\chi(a_i) = 1$ for all $i$ and $\chi(f_X(a_1, \ldots, a_n)) = 0$. The basic open 

$$U_{f; a_1, \ldots, a_n} \coloneqq \{\omega \in 2^X: \; \omega(a_1) = 1, \ldots, \omega(a_n) = 1, \; \omega(f_X(a_1, \ldots, a_n)) = 0\}$$ 

would thus contain $\chi$ and also exclude any substructure; we conclude that the collection of substructures forms a closed subset $C$ of $2^X$. Then the Cantor-Bendixson theorem (i.e., Corollary \ref{CH}) shows that ${|C|}$ is either countable or the continuum. 
=-- 

## Polish spaces of mappings ##

In his study of wild knots, [Kulnikov](#Kulnikov) studied the space of [[embeddings]] of $S^1$ in $S^3$, and implicit in his work, though perhaps not explicitly proved, is the fact that this space is a Polish space.  More generally, we can show that the space of embeddings of a compact Polish space $X$ in a Polish space $Y$ is again a Polish space. For this we first give the space $Y^X$ the metric 

$$ d(f,g) = \sup_{x \in X} d(f(x),g(x))  $$

where the supremum is well-defined because $X$ is compact.  The topology coming from this metric is called the ''uniform topology''.

+-- {: .num_prop} 
###### Proposition
If $X$ is a compact Polish space and $Y$ is a Polish space, then $Y^X$ with the above metric is a Polish space, and its uniform topology is the compact-open topology.
=-- 

+-- {: .proof} 
###### Proof 
Given any compact metric space $X$ and metric space $Y$, the uniform topology on $Y^X$ agrees with the compact-open topology.  If $X$ is any locally compact Polish space and $Y$ is a Polish space, $Y^X$ with its compact-open topology is a Polish space, by A.10 of [Kerr and Li](#KerrLi2016).
=--

We then have:

+-- {: .num_prop} 
###### Proposition 
Let $X$ be a compact Polish space and $Y$ a Polish space.  Let $\mathrm{Emb}(X,Y) \subseteq Y^X$ be the space of embeddings of $X$ in $Y$, with its subspace topology. Then $\mathrm{Emb}(X,Y)$ is a Polish space.
=-- 

+-- {: .proof} 
###### Proof 
Since $X$ is compact and $Y$ is Hausdorff, a map $f : X \to Y$ is an embedding, i.e. $f$ is a homeomorphism from $X$ to its image, if and only if $f$ is injective.  Thus we have

$$ \mathrm{Emb}(X,Y) = \{ f \in Y^X\; \vert \; (\forall x, y \in X) \; x \ne y \Rightarrow f(x) \ne f(y) \} $$

To show $\mathrm{Emb}(X,Y)$ is a Polish space it is sufficient to show that is a $G_\delta$, i.e. a countable intersection of open subsets of $Y^X$ ([Marker](#Marker), Theorem 1.33).  For this we consider the sets

$$ O_m = \{ f \in Y^X \; \vert \; \forall x, y \in X \; d(x,y) \ge 1/m \implies f(x) \ne f(y) \} $$

If each set $O_m$ is open then $\mathrm{Emb}(X,Y)$ is a $G_\delta$, since 

$$\array{ 
 \mathrm{Emb}(X,Y) & = & \{ f \in Y^X\; \vert \; (\forall x, y \in X) \; (\exists m \in \mathbb{N}\; d(x, y) \geq 1/m) \implies f(x) \ne f(y) \} \\
& = & \{ f \in Y^X\; \vert \; (\forall x, y \in X \; \forall m \in \mathbb{N}) \; (d(x, y) \geq 1/m) \implies f(x) \ne f(y) \} \\
& = & \bigcap_{m=1}^\infty \{ f \in Y^X \; \vert \; (\forall x, y \in X) \; (d(x, y) \geq 1/m) \implies f(x) \ne f(y) \} \\
& = & \bigcap_{m=1}^\infty O_m. }$$

To complete the proof we show $O_m$ is open.  Note that for each $m$ the set

$$\array{
U_m & = & \{(x, y, f) \in X^2 \times Y^X \; \vert \; d(x,y) \ge 1/m \implies f(x) \neq f(y) \} \\
& = & \{(x, y, f) \in X^2 \times Y^X \; \vert \; d(x, y) \lt 1/m \vee f(x) \neq f(y)\}}$$

is open in $X^2 \times Y^X$.  Then we use a lemma (the overt space version of the [[tube lemma]]): if $K$ is a compact topological space and $A$ is an arbitrary topological space, and $U \subseteq K \times A$ is open, then

$$   \{ a \in A \; \vert \; \forall k \in K \;\; (k,a) \in U \} $$

is open.  Thanks to this and the fact that $K = X^2$ is compact, the set

$$ O_m = \{ f \in C(X,Y) \; \vert \; \forall (x,y) \in X^2 \;\; (x, y, f) \in U_m \} $$ 

is indeed open.
=-- 

##References##

* David Kerr, Hanfeng Li, _Ergodic Theory_. Springer Monographs in Mathematics (2016). doi:10.1007/978-3-319-49847-8 
{#KerrLi2016}

* [Polish spaces](http://golem.ph.utexas.edu/category/2008/08/polish_spaces.html), blog discussion, $n$-Category Caf&#233;, 2008.

* David Marker, _Descriptive Set Theory_, UIC Course Notes (Fall 2002) ([pdf](http://homepages.math.uic.edu/~marker/math512/dst.pdf)) 
{#Marker} 

* S.K. Berberian, _Borel spaces_, ([pdf](https://www.ma.utexas.edu/mp_arc/c/02/02-156.pdf)) 
{#Ber} 
  
* A.S. Kechris, _Classical descriptive set theory_, Springer-Verlag (1994). 
{#Kechris}

Internal groupoids in Polish spaces are considered in

* Martino Lupini, _Polish groupoids and functorial complexity_. ([arxiv](http://arxiv.org/abs/1407.6671))

The space of embeddings of $S^1$ in $S^3$ was studied using Polish spaces in

* Vadim Kulikov, A non-classification result for wild knots, Transactions AMS, 369 (2017), 5829-5853.   ([arXiv](https://arxiv.org/abs/1504.02714)).
{#Kulikov}

[[!redirects Polish spaces]]
