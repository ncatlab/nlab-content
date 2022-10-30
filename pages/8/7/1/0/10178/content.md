
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

This page describes a proposal for a formalization of the concept of [[quantization]] (from  [[local prequantum field theory]] to [[local quantum field theory]]) formulated in terms of [[cohomology]] in [[higher differential geometry]], specifically in [[cohesive (∞,1)-toposes]].

The basic observation is that is natural to 

1. (**prequantum fields**) -- identify spaces of [[trajectories]] of [[field (physics)|fields]] as [[correspondences]] of higher [[moduli stacks]], hence objects of a [[base (∞,1)-topos]];

1. (**local action functionals**) -- identify [[local action functionals]] as lifts of these [[correspondences]] to the [[slice (∞,1)-topos|slice]] of the base $\infty$-topos over an [[∞-group of units]] of a suitably [[E-∞ ring]] object $E$;

1. (**path integral**) -- identify the [[path integral]] [[quantization]] of these local action functionals on spaces of trajectories as the [[path integral as a pull-push transform|pull-push]] operation in [[twisted cohomology|twisted]] $E$-[[cohomology theory]].

Here a [[correspondence]] 

$$
  \array{
    && \mathbf{Trajectories}
    \\
    & {}^{\mathllap{i_1}}\swarrow && \searrow^{\mathrlap{i_2}}
    \\
    \mathbf{Fields}_{in}
    && \swArrow_{\xi} &&
    \mathbf{Fields}_{out}
    \;\;\;\;\;\;\;\;\;\;
    \in \mathbf{H}_{/\mathbf{B}GL_1(E)}
    \\
    & {}_{\chi_{in}}\searrow && \swarrow_{\chi_{out}}
    \\
    && \mathbf{B} GL_1(E)
  }
$$

in the [[slice (∞,1)-topos]] is equivalently a [[correspondence]] of [[spaces]] equipped with a [[cocycle]] $\xi \in H^{\bullet + i_{in}^\ast \chi_{in} + i_{out}^\ast \chi_{out}}(\mathbf{Fields}_{in}, \mathbf{Fields}_{out}; E)$ in [[bivariant cohomology]] $(i_{in}^\ast \chi_{in}, i^\ast_{out} \chi_{out})$-[[twisted cohomology|twisted]] $E$-[[cohomology]] on its correspondence space, and the quantization step takes this to the [[equivalence class]] of maps of $E$-[[∞-modules]] that it induces under [[fiber integration in generalized cohomology]]:

$$
  \Gamma(\chi_{in})
  \stackrel{\;\;\;\;\; \underset{i_2}{\int} i_1^\ast \xi \;\;\;\;\;}{\to}
  \Gamma(\chi_{out})
  \;\;\;\;\;\;\;\;\;
  \in E \mathbf{Mod}
  \,.
$$

Since this process is analogous to how [[Chow motives]] induce cocycles in [[motivic cohomology]] (an observation which for $E = $ [[K-theory spectrum|KU]] was amplified in ([Connes-Skandalis 84](#ConnesSkandalis84), [Connes-Consani-Marcolli 05](#ConnesConsaniMarcolli05))) it may be useful to refer to this process as _[[motive|motivic]] quantization_. Just as the idea of a category of [[motives]] is to constitute a "linearization" or "abelianization" of a category of [[spaces]], so [[quantization]] is a process that sends (non-linear) spaces of field configurations to linear [[spaces of quantum states]]. This linearization by which [[quantum states]] may be added as elements of an [[abelian group]] encodes the [[superposition principle]] and hence [[quantum interference]], the hallmark of [[quantum physics]].

In the following we first lay out the basic definitions of motivic quantization in 

* _[General theory](#GeneralTheory)_

and then we discuss a list of examples in 

* _[Examples](#Examples)_

## General theory
 {#GeneralTheory}

### Basic notions

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]]. Write $(\Pi \dashv \flat \dashv \sharp)$ for the corresponding [[shape modality]], [[flat modality]], [[sharp modality]], respectively.

Write

* $Grp(\mathbf{H}) \coloneqq E_1 Alg^{grp}(\mathbf{H})$ for the [[(∞,1)-category]] of [[∞-group]] objects in $\mathbf{H}$;

* $AbGrp(\mathbb{H}) \coloneqq E_\infty Alg^{grp}(\mathbf{H}) for its [[full sub-(∞,1)-category]] of [[abelian ∞-groups]];

* $Sp(\mathbf{H})$ for the [[stable (∞,1)-category]] of [[spectrum objects]] in $\mathbf{H}$;

* $CRing(\mathbf{H}) \coloneqq E_\infty Alg(Sp(\mathbf{H}))$ for the [[(∞,1)-category]] of [[E-∞ ring]] objects in $\mathbf{H}$;

* $E Mod(\mathbf{H})$ for the [[symmetric monoidal (∞,1)-category]] of $E$-[[∞-modules]] in $\mathbf{H}$.

For $\mathbb{G} \in Grp(\mathbf{G}) \stackrel{forget}{\to} \mathbf{H}$ write $\mathbf{H}_{/\mathbb{G}}$ for the [[slice (∞,1)-topos]] of $\mathbf{H}$ over $\mathbb{G}$. This carries apart from its canonical structure of a [[cartesian monoidal (∞,1)-category]] $(\mathbf{H}_{/\mathbb{G}}, \times_{\mathbb{G}})$ also a second structure of a [[symmetric monoidal (∞,1)-category]] $(\mathbf{H}_{/\mathbb{G}}, \otimes_{\mathbb{G}})$, obtained using the monoid structure on $\mathbb{G}$: 

$$
  \left[
    \array{
      X_1
      \\
      \downarrow^{\mathrlap{\chi_1}}
      \\
      \mathbb{G}
   }
  \right]
  \otimes_{\mathbb{G}}
  \left[
    \array{
      X_2
      \\
      \downarrow^{\mathrlap{\chi_2}}
      \\
      \mathbb{G}
   }
  \right]
  \;\;
  \coloneqq
  \;\;
  \left[
    \array{
      X_1 \times X_2
      \\
      \downarrow^{\mathrlap{(\chi_1, \chi_2)}}
      \\
      \mathbb{G} \times \mathbb{G}
      \\
      \downarrow^{\mathrlap{\cdot}}
      \\
      \mathbb{G}
    }
  \right]
  \,.
$$

For $\mathcal{C}$ any [[(∞,1)-category]] with [[(∞,1)-pullbacks]] write $Corr(\mathcal{C})$ for the [[(∞,1)-category of correspondences]] in $\mathcal{C}$, whose [[objects]] are those of $\mathcal{C}$, whose [[morphisms]] are [[diagrams]] in $\mathcal{C}$ of the form

$$
  X_1 \leftarrow Q \rightarrow X_2
$$

and [[composition]] is given by [[(∞,1)-fiber product]] of such diagrams.

If $\mathcal{C}$ is equipped with the stucture of a [[monoidal (∞,1)-category]] $(\mathcal{C}, \otimes)$, then $Corr(\mathcal{C})$ naturally inheretic a monoidal structure, too, given by the objectwise [[tensor product]] in $\mathcal{C}$. 

Notice that even if $(\mathcal{C}, \times)$ is a [[cartesian monoidal (∞,1)-category]] then the induces monoidal structure $(Corr(\mathcal{C}), \otimes)$ is _not_ cartesian. Notice also that if $(\mathcal{C}, \otimes)$ is [[symmetric monoidal (∞,1)-category|symmetric monoidal]], then so is the induces structure on $Corr(\mathcal{C})$.

In the following we consider $Corr(\mathbf{H}_{/\mathbb{G}})$ always equipped with the [[monoidal (∞,1)-category]] structure which is induced by the non-cartesian tensor monoidal structure $\otimes_{\mathbb{G}}$ on $\mathbf{H}_{/\mathbb{G}}$.

For $\mathcal{C}$ any [[(∞,1)-category]], write $\mathcal{C}^{\Box^n}$ for the [[(∞,1)-category]] of $n$-dimensional [[cube]] [[diagrams]] in $\mathcal{C}$. Under [[pasting]] of diagrams this is naturally an [[(∞,n)-category]]. 

We write for short

$$
  Corr_n\left(\mathbf{H}_{\mathbb{G}}\right)
   \;\coloneqq\;
  Corr\left(\mathcal{H}_{/\mathbb{G}}\right)^{\Box^n}
  \,.
$$

This is a [[symmetric monoidal (∞,n)-category]]. 


### Correspondences and local prequantum field theory


There is a pair of  [[adjoint (∞,1)-functors]]

$$
  CRing(\mathbf{H})
   \stackrel{\overset{\mathbb{S}[-]}{\leftarrow}}{\underset{\mathbf{GL}_1}{\to}}
  AbGrp(\mathbf{H})
$$

where $\mathbf{GL}_1(-)$ forms the [[∞-group of units]] (see there) of an [[E-∞ ring]] object. 

Choose now once and for all 

* $n \in \mathbb{N}$

* $E \in CRing(\mathbf{H})$. 

Write $Bord_n$ for the [[(∞,n)-category of cobordisms|(∞,n)-category of framed cobordisms]].

We say



* a [[field (physics)|physical field]] of a [[local prequantum field theory]] of [[dimension]] $n$ is a [[monoidal (∞,n)-functor]]

  $$
    \mathbf{Fields} \;\colon \; Bord_n^\otimes \to Corr_n\left(\mathbf{H}\right)^\otimes
  $$

* a [[local prequantum field theory]] of [[dimension]] $n$ with field content $\mathbf{Fields}$ and with _[[phase and phase space in physics|phases]]_ in $\mathbf{GL}_1(E)$ is a lift $\exp(i S)$ in the [[diagram]]

  $$
    \array{
      && Corr_n\left(\mathbf{H}_{/\mathbf{B}\mathbf{GL}_1\left(E\right)}\right)^\otimes
      \\
      & {}^{\exp(i S)}\nearrow \;\;\;\;\; & \downarrow
      \\
      Bord_n^\otimes &\stackrel{\mathbf{Fields}}{\to}& Corr_n\left(\mathbf{H}\right)^\otimes
    }
    \,.
  $$


## Examples
 {#Examples}

(...)

### The Poisson manifold at the boundary of the non-perturvative Poisson $\sigma$-model (2d Chern-Simons theory)

(...)

### The charged particle at the boundary of the open superstring

(...)

### The heterotic string at the boundary of the M2-brane

(...)




## References

Aspects of motivic quantization are discussed in 

* [[Joost Nuiten]], Master thesis 2013

The point of view that pull-push along [[correspondences]] equipped with [[operator K-theory]] [[cycles]] in [[KK-theory]] is an [[K-theory]]-analog of [[motives]] was amplified in 

* [[Alain Connes]], [[Georges Skandalis]], _The longitudinal index theorem for foliations_. Publ. Res. Inst. Math. Sci. 20,
no. 6, 1139&#8211;1183 (1984) ([pdf](http://www.alainconnes.org/docs/longitudinal.pdf))
 {#ConnesSkandalis84}


* [[Alain Connes]], Caterina Consani, [[Matilde Marcolli]], _Noncommutative geometry and motives: the thermodynamics of endomotives_ ([arXiv:math/0512138](http://arxiv.org/abs/math/0512138))
 {#ConnesConsaniMarcolli05}

