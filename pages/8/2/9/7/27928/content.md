
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### QFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



\tableofcontents

## Idea

Under *Maxwell-Chern-Simons theories* one understands [[Lagrangian field theories]] whose [[field (physics)|field]] content is a single [[circle group|$\mathrm{U}(1)$]] [[gauge field]] (locally on [[spacetime]] given by a [[differential 1-form]] $A$ with [[flux density]] $F = \mathrm{d}A$) and whose [[Lagrangian density]] is a [[sum]] of that of (vacuum) [[Maxwell theory]] with that of an [[abelian Chern-Simons theory]].

This means, over a [[spacetime]] of [[dimension of a manifold|dimension]] $D = 3$, that the Lagrangian density is proportional to

$$
  L_{MCS}^{3D}(A)
  \;\propto\;
  \tfrac{1}{2}
  F \wedge \star F
  \;-\;
  \tfrac{c}{2} A \wedge F
  \,.
$$

The corresponding [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] are (where we include the [[Bianchi identity]] in the first line in order to highlight the comparison to [[Maxwell's equations]]):

$$
  \begin{aligned}
    \mathrm{d} F & = 0
    \\
    \mathrm{d} \star F & = c \,F
    \,.
  \end{aligned}
$$

Similarly, there are higher dimensional versions. For instance over a [[spacetime]] of [[dimension of a manifold|dimension]] $D =5$ and using the Lagrangian density of abelian [[D=5 Chern-Simons theory]], one has
 
$$
  L_{MCS}^{5D}(A)
  \;\propto\;
  \tfrac{1}{2}
  F \wedge \star F
  \;-\;
  \tfrac{c}{3} A \wedge F \wedge F
$$

with [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] 

\[
  \label{EoMof5dMCS}
  \begin{aligned}
    \mathrm{d} F & = 0
    \\
    \mathrm{d} \star F & = c \,F \wedge F
    \,.
  \end{aligned}
\]

This appears notably in the [[bosonic field|bosonic]] sector of [[D=5 supergravity]] (which is an [[Einstein-Maxwell theory|Einstein-Maxwell]]-[[D=5 Chern-Simons theory]]).



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
and thus implies the vanishing of the right hand sides of the second and third equations in (eq:SecondEoMInKKComponents), whence (and this conclusion is generally obtained by [[gauge fixing|fixing]] [[temporal gauge]]) the only remaining condition expressed by (eq:SecondEoMInKKComponents) is
$$
  \mathrm{d}_X \big( \star_X F_1^{(X v)} \big)
  \;\to\; 
  0
  \,.
$$
Finally, the first equation of motion (eq:EoMof5dMCS) says that the component forms (eq:DimRedDecompositionOfFluxDensity) are closed. The closure of the 0-form component $F_0^{(l v)}$ means that it is locally constant, and the closure of $F_1^{(X -)}$ implies the closure of their wedge product $F_2^{(X X)}$. This completes the proof of the claim (eq:5DMCSEoMdimReducedTo3D).
\end{proof}





## Related entries

* [[Chern-Simons theory]], [[abelian Chern-Simons theory]]

* [[Einstein-Maxwell theory]]

* [[Einstein-Yang-Mills theory]]


## References

### In 3D 
 {#ReferencesIn3D}

#### Plain

Early discussion of 3D Maxwell-Chern-Simons theory:

> See also early discussions of [[abelian Chern-Simons theory]] as an [[effective field theory]] for [[fractional quantum Hall systems]], [here](abelian+Chern-Simons+theory#ReferencesAbCSForFQHE), many of which start with Maxwell-Chern-Simons theory; but beware of the claim in [Haller & Lim 1992](#HallerLim1992), [1996](#HallerLim1996) that "[[anyon statistics]]" does not actually arise in MCS as often claimed. 

* Jonathan F. Schonfeld: *A mass term for three-dimensional gauge fields*, Nuclear Physics B **185** 1 (1981) 157-171 \[<a href="https://doi.org/10.1016/0550-3213(81)90369-2">doi:10.1016/0550-3213(81)90369-2</a>\]

* [[Stanley Deser]], [[Roman Jackiw]] S. Templeton: *Topologically massive gauge theories* Annals of Physics **140** 2 (1982) 372-411 \[<a href="https://doi.org/10.1016/0003-4916(82)90164-6">doi:10.1016/0003-4916(82)90164-6</a>\]

* [[A. P. Balachandran]], L. Chandar, E. Ercolessi, T. R. Govindarajan, [[Ramamurti Shankar]]: *Maxwell-Chern-Simons electrodynamics on a disk*, International Journal of Modern Physics A **09** 19 (1994) 3417-3441 &lbrack;[doi:10.1142/S0217751X94001357](https://doi.org/10.1142/S0217751X94001357)&rbrack;

In relation to [[area-preserving diffeomorphisms]]:

* Ian I. Kogan: *Area Preserving Diffeomorphisms and  Symmetry in a  Chern-Simons Theory* &lbrack;[arXiv:hep-th/9208028](https://arxiv.org/abs/hep-th/9208028)&rbrack;

On the [[quantization]] of the theory:

* F. P. Devecchi, M. Fleck, H. O Girotti: *Coulomb Gauge Quantization of the Maxwell-Chern-Simons Theory*, Annals of Physics **242** 2 (1995) 275-291 \[<a href="https://doi.org/10.1006/aphy.1995.1081">doi:10.1006/aphy.1995.1081</a>\]
  > (in [[Coulomb gauge]])

* Lorenzo Leal, Oswaldo Zapata: *Maxwell Chern Simons Theory in a Geometric Representation*, Phys. Rev. D **63** (2001) 065010 \[<a href="https://doi.org/10.1103/PhysRevD.63.065010">doi:10.1103/PhysRevD.63.065010</a>, [arXiv:hep-th/0008049](https://arxiv.org/abs/hep-th/0008049)\]


Review:

* [[Gerald V. Dunne]]: section 2.2 in: *Aspects of Chern-Simons Theory*, in: *Topological aspects of low dimensional systems*, Les Houches -- École d'Été de Physique Théorique **69**, Springer (1999) &lbrack;[doi:10.1007/3-540-46637-1_3](https://doi.org/10.1007/3-540-46637-1_3), [arXiv:hep-th/9902115](https://arxiv.org/abs/hep-th/9902115)&rbrack;

* S. I. Kruglov: *Maxwell–Chern–Simons Topologically Massive Gauge Fields in the First-Order Formalism*, Int J Theor Phys **51** (2012) 1–13 &lbrack;[doi:10.1007/s10773-011-0872-1](https://doi.org/10.1007/s10773-011-0872-1), [arXiv:1010.4728](https://arxiv.org/abs/1010.4728)&rbrack;


With [[boundary field theory|boundaries]]:

* A. Blasi, N. Maggiore, N. Magnoli, S. Storace: *Maxwell-Chern-Simons Theory With Boundary*, Class. Quant. Grav. **27** (2010) 165018 &lbrack;[arXiv:1002.3227](https://arxiv.org/abs/1002.3227), [doi:10.1088/0264-9381/27/16/165018](https://doi.org/10.1088/0264-9381/27/16/165018)&rbrack;

In view of [[electric-magnetic duality]] ("[[S-duality]]"):

* Adi Armoni: *S-Dual of Maxwell Chern-Simons Theory*, Phys. Rev. Lett. **130** (2023) 141601 &lbrack;[doi:10.1103/PhysRevLett.130.141601](https://doi.org/10.1103/PhysRevLett.130.141601), [arXiv:2212.00513](https://arxiv.org/abs/2212.00513)&rbrack;

On [[lattice gauge theory]]-simulations:

* Ze-An Xu, Jing-Yuan Chen: *Lattice Chern-Simons-Maxwell Theory and its Chirality*, JHEP 08 (2025) 062 \[<a href="https://doi.org/10.1007/JHEP08(2025)062">doi:10.1007/JHEP08(2025)062</a>, [arXiv:2410.11034](https://arxiv.org/abs/2410.11034)\]



#### With fermions

Discussion of coupling to [[fermion]] [[field (physics)|fields]] hence of *Maxwell-Chern-Simons-Dirac theory* (MCSD) or *topologically massive [[QCD]]*:

* {#HallerLim1992} [[Kurt Haller]], Edwin Lim-Lombridas: *Canonical quantization of $(2+1)$-dimensional QED with a topological mass term*, Phys. Rev. D **46** (1992) 1737 &lbrack;[doi:10.1103/PhysRevD.46.1737](https://doi.org/10.1103/PhysRevD.46.1737)&rbrack;

* {#HallerLim1996} [[Kurt Haller]], Edwin Lim-Lombridas: *Maxwell-Chern-Simons Theory in Covariant and Coulomb Gauges* Annals of Physics **246** 1 (1996) 1-48 \[<a href="https://doi.org/10.1006/aphy.1996.0019">doi:10.1006/aphy.1996.0019</a>\]

* Kei-Ichi Kondo: *First and Second Order Phase Transitions in Maxwell--Chern-Simons Theory Coupled to Fermions*, Int. J. Mod. Phys. A **11** (1996) 777-822 &lbrack;[arXiv:hep-ph/9509345](https://arxiv.org/abs/hep-ph/9509345), [doi:10.1142/S0217751X96000365](https://doi.org/10.1142/S0217751X96000365)&rbrack;

On the [[quantum states]] of (tacitly) 3D MCSD theory as [[sections]] of [[determinant line bundles]] [[linear representation|representing]] [[area-preserving diffeomorphisms]]:

* {#Pickrell2000} [[Doug Pickrell]]: *On the Action of the Group of Diffeomorphisms of a Surface on Sections of the Determinant Line Bundle*, Pacific Journal of Mathematics **193** 1 (2000) 177-199 &lbrack;[doi:10.2140/pjm.2000.193.177](http://dx.doi.org/10.2140/pjm.2000.193.177), [pdf](https://msp.org/pjm/2000/193-1/pjm-v193-n1-p10-s.pdf)&rbrack;


As an [[effective field theory|effective]] description of [[superconductivity]]:

* [[M. Cristina Diamantini]], P. Sodano, [[Carlo A. Trugenberger]]: *Gauge Theories of Josephson Junction Arrays*, Nucl. Phys. B **474** (1996) 641-677 \[<a href="https://doi.org/10.1016/0550-3213(96)00309-4">doi:10.1016/0550-3213(96)00309-4</a>, [arXiv:hep-th/9511168](https://arxiv.org/abs/hep-th/9511168)\]

* Adam Fredriksson: *$2+1$ Dimensional Chern-
Simons Theory for Landau-Ginzburg Theory*, thesis, Uppsala (2023) &lbrack;[pdf](https://www.diva-portal.org/smash/get/diva2:1765576/FULLTEXT01.pdf)&rbrack;




### In 5d

In the context of minimal [[D=5 supergravity]]:

* {#ChamseddineNicolai80} [[Ali Chamseddine]], [[Hermann Nicolai]]: *Coupling the $SO(2)$ Supergravity Through Dimensional Reduction*, Physics Letters B **96** 1–2 (1980) 89-93 \[<a href="https://doi.org/10.1016/0370-2693(80)90218-X">doi:10.1016/0370-2693(80)90218-X</a>, [[ChamseddineNicolai-SU2SuGra.pdf:file]]\]

  see equation (0.1) in: Corrigendum: Phys. Lett. B **785** (2018) 631-632 &lbrack;[arXiv:1808.08955](https://arxiv.org/abs/1808.08955), [doi:10.1016/j.physletb.2018.05.029](https://doi.org/10.1016/j.physletb.2018.05.029)&rbrack;


In the context of [[quantum electrodynamics]] in 5d:

* [[Christopher T. Hill]]: *Anomalies, Chern-Simons Terms and Chiral Delocalization in Extra Dimensions*, Phys. Rev. D **73** (2006) 085001 &lbrack;[arXiv:hep-th/0601154](https://arxiv.org/abs/hep-th/0601154), [doi:10.1103/PhysRevD.73.085001](https://doi.org/10.1103/PhysRevD.73.085001)&rbrack;

* [[Christopher T. Hill]]: _Physics of $D = 5$ Chern-Simons term_ (2006) &lbrack;[pdf](https://particle.physics.ucdavis.edu/seminars/lib/exe/fetch.php?media=2006:oct:hill.pdf), [[Hill-5dCS.pdf:file]]&rbrack;

With [[QFT with defects|defects]]:

* Jeremias Aguilera Damia, Riccardo Argurio, Eduardo Garcia-Valdecasas: *Non-Invertible Defects in 5d, Boundaries and Holography*, SciPost Phys. **14** 067 (2023) &lbrack;[arXiv:2207.02831](https://arxiv.org/abs/2207.02831), [doi:10.21468/SciPostPhys.14.4.067](https://doi.org/10.21468/SciPostPhys.14.4.067)&rbrack;





[[!redirects Maxwell-Chern-Simons theories]]


[[!redirects 3D Maxwell-Chern-Simons theory]]
[[!redirects 3D Maxwell-Chern-Simons theories]]

[[!redirects D=3 Maxwell-Chern-Simons theory]]
[[!redirects D=3 Maxwell-Chern-Simons theories]]


[[!redirects 5D Maxwell-Chern-Simons theory]]
[[!redirects 5D Maxwell-Chern-Simons theories]]

[[!redirects D=5 Maxwell-Chern-Simons theory]]
[[!redirects D=5 Maxwell-Chern-Simons theories]]

[[!redirects Maxwell-Chern-Simons field]]
[[!redirects Maxwell-Chern-Simons fields]]



