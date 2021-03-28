
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
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


## Definition

### Finite-dimensional spheres


+-- {: .num_defn}
###### Definition

The $n$-dimensional unit **sphere** , or simply **$n$-sphere**, is the [[topological space]] given by the [[subset]] of the $(n+1)$-dimensional [[Cartesian space]] $\mathbb{R}^{n+1}$ consisting of all points $x$ whose distance from the origin is $1$

$$ 
  S^n = \{ x: \mathbb{R}^{n+1} \;|\; \|x\| = 1 \} 
  \,.
$$

The $n$-dimensional sphere of radius $r$ is
$$ S^n_r = \{ x: \mathbb{R}^{n+1} \;|\; \|x\| = r \} .$$
Topologically, this is equivalent ([[homeomorphism|homeomorphic]]) to the unit sphere for $r \gt 0$, or a [[point]] for $r = 0$.

This is naturally a [[smooth manifold]] of [[dimension]] $n$, with the [[smooth structure]] induced by the standard smooth structure on $\mathbb{R}^n$.

=--



### Infinite dimensional spheres 
 {#InfiniteDimensionalSphere}

One can also talk about the [[infinite-dimensional sphere]] in an arbitrary (possibly infinite-dimensional) [[normed vector space]] $V$:
$$ S(V) = \{ x: V \;\text{such that}\; {\|x\|} = 1 \} .$$

If a [[LCTVS|locally convex topological vector space]] admits a continuous linear injection into a [[normed vector space]], this can be used to define its sphere.  If not, one can still define the sphere as a *quotient* of the space of non-zero vectors under the scalar action of $(0,\infty)$.

Homotopy theorists define $S^\infty$ to be the sphere in the (incomplete) [[normed vector space]] (traditionally with the $l^2$ norm) of infinite [[sequence]]s almost all of whose values are $0$, which is the [[directed colimit]] of the $S^n$:
$$ S^{-1} \hookrightarrow S^0 \hookrightarrow S^1 \hookrightarrow S^2 \hookrightarrow \cdots S^\infty .$$
In themselves, these provide nothing new to [[homotopy theory]], as they are at least weakly contractible and usually [[contractible space|contractible]].  However, they are a very useful source of big contractible spaces and so are often used as a starting point for making concrete models of [[classifying spaces]].

If the vector space is a [[shift space]], then contractibility is straightforward to prove.

+-- {: .num_theorem #theorem}
###### Theorem
Let $V$ be a [[shift space]] of some order.  Let $S V$ be its sphere (either via a norm or as the quotient of non-zero vectors).  Then $S V$ is contractible.
=--

+-- {: .proof}
###### Proof
Let $T \colon V \to V$ be a [[shift map]].  The idea is to homotop the sphere onto the image of $T$, and then down to a point.

It is simplest to start with the non-zero vectors, $V \setminus \{0\}$.  As $T$ is injective, it restricts to a map from this space to itself which commutes with the scalar action of $(0,\infty)$.  Define a homotopy $H \colon [0,1] \times (V \setminus
 \{0\}) \to V \setminus \{0\}$ by $H_t(v) = (1 - t)v + t T v$.  It is clear that, assuming it is well-defined, it is a homotopy from the identity to $T$.  To see that it is well-defined, we need to show that $H_t(v)$ is never zero.  The only place where it could be zero would be on an eigenvector of $T$, but as $T$ is a [[shift map]] then it has none.

As $T$ is a [[shift map]], it is not surjective and so we can pick some $v_0$ not in its image.  Then we define a homotopy $G \colon [0,1] \times (V \setminus \{0\}) \to V \setminus \{0\}$ by $G_t(v) = (1 - t)T v + t v_0$.  As $v_0$ is not in the image of $T$, this is well-defined on $V \setminus \{0\}$.  Combining these two homotopies results in the desired contraction of $V \setminus \{0\}$.

If $V$ admits a suitable function defining a spherical subset (such as a norm) then we can modify the above to a contraction of the spherical subset simply by dividing out by this function.  If not, as the homotopies above all commute with the scalar action of $(0,\infty)$, they descend to the definition of the sphere as the quotient of $V \setminus \{0\}$.
=--


## Properties

### Basic

* The $n$-sphere is the [[boundary]] of the $(n+1)$-[[ball]].

* These spheres, or rather their underlying [[topological spaces]] or [[simplicial set]]s, are fundamental in (ungeneralised) [[homotopy theory]].  In a sense, [[Whitehead's theorem]] says that these are all that you need; no further [[generalized (Eilenberg-Steenrod) homotopy theory|generalised homotopy theory]] (in a sense [[Eckmann–Hilton duality|dual]] to [[Eilenberg–Steenrod cohomology theory]]) is needed.

* [[positive dimension spheres are H-cogroup objects]], and this is the origin of the [[group]] structure on [[homotopy groups]]). 


### Coset space structure
 {#LabelCosetSpaceStructure}



+-- {: .num_prop #nSphereAsCosetSpace}
###### Proposition

For $n \in \mathbb{N}$ the [[n-spheres]] are [[coset spaces]] of [[orthogonal groups]]

$$
  S^n \;\simeq\; O(n+1)/O(n)
  \,.
$$

Similarly for the corresponding [[special orthogonal groups]]

$$
  S^n \;\simeq\; SO(n+1)/SO(n)
$$

and [[spin groups]]

$$
  S^n \;\simeq\; Spin(n+1)/Spin(n)
$$

and [[pin groups]]

$$
  S^n \;\simeq\; Pin(n+1)/Pin(n)
  \,.
$$


=--

+-- {: .proof}
###### Proof

Fix a [[unit vector]] in $\mathbb{R}^{n+1}$. Then its [[orbit]] under the defining $O(n+1)$-[[action]] on $\mathbb{R}^{n+1}$ is clearly the canonical embedding $S^n \hookrightarrow \mathbb{R}^{n+1}$. But precisely the subgroup of $O(n+1)$ that consists of rotations around the axis formed by that unit vector [[stabilizer group|stabilizes]] it, and that subgroup is isomorphic to $O(n)$, hence $S^n \simeq O(n+1)/O(n)$.

=--

Similarly, the analogous argument for [[unit spheres]] inside (the [[real vector spaces]] underlying) [[complex vector spaces]], we have

+-- {: .num_prop #OddDimSphereAsSpecialUnitaryCoset}
###### Proposition

For $k \in \mathbb{N}$ the [[n-sphere|(2k+1)-sphere]] $S^{2k+1}$ is the [[coset space]] of [[special unitary groups]]:

$$
  S^{2k+1}
  \;\simeq\;
  SU(k+1)/SU(k)
  \,.
$$

=--

And still similarly, the analogous argument for [[unit spheres]] inside (the [[real vector spaces]] underlying) [[quaternionic vector spaces]], we have

+-- {: .num_prop #SphereAsSymplecticUnitaryCoset}
###### Proposition

For $k \in \mathbb{N}$, $k \geq 1$ the [[n-sphere|(4k-1)-sphere]] $S^{4k-1}$ is the [[coset space]] of [[quaternionic unitary groups]]:

$$
  S^{4k-1}
  \;\simeq\;
  Sp(k)/Sp(k-1)
  \,.
$$

=--

Generally:

+-- {: .num_prop #TransitiveEffectiveActionsOfConnectedLieGroupsOnSpheres}
###### Proposition

The [[connected topological space|connected]] [[Lie groups]] with [[effective action|effective]] [[transitive actions]]  on [[n-spheres]] are precisely (up to [[isomorphism]]) the following:

* [[SO(n)]]

* [[U(n)]]

* [[SU(n)]]

* [[Sp(n)]]

* [[Sp(n).Sp(1)|Sp(n).SO(2)]]

* [[Sp(n).Sp(1)]]

* [[G2]]

* [[Spin(7)]]

* [[Spin(9)]]

with [[coset spaces]]

$$
  \begin{aligned}
    SO(n)/SO(n-1)
    & \simeq S^{n-1}
    \\
    U(n)/U(n-1) & \simeq S^{2n-1}
    \\
    SU(n)/SU(n-1) & \simeq S^{2n-1}    
    \\
    Sp(n)/Sp(n-1) & \simeq S^{4n-1}    
    \\
    Sp(n)\cdot SO(2)/Sp(n-1)\cdot SO(2) & \simeq S^{4n-1}    
    \\
    Sp(n)\cdot Sp(1)/Sp(n-1)\cdot Sp(1) & \simeq S^{4n-1}    
    \\
    G_2/SU(3) & \simeq S^6
    \\
    Spin(7)/G_2 & \simeq S^7
    \\
    Spin(9)/Spin(7) & \simeq S^{15}
  \end{aligned}
$$

=--

This goes back to [Montogomery-Samelson 43](#MontogomerySamelson43), see  
[Gray-Green 70, p. 1-2](#GrayGreen70)

(also e.g [Borel-Serre 53, 17.1](#BorelSerre53))


+-- {: .num_remark}
###### Remark

The [[isomorphisms]] in Prop. \ref{nSphereAsCosetSpace} and Prop. \ref{OddDimSphereAsSpecialUnitaryCoset} above hold in the [[category]] of [[topological spaces]] ([[homeomorphisms]]), but in fact also in the [[category]] of [[smooth manifolds]] ([[diffeomorphisms]]) and even in the [[category]] of [[Riemannian manifolds]] ([[isometries]]).

But the other [[coset space]] realizations of some [[n-spheres]] in Prop. \ref{TransitiveEffectiveActionsOfConnectedLieGroupsOnSpheres} are [[homeomorphisms]], but not necessarily [[isometries]] ("[[squashed spheres]]"). There is also a [[double coset space]] realization which is not even a [[diffeomorphisms]] ("[[exotic sphere]]", the [[Gromoll-Meyer sphere]]). 

For more see _[7-sphere -- Coset space realization](7-sphere#CosetSpaceRealization)_.

=--

[[!include coset space structure on n-spheres -- table]]


### Spin structure

\begin{example}
The $n$-sphere, for each $n \in \mathbb{N}$, carries a canonical [[spin structure]], induced from its [[coset space]]-realization $S^n \simeq Spin(n+1)/Spin(n)$ 
([above](#LabelCosetSpaceStructure)), as a special case of the canonical $H$-structure on $G/H$ ([this example](G-structure#CanonicalHStructureOnFModH)).
\end{example}

Other ways to see this:


* {#Nowaczyk15} Nikolai Nowaczyk, Theorem A.6.6 in: _Dirac Eigenvalues of higher Multiplicity_, Regensburg 2015 ([arXiv:1501.04045](https://arxiv.org/abs/1501.04045))

* {#SpinorsInGeometryAndPhysics} S. Gutt, _Killing spinors on spheres and projective spaces_, p. 238-248 in: A. Trautman, G. Furlan (eds.) _Spinors in Geometry and Physics -- Trieste 11-13 September 1986_, World Scientific 1988
([doi:10.1142/9789814541510](https://doi.org/10.1142/9789814541510),  [GBooks, p. 243](https://books.google.ae/books?id=d14GCwAAQBAJ&lpg=PA243&ots=_tH_He8UFg&dq=%22spin%20structure%20on%20spheres%22&pg=PA243#v=onepage&q=%22spin%20structure%20on%20spheres%22&f=false))


\linebreak

### Parallelizability

* Precisely four spheres are [[parallelizable]], and three of these are so via [[Lie group]] structure (hence are the only spheres with Lie group structure) (see at _[[Hopf invariant one theorem]]_):

  * $S^0$ (the [[group of order two]], the group of units of the [[real numbers]]);

  * $S^1$ (the [[circle group]], the group of unit [[complex numbers]]);

  * $S^3$ (the [[special unitary group]] $SU(2)$, the group of unit [[quaternions]]);

  * $S^7$ (the [[Moufang loop]] of unit [[octonions]])

### Branched covers

Every $n$-[[dimension|dimensional]] [[PL manifold]] admits a [[branched covering]] of the [[n-sphere]] ([Alexander 20](branched+cover#Alexander20)). 

By the [[Riemann existence theorem]], every [[connected topological space|connected]] [[compact topological space|compact]] [[Riemann surface]] admits the [[structure]] of a branched cover by a [[holomorphic function]] to the [[Riemann sphere]]. See [there](branched+cover+of+the+Riemann+sphere#RiemannSurfaces) at _[[branched cover of the Riemann sphere]]_.

\begin{center}
<img src="https://ncatlab.org/nlab/files/TorusBranchedCoverOverSphere.jpg" width="500">
\end{center}

> graphics grabbed from [Chamseddine-Connes-Mukhanov 14, Figure 1](branched+cover#ChamseddineConnesMukhanov14), [Connes 17, Figure 11](branched+cover#Connes17)


For [[3-manifolds]] branched covering the [[3-sphere]] see ([Montesinos 74](branched+cover#Montesinos74)).


All [[PL manifold|PL]] [[4-manifolds]] are _simple_ branched covers of the  [[4-sphere]] ([Piergallini 95](#Piergallini95), [Iori-Piergallini 02](branched+cover#IoriPiergallini02)).

But the [[n-torus]] for $n \geq 3$ is _not a [[cyclic group|cyclic]]_ branched over of the [[n-sphere]] ([Hirsch-Neumann 75](branched+cover#HirschNeumann75))


### Iterated loop spaces

+-- {: .num_prop #RationalCohomologyOfIteratedLoopSpaceOf2kSphere}
###### Proposition     
**([[rational cohomology]] of [[iterated loop space]] of the [[n-sphere|2k-sphere]])**

Let 

$$
  1 \leq D \lt n = 2k \in \mathbb{N}

$$ 

(hence two [[positive number|positive]] [[natural numbers]], one of them required to be [[even number|even]] and the other required to be smaller than the first) and consider the [[iterated loop space|D-fold loop space]] $\Omega^D S^n$ of the [[n-sphere]]. 

Its [[rational cohomology|rational]] [[cohomology ring]] is the [[free construction|free]] [[graded-commutative algebra]] over $\mathbb{Q}$ on one [[generators and relations|generator]] $e_{n-D}$ of degree $n - D$ and one generator $a_{2n - D - 1}$ of degree $2n - D - 1$:

$$
  H^\bullet
  \big(
    \Omega^D S^n
    ,
    \mathbb{Q}
  \big)
  \;\simeq\;
  \mathbb{Q}\big[ e_{n - D}, a_{2n - D - 1} \big] 
  \,.
$$  

=--

([Kallel-Sjerve 99, Prop. 4.10](#KallelSjerve99))


## Examples
 {#Examples}

*  The $(-1)$-sphere is the [[empty space]].

*  The [[0-sphere]] is the [[disjoint union]] of two [[points]].

*  The [[1-sphere]] is the [[circle]].

*  The [[2-sphere]] is usual sphere from ordinary geometry. This canonically carries the structure of a [[complex manifold]] which makes it the [[Riemann sphere]].

* The [[3-sphere]] and [[4-sphere]], [[5-sphere]] and [[6-sphere]] and [[7-sphere]] are interesting, too.

## Related concepts

* [[round sphere]]

* [[fuzzy sphere]]

* [[hemisphere]], [[equator]]

* [[unit sphere]]

* [[stereographic projection]]

* [[sphere fiber bundle]]

* [[polar coordinates]]

* [[Reeb sphere theorem]]

* [[homotopy groups of spheres]]

* [[rational n-sphere]]

* [[sphere spectrum]]

* [[spherical fibration]]

* [[geometric quantization of the 2-sphere]]

* [[representation sphere]]

* [[motivic sphere]]

* [[group actions on spheres]]

* [[homology sphere]]

* [[homotopy sphere]]

* [[sphere packing]]

* [[Tate sphere]]

* The [[non-abelian cohomology|non-abelian]] [[generalized cohomology theory]] [[representable functor|represented]] by [[n-spheres]] is [[Cohomotopy cohomology theory]].

## References

### Formalization

Axiomatization of the [[homotopy type]] of the 1-sphere (the [[circle]]) and the 2-sphere, as [[higher inductive types]], is in 

* [[Univalent Foundations Project]], section 6.4 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

Visualization of the idea of the construction for the 2-sphere is in 

* [[Andrej Bauer]], _HoTT $S^2$_ ([video](https://vimeo.com/119606901))

### Group actions on spheres

Discussion of [[free actions|free]] [[group actions on spheres]] by [[finite groups]] includes

* {#Wall78} [[C. T. C. Wall]], _Free actions of finite groups on spheres_, Proceedings of Symposia in Pure Mathematics, Volume 32, 1978 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/wall7.pdf))

* [[Alejandro Adem]], _Constructing and deconstructing group actions_ ([arXiv:0212280](http://arxiv.org/abs/math/0212280))

The subgroups of [[special orthogonal group|SO(8)]] which act freely on $S^7$ have been classified in 

* J. A. Wolf, _Spaces of constant curvature_, Publish or Perish, Boston, Third ed., 1974

and lifted to actions of [[Spin group|Spin(8)]] in 

* S. Gadhia, _Supersymmetric quotients of M-theory and supergravity backgrounds_, PhD thesis, School of Mathematics, University of Edinburgh, 2007

Discussion of [[transitive actions]] on $n$-spheres by [[compact Lie groups]]:

* {#MontogomerySamelson43} Deane Montgomery, Hans Samelson, _Transformation Groups of Spheres_, Annals of Mathematics Second Series, Vol. 44, No. 3 (Jul., 1943), pp. 454-470 ([jstor:1968975](https://www.jstor.org/stable/1968975))

* {#GrayGreen70} [[Alfred Gray]], Paul S. Green, _Sphere transitive structures and the triality automorphism_, Pacific J. Math. Volume 34, Number 1 (1970), 83-96 ([euclid:1102976640](https://projecteuclid.org/euclid.pjm/1102976640))

Further discussion of these actions is in

* {#MFFGME09} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], Sunil Gadhia, [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))

where they are related to the [[black brane|black]] [[M2-brane]] [[BPS state|BPS]]-solutions of [[11-dimensional supergravity]] at [[ADE-singularities]].


See also the [[ADE classification]] of such actions on the [[7-sphere]] (as discussed there)


### Geometric structures on spheres

Coset space structures on spheres:

* {#BorelSerre53} [[Armand Borel]], [[Jean-Pierre Serre]], _Groupes de Lie et Puissances Reduites de Steenrod_, American Journal of Mathematics, Vol. 75, No. 3 (Jul., 1953), pp. 409-448 ([jstor:2372495](https://www.jstor.org/stable/2372495))

The following to be handled with care:

* [[Michael Atiyah]], _The non-existent complex 6-sphere_, [arxiv/1610.09366](https://arxiv.org/abs/1610.09366)

### Embeddings of spheres

The ([[isotopy]] [[equivalence class|class]] of an) [[embedding of differentiable manifolds|embedding]] of a [[circle]] (1-sphere) into the [[3-sphere]] is a _[[knot]]_. Discussion of embeddings of spheres of more general dimensions into each other:

* {#Haefliger66} [[André Haefliger]], _Differentiable Embeddings of $S^n$ in $S^{n+q}$ for $q \gt 2$_, Annals of Mathematics Second Series, Vol. 83, No. 3 (May, 1966), pp. 402-436 ([jstor:1970475](https://www.jstor.org/stable/1970475))

### Iterated loop spaces

* {#KallelSjerve99} [[Sadok Kallel]], [[Denis Sjerve]], _On Brace Products and the Structur eof Fibrations with Section_, 1999 ([pdf](https://www.math.ubc.ca/~sjer/brace.pdf), [[KallelSjerv99.pdf:file]])

[[!redirects n-sphere]]
[[!redirects n-spheres]]

[[!redirects spheres]]

[[!redirects infinite sphere]]

[[!redirects 1-sphere]]
[[!redirects 1-spheres]]

[[!redirects 2-sphere]]
[[!redirects 2-spheres]]

