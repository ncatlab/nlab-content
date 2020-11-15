


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Hypercomplex numbers
* table of contents
{: toc}

## Idea

A __hypercomplex number system__ is a [[finite-dimensional vector space|finite-dimensional]] [[nonassociative algebra|algebra]] over the [[field]] $\mathbb{R}$ of [[real numbers]].  A __hypercomplex number__ is an [[element]] of one of these algebras.


## Examples by dimension

*  There is [[the|only one]] hypercomplex number system of [[dimension]] $0$, of course.

*  There is also only one hypercomplex number system of dimension $1$, which is $\mathbb{R}$ itself.

*  Up to [[isomorphism]], there are three hypercomplex number systems of dimension $2$, each of which is a [[commutative algebra]]. Given the rule

   $$ e^2 = a + b e $$

   (for $a, b$ fixed real numbers), the algebra $\mathbb{R}[e]$ may be identified as one of these three cases by the sign of $b^2 - 4 a$.  They are:

   *  the [[complex numbers]] (elliptic case, $b^2 - 4 a \gt 0$),

   *  the [[dual numbers]] (parabolic case, $b^2 - 4 a = 0$),

   *  the [[perplex numbers]] (hyperbolic case, $b^2 - 4 a \lt 0$).

   Notice that the [[complex numbers]] have 2 distinct [[continuous function|continuous]] [[automorphisms]], given, over $\mathbb{R}$, by $e \mapsto \pm e$ (see at _[[automorphism of the complex numbers]]_).

   On the other hand, the [[ring of dual numbers]] has a continuous automorphism $e \mapsto k e$ for each $k \in \mathbb{R} \setminus \{e\}$. But the  latter space is [[homotopy equivalence|homotopy equivalent]] to two points, corresponding to the [[connected components]] of, again, $e \mapsto \pm e$. 

   Maybe $e \mapsto \pm e$ are also the two non-trivial continuous automorphisms of the [[perplex numbers]]. 

   If that is the case, one could say that the [[Euler characteristic]] of the space of continuous automorphisms of each 2d hypercomplex number systems is 2. And maybe with a bit of handwaving towards _[[groupoid cardinality]]_ one might summarize this in saying that there are 3/2 2d hypercomplex number systems.

  

*  Famous hypercomplex number systems of dimension $4$ include the [[quaternion]]s and the [[bicomplex number]]s.

*  In dimension $8$, try the [[octonion]]s and the [[biquaternion]]s.

*  In dimension $16$, try the [[sedenion]]s and the [[bioctonion]]s.

Of course, these are not the only possibilities by any means.  One can always form the [[direct product]] of two hypercomplex number systems to get a hypercomplex number systems with the sum of the dimensions.  Another way to double the dimension is to form the [[tensor product]] with any of the hypercomplex number systems of dimension $2$; in particular, [[complexification]] (the tensor product with the complex numbers) is often denoted by the prefix 'bi&#8209;'.  The [[Cayley–Dickson construction]] will double the dimension of any hypercomplex number system equipped with a (possibly trivial) involution.  Another way to generate associative hypercomplex number systems is through [[Clifford algebra]]s.

There is a thorough list of examples on [the English Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Hypercomplex_number).


[[!redirects hypercomplex number]]
[[!redirects hypercomplex numbers]]
[[!redirects hypercomplex number system]]
[[!redirects hypercomplex number systems]]
