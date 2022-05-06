
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents 
{: toc}

## Introduction 

Both [[category theory]] and [[graph theory]] study patterns based on [[diagrams]] consisting of nodes and edges. Despite this surface impression, there is in fact very little interaction between the scientific communities of category theorists and of graph theorists. 

This article is a modest bridge, indicating that the _[[category]] of [[graphs]]_ (in the usual graph-theorist's sense -- see for example [Diestel](#Diestel)) has some very nice properties. 


## Simple graphs as relations 

By a **simple [[graph]]**, we mean a [[set]] $V$ whose elements are called *vertices*, together with a collection of 2-element subsets $\{x, y\}$ of $V$; these are called *edges* of the graph. 

There are various ways of forming a category of simple graphs. Perhaps the most straightforward is to define a morphism of graphs $G \to H$ to be a function $f: V \to W$ between the vertex sets to be a graph morphism if $\{f(x), f(y)\}$ is an edge of $H$ whenever $\{x, y\}$ is an edge of $G$. 

Another option -- and this is the one chosen for this article -- starts by regarding a simple graph as carrying the same information as a set $V$ equipped with a [[symmetric relation|symmetric]] [[reflexive relation|reflexive]] [[relation]] $E$. Indeed, such a relation determines (and is uniquely determined by) a simple graph $G$ where for given vertices $x, y \in V$, there is an edge $\{x, y\}$ between $x$ and $y$ in $G$ iff both $(x, y) \in E$ and $x \neq y$. We will write $E(x, y)$ to mean $(x, y) \in E$. 

Then, under the relational formulation, we define a morphism $(V, E) \to (W, F)$ between simple graphs straightforwardly[^1] as a function $f: V \to W$ that preserves the relevant structure, i.e., that $E(x, y)$ implies $F(f(x), f(y))$. One reason for preferring this notion of morphism is that it allows, for example, consideration of arbitrary edge contractions of a simple graph as [[quotients]] in the category (cf. [[graph minor]]), something that is not possible under the prior notion of morphism. 

[^1]: In other words, the usual notion of morphism between structures or models as in [[model theory]]. 

Thus we will adopt the latter notion of morphism which takes reflexive symmetric relations $E$ as primary. The resulting [[category]] of simple graphs is denoted by $SimpGph$. 

Note that graphs and their morphisms can also be understood in functorial language, by regarding simple graphs as special types of [[presheaves]], as follows. Let $C$ be the category of sets $1 \coloneqq \{\ast\}$ and $2 \coloneqq \{s, t\}$ and functions between them. Then a presheaf $X: C^{op} \to Set$ is given by sets $V = X(1)$ and $E = X(2)$ and maps 

* $d_0: X(2) \stackrel{X(\ast \mapsto s)}{\to} X(1)$ (source map), 

* $d_1: X(2) \stackrel{X(\ast \mapsto t)}{\to} X(1)$ (target map), 

* $i: X(1) \stackrel{X(s, t \mapsto \ast)}{\to} X(2)$ (reflexive map), 

* $\sigma: X(2) \stackrel{X(s \mapsto t, t \mapsto s)}{\to} X(2)$ (symmetry map). 

satisfying appropriate identities imposed by equations in $C$. Simple graphs can then be regarded [[equivalence|equivalently]] as such presheaves where the map 

$$\langle d_0, d_1 \rangle: X(2) \to X(1) \times X(1)$$ 

is a [[monomorphism]]. In that case, a morphism of simple graphs amounts to a [[natural transformation]] between such presheaves. 

### An aside on other notions of graph 

"Simple graph" as defined in the nLab (see [[graph]]) means that edges are 2-element subsets of $V$, but of course that doesn't preclude consideration of other types of graph. One option is to consider sets $V$ equipped with a collection of subsets of $V$ of cardinality either 1 or 2, i.e., allowing some but not necessarily all loops as edges. We don't call those "simple graphs" (at [[graph]] they are called "loop graphs"), but nevertheless they form a respectable category under the straightforward notion of morphism $f$ (if $\{x, y\}$ is an edge of the domain, possibly with $x = y$, then $\{f(x), f(y)\}$ is an edge of the codomain). Chih and Scull use this category, which they refer to as $Gph$, in their paper [_Homotopy in the Category of Graphs_](#ChihScul).


## Properties of $SimpGph$ 

The category $SimpGph$ has very good properties. For example,  

+-- {: .num_theorem} 
###### Theorem 
$SimpGph$ is a [[Grothendieck quasitopos]]. In particular, it is a [[regular category]] and even a [[logos]], and $SimpGph^{op}$ is also regular. It is also $\infty$-[[extensive category|extensive]]. 
=-- 

+-- {: .proof} 
###### Proof 
(See also [Adamek and Herrlich](#AdamHerr).) As above, let $C$ be the category of sets $1$ and $2$ and functions between them, and regard the category of simple graphs as a full subcategory of the presheaf [[topos]] $Set^{C^{op}}$. For this presheaf topos, there is just one nontrivial $\neg\neg$-dense sieve, namely the inclusion 

$$(s, t): C(-, 1) + C(-, 1) \to C(-, 2)$$ 

(where $s$ is shorthand for $C(-, \ast \mapsto s)$ and similarly for $t$) and so the category of $\neg\neg$-[[separated presheaves]] is equivalent to the category of presheaves $X$ such that the induced map 

$$X(2) \cong Set^{C^{op}}(C(-, 2), X) \stackrel{(s, t)^\ast}{\to} Set^{C^{op}}(C(-, 1) + C(-, 1), X) \cong X(1) \times X(1),$$ 

which is the source-target pairing $\langle d_0, d_1 \rangle: X(2) \to X(1) \times X(1)$, is monic. In other words, a simple graph in this language is exactly a separated presheaf. On the other hand, a Grothendieck quasitopos is, essentially by definition, the category of separated presheaves for a topology on a presheaf topos, in this case the $\neg\neg$-topology. 

Being a quasitopos with small coproducts, it is $\infty$-extensive provided that coproducts are disjoint. However, this is trivial to check (it even suffices to check, according to [[Elephant]] 2.6.5, that $0 \to 1$ is a [[regular monomorphism]], or that $1 + 1$ is a disjoint coproduct, which it obviously is). 
=-- 

+-- {: .num_remark #quasitopos} 
###### Remark 
Implicit in this proof is the way in which (for example) limits of simple graphs are calculated. Since $SimpGph$ is realized as a category of separated presheaves which is a [[reflective subcategory]] of all presheaves, limits in $SimpGph$ are calculated just as they are in the presheaf category $Set^{C^{op}}$, which is to say: they are computed objectwise, at the objects $1, 2$ of $C$. 

For example, consider how to construct the [[equalizer]] of a pair of graph maps $f, g: G \rightrightarrows H$. For the vertex set of the equalizer (computing the equalizer at the object $1$ of $C$), one just takes the equalizer of the functions between the vertex sets of $G$ and $H$. At the edge set level where we have maps $E = G(2) \rightrightarrows F = H(2)$: since there is at most one edge between two vertices, the maps $f(2), g(2)$ must agree on $e \in E$ provided $f(d_0 e) = g(d_0 e)$ and $f(d_1 e) = g(d_1 e)$, so the equalizer graph is just the full or [[graph|induced subgraph]] of $G$ given by the equalizer vertex set. 

Moreover, every induced subgraph $H \hookrightarrow G$ arises as an equalizer (consider the equalizer of the two embeddings of $G$ into the amalgamation $G +_H G$, which at the vertex level agrees with $H \hookrightarrow G$). 

Of course this is elementary, but we get much more more: the quasitopos $SimpGph$ is also a [[locally cartesian closed category]], and [[dependent products]] can also be read off directly from how they work for presheaves. 
=-- 

It is easy to describe [[monomorphism|monos]] and [[epimorphism|epis]] in $SimpGph$. For, let $\Gamma = \hom(1, -): SimpGph \to Set$ be the underlying vertex-set [[forgetful functor]]. 

+-- {: .num_prop #EmbeddingOfSimpGphIntoSet} 
###### Proposition 
The forgetful functor $\Gamma = \hom(1, -): SimpGph \to Set$ is faithful, in fact exhibits $SimpGph$ as a [[topological concrete category]]. 
=-- 

We omit the easy proof. Next we have two easy results:  

+-- {: .num_prop} 
###### Proposition 
$\Gamma$ [[reflected limit|reflects]] monos and epis (because $\Gamma$ is faithful). 
=-- 

+-- {: .num_prop} 
###### Proposition 
$\Gamma$ [[preserved limit|preserves]] [[limits]] and [[colimits]] (because it has a [[left adjoint]] $\Delta$ and a [[right adjoint]] $\nabla$). 
=-- 

It follows that $\Gamma: SimpGph \to Set$ both preserves and reflects monos and epis. As a result, we can prove various simple exactness results in $SimpGph$. For instance: 

+-- {: .num_lemma}
###### Lemma 
In $SimpGph$, the [[pushout]] of any mono is a mono. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose we have a pushout diagram in $SimpGph$: 

$$\array{
G & \to & H \\
 ^\mathllap{mono} \downarrow & & \downarrow^\mathrlap{k} \\ 
G' & \to & H'
}$$ 

Since $\Gamma$ preserves both pushouts and monos, and since the pushout of a mono in $Set$ is a mono, we have that $\Gamma(k)$ is monic in $Set$. Since $\Gamma$ reflects monos, this means $k$ is monic in $SimpGph$. 
=-- 

As already observed, there is a chain of adjoint functors $\Delta \dashv \Gamma \dashv \nabla: Set \to SimpGph$. But in fact there is a fourth functor in the chain: $\Delta$ has a left adjoint $\Pi: SimpGph \to Set$, the [[connected object|connected components]] functor. If $E$ is the simple graph consisting of two vertices $a, b$ with an edge between them, then there is a reflexive fork 

$$a, b: 1 \rightrightarrows E \stackrel{!}{\to} 1$$ 

and $\Pi$ is formed as a [[reflexive coequalizer]] of the induced diagram: 

$$SimpGph(1, -) \to SimpGph(E, -) \rightrightarrows SimpGph(1, -) \to \Pi$$ 

+-- {: .num_prop} 
###### Proposition 
$\Pi \dashv \Delta$, and $\Pi$ preserves products. 
=-- 

+-- {: .proof} 
###### Proof 
$\Pi$ preserves products because being a reflexive coequalizer, it is a [[sifted colimit]] of product-preserving functors. For graphs $G$, there is a natural map $u G: G \to \Delta \Pi G$ which at the underlying vertex-set level sends a vertex to its connected component; if $S$ is any set, then a graph map $f: G \to \Delta S$ must send any two vertices with an edge between them to the same point, and so $f$ factors as $G \stackrel{u G}{\to} \Delta \Pi G \stackrel{\Delta g}{\to} \Delta S$ for a unique map $g: \Pi G \to S$, and this establishes the adjunction $\Pi \dashv \Delta$. 
=-- 

### Equalizers and coequalizers

If $f, g \colon G \stackrel{\to}{\to} H$ are maps in $SimpGph$, then their [[equalizer]] $Eq(f, g) = i \colon K \to G$ is given at the vertex level by 

$$\Gamma(i) = Eq(\Gamma(f), \Gamma(g))$$ 

and at the edge level by $K(x, y) \Leftrightarrow G(i(x), i(y))$; in other words, if $x, y$ belong to $K$ and there is an edge between them in $G$, then that edge lies in $K$. To express this last condition, we say the subgraph $i$ is _full_ (at the edge level). 

Thus, $i$ is a regular mono in $SimpGph$ iff both $\Gamma(i)$ is monic in $Set$ and $i$ is full at the edge level (see Remark \ref{quasitopos}). 

The [[coequalizer]] of $f$ and $g$, say $Coeq(f, g) = q \colon H \to Q$, is given at the vertex level by 

$$\Gamma(q) = Coeq(\Gamma(f), \Gamma(g))$$ 

and at the edge level by taking the image of the composite $E_H \hookrightarrow Vert(H)^2 \stackrel{q^2}{\to} Vert(Q)^2$, so that 

$$Q(x, y) \Leftrightarrow \exists_{u, v} H(u, v) \wedge q(u) = x \wedge q(v) = y.$$ 

Thus, $q$ is a [[regular epimorphism]] if it is surjective at both the vertex and edge levels. 


### Ternary factorization 

The category of simple graphs has a [[ternary factorization system]] as follows: each morphism $f \colon G \to H$ factors as 

$$G \stackrel{q}{\to} G' \stackrel{a}{\to} H' \stackrel{i}{\to} H$$ 

where 

* $q$ is a surjection between vertex-sets and at the edge level, i.e., is a [[regular epi]]; 

* $a$ induces an identity between vertex-sets (hence is [[bimorphism|jointly monic and epic]]), but without necessarily being full at the edge level; 

* $i$ is given by an injection between vertex-sets and is full at the edge level, and (thus) is a [[regular mono]]. 

The factorization of $f$ into $q$ followed by $i \circ a$ is the (regular epi)-mono factorization, while the factorization of $f$ into $a \circ q$ followed by $i$ is the epi-(regular mono) factorization. (The fact that regular monos are stable under pushout, used to ensure that the epi-(regular mono) factorization is an [[orthogonal factorization system]], is true because $SimpGph$, being a [[quasitopos]], is a *coregular category*, meaning $SimpGph^{op}$ is [[regular category|regular]].) Both factorizations coincide at the level of underlying functions between vertex sets, both being the usual epi-mono factorization. 

In particular, we have the easy facts that 

* $f$ is a mono iff $q$ is a graph isomorphism: monos in $SimpGph$ are simple graph maps that are injective on vertices and edges, 

* $f$ is an epi iff $i$ is a graph isomorphism: epis in $SimpGph$ are simple graph maps that are surjective on vertices. 


### Subcategories

Graph theory suggests both full and wide subcategories of $SimpGph$. See [[the category of simple graphs from a graph-theoretic perspective]] for more details. 

### Natural numbers object 

The category $SimpGph$ has a [[natural numbers object]]; on abstract grounds this is formed by applying the reflection functor 

$$L: Set^{C^{op}} \to SimpGph$$ 

to the natural numbers object in $Set^{C^{op}}$. 

## References 

* [[Jiří Adámek]] and Horst Herrlich, _Cartesian closed categories, quasitopoi, and topological universes_. Comm. Math. Univ. Carol., Vol. 27, No. 2 (1986), 235-257. ([web](http://dml.cz/handle/10338.dmlcz/106447))
{#AdamHerr} 

* [[Tien Chih]], [[Laura Scull]], _Homotopy in the Category of Graphs_, ([arXiv:1901.01619](https://arxiv.org/abs/1901.01619))
{#ChihScul}

* Reinhard Diestel, Graph Theory (Second Edition), Graduate Texts in Mathematics 173, Springer (2000). 
{#Diestel}


category: category

[[!redirects category of simple graphs]]
[[!redirects Simp Gph]]
[[!redirects SimpGph]]

[[!redirects simple graph]]
[[!redirects simple graphs]]