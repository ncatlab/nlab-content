
Consider the homotopy fiber sequence

$$
  S^4
    \longrightarrow 
  S^4//S^1
    \longrightarrow 
  B S^1
$$

since all three spaces are connected with abelian fundamental group, we have the corresponding long exact sequence of rational homotopy groups (e.g. cor. 1.2.2 [here](http://www.ru.nl/publish/pages/813276/rational_homotopy_theory.pdf))

$$
  \cdots
   \to
  \pi^{\bullet+1}(S^4)_{\mathbb{Q}}
    \longrightarrow 
  \pi^{\bullet+1}(S^4//S^1)_{\mathbb{Q}}
    \longrightarrow 
  \pi^{\bullet+1}(B S^1)_{\mathbb{Q}}
    \longrightarrow
  \pi^{\bullet}(S^4)_{\mathbb{Q}}
    \longrightarrow 
  \pi^\bullet(S^4//S^1)_{\mathbb{Q}}
    \longrightarrow 
  \pi^\bullet(B S^1)_{\mathbb{Q}}
    \longrightarrow
  \pi^{\bullet-1}(S^4)_{\mathbb{Q}}
    \longrightarrow 
  \pi^{\bullet-1}(S^4//S^1)_{\mathbb{Q}}
    \longrightarrow 
  \pi^{\bullet-1}(B S^1)_{\mathbb{Q}}
    \to
  \cdots
$$

This yields

$$
  \array{
  &&
  0
    &\longrightarrow&
  \pi^1(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
  &&
  0
    &\longrightarrow&
  \pi^2(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  \mathbb{Q}
    &\longrightarrow&
   0
  \\
  &&
  0
    &\longrightarrow&
  \pi^3(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
  0
    &\longrightarrow&
  \mathbb{Q}
    &\longrightarrow&
  \pi^4(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
    &&
  0
    &\longrightarrow&
  \pi^5(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
    &&
  0
    &\longrightarrow&
  \pi^6(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
  0
    &\longrightarrow&
  \mathbb{Q}
    &\longrightarrow&
  \pi^7(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
  \\
  &&
  0
    &\longrightarrow&
  \pi^{2k+8}(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  }
$$

hence in conclusion

| $n$ | 0 | 1 | 2 | 3 | 4 |  5 | 6 | 7 | 8 | 9 | 10 | $\cdots$ |
|-----|---|---|---|---|---|----|---|---|---|----|----------|
| $\pi^n(S^4//S^1)_{\mathbb{Q}} =$ |  $\mathbb{Q}$ | $0$ | $\array{ 0 \\ \oplus \\ \mathbb{Q}}$ | $0$ | $\array{\mathbb{Q} \\ \oplus \\ 0}$ | $0$ | $\array{ 0 \\ \oplus \\ 0}$ | $\array{ \mathbb{Q} \\ \oplus \\ 0 }$   | $\array{ 0 \\ \oplus \\ 0 }$  | $0$   | $\array{ 0 \\ \oplus \\ 0 }$  |  $\cdots$ |

$\,$

We also have the long exact sequence in cohomology

$$
   \longrightarrow
  H^{\bullet-1}(B S^1,\mathbb{Q})
   \longrightarrow
  H^{\bullet-1}(S^4//S^1,\mathbb{Q})
   \longrightarrow
  H^{\bullet-1}(S^4,\mathbb{Q})
    \longrightarrow
  H^\bullet(B S^1,\mathbb{Q})
   \longrightarrow
  H^\bullet(S^4//S^1,\mathbb{Q})
   \longrightarrow
  H^\bullet(S^4,\mathbb{Q})
   \longrightarrow
  H^{\bullet+1}(B S^1,\mathbb{Q})
   \longrightarrow
  H^{\bullet+1}(S^4//S^1,\mathbb{Q})
   \longrightarrow
  H^{\bullet+1}(S^4,\mathbb{Q})
    \longrightarrow
  \cdots
$$

This yields

$$
  \array{
    &&
    0
      &\longrightarrow&
    H^1(S^4//S^1,\mathbb{Q})
      &\longrightarrow&
    0
    \\
    0
      &\longrightarrow&
    \mathbb{Q}
      &\longrightarrow&
    H^2(S^4//S^1,\mathbb{Q})
      &\longrightarrow&
    0
    \\
    &&
    0
      &\longrightarrow&
    H^3(S^4//S^1,\mathbb{Q})
      &\longrightarrow&
    0
    \\
    0
      &\longrightarrow&
    \mathbb{Q}
      &\longrightarrow&
    H^4(S^4//S^1,\mathbb{Q})
      &\longrightarrow&
    \mathbb{Q}
      &\longrightarrow&
    0
    \\
      &&
    0
      &\longrightarrow&
    H^5(S^4//S^1,\mathbb{Q})
      &\longrightarrow&
    0
    \\
    0
      &\longrightarrow&
    \mathbb{Q}
      &\longrightarrow&
    H^6(S^4//S^1,\mathbb{Q})
      &\longrightarrow&
    0
    \\
      &&
    0
      &\longrightarrow&
    H^7(S^4//S^1,\mathbb{Q})
      &\longrightarrow&
    0
    \\
    0
      &\longrightarrow&
    \mathbb{Q}
      &\longrightarrow&
    H^8(S^4//S^1,\mathbb{Q})
      &\longrightarrow&
    0
  }
$$


hence in conclusion

| $n$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | $\cdots$ |
|-----|---|---|---|---|---|---|---|---|---|---|----|----------|
| $H^n(S^4//S^1,\mathbb{Q}) =$ |  $\mathbb{Q}$ | $0$ | $\array{ 0 \\ \oplus \\ \mathbb{Q}}$ | $0$ | $\array{\mathbb{Q} \\ \oplus \\ \mathbb{Q}}$ | $0$ | $\array{0 \\ \oplus \\ \mathbb{Q}}$ | $\array{ 0 \\ \oplus \\ 0 }$   | $\array{ 0 \\ \oplus \\ \mathbb{Q} }$  | $0$   | $\array{ 0 \\ \oplus \\ \mathbb{Q} }$  |  $\cdots$ |


$\,$

$\,$

$\,$

$\,$
$\,$

$\,$


$\,$

$\,$

* D. Cremades, [[Luis Ibáñez]], F. Marchesano, _Intersecting brane models of particle physics and the Higgs mechanism_, JHEP, 0207, 022 2002 ([arXiv:hep-th/0203160](https://arxiv.org/abs/hep-th/0203160))
 
[[HiggsVacuumStabilityIII.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStabilityIII.png" width="700">



[[HiggsPotentials.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsPotentials.png" width="600">


[[HiggsVacuumStability.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStability.png" width="600">

[[HiggsVacuumStabilityII.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStabilityII.png" width="400">



