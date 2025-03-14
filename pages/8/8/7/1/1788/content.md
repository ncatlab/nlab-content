

On the $k$-dimensional complex vector space $Span_{\mathbb{C}}\Big( {\vert 0 \rangle}, \, {\vert 1 \rangle}, \cdots, {\vert k-1 \rangle} \Big)$ consider the linear operators

$$
  \begin{array}{ccl}
  S
    {\big\vert n \big\rangle}
  &=&
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{ \widehat n }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, n
     }{
       k
     }
  }
  {\big\vert \widehat{n} \big\rangle}
  \\
  T
  {\big\vert n \big\rangle}
  &=&
  e^{ 
    \pi \mathrm{i}
    \tfrac{ n^2 }{ k }
  }
  {\big\vert
    n 
  \big\rangle}
  \end{array}
$$

The claim ([Gocho 90](https://ncatlab.org/nlab/show/SL2Z#Gocho90), [Funar 00](https://ncatlab.org/nlab/show/SL2Z#Funar00), [Manoliu 98](https://ncatlab.org/nlab/show/SL2Z#Manoliu98)) is that this gives a (projective) representation of $SL_2(\mathbb{Z})$.

It is immediate that $S^2 {\vert n \rangle} = {\vert -n \rangle}$ and hence that $S^4 = id$ and that $S^2$ commutes with $T S$. But how about the remaining relation $(T S)^3 = id$. I get

$$
  \begin{array}{l}
    T^{-1} S^{-1} T^{-1}
    {\vert n \rangle}
    \;=\;
    T^{-1} S^{-1}
    e^{ - \tfrac{\pi \mathrm{i}}{k} n^2 }
    {\vert n \rangle}
    \\
    \;=\;
    T^{-1}
    \tfrac{1}{\sqrt{k}}
    \sum_{\widehat{n}}
    e^{ 
      \tfrac{\pi \mathrm{i}}{k} 
      (
        - n^2 - 2 \widehat{n} n 
      )   
    }
    {\vert \widehat{n} \rangle}
    \\
    \;=\;
    \tfrac{1}{\sqrt{k}}
    \sum_{\widehat{n}}
    e^{ 
      \tfrac{\pi \mathrm{i}}{k} 
      (
        - n^2 - 2 \widehat{n} n - \widehat{n}^2
      )   
    }
    {\vert \widehat{n} \rangle}
    \\
    \;=\;
    \tfrac{1}{\sqrt{k}}
    \sum_{\widehat{n}}
    e^{
      - 
      \tfrac{\pi \mathrm{i}}{k} 
      (\widehat{n} + n)^2
    }
    {\vert \widehat{n} \rangle}
  \end{array}
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \text{but}
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \begin{array}{l}
  S T S
    {\big\vert n \big\rangle}
  \;=\;
  S T 
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      \widehat n
  }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, n
     }{
       k
     }
  }
  {\big\vert \widehat{n} \big\rangle}
  \\
  \;=\;
  S
  \tfrac{1}{\sqrt{k}}
  \sum_{
      \widehat n
  }
  \,
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    (
      2 \widehat{n} \, n
      +
      \widehat{n}^2
    )
  }
  {\big\vert \widehat{n} \big\rangle}
  \\
  \;=\;
  \frac{1}{k}
  \sum_{
    \widehat n
    ,\,
    \widehat{\widehat{n}}
  }
  \,
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    (
      2 \widehat{n} \, n
      +
      \widehat{n}^2
      +
      2 \widehat{\widehat{n}} \widehat{n}
    )
  }
  {\big\vert \widehat{\widehat{n}} \big\rangle}
  \\
  \;=\;
  \frac{1}{\sqrt{k}}
  \sum_{ \widehat{\widehat{n}} }
  \underset{??}{
  \underbrace{
  \tfrac{1}{\sqrt{k}}
  \sum_{ \widehat n }
  \,
  e^{
    \tfrac{\pi \mathrm{i}}{k}
      (\widehat{n} + (n + \widehat{\widehat{n}}))^2
  }
  }
  }
  e^{
    -
    \tfrac{\pi \mathrm{i}}{k}
      (n + \widehat{\widehat{n}})^2
  }
  {\big\vert \widehat{\widehat{n}} \big\rangle}
\end{array}
$$

If the term over the brace had another factor of 2 in the exponent, then it would at least be independent of $n$ and $\widehat{\widehat{n}}$ and could be normalized away. But it doesn't. --- But it works for *even $k$*.


$$
  S^2 T S = T S^3 = T S^{-1}
$$
$$
  S T S = S^{-1} T S^{-1}
$$

$$
  T S T S T S \,=\, \mathrm{e}
$$

$$
  S T S 
    \,=\, 
  T^{-1} S^{-1} T^{-1}
$$



$$
  T
  S
    {\big\vert [n] \big\rangle}
  \;=\;
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
     \tfrac{
       \pi \mathrm{i}
     }{k}
     (
       \widehat{n}^2
       +
       2\widehat{n} \, n
     )
  }
  {\big\vert[\widehat{n}]\big\rangle}
$$

$$
  \begin{array}{l}
  (T S)^2
    {\big\vert [n] \big\rangle}
  \;=\;
  \frac{1}{k}
  \sum_{
      [\widehat{\widehat n}] 
  }
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
     \tfrac{
       \pi \mathrm{i}
     }{k}
     (
       \widehat{n}^2
       +
       2\widehat{n} \, n
       +
       \widehat{\widehat{n}}^2
       +
       2\widehat{\widehat{n}} \, \widehat{n}
     )
  }
  {\big\vert[\widehat{\widehat{n}}]\big\rangle}
  \\
  \;=\;
  \frac{1}{k}
  \sum_{
      [\widehat{\widehat n}] 
  }
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
     \tfrac{
       \pi \mathrm{i}
     }{k}
     (
       (\widehat{n} + n + \widehat{\widehat{n}})^2
       -
       (n + \widehat{\widehat{n}})^2
       +
       \widehat{\widehat{n}}^2
     )
  }
  {\big\vert[\widehat{\widehat{n}}]\big\rangle}
  \\
  \;=\;
  const
  \sum_{
      [\widehat{\widehat n}] 
  }
  \,
  e^{
     \tfrac{
       \pi \mathrm{i}
     }{k}
     (
       -n^2 - 2 \widehat{\widehat{n}}n
     )
  }
  {\big\vert[\widehat{\widehat{n}}]\big\rangle}
  \end{array}
$$


$$
  \begin{array}{l}
    (T S)^3
      {\big\vert [n] \big\rangle}
    \\
    \;=\;
  const
  \sum_{
      [\widehat{\widehat{\widehat n}}] 
  }
  \sum_{
      [\widehat{\widehat n}] 
  }
  \,
  e^{
     \tfrac{
       \pi \mathrm{i}
     }{k}
     (
       -n^2 - 2 \widehat{\widehat{n}}n
       + 
       \widehat{\widehat{\widehat{n}}}^2
       +
       2 \widehat{\widehat{\widehat{n}}}\widehat{\widehat{n}}
     )
  }
  {\big\vert[\widehat{\widehat{\widehat{n}}}]\big\rangle}
  \end{array}
$$


$$
  \begin{array}{rcl}
  S^2
  {\big\vert [n] \big\rangle}
  &=&
  S\,
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, n
     }{
       k
     }
  }
  {\big\vert[\widehat{n}]\big\rangle}
  \\
  &=&
  \sum_{
      [\widehat{\widehat n}] 
  }
  \,
  \underset{
    \delta_{-n}(\widehat{\widehat{n}})
  }{
  \underbrace{
  \frac{1}{k}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, 
       (n + \widehat{\widehat{n}})
     }{
       k
     }
  }
  }
  }
  \,
  {\big\vert[\widehat{\widehat{n}}]\big\rangle}
  \\
  &=&
  {\big\vert[-n]\big\rangle}
  \end{array}
$$

$$
  \begin{array}{rcl}
    S T
     {\big\vert [n] \big\rangle}
    &=&
    S
    e^{ 
      \pi \mathrm{i}
      \tfrac{ n^2 }{ k }
    }
    {\big\vert [ n ] \big\rangle}
    \\
    &=&
    \frac{1}{\sqrt{\vert k \vert}}
    \sum_{
        [\widehat n] 
    }
    \,
    e^{
      \tfrac{2 \pi \mathrm{i}}{k}
      (
         \widehat{n} \, n
         +
         n^2/2 
      )
    }
    {\big\vert[\widehat{n}]\big\rangle}
  \end{array}
$$

$$
  \begin{array}{rcl}
    (S T)^2
     {\big\vert [n] \big\rangle}
    &=&
    \frac{1}{k}
    \sum_{
        [\widehat n] 
    }
    \,
    e^{
      \tfrac{2 \pi \mathrm{i}}{k}
      (
         \widehat{n} \, n
         +
         n^2/2 
      )
    }
    \sum_{
        [\widehat{\widehat n}] 
    }
    \,
    e^{
      \tfrac{2 \pi \mathrm{i}}{k}
      (
         \widehat{\widehat{n}} \, \widehat{n}
         +
         \widehat{n}^2/2 
      )
    }
    {\big\vert[\widehat{\widehat{n}}]\big\rangle}
    \\
    &=&
    \frac{1}{k}
    \sum_{
        [\widehat{\widehat n}] 
    }
    \sum_{
        [\widehat n] 
    }
    \,
    e^{
      \tfrac{\pi \mathrm{i}}{k}
      (
         \widehat{n}^2
         + 
         2 \widehat{n}(n + \widehat{\widehat{n}})
         +
         n^2
      )
    }
    {\big\vert[\widehat{\widehat{n}}]\big\rangle}
    \\
    &=&
    \frac{1}{k}
    \sum_{
        [\widehat{\widehat n}] 
    }
    \sum_{
        [\widehat n] 
    }
    \,
    e^{
      \tfrac{\pi \mathrm{i}}{k}
      \big(
         (\widehat{n}
         + 
         n + \widehat{\widehat{n}}
         )^2
         -
         (n + \widehat{\widehat{n}})^2
         +
         n^2
      \big)
    }
    {\big\vert[\widehat{\widehat{n}}]\big\rangle}
    \\
    &=&
    const
    \sum_{
        [\widehat{\widehat n}] 
    }
    \,
    e^{
      -
      \tfrac{2\pi \mathrm{i}}{k}
      \big(
         \widehat{\widehat{n}}^2/2
         +
         n \widehat{\widehat{n}}
      \big)
    }
    {\big\vert[\widehat{\widehat{n}}]\big\rangle}
  \end{array}
$$

$$
  \begin{array}{rcl}
    (S T)^3
     {\big\vert [n] \big\rangle}
    &=&
    const
    \,S T\,
    \sum_{
        [\widehat{\widehat n}] 
    }
    \,
    e^{
      -
      \tfrac{2\pi \mathrm{i}}{k}
      \big(
         \widehat{\widehat{n}}^2/2
         +
         n \widehat{\widehat{n}}
      \big)
    }
    {\big\vert[\widehat{\widehat{n}}]\big\rangle}
    \\
    &=&
    const
    \,S T\,
    \sum_{
        [\widehat{\widehat n}] 
    }
    \,
    e^{
      -
      \tfrac{2\pi \mathrm{i}}{k}
      \big(
         \widehat{\widehat{n}}^2/2
         +
         n \widehat{\widehat{n}}
      \big)
    }
    \sum_{\widehat{\widehat{\widehat{n}}}}
    e^{
      \tfrac{2 \pi \mathrm{i}}{2}
      (
      \widehat{\widehat{\widehat{n}}}
      \widehat{\widehat{n}}
      + 
      \widehat{\widehat{n}}^2/2
      )
    }
    {\big\vert[\widehat{\widehat{\widehat{n}}}]\big\rangle}
  \end{array}
$$

* [[Maissam Barkeshli]], [[Xiao-Liang Qi]]: *Synthetic Topological Qubits in Conventional Bilayer Quantum Hall Systems*, Phys. Rev. X **4** (2014) 041035 \[<a href="https://doi.org/10.1103/PhysRevX.4.041035">doi:10.1103/PhysRevX.4.041035</a>, [arXiv:1302.2673](https://arxiv.org/abs/1302.2673)\]


* Roger S. K. Mong et al.: *Universal Topological Quantum Computation from a Superconductor-Abelian Quantum Hall Heterostructure*, Phys. Rev. X **4** (2014) 011036 \[<a href=" https://doi.org/10.1103/PhysRevX.4.011036">doi:10.1103/PhysRevX.4.011036</a>, [arXiv:1307.4403](https://arxiv.org/abs/1307.4403)\]

* D. V. Averin, V. J. Goldman: *Quantum computation with quasiparticles of the Fractional Quantum Hall Effect*, Solid State Communications **121** 1 (2001) 25-28 \[<a href="https://doi.org/10.1016/S0038-1098(01)00447-1">doi:10.1016/S0038-1098(01)00447-1</a>, [arXiv:cond-mat/0110193](https://arxiv.org/abs/cond-mat/0110193)\]



* A. P. Balachandran, A. Ibort, G. Marmo, M. Martone: *Quantum Geons and Noncommutative Spacetimes*

$$
  0
  \to
  \pi_1(Maps)
  \to
  \pi_2\big(Maps \sslash Diff\big)
  \to   
  B (\mathbb{Z} \times \mathbb{Z})
  \to 
  \pi_1(Maps)
  \to
  \pi_1\big(Maps \sslash Diff\big)
  \to
  B MCG
  \to
  \mathbb{Z}
  \to
  \mathbb{Z}
  \to
  \pi_0(B Diff)
$$

## Annular braid group

The *annular braid group* $Br_n(An)$ on $n \in \mathbb{N}$ strands is the [[surface braid group]] of the [[annulus]], hence the [[fundamental group]] of the [configuration space of points|configuration space of $n$-points]] inside the [[annulus]].

## Properties

\begin{proposition}
  The annular braid group is [[isomorphism|isomorphic]] to a [[semidirect product group|semidirect product]] 
$$
  Br_n(An)
  \,\simeq\,
  Br_n^{aff} \rtimes \mathbb{Z}
$$
of the the [[affine braid group]] with the group of [[integers]], the latter generated by the braid which exhibits a 1-step [[cyclic permutation]].
\end{proposition} 

## References

* Richard P. Kent, David Pfeifer: *A Geometric and algebraic description a
Of annular braid groups*, International Journal of Algebra and Computation **12** 01n02 (2002) 85-97 &lbrack;[doi:10.1142/S0218196702000997](https://doi.org/10.1142/S0218196702000997)&rbrack;


* Paolo Bellingeri, Arnaud Bodin: *The braid group of a necklace*, Mathematische Zeitschrift **283** 3 (2014) &lbrack;[arXiv:1404.2511](https://arxiv.org/abs/1404.2511), [doi:10.1007/s00209-016-1630-0](https://doi.org/10.1007/s00209-016-1630-0)&rbrack;



## Asymptotic gauge groups

Given a [[gauge theory]] (and/or [[gravity]]) on a [[spacetime]] with [[asymptotic boundary]], certain would-be [[gauge transformations]] ([[diffeomorphisms]]) that act non-trivially on asymptotic "boundary data" may in fact be identified as physically observable [[global symmetries]] and hence have, in contrast to actual [[gauge symmetries]], "direct empirical significance" (DES, [Teh 2016](#Teh16)).

A key example is (symmetry generated by) the [[ADM mass]] and generally the [[BMS group]] of asymptotic symmetries in [[asymptotically flat spacetimes]].

Up to technical fine-print (cf. [Borsboom & Posthuma 2015](#BorsboomPosthuma15)) a group of asymptotic symmetries is the [[coset space]] of all gauge symmetries that respect boundary data by the [[subgroup]] of [[bulk]] gauge transformations which act as the [[identity map]] on the [[asymptotic boundary]] (cf. [Strominger 2018 (2.10.1)](#Strominger18), [Borsboom & Posthuma 2015 p 2](#BorsboomPosthuma15)):

$$
  AsymptoticSymmetries
  \;=\;
  \frac{
    BoundaryAdmissibleGaugeSymmetries
  }{
    BulkGaugeSymmetriesTrivialAtBoundary
  }
$$ 

Hence if the bulk gauge symmetries form a [[normal subgroup]] then the asymptotic symmetries form a [[quotient group]] characterized by a [[short exact sequence]] of the form

$$
  1 \to
  BulkGaugeSymmetriesTrivialAtBoundary
  \longrightarrow
  BoundaryAdmissibleGaugeSymmetries
  \longrightarrow
  AsymptoticSymmetries
  \to 
  1
  \,.
$$


## References

* [[Steve Carlip]]: *Dynamics of Asymptotic Diffeomorphisms in $(2+1)$-Dimensional Gravity*, Class. Quant. Grav. **22** (2005) 3055-3060 &lbrack;[arXiv:gr-qc/0501033](https://arxiv.org/abs/gr-qc/0501033), [doi:10.1088/0264-9381/22/14/014](https://doi.org/10.1088/0264-9381/22/14/014)&rbrack;

* {#Teh16} Nicholas Teh: *Galileo's Gauge: Understanding the Empirical Significance of Gauge Symmetry*,  Philosophy of Science **83** (2016) 93-118. 

* {#Strominger18} [[Andrew Strominger]]: *Asymptotic Symmetris*, section 2.10 in: *Lectures on the Infrared Structure of Gravity and Gauge Theory*, Princeton University Press (2018) &lbrack;[ISBN:9780691179506](https://press.princeton.edu/books/hardcover/9780691179506/lectures-on-the-infrared-structure-of-gravity-and-gauge-theory?srsltid=AfmBOoqkVIpm2JaFfW7RzM4IXdIwlfMLkDqPPqfi6QEV9FH87fE5InCT), 
[arXiv:1703.05448](https://arxiv.org/abs/1703.05448)&rbrack;


* {#BorsboomPosthuma15} Silvester Borsboom, [[Hessel Posthuma]]: *Global Gauge Symmetries and Spatial Asymptotic Boundary Conditions in Yang-Mills theory* &lbrack;[arXiv:2502.16151](https://arxiv.org/abs/2502.16151)&rbrack;





[[BonettiAtCQTS-Feb2025.pdf:file]]

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





