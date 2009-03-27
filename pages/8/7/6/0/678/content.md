#Definition#

_Simplicial presheaves_ over some [[site]] $S$ are
 
* [[presheaf|Presheaves]] with values in the category [[SimpSet]] of simplicial sets, i.e., functors $S^{op} \to \Simp\Set$, i.e., functors $S^{op} \to [\Delta^{op}, \Set]$;

or equivalently, using the Hom-[[adjoint functor|adjunction]] and symmetry of the [[closed monoidal category|closed monoidal structure]] on [[Cat]]

* simplicial objects in the category of presheaves, i.e. functors $\Delta^{op} \to [S^{op},\Set]$.

#Interpretation as $\infty$-stacks#

Regarding $\Simp\Set$ as a [[model category]] using the standard [[model structure on simplicial sets]] and inducing from that a model structure on $[S^{op}, \Simp\Set]$ makes simplicial presheaves a model for $\infty$-[[infinity-stack|stacks]], as described at [[infinity-stack homotopically]].

In more illustrative language this means that a simplicial presheaf on $S$ can be regarded as an $\infty$-[[infinity-groupoid|groupoid]] (in particular a [[Kan complex]]) whose space of $n$-morphisms is modeled on the objects of $S$ in the sense described at [[space and quantity]].

#Examples#

* Notice that most definitions of $\infty$-[[infinity-category|category]] the $\infty$-category is itself defined to the a [[simplicial set]] with extra structure (in a [[geometric definition of higher category]]) or gives rise to a simplicial set under taking its [[nerve]] (in an [[algebraic definition of higher category]]). So most notions of presheaves of higher categories will naturally induce presheaves of simplicial sets.

* In particular, regarding a [[group]]s $G$ as one object categories $\mathbf{B}G$ and then taking the nerve $N(\mathbf{B}G) \in \Simp\Set$ of these (the "classifying simplicial set of the group whose [[geometric realization]] is the [[classifying space]] $\mathcal{B}G$), which is clearly a functorial operation, turns any presheaf with values in groups into a simplicial presheaf.

#Remarks#

* There are various useful [[model category]] structures on the category of simplicial presheaves. See [[model structure on simplicial presheaves]].

#References#

The theory of simplicial presheaves and of simplicial sheaves was developed by J. Jardine in a long series of articles, some of which are listed below. It's usage as a model for [[infinity-stack]]s was developed by To&#235; as described at [[infinity-stack homotopically]].

* **JardStackSSh** -- J. Jardine, _Stacks and the homotopy theory of simplicial sheaves_, Homology, homotopy and applications, vol. 3(2), 2001 p. 361-284 ([pdf](http://intlpress.com/HHA/v3/n2/a5/v3n2a5.pdf))
* **JardSimpSh** -- J. Jardine, _Fields Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))