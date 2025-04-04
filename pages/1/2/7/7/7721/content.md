
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


_Type II geometry_ (often _doubled geometry_ as in "[[double field theory]]") is to [[Riemannian geometry]] as [[generalized complex geometry]] is to [[complex geometry]].

Where the latter is the [[geometry]] induced by [[reduction of the structure group]] of the [[generalized tangent bundle]] of an even dimensional [[manifold]] along the inclusion $U(d,d) \to O(2d,2d)$ of the indefinite [[unitary group]] into the [[orthogonal group]], type II geometry is the geometry induced by reduction along the inclusion of the product of [[orthogonal group|orthogonal groups]]

$$
  O(n) \times O(n) \to O(n,n)
  \,,
$$

which is the inclusion of the [[maximal compact subgroup]] into the [[Narain group]].


This notion takes its name from the fact that it describes a good bit of the geometry of [[type II supergravity]].

## Definition

The definition of type II geometry proceeds in direct analogy with that of [[Riemannian geometry]] in terms of [[orthogonal structure]]/[[vielbein]] fields on the tangent bundle, generalized here to the [[generalized tangent bundle]]: 

1. [As a fiberwise metric on the generalized tangent bundle](#FiberwiseMetric)

1. [By reduction of the structure group of the generalized tangent bundle](#ReductionOfStructureGroup)

### By fiberwise metric on the generalized tangent bundle
 {#FiberwiseMetric}

(...)

### By reduction of the generalized tangent bundle
 {#ReductionOfStructureGroup}

We discuss how a type II geometry is the [[reduction of the structure group]] of the [[generalized tangent bundle]] along the inclusion $O(d) \times O(d) \to O(d,d)$.

+-- {: .num_defn #InclusionForTypeIIGeometry}
###### Definition

Consider  the [[Lie group]] inclusion
$$
  \mathrm{O}(d) \times \mathrm{O}(d)
  \to 
  \mathrm{O}(d,d)
$$

of those [[orthogonal group|orthogonal transformations]], that preserve the positive definite part
or the negative definite part of the [[bilinear form]] of signature $(d,d)$, respectively.

If $\mathrm{O}(d,d)$ is presented as the group of $2d \times 2d$-[[matrix|matrices]] that 
preserve the [[bilinear form]] given by the $2d \times 2d$-matrix
$$
  \eta 
  \coloneqq
  \left( 
     \array{
       0 & \mathrm{id}_d
       \\
       \mathrm{id}_d & 0
     }
  \right)
$$

then this inclusion sends a pair $(A_+, A_-)$ of [[orthogonal group|orthogonal]] $n \times n$-matrices
to the matrix
$$
  (A_+ , A_-) 
    \mapsto 
  \frac{1}{\sqrt{2}}
  \left(
    \array{
	   A_+ + A_- & A_+ - A_-
	   \\
	   A_+ - A_- & A_+ + A_-
     }
  \right)
  \,.
$$

=--

This inclusion of [[Lie groups]] induces the corresponding morphism of 
[[smooth infinity-groupoid|smooth]] [[moduli stacks]]
of [[principal bundles]]

$$
  \mathbf{TypeII}
  :
  \mathbf{B}(\mathrm{O}(d) \times \mathrm{O}(d))
  \to 
  \mathbf{B} \mathrm{O}(d,d)  
  \,.
$$

+-- {: .num_prop }
###### Proposition

There is a [[fiber sequence]] of [[smooth infinity-groupoid|smooth stacks]] 

  $$
      O(d) \backslash O(d,d) / O(d)
	 \to
  \mathbf{B}(\mathrm{O}(d) \times \mathrm{O}(d))
     \stackrel{\mathbf{TypeII}}{\to}
    \mathbf{B} \mathrm{O}(d,d)  	
  \,,
  $$

where the fiber on the left is the [[coset space]] of the [[action]] of $O(d) \times O(d)$ on $O(d,d)$.

=--

+-- {: .num_defn }
###### Definition

There is a canonical embedding
$$
  \mathrm{GL}(d) \hookrightarrow \mathrm{O}(d,d)
$$

of the [[general linear group]].

In the above matrix presentation this is given by sending

$$
  a
  \mapsto 
  \left( 
     \array{
	    a & 0
		\\
		0 & a^{-T}
      }
  \right)
  \,,
$$

where in the bottom right corner we have the [[transpose matrix|transpose]] of the inverse matrix of the invertble
matrix $a$.

=--

+-- {: .num_defn }
###### Definition

Under inclusion of def. \ref{InclusionForTypeIIGeometry}, the 
[[tangent bundle]] of a $d$-[[dimension|dimensional]] 
[[manifold]] $X$ defines an $\mathrm{O}(d,d)$-[[cocycle]]

$$
  T X \oplus T^* X
  :
  
    X 
     \stackrel{T X}{\to}
    \mathbf{B}\mathrm{GL}(d)  
      \stackrel{}{\to}
    \mathbf{B} \mathrm{O}(d,d) 
  \,.
$$

The [[vector bundle]] canonically associated to this composite cocycles may 
canonically be identified with
the [[direct sum]] vector bundle $T X \oplus T^* X$, and so we will
refer to this cocycle by these symbols, as indicated. 
This is also called the **[[generalized tangent bundle]]** of $X$.

=--

Therefore we may canonically consider the groupoid of 
$T X \oplus T^* X$-twisted $\mathbf{TypeII}$-structures, 
according to the general notion of [[twisted differential c-structures]].

More generally, instead of $E = T X \oplus T^* X$ one considers bundle [[extensions]] $E$ of the form

$$
  T^* X \to E \to T X
  \,.
$$

These may have structure froups in $O(n,n)$ but not in the inclusion $GL(n) \hookrightarrow O(n,n)$. For more on this see the section _[Geometric and non-geometric type II geometries](#GeometricAndNonGeometric)_ below. Accordingly, in all of the following $T X \oplus T^* X$ could be replaced by a more general extension $E$.

+-- {: .num_defn }
###### Definition

A **type II generalized vielbein** on a [[smooth manifold]] $X$ is a diagram

$$
  \array{
    X &&\stackrel{\widetilde(T X \oplus T^* X)}{\to}&& \mathbf{B}(O(n) \times O(n))
    \\
    & {}_{\mathllap{T X \oplus T^* X}}\searrow &\swArrow_{E}& \swarrow_{\mathrlap{\mathbf{TypeII}}}
    \\
    && \mathbf{B} O(n,n)
  }
$$

in $\mathbf{H} = $ [[Smooth∞Grpd]], hence a cocycle in the smooth [[twisted cohomology]]

$$
  E 
   \in 
  \mathbf{TypeII}Struc(X)
  \coloneqq
  \mathbf{H}_{/\mathbf{B} O(n,n)}(T X \oplus T^* X, \mathbf{TypeII})
  \,.
$$


=--

+-- {: .num_prop }
###### Proposition / Definition

  The [[groupoid]] $\mathbf{TypeII}\mathrm{Struc}(X)$
  is that of "generalized vielbein fields" on $X$, as considered for instance 
  around equation (2.24) of ([GMPW](#GMPW))
  (there only locally, but the globalization is evident).
  
  In particular, its set of equivalence classes is the set of 
  type-II generalized geometry structures on $X$.

=--

+-- {: .proof}
###### Proof

Over a local [[coordinate chart]] $\mathbb{R}^d \simeq U_i \hookrightarrow X$, the most general such generalized vielbein
(hence the most general $\mathrm{O}(d,d)$-valued function)
may be parameterized as
$$
  E = 
  \frac{1}{2}
  \left(
    \array{
	  (e_+ + e_-) + (e_+^{-T} - e_-^{-T})B & (e_+^{-T} - e_-^{-T})
	  \\
	  (e_+ - e_-) - (e_+^{-T} + e_-^{-T})B & (e_+^{-T} + e_-^{-T})
     }
  \right)
  \,,
$$

where $e_+, e_- \in C^\infty(U_i, \mathrm{O}(d))$ are thought of as two 
[[vielbein|ordinary vielbein]] fields, and where $B$ is any smooth skew-symmetric $n \times n$-matrix valued function on 
$\mathbb{R}^d \simeq U_i$. 

By an $\mathrm{O}(d) \times \mathrm{O}(d)$-[[gauge transformation]] this can always be brought
into a form where $e_+ = e_- =: \tfrac{1}{2}e$ such that
$$
  E = 
  \left(
    \array{
	  e & 0
	  \\
	  - e^{-T}B  & e^{-T}
	}
  \right)
  \,.
$$

The corresponding "generalized metric" over $U_i$ is

$$
  E^T 
  E
  = 
  \left(
    \array{
	  e^T & B e^{-1}
	  \\
	  0  & e^{-1}
    }
  \right)
  \left(
    \array{
	  e & 0
	  \\
	  - e^{-T}B  & e^{-T}
    }
  \right)
  = 
  \left(
    \array{
	  g - B g^{-1} B & B g^{-1}
	  \\
	  - g^{-1} B  & g^{-1}
     }
  \right)
  \,,
$$

where

$$
  g \coloneqq e^T e
$$

is the [[metric]] (over $\mathbb{R}^q \simeq U_i$ a smooth function with values in symmetric $n \times n$-matrices) 
given by the [[vielbein|ordinary vielbein]] $e$.

=--

### Geometric and "non-geometric" type II geometries
 {#GeometricAndNonGeometric}

+-- {: .num_defn }
###### Definition

An element in $O(d,d)$ which in the canonical matrix presentation is of the block form

$$
  e^\omega \coloneqq \left(
    \array{
      1_d & 0 
      \\
      \omega &  1_d
    }
  \right)
$$

is called a **$B$-transform**. An element of the block form

$$
  e^\beta \coloneqq \left(
    \array{
      1_d & \beta 
      \\
      0 &  1_d
    }
  \right)
$$

is called a **$\beta$-transform**. The [[subgroup]]

$$
  G_{geom}(d) \hookrightarrow O(d,d)
$$

generated by $Gl(d) \hookrightarrow O(d,d)$ and the B-transforms, hence that of matrices with vaishing top right block is called the **geometric subgroup** (e.g. [GMPW, p.5](#GMPW)). 

A type II background where the structure group of the [[generalized tangent bundle]] is not in the inclusion of the geometric subgroup is often called a **non-geometric background** (e.g. [GMPW, section 5](#GMPW)).
 
=--



## Application in type II supergravity

The [[target space]] geometry for [[type II superstrings]] 
in the NS-NS sector , [[type II supergravity]], is naturally
encoded by type II geometry.

...


## Related concepts

* [[exceptional generalized geometry]]

* [[non-geometric string theory vacua]]

* [[T-folds]]

* [[twisted smooth cohomology in string theory]]



## References

### General

The appearance of type II geometry in [[type II supergravity]]/[[type II string theory]] is discussed for instance in

* {#Ellwood07} Ian Ellwood: _NS-NS fluxes in Hitchin's generalized geometry_ &lbrack;[arXiv:hep-th/0612100](https://arxiv.org/abs/hep-th/0612100)&rbrack;

* {#GMPW} [[Mariana Graña]], [[Ruben Minasian]], Michela Petrini, [[Daniel Waldram]], _T-duality, Generalized Geometry and Non-Geometric Backgrounds_ ([arXiv:0807.4527](http://arxiv.org/abs/0807.4527))
 

The genuine reformulation of type II supergravity as a $\big(O(d)\times O(d) \hookrightarrow O(d,d)\big)$-gauge/gravity theory:

* André Coimbra, [[Charles Strickland-Constable]], [[Daniel Waldram]]: *Supergravity as Generalised Geometry I: Type II Theories*,  J. High Energ. Phys. **2011** 91 (2011). &lbrack;[arXiv:1107.1733](http://arxiv.org/abs/1107.1733), <a href="https://doi.org/10.1007/JHEP11(2011)091">doi:10.1007/JHEP11(2011)091</a>&rbrack;

In 

* [[Chris Hull]], _Generalised Geometry for M-Theory_, JHEP 0707:079,2007 ([arXiv:hep-th/0701203](http://arxiv.org/abs/hep-th/0701203)) 

the geometry of the reduction $O(d) \times O(d) \to O(d,d)$ was referred to as "type I geometry", with "type II geometry" instead referring to further [[U-duality]] group extensions, discussed at _[[exceptional generalized geometry]]_.

Review:

* [[Charles Strickland-Constable]]: *Supergravity Fluxes and Generalised Geometry*, in: Proceedings of _[[Higher Structures in M-Theory 2018]]_, Fortschritte der Physik, Special Issue **67** 8-9 &lbrack;[arXiv:1903.02842](https://arxiv.org/abs/1903.02842), [doi:10.1002/prop.201910021](https://doi.org/10.1002/prop.201910021)&rbrack;

Issues with [[higher curvature corrections]]:

* Steven Weilong Hsia, Ahmed Rakin Kamal, [[Linus Wulff]]: *No manifest T-duality at order $\alpha'{}^3$* &lbrack;[arXiv:2411.15302](https://arxiv.org/abs/2411.15302)&rbrack;



See also for [[para-Hermitian manifolds]]:

* Vincenzo Emilio Marotta, [[Richard J. Szabo]], *Born Sigma-Models for Para-Hermitian Manifolds and Generalized T-Duality*,  Reviews in Mathematical Physics **33** 09 (2021)  2150031 &lbrack;[arXiv:1910.09997](https://arxiv.org/abs/1910.09997), [doi:10.1142/S0129055X21500318](https://doi.org/10.1142/S0129055X21500318)&rbrack;


### Doubled super-geometry
  {#ReferencesDoubledSupergeometry}

Much of the discussion of type II geometry has in fact been purely bosonic, ignoring the [[super-geometry]] of [[supergravity]].

In contrast, discussion combining [[doubled geometry]] with [[super-geometry]] includes the following:

* Machiko Hatsuda, Kiyoshi Kamimura, [[Warren Siegel]], *Superspace with manifest T-duality from type II superstring*, J. High Energ. Phys.  **2014** 39 (2014) &lbrack;[arXiv:1403.3887](https://arxiv.org/abs/1403.3887), <a href="https://doi.org/10.1007/JHEP06(2014)039">doi:10.1007/JHEP06(2014)039</a>&rbrack;

* {#Bandos15} [[Igor Bandos]]: *Superstring in doubled superspace*, Physics Letters B **751** (2015) 408-412 &lbrack;[doi:10.1016/j.physletb.2015.10.081](https://doi.org/10.1016/j.physletb.2015.10.081), [arXiv:1507.07779](https://arxiv.org/abs/1507.07779)&rbrack;

* {#Cederwall16} [[Martin Cederwall]], _Double supergeometry_, J. High Energ. Phys. **2016** 155 (2016) &lbrack;[arXiv:1603.04684](https://arxiv.org/abs/1603.04684), <a href="https://doi.org/10.1007/JHEP06(2016)155">doi:10.1007/JHEP06(2016)155</a>&rbrack;

* Bojan Nikolić, Branislav Sazdović, _T-dualization of type II superstring theory in double space_, Eur. Phys. J. C **77** 3 (2017) 197 &lbrack;[arXiv:1505.06044](https://arxiv.org/abs/1505.06044), [doi:10.1140/epjc/s10052-017-4758-0](https://doi.org/10.1140/epjc/s10052-017-4758-0)&rbrack;

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:T-Duality from super Lie n-algebra cocycles for super p-branes]]*, Adv. Theor. Math. Phys **22** 5 (2018) &lbrack;[arXiv:1611.06536](https://arxiv.org/abs/1611.06536), [doi:10.4310/ATMP.2018.v22.n5.a3](https://dx.doi.org/10.4310/ATMP.2018.v22.n5.a3)&rbrack;

* Bojan Nikolić, Branislav Sazdović, _Advantage of the second-order formalism in double space T-dualization of type II superstring_ &lbrack;[arXiv:1907.03571](https://arxiv.org/abs/1907.03571)&rbrack;

* [[Chris D. A. Blair]], Ondrej Hulik, Alexander Sevrin, [[Daniel C. Thompson]]: *Doubled space and extended supersymmetry*,  J. High Energ. Phys. **2022** 119 (2022) \[<a href=" https://doi.org/10.1007/JHEP08(2022)119">doi:10.1007/JHEP08(2022)119</a>\]


See also the references on the corresponding [[super-geometry]]-enhancement of [[exceptional generalized geometry]]: _[Super-exceptional geometry -- References](exceptional+generalized+geometry#SuperExceptionalGeometryReferences)_



[[!redirects type II geometries]]


[[!redirects double geometry]]
[[!redirects doubled geometry]]

[[!redirects double geometries]]
[[!redirects doubled geometries]]

[[!redirects double supergeometry]]
[[!redirects double supergeometries]]
[[!redirects double super-geometry]]
[[!redirects double super-geometries]]

[[!redirects doubled supergeometry]]
[[!redirects doubled supergeometries]]
[[!redirects doubled super-geometry]]
[[!redirects doubled super-geometries]]



