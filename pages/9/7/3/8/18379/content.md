[[!redirects category of simple graphs and graph theory]]
[[!redirects category of simple graphs and some graph-theoretical questions]]
[[!redirects the category of simple graphs from a graph-theoretic perspective]]
Graph theory studies both full and wide subcategories of the category SimpGph defined in [[category of simple graphs]]. 
(Needless to say, other categories of graphs have and will be used, but this page focuses on SimpGph.)

#### Wide subcategories

Definition \ref{threeWideSubcategories} gives three examples of wide subcategories, the definitons being graph-theoretic, the names immediately chosen to be category-theoretic, for systematic reasons.

+-- {: .num_defn #threeWideSubcategories}
###### Definition 

Let MonoSimpGph, RegMonoSimpGph, and IsomeRegMonoSimpGph be the wide subcategories of SimpGph with the following hom-sets:

MonoSimpGph($G_0,G_1$) $:=$  $\{$ $f$ $\in$ SimpGph$(G_0,G_1)$: the function $f$ is injective $\}$,

RegMonoSimpGph($G_0,G_1$) $:=$  $\{$ $f$ $\in$ SimpGph$(G_0,G_1)$: $f$ is a graph-isomorphism onto its image $\}$,

IsomeRegMonoSimpGph($G_0,G_1$) $:=$ $\{$ $f$ $\in$ SimpGph$(G_0,G_1)$: $f$ is a graph-isomorphism onto its image, and, for any $x,y\in V$ we have $\mathrm{dist}_{\mathrm{im}(f)}(f(x),f(y))=\mathrm{dist}_{G_1}(f(x),f(y))\}$.

(Here $\mathrm{dist}_G\colon V\times V\rightarrow\omega$ denotes the function which takes any pair of vertices to the length of a shortest graph-theoretic path with these endpoints.)


 =--

Closedness under composition of each of the three subclasses of $\mathrm{Mor}(SimpGph)$ defined by Definition \ref{threeWideSubcategories} is immediate from the respective definitions. 




Evident remarks: 

* Each of MonoSimpGph, RegMonoSimpGph, IsomeRegMonoSimpGph are [[concrete categories]]. (because of Proposition \ref{EmbeddingOfSimpGphIntoSet}) 

*  There are the class inclusions (of which the first would be false for multigraphs),

Mor(IsomeRegMonoSimpGph) $\subset$ Mor(RegMonoSimpGph) $\subset$ Mor(MonoSimpGph) $=$ Monos(SimpGph).

* Because of the latter equality, each of MonoSimpGph, RegMonoSimpGph, IsomeRegMonoSimpGph is a [[left cancellative category]]. (And none is a groupoid or a preorder.)


* None of 
MonoSimpGph, RegMonoSimpGph, IsomeRegMonoSimpGph has any [[terminal object]].

* The relation $(\emptyset,\emptyset)$, which is symmetric and reflexive, is the (only) initial object of each of MonoSimpGph, RegMonoSimpGph, IsomeRegMonoSimpGph, because this is the only initial object of SimpGph. 


We now explain the names of the three subcategories. 

* It is evident (using the functor $\Gamma$ from the Proposition [here](/nlab/show/category+of+simple+graphs#EmbeddingOfSimpGphIntoSet) that the morphisms of Simp.Gph.Monos are indeed precisely the [[monos]] of SimpGph. 
 
* How to get from the _definition_ of RegMonoSimpGph given in Definition \ref{threeWideSubcategories} to [[regular monomorphism]]s? Answer: directly by definition of _graph-isomorphism_, Definition \ref{threeWideSubcategories} says that the morphisms $f$ of RegMonoSimpGph are those for which the vertex-set $\mathrm{im}(\Gamma(f))$, with $\Gamma$ from Proposition \ref{EmbeddingOfSimpGphIntoSet}, induces a graph isomorphic to the graph $\mathrm{dom}(f)$. Therefore, these morphisms are those injective graph homomorphisms whose image is an _induced_ subgraph of the target. Further, the term used in the nLab instead of _induced_ is _full_, so the question reduces to why the morphisms $f$ of $SimpGph$ with the two properties that (1) $\Gamma(f)$ is injective and (2) the graph $im(f)$ is a full subgraph of $\mathrm{cod}(f)$, are the regular monos; but sufficient explanations for this _have already been given_ in Section "Equalizers and coequalizers" of [[category of simple graphs]].

* By definition of IsomeRegMonoSimpGph, for each morphism of that subcategory, the graph im($f$) is what in graph theory usually is called an _isometric subgraph_. 

Isometric subgraphs have several uses in graph-theoretical considerations, which to describe here would take us too far afield.

## References 

* [[Hans-Jürgen Bandelt, Victor Chepoi]], Metric graph theory and geometry: a survey. Contemporary Mathematics, Volume 453, 2008, 
{#BandeltChepoi2008}