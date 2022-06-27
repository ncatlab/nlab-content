
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _Lie 2-group_ is the generalization of the notion of [[Lie group]] as [[group]]s are generalized to [[2-groups]]: 

it is a [[smooth 2-group]] that happens to have a model given by a [[Lie groupoid]] equipped with the structure of a [[group object]] (in general only up to [[homotopy]]). 

One general way to make the notion precise is as a special case of an [[smooth ∞-groupoid]], namely a [[1-truncated]] [[∞-group]] object in [[∞-stack]]s over the [[site]] [[CartSp]]/[[SmthMfd]], possibly with some representability condition:

these are [[stack]]s on the [[site]] of [[smooth manifold]]s (representable by [[Lie groupoid]]s and) equipped with group structure:  "group stacks" or "gr-stacks".

Special cases of this have simpler definitions. For instance a [[crossed module]] [[internal category|internal]] to [[Diff]] is a model for a strict and comparatively tame Lie 2-group.

Analogous to how the [[infinitesimal object|infinitesimal]] version of a [[Lie group]] is a [[Lie algebra]], the infinitesimal version of a Lie 2-group is a [[Lie 2-algebra]].

## Examples

* Every ordinary [[Lie group]] $G$ is in particular a Lie 2-group with $G$ as its space of [[object]]s and only [[identity morphism]]s.

* Every [[discrete infinity-groupoid|discrete]] [[2-group]] is a Lie 2-group equipped with [[discrete space|discrete smooth structure]];

* For $A$ an [[abelian group|abelian]] [[Lie group]] there is a Lie 2-group denoted $\mathbf{B}A$ or $(A \to 1)$, which has a single [[object]] and $A$ as its space of [[morphism]].

  For $A = U(1)$ the [[circle group]], the Lie 2-group $\mathbf{B}U(1)$ is the _[[circle n-group|circle 2-group]]_ .

* Every [[crossed module]] of Lie groups $(H \to G )$, $G \to Aut(H)$ gives an example of a [[strict 2-group|strict]] Lie 2-group, using the general relation between crossed modules and [[strict 2-group]]s. 

  For instance the crossed module $Spin(n) \to O(n)$. Or $(U(1) \to 1)$.
  Etc.

* The [[string 2-group]] $String(G)$ 
  has various different but equivalent incarnations
  as a Lie 2-group. One is given by the [[crossed module]]
  $\hat \Omega_* G \to P_* G$ internal to [[Frechet manifold|Frechet]]
  Lie groups.

* For $X$ a [[Lie groupoid]], its [[automorphism infinity-group]] is a smooth 2-group.

## Constructions and Applications

### Delooping 2-groupoids
 {#DeloopingLie2Groupoid}

By the discussion at [[looping and delooping]], every Lie 2-group $G$ induces a [[delooping]] [[Lie 2-groupoid]] $\mathbf{B}G$: this has a single [[object]], the space of [[morphism]]s is $G_0$, the space of [[2-morphism]]s is $G_1$ and the [[horizontal composition]] is given by the group product.

### Principal 2-bundles

For $X$ a [[smooth manifold]] (or itself a [[Lie groupoid]] such as an [[orbifold]], or generally any [[smooth ∞-groupoid]]), morphisms

$$
  g : X \to \mathbf{B}G
$$

of [[smooth ∞-groupoid]]s from $X$ to the [delooping Lie 2-groupoid](#DeloopingLie2Groupoid) $\mathbf{B}G$ classify smooth $G$-[[principal 2-bundle]]s over $X$.

If $G = AUT(H)$ is the [[automorphism 2-group]] of a [[Lie group]] $H$ then these are equivalently smooth $H$-[[gerbe]]s over $X$.

Notice that a morphism of smooth $\infty$-groupoids $X \to \mathbf{B}G$ is presented by an [[infinity-anafunctor|2-anafunctor]] of 2-groupoid valued presheaves, given by a [[span]]

$$
  \array{
     C(U_i) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\simeq}
     \\
     X
  }
 \,,
$$

where $C(U_i)$ is the [[Cech nerve]] 2-groupoid of some [[covering]]. The top morphism here encodes degree-1 [[nonabelian cohomology|nonabelian]] [[Cech cohomology|Cech]] [[hypercohomology]] with coefficients in $G$. 


## Related concepts

* [[group]], [[Lie group]], [[Lie groupoid]]

* [[2-group]], **Lie 2-group**, [[Lie 2-groupoid]]

  * [[Poisson Lie 2-group]]

* [[∞-group]], [[smooth ∞-group]], [[smooth ∞-groupoid]]

## References

A first exposition is in the lecture notes

* Alissa Crans, _A survey of higher Lie theory_ ([pdf](http://myweb.lmu.edu/acrans/SurveyHigherLieTheory.pdf))

A general review of Lie 2-groups, as well as a discussion of the example of the [[string 2-group]] is in 

* [[John Baez]], Alissa Crans, [[Urs Schreiber]], [[Danny Stevenson]], _From Loop Groups to 2-Groups_ ([arXiv:math/0504123](http://arxiv.org/abs/math/0504123))

Discussion in a more comprehensive context is in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

with an introduction in section 1.3.1 and a general abstract discussion in 3.3.2.

On the [[cohomology]] of Lie 2-groups:

* [[Grégory Ginot]], [[Ping Xu]], _Cohomology of Lie 2-groups_ ([pdf](http://people.math.jussieu.fr/~ginot/papers/CohLie2gp.pdf))

* [[Christoph Wockel]],  _Categorified central extensions, &#233;tale Lie 2-groups and Lie&#700;s Third Theorem for locally exponential Lie algebras_ ([web](http://www.sciencedirect.com/science/article/pii/S0001870811002313))

* [[Chris Schommer-Pries]], _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ ([arXiv](http://arxiv.org/abs/0911.2483))

[[!redirects Lie 2-groups]]