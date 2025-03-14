
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _cubical structure_ on a [[complex line bundle]] over an [[abelian group]] is a certain trivialization of a certain induced line bundle on the 3-fold Cartesian product ("cube") of the group which is constructed in a kind of cubical generalization of the [[polarization identity]] formula for [[quadratic forms]].

Over [[formal groups]] associated with [[complex oriented cohomology theories]] cubical structures encode [[orientation in generalized cohomology]].


## Definition

+-- {: .num_defn}
###### Definition

Given a [[circle group]]-[[principal bundle]]/[[complex line bundle]] $\mathcal{L}$ on an [[abelian group]] $A$, write $\Theta(\mathcal{L})$ for the line bundle on $G^3$ which is given by the formula

$$
  \Theta(\mathcal{L})_{x,y,z}
  =
  \mathcal{L}_{x+y+z} \otimes \mathcal{L}_{x+y}^{-1} \otimes \mathcal{L}_{x+z}^{-1} \otimes \mathcal{L}_{y+z}^{-1} \otimes \mathcal{L}_x \otimes \mathcal{L}_y \otimes \mathcal{L}_z \otimes \mathcal{L}_0^{-1}
  \,.
$$

=--

+-- {: .num_defn #CubicalStructure}
###### Definition

A _cubical structure_ on $\mathcal{L}$ is a trivializing [[section]] $s$ of $\Theta(\mathcal{L})$ such that

1. $s(0,0,0) = 1$

1. $s(x_{\sigma(1)}, x_{\sigma(2)}, x_{\sigma(3)}) = s(x_1, x_2, x_3)$

1. $s(w+x,y,z) s(w,x,z) = s(w,x + y, z) s(x,y,z)$

for all elements of $A$ as indicated, and for all [[permutations]] $\sigma$ of three elements. Here the equalities are equalities of sections after applying the canonical [[isomorphisms]] of [[complex lines]] on both sides.

=--

([Breen 83](#Breen83), [Hopkins 94, section 4](#Hopkins94), [Ando-Hopkins-Strickland 01, def. 2.40](#AndoHopkinsStrickland01))

+-- {: .num_remark}
###### Remark

The canonical isomorphsms hidden in def. \ref{CubicalStructure} are:

1. $\mathcal{L}_0^{\otimes 3} \otimes (\mathcal{L}_0^{-1})^{\otimes 3} \to 1$ the canonical map exhibiting $\mathcal{L}_0^{-1}$ as the inverse ([[dual object]]) of $\mathcal{L}_0$:

1. etc.

=--

There is the following further refinement.

+-- {: .num_defn }
###### Definition

In the situation of def. \ref{CubicalStructure}, if the line bundle $\mathcal{L}$ is equipped with a natural "symmetry"

$$
  t \colon \mathcal{L}_x \stackrel{\simeq}{\longrightarrow} \mathcal{L}_{-x}
$$

then a _$\Sigma$-structure_ on $\mathcal{L}$ is a cubical structure, def. \ref{CubicalStructure}, such that in addition

$$
  s(x,y , -x-y) = 1
 \,.
$$


=--

## Examples

### Relation to orientations in complex-oriented cohomology theory

For $E$ a [[multiplicative cohomology theory|multiplicative]] [[weakly periodic cohomology theory|weakly periodic]] [[complex orientable cohomology theory]], we have that $Spec E^0(B U\langle 6\rangle)$ is naturally equivalent to the space of cubical structures on the trivial line bundle over the [[formal group]] of $E$.

In particular, [[homotopy classes]] of [[morphisms]] of [[E-infinity ring]] spectra $MU\langle 6\rangle \to E$ from the [[Thom spectrum]] to $E$, and hence universal $MU\langle 6\rangle$-[[orientation in generalized cohomology|orientations]] (see there) of $E$ are in natural bijection with these cubical structures.

([Hopkins 94, theorem 6.1, 6.2](#Hopkins94), [Ando-Hopkins-Strickland 01, corollary 2.50](#AndoHopkinsStrickland01))

This way for instance the [[string orientation of tmf]] has been constructed. See there for more on this.

### On the 11-dimensional Chern-Simons term

The [[higher dimensional Chern-Simons theory|11-dimensional Chern-Simons]] [[action functional]] in [[11-dimensional supergravity]] gives a line bundle $L$ on the space of [[supergravity C-fields]] whose $\Theta^3(L)$ is the [[transgression]] of the [[cup product in ordinary differential cohomology]] of three factors. It seems that each trivialization of the class of the [[supergravity C-field]] induces a "cubical" trivialization of $\Theta^3(L)$ as above, and hence a cubical structure on $L$. See at _[[cubical structure in M-theory]]_ for more on this.

## Related concept

* [[theta characteristic]]

## References

An early reference discussing the relation with [[theta functions]] is

* {#Breen83} [[Lawrence Breen]], _Fonctions th&#234;ta et th&#233;or&#232;me du cube_, Springer Lecture Notes in Mathematics **980** (1983). ([MR0823233](http://www.ams.org/mathscinet-getitem?mr=823233)).

In relation to [[orientation in generalized cohomology]] cubical structures have been prominently discussed in 

* {#Hopkins94} [[Michael Hopkins]], _Topological modular forms, the Witten genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&#252;rich, 1994) (Basel), Birkh&#228;user, 1995, 554&#8211;565. MR 97i:11043 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

* {#AndoHopkinsStrickland01} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _Elliptic spectra, the Witten genus and the theorem of the cube_, Invent. Math. 146 (2001) 595&#8211;687 MR1869850 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/musix.pdf))

[[!redirects cubical structures on a line bundle]]
[[!redirects cubical structures on line bundles]]

[[!redirects cubical structure on a complex line bundle]]
[[!redirects cubical structures on a complex line bundle]]