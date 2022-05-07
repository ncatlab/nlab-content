
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Stein manifold_ is a [[complex manifold]] satisfying some niceness condition generalizing the concept of a [[domain of holomorphy]]. From the point of view of [[cohomology]] Stein manifolds are to [[complex manifolds]] as [[Cartesian spaces]] are to [[smooth manifolds]]: 

every [[complex manifold]] has a "good [[cover]]" by Stein manifolds and the positive-degree [[abelian sheaf cohomology]] with values in any analytic [[coherent sheaf]] on any Stein manifold vanishes (this is _[[Cartan's theorem B]]_, see [below](#CartanTheoremB)). This implies for instance that with respect to [[covers]] of complex manifolds by Stein manifolds usual [[Cech cohomology]] techniques work for analytic coherent sheaves (such as the [[structure sheaf]] of [[holomorphic functions]]).

Accordingly, Stein spaces are close to being the [[affine varieties]] over the [[complex numbers]], but not quite, see [below](#RelationToAffineVarieties).

## Definition

### Stein manifold

The original definition ([Stein 51](#Stein51)) says that
a _Stein manifold_  $\Sigma$ is a [[complex manifold]] which is a "holomorphically convex" and "holomorphically separable" subset of a $\mathbb{C}^n$.

This is equivalent to ([[Reinhold Remmert]], Narasimhan, Bishop) saying that $\Sigma$ admits a [[proper morphism|proper]] [[holomorphic function|holomorphic]]  [[immersion]] $\Sigma \hookrightarrow\mathbb{C}^n$.

### Stein spaces

A [[complex analytic space]] is a _Stein space_ precisely if its [[reduction modality|reduction]] is a [[Stein manifold]].

## Examples

Every [[domain of holomorphy]] in some $\mathbb{C}^n$ is a Stein manifold.

Every closed [[submanifold|sub-]][[complex manifold]] of a Stein manifold is itself Stein.

Every non-[[compact topological space|compact]] [[Riemann surface]] is a Stein manifold (by Behnke-Stein).




## Properties

### Basic properties

A Stein manifold is necessarily a non-[[compact topological space]].

### Good covers by Stein manifolds
 {#GoodCoversBySteinManifolds}

Every [[complex manifold]] admits a [[good cover]] by Stein manifolds, in the sense that all finite non-empty intersections of the cover are Stein manifolds (e.g. [Maddock 09, lemma 3.2.8](#Maddock09)), _not_ in the sense that these intersections are contractible! Rather, all Dolbeault cohomology in positive degree vanishes.

### Cohomology
 {#Cohomology}

The following central property of Stein manifolds is due to [[Henri Cartan]]

+-- {: .num_theorem #CartanTheoremB}
###### Theorem
**[[Cartan's theorem B]]**

On a Stein manifold $\Sigma$  and for $A$ an analytic [[coherent sheaf]] on $\Sigma$ then all the [[positive number|positive]]-degree [[abelian sheaf cohomology]] groups of $\Sigma$ with [[coefficients]] in $A$ vanish:

$$
  H^{\bullet \geq 1}(\Sigma, A) = 0
  \,.
$$

=--

This is recalled for instance as ([Forstneri&#269; 11, theorem 2.4.1](#Forstneric11))

+-- {: .num_theorem}
###### Theorem

Also all [[positive number|positive]]-degree [[Dolbeault cohomology]] groups vanish:

$$
  H^{\bullet, \bullet \geq 1}_{\bar \partial}(\Sigma) = 0
  \,.
$$

=--

This is recalled for instance as  ([Forstneri&#269; 11, theorem 2.4.6](#Forstneric11)).

### Relation to affine varieties
 {#RelationToAffineVarieties}

The [[analytification]] of any [[affine variety]] over the [[complex numbers]] is a Stein space, but the converse is not quite true. ([Zhang 06](#Zhang06)). There is also [some theorem by Neeman](http://mathoverflow.net/a/2087/381) to this effect.

See also at _[affine variety -- Cohomology](affine+variety#Cohomology)_.

### Oka-Grauert principle

The _[[Oka-Grauert principle]] states that for any [[Stein manifold]] $X$ the holomorphic and the topological classification of [[complex vector bundles]] on $X$ coincide. The original reference is ([Grauert 58](#Grauert)).

## Related concepts

* [[complex analytic ∞-groupoid]]

## References

The original article is 

* {#Stein51} [[Karl Stein]],  _Analytische Funktionen mehrerer komplexer Ver&#228;nderlichen zu vorgegebenen Periodizit&#228;tsmoduln und das zweite Cousinsche Problem_, Math. Ann. (in German) 123: 201&#8211;222, (1951) MR 0043219

The theory was the developed in

* {#Grauert58} [[Hans Grauert]], _Analytische Faserungen &#252;ber holomorph-vollst&#228;ndigen R&#228;umen_, Math. Ann. __135__, 263&#8211;-273 (1958) [doi](http://dx.doi.org/10.1007/BF01351803)


Reviews include

* Wikipedia, _[Stein manifold](http://en.wikipedia.org/wiki/Stein_manifold)_

* [[eom]], _[Stein space](http://www.encyclopediaofmath.org/index.php/Stein_space)_

* {#Maddock09} Zachary Maddock, _Dolbeault cohomology_, notes 2009 ([[MaddockDolbeault09.pdf:file]])


Texbook accounts include

* {#GrauertRemmert04} [[Hans Grauert]], [[Reinhold Remmert]], _Theory of Stein Spaces_, Springer-Verlag, Berlin Heidelberg, 2004.

* {#Forstneric11} [[Franc Forstnerič]], _Stein manifolds and holomorphic mappings -- The homotopy principle in complex analysis_, Springer 2011

Discussion of the relation to affine varieties includes

* {#Zhang06} Jing Zhang, _Algebraic Stein Varieties_ ([arXiv:math/0610886](http://arxiv.org/abs/math/0610886))

In relation to the [[homotopy theory|homotopy-theoretic]] [[Oka principle]]:

* {#Forstneric11} [[Franc Forstnerič]], _Stein manifolds and holomorphic mappings -- The homotopy principle in complex analysis_, Springer 2011 ([doi:10.1007/978-3-642-22250-4](https://link.springer.com/book/10.1007/978-3-642-22250-4))


As a [[site]] for [[higher complex analytic geometry]] the category of Stein manifolds appears in 

* [[Jacob Lurie]], section 4.4. of _[[Structured Spaces]]_

[[!redirects Stein manifolds]]

[[!redirects Stein space]]
[[!redirects Stein spaces]]

[[!redirects Stein domain]]
[[!redirects Stein domains]]

