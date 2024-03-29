
# The Lambert $W$ function
* table of contents
{: toc}

## Idea 

In [[complex analysis]], the Lambert $W$-function is a [[multivalued function|multi-branched function]] [[inverse function|inverse]] to the function $f(z) = z e^z$. Among other things, it is important in the enumeration of tree-like structures, for instance [[tree|rooted trees]], and in the combinatorial study of the [[Lagrange inversion formula]]. 

We have $W(z) e^{W(z)} = z$. In a neighborhood of $z = 0$, we may develop $W(z)$ as a formal [[power series]], and there is a quite remarkable formula: 

$$ W(z) = \sum_{n = 1}^{\infty} \frac{(-n)^{n-1} z^n}{n!} .$$ 

A proof of this formula is sketched below. 


## Lambert $W$ and rooted trees 

Let $R(X)$ be the [[species]] of rooted trees. Choosing a structure of rooted tree $T$ (on a finite set of vertices) amounts to 

* Choosing one vertex to serve as the root of $T$; 

* Choosing a structure of "rooted forest" (a disjoint collection of rooted trees) on the complement of the root. 

The idea is that given a rooted forest, we get a rooted tree by adding in a new vertex (which serves as root) and drawing an edge from each root of the forest to the new vertex. 

This observation leads to the structural isomorphism 

$$ R(X) = X \otimes \exp(R(X))	$$ 

Let $R(x) = \sum_{n \geq 0} \frac{a_n x^n}{n!}$ be the formal power series corresponding to the generating function of $R(X)$, so that $a_n$ counts the number of rooted trees on $n$ vertices. We may call $R(x)$ the _cardinality_ of $R(X)$. One has the analogous decategorified formula 

$$R(x) = x e^{R(x)}$$ 

or 

$$R(x) e^{-R(x)} = x$$ 

which means, after a short series of algebraic manipulations, that $R(x)$ is related to the Lambert $W$ function as follows: 

$$R(x) = - W(-x).$$ 


## Counting rooted trees 

The number of possible rooted tree structures on $n$ labeled vertices is $n^{n-1}$. We sketch Joyal's beautiful proof of this fact; it follows that 

$$\array{
W(x) & = & - R(-x) \\ 
 & = & - \sum_{n \geq 1} \frac{n^{n-1} (-x)^n}{n!} \\ 
 & = & \sum_{n \geq 1} \frac{(-n)^{n-1} x^n}{n!}
}$$ 

as claimed earlier. 

In fact, Joyal counts the number of _bipointed_ trees (trees equipped with an ordered pair of vertices, possibly the same one), and shows this is the same as the number of endofunctions on an $n$ element set. Since this is $n^n$, and since the number of ordered pairs of vertices is $n^2$, it follows that the number of tree structures on an $n$-element set is $n^{n-2}$, a result referred to as **Cayley's theorem**. Therefore the number of _rooted_ trees is $n \cdot n^{n-2} = n^{n-1}$. 

For a bipointed tree $T$, let the ordered pair of vertices be $(t, h)$ where $t$ is called a _tail_ and $h$ a _head_. The set of vertices on the unique path from $t$ to $h$ is endowed with a [[linear order]] (namely, the order in which they appear on the path, with $t$ first). We call this ordered set the _spine_ of the bipointed tree. At the same time, each vertex $v$ along the spine is the root of a rooted tree $T_v$: a full subgraph where a vertex $w$ of $T$ belongs to $T_v$ if the unique path from $w$ to $h$ first meets the spine at $v$. 

A choice of bipointed tree structure on a finite set $S$ can thus be equivalently described as follows: 

* Partition $S$ into one or more subsets (which are equivalence classes); 

* Choose a rooted tree structure on each class (if the root is $v$, this tree structure will be $T_v$); 

* Choose a way of linearly ordering the equivalence classes (which is really the same as linearly ordering the roots). 

If $L$ is the species of linearly ordered sets, and $R$ is the species of rooted trees, this way of describing bipointed trees establishes an explicit bijection between $L \circ R$ and the species of bipointed trees. 

For an endofunction $f \colon S \to S$, let $K$ be the intersection of images of iterates $f^{(n)}(S)$. It is immediate that the restriction $f\colon K \to K$ is a surjection and therefore a bijection (permutation). Picturing an endofunction as a graph (where an edge is drawn between $s$ and $f(s)$), each vertex $v \in K$ is the root of a rooted tree $T_v$: a full subgraph where a vertex $w$ belongs to $T_v$ if $f^{(n)}(w) = v$ for some $n$, but $f^{(k)}(w)$ does not belong to $K$ for $k \lt n$. 

A choice of endofunction structure on $S$ can thus be equivalently described as follows: 

* Partition $S$ into one or more subsets (equivalence classes); 

* Choose a rooted tree structure on each class (if the root is $v$, this tree structure is $T_v$); 

* Choose a permutation on the set of equivalence classes (tantamount to a permutation of the roots $v$). 

If $P$ is the species of permutations, and $R$ the species of rooted trees, this establishes an explicit bijection between $P \circ R$ and the species of endofunctions. 

Since the species $L$ of linear orderings and the species $P$ of permutations have the same cardinality, it follows that the species $L \circ R$ and $P \circ R$ also have the same cardinality, which is to say that the number of bipointed tree structures on $S$ equals the number of endofunctions, as was to be proved. 
 

[[!redirects Lambert W function]]
[[!redirects Lambert W-function]]
