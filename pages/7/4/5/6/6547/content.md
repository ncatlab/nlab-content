
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $X$ a [[space]] equipped with a $G$-[[connection on a bundle]] $\nabla$ (for some [[Lie group]] $G$) and for $x \in X$ any point, the [[parallel transport]] of $\nabla$ assigns to each [[curve]] $\Gamma : S^1 \to X$ in $X$ starting and ending at $x$ an element $ hol_\nabla(\gamma) \in  G$: the [[holonomy]] of $\nabla$ along that curve.

The **holonomy group** of $\nabla$ at $x$ is the subgroup of $G$ on these elements.

If $\nabla$ is the [[Levi-Civita connection]] on a [[Riemannian manifold]] and the holonomy group is a proper subgroup $H$ of the [[special orthogonal group]], one says that $(X,g)$ is a manifold of **special holonomy** .

## Properties

### Classification

[[Berger's theorem]] says that if a [[manifold]] $X$ is

* [[simply connected topological space|simply connected]]

* neither locally a product nor a [[symmetric space]]

then the possible special holonomy groups are the following

[[!include special holonomy table]]



### Relation to $G$-reductions

A manifold having special holonmy means that there is a corresponding
[[reduction of structure groups]]. 

+-- {: .num_theorem}
###### Theorem

Let $(X,g)$ be a [[connected topological space|connected]] [[Riemannian manifold]]
of [[dimension]] $n$ with [[holonomy group]]  $Hol(g) \subset O(n)$.

For $G \subset O(n)$ some other [[subgroup]], $(X,g)$ admits a torsion-free 
[[G-structure]] precisely if $Hol(g)$ is [[adjoint action|conjugate]] to 
a [[subgroup]] of $G$.

Moreover, the space of such $G$-structures is the [[coset]] $G/L$,
where $L$ is the group of elements suchthat conjugating $Hol(g)$ with them
lands in $G$.

=--

This appears as ([Joyce prop. 3.1.8](#Joyce))

## Related concepts

* [[connection on a bundle]]

  * [[connection on a 2-bundle]], [[connection on an infinity-bundle]]

* [[parallel transport]], [[higher parallel transport]]

* [[holonomy]]

  * [[holonomy group]]

  * **special holonomy**, [[reduction of structure groups]], [[G-structure]],  [[exceptional geometry]]

## References

The classification in [[Berger's theorem]] is due to

* M. Berger, _Sur les groupes d'holonomie homog&#232;ne des vari&#233;t&#233;s &#224; connexion affine et des
vari&#233;t&#233;s riemanniennes_, Bull. Soc. Math. France 83 (1955)
 {#Berger}

For more see

* [[Dominic Joyce]], _Compact manifolds with special holonomy_ , Oxford Mathematical Monogrophs (200)
  {#Joyce}

* Luis J. Boya, _Special Holonomy Manifolds in Physics_ Monograf&#237;as de la Real Academia de Ciencias de Zaragoza. 29: 37&#8211;47, (2006). ([pdf](http://www.unizar.es/acz/05Publicaciones/Monografias/MonografiasPublicadas/Monografia29/037.pdf))



[[!redirects manifold with special holonomy]]
[[!redirects manifolds with special holonomy]]

