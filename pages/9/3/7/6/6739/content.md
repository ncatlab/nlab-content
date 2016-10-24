#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

Let $G$ and $H$ be [[graph|simple graphs]]. Then $H$ is a **graph minor** of $G$ if it is isomorphic to a graph obtained by applying a sequence of operations of the following sort, starting from $G$: 

* Removing edges; 

* Removing isolated points; 

* Contracting edges, where contracting an edge means removing it and identifying its endpoints. 

Graph minors can be viewed as certain types of subquotients in an appropriate category of graphs. 

## Categorical POV  

We take the point of view that a simple graph is essentially the same thing as a set $V$ equipped with a reflexive symmetric relation $E$, and a morphism of simple graphs is a function which respects these relations. Indeed, such a relation determines and is uniquely determined by a simple graph $G$ where for given vertices $x, y \in V$, there is an edge between $x$ and $y$ in $G$ iff both $E(x, y)$ and $x \neq y$. 

Notice that contraction of edges yields a quotient in this category. For example, if we want to contract a collection of edges by identifying certain points along an equivalence relation $R$, that is via some quotient map $q \colon V \to V/R$, then we simply take the image of the composite 

$$E \hookrightarrow V \times V \stackrel{q \times q}{\to} V/R \times V/R;$$ 

notice this image is a reflexive symmetric relation on $V/R$. While it might seem more natural to use instead an _irreflexive_ relation to express _loop-free graphs_ (a relation $E$ being **irreflexive** if it has empty intersection with the diagonal in $V \times V$), the fact of the matter is that irreflexive relations are not closed under the taking of images, and the category of sets with symmetric irreflexive relations and relation-preserving morphisms does not admit the forming of such quotients. 

Thus, we let $SimpGph$ denote the category of sets equipped with a reflexive symmetric relation. This category has many convenient properties: 

+-- {: .num_theorem} 
###### Theorem 
$SimpGph$ is the category of $\neg\neg$-[[separated presheaves]] on the full subcategory of $FinSet$ consisting of the objects $1, 2$. It is thus a [[Grothendieck quasitopos]]. In particular, both it and its opposite $SimpGph^{op}$ are regular categories. 
=-- 

Essentially the same observations apply to the category of finite simple graphs: it too is an [[extensive category|extensive]] quasitopos. 

The category of simple graphs is also *topological*, and *cohesive* in the following sense: 

+-- {: .num_prop} 
###### Proposition 
The forgetful functor $\Gamma = \hom(1, -): SimpGph \to Set$ is faithful, in fact exhibits $SimpGph$ as a [[topological concrete category]], and is *cohesive*: there is an adjoint string $\Pi \dashv \Delta \dashv \Gamma \dashv \nabla: Set \to SimpGph$, with $\Pi: SimpGph \to Set$ product-preserving. 
=-- 

Of course $\Delta$ assigns to a set $X$ the discrete graph on $X$, and $\nabla$ the codiscrete graph, while $\Pi(G)$ is the set of connected components of $G$. Let $\gamma: 1 \to \Delta \Pi$ denote the unit of $\Pi \dashv \Delta$; the component $\gamma G: G \to \Delta \Pi (G)$ takes a vertex $v \in G$ to the connected component to which it belongs. Notice that $\gamma G$ is a regular epi. 

+-- {: .num_defn} 
###### Definition 
A *contraction* map between simple graphs is a morphism $\pi: G \to G'$ that arises by pushing out a map of the form $\gamma K$ along some map $f: K \to G$: 

$$\array{
K & \stackrel{f}{\to} & G \\ 
\mathllap{\gamma K} \downarrow & po & \downarrow \mathrlap{\pi} \\ 
\Pi(K) & \to & G'
}$$ 

is a pushout square. If $G \to G'$ is a contraction map, we also say $G'$ is a *contraction* of $G$. 
=-- 

It is immediate that a contraction map is a regular epi, since every $\gamma K$ is regular epi. 

+-- {: .num_prop} 
###### Proposition 
Contraction maps are closed under composition. 
=-- 

+-- {: .proof} 
###### Proof 

=-- 

+-- {: .num_defn} 
###### Definition 
A graph $H$ is a *minor* of a graph $G$ if it arises as a subobject of some contraction of $G$: 

$$\array{
 & & G \\ 
 & & \downarrow \mathrlap{contraction} \\ 
H & \rightarrowtail & G'
}$$ 

=-- 

+-- {: .num_prop} 
###### Proposition 
The subquotient relation is reflexive and transitive. 
=-- 

+-- {: .proof} 
###### Proof 
Reflexivity is clear. For transitivity, we compose subquotients by taking a pushout square as follows. 

$$\array{
G & \twoheadrightarrow & G' & \twoheadrightarrow & G'' \\
 & &  ^\mathllap{mono} \uparrow & & \uparrow^\mathrlap{mono} \\
 & & H & \twoheadrightarrow & H' \\
 & & & & \uparrow^\mathrlap{mono} \\
 & & & & J
}$$

where we use the simple fact that the pushout of a mono along an arrow in $SimpGph$ is a mono (because $Vert$ reflects monos and preserves monos and pushouts, plus the fact that the pushout of a mono in $Set$ is a mono). 
=-- 

For finite graphs, the subquotient relation is also antisymmetric (if $G$ and $H$ are minors of one another, then they are isomorphic). Indeed, if either the arrow $G \twoheadrightarrow G'$ or the arrow $H \hookrightarrow G'$ is not an isomorphism, then $H$ has strictly fewer edges and vertices than $G$. This is clearly not the case for infinite graphs (e.g., the infinite rooted binary tree without leaves contains as a subgraph a disjoint sum of two copies of itself). 

(I intend to expand this section, eventually. Hopefully one can develop a categorical story about graph minors in particular.) 

## Minor-closed families 

* The collection of forests is closed under the graph minor relation. 

* The collection of planar graphs is closed under the graph minor relation. 

## Graph minor theorem 

This celebrated result of Robertson and Seymour says that no collection of finite graphs, ordered by the graph minor relation, has an infinite [[antichain]]. Equivalently, that in any collection of finite graphs, there are only finitely many elements which are minimal with respect to the graph minor relation. 

As a corollary, any class $F$ of finite graphs which is closed under minors admits a **forbidden minor characterization**: is precisely the class of graphs which do not have any members of a specific finite family of graphs
as a minor. (Proof: the complement of $F$ in the poset of finite graphs has finitely many minimal members. Then, $x$ belongs to $F$ iff none of these minimal members occurs as a minor of $x$. 

For example, the class of forests is precisely the class of finite graphs which do not have a triangle $K_3$ as a minor. The class of planar graphs is precisely the class of finite graphs which do not have $K_5$ or $K_{3, 3}$ as a minor. 

Forbidden minor characterizations also exist for certain classes of [[matroid|matroids]]. (See for example Wikipedia [here](http://en.wikipedia.org/wiki/Matroid#Forbidden_minors).) 

## References 

* Wikipedia article on graph minors [(link)](http://en.wikipedia.org/wiki/Minor_%28graph_theory%29)
