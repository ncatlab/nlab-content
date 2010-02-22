#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A __clique__ of a category $C$ is a pair of a category $T$ which is weakly equivalent to $1$ (i.e., $T$ is the [[indiscrete category]] on an [[inhabited set|inhabited collection]] of [[object]]s) and a [[functor]] $A : T \rightarrow C$. 

We can form a category __$Clique(C)$__ whose objects are cliques of $C$, and whose morphisms and compositions are given as follows: Given two such cliques $(T_0, A_0)$ and $(T_1, A_1)$ in $C$, say that a morphism between them is a natural transformation from $T_0 \times T_1 \stackrel{\pi}{\to} T_0 \stackrel{A_0}{\to} C$ to $T_0 \times T_1 \stackrel{\pi}{\to} T_1 \stackrel{A_1}{\to} C$, where the $\pi$ are the appropriate projections. Given such morphisms $m : (T_0, A_0) \rightarrow (T_1, A_1)$ and $n : (T_1, A_1) \rightarrow (T_2, A_2)$, and $(t_0, t_2) \in Ob(T_0 \times T_2)$, note that the composite $n_{(t_1, t_2)} m_{(t_0, t_1)}$ of corresponding components has the same value no matter what the choice of $t_1 \in Ob(T_1)$, and there is at least one such choice. Accordingly, we can take this to give a well-defined component $(n m)_{(t_0, t_2)}$, thus defining binary composition of morphisms of cliques. Similarly, we can take the identity on a clique $(T, A)$ to be the natural transformation whose component on $(t, t') \in Ob(T \times T)$ is the value of $A$ on the unique morphism from $t$ to $t'$ in $T$.

There is an obvious [[anafunctor]] from $Clique(C)$ into $C$, through which every other anafunctor into $C$ factors in an essentially unique way into a genuine functor. This induces for $Clique(-)$ the structure of a (2-)monad on $Str Cat$ (the (2-)category of genuine functors between categories), such that the Kleisli category for this monad will be $Cat_{ana}$ (the (2-)category of anafunctors between categories). Thus, we can use cliques to define anafunctors, taking an anafunctor from $C$ into $D$ to simply be a genuine functor from $C$ into $Clique(D)$. (With composition of these defined in a straightforward way, and natural transformations between these being simply natural transformations of the corresponding genuine functors into $Clique(D)$). Accordingly, $Clique(-)$ is itself the same as $Cat_{ana}(1, -)$.

## Applications ## 

#### Monoidal strictifications #### 

Unsurprisingly, cliques provide a useful technical device for describing strictifications of [[monoidal category|monoidal categories]]. 

It is relevant first to recall the original form of Mac Lane's [[coherence theorems|coherence theorem]]: the free monoidal category on one generator, $F[1]$, is monoidally equivalent to the discrete monoidal category $(\mathbb{N}, +, 0)$. Thus each connected component $C_n$ of $F[1]$ is an indiscrete category whose objects are the possible $n$-fold tensor products of the generator, possibly with instances of the unit object folded in; the indiscreteness says that "all diagrams commute". 

Now suppose given a monoidal category $(M, \otimes, I, \alpha, \lambda, \rho)$. Then 

1. We may form a monoidal category $Op(M)$ whose objects are functors 
$$F: M^j \to M$$ 
and whose morphisms are natural transformations between such functors. The tensor product of $F: M^j \to M$ and $G: M^k \to M$ in $Op(M)$ is the composite 
$$M^{j+k} \cong M^j \times M^k \stackrel{F \times G}{\to} M \times M \stackrel{\otimes}{\to} M$$ 
and the rest of the monoidal structure on $Op(M)$ is inherited from the monoidal structure on $M$. 

1. Next, we then have a (strict) monoidal functor 
$$\kappa: F[1] \to Op(M)$$ 
uniquely determined as the one which sends the generator $1$ of $F[1]$ to $Id_M$. On each connected component $C_n$ of $F[1]$, this restricts to a functor 
$$C_n \stackrel{\kappa|}{\to} Cat(M^n, M)$$ 

1. Thus, for each $n$-tuple of objects $(x_1, \ldots, x_n)$ of objects of $M$, there is an associated clique $\kappa_{x_1, \ldots, x_n}$ in $M$: 
$$C_n \stackrel{\kappa|}{\to} Cat(M^n, M) \stackrel{eval_{(x_1, \ldots, x_n)}}{\to} M$$

1. Now we describe the strictification $M^{st}$. The objects of $M^{st}$ are $n$-tuples $(x_1, \ldots, x_n)$ of objects of $M$. A morphism 
$$(x_1, \ldots, x_m) \to (y_1, \ldots, y_n)$$ 
is precisely a clique morphism $\kappa_{x_1, \ldots, x_m} \to \kappa_{y_1, \ldots, y_n}$. There is an evident strict monoidal category structure on $M^{st}$ which at the object level is just concatenation of tuples. 

It is straightforward to check that the natural inclusion 

$$i: M \to M^{st},$$ 

which interprets each object as a 1-tuple and each morphism as an evident clique morphism, is a monoidal equivalence. 

## Etymology and relation to graph theory ## 

There is a notion of clique in an undirected (simple) [[graph]] familiar to graph-theorists: a _clique_ $C$ in a graph $G$ is a subgraph which is complete as a graph, i.e., one for which any two distinct vertices are connected by an edge. Thus, a clique having $n$ vertices is isomorphic to an inclusion of a $K_n$. 

A reasonable analogue for directed graphs ([[digraph]]s) might be a subgraph $C$ which is _indiscrete_: there is exactly one edge in $C$ from $x$ to $y$ for any vertices $x$, $y$ of $C$. 

The categorical notion of clique is one step removed from that: a clique in a category $C$ is a functor $i: K \to C$ where the underlying graph of $K$ is indiscrete. The generic "picture" of a clique in a category is reminiscent of (and no doubt derived from) the graph-theoretic notion, even if the notions are technically distinct. 
