
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


\linebreak

{#NotAnMCG} **Beware** that the spherical $n$-braid groups for $n \geq 3$ are *not* [[isomorphic|isomorphic]] to the [[mapping class groups]] of the $n$-[[punctured]] [[2-sphere]], see the examples [there](mapping+class+group#MappingClassGroupsOfNPuncturedSpheres). 

\begin{imagefromfile}
    "file_name": "KernelofSphericalBraidGroupToMCG.jpg",
    "float": "right",
    "width": 150,
    "unit": "px",
    "margin": {
        "top": -55,
        "bottom": 20,
        "right": 0, 
        "left": 25
    },
    "caption": "([Farb-Margalit '12 Fig. 9.6](#FarbMargalit12))"
\end{imagefromfile}

The generalized Birman sequence ([here](braid+group#GenBirmanSequenceForTrivialPi)), which would superficially imply such isomorphism, does not apply to punctured spheres, since its assumption is violated:
The map $C_2 \simeq \pi_1 Diff^{+}(S^2) \longrightarrow Br_n(S^2)$ is not trivial, whence the actual mapping class group is the [[quotient group]] of this [[normal subgroup]]-inclusion (cf. [Farb & Margalit 2012 (9.1)](#FarbMargalit12)), whose generator is the cyclic braid illustrated on the right.






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

* {#FarbMargalit12} [[Benson Farb]], [[Dan Margalit]], around (9.1 in): *A primer on mapping class groups*, Princeton Mathematical Series, Princeton University Press (2012) &lbrack;[ISBN:9780691147949](https://press.princeton.edu/books/hardcover/9780691147949/a-primer-on-mapping-class-groups), [jstor:j.ctt7rkjw](https://www.jstor.org/stable/j.ctt7rkjw), [pdf](http://euclid.nmu.edu/~joshthom/Teaching/MA589/farbmarg.pdf)&rbrack;


* {#Tan24} Cindy Tan: *Smallest nonabelian quotients of surface braid groups*, Algebr. Geom. Topol. **24** (2024) 3997-4006 &lbrack;[arXiv:2301.01872](https://arxiv.org/abs/2301.01872), [doi:10.2140/agt.2024.24.3997](https://doi.org/10.2140/agt.2024.24.3997)&rbrack;


On the [[representation theory]] of the spherical braid group:

* V. G. Bardakov: *Linear Representations of the Braid Groups of Some Manifolds*, Acta Appl Math **85** (2005) 41–48 &lbrack;[doi:10.1007/s10440-004-5584-6](https://doi.org/10.1007/s10440-004-5584-6)&rbrack;

On [[subgroups]] of spherical braid groups:

* {#GoncalvesGuaschi11} [[Daciberg Lima Gonçalves]], [[John Guaschi]]: *The classification of the virtually cyclic subgroups of the sphere braid groups*, Briefs in Mathematics, Springer (2013) &lbrack;[arXiv:1110.6628](https://arxiv.org/abs/1110.6628), [doi:10.1007/978-3-319-00257-6](https://doi.org/10.1007/978-3-319-00257-6),  [pdf](https://link.springer.com/content/pdf/bbm%3A978-3-319-00257-6%2F1.pdf)&rbrack;


[[!redirects spherical braid groups]]

[[!redirects sphere braid group]]
[[!redirects sphere braid groups]]

