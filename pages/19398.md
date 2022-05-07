

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The possible [[actions]] of well-behaved [[topological groups]] (such as [[compact Lie groups]]) on [[topological space|topological]] or [[smooth manifold|smooth]] [[n-spheres]] display various interesting patterns in their classification. 

This entry is meant to eventually list and discuss some of these. For the moment it mainly just collects some references.

## Properties

### Free actions by finite groups and spherical space forms
 {#FreeActionsByFiniteGroupsAndSphericalSpaceForms}

We discuss some aspects of ([[G-space|continuous]]) [[free actions]] of [[finite groups]] on [[n-spheres]]. 

If the action is by [[isometries]] then the [[topological quotient spaces]] of such actions are known as *[[spherical space forms]]*.


#### Basic examples
 {#BasicExamplesOfFreeActionsOnSpheres}

We make explicit some elementary but important examples of free continuous finite group actions on $n$-spheres.

\begin{example}
\label{ActionOfZModTwoByAntipodalInversion}
**(action of $\mathbb{Z}/2$ by antipodal involution)**
\linebreak
  For all $n \in \mathbb{N}$, the group [[cyclic group of order 2|$\mathbb{Z}/2$]] has a [[continuous function|continuous]] [[free action]]  on the [[n-sphere]], given by [[antipode|antipodal]] reflection (hence reversing the [[orientation]]).

The [[topological quotient space]] of this action is the [[real projective space]] $S^{n+1}/(\mathbb{Z}/2) \,\simeq\, \mathbb{R}P^n$.
\end{example}


\begin{example}
\label{FiniteCyclicGroupsActFreelyOnAddDimensionalSpheres}
**(Finite cyclic groups act freely on odd-dimensional spheres)**
\linebreak
 For every non-[[trivial group|trivial]] [[finite group|finite]] [[cyclic group]] $\mathbb{Z}/n \,\subset\, U(1)$, its left-multiplication action on the [[n-sphere|$2n+1$-sphere]], regarded as the [[unit sphere]] in the [[complex numbers|complex]] $n$-space
$$
  S^{2n+1} 
    \,\simeq\,
  S\big(\mathbb{R}^{2n+2}\big)
    \,\simeq\,
  S\big(\mathbb{C}^{n+1}\big)
  \,,
$$
is (a [[G-space|continuous group action]] and) [[free action|free]].
\end{example}
This follows verbatim as the (slightly more interesting) Ex. \ref{FiniteADEGroupsActFreelyOnFourNPlusThreeSpheres} below, interchanging the [[complex numbers]] with the [[quaternions]].

\begin{example}
\label{FiniteADEGroupsActFreelyOnFourNPlusThreeSpheres}
**(Finite ADE-groups act freely on $S^{4n+3}$-spheres)**
\linebreak
For every non-[[trivial group|trivial]] [[finite subgroup of SU(2)]] $G \,\subset\, $ [[SU(2)]] $\simeq$ [[Sp(1)]] its [[quaternion|quaternionic]] left-multiplication action on the [[n-sphere|$4n+3$-sphere]], regarded as the [[unit sphere]] in the [[quaternion|quaternionic]] $n$-space
$$
  S^{4n+3} 
    \,\simeq\,
  S\big(\mathbb{R}^{4n+4}\big)
    \,\simeq\,
  S\big(\mathbb{H}^{n+1}\big)
  \,,
$$
is (a [[G-space|continuous group action]] and) [[free action|free]].
\end{example}
\begin{proof}
Here are the elementary and straightforward details:
 
Under the given identification, points in $S^{4n+3}$ correspond to $(n+1)$-[[tuples]] of [[quaternions]] $\vec v \,=\, (v_1, \cdots, v_{n+1})$, $v_i \,\in\, \mathbb{H}$ (i.e. quaternionic [[vectors]]) such that

\[
  \label{UnitNormConditionOnQuaternionicVectors}
  \begin{aligned}
    \left\vert \vec v \right\vert^2
    &
    \;\coloneqq\;
    \vec v^\dagger \cdot \vec v
    \\
    &
    \;\coloneqq\;
    \bar v_1 \cdot v_1  +  \cdots  +  \vec v_{n+1} \cdot v_{n+1} 
    \\
    &
    \;\overset{!}{=}\; 
    1
  \end{aligned}
  \,,
\]

where $\overline{(-)}$ denotes [[quaternionic conjugation]]. 

Since [[Sp(1)]] is the [[subgroup]] of the quaternionic [[group of units]] on the unit-[[norm]] elements

$$
  Sp(1)
  \;\coloneqq\;
  \big\{ 
    q \,\in\, \mathbb{H}^\times
    \,\vert\,
    \bar q \cdot q \,=\, 1
  \big\}
  \;\subset\;
  \mathbb{H}^\times
$$

we have

$$
  \begin{aligned}
    \left\vert
      q \cdot \vec v
    \right\vert
    &
    \;=\;
    (q \cdot \vec v)^\dagger
    \cdot
    (q \cdot \vec v)
    \\
    &
    \;=\;
    \vec v^\dagger 
      \cdot 
    \underset{ = 1}{\underbrace{q^\dagger \cdot q}} 
      \cdot 
    \vec v
    \\
    &
    \;=\;
    \vec v^\dagger \cdot \vec v
    \\
    &
    \;=\;
    \left\vert \vec v\right\vert^2
    \,,
  \end{aligned}
$$

showing that the left multiplication action of $Sp(1)$ on $\mathbb{H}^{n+1}$ does restrict to an action on its unit sphere.
Moreover, since quaternion-multiplication is clearly [[continuous function|continuous]] with respect to the [[Euclidean topology]] on $\mathbb{H} \simeq_{\mathbb{R}} \mathbb{R}^4$, this yields a continuous action on $S^{4n+3}$.

Finally, since $\mathbb{H} \,\ni\, q \,\mapsto\, \bar q \cdot q \,\in\, \mathbb{R}$ is positive definite ($\bar q \cdot q = 0 \,\;\Leftrightarrow\;\, q = 0$ ), at least one of the components $v_i$ of $\vec v$ needs to be non-zero in order for  (eq:UnitNormConditionOnQuaternionicVectors) to hold. But on this component the left action $v_i \,\mapsto\, q \cdot v_i$ is left-multiplication in the [[group of units]] $\mathbb{H}^{\times} \,=\, \mathbb{H} \setminus \{0\}$ and hence is free, as the multiplication action of any group on itself is free.
\end{proof}

Notice that, while an analogous argument shows that with $G \subset Sp(1)$ also the [[direct product group]] $G^{n+1}$ canonically acts on $S^{4n+3}$ by componentwise left multiplication, for $n \geq 2$ this action is no longer free, as the $k$th factor subgroup now fixes the elements whose $k$th component vanishes. In fact, higher direct product powers of cyclic groups in general have *no* free action on spheres of any dimension, see Smith's $p^2$-condition (Prop. \ref{SmithPSquareCondition} below).


#### Free involutions
 {#Involutions}

The [above examples](#BasicExamplesOfFreeActionsOnSpheres) of free actions on spheres are all on odd-dimensional spheres, except when the group is [[cyclic group of order 2|$\mathbb{Z}/2$]], hence when the action is by [[involutions]] (Rem. \ref{ZTwoActionsAreInvolutions} below), where the antipodal free action (Ex. \ref{ActionOfZModTwoByAntipodalInversion}) exists in all dimensions. Indeed, it holds in general that the only free actions of finite groups on even-dimensional spheres are [[involutions]] (Prop. \ref{OnlyZModTwoCanActFreelyOnEvenDimensionalSpheres} below), and, as in the canonical example, all free involutions on even-dimensional spheres are [[orientation]]-reversing, and those on odd-dimensional spheres are orientation-preserving (Prop. \ref{FreeZModTwoActionOnEvenDimSphereMustBeOrientationReversing} below).


While, therefore, all free involutions on a given $n$-sphere are [[homotopy|homotopic]] to the antipodal involution (Rem. \ref{FreeInvolutionsOnNSphereAllHaveTheSameHomotopyClass} below), at least in the [[categories]] of [[piecewise-linear structure|piecewise-linear]] and of [[smooth structure|smooth]] actions there are families of distinct exotic involutions on $n$-spheres (Ex. \ref{NonStandardFreeInvolutions} below).


\begin{proposition}
\label{OnlyZModTwoCanActFreelyOnEvenDimensionalSpheres}
**(only $\mathbb{Z}/2$ has free actions on even-dimensional spheres)**
\linebreak
  The only [[finite group]] with any [[free action|free]] [[G-space|continuous action]] on a [[sphere]] $S^{2n}$ of [[positive number|positive]] [[even number|even]] [[dimension of a manifold|dimension]] is [[cyclic group of order 2|$\mathbb{Z}_2$]].
\end{proposition}
\begin{proof}
  Given a fixed-point free-action, the [[quotient space]] [[coprojection]] 
  $S^{2n} \xrightarrow{q} S^{2n/G}$ is a [[covering space]] with [[degree of a continuous function|degree]] $deg(q) = ord(G)$ equal to the [[order of a group|order]] of $G$. Passing to [[Euler characteristics]] $\chi(-)$ and using that

1. $\chi(-)$ is always an [[integer]] (by definition);

1. $\chi(S^{2n}) = 2$ (by [this Prop.](Euler+characteristic#EulerCharacteristicOfSpheres));

1. $\chi(-)$ of any finite covering coprojection is multiplication by the degree ([this Prop.](Euler+characteristic#EulerCharacteristicOfCoveringSpaces))

we obtain the [[equation]]

$$
  2 
    \;=\; 
  \chi(S^{2n})
    \;=\;
  ord(G) \cdot \chi(S^{2n}/G)
  \,.
$$

The only solutions for this algebraic equation (over the [[integers]]) have $ord(G) \,\in\, \{1, 2\}$. But $ord(G) = 1$ implies that $G$ is the [[trivial group]], whose action certainly has fixed points. Hence the only admissible solution is $ord(G) = 2$ and the only group of that order is [[cyclic group of order 2|$\mathbb{Z}_2$]]. That this does have at least one fixed-point free action is Ex. \ref{ActionOfZModTwoByAntipodalInversion}.
\end{proof}
\begin{remark}
  The nature of the [[fixed loci]] of finite group actions on even-dimensional spheres is discussed in [Craciun 2013](#Craciun13).
\end{remark}

\begin{remark}
\label{ZTwoActionsAreInvolutions}
**([[cyclic group of order 2|$\mathbb{Z}/2$]]-[[group action|actions]] are equivalently [[involutions]])**
\linebreak
  Any [[group action]] of $\rho \,\colon\, \mathbb{Z}/2 \times S^n \to S^n$ of the [[cyclic group of order 2|$\mathbb{Z}/2$]] is determined by its value $\rho(\sigma) \,\colon\, S^n \to S^n$ on the single non-trivial element $\sigma \,\in\, \mathbb{Z}/2$, which is an [[involution]], and every involution corresponds to a unique $\mathbb{Z}/2$-action this way.
\end{remark}


\begin{proposition}
\label{FreeZModTwoActionOnEvenDimSphereMustBeOrientationReversing}
Every [[free action|free]] [[involution]]

* on an [[even number|even]]-dimensional sphere is [[orientation]]-reversing;

* on an [[even number|odd]]-dimensional sphere is [[orientation]]-preserving.

\end{proposition}
\begin{proof}
By the [[Lefschetz fixed point theorem]],
see [this example](Lefschetz+trace+formula#FixedPointTheoremForHomeomorphismsOfnSpheres) for details.
\end{proof}

\begin{remark}
\label{FreeInvolutionsOnNSphereAllHaveTheSameHomotopyClass}
  Prop. \ref{FreeZModTwoActionOnEvenDimSphereMustBeOrientationReversing} implies that the [[homotopy class]] of any fixed-point free [[involution]] $\sigma \,\colon\, S^{n} \to S^n$ is, as an element in the [[homotopy groups of spheres]],

* on an [[even number|even]]-dimensional $n$-sphere, $n = 2k$, equal to 

  $$  
    [\sigma] \,=\, - 1 \,\in\, \mathbb{Z} \,\simeq\, \pi_{2k}(S^{2k})
  $$

* on an [[odd number|odd]]-dimensional $n$-sphere, $n = 2k+1$, equal to 

  $$  
    [\sigma] \,=\, + 1 \,\in\, \mathbb{Z} \,\simeq\, \pi_{2k+1}(S^{2k+1}) 
    \,.
  $$

which means that every free involution on any $n$-sphere is [[homotopy|homotopic]] to the antipodal involution (Ex.\ref{ActionOfZModTwoByAntipodalInversion}).
\end{remark}
Nevertheless, there are in general several involutions on any given $n$-sphere which are *not* [[isomorphism|isomorphic]] to the antipodal involution as $\mathbb{Z}/2$-actions, certainly if regarded in the category of smooth (or just piecewise-linear) actions:

\begin{example}
\label{NonStandardFreeInvolutions}
**(non-standard free smooth involutions on $n$-spheres)**
\linebreak
There are, in the [[category]] [[smooth function|smooth]] $\mathbb{Z}/2$-[[group action|actions]], up to [[isomorphism]]:

* a single free involution on the [[3-sphere]] $S^3$ (hence the antipodal Ex. \ref{ActionOfZModTwoByAntipodalInversion})

  ([Livesay 1960](#Livesay60))

* at least 2 distinct free involutions on the [[4-sphere]] $S^4$

  ([Fintushel & Stern 1981](#FintushelStern81))

* 4 distinct free involutions on the [[5-sphere]] [[5-sphere|$S^5$]]

* 4 distinct free involutions on the [[6-sphere]] [[6-sphere|$S^6$]]

* $card(\mathbb{Z}/2 \oplus \mathbb{Z}/28 \oplus \mathbb{Z})$ distinct free involutions on the [[7-sphere]] [[7-sphere|$S^7$]]

  ([López de Medrano, Sec. V.6.1](#LopezdeMedrano71))

\end{example}
Here all spheres are equipped with their standard smooth structure (?), it is just the extra involutions which are non-standard.


#### General obstructions and existence
 {#GeneralObstructionToAndExistenceOfFreeActions}

Not all [[finite groups]] have any free continuous action on any $n$-sphere: One [[obstruction]] is Smith's "$p^2$-condition" (Prop. \ref{SmithPSquareCondition} below), another is Milnor's "$2 p$-condition". But these are the only two obstructions, and a finite group that evades these is guaranteed to act not just continuously on a sphere of a single dimension, but smoothly on spheres of any dimension which is a multiple of its [[Artin-Lam induction exponent]] (Prop. \ref{MadsenThomasWallTheorem} below).

\begin{proposition}
\label{SmithPSquareCondition}
**(Smith's $p^2$-condition)**
\linebreak
  For $p$ a [[prime number]],
  the [[direct product group]] $\mathbb{Z}/p \times \mathbb{Z}/p$ and more generally the higher powers $(\mathbb{Z}/p)^{\geq 2}$ of the prime [[cyclic group]] do *not* have any [[G-space|continuous]] [[free action]] on any [[n-sphere]].
\end{proposition}
([Smith 1944, p. 107 (4 of 5)](#Smith44))

\begin{remark}
By the [[fundamental theorem of finitely generated abelian groups]], 
Prop. \ref{SmithPSquareCondition} immediately implies that if a [[finite group]] has any [[G-space|continuous]] [[free action]] on any [[n-sphere]], then it must satisfy the condition that all its [[subgroups]] of [[order of a group|order]] $p^2$ are [[cyclic group|cyclic]], i.e. [[isomorphism|isomorphic]] to $\mathbb{Z}/p^2$. 

This condition has come to be called the "$p^2$-condition" (Def. \ref{pqCondition} below).
\end{remark}


\begin{definition}\label{pqCondition}
**($p q$ condition)**
For $p, q$ a [[pair]] of [[prime numbers]], not necessarily distinct, 
a [[finite group]] $G$ is said to satisfy the *$p q$-condition* if all [[subgroups]] of [[order of a group|order]] $p \cdot q$ are [[cyclic groups]]:
$$
  H \,\subset\, G
  \;\;\;
  \text{with}
  \;\;\;
  ord(H) \,=\, p q
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  H \,\simeq\, \mathbb{Z}/(p q)
  \,.
$$ 
\end{definition}

\begin{proposition}\label{EquivalentVersionsOfPSquareCondition}
**(equivalent statements of the $p^2$-condition)
\linebreak
  For a [[finite group]] $G$, the following are equivalent: 

  1. For all [[prime numbers]] $p$, $G$ satisfies the $p^2$-condition (Def. \ref{pqCondition}).

  1. For all [[prime number|primes]] $p$,  the $p$-[[Sylow subgroup]] of $G$ is either cyclic or (if $p = 2$) [[generalized quaternion group|generalized quaternion]].

  1. $G$ has "periodic cohomology" in that there exists $k \in \mathbb{N}$ such that its [[integral cohomology|integral]] [[group cohomology]] [[cohomology groups|group]] in degree $k$ is [[cyclic group|cyclic]]:

     $$
       \underset{k \in \mathbb{N}}{\exists}
       \;
       \underset{N_k \in \mathbb{N}}{\exists}
       \;\;
       H^k_{grp}(G;\, \mathbb{Z}) \,\simeq\, \mathbb{Z}/_{n_k}
     $$ 

     In this case the possible "periods" $k$ form a [[subgroup]] of $\mathbb{Z}$ ([Cartan & Eilenberg 1956, p. 261 (283 of 421)](homological+algebra#CartanEilenberg), with $H^{-k}(G;\, \mathbb{Z}) \coloneqq H_k(G;\, \mathbb{Z})$ by [p. 232 (254 of 421)](homological+algebra#CartanEilenberg)) 

1. Every [[abelian group|abelian]] [[subgroup]] of $G$ is [[cyclic group|cyclic]].

\end{proposition}
([Cartan & Eilenberg 1956, Thm. IV 11.6, p. 262 (284 of 421)](homological+algebra#CartanEilenberg))


\begin{proposition}\label{MadsenThomasWallTheorem}
**(Madsen-Thomas-Wall theorem)**
\linebreak
  A [[finite group]] $G$ has a [[G-space|continuous]] [[free action]] on some [[n-sphere]] if and only if it satisfies 

1. the $p^2$-condition (see Prop. \ref{EquivalentVersionsOfPSquareCondition})

1. the $2 p$-condition 

for all [[prime numbers]] $p$ (Def. \ref{pqCondition}).

In this case there exists also a [[smooth structure]] on some [[n-sphere]] (possibly an [[exotic smooth structure]]) such that $G$ has a [[smooth function|smooth]] [[free action]] on it.

Specifically, such free smooth actions exist in particular on all $S^n$ for which $n+1$ is any multiple of the [[Artin-Lam induction exponent]], hence exist on spheres of arbitrarily large dimension.
\end{proposition}

([Madsen, Thomas and Wall 1976, Thm. 0.5-0.6](#MadsenThomasWall76), [1983, Thm. 5](#MadsenThomasWall83), reviewed in [Hambleton 2014, Thm. 6.1](#Hambleton14))

\linebreak


### Fixed loci of the circle group acting on spheres

+-- {: .num_prop}
###### Proposition

Given an continuous [[action]] of the [[circle group]] on the [[topological space|topological]] [[4-sphere]], its [[fixed point]] space is of one of two types:

1. either it is the [[0-sphere]] $S^0 \hookrightarrow S^4$

1. or it has the [[rational homotopy theory|rational homotopy type]] of an even-dimensional sphere.

=--

([Félix-Oprea-Tanré 08, Example 7.39](#FelixOpreaTanre08))


(...)

## References

### Characterization of finite free actions by homeomorphisms

The non-existence of free actions of $(\mathbb{Z}/p)^{\geq 2}$ on any [[n-sphere]]:

* {#Smith44} P. A. Smith, *Permutable Periodic Transformations*, Proceedings of the National Academy of Sciences of the United States of America Vol. 30, No. 5 (May 15, 1944), pp. 105-108 ([jstor:87918](https://www.jstor.org/stable/87918))

Discussion of [[free actions|free]] [[group actions on spheres]] by [[finite groups]]:

* {#Wall78} [[C. T. C. Wall]], _Free actions of finite groups on spheres_, Proceedings of Symposia in Pure Mathematics, Volume 32, 1978 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/wall7.pdf))

* {#MadsenThomasWall76} [[Ib Madsen]], [[Charles B. Thomas]], [[C. T. C. Wall]], *The topological spherical space form problem II: existence of free actions*, Topology Volume 15, Issue 4, 1976, Pages 375-382 (<a href="https://doi.org/10.1016/0040-9383(76)90031-8">doi:10.1016/0040-9383(76)90031-8</a>)

* {#MadsenThomasWall83} [[Ib Madsen]], [[Charles B. Thomas]], [[C. T. C. Wall]], *Topological spherical space form problem III: Dimensional bounds and smoothing*,  Pacific J. Math. 106(1): 135-143 (1983) ([pjm:1102721110](https://projecteuclid.org/journals/pacific-journal-of-mathematics/volume-106/issue-1/Topological-spherical-space-form-problem-III-Dimensional-bounds-and-smoothing/pjm/1102721110.full))

Discussion of free actions on [[product topological space|products]] of spheres:

* [[Alejandro Adem]], _Constructing and deconstructing group actions_, in [[Paul Goerss]], [[Stewart Priddy]], *Homotopy Theory: Relations with Algebraic Geometry, Group Cohomology, and Algebraic K-Theory*, Contemporary Mathematics **346** AMS 2004 ([arXiv:0212280](http://arxiv.org/abs/math/0212280), [doi:10.1090/conm/346](http://dx.doi.org/10.1090/conm/346))

Discussion of the fixed point-sets of finite group actions on even-dimensional spheres:

* {#Craciun13} Gheorghe Craciun, *Most homeomorphisms with a fixed point have a Cantor set of fixed points*, Archiv der Mathematik volume 100, pages 95–99 (2013) ([doi:10.1007/s00013-012-0466-z](https://doi.org/10.1007/s00013-012-0466-z))

### Classification of free involutions:

* {#Livesay60} [[G. R. Livesay]]  *Fixed Point Free Involutions on the 3-Sphere*, Annals of Mathematics Second Series, Vol. 72, No. 3 (Nov., 1960), pp. 603-611 ([jstor:1970232](https://www.jstor.org/stable/1970232))

* {#LopezdeMedrano71} [[Santiago López de Medrano]], *Involutions on Manifolds*,  Ergebnisse der Mathematik und ihrer Grenzgebiete **59**, Springer 1971 ([doi:10.1007/978-3-642-65012-3](https://link.springer.com/book/10.1007/978-3-642-65012-3))

* {#FintushelStern81} [[Ronald Fintushel]], [[Ronald J. Stern]], *An Exotic Free Involution on $S^4$*, Annals of Mathematics Second Series, Vol. 113, No. 2 (Mar., 1981), pp. 357-365 ([jstor:2006987](https://www.jstor.org/stable/2006987))

### Classification of finite free actions by isometries

Classification of free finite group actions by [[isometries]], hence with [[quotient spaces]] being [[spherical space forms]]:

* {#Wolf74} [[Joseph Wolf]], _Spaces of constant curvature_, Third ed.: Publish or Perish, Boston, 1974, Sixth edition: AMS Chelsea Publishing 2011 ([doi:10.1090/chel/372](https://doi.org/10.1090/chel/372))

review:

* {#Hambleton14} [[Ian Hambleton]], _Topological spherical space forms_, Handbook of Group Actions (Vol. II), ALM 32 (2014), 151-172. International Press, Beijing-Boston ([arXiv:1412.8187](https://arxiv.org/abs/1412.8187))

streamlined re-proof:

* {#Allock15} [[Daniel Allcock]], _Spherical space forms revisited_, Trans. Amer. Math. Soc. 370 (2018), 5561-5582  ([arXiv:1509.00906](https://arxiv.org/abs/1509.00906), [doi:10.1090/tran/7167](https://doi.org/10.1090/tran/7167))


The subgroups of [[special orthogonal group|SO(8)]] which act freely on $S^7$ have been classified in [Wolf 1974](#Wolf74) and lifted to actions of [[Spin group|Spin(8)]] in 

* {#Gadhia07} [[Sunil Gadhia]], _Supersymmetric quotients of M-theory and supergravity backgrounds_, PhD thesis, School of Mathematics, University of Edinburgh, 2007 ([spire:1393845](http://inspirehep.net/record/1393845/))


Further discussion of these actions of $Spin(8)$ on the [[7-sphere]] is in

* {#MFFGME09} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Sunil Gadhia]], [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))

where they are related to the [[black brane|black]] [[M2-brane]] [[BPS state|BPS]]-solutions of [[11-dimensional supergravity]] at [[ADE-singularities]].

### Discussion of circle-actions

Discussion of [[circle group]]-actions on spheres:

* {#FelixOpreaTanre08} [[Yves Félix]], [[John Oprea]], [[Daniel Tanré]], _Algebraic Models in Geometry_, Oxford University Press 2008


[[!redirects group action on spheres]]

[[!redirects free group actions on spheres]]
[[!redirects free group action on spheres]]

[[!redirects group action on an n-sphere]]
[[!redirects group actions on an n-sphere]]

[[!redirects group action on n-spheres]]
[[!redirects group actions on n-sphere]]

[[!redirects group action on n-spheres]]
[[!redirects group actions on n-spheres]]

[[!redirects free group actions on n-spheres]]
[[!redirects free group action on n-spheres]]


