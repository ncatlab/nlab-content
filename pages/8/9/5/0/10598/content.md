
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
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

The concept of _$G$-CW  complex_ is to that of [[CW-complexes]] as [[topological G-spaces]] are to [[topological spaces]]: for $G$ a [[compact topological group]], the notion of _$G$-CW-complex_ is much like that of [[CW-complex]], only that where in the latter case one builds a [[topological space]] from gluing of [[disks]] $D^n$ ("[[cell complex|cells]]") for a $G$-CW-complex one glues [[products]] ([[product topological spaces]]) of [[disks]] with $G$-[[orbits]] $G/H$ ([[coset spaces]]) for [[compact Lie group|compact]] [[subgroups]] $H$.

These are [[cofibrant objects]] in the $G$-[[fine model structure on topological G-spaces]].

## Definition

Let the [[equivariance group]] $G$ be [[topological group]] (typically required to be a [[compact Lie group]], see [there](compact+Lie+group#InEquivariantHomotopyTheory)).

As $H \underset{clsd}{\subset} G$ ranges over its [[closed subgroups]], consider the [[coset spaces]] $G/H$ as [[G-spaces]] with respect to the residual left multiplication action by $G$, and regard its [[product spaces]] $S^n \times G/H$ and $D^n \times G/H$ with the [[n-sphere]] and the [[n-disk]], respectively, for the latter equipped with the [[trivial action]].

This way, the canonical [[boundary of a manifold|boundary]] inclusions 
$$
  \iota_n 
    \,\colon\, 
  S^{n-1} \xhookrightarrow{\phantom{--}} D^n
$$ 
considered for ordinary [[CW-complexes]] induces $G$-[[equivariant maps]]

\[
  \label{GeneratingEquivariantCofibrations}
  S^{n-1}
  \times G/H
  \xhookrightarrow{
    \phantom{-}
    \iota_n \times id_{G/H}
    \phantom{-}
  }
  D^n \times G/H
  \,,\;\;\;\;\;\;
  n \in \mathbb{N}
  ,\,
  H \underset{clsd}{\subset} G
  \,.
\]

\begin{definition} 
  A *$G$-CW-complex* $X$ is a [[G-space]] [[isomorphism|isomorphic]] to the result of a [[sequence]], [[monotone function|monotone]] in cell dimension $n$, of [[cell attachments]] via the $G$-equivariant attaching maps (eq:GeneratingEquivariantCofibrations).
\end{definition}




\begin{remark}\label{FiniteGroupCWComplexesAreCWComplexesWithCellularGAction}
  For [[finite group|finite]] [[equivariance groups]] $G$, a $G$-CW-complex structure may be identified with 

* a plain [[CW-complex]]-structure 

* on which the $G$-[[group action|action]] is [[cell complex|cellular]] (sends $n$-cells onto $n$-cells, respecting their boundaries) 

* which on cells that are sent to themselves actually restricts to the [[identity function|identity]] (i.e. cells that are fixed under the action are actually fixed point-wise).

This special case was the original definition on [Bredon 1967b, I.1](#Bredon67b).
\end{remark}

## Examples

### $G$-Manifolds
  {#GManifolds}

The _[[equivariant triangulation theorem]] says that
if a [[compact Lie group]] $G$ acts on a [[compact topological space|compact]] [[smooth manifold]] $X$, then the manifold admits an [[equivariant triangulation]]. In particular:

\begin{proposition}\label{GManifoldsAreGCWComplexes}
For $G$ a [[compact Lie group]], every [[closed manifold|closed]] [[smooth manifold|smooth]] [[G-manifold]] admits the structure of a G-CW complex. 
\end{proposition}
This is due to [Matumoto 72, Prop. 4.4](#Matumoto72), [Illman 72a, Thm. 3.1, Cor. 4.1](#Illman72a), [Illman 72b, Thm. 2.6](#Illman72), [Illman 73, Thm. 2.1](#Illman73), [Illman 83, Thm. 7.1, Cor. 7.2](equivariant+triangulation+theorem#Illman83) -- review in [ALR 07, theorem 3.2](#ALR07), see also [Waner 80, p. 6](#Waner80).

Moreover, if the manifold does have a [[manifold with boundary|boundary]], then its G-CW complex may be chosen such that the boundary is a G-subcomplex. ([Illman 83, last sentence above theorem 7.1](equivariant+triangulation+theorem#Illman83))

In particular:

+-- {: .num_prop #RepresentationSpheresAreGCWComplexes}
###### Proposition
**([[G-representation spheres are G-CW-complexes]])**

For $G$ a [[compact Lie group]] (e.g. a [[finite group]]) and $V \in RO(G)$ a [[finite dimensional vector space|finite-dimensional]] [[orthogonal group|orthogonal]] $G$-[[linear representation]], the [[representation sphere]] $S^V$ admits the structure of a [[G-CW-complex]].

=--

### $G$-Surfaces
 {#ExamplesGSurfaces}

Simple examples of [[G-manifolds]] ([above](#GManifolds)) are [[surfaces]] with $G$-action.

\begin{example}
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with the [[cyclic group of order 2|$\mathbb{Z}_{/2}$]]-[[group action|action]] which [[reflection at a hyperplane|reflects]] one of the two [[coordinate]] axes:

\begin{imagefromfile}
    "file_name": "ReflectionTorusCellStructure.png",
    "width": 470,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}



## Properties

### Closure properties

\begin{proposition}\label{ClosureUnderProductsForFiniteGroups}
  For $G$ (at least) a [[finite group]] , the [[product]] of two $G$-CW-complexes in [[compactly generated weak Hausdorff spaces]] is itself a $G$-CW-complex.
\end{proposition}
\begin{proof}
  Since for finite $G$, a $G$-CW complex is the same as a plain [[CW-complex]] equipped with a [[cell complex|cellular]] [[group action|action]] by $G$ (Rem. \ref{FiniteGroupCWComplexesAreCWComplexesWithCellularGAction}) it is clear that for this structure to be preserved by the product operation it is sufficient that the products of underlying cells constitute a CW-complex, hence that products preserve CW-complexes in compactly generated Hausdorff spaces. That is this the case is [this Proposition](CW+complex#ClosureOfCWComplexesUnderCartesianProduct).
\end{proof}

### Equivariant cellular approximation

See at _[[equivariant cellular approximation theorem]]_.

### Equivariant CW-approximation

See at _[[G-CW approximation]]_.

### Equivariant Whitehead theorem

See at _[[equivariant Whitehead theorem]]_.

### Elmendorf's theorem

See at _[[Elmendorf's theorem]]_.


## References

The notion of G-CW complexes is, for the case of [[finite groups]] $G$, due to

* {#Bredon67b} [[Glen Bredon]], Section I.1. of _[[Equivariant cohomology theories]]_, Springer Lecture Notes in Mathematics Vol. 34. 1967 ([doi:10.1007/BFb0082690](https://link.springer.com/book/10.1007/BFb0082690))

announced in

* {#Bredon67a} [[Glen Bredon]], _Equivariant cohomology theories_, Bull. Amer. Math. Soc. Volume 73, Number 2 (1967), 266-268. ([educlid:1183528794](https://projecteuclid.org/euclid.bams/1183528794))

In the broader generality of general [[topological groups]] and specifically of [[compact Lie groups]], the notion of G-CW-complexes and their [[equivariant Whitehead theorem]] is due to:

* {#Matumoto71} [[Takao Matumoto]], _On $G$-CW complexes and a theorem of JHC Whitehead_, J. Fac. Sci. Univ. Tokyo Sect. IA **18** (1971) 363-374 &lbrack;[irdb:00926/0001786419](https://irdb.nii.ac.jp/en/00926/0001786419), [[matumoto.pdf:file]]&rbrack;

*  {#Matumoto72} [[Takao Matumoto]], _Equivariant K-theory and Fredholm operators_, J. Fac. Sci. Tokyo 18 (1971/72), 109-112 ([pdf](https://repository.dl.itc.u-tokyo.ac.jp/?action=repository_action_common_download&item_id=39826&item_no=1&attribute_id=19&file_no=1), [[MatumotoEquivariantKTheory.pdf:file]])

and, independently, due to:

* {#Illman72a} [[Sören Illman]], Chapter I of: *Equivariant algebraic topology*, Princeton University 1972 ([[Illman_EquivariantAlgebraicTopology1972.pdf:file]])

* {#Illman72b} [[Sören Illman]], Section 2 of: *Equivariant singular homology and cohomology for actions of compact lie groups* ([doi:10.1007/BFb0070055](https://doi.org/10.1007/BFb0070055)) In: H. T. Ku, L. N. Mann, J. L. Sicks, J. C. Su (eds.), *Proceedings of the Second Conference on Compact Transformation Groups* Lecture Notes in Mathematics, vol 298. Springer 1972 ([doi:10.1007/BFb0070029](https://link.springer.com/book/10.1007/BFb0070029))

* {#Illman73} [[Sören Illman]], Section 2 of: *Equivariant algebraic topology*, Annales de l'Institut Fourier, Tome 23 (1973) no. 2, pp. 87-91 ([doi:10.5802/aif.458](https://doi.org/10.5802/aif.458))


(Which, in hindsight and with [[Elmendorf's theorem]], gives a deeper justification for the parametrization over the [[orbit category]] already proposed in [Bredon 67a](#Bredon67a), [Bredon 67b](#Bredon67b).)

* {#Waner80} [[Stefan Waner]], _Equivariant Homotopy Theory and Milnor's Theorem_, Transactions of the American Mathematical Society Vol. 258, No. 2 (Apr., 1980), pp. 351-368 ([JSTOR](http://www.jstor.org/stable/1998061))

Proof that $G$-[[absolute neighbourhood retract|ANRs]] have the [[equivariant homotopy type]] of [[G-CW-complexes]] (for $G$ a [[compact Lie group]]):

* {#Kwasik81} [[Slawomir Kwasik]], _On the Equivariant Homotopy Type of $G$-ANR's_, Proceedings of the American Mathematical Society Vol. 83, No. 1 (Sep., 1981), pp. 193-194 (2 pages) ([jstor:2043921](https://www.jstor.org/stable/2043921))

Textbook accounts:

* {#tomDieck87} [[Tammo tom Dieck]], Sections I.1 and I.2 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))

* {#Lueck89} [[Wolfgang Lück]], Sections I.1, I.2 of: _Transformation Groups and Algebraic K-Theory_, Lecture Notes in Mathematics **1408** (Springer 1989) ([doi:10.1007/BFb0083681](https://doi.org/10.1007/BFb0083681))

* {#May96} [[Peter May]] et al., Section I.3 of:  _Equivariant homotopy and cohomology theory_, CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996 ([ISBN: 978-0-8218-0319-6](https://bookstore.ams.org/cbms-91/?startBookmarkIdx=200)  [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/alaska1.pdf), [[MayEtAlEquivariant96.pdf:file]])


Lecture notes:

* {#Blumberg17} [[Andrew Blumberg]], _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))




[[!redirects G-CW complexes]]

[[!redirects G-CW-complex]]
[[!redirects G-CW-complexes]]

[[!redirects G-cell complex]]
[[!redirects G-cell complexes]]
