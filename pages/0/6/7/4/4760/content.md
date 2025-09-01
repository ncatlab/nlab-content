[[!redirects Geometric nerve of a bicategory]]
[[!redirects Duskin nerve]]
[[!redirects Duskin nerves]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The (unitary) _geometric nerve_ is a natural  [[nerve]] operation on [[bicategories]]. It is a [[functor]] from [[BiCat]] to [[sSet]]. This is also sometimes called the _Duskin nerve_. The  notion is implicit in work by R. Street (1987). The direct approach was used by Duskin in work at about the same time, as explained in both articles. (Duskin's article directly on the idea was published in 2002.) 

The construction, thus, yields a functor:

$$
  N : BiCat_{NLax} \to sSet
  \,.
$$

extending the ordinary nerve construction on the category of small categories, where morphisms of BiCat are _normal lax 2-functors_: these are the lax 2-functors which strictly preserve identities. 

Special cases of the construction relate to earlier constructions relating to the [[homotopy coherent nerve]], see below for more detail.


## Definition

We may think of the [[simplex category]] $\Delta$ as the [[full subcategory]] of [[Cat]] on the categories free on non-empty finite linear graphs. This gives the canonical inclusion $\Delta \hookrightarrow Cat$ that defines the ordinary nerve of categories. 

There is also the canonical embedding of categories into bicategories. Combined this gives the inclusion 

$$
  \Delta \hookrightarrow Cat \hookrightarrow BiCat
  \,.
$$

The bicategorical nerve is the nerve induced from that. So for $C$ a bicategory we have

$$
  N(C) : [k] \mapsto BiCat_{NLax}(\Delta[k], C)
  \,.
$$

There are also an oplax version and two non-normalized versions.
 
## Properties

* The [[simplicial set]]s in the image of the geometric nerve are 3-[[coskeletal]].

* The geometric nerve identifies precisely [[bigroupoid]]s with 2-[[hypergroupoid]]s: those [[Kan complexes]] for which the horn fillers in dimension $\geq 3$ are _unique_ . (Theorem 8.6 in ([Duskin 2002](#Duskin02)))  

(This shows in particular that bigroupoids model all [[homotopy 2-type]]s.)

* The nerve is a full and faithful functor $BiCat_{NLax}\to sSet$.

## Example

Any [[strict 2-category]] determines both a 'bicategory' in the above sense (since a 'strict' thing is also a 'weak' one)  and a simplicially enriched category.  The latter is found by taking the nerve of each 'hom-category'.  The Duskin nerve of a 2-category is the same as the [[homotopy coherent nerve]] of the corresponding $sSet$-category.  This can also be applied to [[2-groupoid]]s and, thus, results in a classifying space construction for [[crossed module]]s. 

## Picturing the Duskin nerve
Following ([Johnson–Yau, Section 5.4](#JohnsonYau20)), one may picture the Duskin nerve $N(\mathcal{C})$ of a bicategory $(\mathcal{C},1^{\mathcal{C}},\circ_{\mathcal{C}},\alpha^{\mathcal{C}},\lambda^{\mathcal{C}},\rho^{\mathcal{C}})$ as follows:

1. The $0$-simplices of $N(\mathcal{C})$ are the objects of $\mathcal{C}$;

2. The $1$-simplices of $N(\mathcal{C})$ are the $1$-morphisms of $\mathcal{C}$;

3. The $2$-simplices of $N(\mathcal{C})$ are quadruples $(i,j,k,\theta)$ as in the diagram

   [[2-simplex-of-NC.svg:pic]]
   where $A,B,C\in\mathrm{Obj}(\mathcal{C})$, $i,j,k\in\mathrm{Mor}_1(\mathcal{C})$ and $\theta\colon j\circ i\Rightarrow k$ is a $2$-morphism of $\mathcal{C}$;
4. The $3$-simplices of $N(\mathcal{C})$ are $14$-tuples 
   $$(A_{0},A_{1},A_{2},A_{3},f_{01},f_{02},f_{03},f_{12},f_{13},f_{23},\theta_{012},\theta_{013},\theta_{023},\theta_{123})$$
   as in the diagram
   [[3-simplex-of-NC.svg:pic]]
   such that we have an equality
   [[3-simplex-of-NC-equality-of-pasting-diagrams.svg:pic]]
   of pasting diagrams in $\mathcal{C}$;
5. The $n$-simplices of $N(\mathcal{C})$ consist of

   * A collection $\{A_{i}\}_{0\leq i\leq n}$ of objects of $\mathcal{C}$,
   * A collection $\{f_{ij}\colon A_{i}\longrightarrow A_{j}\}_{0\leq i\lt j\leq n}$ of $1$-morphisms of $\mathcal{C}$, and
   * A collection $\{\theta_{ijk}\colon f_{jk}\circ f_{ij}\Rightarrow f_{ik}\}_{0\leq i\lt j\lt k\leq n}$ of $2$-morphisms of $\mathcal{C}$

   such that, for each $i,j,k\in\mathbb{N}$ with $0\leq i\lt j\lt k\leq n$, we have an equality
   [[n-simplex-of-NC-equality-of-pasting-diagrams.svg:pic]]
   of pasting diagrams in $\mathcal{C}$;
6. The degeneracy map
   $$\mathrm{s}^{0}_{0}\colon N_{0}(\mathcal{C})\longrightarrow N_{1}(\mathcal{C})$$
   of $N(\mathcal{C})$ in degree $0$ is the map sending a $0$-simplex $A$ of $N(\mathcal{C})$ (i.e. an object $A$ of $\mathcal{C}$) to the $1$-simplex $\mathrm{id}_{A}\colon A\to A$.
7. The degeneracy maps
   $$
   \mathrm{s}^{1}_{0} \colon N_{1}(\mathcal{C})\longrightarrow N_{2}(\mathcal{C}),
   $$
   $$
   \mathrm{s}^{1}_{1} \colon N_{1}(\mathcal{C})\longrightarrow N_{2}(\mathcal{C}),
   $$
   of $N(\mathcal{C})$  in degree $1$ are the maps described as follows: given a $1$-simplex $\sigma=(A\xrightarrow{f}B)$ of $N(\mathcal{C})$, we have
   [[deg-1-degeneracies-of--duskin-nerve.svg:pic]]
8. The degeneracy maps in degree $2$
   $$
   \mathrm{s}^{2}_{0} \colon N_{2}(\mathcal{C})\longrightarrow N_{3}(\mathcal{C}),
   $$
   $$
   \mathrm{s}^{2}_{1} \colon N_{2}(\mathcal{C})\longrightarrow N_{3}(\mathcal{C}),
   $$
   $$
   \mathrm{s}^{2}_{2} \colon N_{2}(\mathcal{C})\longrightarrow N_{3}(\mathcal{C}),
   $$
   of $N(\mathcal{C})$  in degree $2$ are the maps described as follows: given a $2$-simplex
   [[2-simplex-duskin-sigma.svg:pic]]
   of $N(\mathcal{C})$, we have
   [[deg-2-degeneracies-duskin-new.svg:pic]]
9. The face maps
   $$
   \mathrm{d}^{1}_{0} \colon N_{1}(\mathcal{C})\longrightarrow N_{0}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{1}_{1} \colon N_{1}(\mathcal{C})\longrightarrow N_{0}(\mathcal{C}),
   $$
   of $N(\mathcal{C})$ in degree $1$ are given by
   $$\mathrm{d}^{1}_{0}(A\xrightarrow{f}B)=B$$
   $$\mathrm{d}^{1}_{1}(A\xrightarrow{f}B)=A$$
10. The face maps
   $$
   \mathrm{d}^{2}_{0} \colon N_{2}(\mathcal{C})\longrightarrow N_{1}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{2}_{1} \colon N_{2}(\mathcal{C})\longrightarrow N_{1}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{2}_{1} \colon N_{2}(\mathcal{C})\longrightarrow N_{1}(\mathcal{C}),
   $$
   of $N(\mathcal{C})$ in degree $2$ are described as follows: given a $2$-simplex
   [[2-simplex-duskin-sigma.svg:pic]]
   of $N(\mathcal{C})$, we have
   [[face-maps-deg-2-duskin.svg:pic]]
11. The face maps
   $$
   \mathrm{d}^{3}_{0} \colon N_{3}(\mathcal{C})\longrightarrow N_{2}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{3}_{1} \colon N_{3}(\mathcal{C})\longrightarrow N_{2}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{3}_{2} \colon N_{3}(\mathcal{C})\longrightarrow N_{2}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{3}_{3} \colon N_{3}(\mathcal{C})\longrightarrow N_{2}(\mathcal{C}),
   $$
   of $N(\mathcal{C})$ in degree $3$ are described as follows: given a $3$-simplex
   [[3-simplex-duskin.svg:pic]]
   of $N(\mathcal{C})$, we have
   [[face-maps-deg-3-duskin.svg:pic]]
12. The face maps
   $$
   \mathrm{d}^{4}_{0} \colon N_{4}(\mathcal{C})\longrightarrow N_{3}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{4}_{1} \colon N_{4}(\mathcal{C})\longrightarrow N_{3}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{4}_{2} \colon N_{4}(\mathcal{C})\longrightarrow N_{3}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{4}_{3} \colon N_{4}(\mathcal{C})\longrightarrow N_{3}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{4}_{4} \colon N_{4}(\mathcal{C})\longrightarrow N_{3}(\mathcal{C}),
   $$
   of $N(\mathcal{C})$ in degree $4$ are described as follows: given a $4$-simplex $\sigma$ of $N(\mathcal{C})$ as in the diagram
   [[4-simplex-duskin.svg:pic]]
   we have
   \begin{imagefromfile}
       "file_name": "face-maps-deg-4-duskin-new2.svg"
   \end{imagefromfile}


## Related concepts

* [[nerve]]

* **geometric nerve of a bicategory**

* [[geometric nerve of a tricategory]]

* [[∞-nerve]]

* [[homotopy coherent nerve]]



## References

* [[Ross Street]]: _The algebra of oriented simplexes_, Journal of Pure and Applied Algebra **49** 3 (1987) 283-335

* {#Duskin02} [[John Duskin]]: _Simplicial matrices and the nerves of weak n-categories I: nerves of bicategories_, Theory and Applications of Categories **9** 10 (2002) 198-308 &lbrack;[tac:9-10](http://www.tac.mta.ca/tac/volumes/9/n10/9-10abs.html)&rbrack;

* V. Blanco, M. Bullejos, E. Faro, _A Full and faithful Nerve for 2-categories_, Applied Categorical Structures **13** 3 (2005) 223-233 &lbrack;[arxiv:math/0406615](http://arxiv.org/abs/math/0406615)&rbrack;

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], *2-Dimensional Categories*, Oxford University Press (2021) &lbrack;[arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378)&rbrack;

[[!redirects bicategory nerve]]
[[!redirects nerve of bicategories]]
[[!redirects nerves of bicategories]]

[[!redirects nerve of a bicategory]]

[[!redirects simplicial nerve of a 2-category]]
[[!redirects simplicial nerve of 2-categories]]



