
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

\tableofcontents

## Definition

### On vector spaces
 {#OnVectorSpaces}

On a [[finite-dimensional vector space|finite-dimensional]] [[real vector space|real]] [[vector space]] $V$, canonically regarded also as a [[smooth manifold]], the *Euler vector field* $\epsilon \colon V \longrightarrow T V$ is that [[vector field]] whose [[flow of a vector field|flow]] $\phi_\epsilon$ is the linear multiplication action of the vector space

$$
  \array{
    V \times \mathbb{R}
      &\xrightarrow{\; \phi_\epsilon \;}&
    V
    \\
    (v,t) 
      &\mapsto& 
    t\cdot v
    \mathrlap{\,.}
  }
$$

For $\big\{v^i \in V^\ast \big\}_{i =1}^{dim(V)}$ any [[linear basis]] of the [[dual vector space]] to $V$, which may be regarded as [[coordinate functions]] on the manifold $V$, then the Euler vector field is equivalenty given by
\[
  \label{CoordinateExpression}
  \epsilon 
    \;=\; 
  \textstyle{\sum_{i=1}^{dim(V)}} 
    v^i \partial_{v^i}
  \,.
\]

### On vector bundles
 {#OnVectorBundles}

More generally, for $V$ a [[real vector bundle|real]] [[vector bundle]] over a [[smooth manifold]] $X$, its Euler vector field is the [[vector field]] on the total space $V$ which over each point $x \in X$ restricts to the above Euler vector field on the [[fiber]] space $V_x$.

For $U \hookrightarrow X$ a [[coordinate chart]] over the base manifold with coordinate functions $\big\{x^j\big\}_{j=1}^{dim(X)}$, so that $V_{\vert U}$ has coordinate functions $(x^j, v^i)$, the Euler vector field on $V_{\vert U}$ is again given by the form (eq:CoordinateExpression).

### For submanifold embeddings

For $Y \xrightarrow{\iota} X$ a [[submanifold]] [[embedding of smooth manifolds|embedding]] of [[smooth manifolds]], a [[vector field]] on $X$ is called *Euler-like* (with respect to $\iota$) if it vanishes on $Y$ and its linear expansion around $Y$ is an Euler vector field, in the [above sense](#OnVectorBundles), on the [[normal bundle]] $N_\iota(Y)$.

([BLM19, Def. 2.6](#BLM19))

## Properties

### Relation to homogeneous functions

A [[smooth function]] $f \colon V \xrightarrow{} \mathbb{R}$ is [[homogeneous function|homogeneous]] of degree $n \in \mathbb{N}$ iff its [[derivative]] along the Euler vector field $\epsilon$ ([above](#OnVectorSpaces)) satisfies

$$
  \epsilon f
  \;=\;
  n f
  \,.
$$

This basic fact is known as *Euler's homogeneous function theorem* (e.g. [Courant 1936](#Courant36)) and this is the origin of the notion of the Euler vector field.


## Related concepts

* [[Liouville-Poincaré 1-form]]


## References

The Euler vector field originates in the proof of [[Leonhard Euler]]'s theorem on [[homogeneous functions]]:

* {#Courant36} [[Richard Courant]]: *Homogeneous Functions*, pp. 108 in vol 1 of: *Differential & Integral Calculus*, 2 volumes (1936) &lbrack;vol1: [ISBN:978-1-118-03149-0](https://www.wiley.com/en-ae/Differential+and+Integral+Calculus%2C+Volume+1%2C+2nd+Edition-p-9781118031490), [ark:/13960/t4fn6m190](https://archive.org/details/in.ernet.dli.2015.205513/), vol2: [ISBN:978-0-471-60840-0](https://www.wiley-vch.de/de/fachgebiete/mathematik-und-statistik/mathematik-16ma/analysis-16ma3/differential-and-integral-calculus-volume-2-978-0-471-60840-0), [ark:/13960/t2g82wq0c](https://archive.org/details/dli.ernet.19986/page/n5/mode/2up), [pdf](https://www.ime.usp.br/~gorodski/ps/Courant-DifferentialIntegralCalculusVolIi.pdf)&rbrack;

* Wolfram MathWorld: *[Euler's Homogeneous Function Theorem](https://mathworld.wolfram.com/EulersHomogeneousFunctionTheorem.html)*

Discussion in the generality of [[dg-manifolds]] ([[L-infinity algebroids|$L_\infty$-algebroids]]):

* [[Dmitry Roytenberg]]: §2 in: *On the structure of graded symplectic supermanifolds and Courant algebroids*, in *Quantization, Poisson Brackets and Beyond*, Contemp. Math. **315**, Amer. Math. Soc. (2002) &lbrack;[arXiv:math/0203110](https://arxiv.org/abs/math/0203110), [ams:conm-315](https://bookstore.ams.org/conm-315)&rbrack;

On Euler-like vector fields:

* {#BLM19} [[Henrique Bursztyn]], Hudson Lima, [[Eckhard Meinrenken]], section 2 of: *Splitting theorems for Poisson and related structures*, J. Reine Angew. Math. **754** (2019) 281--312 &lbrack;[arXiv:1605.05386](https://arxiv.org/abs/1605.05386), [doi:10.1515/crelle-2017-0014](https://doi.org/10.1515/crelle-2017-0014)&rbrack;

* [[Eckhard Meinrenken]]: *Euler-like vector fields, normal forms, and isotropic embeddings*, Indagationes Mathematicae **32** 1 (2021) 224-245, Indagationes Mathematicae &lbrack;[arXiv:2001.10518](https://arxiv.org/abs/2001.10518), [doi:10.1016/j.indag.2020.08.006](https://doi.org/10.1016/j.indag.2020.08.006)&rbrack;

* Arthur Lei Qiu: *Euler-like vector fields* (2021) &lbrack;notes:[pdf](https://www.math.toronto.edu/qiu/writings/EulerLike.pdf), [[Qiu-EulerVFnotes.pdf:file]], slides:[pdf](https://www.math.toronto.edu/qiu/writings/EulerLike_Slides_annotated.pdf), [[Qiu-EulerVFslides.pdf:file]]&rbrack;

* L. A. Visscher: *Euler-like vector fields and normal forms*, Master thesis (2021) &lbrack;[pdf](https://webspace.science.uu.nl/~crain101/thesis-Luuk-Vischer.pdf), [[Visscher-EulerVectorFields.pdf:file]]&rbrack;

[[!redirects Euler vector fields]]

[[!redirects Euler's homogeneous function theorem]]
[[!redirects Euler homogeneous function theorem]]

[[!redirects Euler's theorem on homogeneous functions]]

