

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]] via the method of [[effective quantum field theories]] what is called _Wilsonian RG_ (remark \ref{GroupoidOfEFTs} below) and specifically _Polchinski's flow equation_ (prop. \ref{FlowEquationPolchinski} below) is a characterization of the ([[infinitesimal]]) dependence of [[relative effective actions]] $S_{eff,\Lambda}$ ("effective potentials") on the choice of [[UV cutoff]]-scale $\Lambda$. 

Solving Polchinki's flow equation with a choice of initial conditions may be used to choose a [[renormalization|("re"-)normalization]] of an [[interacting field theory|interacting]] [[perturbative QFT]].

This is related to, but conceptually different from, the _[[renormalization group flow]] via [[beta functions]]_ in the sense of [[Gell-Mann-Low renormalization cocycles]].

## Statement

+-- {: .num_remark #GroupoidOfEFTs}
###### Remark
**(Wilsonian [[groupoid]] of [[effective quantum field theories]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum ([this def.](effective+quantum+field+theory#CutoffsUVForPerturbativeQFT)).

Then the [[relative effective actions]] $\mathcal{S}_{eff,\Lambda, \Lambda_0}$ ([this def.](efffective+QFT#EffectiveActionRelative)) satisfy

$$
  S_{eff, \Lambda', \Lambda_0}
  \;=\;
  \left(
    \mathcal{S}_{\Lambda'}^{-1}
    \circ
    \mathcal{S}_\Lambda
  \right)
  \left(
    S_{eff, \Lambda, \Lambda_0}
  \right)
  \phantom{AAA}
  \text{for}
  \,
  \Lambda,\Lambda' \in [0,\infty)
  \,,\,
  \Lambda_0 \in [0,\infty) \sqcup \{\infty\}
  \,.
$$


This is similar to a [[group]] of UV-cutoff scale-transformations. But since the [[composition]] operations are only sensible when the UV-cutoff labels match, as shown, it is really a [[groupoid]] [[groupoid action|action]].

This is often called the _Wilsonian RG_, following ([Wilson 71](#Wilson71)).

=--

We now consider the [[infinitesimal]] version of this "flow":

+-- {: .num_prop #FlowEquationPolchinski}
###### Proposition
**([[Polchinski's flow equation]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)), let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum  (def. \ref{CutoffsUVForPerturbativeQFT}), such that $\Lambda \mapsto \Delta_{F,\Lambda}$ is [[differentiable function|differentiable]].

Then for _every_ choice of [[UV regularization]] $\mathcal{S}_\infty$ ([this prop.](effective+QFT#UVRegularization)) the
corresponding [[relative effective actions]] $S_{eff,\Lambda}$ ([this def.](effective+QFT#EffectiveActionRelative)) satisfy the following [[differential equation]]:

$$
  \frac{d}{d \Lambda}
  S_{eff,\Lambda}
  \;=\;
  -
  \frac{1}{2} \frac{1}{i \hbar}
  \frac{d}{d \Lambda'}
  \left(
    S_{eff,\Lambda}
      \star_{F,\Lambda'}
    S_{eff,\Lambda}
  \right)\vert_{\Lambda' = \Lambda}
  \,,
$$

where on the right we have the [[star product]] induced by $\Delta_{F,\Lambda'}$ ([this def.](star+product#PropagatorStarProduct)).

=--

This goes back to ([Polchinski 84, (27)](#Polchinski84)). The rigorous formulation and proof is due to ([Brunetti-Dütsch-Fredenhagen 09, prop. 5.2](#BrunettiDuetschFredenhagen09), [Dütsch 10, theorem 2](#Duetsch10)).

+-- {: .proof}
###### Proof

First observe that for any [[polynomial observable]] $O \in PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]$ we have

$$
  \begin{aligned}
  &
  \frac{1}{(k+2)!}
  \frac{d}{d \Lambda}
  (
    \underset{
      k+2 \, \text{factors}
    }{
    \underbrace{
      O
        \star_{F,\Lambda}
        \cdots
        \star_{F,\Lambda}
      O
    }
    }
  )
  \\
  & =
  \frac{1}{(k+2)!}
  \frac{d}{d \Lambda}
  \left(
    prod
    \circ
    \exp\left(
      \hbar
      \underset{1 \leq i \lt j \leq k}{\sum}
      \left\langle
         \Delta_{F,\Lambda}
         ,
         \frac{\delta}{\delta \mathbf{\Phi}_i}
         \frac{\delta}{\delta \mathbf{\Phi}_j}
      \right\rangle
    \right)
    (
      \underset{
        k + 2 \, \text{factors}
      }{
      \underbrace{
        O \otimes \cdots \otimes O
      }
      }
    )
  \right)
  \\
  & =
  \underset{
    = \frac{1}{2} \frac{1}{k!}
  }{
  \underbrace{
    \frac{1}{(k+2)!}
    \left(
      k + 2
      \atop
      2
    \right)
  }}
  \left(
    \frac{d}{d \Lambda}
    O
     \star_{F,\Lambda}
    O
  \right)
    \star_{F,\Lambda}
  \underset{
    k \, \text{factors}
  }{
  \underbrace{
  O
    \star_{F,\Lambda}
    \cdots
    \star_{F,\Lambda}
  O
  }
  }
  \end{aligned}
$$

Here $\frac{\delta}{\delta \mathbf{\Phi}_i}$ denotes the functional derivative of the $i$th tensor factor of $O$, and the binomial coefficient counts the number of ways that an unordered pair of distinct labels of tensor factors may be chosen from a total of $k+2$ tensor factors, where we use that the [[star product]] $\star_{F,\Lambda}$ is commutative (by symmetry of $\Delta_{F,\Lambda}$) and associative (by [this prop.](star+product#AssociativeAndUnitalStarProduct)).

With this and the defining equality $\mathcal{S}_\Lambda(S_{eff,\Lambda}) =  \mathcal{S}(g S_{int} + j A)$ ([this equation](effective+QFT#eq:RelativeEffectiveActionRelativeToInfinity)) we compute as follows:

$$
  \begin{aligned}
    0
    & =
    \frac{d}{d \Lambda} \mathcal{S}(g S_{int} + j A)
    \\
    & =
    \frac{d}{d \Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    \\
    & =
    \left(
      \frac{1}{i \hbar}
      \frac{d}{d \Lambda} S_{eff,\Lambda}
    \right)
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    +
    \left(
      \frac{d}{d \Lambda}
      \mathcal{S}_{\Lambda}
   \right)
   \left( S_{eff, \Lambda} \right)
    \\
    & =
    \left(
      \frac{1}{i \hbar}
      \frac{d}{d \Lambda} S_{eff,\Lambda}
    \right)
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    \;+\;
    \frac{1}{2}
    \frac{d}{d \Lambda'}
    \left(
      \frac{1}{i \hbar} S_{eff,\Lambda}
        \star_{F,\Lambda'}
      \frac{1}{i \hbar} S_{eff, \Lambda}
    \right)
    \vert_{\Lambda' = \Lambda}
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda
    \left(
      S_{eff, \Lambda}
    \right)
  \end{aligned}
$$

Acting on this equation with the multiplicative inverse $(-) \star_{F,\Lambda} \mathcal{S}_\Lambda( - S_{eff,\Lambda} )$ (using that $\star_{F,\Lambda}$ is a commutative product, so that exponentials behave as usual) this yields the claimed equation.

=--

## Related concepts

* [[renormalization group flow]]

* [[gauge coupling unification]]

## References

The idea of [[effective quantum field theory]] was promoted in

* {#Wilson71} [[Kenneth Wilson]], _Renormalization group and critical phenomena_ , I., Physical review B 4(9) (1971).

The flow equation in its original form is due to

* {#Polchinski84} [[Joseph Polchinski]], equation (27) in _Renormalization and effective Lagrangians_ , Nuclear Phys. B B231, 1984 ([pdf](http://max2.physics.sunysb.edu/~rastelli/2016/Polchinski.pdf))

The rigorous formulation and proof in [[causal perturbation theory]]/[[perturbative AQFT]] is due to

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], prop. 5.2 of _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

* {#Duetsch10} [[Michael Dütsch]], theorem 2 in _Connection between the renormalization groups of Stückelberg-Petermann and Wilson_, Confluentes Mathematici, Vol. 4, No. 1 (2012) 12400014 ([arXiv:1012.5604](https://arxiv.org/abs/1012.5604))

reviewed in

* {#Duetsch18} [[Michael Dütsch]], section 3.8 of _[[From classical field theory to perturbative quantum field theory]]_, 2018





[[!redirects Wilsonian RG]]
[[!redirects Wilsonian RGs]]

[[!redirects Wilsonian RG flow]]
[[!redirects Wilsonian RG flows]]


[[!redirects Polchinski's flow equation]]
[[!redirects Polchinski's flow equations]]

[[!redirects Polchinski flow equation]]
[[!redirects Polchinski flow equations]]
