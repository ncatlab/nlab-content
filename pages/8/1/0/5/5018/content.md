+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _holonomy groupoid_ is a ([[topological groupoid|topological]]/[[Lie groupoid|Lie]]-) [[groupoid]] naturally associated with a [[foliation]] $ \mathcal{F} $ of a [[manifold]] $ X $. It is, in some sense, the smallest de-singularization of the [[leaf space|leaf-space]] [[quotient]] $ X/\mathcal{F} $ of the foliation, which is, in general, not a manifold itself. Every [[foliation groupoid]] of $ \mathcal{F} $ has this de-singularization property, but the holonomy groupoid is, in some sense, minimal with respect to this property.

Explicitly, given a [[foliation]] $ \mathcal{F} $ on a manifold $ X $, the _holonomy groupoid_ of $ \mathcal{F} $ has as objects the points of $ X $. Given points $ x,y $ in the same leaf, a morphism between them is the equivalence class of a path in the leaf from $ x $ to $ y $, where two paths are identified if they induce the same [[germ]] of a holonomy transformation between small transversal sections through $ x $ and $ y $. If $ x $ and $ y $ are not in the same leaf, then there is no morphism between them.

This is naturally a [[topological groupoid]] and a [[Lie groupoid]] if done right.

The **monodromy groupoid** of the foliation is obtained from this by further dividing out the [[homotopy]] between paths in a leaf.

## Definition

### Foliation Holonomy

Let $ (X,\mathcal{F}) $ be a foliated manifold with $ q = codim(\mathcal{F}) $. Let $ L $ be a leaf of $ \mathcal{F} $; let $ x,y \in L $ be two points; and let $ S $ and $ T $ be transversal sections through $ x $ and $ y $ respectively (i.e., $ S $ and $ T $ are sub-manifolds transversal to the leaves of $ \mathcal{F} $).

To a path $ \gamma: [0,1] \to L $ from $ x $ to $ y $, we assign the [[germ]] of a (partially defined) [[diffeomorphism]]

$$
{hol^{S,T}}(\gamma): (S,x) \to (T,y),
$$

called the **holonomy transformation** of the path $ \gamma $ with respect to $ S $ and $ T $, as follows:

If there exists a single foliation chart $ U $ of $ \mathcal{F} $ that contains the image of $ \gamma $, then there exists a sufficiently small open [[neighbourhood|neighborhood]] $ A $ of $ x $ in the space $ S \cap U $ for which there exists a unique smooth map $ f: A \to T $ satisfying the following conditions:

* $ f(x) = y $;

* For every $ a \in A $, the point $ f(a) $ lies in the same plaque in $ U $ as $ a $. Observe that $ f $ is a [[diffeomorphism]] onto its image.

Then define $ {hol^{S,T}}(\gamma) $ to be the [[germ]] of this diffeomorphism at $ x $:

$$
{hol^{S,T}}(\gamma) \stackrel{def}{=} {germ_{x}}(f).
$$

In general, the image of $ \gamma $ is not contained inside any single foliation chart $ U $, but as it is a compact subspace of $ X $, there exist finitely many foliation charts $ U_{1},\ldots,U_{n+1} $ and numbers $ t_{0},\ldots,t_{n+1} $ such that

* $ 0 = t_{0} \lt t_{1} \lt \cdots \lt t_{n} \lt t_{n+1} = 1 $ and

* $ \gamma([t_{i-1},t_{i}]) $ is contained in $ U_{i} $ for $ i = 1,\ldots,n+1 $.

Then arbitrarily choose transversal sections $ T_{i} $ through $ \gamma(t_{i}) $ for $ i = 1,\ldots,n $ and define

$$
{hol^{S,T}}(\gamma) \stackrel{def}{=}
{hol^{T_{n},T}} \left( \gamma|_{[t_{n},t_{n+1}]} \right) \circ
{hol^{T_{n-1},T_{n}}} \left( \gamma|_{[t_{n-1},t_{n}]} \right) \circ \cdots \circ
{hol^{T_{1},T_{2}}} \left( \gamma|_{[t_{1},t_{2}]} \right) \circ
{hol^{S,T_{1}}} \left( \gamma|_{[0,t_{1}]} \right).
$$ 

This definition is independent of the choice of $ U_{i} $'s, $ t_{i} $'s and $ T_{i} $'s. It only depends on the initial and final transversal sections $ S $ and $ T $.

**Proposition**

* Two homotopic paths with the same endpoints induce the same holonomy. (Note, however, that the converse is not true. Two paths with the same endpoints inducing the same holonomy may not be homotopic.)

* If $ S,S' $ are two transversal sections through $ x $ and $ T,T' $ two transversal sections through $ y $, then

$$
hol^{S',T'}(\gamma)
= 
{hol^{T,T'}}(const_{y}) \circ {hol^{S,T}}(\gamma) \circ {hol^{S',S}}(const_{x}).
$$

### Holonomy Groupoid

Given a foliated manifold $ (X,\mathcal{F}) $, the **monodromy groupoid** is the [[disjoint union]] of the [[fundamental groupoids]] of the leaves of $ \mathcal{F} $, which is the groupoid having the following properties:

1. Its objects are the points of $ X $.

2. There are no morphisms between two points on different leaves.

3. The morphisms between two points on the same leaf are [[homotopy]]-classes of paths lying in the leaf joining those points.

The **holonomy groupoid** is defined analogously, where instead of identifying two paths if they are homotopic, they are identified if they induce the same holonomy as described above.

## References

The holonomy groupoid appears in 

* [[Charles Ehresmann]], _Structures Feuillet&#233;es_ , Proc. 5th Canadian Math. Congress, Univ. of Toronto Press 1963, 1961, pp. 109&#8211;172.

and was studied extensively in 

* H. E. Winkelnkemper, _The graph of a foliation_ , Ann. Global Anal. Geom. 1 (1983), no. 3, 51&#8211;75.

See also

* [[Marius Crainic]], [[Ieke Moerdijk]], _Foliation groupoids and their cyclic homology_, [arXiv:math/0003119](http://arxiv.org/abs/math/0003119)

* [[Ronnie Brown]], Osman Mucuk, _Foliations, locally Lie groupoids and holonomy_, [numdam](http://www.numdam.org/item?id=CTGDC_1996__37_1_61_0)

Applications to singular foliations and to Poisson manifolds in particular are in

* Iakovos Androulidakis, [[Georges Skandalis]],  _The holonomy groupoid of a singular foliation_, [arXiv:math/0612370](http://arxiv.org/abs/math/0612370)
* Iakovos Androulidakis, Marco Zambon, _Almost regular Poisson manifolds and their holonomy groupoids_, [arxiv/1606.09269](http://arxiv.org/abs/1606.09269)

[[!redirects holonomy groupoids]]

[[!redirects monodromy groupoid]]
[[!redirects monodromy groupoids]]