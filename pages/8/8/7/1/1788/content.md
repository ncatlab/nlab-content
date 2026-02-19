> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak



***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


### Idea

A *Heisenberg manifold* is the [[quotient space]] of a real [[Heisenberg group]] by an [[integer Heisenberg group|integer Heisenberg]] [[subgroup]]. 

By default this is understood in the case of the 3-dimensional Heisenberg group (which is the [[central extension|central]] [[group extension]] of the additive group $\mathbb{R}^2$ by the [[group cohomology|group]] [[cocycle]] which is the canonical [[symplectic form]]) and one refers to *the Heisenberg manfifold* for this case, a [[3-manifold]].

## Properties

Beware that Heisenberg manifolds does not inherit [[group]] [[structure]] since the [[integer Heisenberg group]] is not [[normal subgroup|normal]] as a [[subgroup]] of the real Heisenberg group.


\begin{proposition}
  The Heisenberg manifold is a [[nilmanifold]].
\end{proposition}


\begin{proposition}
  The Heisenberg manifold is a [[Seifert manifold]].
\end{proposition}


### References


See also:

* Yoshiaki Suzuki: *Heisenberg Manifolds*, section 2 of: *The Folland-Stein spectrum of some Heisenberg Bieberbach manifolds*, Kyushu Journal of Mathematics (2026) &lbrack;[arXiv:2402.15093](https://arxiv.org/abs/2402.15093)&rbrack;

* J. W. Cannon, W. J. Floyd, W. R. Parry; Ex. 7.4 in: *A Survey of twisted face-pairing 3-manifolds* &lbrack;[pdf](https://personal.math.vt.edu/floyd/research/papers/survey.pdf)&rbrack;

* Richard Tolimieri: *Analysis on the Heisenberg manifold*, Amer. Math. Soc. **228** (1977) 329-343 &lbrack;[doi:10.1090/S0002-9947-1977-0447473-8](https://doi.org/10.1090/S0002-9947-1977-0447473-8), [pdf](https://www.ams.org/journals/tran/1977-228-00/S0002-9947-1977-0447473-8/S0002-9947-1977-0447473-8.pdf)&rbrack;

Discussion in the context of [[sub-Riemannian geometry]]:

* Ovidiu Calin, Der-Chen Chang: *Heisenberg Manifolds*, Chapter 9 in: *Sub-Riemannian Geometry -- General Theory and Examples*, Cambridge University Press (2009) 175--230 &lbrack;[doi:10.1017/CBO9781139195966.010](https://doi.org/10.1017/CBO9781139195966.010)&rbrack;




### FQH Excitation modes



On multiple modes resolving the would-be single GMP mode for [FQH excitations](quantum+Hall+effect#CollectiveExcitations) 

near filling fraction $\nu = 1/4$:

* Dung Xuan Nguyen, [[F. D. M. Haldane]], [[Edward H. Rezayi]], [[Dam Thanh Son]], Kun Yang: *Multiple Magnetorotons and Spectral Sum Rules in Fractional Quantum Hall Systems*, Phys. Rev. Lett. **128** (2022) 246402 \[<a href="https://doi.org/10.1103/PhysRevLett.128.246402">doi:10.1103/PhysRevLett.128.246402</a>, [arXiv:2111.10593](https://arxiv.org/abs/2111.10593), suppl:[pdf](https://journals.aps.org/prl/supplemental/10.1103/PhysRevLett.128.246402/Supp.pdf)\]

at [Jain filling fractions](quantum+Hall+effect#CompositeParticlePicture) $n/(2 p n \pm 1)$ with ${\vert n \vert}\geq 2$ (e.g. $\nu = 2/5, 3/7, 2/9, 2/7$):

* [[Ajit C. Balram]], Zhao Liu, [[Andrey Gromov]], [[Zlatko Papić]]: *Very-High-Energy Collective States of Partons in Fractional Quantum Hall Liquids*, Phys. Rev. X **12** (2022) 021008 \[<a href="https://doi.org/10.1103/PhysRevX.12.021008">doi:10.1103/PhysRevX.12.021008</a>, [arXiv:2111.10395](https://arxiv.org/abs/2111.10395)\]

at filling fractions $\nu  = n/(4 n \pm 1)$:

* [[Ajit C. Balram]], G. J. Sreejith, [[Jainendra K. Jain]]: *Splitting of Girvin-MacDonald-Platzman density wave and the nature of chiral gravitons in fractional quantum Hall effect*, Phys. Rev. Lett. **133** (2024) 246605 \[<a href="https://doi.org/10.1103/PhysRevLett.133.246605">doi:10.1103/PhysRevLett.133.246605</a>, [arXiv:2406.02730](https://arxiv.org/abs/2406.02730)\]

in FQH liquids that are not fully spin-polarized:

* Rakesh K. Dora, [[Ajit C. Balram]]: *Dispersion of collective modes in spinful fractional quantum Hall states on the sphere* \[<a href="https://arxiv.org/abs/2509.13100">arXiv:2509.13100</a>\] 

\linebreak

\begin{example}
In the category of [[schemes]] the subcategory of [[affine schemes]] is dense, see [[affine scheme#AffineSchemesFullSubcategoryOfOppositeOfRings|here]].
\end{example}

\begin{example}
In the category of [[smooth manifolds]], the full subcategory whose objects are given by $\mathbb{R}^n$ for $n\geq 1$ with the standard smooth structure, is dense.
\end{example}

Proof: The restricted Yoneda to the full subcategory spanned by ${\{R\}}$ is faithful, hence so is when restricted to the subcat spanned by $\{R,R^2\}$. To see fullness when restricted to the subcat spanned by $\{R,R^2\}$, suppose we are given a morphism $\operatorname{Hom}(-,M)\Rightarrow\operatorname{Hom}(-,N)$ of presheaves on $\mod_{\{R,R^2\}}$. Given $x\in M$, write $z_x\in N$ for the image of $1\in R$ of the induced map $R\to N$ from $R\to M,1\mapsto x$. Write $[x,y]:R^2\to M$ for the map sending $(1,0)$ and $(0,1)$ to $x$ and $y$, respectively, and write $z_{[x,y]}:R^2\to N$ for the induced map. Then $z_{[x,y]}=[z_x,z_y]$ by compatibility with the $i$-th component map $c_i:R\to R^2$, $i=1,2$. Thus, compatibility with the diagonal map $\Delta:R\to R^2$ gives $z_{x+y}=\Delta^*z_{[x,y]}=\Delta^*[z_x,z_y]=z_x+z_y$. On the other hand, given $r\in R$, compatibility with $r: k\to k$ gives $z_{r x}=rz_x$. Thus $x\mapsto z_x$ defines a map $f:M\to N$ of $R$-modules such that $f^*:\operatorname{Hom}(-,M)\Rightarrow\operatorname{Hom}(-,N)$ is the morphism we began with.


