

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

### Free actions by finite groups on spheres

\begin{example}
\label{ActionOfZModTwoByAntipodalInversion}
**(action of $\mathbb{Z}/2$ by antipodal inversion)**
\linebreak
  For all $n \in \mathbb{N}$, the group [[cyclic group of order 2|$\mathbb{Z}/2$]] has a [[continuous function|continuous]] [[free action]]  on the [[n-sphere]], given by [[antipode|antipodal]] reflection (hence reversing the [[orientation]]).

The [[topological quotient space]] of this action is the [[real projective space]] $S^{n+1}/(\mathbb{Z}/2) \,\simeq\, \mathbb{R}P^n$.
\end{example}

\begin{example}
  For every [[finite subgroup of SU(2)]] $G \,\subset\, $  [[SU(2)]] $\simeq$ [[Sp(1)]] its [[quaternion|quaternionic]] left-multiplication action on the [[$4n+3$-sphere|n-sphere]], regarded as the [[unit sphere]] in the [[quaternion|quaternionic]] $n$-space
$$
  S^{4n+3} 
    \,\simeq\,
  S\big(\mathbb{R}^{4n+4}\big)
    \,\simeq\,
  S\big(\mathbb{H}^{n+1}\big)
$$
\end{example}

\begin{proposition}
  For $p$ a [[prime number]],
  the [[direct product group]] $\mathbb{Z}/p \times \mathbb{Z}/p$ and more generally the higher powers $(\mathbb{Z}/p)^{\geq 2}$ do *not* have any continuous [[free action]] on any [[n-sphere]]
\end{proposition}
([Smith 1944, p. 107 (4 of 5)](#Smith44))

\begin{proposition}
\label{OnlyZModTwoCanActFreelyOnEvenDimensionalSpheres}
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
  The nature of the  [[fixed loci]] of other finite group actions on even-dimensional spheres is discussed in [Craciun 2013](#Craciun13).
\end{remark}


### Spherical space forms

Let $G$ be a [[discrete group]] and $\rho$ an [[action]] of $G$ on the [[n-sphere]] by [[isometries]], which is [[free action|free]] and [[properly discontinuous action|properly discontinuous]].

The induced [[quotient spaces]] $S^n/G$ in this case are also called _[[spherical space forms]]_.


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

The non-existence of free actions of $(\mathbb{Z}/p)^{\geq 2}$ on any $n$-sphere:

* {#Smith44} P. A. Smith, *Permutable Periodic Transformations*, Proceedings of the National Academy of Sciences of the United States of America Vol. 30, No. 5 (May 15, 1944), pp. 105-108 ([jstor:87918](https://www.jstor.org/stable/87918))

Discussion of [[free actions|free]] [[group actions on spheres]] by [[finite groups]]:

* {#Wall78} [[C. T. C. Wall]], _Free actions of finite groups on spheres_, Proceedings of Symposia in Pure Mathematics, Volume 32, 1978 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/wall7.pdf))

* [[Alejandro Adem]], _Constructing and deconstructing group actions_ ([arXiv:0212280](http://arxiv.org/abs/math/0212280))

Discussion of the fixed point-sets of finite group actions on even-dimensional spheres:

* {#Craciun} Gheorghe Craciun, *Most homeomorphisms with a fixed point have a Cantor set of fixed points*, Archiv der Mathematik volume 100, pages 95–99 (2013) ([doi:10.1007/s00013-012-0466-z](https://doi.org/10.1007/s00013-012-0466-z))


Discussion of [[circle group]]-actions on spheres includes

* {#FelixOpreaTanre08} [[Yves Félix]], John Oprea, Daniel Tanré, _Algebraic Models in Geometry_, Oxford University Press 2008


The subgroups of [[special orthogonal group|SO(8)]] which act freely on $S^7$ have been classified in 

* {#Wolf74} [[Joseph Wolf]], _Spaces of constant curvature_, Publish or Perish, Boston, Third ed., 1974

and lifted to actions of [[Spin group|Spin(8)]] in 

* {#Gadhia07} [[Sunil Gadhia]], _Supersymmetric quotients of M-theory and supergravity backgrounds_, PhD thesis, School of Mathematics, University of Edinburgh, 2007 ([spire:1393845](http://inspirehep.net/record/1393845/))


Further discussion of these actions of $Spin(8)$ on the [[7-sphere]] is in

* {#MFFGME09} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Sunil Gadhia]], [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))

where they are related to the [[black brane|black]] [[M2-brane]] [[BPS state|BPS]]-solutions of [[11-dimensional supergravity]] at [[ADE-singularities]].


[[!redirects group action on spheres]]

[[!redirects group action on an n-sphere]]
[[!redirects group actions on an n-sphere]]

[[!redirects group action on n-spheres]]
[[!redirects group actions on n-sphere]]

[[!redirects group action on n-spheres]]
[[!redirects group actions on n-spheres]]
