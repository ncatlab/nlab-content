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


## Yang-Mills-Higgs action functional
 {#ActionFunctional}

Consider 

* $G$ be a [[compact Lie group]] 

* with [[Lie algebra]] $\mathfrak{g}$,

* $P \twoheadrightarrow B$ a [[principal bundle|principal $G$-bundle]] over 

* a compact [[orientable]] [[Riemannian manifold]] $(B,g)$, 

and write

*  $Ad_P \,\coloneqq\, P \times_G \mathfrak{g}$ for its [[adjoint bundle]],

* $\Gamma(Ad_P)$ for the [[space of smooth sections]],

* $\Omega^1_{conn}(P;\mathfrak{g}) \subset \Omega^1(P;\mathfrak{g})$ for the [[Lie algebra valued differential 1-forms]] which are ([[Ehresmann connection|Ehresmann]]) [[connection on a principal bundle|connection forms]]

  (and [[invariant polynomial|recall]] that the [[gauge invariance|gauge-invariants]] of the [[curvature 2-form]] $F_A$ of $A \in \Omega^1_{conn}(P;\mathfrak{g})$ descend to, hence are [[pullback of differential forms|pulled back from]], plain [[differential forms]] on $B$).

The _Yang-Mills-Higgs [[action functional]]_ (or _YMH action functional_) is given by:

$$
  \begin{array}{ccc}
  \mathllap{
    S_{YMH}
    \,\colon\,
  }
  \Omega^1_{conn}(P;\mathfrak{g})
  \times
  \Gamma(Ad_P)
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
$$

(cf. [Taubes 1982a, Equation (2.1)](#Taubes82a))

## Yang-Mills-Higgs equations and pairs

A connection $A\in\Omega^1(B,\operatorname{Ad}(E))$ and a section $\Phi\in\Gamma^\infty(B,\operatorname{Ad}(E))$ are called _Yang-Mills-Higgs pair_ (or _YMH pair_) if they are a critical point of the Yang-Mills-Higgs action functional, hence if:

$$
  \frac{\mathrm{d}}{\mathrm{d}t}
  S_{YMH}(\alpha(t),\varphi(t))\vert_{t=0}
  \;=\;
  0
$$

for all smooth families $\alpha\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(B,\operatorname{Ad}(E))$ with $\alpha(0)=A$ and $\varphi\colon(-\varepsilon,\varepsilon)\rightarrow\Gamma^\infty(B,\operatorname{Ad}(E))$ with $\varphi(0)=\Phi$.

This is the case iff the _Yang-Mills-Higgs equations_ (or _YMH equations_) are fulfilled:

$$
\mathrm{d}_A\star F_A
+\star[\Phi,\mathrm{d}_A\Phi]
=0;
$$
$$
\mathrm{d}_A\star\mathrm{d}_A\Phi
=0.
$$

([Taubes 82a, Equations (2.2a) and (2.2b)](#Taubes82a), [Taubes 84, Equation (1)](#Taubes84), [Taubes 85, Equations (A.1.1a) and (A.1.1b)](#Taubes85))

([Taubes 84, Equation (1)](#Taubes84) is missing the second [[Hodge star operator]] in the first [[Yang-Mills-Higgs equation]].)

Furthermore the following [[Bianchi identities]] hold:

$$
\mathrm{d}_A F_A
=0;
$$
$$
\mathrm{d}_A\mathrm{d}_A\Phi
+[\Phi,F_A]
=0.
$$

([Taubes 82a, Equations (2.2c) and (2.2d)](#Taubes82a))

Furthermore the Higgs field is required to vanish at infinity:

$$
\lim_{|x|\rightarrow\infty}|\Phi|(x)
=0.
$$

([Taubes 82a, Equation (2.3)](#Taubes82a))

A solution $(A,\Phi)$ of the [[Yang-Mills-Higgs equations]] is called _Yang-Mills-Higgs pair_.

Using $\star^2=(-1)^{k(n-k)}$ and $\delta_A=(-1)^{n(k+1)+1}\star\mathrm{d}_A\star$ when applied to $k$-forms, the first [[Yang-Mills-Higgs equation]] can also be rewritten as:

$$
\delta_A F_A
+[\Phi,\mathrm{d}_A\Phi]
=0.
$$

The second [[Yang-Mills-Higgs equation]] can also be rewritten as:

$$
\delta_A\mathrm{d}_A\Phi
=0.
$$

## Properties

\begin{lem}
$A\in\Omega^1(B,\operatorname{Ad}(E))$ is a Yang-Mills connection iff $(A,0)\in\Omega^1(B,\operatorname{Ad}(E))\times\Gamma^\infty(B,\operatorname{Ad}(E))$ is a Yang-Mills-Higgs pair.
\end{lem}

## Abelian Yang-Mills-Higgs equation

For an abelian [[Lie group]] as [[structure group]], its [[Lie algebra]] is also abelian and hence all [[Lie brackets]] vanish and makes the [[Yang-Mills-Higgs equations]] into:

$$
\mathrm{d}\star\mathrm{d}A
=0;
$$
$$
\mathrm{d}\star\mathrm{d}\Phi
=0.
$$

## Connection with generalized Laplace equation

Let:

$$
\Delta_A
\coloneqq\delta_A\mathrm{d}_A
+\mathrm{d}_A\delta_A\colon
\Omega^k(B,\operatorname{Ad}(E))\rightarrow\Omega^k(B,\operatorname{Ad}(E))
$$

be a [[generalized Laplace operator]].

The [[Bianchi identity]] $\mathrm{d}_A F_A=0$ and the first [[Yang-Mills-Higgs equation]] $\delta_A F_A=-[\Phi,\mathrm{d}_A\Phi]$ combine to:

$$
\Delta_A F_A
=-\mathrm{d}_A[\Phi,\mathrm{d}_A\Phi].
$$

The trivial identity $\delta_A\Phi=0$ (since $\Phi$ is a $0$-form whose degree cannot be lowered any further) and the second [[Yang-Mills-Higgs equation]] $\delta_A\mathrm{d}_A\Phi=0$ combine to:

$$
\Delta_A\Phi
=0.
$$

## Related entries

* [[stable Yang-Mills-Higgs pair]]

* [[Einstein-Yang-Mills-Dirac-Higgs theory]]

## References

* {#Taubes82a} [[Clifford Taubes]], _The existence of a non-minimal solution to the $\operatorname{SU}(2)$ Yang-Mills-Higgs equations on $\mathbb{R}^3$ Part I_, Communications in Mathematical Physics **86** (1982) 257–298 &lbrack;[doi:10.1007/BF01206014](https://doi.org/10.1007/BF01206014)&rbrack;

* {#Taubes82b} [[Clifford Taubes]], _The existence of a non-minimal solution to the $\operatorname{SU}(2)$ Yang-Mills-Higgs equations on $\mathbb{R}^3$ Part II_, Communications in Mathematical Physics **86** (1982) 299–320 &lbrack;[doi:10.1007/BF01212170](https://doi.org/10.1007/BF01212170)&rbrack;

* {#Taubes84} [[Clifford Taubes]], _On the Yang--Mills--Higgs equations_, Bulletin of the American Mathematical Society **10** (1984) 295–297 &lbrack;[doi:10.1090/s0273-0979-1984-15254-6](https://doi.org/10.1090/s0273-0979-1984-15254-6)&rbrack;

* {#Taubes85} [[Clifford Taubes]], _Min-max theory for the Yang-Mills-Higgs equations_, Communications in Mathematical Physics **97** (1985) 295–297 &lbrack;[doi:10.1007/BF01221215](https://doi.org/10.1007/BF01221215)&rbrack;

See also:

* Wikipedia, [Yang-Mills-Higgs equations](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills%E2%80%93Higgs_equations)

[[!redirects Yang-Mills-Higgs equation]]
[[!redirects Yang-Mills-Higgs pair]]
[[!redirects Yang-Mills-Higgs pairs]]
[[!redirects YMH equation]]
[[!redirects YMH equations]]
[[!redirects YMH pair]]
[[!redirects YMH pairs]]
