+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea
A __clique__ in a category $C$ is a contractible choice of objects, i.e. a collection of objects of $C$ which are isomorphic to each other in exactly one way. 

Cliques are ubiquitous in category theory: [[universal properties]] define cliques, not single objects; but also because [[coherence theorems]] can be easily phrased in terms of cliques.

## Definition

A __clique__ of a category $C$ is a [[functor]] $A\colon T \rightarrow C$ out of a [[(-2)-groupoid]] $T$, i.e. $T$ is the [[indiscrete category]] on an [[inhabited set]].

Equivalently, a clique is an [[anafunctor]] $1 \to C$ from the [[trivial category]]. Indeed, a clique is also sometimes called an **anaobject**, in analogy with the fact that an [[object]] of $C$ is a _[[functor]]_ (not anafunctor) $1 \to C$.

We can form a category __$Clique(C)$__ whose objects are cliques of $C$, and whose morphisms and compositions are given as follows: given two such cliques $(T_0, A_0)$ and $(T_1, A_1)$ in $C$, say that a morphism between them is a natural transformation as below:
\begin{tikzcd}[ampersand replacement=\&]
	{T_0 \times T_1} \& {T_0} \\
	{T_1} \& C
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\pi_0}", from=1-1, to=1-2]
	\arrow[""{name=0p, anchor=center, inner sep=0}, phantom, from=1-1, to=1-2, start anchor=center, end anchor=center]
	\arrow["{\pi_1}"', from=1-1, to=2-1]
	\arrow["{A_0}", from=1-2, to=2-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{A_1}"', from=2-1, to=2-2]
	\arrow[""{name=1p, anchor=center, inner sep=0}, phantom, from=2-1, to=2-2, start anchor=center, end anchor=center]
	\arrow["m", shorten <=6pt, shorten >=6pt, Rightarrow, from=0p, to=1p]
\end{tikzcd}
Given consecutive such morphisms $m : (T_0, A_0) \rightarrow (T_1, A_1)$ and $n : (T_1, A_1) \rightarrow (T_2, A_2)$, and $(t_0, t_2) \in Ob(T_0 \times T_2)$, note that the composite $n_{(t_1, t_2)} m_{(t_0, t_1)}$ of corresponding components has the same value no matter what the choice of $t_1 \in Ob(T_1)$, and there is at least one such choice. Accordingly, we can take this to give a well-defined component $(n m)_{(t_0, t_2)}$, thus defining binary composition of morphisms of cliques. Similarly, we can take the identity on a clique $(T, A)$ to be the natural transformation whose component on $(t, t') \in Ob(T \times T)$ is the value of $A$ on the unique morphism from $t$ to $t'$ in $T$.

## Applications

### Objects with universal properties

Many [[universal properties]] that are commonly considered as defining "an object" actually define a clique.  For example, given two objects $a$ and $b$ of a category $C$, their [[cartesian product]] can be considered as the clique $T\to C$, where $T$ is the indiscrete category whose objects are product diagrams $a \overset{\leftarrow}{p} c \overset{\to}{q} b$, and where the functor $T\to C$ sends each such diagram to the object $c$ and each morphism to the unique comparison isomorphism between two cartesian products.  Note that unlike "the product" of $a$ and $b$ considered as a single object, this clique is defined without making any arbitrary choices.  This of course is the same philosophy which leads to [[anafunctors]], and so cliques are closely related to anafunctors.


### Cliques and anafunctors

There is an obvious [[anafunctor]] from $Clique(C)$ into $C$, through which every other anafunctor into $C$ factors in an essentially unique way into a genuine functor. If we ignore size issues (like that $Clique(C)$ will be large even for small $C$), this induces for $Clique(-)$ the structure of a (2-)monad on $Str Cat$ (the (2-)category of "genuine" functors between categories), such that the [[Kleisli category]] for this monad will be $Cat_{ana}$ (the (2-)category of anafunctors between categories).  This monad can also be described more explicitly; in particular the unit (a "genuine" functor) $C\to Clique(C)$ takes each object $c\in C$ to the corresponding clique $c\colon 1\to C$ defined on the domain $1$.  Note that this functor is a [[weak equivalence]], i.e. fully faithful and essentially surjective on objects, but not a strong equivalence unless one assumes the [[axiom of choice]].

In particular, we can use cliques to *define* anafunctors, taking an anafunctor from $C$ into $D$ to simply be a genuine functor from $C$ into $Clique(D)$. (With composition of these defined in a straightforward way, and natural transformations between these being simply natural transformations of the corresponding genuine functors into $Clique(D)$). Accordingly, $Clique(-)$ is itself the same as $Cat_{ana}(1, -)$, and this can also be taken as a definition of a clique (hence the alternate name *anaobject*).


### Monoidal strictifications

Unsurprisingly, cliques provide a useful technical device for describing strictifications of [[monoidal category|monoidal categories]]. 

It is relevant first to recall the original form of Mac Lane's [[coherence theorems|coherence theorem]]: the free monoidal category on one generator, $F[1]$, is monoidally equivalent to the discrete monoidal category $(\mathbb{N}, +, 0)$. Thus each connected component $C_n$ of $F[1]$ is an indiscrete category whose objects are the possible $n$-fold tensor products of the generator, possibly with instances of the unit object folded in; the indiscreteness says that "all diagrams built from associativity and unit constraints commute". 

One canonical way to strictify a monoidal category $M$ is by considering cliques in $M$ where the domains are the $C_n$ and the functors model associativity and unit constraints, in the following precise sense: 

1. We may form a monoidal category $Oper(M)$ whose objects are functors 
$$F: M^j \to M$$ 
for natural numbers $j$, and whose morphisms are natural transformations between such functors. The tensor product of $F: M^j \to M$ and $G: M^k \to M$ in $Oper(M)$ is the composite 
$$M^{j+k} \cong M^j \times M^k \stackrel{F \times G}{\to} M \times M \stackrel{\otimes}{\to} M$$ 
and the rest of the monoidal structure on $Oper(M)$ is inherited from the monoidal structure on $M$. 

1. By freeness of $F[1]$, we have a (strict) monoidal functor 
$$\kappa: F[1] \to Oper(M)$$ 
uniquely determined as the one which sends the generator $1$ of $F[1]$ to $Id_M$. On each connected component $C_n$ of $F[1]$, this restricts to a functor 
$$C_n \stackrel{\kappa|}{\to} Cat(M^n, M)$$ 

1. Then, for each $n$-tuple of objects $(x_1, \ldots, x_n)$ of objects of $M$, there is an associated clique $\kappa_{x_1, \ldots, x_n}$ in $M$: 
$$C_n \stackrel{\kappa|}{\to} Cat(M^n, M) \stackrel{eval_{(x_1, \ldots, x_n)}}{\to} M$$

1. Finally, the objects of the strictification $M^{st}$ are $n$-tuples $(x_1, \ldots, x_n)$ of objects of $M$. A morphism 
$$(x_1, \ldots, x_m) \to (y_1, \ldots, y_n)$$ 
is by definition a clique morphism $\kappa_{x_1, \ldots, x_m} \to \kappa_{y_1, \ldots, y_n}$. There is an evident strict monoidal category structure on $M^{st}$ which at the object level is just concatenation of tuples. 

It is straightforward to check that the natural inclusion 

$$i: M \to M^{st},$$ 

which interprets each object as a 1-tuple and each morphism as an evident clique morphism, is a monoidal equivalence. The essential idea is that there is a canonical clique isomorphism 

$$(x_1, x_2, \ldots, x_n) \to i(Bracketing(x_1 \otimes \ldots \otimes x_n))$$ 

for every choice of bracketing the tensor product on the right in $M$ (possibly with units thrown in). 


## In graph theory

There is a notion of clique in an undirected simple [[graph]] familiar to graph-theorists: a _clique_ in a graph $G$ is a subset of vertices $C \subseteq V(G)$ such that any two distinct vertices $x,y \in C$ are connected by an edge. The cliques of cardinal $1$ are exactly the vertices and the cliques of cardinal $2$ are exactly the edges. Thus, if we know all the cliques of a graph, we know automatically this graph. If we know a graph, we can compute the cliques of this graph. There is thus a bijection between the undirected simple graphs and the sets of all cliques of an undirected simple graph. But it would be better to have an intrinsic definition of what is the set of all cliques of an undirected simple graph without reference to graphs in order to state this bijection. The set of all cliques of an undirected simple graph can be seen as a [[coherence space]] and we then have a bijection between undirected simple graphs and coherence spaces. Note that although it is a bijection, it requires some work to compute the set of all cliques of an undirected graph for a human or a computer. Thus, a coherence space can be seen as a richer description of an undirected simple graph.

This definition is specialized to simple graphs, however, and a more general definition that works for arbitrary undirected graphs (possibly containing loops and multiple edges) takes a clique (of size $n$) in $G$ to be a graph homomorphism $C : K_n \to G$ from the [[complete graph]] on $n$ vertices.  Indeed, this latter definition could also be taken as a reasonable notion of clique in any undirected graph/[[quiver]].  Equivalently, a clique in this sense is a subgraph $C$ of $G$ which is _indiscrete_: there is exactly one edge in $C$ from $x$ to $y$ for any vertices $x$, $y$ of $C$. 

The categorical notion of clique is one step removed from that: a clique in a category $C$ is a functor $i: K \to C$ where the underlying graph of $K$ is indiscrete. The generic "picture" of a clique in a category is reminiscent of (and no doubt the etymology derives from) the graph-theoretic notion, even if the notions are technically distinct. 


[[!redirects clique]]
[[!redirects cliques]]
