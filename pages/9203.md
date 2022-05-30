
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[local Lagrangian]] of [[Chern-Simons theory]] gives rise to an [[action functional]] which is [[gauge invariance|gauge invariant]] only for certain discrete choices of the scale (a global prefactor) of the Lagrangian. This is called the **level** of the [[theory (physics)|theory]]. The fact that it takes values in a [[discrete group|discrete]] [[subgroup]] of the [[real numbers]] is called **level quantization** of the [[theory (physics)|theory]].

## Properties

### As a characteristic class

Formally, for [[gauge group]] being some [[compact Lie group]] $G$, the level is identified with a choice of [[universal characteristic class]], hence an element

$$
  [c] \in H^4(B G, \mathbb{Z})
$$

in the [[integral cohomology]] of the [[classifying space]] of $G$. Under the [[Chern-Weil homomorphism]] every such $c$ corresponds to an [[invariant polynomial]] $\langle -,-\rangle_c$ on the [[Lie algebra]]. (The point being here that while every scalar multiple of an invariant polynomial is itself again an invariant polynomial, only a lattice of these does corespond to a class in [[integral cohomology]].)

If $G$ is furthermore connected and simply connected, then the [[local Lagrangian]] of Chern-Simons theory is the [[Chern-Simons form]] $CS_c$ of this specific invariant polynomial $\langle -,-\rangle_c$.

Generally, for $c \;\colon\; B G \to B^3 U(1) \simeq K(\mathbb{Z},4)$ a [[universal characteristic map]] the [[extended Lagrangian]] of  the corresponding [[3d Chern-Simons theory]] is a [[differential characteristic class|differential refinement]] $\hat \mathbf{c}$ of a lift $\mathbf{c}$ through [[geometric realization of cohesive infinity-groupoids|geometric realization]] of [[smooth infinity-groupoids]]

$$
  \array{
    \mathbf{B}G_{conn}
    &\stackrel{\hat \mathbf{c}}{\to}&
    \mathbf{B}^3 U(1)_{conn} 
    \\
    \downarrow && \downarrow &&& \mathbf{H}
    \\
    \mathbf{B}G
    &\stackrel{\mathbf{c}}{\to}&
    \mathbf{B}^3 U(1)
    \\
    && &&& \downarrow^{\mathrlap{{\vert \Pi(-)\vert}}}
    \\
    B G &\stackrel{c}{\to}& B^3 U(1) &&& L_{whe} Top
  }
  \,.
$$

Hence $\hat \mathbf{c}$ is the "differentially refined level" of the theory. Notice that in terms of this the statement that the [[action functional]] is [[gauge invariance|gauge invariant]] for "given level" is the statement that for $\Sigma_3$ a [[closed manifold]] of [[dimension]] 3, the [[transgression]] of the [[extended Lagrangian]] $\hat \mathbf{c}$ to the [[moduli stack]] fo [[field (physics)|fields]] on $\Sigma_3$ is a map of [[smooth ∞-groupoid|smooth stacks]]

$$
  \exp\left(
    2 \pi i
    \int_{\Sigma_3} [\Sigma_3, \hat \mathbf{c}]
  \right)
  \;\colon\;
  [\Sigma_3, \mathbf{B}G_{conn}]
  \to 
  U(1)
  \,.
$$

Analogous reasoning and termionology applies to [[higher dimensional Chern-Simons theory]] and generally to [[∞-Chern-Simons theory]].


### Level renormalization
 {#LevelRenormalization}

Upon [[quantization of 3d Chern-Simons theory|quantization]], the [[level (Chern-Simons theory)|Chern-Simons level]] receives a [[renormalization]] which shifts it by the [[dual Coxeter number]] of the [[gauge group]] (see the references [below](#ReferencesLevelRenormalization)).



## Related concepts

* [[su(2)-anyon]]

* [[quantization of 3d Chern-Simons theory]]

[[!include extended prequantum field theory - table]]



## References

### General

For traditional accounts see at  _[Chern-Simons theory - References](#Chern-Simons+theory)_.

Introductory discussion is in the section _[Physics in Higher Geometry: Motivation and Survey](geometry%20of%20physics#PhysicsMotivationAndSurvey)_ at 

* _[[geometry of physics]]_.


### Level renormalization
 {#ReferencesLevelRenormalization}

On the [[renormalization]] of the Chern-Simons level (shift by the [[dual Coxeter number]]):

* [[Luis Alvarez-Gaumé]], J. M. F. Labastida, A. V. Ramallo, *A note on perturbative Chern-Simons theory*, Nuclear Physics B **334** 1 (1990) 103-124 (<a href="https://doi.org/10.1016/0550-3213(90)90658-Z">doi:10.1016/0550-3213(90)90658-Z</a>)

* [[Mikhail A. Shifman]], *Four-dimension aspect of the perturbative renormalization in three-dimensional Chern-Simons theory*, Nuclear Physics B **352** 1 (1991) 87-112 (<a href="https://doi.org/10.1016/0550-3213(91)90130-P">doi:10.1016/0550-3213(91)90130-P</a>)

* M. Asorey, F. Falceto, J. L. Lopez, G. Luzon, *Universalty and Ultraviolet Regularizations of Chern-Simons Theory*, Nucl.Phys. B **429** (1994) 344-374 ([arXiv:hep-th/9403117](https://arxiv.org/abs/hep-th/9403117), <a href="https://doi.org/10.1016/0550-3213(94)00331-9">doi:10.1016/0550-3213(94)00331-9</a>)

[[!redirects Chern-Simons level]]
