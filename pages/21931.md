
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The third [[stable homotopy group of spheres]] (the third [[stable stem]]) is the [[cyclic group]] of [[order of a group|order]] 24:

\[
  \label{QuaternionicHopfFibrationGeneratingpi3}
  \array{
    \pi_3^s &\simeq& \mathbb{Z}/24
    \\
    [h_{\mathbb{H}}] &\leftrightarrow& [1]
  }
\]

where the generator $[1] \in \mathbb{Z}/24$ is represented by the [[quaternionic Hopf fibration]] $S^7 \overset{h_{\mathbb{H}}}{\longrightarrow} S^4$.

\begin{imagefromfile}
        "file_name": "K3CobordismBetween24ThreeSpheres.jpg",
        "web": "nlab",
        "width": 260,
        "unit": "px",
        "float": "right",
        "margin": {
            "top": -40,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

## Properties

### As the third framed bordism group 

Under the [[Pontrjagin-Thom isomorphism]], identifying the [[stable homotopy groups of spheres]] with the [[bordism ring]] $\Omega^{fr}_\bullet$ of [[stable framing|stably framed]] manifolds (see at _[[MFr]]_), the generator (eq:QuaternionicHopfFibrationGeneratingpi3) is represented by the [[3-sphere]] (with its left-invariant framing induced from the identification with the [[Lie group]] [[SU(2)]] $\simeq$ [[Sp(1)]] )


$$
  \array{
    \pi_3^s & \simeq & \Omega_3^{fr} 
    \\
    [h_{\mathbb{H}}] & \leftrightarrow & [S^3_{fr=1}]
    \,.
  }
$$

Moreover, the relation $24 \cdot [S^3_{Lie}] \,\simeq\, 0$ is represented by the [[bordism]] which is the [[complement]] of 24 [[open balls]] inside [[generalized the|the]] [[K3]]-manifold (e.g. [Wang-Xu 10, Sec. 2.6](#WangXu10), [Bauer 10](#Bauer10), [SP 17](#SP17)).

### Via the fourth $(SU,fr)$-bordism group
 {#ViaTheFourthSuFrBordismGroup}

Equivalently, the elements of $\pi_3^s \,\simeq\, \Omega^{fr}_3$ are detected by half the [[Todd classes]] of [[coboundary|cobounding]] manifolds with [[special unitary group]]-[[tangential structure]] on their [[stable tangent bundle]] (elements of the [[MSUFr]]-[[bordism ring]]):

We have the following [[short exact sequence]] of the [[MSU]]-, [[MSUFr]]- and [[MFr]]-[[bordism rings]] ([Conner-Floyd 66, p. 104](#ConnerFloyd66))

\[
  \label{HalfToddClassesOnShortExactSequenceOfSUFrBordismRings}
  \array{
  0 
  \to
  &
  \Omega^{SU}_{8\bullet+4}
  &
  \overset{i}{\longrightarrow}
  &
  \Omega^{SU,fr}_{8\bullet+4}
  &
  \overset{\partial}{
    \longrightarrow
  }
  &
  \Omega^{fr}_{8\bullet + 3}
  &
  \simeq
  &
  \pi^s_{8\bullet+3}
  \\
  & 
  \big\downarrow{}^{\tfrac{1}{2}\mathrlap{Td}}
  &&
  \big\downarrow{}^{\tfrac{1}{2}\mathrlap{Td}}
  &&
  \big\downarrow{}^{}
  &&
  \big\downarrow{}^{e_{\mathbb{R}}}
  \\
  0 
  \to
  & 
  \mathbb{Z}
  &\overset{\;\;\;\;\;}{\hookrightarrow}&
  \mathbb{Q}  
  &\overset{\;\;\;\;}{\longrightarrow}&
  \mathbb{Q}/\mathbb{Z}
  &=&
  \mathbb{Q}/\mathbb{Z}
  }
\]

which produces from half the [[Todd class]] of cobounding $(SU,fr)$-manifolds the [[KO]]-theoretic [[Adams e-invariant]] $e_{\mathbb{R}}$ ([Adams 66, p. 39](e-invariant#Adams66)) of the boundary manifold in $\Omega^{fr}_{8k + 3} \simeq \pi^s_{8k+3}$. For $k = 0$ this detects the third stable homotopy group of spheres, by the following:

+-- {: .num_prop #AdamseRInvariantDetectsThirdStableHomotopyGroupOfSpheres} 
###### Proposition
**([Adams 66, Example 7.17  and p. 46](e-invariant#Adams66))**

In degree 3, the [[KO]]-theoretic [[e-invariant]] $e_{\mathbb{R}}$ takes the value $\left[\tfrac{1}{24}\right] \in \mathbb{Q}/\mathbb{Z}$ on the [[quaternionic Hopf fibration]] $S^7 \overset{h_{\mathbb{H}}}{\longrightarrow} S^4$  and hence reflects the full [[third stable homotopy group of spheres]]:

$$
  \array{
    \pi^s_3 
      &
      \underoverset{
        \simeq
      }{
        e_{\mathbb{R}}
      }{
        \;\;\longrightarrow\;\;
      } 
      &
    \mathbb{Z}/24 
    & 
    \subset 
    &  
    \mathbb{Q}/\mathbb{Z}
    \\
    [h_{\mathbb{H}}]
    &&\mapsto&&
    \left[\tfrac{1}{24}\right]    
  }
$$

while $e_{\mathbb{C}}$ sees only "half" of it (by [Adams 66, Prop. 7.14](e-invariant#Adams66)).

=--


## Related concepts

* [[quaternionic Hopf fibration]]

* [[first stable homotopy group of spheres]]

* [[second stable homotopy group of spheres]]

## References

The original computation:

* [[Vladimir Abramovich Rokhlin]], _On a mapping of the $(n+3)$-dimensional sphere into the $n$-dimensional sphere_,  (Russian) Doklady Akad. Nauk SSSR (N.S.) 80, (1951). 541–544

with a mistake (in the unstable range) corrected in 

* [[Vladimir Abramovich Rokhlin]], _New results in the theory of four-dimensional manifolds_, (Russian) Doklady Akad. Nauk SSSR (N.S.) 84, (1952). 221–224.

French translations are in:

* Lucien Guillou, Alexis Marin (eds.), _A la Recherche de la Topologie Perdue: I. Du côté de chez Rohlin. II. Le côté de Casson_, Progress in Mathematics 62, Birkhäuser Boston 1985 (ISBN:0817633294, 9780817633295)


Review:

* {#WangXu10} [[Guozhen Wang]], Zhouli Xu, Section 2.6 of: _A survey of computations of homotopy groups of Spheres and Cobordisms_, 2010 ([[WangXuHomotopyGroupsOfSpheres2010.pdf:file]])

More on the computation via the [[MFr|framed cobordism ring]] and the [[K3-manifold]] giving the [[cobordism]] that witnesses the [[order of a group|order]] of 24:

* {#Bauer10} [[Tilman Bauer]], answer to: _third stable homotopy group of spheres via geometry?_, 2010 ([MO:a/44885](https://mathoverflow.net/a/44885/381))

* {#SP17} [[Chris Schommer-Pries]], answer to: _Nilpotence of the stable Hopf map via framed cobordism_, 2017 ([MO:a/218053](https://mathoverflow.net/a/218053/381))

Via [[immersions]] of 3-spheres into Euclidean 4-space

* A. Szűcs, _Two Theorems of Rokhlin_, Journal of Mathematical Sciences 113, 888–892 (2003) ([doi:10.1023/A:1021208007146](https://doi.org/10.1023/A:1021208007146))


* Tobias Ekholm, Masamichi Takase, _Singular Seifert surfaces and Smale invariants for a family of 3-sphere immersions_, 	Bulletin of the London Mathematical Society 43 (2011) 251--266 ([arXiv:0903.0238](https://arxiv.org/abs/0903.0238))




[[!redirects 3rd stable homotopy group of spheres]]

[[!redirects third stable stem]]
[[!redirects 3rd stable stem]]


