+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _Yang-Mills-Higgs equations_ (or _YMH equations_) arise from a generalization of the Yang-Mills action functional with a section, which in physics represents the [[Higgs field]].


## Definition


In the following, consider 

* $G$ be a [[compact Lie group]] 

* with [[Lie algebra]] $\mathfrak{g}$,

* $P \twoheadrightarrow B$ a [[principal bundle|principal $G$-bundle]] over 

* a compact [[orientable]] [[Riemannian manifold]] $(B,g)$, 

and write

*  $Ad_P \,\coloneqq\, P \times_G \mathfrak{g}$ for its [[adjoint bundle]],

* $\Gamma^\infty(Ad_P)$ for the [[space of smooth sections]],

* $\Omega^1_{conn}(P;\mathfrak{g}) \subset \Omega^1(P;\mathfrak{g})$ for the [[Lie algebra valued differential 1-forms]] which are ([[Ehresmann connection|Ehresmann]]) [[connection on a principal bundle|connection forms]]

  (and [[invariant polynomial|recall]] that the [[gauge invariance|gauge-invariants]] of the [[curvature 2-form]] $F_A$ of $A \in \Omega^1_{conn}(P;\mathfrak{g})$ descend to, hence are [[pullback of differential forms|pulled back from]], plain [[differential forms]] on $B$).

If the base space is not [[compact topological space|compact]], then in the following the [[gauge field]] $A \in \Omega^1_{conn}(P;\mathfrak{g})$ and the [[Higgs field]] $\Phi \in \Gamma^\infty(Ad_P)$ are required to [[vanishing at infinity|vanish at infinity]] (cf. [Taubes 1982a, Equation (2.3)](#Taubes82a)).

### Action functional
 {#ActionFunctional}

The _Yang-Mills-Higgs [[action functional]]_ (or _YMH action functional_) is given by:

\[
  \label{TheActionFunctional}
  \begin{array}{ccc}
  \mathllap{
    S_{YMH}
    \,\colon\,
  }
  \Omega^1_{conn}(P;\mathfrak{g})
  \times
  \Gamma^\infty(Ad_P)
  &\longrightarrow&
  \mathbb{R}
  \\
  \big(A, \Phi\big)
  &\mapsto&
  S_{YMH}(A,\Phi)
  \mathrlap{
    \coloneqq
  \textstyle{\int_B}
    \big(
      \|F_A\|^2 
        + 
      \|\mathrm{d}_A\Phi\|^2
    \big)
  \mathrm{d}\vol_g
  \,.
  }
  \end{array}
\]

(cf. [Taubes 1982a, Equation (2.1)](#Taubes82a))

### Yang-Mills-Higgs equations and pairs

A [[pair]] consisting of a [[connection on a principal bundle|connection]] $A\in\Omega^1_{conn}(P;\mathfrak{g})$ and a [[section]] $\Phi\in\Gamma^\infty(B,Ad_P)$ is called a _Yang-Mills-Higgs pair_ (or _YMH pair_) if it is a [[critical point]] of the Yang-Mills-Higgs action functional (eq:TheActionFunctional), hence if:

$$
  \frac{\mathrm{d}}{\mathrm{d}t}
  S_{YMH}\big(
    \alpha(t),
    \varphi(t)
  \big)\vert_{t=0}
  \;=\;
  0
$$

for all pairs of smooth families 

$$
  \begin{array}{ccc}
  \mathllap{
    \alpha\colon
  }
  (-\varepsilon, \varepsilon)
    &
    \longrightarrow 
    &
  \Omega^1_{conn}(P;\mathfrak{g})
  \\
  \mathllap{
    \varphi\colon
  }
  (-\varepsilon,\varepsilon)
    &
    \longrightarrow
    &
  \Gamma^\infty(Ad_P)
  \mathrlap{\,,}
  \end{array}
$$ 

with $\alpha(0)=A and \varphi(0)=\Phi$,

(where $(-\epsilon, \epsilon) \subset \mathbb{R}$ denotes an [[open ball]] around the origin of the [[real line]]).


This is the case iff the [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] are satisfies, here called the *Yang-Mills-Higgs equations* (or _YMH equations_):

\[
  \label{YMHEquations}
  \begin{array}{ccc}
    \mathrm{d}_A \star F_A
    +  
    \star[\Phi,\mathrm{d}_A\Phi]
    &=&
    0
    \\
    \mathrm{d}_A\star\mathrm{d}_A\Phi
    &=&
    0
    \mathrlap{\,.}
  \end{array}
\]

(cf. [Taubes 1982a, Eq. (2.2a) and (2.2b)](#Taubes82a), [Taubes 1984, Eq. (1)](#Taubes84), [Taubes 1985, Eq. (A.1.1a) and (A.1.1b)](#Taubes85), but beware that [Taubes 1984, Eq. (1)](#Taubes84) is missing the second [[Hodge star operator]] in the first [[Yang-Mills-Higgs equation]]. cf. [Naber 11, Eq. (2.5.12)](#Naber11))

Furthermore, the following [[Bianchi identities]] hold:

$$
  \begin{array}{ccc}
  \mathrm{d}_A F_A
  &=&
  0
  \\
  \mathrm{d}_A\mathrm{d}_A\Phi
  +[\Phi,F_A]
  &=&
  0
  \end{array}
$$

(cf. [Taubes 1982a, Eq. (2.2c) and (2.2d)](#Taubes82a), [Naber 11, Eq. (2.5.13)](#Naber11))


Using $\star^2=(-1)^{k(n-k)}$ (see [there](Hodge+star+operator#BasicProperties)) and $\delta_A=(-1)^{n(k+1)+1}\star\mathrm{d}_A\star$ when applied to $k$-forms, the first Yang-Mills-Higgs equation (eq:YMHEquations) is equivalent to:

$$
  \delta_A F_A
  +
  [\Phi,\mathrm{d}_A\Phi]
  \;=\;
  0
  \mathrlap{\,.}
$$

and the second one to:

$$
  \delta_A\mathrm{d}_A\Phi
  \;=\;
  0  
  \mathrlap{,.}
$$

\begin{remark}
For an [[abelian group|abelian]] [[Lie group]] as [[structure group]], its [[Lie algebra]] is also abelian and hence all [[Lie brackets]] vanish and the YMH equations (eq:YMHEquations) reduce to:

$$
  \begin{array}{ccc}
  \mathrm{d}\star\mathrm{d}A
  &=&
  0
  \\
  \mathrm{d}\star\mathrm{d}\Phi
  &=&
  0
  \mathrlap{\,.}
  \end{array}
$$

\end{remark}


## Properties

### General

Essentially by definition:

\begin{lem}
$A\in\Omega^1_{conn}(P; \mathfrak{g})$ is a Yang-Mills connection (a solution of the plain [[Yang-Mills equations]]) iff $(A,0)\in\Omega^1_{conn}(P)\times\Gamma^\infty(Ad_P)$ is a Yang-Mills-Higgs pair.
\end{lem}


### Relation to generalized Laplace equation

Let:

$$
  \Delta_A
  \;\coloneqq\;
  \delta_A\mathrm{d}_A
    +
  \mathrm{d}_A\delta_A
  \;\colon\;
  \Omega^k(B,\operatorname{Ad}(E))
    \longrightarrow
  \Omega^k(B,\operatorname{Ad}(E))
$$

be a [[generalized Laplace operator]].

The [[Bianchi identity]] $\mathrm{d}_A F_A=0$ and the first [[Yang-Mills-Higgs equation]] $\delta_A F_A=-[\Phi,\mathrm{d}_A\Phi]$ combine to:

$$
  \Delta_A F_A
  \;=\;
  -\mathrm{d}_A[\Phi,\mathrm{d}_A\Phi].
$$

The trivial identity $\delta_A\Phi=0$ (since $\Phi$ is a $0$-form whose degree cannot be lowered any further) and the second [[Yang-Mills-Higgs equation]] $\delta_A\mathrm{d}_A\Phi=0$ combine to:

$$
  \Delta_A\Phi
  \;=\;
  0
  \mathrlap{\,.}
$$

## Inhomogenous Yang-Mills-Higgs equations

For a [[principal connection]] $B\in\Omega^1_{conn}(P)$ and a [[smooth section]] $\Psi\in\Gamma^\infty(Ad_P)$, one can consider the *inhomogenous Yang-Mills-Higgs equations*:
\[
  \label{inhomYMHEquations}
  \begin{array}{ccc}
    \delta_A F_A
    +[\Phi,\mathrm{d}_A\Phi]
    &=&
    B
    \\
    \delta_A\mathrm{d}_A\Phi
    &=&
    \Psi
    \mathrlap{\,.}
  \end{array}
\]


## Related entries

* [[stable Yang-Mills-Higgs pair]]

* [[Einstein-Yang-Mills-Dirac-Higgs theory]]

## References

* {#Taubes82a} [[Clifford Taubes]], _The existence of a non-minimal solution to the $\operatorname{SU}(2)$ Yang-Mills-Higgs equations on $\mathbb{R}^3$ Part I_, Communications in Mathematical Physics **86** (1982) 257–298 &lbrack;[doi:10.1007/BF01206014](https://doi.org/10.1007/BF01206014)&rbrack;

* {#Taubes82b} [[Clifford Taubes]], _The existence of a non-minimal solution to the $\operatorname{SU}(2)$ Yang-Mills-Higgs equations on $\mathbb{R}^3$ Part II_, Communications in Mathematical Physics **86** (1982) 299–320 &lbrack;[doi:10.1007/BF01212170](https://doi.org/10.1007/BF01212170)&rbrack;

* {#Taubes84} [[Clifford Taubes]], _On the Yang--Mills--Higgs equations_, Bulletin of the American Mathematical Society **10** (1984) 295–297 &lbrack;[doi:10.1090/s0273-0979-1984-15254-6](https://doi.org/10.1090/s0273-0979-1984-15254-6)&rbrack;

* {#Taubes85} [[Clifford Taubes]], _Min-max theory for the Yang-Mills-Higgs equations_, Communications in Mathematical Physics **97** (1985) 295–297 &lbrack;[doi:10.1007/BF01221215](https://doi.org/10.1007/BF01221215)&rbrack;

* {#Naber11} [[Gregory L. Naber]], *Topology, Geometry and Gauge fields -- Foundations*,  Texts in Applied Mathematics **25** (2011) &lbrack;[doi:10.1007/978-1-4419-7254-5](https://doi.org/10.1007/978-1-4419-7254-5)&rbrack;

See also:

* Wikipedia, [Yang-Mills-Higgs equations](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills%E2%80%93Higgs_equations)

[[!redirects Yang-Mills-Higgs equation]]
[[!redirects Yang-Mills-Higgs pair]]
[[!redirects Yang-Mills-Higgs pairs]]
[[!redirects YMH equation]]
[[!redirects YMH equations]]
[[!redirects YMH pair]]
[[!redirects YMH pairs]]

[[!redirects inhomogenous Yang-Mills-Higgs equation]]
[[!redirects inhomogenous Yang-Mills-Higgs equations]]
[[!redirects inhomogenous Yang-Mills-Higgs pair]]
[[!redirects inhomogenous Yang-Mills-Higgs pairs]]
[[!redirects inhomogenous YMH equation]]
[[!redirects inhomogenous YMH equations]]
[[!redirects inhomogenous YMH pair]]
[[!redirects inhomogenous YMH pairs]]

[[!redirects Yang-Mills-Higgs action]]
[[!redirects Yang-Mills-Higgs action functional]]
[[!redirects YMH action]]
[[!redirects YMH action functional]]