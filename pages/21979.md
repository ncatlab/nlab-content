
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

The first [[stable homotopy group of spheres]] (the first [[stable stem]]) is the [[cyclic group of order 2]]:

\[
  \label{ComplexHopfFibrationGeneratingpi1}
  \array{
    \pi_1^s &\simeq& \mathbb{Z}/2
    \\
    [h_{\mathbb{C}}] &\leftrightarrow& [1]
  }
\]

where the generator $[1] \in \mathbb{Z}/2$ is represented by the [[complex Hopf fibration]] $S^3 \overset{h_{\mathbb{C}}}{\longrightarrow} S^2$.

\begin{imagefromfile}
        "file_name": "PuncturedSphereBordismBetweenTwoCircles.jpg",
        "web": "nlab",
        "width": 200,
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

### As the first framed bordism group 

Under the [[Pontrjagin-Thom isomorphism]], identifying the [[stable homotopy groups of spheres]] with the [[bordism ring]] $\Omega^{fr}_\bullet$ of [[stable framing|stably framed]] manifolds (see at _[[MFr]]_), the generator (eq:ComplexHopfFibrationGeneratingpi1) is represented by the [[1-sphere]] (with its left-invariant framing induced from the identification with the [[Lie group]] [[U(1)]])


$$
  \array{
    \pi_1^s & \simeq & \Omega_1^{fr} 
    \\
    [h_{\mathbb{C}}] & \leftrightarrow & [S^1_{fr=1}]
    \,.
  }
$$

Moreover, the relation $2 \cdot [S^1_{Lie}] \,\simeq\, 0$ is represented by the [[bordism]] which is the [[complement]] of 2 [[open balls]] inside [[generalized the|the]] [[2-sphere]].



## Related concepts

* [[complex Hopf fibration]]

* [[second stable homotopy group of spheres]]

* [[third stable homotopy group of spheres]]

## References

The original computation:

* {#Pontrjagin55} [[Lev Pontrjagin]], Sections 14, 15 of: _Smooth manifolds and their applications in Homotopy theory_, Trudy Mat. Inst. im Steklov, No 45, Izdat. Akad. Nauk. USSR, Moscow, 1955 (AMS Translation Series 2, Vol. 11, 1959) ([doi:10.1142/9789812772107_0001](https://www.worldscientific.com/doi/abs/10.1142/9789812772107_0001))


Review:

* [[Daniel Freed]], [[Karen Uhlenbeck]], Appendix B of: _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

* {#WangXu10} [[Guozhen Wang]], Zhouli Xu, Section 2.3 of: _A survey of computations of homotopy groups of Spheres and Cobordisms_, 2010 ([[WangXuHomotopyGroupsOfSpheres2010.pdf:file]])

* {#Putnam} [[Andrew Putman]], Section 5 of: _Homotopy groups of spheres and low-dimensional topology_ ([pdf](http://www.math.rice.edu/~andyp/notes/HomotopySpheresLowDimTop.pdf), [[PutmanHomotopyGroupsOfSpheres.pdf:file]])





[[!redirects 1st stable homotopy group of spheres]]

[[!redirects first stable stem]]
[[!redirects 1st stable stem]]


