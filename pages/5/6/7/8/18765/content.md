

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Given a [[linear differential operator]] $P$, then a _generalized solution_ or _weak solution_ of the corresponding homogenous [[differential equation]] is a [[distribution]] $u$ (hence a "[[generalized function]]" via [this prop](non-singular+distribution#NonSingularDistributionsAreDenseInAllDistributions)) satisfying 

$$
  P u = 0
  \,,
$$

where the differential operator on the left now acts via [[derivatives of distributions]]. This means that for all $b \in \mathcal{D}$ we have

$$
 u(P^\ast(b)) = 0
 \,,
$$

where $P^\ast$ is the [[formally adjoint differential operator]].

This is such that in the case that $u = u_f$ happens to be a [[non-singular distribution]] given by an ordinary [[smooth function]] $f$, then $u_f$ is a generalized solution precisely if $f$ is an ordinary solution:

$$
  \begin{aligned}
    P u_f = 0 \;\;
    & \Leftrightarrow\;\;
      u_f(P^\ast b) = 0 \phantom{AAA}\text{for all}\, b \in \mathcal{D}
    \\
    & \Leftrightarrow\;\;
     \int f P^\ast b \, dvol = 0 \phantom{AAA}\text{for all}\, b \in \mathcal{D}
     \\
     & \Leftrightarrow\;\;
     \int (P f) b \, dvol = 0 \phantom{AAA}\text{for all}\, b \in \mathcal{D}
     \\
     & \Leftrightarrow\;\;
     P f = 0
  \end{aligned}
$$

Similarly there are generalized solutions for the inhomogeneous equation, and in fact now the inhomogeneity may itself be a [[distribution]]. In particular for [[delta distribution]]-inhomogeneity

$$
  P u = \delta
$$

the generalized solutions $u$ are the _[[fundamental solutions]]_ or _[[Green's functions]]_ of $P$.

## Related concepts

* [[fundamental solution]]

* [[Green function]]

* [[formal adjoint differential operator]]

* [[Green hyperbolic differential equation]]

## References

* {#Kanwal04} Ram P. Kanwal, section 10.2 of _Generalized Functions: Theory and Applications_, Springer 2004

[[!redirects distributional solutions of a PDE]]

[[!redirects distributional solution of a partial differential equation]]
[[!redirects distributional solutions of a partial differential equation]]

[[!redirects distributional solutions of partial differential equation]]

[[!redirects distributional solution of a differential equation]]
[[!redirects distributional solutions of a differential equation]]

[[!redirects distributional solutions of differential equations]]

[[!redirects distributional PDE solution]]
[[!redirects distributional PDE solutions]]

[[!redirects distributional solution]]
[[!redirects distributional solutions]]

[[!redirects distributional solution of a PDE]]
[[!redirects distributional solutions of a PDE]]
[[!redirects distributional solutions of PDEs]]

[[!redirects generalized solution of a PDE]]
[[!redirects generalized solutions of a PDE]]

[[!redirects generalized solution of a partial differential equation]]
[[!redirects generalized solutions of a partial differential equation]]

[[!redirects generalized solutions of partial differential equation]]

[[!redirects generalized solution of a differential equation]]
[[!redirects generalized solutions of a differential equation]]

[[!redirects generalized solutions of differential equations]]

[[!redirects generalized PDE solution]]
[[!redirects generalized PDE solutions]]

[[!redirects generalized solution]]
[[!redirects generalized solutions]]


[[!redirects weak solution]]
[[!redirects weak solutions]]



