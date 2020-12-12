
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

$$
  \array{
    \pi_3^s &\simeq& \mathbb{Z}/24
    \\
    [h_{\mathbb{H}}] &\leftrightarrow& [1]
  }
$$

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
        "alt": "homotopy pasting diagram exhibiting the homotopy Whitehead integral",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

Under the [[Pontrjagin-Thom isomorphism]], identifying the [[stable homotopy groups of spheres]] with the [[bordism ring]] $\Omega^{fr}_\bullet$ of [[stable framing|stably framed]] manifolds (see at _[[MFr]]_), this generator is represented by the [[3-sphere]] (with its left-invariant framing induced from the identification with the [[Lie group]] [[SU(2)]] $\simeq$ [[Sp(1)]] )


$$
  \array{
    \pi_3^s & \simeq & \Omega_3^{fr} 
    \\
    [h_{\mathbb{H}}] & \leftrightarrow & [S^3]
    \,.
  }
$$

Moreover, the relation $24 \cdot [S^3] \,\simeq\, 0$ is represented by the [[bordism]] which is the [[complement]] of 24 [[open balls]] inside [[generalized the|the]] [[K3]]-manifold (e.g. [Wang-Xu 10, Sec. 2.6](#WangXu10), [Bauer 10](#Bauer10), [SP 17](#SP17)).

## Related concepts

* [[quaternionic Hopf fibration]]

## References

The original computation is due to

* [[Vladimir Abramovich Rokhlin]], _On a mapping of the $(n+3)$-dimensional sphere into the $n$-dimensional sphere_,  (Russian) Doklady Akad. Nauk SSSR (N.S.) 80, (1951). 541–544

with a mistake (in the unstable range) corrected in 

* [[Vladimir Abramovich Rokhlin]], _New results in the theory of four-dimensional manifolds_, (Russian) Doklady Akad. Nauk SSSR (N.S.) 84, (1952). 221–224.

French translations are in:

* Lucien Guillou, Alexis Marin (eds.), _A la Recherche de la Topologie Perdue: I. Du côté de chez Rohlin. II. Le côté de Casson_, Progress in Mathematics 62, Birkhäuser Boston 1985 (ISBN:0817633294, 9780817633295)


Review:

* {#WangXu10} [[Guozhen Wang]], Zhouli Xu, Section 2.6 of: _A survey of computations of homotopy groups of Spheres and Cobordisms_, 2010 ([[WangXuHomotopyGroupsOfSpheres2010.pdf:file]])

See also:

* {#Bauer10} [[Tilman Bauer]], answer to: _third stable homotopy group of spheres via geometry?_, 2010 ([MO:a/44885](https://mathoverflow.net/a/44885/381))

* {#SP17} [[Chris Schommer-Pries]], answer to: _Nilpotence of the stable Hopf map via framed cobordism_, 2017 ([MO:a/218053](https://mathoverflow.net/a/218053/381))



[[!redirects 3rd stable homotopy group of spheres]]

[[!redirects third stable stem]]
[[!redirects 3rd stable stem]]


