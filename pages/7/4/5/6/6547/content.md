
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

For $X$ a [[space]] equipped with a $G$-[[connection on a bundle]] $\nabla$ (for some [[Lie group]] $G$) and for $x \in X$ any point, the [[parallel transport]] of $\nabla$ assigns to each [[curve]] $\gamma : S^1 \to X$ in $X$ starting and ending at $x$ an element $ hol_\nabla(\gamma) \in  G$: the [[holonomy]] of $\nabla$ along that curve.

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

A manifold having special holonomy means that there is a corresponding
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

This appears as [Joyce 2000, prop. 3.1.8](#Joyce00).


### Via $\mathbb{O}$-Riemannian manifolds

[[!include normed division algebra Riemannian geometry -- table]]

## Related concepts

* [[stable form]], [[definite form]]

* [[connection on a bundle]]

  * [[connection on a 2-bundle]], [[connection on an infinity-bundle]]

* [[parallel transport]], [[higher parallel transport]]

* [[holonomy]]

  * [[holonomy group]]

  * **special holonomy**, [[reduction of structure groups]], [[G-structure]],  [[exceptional geometry]], [[Walker coordinates]]

## References

### General

The classification expressed by [[Berger's theorem]] is due to:

* {#Berger} [[Marcel Berger]], _Sur les groupes d'holonomie homog&#232;ne des vari&#233;t&#233;s &#224; connexion affine et des vari&#233;t&#233;s riemanniennes_, Bull. Soc. Math. France 83 (1955)
 

For more see:

* [[Simon Salamon]], *Riemannian Geometry and Holonomy Groups*, Research Notes in Mathematics **201**, Longman (1989)

* [[Nigel Hitchin]], _Special holonomy and beyond_, Clay Mathematics Proceedings ([pdf](https://people.maths.ox.ac.uk/hitchin/hitchinlist/clay.pdf))

* {#Joyce00} [[Dominic Joyce]], *Compact manifolds with special holonomy*, Oxford Mathematical Monographs (2000) &lbrack;[ISBN:9780198506010](https://global.oup.com/academic/product/compact-manifolds-with-special-holonomy-9780198506010?cc=us&lang=en&)&rbrack;
  
* Luis J. Boya, _Special holonomy manifolds in physics_ Monograf&#237;as de la Real Academia de Ciencias de Zaragoza. 29: 37&#8211;47, (2006). ([pdf](http://www.unizar.es/acz/05Publicaciones/Monografias/MonografiasPublicadas/Monografia29/037.pdf))

Discussion of the relation to [[Killing spinors]] includes

* [[Andrei Moroianu]], [[Uwe Semmelmann]], _Parallel spinors and holonomy groups_, Journal of Mathematical Physics 41 (2000), 2395-2402 ([arXiv:math/9903062](https://arxiv.org/abs/math/9903062))

Discussion in terms of [[Riemannian geometry]] modeled on [[normed division algebras]] is in

* {#Leung02} [[Naichung Conan Leung]], _Riemannian geometry over different normed division algebras_, J. Diff. Geom. __61__:2 (2002) 289--333([euclid](https://projecteuclid.org/euclid.jdg/1090351387))

See also

* {#Freudenthal65} [[Hans Freudenthal]], _Lie groups in the foundations of geometry_, Advances in Mathematics, __1__ (1965) 145--190 ([dspace](http://dspace.library.uu.nl/handle/1874/17442))

On [[special holonomy orbifolds]]:

* [[Jeff Cheeger]], [[Gang Tian]], _Anti-self-duality of curvature and degeneration of metrics with special holonomy_, Commun. Math. Phys. __255__, 391--417 (2005) ([doi:10.1007/s00220-004-1279-0](https://doi.org/10.1007/s00220-004-1279-0))


### In supergravity and string theory

Discussion of special holonomy manifolds in [[supergravity]] and [[superstring theory]] as fiber-spaces for [[KK-compactifications]] preserving some [[number of supersymmetries]]:

* {#Gubser01} [[Steven Gubser]], _Special holonomy in string theory and M-theory_, In [[Steven Gubser]], Joseph Lykken (eds.) _Strings, Branes and Extra Dimensions - TASI 2001_, World Scientific 2004 ([arXiv:hep-th/0201114](https://arxiv.org/abs/hep-th/0201114), [doi:10.1142/5495](https://doi.org/10.1142/5495))


[[!redirects manifold with special holonomy]]
[[!redirects manifolds with special holonomy]]
[[!redirects special holonomy manifold]]

[[!redirects special holonomy orbifold]]
[[!redirects special holonomy orbifolds]]

