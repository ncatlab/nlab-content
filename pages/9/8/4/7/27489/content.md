
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--


\tableofcontents


## Definition

By the *spherical braid group* $Br_n(S^2)$, for $n \in \mathbb{N}$, one means the *sphere braid group*, hence the [[surface braid group]], where the [[surface]] in question is the [[2-sphere]] $S^2$. More concretely, the spherical braid group 

$$
  Br_n(S^2)
  \;\simeq\;
  \pi_1
  Conf_n(S^2)
  \,,
$$

\begin{imagefromfile}
    "file_name": "BraidOn2Sphere.png",
    "float": "right",
    "width": 150,
    "unit": "px",
    "margin": {
        "top": -60,
        "bottom": 20,
        "right": 0, 
        "left": 25
    }
\end{imagefromfile}

is the [[fundamental group]] $\pi_1(-)$ of the [[configuration spaces of points|configuration space of $n$-points]], $Conf_n(-)$, on the [[2-sphere]].


Illustrated on the right is the element $b_2 b_1 \in Br_3(S^2)$ (where $b_i$ denote the [Artin braid generators](braid+group#ArtinPresentation), cf. Prop. \ref{AsQuotientOfPlainBraidGroup}.)






## Properties

\begin{imagefromfile}
    "file_name": "RelationInSphericalBraidGroup.png",
    "float": "right",
    "width": 100,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 25
    },
    "caption": "(from [math.SE:q/136821](https://math.stackexchange.com/q/136821/58526))"
\end{imagefromfile}



\begin{proposition}\label{AsQuotientOfPlainBraidGroup}
The spherical braid group is the [[quotient group]] of the ordinary [[braid group]] by one further relation:
\[
  \label{ArtinPresentation}
  Br_n(S^2) 
  \;\simeq\;
  Br_n/
  \big( 
    (b_1 b_2 \cdots b_{n-1})(b_{n-1} \cdots b_2 b_1)
  \big)
  \,,
\]
where the $b_i$ denote the [Artin braid generators](braid+group#ArtinPresentation). 

Moreover, the canonical map from the plain braid group to the [[symmetric group]] $Sym_n$ factors through the corresponding quotient [[coprojection]]:

\begin{tikzcd}[
  column sep=10pt
]
  \mathrm{Br}_n
  \ar[
    rr,
    ->>
  ]
  \ar[dr, ->>]
  &&
  \mathrm{Br}_n(S^2)
  \ar[dl,->>]
  \\
  &
  \mathrm{Sym}_n
\end{tikzcd}

\end{proposition}
([Fadell & Van Buskirk 1961 p 245, 255](#FadellVanBuskirk61), cf. [Tan 2024 §3.1](#Tan24))

\begin{proposition}\label{GroupOrder}
  The [[order of a group|order]] $\vert Br_n(S^2) \vert$ of the spherical braid group is:

1. $2$ for $n = 2$ (cf. Ex. \ref{SphericalBraidsOnTwoStrands}),

1. $12$ for $n =3$,

1. $\infty$ for $n \geq 4$.

\end{proposition}
([Fadell & VanBuskirk 1961 p 255](#FadellVanBuskirk61))

## Examples

\begin{example}\label{SphericalBraidsOnTwoStrands}
  For $n = 2$ strands the ordinary [[braid group]] is [[free group|free]] on the single Artin generator $b_1$, 
$$
  Br_2 \;\simeq\; \langle b_1 \rangle \,\simeq\, \mathbb{Z}
  \,,
$$  
but the spherical braid group on $n = 2$ strands is [[cyclic group of order two|cyclic of order 2]], due to the relation (eq:ArtinPresentation):
$$
  Br_2(S^2) 
    \;\simeq\; 
  \langle b_1\rangle/\big(b_1^2\big) \,\simeq\, 
  \mathbb{Z}/2 \,\eqqcolon\, C_2
  \,.
$$

Geometrically, the element $n \in \mathbb{Z}$ of the ordinary braid group $Br_2$ is the braid on two strands which makes $n$ *half* rotations in itself. But on the sphere, one full rotation (two half rotations) of one point around another may be contracted to a loop constant on the [[antipode|antipodal point]].
\end{example}
(cf. [Fadell & VanBuskirk 1961 p 254](#FadellVanBuskirk61) and Prop. \ref{GroupOrder})




## References

* {#FadellVanBuskirk61} [[Edward Fadell]], James Van Buskirk: *On the braid groups of $E^2$ and $S^2$*,  Bull. Amer. Math. Soc. **67** 2 (1961) 211-213 &lbrack;[euclid:bams/1183524083](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society/volume-67/issue-2/On-the-braid-groups-of-E2-and-S2/bams/1183524083.full)&rbrack;

* {#Tan24} Cindy Tan: *Smallest nonabelian quotients of surface braid groups*, Algebr. Geom. Topol. **24** (2024) 3997-4006 &lbrack;[arXiv:2301.01872](https://arxiv.org/abs/2301.01872), [doi:10.2140/agt.2024.24.3997](https://doi.org/10.2140/agt.2024.24.3997)&rbrack;

[[!redirects spherical braid groups]]

[[!redirects sphere braid group]]
[[!redirects sphere braid groups]]

