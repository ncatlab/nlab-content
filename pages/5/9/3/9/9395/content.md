
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Let $X$ be an [[H-space]].  The _Hopf construction_ ([Hopf 35](#Hopf35)) on $X$ is a [[fibration]]

$$ 
  X \hookrightarrow X\ast X \to \Sigma X
$$

whose [[fiber]] is $X$, whose base space is the [[suspension]] of $X$, and whose total space is the [[join of topological spaces|join]] of $X$ with itself. ([Stasheff 70, chapter 1](#Stasheff70)).

Specialized to $X$ the [[sphere]] of [[dimension]] [[0-sphere|0]], [[1-sphere|1]], [[3-sphere|3]], or [[7-sphere|7]], the Hopf construction yields the _[Hopf fibrations](#HopfFibrations)_. (And by the [[Hopf invariant one theorem]] these are the only dimensions for in which spheres are H-spaces.)

## Definition
 {#Definition}

+-- {: .num_defn #SuspensionJoin}
###### Definition

Write $I \coloneqq [0,1]$ for the unit interval, regarded as a [[topological space]].

Let $X,Y $ be [[topological spaces]].

1. The [[suspension]] $\Sigma X$ is the [[quotient space]]

   $$
     \Sigma X \coloneqq (X \times I)_{/\sim}
   $$

   by the [[equivalence relation]]  given by

   $$
     (x_1,0) \sim (x_2,0) \;\,,\;\;  (x_1, 1) \sim (x_2, 1) \;\;\; \forall x_1,x_2 \in X
   $$

1. The [[join of topological spaces|join]] $X \ast Y$ is the [[quotient space]]

   $$
      X \ast Y \coloneqq (X \times I \times Y)_{/\sim}
   $$

   by the [[equivalence relation]]

   $$
     (x, 0, y_1) \simeq (x,0,y_2) \;\;,\;\; (x_1,1,y) \sim (x_2, 1, y)
     \,.
   $$

=--

+-- {: .num_defn #HopfConstruction}
###### Definition

Given a [[continuous function]] of the form

$$
  f \colon X \times Y \longrightarrow Z
$$

its _Hopf construction_ is the continuous function

$$
  H_f \colon X \ast Y \longrightarrow \Sigma Z
$$

out of the [[join of topological spaces|join]] into the [[suspension]], given in the coordinates of def. \ref{SuspensionJoin} by

$$
  H_f \colon (x,t,y) \mapsto (f(x,y), t)
  \,.
$$

=--

## Properties
 {#Properties}

### Homotopy fiber
  {#HomotopyFiber}

If $X$ is an "grouplike H-space", in that it is a topological [[magma]] such that left multiplication acts by [[weak homotopy equivalences]], then the [[homotopy fiber]] of the Hopf construction $X \ast X \to \Sigma X$ over any point is
[[weak homotopy equivalence|weakly homotopy equivalent]] to $X$ ([here](https://nforum.ncatlab.org/discussion/3391/hopf-fibration/?Focus=76088#Comment_76088)).

Beware that it may not generally be true that the ordinary [[fibers]] of the Hopf construction are [[weak homotopy equivalence|weakly homotopy equivalent]] to the [[homotopy fibers]], see also the discussion of [[quasifibrations]] [below](#RealizationAsAQuasiFibration). But in the classical examples it Happens to be the case, see at [[Hopf fibration]].



### Relation to Hopf invariant

Consider $X = S^{n-1}$ a [[sphere]]

+-- {: .num_prop #HopfInvariantFromProductOfDegrees}
###### Proposition

Given a [[continuous function]]

$$
  f \colon S^{n-1}\times S^{n-1} \longrightarrow S^{n-1}
$$

the [[degree of a continuous function|degrees]] 

$$
  \alpha \coloneqq deg(f(x,-)) \;\;\; \beta \coloneqq deg(f(-,x))
$$

are independent of the choice of $x \in S^{n-1}$. The [[Hopf invariant]]  $h$ of the Hopf construction $H_f$ of $f$, def. \ref{HopfConstruction}, is the product of these two:

$$
  h(H_f) = \alpha \beta
  \,.
$$

=--

([Mosher-Tangora, exercises to section 4, page 38](#MosherTangora))


### Realization as a quasi-fibration
 {#RealizationAsAQuasiFibration}

Beware that [Stasheff 70, theorem 1.2](#Stasheff70) claims that Sugawara claimed that the Hopf construction for any [[CW-complex|CW]] H-space is necessarily a [[quasifibration]]. But it seems ([here](https://nforum.ncatlab.org/discussion/3391/hopf-fibration/?Focus=75986#Comment_75986)) that Sugawara never actually claimed this and also ([here](https://nforum.ncatlab.org/discussion/3391/hopf-fibration/?Focus=75985#Comment_75985)) that it is not actually the case.

A different but homotopy-equivalent realization of the Hopf construction, which over grouplike H-spaces is guaranteed to be a [[quasifibration]], is maybe given in [Dold-Lashof 59](#DoldLashof59), see also [Stasheff 70, theorem 1.4](#Stasheff70).


## Examples

### Hopf fibrations
 {#HopfFibrations}

When $X$ is a [[sphere]] that is an $H$-space, namely, one of the [[groups]] $S^0 = \mathbb{Z}/2$ the [[group of order 2]], $S^1 = U(1)$ the [[circle group]], the [[3-sphere]] [[special unitary group]] $S^3 = SU(2)$;  or the [[7-sphere]] $S^7$ with its [[Moufang loop]] structure, then the Hopf construction produces the four _[[Hopf fibrations]]_:

1. $S^0 \hookrightarrow S^1 \to S^1 $ -- [[real Hopf fibration]]
1. $ S^1 \hookrightarrow S^3 \to S^2 $ -- [[complex Hopf fibration]]
1. $ S^3 \hookrightarrow S^7 \to S^4 $ -- [[quaternionic Hopf fibration]]
1. $ S^7 \hookrightarrow S^{15} \to S^8 $ -- [[octonionic Hopf fibration]]

In detail, let $A \in \{\mathbb{R}, \mathbb{C}, \mathbb{H}, \mathbb{O}\}$
be one of the real [[normed division algebras]] and write

$$
  n \coloneqq dim_{\mathbb{R}}(A) \in \{1,2,4,8\}
$$

for its [[dimension]] as a real vector space. Then the $S^{n-1}$-sphere may be identified with the subspace of unit norm elements in $A$:

$$
  S^{n-1} \simeq
  \left\{
    x \in A
    \,;
    {\vert x\vert}^2 = 1
  \right\}
  \,.
$$

Consider then the pairing map

$$
  f \colon S^{n-1}\times S^{n-1} \longrightarrow S^{n-1}
$$

which is the restriction to these unit norm elements of the product in $A$:

$$
  f \colon (x,y) \mapsto x \cdot y
$$

This is well defined by the very property that for [[normed division algebras]] the norm is multiplicative.

Accordingly, the [[join of topological spaces|join]] of two such spheres is naturally parameterized as follows

$$
  S^{n-1}\ast S^{n-1}
  =
  (S^{n-1}\times I \times S^{n-1})_{/\sim}
  \simeq
  \left\{
    (x,t,y)
    \,,
    {\vert x \vert}^2 = 2t
    \,,\;
    {\vert y\vert}^2 = 2 - 2t
  \right\}
$$

which makes manifest that

$$
  S^{n-1} \ast S^{n-1} \simeq S^{2n-1}
$$

Similarly, the [[suspension]] is parameterized by 

$$
  \Sigma S^{n-1}
  =
  (S^{n-1}\times I)_{/\sim}
  \simeq
  \left\{
    (z,t)
    \,,\;
    {\vert z \vert}^2 + (1 - 2t)^2   = 1
  \right\}
$$

where we take $I = [0,1]$ and $t \in I$. This makes manifest that

$$
  \Sigma S^{n-1} \simeq S^n
  \,.
$$

Moreover, in this parameterization the Hopf construction, def. \ref{HopfConstruction}, which is given by 

$$
  (x,y) \mapsto x \cdot \overline{y}
$$

manifestly gives the Hopf fibration map. 

Notice that it is again the multiplicativity of the norm in division algebras which makes this work: if  ${\vert x \vert}^2 = 2t$ and ${\vert y\vert}^2 = 2 - 2t$ then it follows that

$$
  \begin{aligned}
     {\vert x \cdot \overline{y}\vert}^2 + (1- 2t)^2
     & = 
     {\vert x \vert}^2 {\vert y \vert}^2
     + (1-2t)^2
     \\
     & = 2t (2-2t) + (1 - 2t)^2 
     \\
     & = 1
  \end{aligned}
  \,,
$$

hence that indeed we have a well-defined map like so:

$$
  \array{
      S^7 & \longrightarrow & S^4
      \\
     \left\{
       (x,t,y)
        \,,
       {\vert x \vert}^2 = 2t
        \,,\;
        {\vert y\vert}^2 = 2 - 2t
     \right\}
     &\stackrel{{(x,y) \mapsto z \coloneqq x \cdot \overline{y}}\atop{t \mapsto t}}{\longrightarrow}&
    \left\{
       (z,t)
       \,,\;
       {\vert z \vert}^2 + (1 - 2t)^2   = 1
    \right\}  
  }
  \,.
$$

## See also

* [[Hopf construction in homotopy type theory]]

## References

The original sources are

* {#Hopf35} [[Heinz Hopf]], _&#220;ber die Abbildungen von Sph&#228;ren auf Sph&#228;ren niedrigerer Dimension_, Fund. Math. 25: 427&#8211;440 (1935) ([Euclid](https://eudml.org/doc/212801))

* [[George Whitehead]], _On the homotopy groups of spheres and rotation groups_, Annals of Mathematics. Second Series 43 (4): 634&#8211;640, (1942) ([JSTOR](http://www.jstor.org/stable/1968956))

* {#DoldLashof59} [[Albrecht Dold]], [[Richard Lashof]], _Principal quasifibrations and fibre homotopy equivalence of bundles_, Illinois J. Math. Volume 3, Issue 2 (1959), 285-305 ([euclid:1255455128](https://projecteuclid.org/euclid.ijm/1255455128))

Review inclides

* {#Stasheff70} [[Jim Stasheff]], chapter 1 in  _H-Spaces from a Homotopy point of view_, Lecture Notes in Mathematics Volume 161 1970

Textbook accounts include

* {#MosherTangora} [[Robert Mosher]], [[Martin Tangora]], p. 38 of _Cohomology Operations and Application in Homotopy Theory_, Harper and Row (1968) ([pdf](http://math.jhu.edu/~anakade1/notes/Dec%202014/Mosher%20and%20Tangora%20Notes/mosher-tangora.pdf))

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 10.6 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

See also 

* {#Moreno04} Guillermo Moreno, _Hopf construction map in higher dimensions_ ([arXiv:math/0404172](https://arxiv.org/abs/math/0404172))

*  Feza Guersey, Chia-Hsiung Tze, (4b.2) in _On the role of Division, Jordan and Related algebras in Particle Physics_



Discussion of the situation in [[parameterized homotopy theory]] includes

* {#CookCrabb93} A. L. Cook, M.C. Crabb, _Fiberwise Hopf structures on sphere bundles_, J. London Math. Soc. (2) 48 (1993) 365-384 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/crabbcook.pdf))

* {#Iriye95} Kouyemon Iriye, _Equivariant Hopf structures on a sphere_, J. Math. Kyoto Univ. Volume 35, Number 3 (1995), 403-412 ([Euclid](http://projecteuclid.org/euclid.kjm/1250518704))


See also

* Wikipedia, _[Hopf construction](https://en.wikipedia.org/wiki/Hopf_construction)_


[[!redirects Hopf constructions]]

[[!redirects Hopf map]]
[[!redirects Hopf maps]]