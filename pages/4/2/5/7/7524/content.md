
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

In an ordinary undirected [[graph]], each edge $e$ links an [[unordered pair]] of vertices $x$ and $y$ (perhaps allowing for the possibility that $x = y$, as in the case of a loop).  Hypergraphs generalize this, allowing a "hyperedge" to link any set of "hypervertices".  Abstracting everything away but the _incidence_ relation between hypervertices and hyperedges, a hypergraph can be modelled as an arbitrary heterogenous [[relation]], or more generally as a [[span]].

## Categories of hypergraphs: Definition

As with "[[graph]]", the word "hypergraph" does not have an entirely standardized meaning.  We take as our starting point [(Schmidt & Str&#246;hlein)](#SchmidtStroehlein), who define hypergraphs as heterogenous relations (usually presented as boolean-valued matrices) and give an appropriate notion of morphism.  We call these "simple" hypergraphs, since they are a special case of a more general definition given below.

+-- {: .num_defn }
###### Definition

The **category of simple hypergraphs** $SimpHGrph$ has objects consisting of a pair of sets $(V,E)$ equipped with a relation $R \subseteq V \times E$, and morphisms $(R \subseteq V \times E) \to (R' \times V' \times E')$ consisting of pairs of functions $(f : V \to V', g : E \to E')$ which preserve the relation, i.e., such that for all $v\in V, e \in E$, if $(v,e) \in R$ then $(f v,g e) \in R'$.

=--

The category of simple hypergraphs could also be referred to more dryly as "the category of binary relations", although this has potential for confusion with [[Rel]] (whose _morphisms_ are binary relations).

In a simple hypergraph, a hypervertex can be incident to a hyperedge at most once, but in some situations one wants to allow a hypervertex to be incident to a hyperedge multiple times.  To define hypergraphs in this more general sense, we keep the intuition of hypergraphs-as-heterogenous-relations, but generalize relations to spans.

+-- {: .num_defn }
###### Definition

The **category of hypergraphs** $HGrph$ has objects consisting of a pair of sets $(V,E)$ equipped with a span $V \overset{v}\leftarrow R \overset{e}\rightarrow E$, and morphisms $(V \overset{v}\leftarrow R \overset{e}\rightarrow E) \to (V' \overset{v'}\leftarrow R' \overset{e'}\rightarrow E')$ consisting of triples of functions $(f : V \to V', g : E \to E', h:R \to R')$ such that $v'\circ h = f\circ v$ and $e'\circ h = g\circ e$.

=--

Note that $HGrph$ is just the [[category of presheaves]] over the "[[walking structure|walking]] cospan" $\bullet \rightarrow \bullet \leftarrow \bullet$, and that $SimpHGrph$ is a [[full subcategory]] of $HGrph$.

## Hypergraphs from a topos-theoretic perspective

In Lawvere ([1986](#Law86) p.6, [1989](#Law89) pp.283-4) it is pointed out that $Set^{\bullet\leftarrow\bullet\rightarrow\bullet}$ is a spatial topos since it is equivalent to the topos of sheaves on the space $X=\{a,b,c\}$ with topology $\tau=\{\emptyset,\{a\},\{b\},\{a,b\},\{a,b,c\}\}$ i.e. $X$ has two isolated points $a,b$ and a [[focal point|focal]] one $c$ whose only neighborhood is the whole space.

The [[lattice of subtoposes]] of $Set^{\bullet\leftarrow\bullet\rightarrow\bullet}$ consists (besides the two obvious subtoposes) of one [[closed subtopos|closed]] and two [[open subtopos|open]] copies of $Set$, two closed copies of the [[Sierpinski topos]] complementing the open copies of $Set$ respectively and an open $Set\times Set=Sh(\{a,b\})=Sh_{\neg\neg}(Set^{\bullet\leftarrow\bullet\rightarrow\bullet})$ complementing the closed copy of $Set$. In particular, $Set^{\bullet\leftarrow\bullet\rightarrow\bullet}$ is a [[scattered topos]].

The complementary open-closed pairs of the subtopos lattice correspond precisely to analyses of $Set^{\bullet\leftarrow\bullet\rightarrow\bullet}$ by [[Artin gluing]].

For instance, take the product functor $\sqcap\colon Set\times Set\to Set$ with  $(X,Y)\mapsto X\times  Y$. $\sqcap$ is left exact since it forms an adjoint string with the [[diagonal functor]] and the coproduct functor: $\sqcup\dashv \triangle\dashv\sqcap$ .

Then $\mathbf{Gl}(\sqcap)$ has objects $((X,Y),Z, u\colon Z\to X\times Y)$ where $(X,Y)\in Set\times Set$ and $Z\in Set$ and $u$ is a morphism in $Set$. Since by the universal property of products $u\colon Z\overset{\langle u_0, u_1\rangle}{\rightarrow} X\times Y$ corresponds to a pair of maps $u_0$, $u_1$, one sees that the objects in $\mathbf{Gl}(\sqcap)$ really correspond to spans in $Set$.

The open inclusion of $Set\times Set$ into $\mathbf{Gl}(\sqcap)$ is given by the [[geometric morphism]]

$$ i_\ast \colon Set\times Set\to \mathbf{Gl}(\sqcap) \qquad (X,Y)\mapsto ((X,Y),X\times Y,id_{X\times Y})$$

$$ i^\ast\colon \mathbf{Gl}(\sqcap)\to Set\times Set \qquad ((X,Y),Z,u)\mapsto (X,Y)$$

$$ i_{!} \colon Set\times Set\to \mathbf{Gl}(\sqcap) \qquad (X,Y)\mapsto ((X,Y),0,0\to X\times Y) \quad ,$$
 
and the closed inclusion of $Set$ by

$$ j_\ast \colon Set\to \mathbf{Gl}(\sqcap) \qquad X\mapsto ((1,1),X,X\to 1\times 1)$$

$$ j^\ast\colon\mathbf{Gl}(\sqcap)\to Set \qquad ((X,Y),Z,u)\mapsto Z\quad .$$

Since $\triangle\dashv\sqcap$ the closed inclusion is [[essential geometric morphism|essential]]:

$$ j_!\colon Set \to \mathbf{Gl}(\sqcap)\qquad X\mapsto ((X,X), X,  X\overset{\langle id_X,id_X\rangle}{\to} X\times X)\quad .$$

Since $\sqcup\dashv \triangle$ there is a somewhat surprising further left adjoint:

$$ j^\circ\colon\mathbf{Gl}(\sqcap)\to Set \qquad ((X,Y),Z,u)\mapsto X\sqcup_u Y\quad .$$

Here $ X\sqcup_u Y$ denotes the [[pushout]] of $X\overset{u_0}{\leftarrow} Z\overset{u_1}{\rightarrow} Y$ where $u_0$, $u_1$ are the pair of maps provided by $u\colon Z\overset{\langle u_0, u_1\rangle}{\rightarrow} X\times Y$ . Since a map from $((X,Y),Z,u)$ to $j_!(W)$ is a triple $(f_0,f_1,f_2)$ such that the following diagram commutes:
$$
\array{
Z & \overset{\langle u_0, u_1\rangle}{\rightarrow} & X\times Y 
\\
f_2\downarrow &  &f_0\downarrow \downarrow f_1 
\\
W & \overset{\langle id_W, id_W\rangle}{\rightarrow} & W\times W
} 
$$
$(f_0,f_1,f_2)$ has to satisfy the two conditions $f_0 u_0= f_2$ and $f_1 u_1=f_2$, or equivalently, $f_0 u_0=f_1 u_1$ . But this is the same as giving a map from $j^\circ ((X,Y),Z,u)= X\sqcup_u Y$ to $W$ by the universal property of the pushout.

Whence we get an adjoint string:

$$j^\circ\dashv j_!\dashv j^\ast \dashv j_\ast \colon Set\to \mathbb{Gl}(\sqcap)$$

with $j_!$, $j_\ast$ [[fully faithful]], exhibiting $\mathbf{Gl}(\sqcap)$ almost as a [[cohesive topos]] over $Set$. Of course, since $Set^{\bullet\leftarrow\bullet\rightarrow\bullet}$ is spatial it is not expected to satisfy all of Lawvere's axioms. In particular, the [[Nullstellensatz]] is violated since neither of the copies of $Set$ is dense in $Set^{\bullet\leftarrow\bullet\rightarrow\bullet}$.

Let $Q$ be the diagram category $N\overset{s}{\underset{t}{\rightrightarrows}} A$ underlying the topos $Set^{Q^{op}}$ of directed graphs or [[quiver|quivers]]. Consider the [[Yoneda embedding]] of the object $A$ into the presheaves: $Y(A)=Hom_Q(-,A)$. Viewed as a graph this gives the basic figure type of an _a_rrow $K_2=\bullet\to\bullet$ , the other basic figure being the _n_ode $\bullet$ given by $Y(N)$ .

The [[category of elements]] $\int_Q Y(A)$ is just the category $\bullet\rightarrow \bullet\leftarrow\bullet$ underlying the hypergraphs. Since $Y(A)$ is the representable presheaf coresponding to $A$ this is equivalent to the [[slice category]] $Q/A$. Then the following equivalence exhibits $Set^{Q^{op}}$ as an [[étendue|étendue topos]] using a general formula for [[slice topos|slices]] of [[presheaf topos|presheaf toposes]] and suggesting to view a quiver as a 'foliated' hypergraph:

$$Set^{Q^{op}}/Y(A)\simeq Set^{(Q/A)^{op}}\simeq Set^{(\int_Q Y(A))^{op}}\simeq Set^{\bullet\leftarrow\bullet\rightarrow\bullet}\quad .$$

This equivalence will be further explained in terms of graph colorings in the next section.

## Hypergraphs as 2-colored graphs

There is a classical equivalence between hypergraphs and [[vertex coloring|2-colored]] (hence [[bipartite graph|bipartite]]) graphs.  Given a hypergraph $H$, define a graph $G(H)$ whose vertex set is the [[disjoint union]] of the hypervertices and the hyperedges of $H$, and with an edge $x_v \sim x_e$ in $G(H)$ whenever the corresponding pair $(v,e)$ are incident in $H$ (creating multiple edges in the case of multiple incidence).  By coloring vertices corresponding to hypervertices in black and vertices corresponding to hyperedges in white, we satisfy the requirement that no pair of vertices sharing an edge have the same color.  Conversely, this construction is clearly reversible: any 2-colored graph $G$ determines a hypergraph $H(G)$ by interpreting black vertices as hypervertices and white vertices as hyperedges that connect all of their (black vertex) neighbors.

Giving a [[vertex coloring]] of a graph $G$ with $n$ colors is equivalent to building a graph homomorphism $G \to K_n$ into the complete graph on $n$ vertices, and so graphs equipped with a $2$-coloring are naturally organized as a [[slice]] category over $K_2$.  The classical equivalence between hypergraphs and 2-colored graphs can then be expressed formally as an [[equivalence of categories]]

$$ HGrph \cong Grph/K_2 $$

between the category of hypergraphs and the slice over $K_2$ of the category of graphs, where by the latter we mean "pseudographs" in the greatest level of generality, allowing for loops, multiple edges between vertices, and dangling half-edges (as described in [[graph#definition_in_terms_of_action_on_a_set_of_halfedges|this definition]]).  Moreover, this equivalence restricts to an equivalence

$$ SimpHGrph \cong LoopGrph/K_2 $$

where $LoopGraph$ is the category of "loop graphs", i.e., the full subcategory of $Grph$ whose objects are symmetric relations.

## Related concepts

* [[hypermap]]

* [[hyperstructure]]

* [[quiver]]

## References

* W. D&#246;rfler and D. A. Waller, _A category-theoretical approach to hypergraphs_, Archiv der Mathematik **34** no.1 (1980) pp.185-192. DOI: 10.1007/BF01224952

* W. Grilliette, _A Functorial Link between Hypergraphs and Quivers_ , Electronic J. of Combinatorics **22** (2015). ([arXiv:1608:00058](http://arxiv.org/abs/1608.00058))

* {#Law86}[[F. William Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary in TAC **9** (2005) pp.1-7. ([pdf](http://www.tac.mta.ca/tac/reprints/articles/9/tr9.pdf))

* {#Law89}[[F. William Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* T. R. S. Walsh, _Hypermaps Versus Bipartite Maps_,  Journal of Combinatorial Theory (B) **18** (1975) pp.155-163.


[[!redirects hypergraphs]]