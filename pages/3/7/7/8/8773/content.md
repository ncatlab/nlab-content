[[!redirects 5d Chern-Simons theory]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


\tableofcontents


## Idea
 {#Idea}

The standard abelian form of [[higher dimensional Chern-Simons theory]] in [[dimension]] 5 is the [[Lagrangian field theory]] with a single abelian ($G = \mathrm{U}(1)$) [[gauge field]] $A$ (locally a [[differential 1-form]] with [[flux density]] $F_A \coloneqq \mathrm{d}A$) and local [[Lagrangian density]] proportional to

\[
  \label{LagrangianDensityFor5dAbelianChernSimons}
  L_{CS}^{5D}(A) \;\propto\; A \wedge F_A \wedge F_A
  \,.
\]

One way this appears is as a "topological mass" term to [[Maxwell theory]] in 5D: 

For [[spacetime]] domain $Y^{1,4}$ a [[Lorentzian manifold]], [[dimension of a manifold|$\mathrm{dim}\big(Y^{1,4}\big) = 5$]], with associated [[Hodge star operator]]
\[
  \label{HodgeStarOnSpacetimeDomain}
  \star_{{}_Y} 
  \;\colon\;
  \Omega^\bullet_{dR}\big(
    Y^{1,4}
  \big)
  \longrightarrow
  \Omega^{5-\bullet}_{dR}\big(
    Y^{1,4}
  \big)
  \,,
\]

the Lagrangian density of *5D [[Maxwell-Chern-Simons theory]]* is proportional to

\[
  \label{LagrangianDensityFor5dMaxwellChernSimons}
  L_{MCS}^{5D}(A)
  \;\propto\;
  \tfrac{1}{2}
  F_A \wedge \star_5 F_A 
   \;-\;
  \tfrac{c}{3}
  A \wedge F_A \wedge F_A
  \,,
\]
for some relative prefactor $c$

This appears notably in the [[bosonic field|bosonic sector]] of minimal [[D=5 supergravity]], which in total is 5D [[Einstein-Maxwell theory|Einstein-Maxwell]]-Chern-Simons theory.

The [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] of 5D Chern-Simons-Maxwell theory (eq:LagrangianDensityFor5dMaxwellChernSimons) are (setting $c=1$, for definiteness):
\[
  \label{EoMof5dMCS}
  \begin{aligned}
    \mathrm{d}\, F_2 & = 0 
    \mathrlap{\,,}
    \\
    \mathrm{d}\, \star_{{}_Y} F_2 
     & =
     \tfrac{1}{2} 
     F_2 \wedge F_2
    \mathrlap{\,.}
  \end{aligned}
\]

These are like [[Maxwell's equations]] where an [[electric current]] is sourced by the gauge field itself.

The structure of the these equations of motion is, up to dimension and form degree, the same as that of the [[supergravity C-field|C-field]] in [[D=11 supergravity]]. The two are closely related under [[double dimensional reduction]] (cf. references [here](D%3D5+supergravity#ReferencesViaMTheoryOnCY3Folds)). 


## Properties




### Dimensional reduction of 5D Maxwell-Chern-Simons to 3D
 {#DimReductionOf5dMaxwellCSTo3D}


Consider the [[dimensional reduction]] of the 5D Maxwell-Chern-Simons equations of motion (eq:EoMof5dMCS) to 3D, specifically: 

Consider the case that the [[spacetime]] $Y^{1,4}$ is a [[product manifold]] (with product [[Riemannian metric|metric]])
\[
  \label{DimRedSpacetime}
  Y^{1,4}
  =
  X^{1,2} \times L^1 \times V^1
  \,,
\]

of:

* a [[Lorentzian manifold]] $X^{1,2}$, $dim\big(X^{1,2}\big) = 3$,

* 1-dimensional [[Riemannian manifolds]] $L^1$ and $V^1$ (not necessarily [[connected topological space|connected]] or [[closed manifold|closed]])

  which in suitable [[coordinates]] $l$ and $v$ have metrics
  $
    \begin{aligned}
      g_L & = \ell_l^2 \mathrm{d}l \otimes \mathrm{d}l
      \\
      g_V & = \ell_v^2 \mathrm{d}v \otimes \mathrm{d}v
    \end{aligned}
  $ 
  for [[positive number|positive]] [[real numbers]] $l,v \in \mathbb{R}_+$, respectively.

and that the [[flux density]] is constant along the fibers, in that

\[
  \label{DimRedDecompositionOfFluxDensity}
  \begin{aligned}
    F_2 
    = & 
    F_2^{(X X)} 
    \\
    & +
    F_1^{(X l)}
    \wedge
    \mathrm{d} l  
    \\
    & + 
    F_1^{(X v)}
    \wedge
    \mathrm{d} v  
    \\
    & +
    F^{(l v)}_0
    \mathrm{d}l
    \wedge
    \mathrm{d}v
  \end{aligned}
  \;\;\;\;\;
  \text{for}
  \;\;\;\;\;
  \left\{
  \begin{aligned}
    F_2^{(X X)}
    & 
    \in
    \Omega^2_{dR}\big(X^{1,2}\big)
    \xhookrightarrow{ p_X^\ast }
    \Omega^2_{dR}\big(Y^{1,4}\big)
    \\
    F_1^{(X l)}, 
    F_1^{(X v)}
    & 
    \in
    \Omega^1_{dR}\big(X^{1,2}\big)
    \xhookrightarrow{ p_X^\ast }
    \Omega^1_{dR}\big(Y^{1,4}\big)
    \\
    F_0^{(l v)}, 
    & 
    \in
    \Omega^0_{dR}\big(X^{1,2}\big)
    \xhookrightarrow{ p_X^\ast }
    \Omega^0_{dR}\big(Y^{1,4}\big)
  \end{aligned}
  \right.
\]
and such that 
\[
  \label{DimRedFluxCompactification}
  \underset{x \in X}{\forall} 
  \;
  F_0^{(l v)}(x) \neq 0
\]
(whence we have a *[[flux compactification]]*).

\begin{proposition}
  In this situation and in the [[limit of a sequence|limit]]
  $\ell_v \to 0$, the equations of motion (eq:EoMof5dMCS) are equivalent to the following system of equations:
\[
  \label{5DMCSEoMdimReducedTo3D}
  \begin{aligned}
    &
    F_2^{(X X)}
    =
    - 
    \tfrac{1}{F_0^{(l v)}}
    F_1^{(X l)} \wedge F_1^{(X v)}
    \\
    &
    \mathrm{d}_X F_1^{(X v)} = 0,
    \;
    \mathrm{d}_X \star_X F_1^{(X v)} = 0,
    \\
    &
    \mathrm{d}_X F_1^{(X l)} = 0
    \mathrlap{\,.}
  \end{aligned}
\]
In particular, when either of the $F_1^{(X -)}$ vanishes, then $F_2^{(X X)}$ satisfies the equations of motion of 3D [[abelian Chern-Simons theory]], in the limit $\ell_v \to 0$.
\end{proposition}
\begin{proof}
This is a standard kind of argument, but seems not to be citable from the literature:

Due to the product spacetime structure (eq:DimRedSpacetime), the Hodge dual of $F_2$ (eq:DimRedDecompositionOfFluxDensity) with respect to $Y^{1,4}$ is expressed in terms of the Hodge star operator $\star_{X}$ associated with $X^{1,2}$ as follows:
$$
  \begin{aligned}
  \star F_2
  =
  &
  \ell_l \ell_v
  \big(
    \star_X F_2^{(X X)} 
  \big)
  \wedge
  \mathrm{d}l
  \wedge
  \mathrm{d}v
  \\
  & +
  \tfrac{\ell_v}{\ell_l}
  \big(
    \star_X F_1^{(X l)}
  \big)
  \wedge
  \mathrm{d} v
  \\
  & -
  \tfrac{\ell_l}{\ell_v}
  \big(
    \star_X F_1^{(X v)}
  \big)
  \wedge
  \mathrm{d} l
  \\
  & + 
  \tfrac{1}{\ell_l \ell_v}
  \star_X F_0^{(l v)}
  \,,
  \end{aligned}
$$
whence the second equation of motion (eq:EoMof5dMCS) is seen to be equivalent to
\[
  \label{SecondEoMInKKComponents}
  \begin{aligned}
    \ell_l \ell_v
    \mathrm{d}_X
    \big(
      \star_X F_2^{(X X)} 
    \big)
    & =
    F_2^{(X X)} \wedge F_0^{(l v)}
    +
    F_1^{(X l)} \wedge F_1^{(X v)}
    \\
    \tfrac{\ell_v}{\ell_l}
    \mathrm{d}_X
    \big(
      \star_X F_1^{(X l)}
    \big)
    & =
    F_2^{(X X)} \wedge F_1^{(X v)}
    \\
    \tfrac{\ell_l}{\ell_v}
    \mathrm{d}_X
    \big(
      \star_X F_1^{(X v)}
    \big)
    & =
    - F_2^{(X X)} \wedge F_1^{(X l)}
    \\
    \tfrac{1}{\ell_l \ell_v}
    \underset{ = 0 }{
      \underbrace{
        \mathrm{d}_X
        \big(
          \star_X F_0^{(l v)}
        \big)
    }}
    & =
    \tfrac{1}{2}
    \underset{ =0 }{
    \underbrace{
      F_2^{(X X)} \wedge F_2^{(X X)}
    }}
    \mathrlap{\,,}
  \end{aligned}
\]
where the terms over the brace vanish by degree reasons.

In the limit $\ell_v \to 0$ the first equation in (eq:SecondEoMInKKComponents) goes to
$$
  \begin{aligned}
    F_2^{(X X)} 
    \;\to\;
    -
    \tfrac{1}{F_0^{(l v)}}
    F_1^{(X l)} \wedge F_1^{(X v)}
  \end{aligned}
$$
and thus implies the vanishing of the right hand sides of the second and third equations in (eq:SecondEoMInKKComponents), whence the only remaining condition expressed by (eq:SecondEoMInKKComponents) is
$$
  \mathrm{d}_X \big( \star_X F_1^{(X v)} \big)
  \;\to\; 
  0
  \,.
$$
Finally, the first equation of motion (eq:EoMof5dMCS) says that the component forms (eq:DimRedDecompositionOfFluxDensity) are closed. The closure of the 0-form component $F_0^{(l v)}$ means that it is locally constant, and the closure of $F_1^{(X -)}$ implies that of their wedge product $F_2^{(X X)}$. This completes the proof of the claim (eq:5DMCSEoMdimReducedTo3D).
\end{proof}



\linebreak

### Moduli of fields (abelian case)

[[!include moduli of higher lines -- table]]

## Related concepts

* [[higher dimensional Chern-Simons theory]]

  * [[D=1 Chern-Simons theory]]

  * [[D=2 Chern-Simons theory]]
  
  * [[D=3 Chern-Simons theory]]

  * [[D=4 Chern-Simons theory]]

  * **D=5 Chern-Simons theory**

    * [[5d supergravity]]

  * [[D=6 Chern-Simons theory]]

  * [[D=7 Chern-Simons theory]]

  * [[D=11 Chern-Simons theory]]

  * [[AKSZ sigma-models]]

  * [[string field theory]]

  * [[infinite-dimensional Chern-Simons theory]]

* [[self-dual Yang-Mills theory]]

* [[D=5 gravity]]

* [[D=5 supergravity]]




## References

In the context of [[D=5 Yang-Mills theory|$D=5$]] [[quantum electrodynamics]] (5d [[Maxwell-Chern-Simons theory]]):

* [[Christopher T. Hill]]: *Anomalies, Chern-Simons Terms and Chiral Delocalization in Extra Dimensions*, Phys. Rev. D **73** (2006) 085001 &lbrack;[arXiv:hep-th/0601154](https://arxiv.org/abs/hep-th/0601154), [doi:10.1103/PhysRevD.73.085001](https://doi.org/10.1103/PhysRevD.73.085001)&rbrack;

* [[Christopher T. Hill]]: _Physics of $D = 5$ Chern-Simons term_ (2006) &lbrack;[pdf](https://particle.physics.ucdavis.edu/seminars/lib/exe/fetch.php?media=2006:oct:hill.pdf), [[Hill-5dCS.pdf:file]]&rbrack;

Canonical [[phase space]] analysis:

* Olivera Miskovic, Ricardo Troncoso, [[Jorge Zanelli]], *Canonical sectors of five-dimensional Chern-Simons theories*, Phys. Lett. B **615** (2005) 277-284 &lbrack;[arXiv:hep-th/0504055](http://arxiv.org/abs/hep-th/0504055), [doi:10.1016/j.physletb.2005.04.043](https://doi.org/10.1016/j.physletb.2005.04.043)&rbrack;


In relation to [[D=5 supergravity]]:

* [[Anna Ceresole]], A. Lerda, [[Peter van Nieuwenhuizen]]: *Five-dimensional gravitational super Chern-Simons terms*, Phys. Rev. D **34** (1986) 1744-1748 &lbrack;[doi:10.1103/PhysRevD.34.1744](https://doi.org/10.1103/PhysRevD.34.1744)&rbrack;

and obtained from [[dimensional reduction]] of [[D=11 supergravity]] ("[[M-theory]]"):

* [[Yuji Tachikawa]]: *Five-dimensional Chern-Simons terms and Nekrasov's instanton counting*, Journal of High Energy Physics, JHEP02 (2004) &lbrack;[arXiv:hep-th/0401184](http://arxiv.org/abs/hep-th/0401184), [doi:10.1088/1126-6708/2004/02/050](https://doi.org/10.1088/1126-6708/2004/02/050)&rbrack;

* [[Federico Bonetti]], [[Thomas Grimm]], [[Stefan Hohenegger]]: *One-loop Chern-Simons terms in five dimensions* &lbrack;[arXiv:1302.2918](http://arxiv.org/abs/1302.2918)&rbrack;


On further [[dimensional reduction]] of $D=5$ Chern-Simons theory:

* M. Temple‐Raston: *The reduction of five dimensional Chern–Simons theories*, J. Math. Phys. **35** (1994) 759–768 &lbrack;[doi:10.1063/1.530665](https://doi.org/10.1063/1.530665), [[TempleRaston-Red5dCS.pdf:file]]&rbrack;

On its [[edge modes]] in higher dimensional generalization of the relation between 3D [[abelian Chern-Simons theory]] and [[fractional quantum Hall systems]]:

* K. S. Gupta, [[Allen B. Stern]]: *4D edge currents from 5D Chern-Simons theory*, Nuclear Physics B **442** 1–2 (1995) 157-178 \[<a href="https://doi.org/10.1016/S0550-3213(95)00075-5">doi:10.1016/S0550-3213(95)00075-5</a>, [arXiv:hep-th/9410216](https://arxiv.org/abs/hep-th/9410216)\]


More on [[supersymmetry|supersymmetric]] 5d CS:

* Sergei M. Kuzenko, Joseph Novak, _On supersymmetric Chern-Simons-type theories in five dimensions_, JHEP 1402 (2014) 096 ([arXiv:1309.6803](http://arxiv.org/abs/1309.6803))

See also:

* Danhua Song, Mengyao Wu, Ke Wu, Jie Yang, *Higher Chern-Simons based on (2-)crossed modules*, JHEP **2023** 207 (2023) &lbrack;[arXiv:2212.04667](https://arxiv.org/abs/2212.04667), <a href="https://link.springer.com/article/10.1007/JHEP07(2023)207">doi:10.1007/JHEP07(2023)207</a>&rbrack;

A 5d [[higher gauge theory|higher gauge]] CS-Theory analogous to [[semi-topological 4d Chern-Simons theory]]:

* [[Alexander Schenkel]], Benoit Vicedo: *5d 2-Chern-Simons theory and 3d integrable field theories*, Commun. Math. Phys. **405** (2024) 293 &lbrack;[arXiv:2405.08083](https://arxiv.org/abs/2405.08083), [doi:10.1007/s00220-024-05170-9](https://doi.org/10.1007/s00220-024-05170-9)&rbrack;



[[!redirects 5-dimensional Chern-Simons theory]]

[[!redirects 5D Chern-Simons theory]]
[[!redirects 5d Chern-Simons theory]]
