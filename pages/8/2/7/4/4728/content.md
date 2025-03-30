
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

A **surface** is a [[space]] of [[dimension]] 2, usually understood to be [[connected topological space|connected]].

In [[differential topology|differential]] [[topology]]/[[differential geometry]] this means a 2-[[dimension of a manifold|dimensional]] ([[differentiable manifold|differentiable]]/[[smooth manifold|smooth]]) [[manifold]].

In [[complex analytic geometry]] this usually means a [[complex manifold]] of _complex_ dimension 2 (hence real dimension 4).

Similarly and more generally, in [[algebraic geometry]] an _[[algebraic surface]]_ is a [[variety]] of algebraic dimension 2. 

## Properties

### Classification
 {#Classification}

The [[orientation|oriented]] 
[[closed manifold|closed]] [[real manifold|real]] surfaces are classified, up to [[isomorphism]], by a [[natural number]] $g \in \mathbb{N}$ called the *[[genus of a surface|genus]]* (intuitively its "number of holes", in a sense):

| [[genus of a surface|genus]] | [[orientation|oriented]] [[surface]] | 
|------------------------------|-------------|
| $0$ | [[2-sphere]] $S^2$ |
| $1$ | [[2-torus]] $\mathbb{T}^2$ |
| $2$ | [[double torus]] $\Sigma^2_2$ |

(cf. [Kinsey 1991 Thm. 4.14](#Kinsey91), [Gallier & Xu 2013 Thm 6.3](#GallierXu13), [Thm. 4.14](#BBR21))

\begin{imagefromfile}
    "file_name": "Hatcher-ClosedSurfaceDecomposition.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 30
    },
    "caption": "From [Hatcher 2002 p 5](#Hatcher02)"
\end{imagefromfile}


{#FundamentalPolygons} Here the closed oriented surface $\Sigma^2_g$ of genus $g$ may be obtained from the [[regular polygon|regular $4g$-gon]] by identifying 

* all the [[boundary]] [[vertices]] with a single point, 

and, going clockwise for $k \in \{0, \cdots, g-1\}$,

* the $4k+1$st boundary [[edge]] with the reverse of the $4k +3$rd, 

* the $4k+2$nd edge with the reverse of the $4k+4$th.

<center>
<img src="/nlab/files/FundamPolygonsForOrntdClosedSurfaces.jpg" width="420">
</center>






Similarly, the [[orientation|non-orientable]] [[closed manifold|closed]] [[real manifold|real]] [[surfaces]] are classified by a [[positive number|positive]] [[natural number]] $h \in \mathbb{N}_{\geq 1}$, also called the (non-orientable) *genus* or the *number of crosscaps*

| [[genus of a surface|# crosscaps]] | [[orientation|non-orientable]] [[surface]] | 
|------------------------------|-------------|
| $1$ | [[real projective plane|projective plane]] $\mathbb{R}P^2$ |
| $2$ | [[Klein bottle]] $\mathbb{R}P^2 # \mathbb{R}P^2$ |

{#FundamentalPolygons} Here the non-orientable surface $\Sigma^2_{\overline{g}}$ with $h$ crosscaps may be obtained from the [[regular polygon|regular $2h$-gon]] by identifying 

* all the [[boundary]] [[vertices]] with a single point, 

and, going clockwise for $k \in \{0, \cdots, h-1\}$,

* the $2k+1$st boundary edge with the $2k + 2$nd.


<center>
<img src="/nlab/files/FundamenPolygonsForNonOrntdClosedSurfaces.jpg" width="310">
</center>


> (This is a conveniently concise but not the most intuitively visualized choice of fundamental polygons -- other choices are possible and often discussed, cf. also [MO:q/172784](https://mathoverflow.net/q/172784/381).)


### Homotopy
 {#Homotopy}

The [above](#Classification) classification may be restated in [[algebraic topology|algebro-topological terms]] by saying that (the [[homotopy type]] of) the oriented closed genus$=g$ surface has a 2-[[dimension of a CW-complex|dimensional]] [[CW-complex]]-[[structure]] exhibited by the following [[pointed topological space|pointed]] [[cell attachment]]:

\begin{tikzcd}
  S^1
  \ar[
    r,
    "{
      \prod_i [a_i, b_i]
    }"
  ]
  \ar[
    d
  ]
  \ar[
    dr,
    phantom,
    "{ \mathcolor{gray}{\mathrm{(po)}} }"{scale=.8, pos=.8}
  ]
  &
  \bigvee_{1 \leq i \leq g}
  S^1_a \vee S^1_b
  \ar[
    d
  ]
  \\
  D^2
  \ar[r]
  &
  \Sigma^2_g
  \mathrlap{\,.}
\end{tikzcd}

Here $\bigvee_{2g} S^1$ is the [[wedge sum]] of $2g$ [[circles]], whose [[fundamental group]] is the [[free group]] on $2g$ generators $(a_i, b_i)_{i=1}^g$, and the [[attaching map]] is a representative in this free group of the composition of [[group commutators]]

$$
  [a_i, b_i]
  \;\coloneqq\;
  a_i \cdot b_i \cdot a_i^{-1} \cdot b_i^{-1}
  \,,
$$

as indicated.

Similarly for (the [[homotopy type]] of) the non-orientable surface $\Sigma^2_{\overline{h}}$ of crosscap number $h$:

\begin{tikzcd}
  S^1
  \ar[
    r,
    "{
      \prod_i a_i^2
    }"
  ]
  \ar[
    d
  ]
  \ar[
    dr,
    phantom,
    "{ \mathcolor{gray}{\mathrm{(po)}} }"{scale=.8, pos=.8}
  ]
  &
  \bigvee_{1 \leq i \leq h}
    S^1
  \ar[
    d
  ]
  \\
  D^2
  \ar[r]
  &
  \Sigma^2_{\overline{h}}
  \mathrlap{\,.}
\end{tikzcd}



It follows that:

\begin{proposition}
The [[fundamental group]] of the [[orientation|oriented]] [[closed manifold|closed]]  [[real manifold|real]] surface $\Sigma^2_g$ of [[genus of a surface|genus]] $g \in \mathbb{N}$ (see [above](#Classification)) is the [[quotient group]] of the [[free group]] on $2g$ generators $(a_1, \cdots, a_g, \, b_1, \cdots, b_g)$ by the [[normal subgroup]] generated by the group product of the [[group commutators]] $[a_i, b_i]$ of the sequence of [[pairs]] of generators:

$$
  \pi_1\big(
    \Sigma^2_g
  \big)
  \;\simeq\;
  \big\langle
    a_1, \cdots, a_g
    ,\,
    b_1, \cdots, b_g
  \big\rangle
  \big/
  \Big(
    \textstyle{\prod_i}
    [a_i, b_i]
  \Big)
  \,.
$$

Similarly, the [[fundamental group]] of the [[orientation|non-orientable]] [[closed manifold|closed]]  [[real manifold|real]] surface $\Sigma^2_{\overline{h}}$ with $h \in \mathbb{N}_{\geq 1}$ [[genus of a surface|crosscaps]]  is the [[quotient group]] of the [[free group]] on $h$ generators $(a_1, \cdots, a_h)$ by the [[normal subgroup]] generated by the group product of the squares $a^2_ \,\coloneqq\, a_i \cdot a_i$ of the sequence of [[pairs]] of generators:


$$
  \pi_1\big(
    \Sigma^2_{\overline{h}}
  \big)
  \;\simeq\;
  \big\langle
    a_1, \cdots, a_h
  \big\rangle
  \big/
  \Big(
    \textstyle{\prod_i}
    a_i^2
  \Big)
  \,.
$$

\end{proposition}

(cf. [Gallier & Xu 2013 p 100](#GallierXu13), [Actipes 2013 Thm. 6.3](#Actipes13)).



### CoHomology
 {#CoHomology}

\begin{proposition}\label{OrdinaryHomologyOfClosedOriented}
  The [[ordinary homology]] with [[integer]] [[coefficients]] of a [[closed manifold|closed]] [[orientation|oriented]] surface $\Sigma_g$ of [[genus of a surface|genus]] $G$ is the [[free abelian group]] on $2g$ generators:
$$
  H_1\big(
    \Sigma_g
    ;\,
    \mathbb{Z}
  \big)
  \;\simeq\;
  \mathbb{Z}^{2g}
  \,.
$$
\end{proposition}
(e.g. [Giblin 1977 Thm 6.13](#Giblin77))

By the [[universal coefficient theorem]] the analogous result holds for the [[integral cohomology]]
$$
  H^1\big(
    \Sigma_g
    ;\,
    \mathbb{Z}
  \big)
  \;\simeq\;
  \mathbb{Z}^{2g}
  \,.
$$

It follows for instance that:

\begin{proposition}\label{SpinStructuresOnClosedSurfaces}
On a [[closed manifold|closed]] [[orientation|oriented]] [[surface]] of [[genus of a surface|genus]] $g \in \mathbb{N}$ there exist precisely $2^{2g}$ distinct spin structures.
\end{proposition}
(cf. [Lawson & Michelson 1989 Ex. 2.6](spin+structure#LawsonMichelson1989))
\begin{proof}
Since spin structures are classified by $H_1(-;C_2)$ (see [there](spin+structure#ClassificationOfSpinStructures))
this follows by Prop. \ref{OrdinaryHomologyOfClosedOriented} and the [[universal coefficient theorem]].
\end{proof}


## Examples

* [[plane]]

* [[disk]], [[annulus]]

* [[sphere]]

* [[torus]]

* [[Klein bottle]]


## Related concepts

* [[punctured]] surface

* [[differential geometry of curves and surfaces]]

* analog for dimension 1: [[curve]], [[algebraic curve]]

* [[genus of a surface]]

* [[area]]

* [[moduli space of curves]]

* [[complex surface]]

* [[surface knot]]

* [[hypersurface]]

* [[minimal surface]]

[[!include low dimensional manifolds -- table]]



## References

Monographs:

* {#Kinsey91} [[L. Christine Kinsey]]: *Topology of Surfaces*, Spinger (1991) &lbrack;[doi:10.1007/978-1-4612-0899-0](https://doi.org/10.1007/978-1-4612-0899-0), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kinsey.pdf)&rbrack;

* [[Richard E. Schwartz]]: *Mostly Surfaces*, American Mathematical Society, Student Mathematical Library **60** (2011) &lbrack;draft: [pdf](http://www.math.brown.edu/reschwar/Papers/surfacebook.pdf), endmatter:[pdf](https://www.ams.org/books/stml/060/stml060-endmatter.pdf)&rbrack;

* {#GallierXu13} [[Jean Gallier]], [[Dianna Xu]]: *A Guide to the Classification Theorem for Compact Surfaces*, Springer (2013) &lbrack;[doi:10.1007/978-3-642-34364-3](https://doi.org/10.1007/978-3-642-34364-3), [Wikipedia entry](https://en.wikipedia.org/wiki/A_Guide_to_the_Classification_Theorem_for_Compact_Surfaces)&rbrack;

* {#BBR21} Clark Bray, Adrian Butcher, Simon Rubinstein-Salzedo, chapters 2 & 4 of: *Algebraic Topology*, Springer (2021) \[<a href="https://doi.org/10.1007/978-3-030-70608-1">doi:10.1007/978-3-030-70608-1</a>, [pdf](https://link.springer.com/content/pdf/10.1007/978-3-030-70608-1.pdf)\]

In the broader context of [[algebraic topology]]:

* {#Giblin77} P. J. Giblin: *Graphs, Surfaces and Homology -- An Introduction to Algebraic Topology*, Chapman and Hall (1977) &lbrack;[doi:10.1007/978-94-009-5953-8](https://doi.org/10.1007/978-94-009-5953-8)&rbrack;

* {#Hatcher02} [[Allen Hatcher]]: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;


See also:

* Wikipedia: *<a href="https://en.wikipedia.org/wiki/Surface_(topology)">Surface (topology)</a>*

* Wikipedia: *[Genus g surface](https://en.wikipedia.org/wiki/Genus_g_surface)*

* [[Manifold Atlas]], _[2-manifolds](www.map.mpim-bonn.mpg.de/2-manifolds)_

* [[Peter Andrews]]: *The Classification of Surfaces*, The American Mathematical Monthly **95** 9 (1988) 861-867 &lbrack;[doi:10.2307/2322906](https://doi.org/10.2307/2322906), [jstor:2322906](https://www.jstor.org/stable/2322906)&rbrack;


Review and exposition of the classification of surfaces by fundamental [[polygons]]:

* [Giblin 1977](#Giblin77), chapter 2

* E. C. Zeeman: *An Introduction to Topology -- The Classification theorem for Surfaces* &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/surgery/zeeman.pdf), [pdf](https://www.maths.ed.ac.uk/~v1ranick/surgery/ecztop.pdf), [[Zeeman-ClassificationOfSurfaces.pdf:file]]&rbrack;

* Chen Hui George Teo: *Classification of Surfaces*, REU notes (2011) &lbrack;[pdf](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Teo.pdf), [[CHGT-ClassificationOfSurfaces.pdf:file]]&rbrack;

* Thomas George: *The Classification of Surfaces with Boundary*, REU notes (2001) &lbrack;[pdf](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/George.pdf), [[George-SurfacesWithBoundary.pdf:file]]&rbrack;

* Eugene Gorsky: *Classification of Surfaces*, lecture notes (2021) &lbrack;[pdf](https://www.math.ucdavis.edu/~egorskiy/MAT215C-s21/Sosinsky.pdf)&rbrack;

* Ana da Silva Rodrigues: *Classification of Surfaces*, BSc thesis, ETH (2023) &lbrack;[pdf](https://people.math.ethz.ch/~acannas/Student_Papers/BSc_Theses/2023_bsc_da_silva_classification_of_surfaces.pdf), [[Rodrigues-ClassificationOfSurfaces.pdf:file]]&rbrack;

See also:

* Wikipedia: *[Fundamental polygon](https://en.wikipedia.org/wiki/Fundamental_polygon)*

Review of the computation of the [[fundamental group]] of surfaces:

* {#Actipes13} Matthew Actipes: *On the fundamental group of surfaces*, REU notes (2013) &lbrack;[pdf](http://math.uchicago.edu/~may/REU2013/REUPapers/Actipes.pdf), [[Actipes-FundamentalGroupOfSurfaces.pdf:file]]&rbrack;

Discussion of [[de Rham cohomology]] of surfaces:

* [[William Fulton]], §18 of: *Algebraic Topology -- A First Course*, Graduate Texts in Mathematics **153**, Springer (1995) \[<a href="https://doi.org/10.1007/978-1-4612-4180-5">doi:10.1007/978-1-4612-4180-5</a>\] 



[[!redirects surface]]
[[!redirects surfaces]]

[[!redirects 2-manifold]]
[[!redirects 2-manifolds]]