+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}


## Idea

__$Quiv$__ or __$DiGraph$__ is the category of [[quivers]] or (as category theorists often call them) [[directed graphs]]. It can be viewed as the default categorical model for the concept of a category of graphs.

## Definition

We can define a quiver to be a functor $G\colon X^{op} \to Set$, where $X^{op}$ is the [[category]] with an [[object]] $0$, an object $1$ and two [[morphisms]] $s, t\colon 1 \to 0$, along with [[identity morphisms]].  This lets us efficiently define $Quiv$ as the category of [[presheaves]] on $X$, where:

* objects are [[functors]] $G\colon X^{op} \to Set$,
* morphisms are [[natural transformations]] between such functors.

In other words, $Quiv$ is the [[functor category]] from this $X^{op}$ to [[Set]].

## As a topos 

The category $Quiv = Set^{X^{op}}$, being a category of [[presheaves]], is a [[topos]]. The [[representable functors]] $X(-, 0), X(-, 1)$ may be pictured as the "generic figures" (generic vertex, generic edge) that occur in directed graphs: 

$$X(-, 0) = \bullet, \qquad X(-, 1) = (x \stackrel{e}{\to} y)$$ 

and from this picture we easily see that $X(-, 0)$ has two subobjects $\emptyset, \bullet$ whereas $X(-, 1)$ has five: $empty, x, y, (x, y), (x \stackrel{e}{\to} y)$.

Being a presheaf topos has a lot of nice consequences and instantly yields answers to questions like whether finite [[limit|limits]] of directed graphs exist or how to construct the [[exponential object|exponential]] quiver $Y^X$ of all homomorphisms $X\to Y$ between two quivers $X,Y$ in $Quiv$ since the answers are provided by topos theory.

In the following subsections some of the topos structure in $Quiv$ is worked out explicitly. 

### The subobject classifier{#Omega_graph}

Knowing the subobjects of the representable functors in turn allows us to calculate the structure of the [[subobject classifier]] $\Omega$ since they correspond to the elements of the value of $\Omega$ at the corresponding objects of $X^{op}$ i.e. the set of vertices of $\Omega$ is $\Omega(0)=\{\emptyset,\bullet\}$ and the set of edges is $\Omega(1)=\{empty, x, y, (x, y), (x \stackrel{e}{\to} y)\}$.

When pictured, $\Omega$ is given by the following quiver with two vertices and five edges: 

$$\array{
\emptyset & \underoverset{x}{y}{\rightleftarrows} & \bullet \\ 
\mathllap{empty} \circlearrowleft & & \circlearrowleft \circlearrowleft \mathrlap{x \stackrel{e}{\to} y} \\ 
 & & \mathllap{(x, y)}  
}$$ 

where the vertex $\emptyset$ has one loop labeled "empty", and the vertex $\bullet$ has two loops with labels $(x, y)$ and ($x \stackrel{e}{\to} y$). 

How does $\Omega$ work? Suppose that $X\subseteq Y$ is a subgraph and $\chi_X:Y\to\Omega$ its characteristic map, then $\chi_X$ maps vertices of $Y$ not in $X$ to $\emptyset$ and vertices in $X$ to $\bullet$ (a vertex is either contained in a subgraph or not - the choice is binary and, accordingly, $\Omega$ needs two vertices to represent this). For edges the situation is more complicated since there are five ways (and, accordingly five edges in $\Omega$ to represent this) for an edge $z$ of $Y$ to be related to the subgraph $X$: the most straightforward is when $z$ has neither source nor target in $X$, such $z$ are definitely not in $X$ and are represented in $\Omega$ by the loop at $\emptyset$. Now suppose that $z$ has either source or target vertex in $X$ but not both: $\chi_X$ maps these to the maps $x,y$ between $\emptyset\rightleftarrows\bullet$, respectively. When $z$ has both source and target in $X$, the edge itself might or might not be in $X$, and the corresponding two cases are represented by the two loops at $\bullet$ , respectively, with $e$ representing the edges that are contained in $X$.

### (Double) negation

The [[negation]] $\neg:\Omega\to \Omega$ is defined as the characteristic map of $\bot:1\to\Omega$. It specifies how

$$im(\bot)= \underoverset{{empty}}{\empty}{\circlearrowleft}$$

sits as a subgraph in $\Omega$: 

since $\bullet$ is not in $im(\bot)$ whereas $\empty$ is, $\neg$ interchanges the two vertices and, accordingly, all loops at $\bullet$ must go to ${empty}$ . Conversely, $empty$ goes to $e$ (since it is fully contained in $im(\bot)$). Now $x$ has its target but not its source in $im(\bot)$ hence it goes to $y$ whereas $y$ has its source but not its target in $im(\bot)$ and therefor goes to $x$.

Complementing a subobject $X\subseteq Y$ i.e. taking the subobject $\neg X$ of $Y$ that is classified by $\neg\circ\chi_X$ amounts to taking all vertices of $Y$ not in $X$ and all the edges in $Y$ between them.

Whence the result $\neg\neg X$ of applying $\neg$ twice to $X\subseteq Y$ amounts to adding to $X$ all the edges of $Y$ that have source and target in $X$. This implies in turn that a subgraph $X\subseteq Y$ is [[dense subobject|dense]] for the [[double negation|double negation topology]] $\neg\circ\neg:\Omega\to\Omega$ , precisely when it contains all vertices of $Y$ since complementing twice will throw into $\neg\neg X$ all the edges in $Y$ between all the vertices in $X$.

By definition, a quiver $X$ is [[separated object|separated]] for $\neg\neg$ when for every other quiver $Y$ and dense subobject $i:S\hookrightarrow Y$ and any map $f:S\to X$ there is at most one $g:Y\to X$ such that the following diagram commutes:

$$
\array{
S & & \\
i\downarrow &\searrow &f \\
Y &\underset{g}{\to} & X
}
$$

A separated quiver $X$ is a $\neg\neg$-sheaf when such a unique $g$ always exists.

Suppose that a quiver $X$ has a pair of parallel edges $w,z$. Then the subgraph $i:S\hookrightarrow X$ that is just like $X$ but has $w,z$ ommitted is dense in $X$. Let $\tau_{zw}:X\to X$ be the automorphism of $X$ that is just like the identity on $X$ except that it interchanges $w$ and $z$. Then $id_X\circ i=\tau_{zw}\circ i=i$ and one sees that $X$ is not separated.

Conversely, let $X$ be a quiver with at most one edge $x\to y$ between any pair $(x,y)$ of vertices and $f:S\to X$ be a map with $i:S\hookrightarrow Y$ is dense in $Y$. Since $i$ is a bijection on the vertex sets of $S$ and $Y$, if a factorization of $f$ through $g:Y\to X$ and $i$ exists the effect of $g$ on the vertices is uniquely determined by $f$ but since in $X$ there is at most one edge between any pair of vertices the image of any edge $a\to b$ in $Y$ under $g$ is already fixed: it is the unique edge between $g(a)$ and $g(b)$. In particular, one sees that a separated object $X$ is a sheaf precisely when there exists exactly one edge between any pair of vertices since then arbitrary edges in arbitrary factors $Y$ can be mapped to the appropriate edge in $X$. To sum up:

+-- {: .num_prop #negneg_subcats} 
###### Proposition
A quiver $X$ is separated for the double negation topology $\neg\neg$ precisely if there exists at most an edge $a\to b$ between any pair $(a,b)$ of vertices. $X$ is a $\neg\neg$-sheaf precisely if there exists a unique edge $a\to b$ between any pair $(a,b)$. $\Box$
=--

The corresponding full subcategories are denoted by $Sep_{\neg\neg}(Quiv)$ and $Sh_{\neg\neg}(Quiv)$ , respectively. By generalities, it follows that $Sep_{\neg\neg}(Quiv)$ is a [[quasitopos]] and $Sh_{\neg\neg}(Quiv)$ is a [[Boolean topos]].

Quivers that have at most one edge between any pair of vertices can be called 'simple' with the caveat that contrary to (the usual concept of) a simple graph they are allowed to have loops. Similarly, $\neg\neg$-sheaves can be called 'complete'.

Since the edges of $\neg\neg$-separated quivers simply encode a binary endorelation on their vertex sets and being a morphism between $\neg\neg$-separated quivers then amounts to preserve that relation one sees that $Sep_{\neg\neg}(Quiv)$ and $Sh_{\neg\neg}(Quiv)$ are equivalent to the categories $Bin$ with objects $(X,\rho)$ where $X$ is a set and $\rho$ a binary endorelation on $X$, and, respectively, the category  $TotalRel$ of sets equipped with the total relation. The latter can be identified with $Set$ since morphisms between sets equipped with the total relation behave just like ordinary functions between sets. 

### Some subcategories and adjunctions

The inclusion $Sh_{\neg\neg}(Quiv)\hookrightarrow Sep_{\neg\neg}(Quiv)$ is actually an [[level|essential localisation]] since it corresponds (from the relational perspective) to the [[adjoint triple|adjoint string]] $e\dashv u\dashv t:Set\hookrightarrow Bin$ where $t$ maps a set $X$ to $(X,\tau_X)$ with $\tau_X$ the total relation on $X$, $u$ is the forgetful functor mapping $(X,\rho)$ to $X$ and, $e$ maps a set $X$ to $(X,\empty)$.

Similarly, $Sh_{\neg\neg}(Quiv)\overset{i}{\hookrightarrow} Quiv$ is an essential subtopos: if we identify sheavification $r$ with the functor that maps a quiver to the quiver on the same vertex set with edge set the total relation on the vertex set, then $l\dashv r\dashv i$ where $l$ forgets the edges of a complete quiver.

In particular, it follows then from general properties of the [[double negation|double negation topology]] that $Sh_{\neg\neg}(Quiv)$ is the [[Aufhebung]] of $0\dashv 1$. Whence, there exists indeed a notion of 'codiscreteness' (= an Aufhebung of $0\dashv 1$) for quivers, namely 'completeness', but it does not arise from a right adjoint to the [[section|section functor]] $\Gamma: Quiv\to Set$ that maps a quiver to its set of loops. Indeed, the adjoint string $\Pi\dashv\Delta\dashv\Gamma:Quiv\to Set$ that comes with the 'discrete' inclusion $\Delta$ that maps a set to the quiver with vertex set $X$ and edge set precisely one loop for every vertex, is not a localisation since $\Pi\dashv\Delta$ is not a [[geometric morphism]] because $\Pi$ fails to preserve products.

Furthermore, since it is a general result for presheaf toposes (cf. La Palme Reyes et al. [2004](#RRZ04), p.204) that $\Gamma$ has a right adjoint $B$ precisely if a generic figure has a point and in the case of Quiv neither the generic vertex nor the generic edge contains a loop, we see that the functor $\Gamma:Quiv\to Set$ has no right adjoint.

## Related entries

* [[hypergraph]]


## References

* R. T. Bumby, D. M. Latch, _Categorical Constructions in Graph Theory_ , Internat. J. Math. & Math. Sci. **9** no.1 (1986) pp.1-16.

* {#Law89a} [[F. W. Lawvere]], *Qualitative Distinctions between some Toposes of Generalized Graphs*, Cont. Math. **92** (1989) pp.261-299.

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, *Generic Figures and their Glueings*, Polimetrica Milano 2004.

* {#Vigna03} S. Vigna, _A Guided Tour in the Topos of Graphs_ , arXiv.0306394 (2003). ([abstract](https://arxiv.org/abs/math/0306394))



category: category

[[!redirects Quiv]]
[[!redirects DiGraph]]
[[!redirects Digraph]]
