
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _formal group_ is a [[group object]] [[internalization|internal to]] [[infinitesimal space]]s. More general than [[Lie algebra]]s, which are group objects in _first order infinitesimal_ spaces, formal groups may be of arbitrary infinitesimal order. They sit between [[Lie algebras]] and finite [[Lie groups]] or [[algebraic groups]].

Since [[infinitesimal spaces]] are typically modeled as [[Isbell duality|formal duals]] to [[algebras]], formal groups are typically conceived as group objects in formal duals to [[formal power series]] algebras.

Specifically, fixing a formal [[coordinate]] chart, then the product operation of a formal group is entirely expressed as a [[formal power series]] in two variables, satisfying conditions. This is called a _formal group law_, a concept that goes back to Bochner and [[Daniel Lazard|Lazard]].

Commutative formal group laws of dimension 1 notably appear in [[algebraic topology]] (originating in work by [[Sergei Novikov|Novikov]], [[Victor Buchstaber|Buchstaber]] and [[Daniel Quillen|Quillen]], see [Adams 74, part II](#Adams74)), where they express the behaviour of [[complex oriented cohomology theories]] evaluated on infinite [[complex projective space]] (i.e. on the [[classifying space]] $B U(1) \simeq \mathbb{C}P^\infty$). In particular [[complex cobordism]] cohomology theory in this context gives the universal formal group law represented by the [[Lazard ring]]. The [[height of a formal group|height of formal groups]] induces a filtering on [[complex oriented cohomology theories]] called the _[[chromatic homotopy theory|chromatic filtration]]_.

More recently [[Fabien Morel|Morel]] and [[Marc Levine]] consider the [[algebraic cobordism]] of smooth schemes in [[algebraic geometry]].  Formal groups are also useful in local [[class field theory]]; they can be used to explicitly construct the local Artin map according to Lubin and Tate.


### Formal group laws
 {#FormalGroupLaw}

+-- {: .num_defn #AdicRing}
###### Definition

An (commutative) [[adic ring]] is a ([[commutative ring|commutative]]) [[topological ring]] $A$ and an ideal $I \subset A$ such that

1. the [[topological space|topology]] on $A$ is the $I$-[[adic topology]];

1. the canonical morphism

   $$
     A \longrightarrow \underset{\longleftarrow}{\lim}_n (A/I^n)
   $$

   to the [[limit]] over [[quotient rings]] by powers of the ideal is an [[isomorphism]].

A [[homomorphism]] of adic rings is a ring [[homomorphism]] that is also a [[continuous function]] (hence a function that preserves the filtering $A \supset \cdots \supset A/I^2 \supset A/I $). This gives a category $AdicRing$ and a subcategory $AdicCRing$ of commutative adic rings.

The [[opposite category]] of $AdicRing$ (on [[Noetherian rings]]) is that of affine [[formal schemes]].

Similarly, for $R$ any fixed [[commutative ring]], then adic rings under $R$ are _adic $R$-algebras_. We write $Adic R Alg$ and $Adic R CAlg$ for the corresponding categories.

=--

+-- {: .num_example #PowerSeriesAlgebra}
###### Example

For $R$ a [[commutative ring]] and $n \in \mathbb{N}$ then the [[formal power series ring]]

$$
  R[ [ x_1, x_2, \cdots, x_n ] ]
$$

in $n$ [[variables]] with [[coefficients]] in $R$ and equipped with the ideal

$$
  I = (x_1, \cdots , x_n)
$$

is an adic ring (def. \ref{AdicRing}).

=--

+-- {: .num_prop }
###### Proposition

There is a [[fully faithful functor]]

$$
  AdicRing \hookrightarrow ProRing
$$

from [[adic rings]] (def. \ref{AdicRing}) to [[pro-rings]], given by 

$$
  (A,I) \mapsto ( (A/I^{\bullet}))
  \,,
$$

i.e. for $A,B \in AdicRing$ two adic rings, then there is a [[natural isomorphism]]

$$
  Hom_{AdicRing}(A,B)
    \simeq
   \underset{\longleftarrow}{\lim}_{n_2}
   \underset{\longrightarrow}{\lim}_{n_1}
   Hom_{Ring}(A/I^{n_1},B/I^{n_2})
  \,.
$$

=--

+-- {: .num_defn #GroupObjectFormalGroupLaw}
###### Definition

For $R \in CRing$ a [[commutative ring]] and for $n \in \mathbb{N}$, a **formal group law** of dimension $n$ over $R$ is the structure of a [[group object]] in the category $Adic R CAlg^{op}$ from def. \ref{AdicRing} on the object $R [ [x_1, \cdots ,x_n] ]$ from example \ref{PowerSeriesAlgebra}.

Hence this is a morphism

$$
  \mu
  \;\colon\;
  R[ [ x_1, \cdots, x_n ] ]
   \longrightarrow
  R [ [ x_1, \cdots, x_n, \, y_1, \cdots, y_n ] ] 
$$

in $Adic R CAlg$ satisfying unitality, associativity.

This is a **commutative formal group law** if it is an abelian group object, hence if it in addition satisfies the corresponding commutativity condition.

=--

This is equivalently a set of $n$ power series $F_i$ of $2n$ variables $x_1,\ldots,x_n,y_1,\ldots,y_n$ such that (in notation $x=(x_1,\ldots,x_n)$, $y=(y_1,\ldots,y_n)$, $F(x,y) = (F_1(x,y),\ldots,F_n(x,y))$) 

$$
  F(x,F(y,z))=F(F(x,y),z)
$$

$$
  F_i(x,y) = x_i+y_i+\,\,higher\,\,order\,\,terms
$$


+-- {: .num_example #Commutative1DimFormalGroupLaw}
###### Example

A 1-dimensional commutative formal group law according to def. \ref{GroupObjectFormalGroupLaw} is equivalently a [[formal power series]]

$$
  \mu(x,y)
  =
  \underset{i,j \geq 0}{\sum} a_{i,j} x^i y^j
$$

(the [[image]] under $\mu$ in $R[ [ x,y ] ]$ of the element $t \in R [ [ t ] ]$) such that


1. (unitality) 

   $$
     \mu(x,0) = x$ and $\mu(0,x) = x
     \,;
   $$

1. (associativity) 

   $$
     \mu(x,\mu(y,z)) = \mu(\mu(x,y),z)
     \,;
   $$

1. (commutativity) 
  
   $$
     \mu(x,y) = \mu(y,x)
     \,.
   $$

The first condition means equivalently that 

$$
  a_{i,0} 
    = 
  \left\{
    \array{
      1 & if \; i = 1
      \\
      0 & otherwise 
    }
  \right.
  \;\;\;\;\,,
  \;\;\;\;\;
  a_{0,i} 
    = 
  \left\{
    \array{
      1 & if \; i = 1
      \\
      0 & otherwise 
    }
  \right.
  \,.
$$

Hence $\mu$ is necessarily of the form

$$
  \mu(x,y)
   \;=\;
   x + y + \underset{i,j \geq 1}{\sum} a_{i,j} x^i y^j
  \,.
$$

The existence of inverses is no extra condition: by [[induction]] on the index $i$ one finds that there exists a unique 

$$
  \iota(x) = \underset{i \geq 1}{\sum} \iota(x)_i x^i
$$

such that 

$$
  \mu(x,\iota(x)) = 0
  \;\;\;\,,
  \;\;\;
  \mu(\iota(x),x) = 0
  \,.
$$

Hence 1-dimensional formal group laws over $R$ are equivalently [[monoids]] in $Adic R CAlg^{op}$ on $R[ [ x ] ]$.

=--

+-- {: .num_example} 
###### Example 
Any [[power series]] of the form $f(x) = x + a_2 x^2 + a_3 x^3 + \ldots$ in $R[ [x] ]$ has a functional or compositional inverse $f^{-1}(x)$ in the monoid $x R[ [x] ]$ under composition. Thus we may define a 1-dimensional formal group law by the formula $\mu(x, y) = f^{-1}(f(x) + f(y))$. That this is in some sense the typical way that 1-dimensional formal group laws arise is the content of [[Lazard ring|Lazard's theorem]]. 
=-- 



### Formal group schemes

Much more general are **formal group schemes** from ([Grothendieck](#Grothendieck))


__Formal group schemes__ are simply the [[group object]]s in a category of [[formal schemes]]; however usually only the case of the formal spectra of complete $k$-algebras is considered; this category is equivalent to the category of complete cocommutative $k$-[[Hopf algebras]]. 

### Formal groups over an operad

For a generalization over [[operads]] see ([Fresse](#Fresse)).



## Properties

### In characteristic 0

+-- {: .num_prop}
###### Proposition

The quotient [[moduli stack]] $\mathcal{M}_{FG} \times Spec \mathbb{Q}$ of formal group over the [[rational numbers]] is isomorphic to $\mathbf{B}\mathbb{G}_m$, the [[delooping]] of the [[multiplicative group]] (over $Spec \mathbb{Q}$). This means that in [[characteristic]] 0 every formal group is determined, up to unique [[isomorphism]], by its [[Lie algebra]].

=--

For instance ([Lurie 10, lecture 12, corollary 3](#Lurie10)).

### Universal 1d commutative formal group law
 {#Universal1dFormalGroupLaw}

It is immediate that there exists a ring carrying a universal formal group law. For observe that for $\underset{i,j}{\sum} a_{i,j} x_1^i x_1^j$ an element in a [[formal power series]] algebra, then the condition that it defines a [[formal group law]] is equivalently a sequence of polynomial [[equations]] on the [[coefficients]] $a_k$. For instance the commutativity condition means that 

$$
  a_{i,j} = a_{j,i}
$$

and the unitality constraint means that

$$
  a_{i 0} 
  =
  \left\{
    \array{
      1 & if \; i = 1
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

Similarly associativity is equivalently a condition on combinations of triple products of the coefficients. It is not necessary to even write this out, the important point is only that it is some polynomial equation. 

This allows to make the following definition

+-- {: .num_defn #LazardRing}
###### Definition

The **[[Lazard ring]]** is the [[graded commutative ring]] generated by  elements $a_{i j}$ in degree $2(i+j-1)$ with $i,j \in \mathbb{N}$

$$
  L = \mathbb{Z}[a_{i j}] / (relations\;1,2,3\;below)
$$

quotiented by the relations

1. $a_{i j} = a_{j i}$

1. $a_{10} = a_{01} = 1$; $\forall i \neq 1: a_{i 0} = 0$

1. the obvious associativity relation

for all $i,j,k$.

The **universal 1-dimensional commutative [[formal group law]]** is the formal power series with [[coefficients]] in the Lazard ring given by

$$
  \ell(x,y) \coloneqq \sum_{i,j} a_{i j} x^i y^j \in L[ [ x , y ] ]
  \,.
$$

=--

+-- {: .num_remark #LazardRing}
###### Remark

The grading is chosen with regards to the formal group laws arising from [[complex oriented cohomology theories]] ([prop.](complex+oriented+cohomology+theory#ComplexOrientedCohomologyTheoryFormalGroupLaw)) where the [[variable]] $x$ naturally has degree -2. This way

$$
 deg(a_{i j} x^i y^j)
  = 
  deg(a_i,j) + i deg(x) + j deg(y)
  =
  -2
  \,.
$$

=--

The following is immediate from the definition:

+-- {: .num_prop #LazardRingIsUniversal}
###### Proposition

For every [[ring]] $R$ and 1-dimensional commutative [[formal group law]] $\mu$ over $R$ (example \ref{Commutative1DimFormalGroupLaw}), there exists a unique ring [[homomorphism]]

$$
  f \;\colon\; L \longrightarrow R
$$

from the [[Lazard ring]] (def. \ref{LazardRing}) to $R$, such that it takes the universal formal group law $\ell$ to $\mu$

$$
  f_\ast \ell = \mu
  \,.
$$
 
=--

+-- {: .proof}
###### Proof

If the formal group law $\mu$ has coefficients $\{c_{i,j}\}$, then in order that $f_\ast \ell = \mu$, i.e. that

$$
  \underset{i,j}{\sum} f(a_{i,j}) x^i y^j
  = 
  \underset{i,j}{\sum} c_{i,j} x^i y^j
$$

it must be that $f$ is given by

$$
  f(a_{i,j}) = c_{i,j}
$$

where $a_{i,j}$ are the generators of the Lazard ring. Hence it only remains to see that this indeed constitutes a ring homomorphism. But this is guaranteed by the vary choice of relations imposed in the definition of the Lazard ring.

=--

What is however highly nontrivial is this statement:

+-- {: .num_theorem #LazardTheorem}
###### Theorem
**([[Lazard's theorem]])**

The [[Lazard ring]] $L$ (def. \ref{LazardRing}) is [[isomorphism|isomorphic]] to a [[polynomial ring]]

$$
  L
  \simeq
  \mathbb{Z}[ t_1, t_2, \cdots ]
$$

in countably many generators $t_i$ in degree $2 i$.

=--

+-- {: .num_remark}
###### Remark

The [[Lazard theorem]] \ref{LazardTheorem} first of all implies, via prop. \ref{LazardRingIsUniversal}, that there exists an abundance of 1-dimensional formal group laws: given any ring $R$ then every choice of elements $\{t_i \in R\}$ defines a formal group law. (On the other hand, it is nontrivial to say which formal group law that is.)

Deeper is the fact expressed by the [[Milnor-Quillen theorem on MU]]: the Lazard ring in its polynomial incarnation of prop. \ref{LazardTheorem} is canonically identified with the [[graded commutative ring]] $\pi_\bullet(M U)$ of [[stable homotopy groups]] of the universal complex [[Thom spectrum]] [[MU]]. Moreover:

1. [[MU]] carries a [[universal complex orientation on MU|universal complex orientation]] in that for $E$ any [[homotopy commutative ring spectrum]] then homotopy classes of homotopy ring homomorphisms $M U \to E$ are in bijection to [[complex oriented cohomology theory|complex orientations]] on $E$;

1. every [[complex oriented cohomology|complex orientation]] on $E$ induced a 1-dimensional commutative [[formal group law]] ([prop.](complex+oriented+cohomology+theory#ComplexOrientedCohomologyTheoryFormalGroupLaw))

1. under forming stable homotopy groups every ring spectrum homomorphism $M U \to E$ induces a ring homomorphism 

   $$
     L \simeq \pi_\bullet(M U) \longrightarrow \pi_\bullet(E)
   $$

   and hence, by the universality of $L$, a formal group law over $\pi_\bullet(E)$. 

This is the formal group law given by the above complex orientation.

Hence the universal group law over the Lazard ring is a kind of [[decategorification]] of the [[universal complex orientation on MU]].


=--



## Examples

* [[formal multiplicative group]]

* [[Artin-Mazur formal group]] of an [[algebraic variety]],

  * [[formal Picard group]],

  * [[formal Brauer group]]

* [[Lubin-Tate formal group]]

* [[Honda formal group]]

## Related concepts

* [[height of a formal group law]]

* [[p-typical formal group law]]

* [[Morava stabilizer group]]

* [[Landweber exact functor theorem]]

* [[chromatic homotopy theory]]

* [[Lie algebra]], [[Lie group]]

* [[formal groupoid]]


Formal geometry is closely related also to the [[rigid analytic geometry]].


(nlab remark: we should explain connections to the Witt rings, Cartier/Dieudonn&#233; modules).


[[!include infinitesimal and local - table]]


## References

### General

* Shigkaki T&#244;g&#244;, _Note of formal Lie groups_ , American Journal of Mathematics, Vol. 81, No. 3, Jul., 1959 ([JSTOR](http://www.jstor.org/stable/2372919))

* A. Fr&#246;hlich, _Formal group_,  Lecture Notes in Mathematics
Volume 74, Springer (1968)


* {#Grothendieck} [[Alexander Grothendieck]] et al. [[SGA]] III, vol. 1, Expose VIIB (P. Gabriel) ETUDE INFINITESIMALE DES SCHEMAS EN GROUPES (part B) 474-560 

* {#Adams74} [[Frank Adams]], Part II.1 of _[[Stable homotopy and generalised homology]]_, 1974

 
* {#Kochmann96} [[Stanley Kochmann]], section 4.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Fresse} [[Benoit Fresse]], _Lie theory of formal groups over an operad_, J. Alg. __202__, 455--511, 1998, [doi](http://dx.doi.org/10.1006/jabr.1997.7280) 
 

* Michiel Hazewinkel, Formal Groups and Applications, [projecteuclid](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183548600)

* Michel [[Demazure, lectures on p-divisible groups]]
 
* [[Jean Dieudonné]], _Introduction to the theory of formal groups_, Marcel Dekker, New York 1973.



### 1-Dimensional formal groups 


A basic introduction is in

* Carl Erickson, _One-dimensional formal groups_ ([pdf](http://people.brandeis.edu/~cwe/pdfs/formal_groups.pdf))

Specifically formal group laws of [[elliptic curves]]:

* Antonia W. Bluher, _Formal groups, elliptic curves, and some theorems of Couveignes_, in: J.P. Buhler (eds.) _Algorithmic Number Theory_ ANTS 1998. Lecture Notes in Computer Science, vol 1423. Springer 1998 ([arXiv:math/9708215](https://arxiv.org/abs/math/9708215), [doi:10.1007/BFb0054887]( https://doi.org/10.1007/BFb0054887))

* {#Friedl17} Stefan Friedl, _An elementary proof of the group law for elliptic curves_ ([arXiv:1710.00214](https://arxiv.org/abs/1710.00214))

[[Quillen's theorem on MU]] is due to

* {#Quillen69} [[Daniel Quillen]], _On the formal group laws of unoriented and complex cobordism theory_, 1969, [projecteuclid](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183530915)

See also

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)) Lecture 11 _Formal groups_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture11.pdf))


* [[Takeshi Torii]], _One dimensional formal group laws of height $N$ and $N-1$_, PhD thesis 2001 ([pdf](http://mathnt.mat.jhu.edu/mathnew/Thesis/Torii.thesis.pdf))

* [[Takeshi Torii]], _On Degeneration of One-Dimensional Formal Group Laws and Applications to Stable Homotopy Theory_,  American Journal of Mathematics Vol. 125, No. 5 (Oct., 2003), pp. 1037-1077 ([JSTOR](http://www.jstor.org/stable/25099207))

* [[Stefan Schwede]], _Formal groups and stable homotopy of commutative rings_, Geom. Topol. 8 (2004) 335-412 ([arXiv:math/0402372](http://arxiv.org/abs/math/0402372))

The [[moduli stack]] of formal groups and its incarnation as a [[Hopf algebroid]]:

* [[Niko Naumann]], _The stack of formal groups in stable homotopy theory_, Advances in Mathematics Volume 215, Issue 2, 10 November 2007, Pages 569&#8211;600 doi:[10.1016/j.aim.2007.04.007](http://dx.doi.org/10.1016/j.aim.2007.04.007), arXiv:[math.AT/0503308](http://front.math.ucdavis.edu/math.AT/0503308)

[[!redirects formal groups]]

[[!redirects formal group scheme]]
[[!redirects formal group schemes]]

[[!redirects formal group law]]
[[!redirects formal group laws]]