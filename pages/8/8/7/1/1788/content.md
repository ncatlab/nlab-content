
* J. Tolar: *On Clifford groups in quantum computing* &lbrack;[arXiv:1810.10259](https://arxiv.org/abs/1810.10259)&rbrack;



## Definition

By the *spherical braid group* $Br_n(S^2)$, for $n \in \mathbb{N}$, one means the [[surface braid group]] 

$$
  Br_n(S^2)
  \;\simeq\;
  \pi_1
  Conf_n(S^2)
  \,,
$$

where the [[surface]] in question is the [[2-sphere]] $S^2$. Hence the surface braid group is the [[fundamental group]] $\pi_1(-)$ of the [[configuration spaces of points|configuration space of $n$-points]], $Conf_n(-)$, on the [[2-sphere]].



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
        "left": 10
    },
    "caption": "(from [math.SE:q/136821](https://math.stackexchange.com/q/136821/58526))"
\end{imagefromfile}



\begin{proposition}
The spherical braid group is the [[quotient group]] of the ordinary [[braid group]] by one further relation:
$$
  Br_n(S^2) 
  \;\simeq\;
  Br_n/
  \big( (b_1 b_2 \cdots b_{n-1})(b_{n-1} \cdots b_2 b_1)
  \,,
$$
where the $b_i$ denote the [Artin braid generators](braid+group#ArtinPresentation). 

Moreover, the canonical map from the plain braid group to the [[symmetric group]] factors through this quotient map to the spherical braid group

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


## References

* {#FadellVanBuskirk61} [[Edward Fadell]], James Van Buskirk: *On the braid groups of $E^2$ and $S^2$*,  Bull. Amer. Math. Soc. **67** 2 (1961) 211-213 &lbrack;[euclid:bams/1183524083](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society/volume-67/issue-2/On-the-braid-groups-of-E2-and-S2/bams/1183524083.full)&rbrack;

* {#Tan24} Cindy Tan: *Smallest nonabelian quotients of surface braid groups*, Algebr. Geom. Topol. **24** (2024) 3997-4006 &lbrack;[arXiv:2301.01872](https://arxiv.org/abs/2301.01872), [doi:10.2140/agt.2024.24.3997](https://doi.org/10.2140/agt.2024.24.3997)&rbrack;





$$  
  \pi_2 S^2
  \to
  \pi_1
  \Maps^\ast(S^2, S^2)
  \to 
  \pi_1
  Maps(S^2, S^2)  
  \to
  \pi_1 S^2
  \to
  \pi_0
  \Maps^\ast(S^2, S^2)
  \to 
  \pi_0
  Maps(S^2, S^2)
  \to
  \pi_0 S^2
$$


\begin{example}
  The [[unitarization]] of the [standard representation](representation+theory+of+the+symmetric+group#StandardRepresentation) of the [[symmetric group]] $Sym_3$ has the two generating [[transpositions]] represented by (what in [[quantum information theory]] is called)

1. the [[Pauli Z-gate]] $Z$ 

1. its composition $- Z \circ R_y(3\pi/2)$ with [[rotation gates]]. 

\end{example}
\begin{proof}
For definiteness of computation, when [[group averaging]] we will be cycling through the elements of $Sym_3$ in this order:
$$
  Sym_3 
  \;=\;
  \left\{
    \begin{array}{l}
    (1 2 3)
    ,\,\\
    (1 3 2)
    ,\,\\
    (2 1 3)
    ,\,\\
    (2 3 1)
    ,\,\\
    (3 1 2)
    ,\,\\
    (3 2 1)
    \end{array}
  \right\}
  \,.
$$

Let $\big\{e_1, e_2, e_3\big\}$ denote the canonical [[linear basis]] of the *defining* representation, with [[group action]] given by
$$
  \sigma \cdot e_i \;\coloneqq\; e_{\sigma(i)}
  \,.
$$

Then a linear basis for the *[standard representation](representation+theory+of+the+symmetric+group#StandardRepresentation)* inside the defining representation is: 

$$
  \begin{array}{ccc}
  \left[\begin{array}{c}1 \\ 0\end{array}\right] 
    \;\coloneqq\; 
  e_1 - e_3
  \\
  \left[\begin{array}{c}0 \\ 1\end{array}\right] 
  \;\coloneqq\; 
  e_2 - e_3
  \mathrlap{\,.}
  \end{array}
$$

The [[group averaging|group-averaged]] inner product of these basis elements is found to be:
$$
  \left\langle
    \left[
      \begin{array}{c}
        1 \\ 0
      \end{array}
    \right]
    ,\,
    \left[
      \begin{array}{c}
        0 \\ 1
      \end{array}
    \right]
  \right\rangle
  \;=\;
  \left(
  \;\;
  \begin{array}{l}
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      1 
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      1
    \end{array}
  \right]
  \end{array}
  \right)/6
  \;=\;
  4/6
  \;=\;
  2/3
$$
$$
  \left\langle
    \left[
      \begin{array}{c}
        0 \\ 1
      \end{array}
    \right]
    ,\,
    \left[
      \begin{array}{c}
        0 \\ 1
      \end{array}
    \right]
  \right\rangle
  \;=\;
  \left(
  \;\;
  \begin{array}{l}
  \left[
    \begin{array}{c}
      0 
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0 
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      1
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      1
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      1
    \end{array}
  \right]
  \end{array}
  \right)/6
  \;=\;
  8/6
  \;=\;
  4/3
$$
$$
  \left\langle
    \left[
      \begin{array}{c}
        1 \\ 0
      \end{array}
    \right]
    ,\,
    \left[
      \begin{array}{c}
        1 \\ 0
      \end{array}
    \right]
  \right\rangle
  \;=\;
  \left(
  \;\;
  \begin{array}{l}
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      1 
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1 
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      0
    \end{array}
  \right]
  \end{array}
  \right)/6
  \;=\;
  8/6
  \;=\;
  4/3
$$

From this an [[orthonormal basis]] for the averaged inner product is
$$
  \begin{array}{l}
  {\vert 0 \rangle}
  \;\coloneqq\;
  \tfrac{1}{2}
  \left[
  \begin{array}{c}
    1
    \\
    1
  \end{array}
  \right]
  \;=\;
  \tfrac{1}{2}(e_1 + e_2) - e_3
  \\
  {\vert 1 \rangle}
  \;\coloneqq\;
  \tfrac{\sqrt{3}}{2}
  \left[
  \begin{array}{c}
    1
    \\
    -1
  \end{array}
  \right]
  \;=\;
  \tfrac{\sqrt{3}}{2}(e_1 - e_2)
  \,.
  \end{array}
$$



On this bases the action of $(213)$ is

$$
  \rho(213)\big({\vert 0 \rangle}\big)
  \;=\;
  {\vert 0 \rangle}
$$
$$
  \rho(213)\big({\vert 1 \rangle}\big)
  \;=\;
  -{\vert 1 \rangle}
$$

and hence $(213)$ acts as the [[Pauli Z-gate]]:

$$
  \rho(213)
    \;=\;
  \left(
  \begin{array}{cc}
    1 & 0 
    \\
    0 & -1
  \end{array}
  \right)
  \;=\;
  Z
$$


On the other hand, the action of $(132)$ is found to be
$$
  \rho(132)\big({\vert 0 \rangle}\big)
  \;=\;
  \rho(132)
  \left(
  \tfrac{1}{2}
  \left[
  \begin{array}{c}
    1
    \\
    1
  \end{array}
  \right]
  \right)
  \;=\;
  \tfrac{1}{2}
  \left[
  \begin{array}{c}
    1
    \\
    -2
  \end{array}
  \right]  
  \;=\;
  -\tfrac{1}{2} {\vert 0 \rangle}
  + \tfrac{\sqrt{3}}{2} {\vert 1 \rangle}
$$
$$
  \rho(132)\big({\vert 1 \rangle}\big)
  \;=\;
  \rho(132)
  \left(
  \tfrac{\sqrt{3}}{2}
  \left[
  \begin{array}{c}
    1
    \\
    -1
  \end{array}
  \right]
  \right)
  \;=\;
  \tfrac{\sqrt{3}}{2}
  \left[
  \begin{array}{c}
    1
    \\
    0
  \end{array}
  \right]  
  \;=\;
  \tfrac{\sqrt{3}}{2} {\vert 0 \rangle}
  +
  \tfrac{1}{2} {\vert 1 \rangle}
$$
and hence
$$
  \rho(132)
  \;=\;
  \left(
  \begin{array}{c}
    -1/2 & \sqrt{3}/2
    \\
    \sqrt{3}/2 & 1/2
  \end{array}
  \right)
  \;=\;
  \left(
  \begin{array}{c}
    -1 & 0
    \\
    0 & 1
  \end{array}
  \right)
  \left(
  \begin{array}{c}
    1/2 & -\sqrt{3}/2
    \\
    \sqrt{3}/2 & 1/2
  \end{array}
  \right)
  \;=\;
  \left(
  \begin{array}{c}
    -1 & 0
    \\
    0 & 1
  \end{array}
  \right)
  \left(
  \begin{array}{c}
    cos(\pi/3) & -sin(\pi/3)
    \\
    sin(\pi/3) & cos(\pi/3)
  \end{array}
  \right)
  \;=\;
  - 
  Z \circ R_y(2\pi/3)
$$
\end{proof}


\linebreak

end

\lnebreak


The action of $(231)$

$$
  (231) {\vert 0 \rangle}
  \;=\;
  \tfrac{1}{2}
  \left[
  \begin{array}{c}
    -2 \\ 1
  \end{array}
  \right]
  \;=\;
  -\tfrac{1}{2} {\vert 0 \rangle}
  -\tfrac{\sqrt{3}}{2} {\vert 1 \rangle}
$$

$$
  (231) {\vert 1 \rangle}
  \;=\;
  \tfrac{\sqrt{3}}{2}
  \left[
  \begin{array}{c}
    0 \\ 1
  \end{array}
  \right]
  \;=\;
  \tfrac{\sqrt{3}}{2} {\vert 0 \rangle}
  - \tfrac{1}{2} {\vert 1 \rangle}
$$

Hence 

$$
  (231) 
  \;=\;
  \left[
  \begin{array}{cc}
    -1/2 & \sqrt{3}/2
    \\
    -\sqrt{3}/2 & - 1/2
  \end{array}
  \right]
$$


The action of $(321)$

$$
  (321) {\vert 0 \rangle}
  \;=\;
  (321) 
  \tfrac{1}{2}
  \left[
    \begin{array}{c}
      1 \\ 1
    \end{array}
  \right]
  \;=\;
  \tfrac{1}{2}
  \left[
    \begin{array}{c}
      -2 \\ 1
    \end{array}
  \right]
  \;=\;
  -\tfrac{1}{2} {\vert 0 \rangle}
  - \tfrac{\sqrt{3}}{2} {\vert 1 \rangle}
$$

$$
  (321) {\vert 1 \rangle}
  \;=\;
  (321) 
  \tfrac{\sqrt{3}}{2}
  \left[
    \begin{array}{c}
      1 \\ -1
    \end{array}
  \right]
  \;=\;
  \tfrac{\sqrt{3}}{2}
  \left[
    \begin{array}{c}
      0 \\ -1
    \end{array}
  \right]
  \;=\;  
  \tfrac{\sqrt{3}}{2} {\vert 0 \rangle}
  - \tfrac{1}{2} {\vert 1 \rangle}
$$

Hence $(321)$ acts as

$$
  (321) 
  \;=\;
  \left[
  \begin{array}{c}
    -1/2 & \sqrt{3}/2
    \\
    -\sqrt{3}/2 & -1/2
  \end{array}
  \right]
  \;=\;
  -
  \left[
  \begin{array}{c}
    1/2 & -\sqrt{3}/2
    \\
    \sqrt{3}/2 & 1/2
  \end{array}
  \right]
  \;=\;
  - R_y(2\pi/3)
$$

\linebreak

\linebreak







## Defect anyons

* [[Maissam Barkeshli]], Chao-Ming Jian, [[Xiao-Liang Qi]]: *Twist defects and projective non-Abelian braiding statistics*, Phys. Rev. B **87** (2013) 045130 &lbrack;[doi:10.1103/PhysRevB.87.045130](https://doi.org/10.1103/PhysRevB.87.045130), [arXiv:1208.4834](https://arxiv.org/abs/1208.4834)&rbrack;





## Controlling anyons

* G. Rosenberg, B. Seradjeh, C. Weeks, M. Franz: *Creation and manipulation of anyons in a layered superconductor-2DEG system*, Phys. Rev. B **79** 205102 (2009) \[<a href="https://doi.org/10.1103/PhysRevB.79.205102">doi:10.1103/PhysRevB.79.205102</a>, [arXiv:0812.3140](https://arxiv.org/abs/0812.3140)\]

* Gábor B. Halász: *Gate-Controlled Anyon Generation and Detection in Kitaev Spin Liquids*, Phys. Rev. Lett. **132** 206501 (2024) \[<a href="https://doi.org/10.1103/PhysRevLett.132.206501">doi:10.1103/PhysRevLett.132.206501</a>\]



## Loop space of the 2-sphere

On the [[loop space]] $\Omega S^2$ of the 2-sphere

in relation to [[braid groups]]

* [[Frederick R. Cohen]], J. Wu: *On Braid Groups, Free Groups, and the Loop Space of the 2-Sphere*, in: *Categorical Decomposition Techniques in Algebraic Topology*, in *Progress in Mathematics* **215**,  Birkhäuser (2003) 93-105  \[<a href="https://doi.org/10.1007/978-3-0348-7863-0_6">doi:10.1007/978-3-0348-7863-0_6</a>\]

On $\Omega S^2 \,\simeq\, B \Omega^2 S^2$ regarded as a [[classifying space]] (for "$\mathbf{l}$ine" bundles):

* [[Jack Morava]]: *A homotopy-theoretic context for CKM/Birkhoff renormalization* &lbrack;[arXiv:2307.10148](https://arxiv.org/abs/2307.10148), [spire:2678618](https://inspirehep.net/literature/2678618)&rbrack;

* [[Jack Morava]]: *Some very low-dimensional algebraic topology* &lbrack;[arXiv:2411.15885](https://arxiv.org/abs/2411.15885)&rbrack;





[[test page]]
