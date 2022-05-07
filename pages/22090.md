

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


The _[[Pontryagin isomorphism]]_ ([Pontryagin 38](#Pontryagin38), [Pontryagin 55](#Pontryagin55), review in [Kosinski 93, IX 5.5](#Kosinski93)) is an identification of [[cobordism classes]] of [[normally framed submanifolds]] of [[codimension]] $n$ in a [[closed manifold]] $X^d$ with the $n$-[[Cohomotopy]] of that manifold -- the [[homotopy classes]] of [[maps]] into the [[n-sphere]] --, which is exhibited by the _[[Cohomotopy charge map]]_, often known as the [[Pontryagin-Thom collapse construction]]_:

$$
  Cob^n_Fr(X)
  \overset{\simeq}{\longrightarrow}
  \pi^n(X)
  \,.
$$

The analogous statement, identifying [[cobordism classes]] of [[normally oriented submanifolds]] with [[homotopy classes]] of maps into the [[universal vector bundle|universal]] [[special orthogonal group|special orthogonal]] [[Thom space]] $M SO(n)$, is _[[Thom's theorem]]_ ([Thom 54](#Thom54)). Both statements, as well as their joint generalization to other [[tangential structures]] and notably their [[stabilization]] to [[Whitehead-generalized cohomology theory|Whitehead-generalized]] [[Cobordism cohomology theory]], have come to be widely known as the _[[Pontryagin-Thom collapse construction]]_, or similar, and form the basis of modern [[cobordism theory]] and its application in [[stable homotopy theory]].

## Details

For $X$ a [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] $D$, the assignment of [[Cohomotopy charge]] (the _[[Pontryagin-Thom construction]]_, in this unstable and framed version due to [Pontrjagin 55](#Pontrjagin55), see review in [Kosinski 93, IX.5](#Kosinski93), [Milnor 97](#Milnor97)) identifies the [[set]] 

$$
  SubMfd_{/bord}^{d}(X)
$$

of [[cobordism classes]] of  [[closed manifold|closed]] and [[normally framed submanifolds]] $\Sigma \overset{\iota}{\hookrightarrow} X$ of [[dimension]] $d$ inside $X$ with the [[cohomotopy]] $\pi^{D-d}(X)$ of $X$ in degree $D- d$

$$
  SubMfd_{/bord}^{d}(X)
    \underoverset{\simeq}{\;\;\;PT\;\;\;}{\longrightarrow}
  \pi^{D-d}(X)
  \,.
$$

(e.g. [Kosinski 93, IX Theorem (5.5)](#Kosinski93))

In particular, by this [[bijection]] the canonical [[group]] [[structure]] on [[cobordism groups]] in sufficiently high [[codimension]] (essentially given by [[disjoint union]] of [[submanifolds]]) this way induces a group structure on the cohomotopy sets in sufficiently high degree.



{#PontrjaginThomConstructionGraphics}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/PontrjaginThomConstructionI.jpg" width="800">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)

Here the [[normal framing]] of the submanifolds plays the role of the [[charge]] in [[Cohomotopy]] which they carry:

{#nCohomotopyChargeOfSubmanifoldsIsNormalFraming}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/nCohomotopyChargeOfSubmanifoldsIsNormalFraming.jpg" width="800">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)


For example:

{#nCohomotopyOfEuclideanNSpaceIllustration}$\,$


<center>
<img src="https://ncatlab.org/nlab/files/nCohomotopyOfEuclideanNSpace.jpg" width="840">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)


This construction generalizes to [[equivariant cohomotopy]], see [there](equivariant+cohomotopy#PontryaginThomConstruction).

With the [[equivariant Hopf degree theorem]] the above example has the following $\mathbb{Z}_2$-[[equivariant homotopy theory|equivariant]] version (see [there](equivariant+Hopf+degree+theorem#EquivariantCohomotopyOfRepresentationSpheres)):

{#EquivariantnCohomotopyOfEuclideanNOrientifoldIllustration}$\,$


<center>
<img src="https://ncatlab.org/nlab/files/EquivariantNCohomotopyOfEuclideanNOrientifold.jpg" width="840">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)


Further by the [[equivariant Hopf degree theorem]] (see [there](equivariant+Hopf+degree+theorem#EquivariantCohomotopyOfRepresentationTori)), this example generalizes to [[equivariant cohomotopy]] of [[toroidal orbifold|toroidal]] [[orientifolds]]:


{#EquivariantnCohomotopyOfToroidalNOrientifoldIllustration}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/EquivariantCohomotopyOfToroidalOrientifold.jpg" width="850">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)

\linebreak

### Composition/product in Cohomotopy
  {#ProductInCohomotopy}

Under the [[Pontryagin-Thom isomorphism]] ([above](#RelationToCobordismGroup)) the product in Cohomotopy, i.e. the [[composition]] operation

$$
  \array{
    \pi^{n_1}
    \big( 
      S^{n_2 + n_1}
    \big)
    \times
    \pi^{n_2 + n_1}(X)
    &\overset{}{\longrightarrow}&
    \pi^{n_1}(X)
    \\
    (c_1, c_2) &\mapsto& c_1 \circ c_2
  }
  \,,
$$

corresponds to forming [[product manifolds]] of submanifolds, in that (see also [Kosinski 93, Section IX 6.1](#Kosinski93)):


$$
    \mathrm{PT}^{-1}(c_1 \circ c_2)
    \;\simeq\;
    \Big[
      \mathrm{PT}^{-1}(c_2) \times \mathrm{PT}^{-1}(c_1)
      \;\subset\;
      \mathrm{PT}^{-1}(c_2) \times \mathbb{R}^{n_2 + n_1}
      \;\subset\;
      X
    \Big]
  \,.
$$

This is exhibited by the following [[pasting diagram]] of [[pullbacks]]/[[fiber products]] (repeatedly using the [[pasting law]]):

\begin{imagefromfile}
        "file_name": "ProductInCohomotopyUnderPT.jpg",
        "web": "nlab",
        "width": 600,
        "unit": "px",
        "margin": {
            "top": -20,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "product in Cohomotopy under the PT isomorphism",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

Here the vertical inclusions are the defining ones of the [[submanifolds]] or of their [[normal bundles]], identified with some choice of [[tubular neighbourhoods]].


## References


[[!include Pontryagin-Thom construction -- references]]


[[!redirects Pontryagin's isomorphism]]

[[!redirects Pontrjagin isomorphism]]
[[!redirects Pontrjagin's isomorphism]]

[[!redirects Pontryagin's theorem]]



