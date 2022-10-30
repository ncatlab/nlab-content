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

A _holonomy groupoid_ is a ([[topological groupoid|topological]]/[[Lie groupoid|Lie]]-)[[groupoid]] naturally associated with a [[foliation]] $\mathcal{F}$ of a [[manifold]] $X$. It is in some sense the smallest de-singularization of the [[leaf space]] [[quotient]] $X/\mathcal{F}$ of the foliation, which is in general not itself a manifold. Every [[foliation groupoid]] of $\mathcal{F}$ has this de-singularization property, but the holonomy groupoid is minimal with this property, in some sense.

Explicitly, given a (Riemannian) [[foliation]] $F$ on a manifold $X$, the _holonomy groupoid_ of $F$ has as objects the points of $X$. Given points $x,y$ on the same leaf, a morphism between them is the equivalence class of a path in the leaf from $x$ to $y$, where two paths are identified if they induce the same [[germ]] of a holonomy transformation on a small transversal subspace between their endpoints. If $x$ any $y$ are not on the same leaf, then there is no morphism between them.

This is naturally a [[topological groupoid]] and a [[Lie groupoid]] if done right.

The **monodromy groupoid** of the foliation is obtained from this by furthermore dividing out [[homotopy]] between paths in a leaf.



## Definition

### Foliation holonomy

Let $ (X,\mathcal{F}) $ be a foliated manifold with $ q = codim(\mathcal{F}) $. Let $ L $ be a leaf of $ \mathcal{F} $; let $ x,y \in L $ be two points; and $ T $ a transverse section through $ x $ and $ S $ a transverse section through $ y $ (hence $ S $ and $ T $ are submanifolds transversal to the leaves of $ \mathcal{F} $).

To a path $ \gamma: [0,1] \to L $ from $ x $ to $ y $, associate the [[germ]] of a (partially defined) [[diffeomorphism]]

$$
  hol(\gamma) = {hol^{S,T}}(\gamma): (T,x) \to (S,y)
$$

called the **holonomy** of the path $ \gamma $ with respect to $ S $ and $ T $, as follows.

If there exists a foliation chart $ U $ of $ \mathcal{F} $ that contains the whole path, then there exists an open [[neighbourhood]] $ A $ of $ x $ in $ T \cap U $ on which there is a smooth map $ f: A \to S $ satisfying the following conditions:

1. $ f(x) = y $;

2. For every $ x' \in A $, the point $ f(x') $ lies in the same plaque in $ U $ as $ x' $. We can choose $ A $ small so that this is an actual [[diffeomorphism]] onto its image. Then define $ {hol^{S,T}}(\gamma) $ to be the [[germ]] of this diffeomorphism:

$$
  {hol^{S,T}}(\gamma) = {germ_{x}}(f) \,.
$$

Generally, if the path $ \gamma $ does not sit within a single $ U $, then there is a decompoasition of $ \gamma $ into pieces $ \{ \gamma_{i} \}_{i=1}^{n} $ and a sequence $ U_{1},U_{2},\cdots,U_{n} $ of foliation charts such $ \gamma_{i} $ sits in $ U_{i} $. Choose transversal sections $ T_{i} $ in the double overlaps and define

$$
      hol^{S,T}(\gamma) 
  =
      {hol^{T_{i-1},T}}(\gamma_{i-1})
      \circ \cdots \circ
      hol^{T_1,T_2}(\gamma_{2})
      \circ \cdots \circ 
      hol^{S,T_1}(\gamma_{1}) \,.
$$ 

This definition is idenpendent of the choices of the $ U_{i} $'s and only depends on the initial and final transversals $ S $ and $ T $.

**Proposition**

* Two homotopic paths with the same endpoints induce the same holonomy.

* If $ S,S' $ are two transversal sections through $ x $ and $ T,T' $ two transversal sections through $ y $, then

$$
     hol^{S',T'}(\gamma)
  = 
     {hol^{T,T'}}(const_{y})
     \circ {hol^{S,T}}(\gamma) \circ {hol^{S,S'}}(const_{x}) \,.
$$

### Holonomy groupoid

Given a foliated manifold $ (\mathcal{F},X) $, the **monodromy groupoid** is the [[disjoint union]] of the [[fundamental groupoids]] of the leaves of $ \mathcal{F} $, the groupoid whose objects are the points of $ X $, which has no morphisms between points on different leaves and for which the morphisms between points on the same leaf are [[homotopy]]-classes relative endpoints between paths in the leaf.

The **holonomy groupoid** is defined analogously, where instead of identifying two paths if they are homotopic, they are identified if they induce the same holonomy transformation, in the above sense.

## References

The holonomy groupoid appears in 

* [[Charles Ehresmann]], _Structures Feuillet&#233;es_ , Proc. 5th Canadian Math. Congress, Univ. of Toronto Press 1963, 1961, pp. 109&#8211;172.

and was studied extensively in 

* H. E. Winkelnkemper, _The graph of a foliation_ , Ann. Global Anal. Geom. 1 (1983), no. 3, 51&#8211;75.

See also

* [[Marius Crainic]], [[Ieke Moerdijk]], _Foliation groupoids and their cyclic homology_ ([arXiv:math/0003119](http://arxiv.org/abs/math/0003119))

* [[Ronnie Brown]], Osman Mucuk, _Foliations, locally Lie groupoids and holonomy_ ([numdam](http://www.numdam.org/item?id=CTGDC_1996__37_1_61_0))

* Iakovos Androulidakis, [[Georges Skandalis]],  _The holonomy groupoid of a singular foliation_ ([arXiv:math/0612370](http://arxiv.org/abs/math/0612370))

[[!redirects holonomy groupoids]]

[[!redirects monodromy groupoid]]
[[!redirects monodromy groupoids]]