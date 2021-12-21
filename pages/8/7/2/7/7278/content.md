
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

A multiple [[loop space]].

A grouplike [[E-k algebra]] in [[Top]].

An [[iterated loop space object]] in [[Top]].

## Properties

### Higher group structure

See at _[[May recognition theorem]]_.

### Homotopy
 {#Homotopy}


\begin{prop}\label{IteratedLoopSpaceAsHomotopyFiberOfMappingSpace}
 For $A$ a [[pointed homotopy type]], hence an [[∞-groupoid]] equipped with a base point $\ast \xrightarrow{ pt_A } A$,
then for $n \,\in\, \mathbb{N}$, the [[iterated loop space|n-fold loop space]] of $A$ is the [[homotopy fiber]] of the basepoint-[[evaluation map]] on the [[mapping space]] from the [[homotopy type]] of the [[n-sphere]]:
$$
  \Omega^n A
  \xrightarrow{ hofib(ev_{\ast}) }
  Maps
  \big( 
    &#643; S^n 
    ,\,
    A
  \big)
  \xrightarrow{ ev_\ast }
  A
$$
\end{prop}
\begin{proof}
  We may [[presentable (infinity,1)-category|present]] the sequence in the [[classical model structure on topological spaces]] or the [[classical model structure on simplicial sets]], in the latter case we may assume that $A$  is presented by a [[Kan complex]], so that, in either case, it is a [[fibrant object]].

In either case, the canonical model for the [[iterated loop space]] is evidently the ordinary [[1-category]]-theoretic [[fiber]] of the [[evaluation map]] out of the [[internal hom]]:
$$
  \Omega^n A
  \xrightarrow{ ev_\ast }
  Maps( &#643; S^d ,\, A )
  \xrightarrow{ ev_\ast }
  A
  \,.
$$
Moreover, the evaluation map is equivalently the image of the point inclusion under the [[internal hom]]-functor
$$
  ev_\ast 
  \;=\;
  Maps( \ast \to S^n ,\, A )
  \,.
$$
Since either model category is a [[cartesian closed category|cartesian closed]] [[monoidal model category]], hence an [[enriched model category]] over itself ([this Exp.](enriched+model+category#TheClassicalModelCategoriesOfTopSpacesAndSimpSets))
and since the canonical model for $\ast \to &#643;  S^n$ is a [[cofibration]], in either case, the [[pullback-power axiom]] implies that $ev_\ast$ is a [[fibration]]. Therefore its ordinary fiber above models the [[homotopy fiber]], and the claim follows.
\end{proof}
\begin{corollary}\label{LESOfHomotopyGroupswithMappingSpace}
The [[homotopy groups]] of the [[mapping space]] $Maps(&#643;  S^n ,\, A)$ out of an [[n-sphere]] form a [[long exact sequence]] with those of $A$, of the following form:
\begin{tikzcd}[column sep=10pt]
    \cdots
    \ar[r]
    &
    \pi_{\bullet + 1}(A)
    \ar[rr]
    &&
    \pi_{\bullet+d}(A)
    \ar[
      rr
    ]
    &&
    \pi_{ \bullet }
    \big(
      \mathrm{Maps}
      ( 
        S^n 
        \,
         A 
      )
    \big)
    \ar[
      rr
    ]
    &&
    \pi_{\bullet}(A)
    \ar[
      rr
    ]
    &&
    \pi_{\bullet + d-1}(A)
    \ar[r]
    &
    \cdots
\end{tikzcd}
\end{corollary}
\begin{proof}
  This is the [[long exact sequence of homotopy groups]] 
  applied to the [[homotopy fiber sequence]]
  from Prop. \ref{IteratedLoopSpaceAsHomotopyFiberOfMappingSpace}.
\end{proof}

\begin{example}
  If $A \,\in\, Grp_\infty$ is [[n-truncated object of an (infinity,1)-category|n-truncated]], then the [[evaluation map]] out of the [[mapping space]] from the [[n-sphere|(n+2)-sphere]] into it is a [[weak homotopy equivalence]]:

$$
  \tau_{n}(A) \,\simeq\, A
  {\phantom{AAAAA}}
  \Rightarrow
  {\phantom{AAAAA}}
  Maps
  \big(
     &#643; S^{n+2}
     ,\,
     A
  \big)
  \underoverset
    {\in \mathrm{W}_{wh}}
    {ev_\ast}
    {\longrightarrow}
  A
  \,.
$$
\end{example}
\begin{proof}
  By assumption, the [[long exact sequence]] from Cor. \ref{LESOfHomotopyGroupswithMappingSpace} collapses to exact segments of the form
$$
  \ast
  \to
  \pi_{\bullet}
  \big(
     Maps(&#643; S^{n+2},\, A) 
  \big)
  \xrightarrow{ 
    \;\;\;
    \pi_\bullet(ev_\ast) 
    \;\;\;
  }
  \pi_\bullet(A)
  \to
  \ast
  \,.
$$
\end{proof}



### Cohomology

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

\linebreak

### Homology

See at _[[homology of iterated loop spaces]]_.

\linebreak

### Relation to configuration spaces of points

+-- {: .num_prop #ScanningMapEquivalenceOverCartesianSpace}
###### Proposition
**([[iterated loop spaces]] equivalent to [[configuration spaces of points]])**

For 

1. $d \in \mathbb{N}$, $d \geq 1$ a [[natural number]] with $\mathbb{R}^d$ denoting the [[Cartesian space]]/[[Euclidean space]] of that [[dimension]],

1. $Y$ a [[manifold]], with [[inhabited set|non-empty]] [[manifold with boundary|boundary]] so that  $Y / \partial Y$ is [[connected topological space|connected]],

the electric field map/[[scanning map]] constitutes a [[homotopy equivalence]]

$$
  Conf\left( 
    \mathbb{R}^d, Y
  \right)
  \overset{scan}{\longrightarrow}
  \Omega^d \Sigma^d (Y/\partial Y)
$$

between 

1. the configuration space of arbitrary points in $\mathbb{R}^d \times Y$ vanishing at the boundary (Def. \ref{ConfigurationSpacesOfnPoints}) 

1. the [[iterated loop space|d-fold loop space]] of the $d$-fold [[reduced suspension]] of the [[quotient space]] $Y / \partial Y$ (regarded as a [[pointed topological space]] with basepoint $[\partial Y]$).

In particular when $Y = \mathbb{D}^k$ is the [[closed ball]] of [[dimension]] $k \geq 1$ this gives a [[homotopy equivalence]]

$$
  Conf\left( 
    \mathbb{R}^d, \mathbb{D}^k
  \right)
  \overset{scan}{\longrightarrow}
  \Omega^d S^{ d + k }
$$

with the [[iterated loop space|d-fold loop space]] of the [[n-sphere|(d+k)-sphere]].

=--

([May 72, Theorem 2.7](#May72), [Segal 73, Theorem 3](#Segal73), see [Bödigheimer 87, Example 13](#Boedigheimer87))


+-- {: .num_prop #StableSplittingOfMappingSpacesOutOfEuclideanSpace}
###### Proposition
**([[stable splitting of mapping spaces]] out of [[Euclidean space]]/[[n-spheres]])**

For 

1. $d \in \mathbb{N}$, $d \geq 1$ a [[natural number]] with $\mathbb{R}^d$ denoting the [[Cartesian space]]/[[Euclidean space]] of that [[dimension]],

1. $Y$ a [[manifold]], with [[inhabited set|non-empty]] [[manifold with boundary|boundary]] so that  $Y / \partial Y$ is [[connected topological space|connected]],

there is a [[stable weak homotopy equivalence]]

$$
  \Sigma^\infty Conf(\mathbb{R}^d, Y)
  \overset{\simeq}{\longrightarrow}
  \underset{n \in \mathbb{N}}{\oplus} \Sigma^\infty Conf_n(\mathbb{R}^d, Y)
$$

between

1. the [[suspension spectrum]] of the [[configuration space of points|configuration space]] of an arbitrary number of points in $\mathbb{R}^d \times Y$ vanishing at the boundary and distinct already as points of $\mathbb{R}^d$ (Def. \ref{ConfigurationSpacesOfnPoints})

1. the [[direct sum]] (hence: [[wedge sum]]) of [[suspension spectra]] of the [[configuration space of points|configuration spaces]] of a fixed number of points in $\mathbb{R}^d \times Y$, vanishing at the boundary and distinct already as points in $\mathbb{R}^d$ (also Def. \ref{ConfigurationSpacesOfnPoints}).

Combined with the [[stabilization]] of the electric field map/[[scanning map]] [[homotopy equivalence]] from Prop. \ref{ScanningMapEquivalenceOverCartesianSpace} this yields a [[stable weak homotopy equivalence]]

$$
  Maps_{cp}(\mathbb{R}^d, \Sigma^d (Y / \partial Y))
  =
  Maps^{\ast/}( S^d, \Sigma^d (Y / \partial Y))
  =
  \Omega^d \Sigma^d (Y/\partial Y)
  \underoverset{\Sigma^\infty scan}{\simeq}{\longrightarrow}
  \Sigma^\infty Conf(\mathbb{R}^d, Y)
  \overset{\simeq}{\longrightarrow}
  \underset{n \in \mathbb{N}}{\oplus} \Sigma^\infty Conf_n(\mathbb{R}^d, Y)
$$

between the latter direct sum and the [[suspension spectrum]] of the [[mapping space]] of pointed [[continuous functions]] from the [[n-sphere|d-sphere]] to the $d$-fold [[reduced suspension]] of $Y / \partial Y$.


=--

([Snaith 74, theorem 1.1](#Snaith74), [Bödigheimer 87, Example 2](#Boedigheimer87))

In fact by [Bödigheimer 87, Example 5](#Boedigheimer87) this equivalence still holds with $Y$ treated on the same footing as $\mathbb{R}^d$, hence with $Conf_n(\mathbb{R}^d, Y)$ on the right replaced by $Conf_n(\mathbb{R}^d \times Y)$ in the well-adjusted notation of Def. \ref{ConfigurationSpacesOfnPoints}:

$$
  Maps_{cp}(\mathbb{R}^d, \Sigma^d (Y / \partial Y))
  =
  Maps^{\ast/}( S^d, \Sigma^d (Y / \partial Y))
  \overset{\simeq}{\longrightarrow}
  \underset{n \in \mathbb{N}}{\oplus} \Sigma^\infty Conf_n(\mathbb{R}^d \times Y)
$$



## Related concepts

[[!include k-monoidal table]]

## References

### General

* [[Peter May]], _Infinite loop space theory_, Bull. Amer. Math. Soc. Volume 83, Number 4 (1977), 456-494. ([euclid:bams/1183538891](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183538891))

  _Infinite loop space theory revisited_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/28.pdf))

* {#Adams} [[John Frank Adams]], _Infinite loop spaces_, Hermann Weyl lectures at IAS, Princeton University Press (1978) ([ISBN:9780691082066](https://press.princeton.edu/books/paperback/9780691082066/infinite-loop-spaces-am-90-volume-90), [doi:10.1515/9781400821259](https://doi.org/10.1515/9781400821259))
 

* [[Peter May]], _The uniqueness of infinite loop space machines_, Topology, vol 17, pp. 205-224 (1978) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/22.pdf))

* {#Lurie} [[Jacob Lurie]], Section 5.1.3 of _[[Higher Algebra]]_ 

On the [[Morava K-theory]] of iterated loop spaces of [[n-spheres]]:

* [[Douglas Ravenel]], *What we still don't know about loop spaces of spheres*, in: [[Mark Mahowald]], [[Stewart Priddy]] (eds.), *Homotopy Theory via Algebraic Geometry and Group Representations*, Contemporary Mathematics **220**, AMS 1998  ([pdf](https://people.math.rochester.edu/faculty/doug/mypapers/loop.pdf), [[Ravenel_LoopSpacesOfSpheres.pdf:file]], [doi:10.1090/conm/220](http://dx.doi.org/10.1090/conm/220))


### Relation to configuration spaces of points

In relation to [[configuration spaces of points]]:

* {#May72} [[Peter May]], _The geometry of iterated loop spaces_, Springer 1972 ([pdf](https://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf), [doi:10.1007/BFb0067491](https://link.springer.com/book/10.1007/BFb0067491))

* {#Segal73} [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))

* {#Snaith74} [[Victor Snaith]],  _A stable decomposition of $\Omega^n S^n X$_, Journal of the London Mathematical Society 7 (1974), 577 - 583 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/snaiths.pdf))

* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf), [[BoedigheimerStableSplittings87.pdf:file]])

### Rational cohomology

On [[ordinary cohomology]] of iterated loop spaces in relation to [[configuration spaces of points]] (see also at _[[graph complex]]_):

* [[Carl-Friedrich Bödigheimer]], [[Fred Cohen]], L. Taylor, _On the homology of configuration spaces_, Topology Vol. 28 No. 1, p. 111-123 1989 ([pdf](https://core.ac.uk/download/pdf/82124359.pdf))

On the [[rational cohomology]]:

* {#KallelSjerve99} [[Sadok Kallel]], [[Denis Sjerve]], _On Brace Products and the Structur eof Fibrations with Section_, 1999 ([pdf](https://www.math.ubc.ca/~sjer/brace.pdf), [[KallelSjerv99.pdf:file]])

[[!redirects iterated loop spaces]]

[[!redirects iterated based loop space]]
[[!redirects iterated based loop spaces]]

[[!redirects n-fold loop space]]
[[!redirects n-fold loop spaces]]



