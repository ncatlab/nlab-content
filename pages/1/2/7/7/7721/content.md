


#Contents#
* table of contents
{:toc}

## Idea


_Type II geometry_ is to [[Riemannian geometry]] as [[generalized complex geometry]] is to [[complex geometry]].

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
  T X \otimes T^* X
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
the [[tensor product]] vector bundle $T X \otimes T^* X$, and so we will
refer to this cocycle by these symbols, as indicated. 
This is also called the **[[generalized tangent bundle]]** of $X$.

=--

Therefore we may canonically consider the groupoid of 
$T X \otimes T^* X$-twisted $\mathbf{TypeII}$-structures, 
according to the general notion of [[twisted differential c-structures]].


+-- {: .num_defn }
###### Definition

A **type II generalized vielbein** on a [[smooth manifold]] $X$ is a diagram

$$
  \array{
    X &&\stackrel{\widetilde(T X \otimes T^* X)}{\to}&& \mathbf{B}(O(n) \times O(n))
    \\
    & {}_{\mathllap{T X \otimes T^* X}}\searrow &\swArrow_{E}& \swarrow_{\mathrlap{\mathbf{TypeII}}}
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
  \mathbf{H}_{/\mathbf{B} O(n,n)}(T X \otimes T^* X, \mathbf{TypeII})
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

## Application in type II supergrabity

The [[target space]] geometry for [[type II superstrings]] 
in the NS-NS sector , [[type II supergravity]], is naturally
encoded by type II geometry.

...


## Related concepts

* [[exceptional generalized geometry]]

* [[twisted smooth cohomology in string theory]]

## References

The appearance of type II geometry in [[type II string theory]] is discussed for instance in

* Ian Ellwood, _NS-NS fluxes in Hitchin's generalized geometry_ ([arXiv:hep-th/0612100](http://arxiv.org/abs/hep-th/0612100))

* Mariana Gra&#241;a, Ruben Minasian, Michela Petrini, Daniel Waldram, _T-duality, Generalized Geometry and Non-Geometric Backgrounds_ ([arXiv:0807.4527](http://xxx.lanl.gov/abs/0807.4527))
 {#GMPW}

The above formulation in terms of [[twisted smooth cohomology in string theory|twisted smooth cohomology]] is discussed in section 5 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

[[!redirects type II geometries]]

