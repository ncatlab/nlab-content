
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Perry-Schwarz Lagrangian_ is [[Lagrangian density]]/[[action functional]] for the [[self-dual higher gauge field]] in 6d and/or the [[M5-brane]] [[Green-Schwarz sigma model]], after [[KK-compactification]] to 5 [[worldvolume]] [[dimensions]].

The construction is closely related to the following basic fact relating [[self-dual higher gauge theory|self-dual]] [[differential 3-forms]] on 6d [[Minkowski spacetime]] and [[D=5 Maxwell theory]]:

[[!include relation between 5d Maxwell theory and self-dual 3-forms in 6d -- section]]


## Details

### For the free self-dual field and trivial target space metric
 {#ForTheFreeSelfDualField}

We review the definitions from [Perry-Schwarz 96, Section 2 "The Free Theory"](#PerrySchwarz96) (following [Henneaux-Teitelboim 88](#HenneauxTeitelboim88)), for the [[worldvolume]] [[Lagrangian density]] of just the [[free field|free]] [[self-dual higher gauge field]] on a [[principal U(1)-bundle]]-[[worldvolume]] for would-be [[target space]] being [[Minkowski spacetime]]. 

In doing so, we translate to [[coordinate chart|coordinate]]-invariant [[Cartan calculus]]-formalism and generalized to [[KK-compactification]] on possibly non-[[trivial bundle|trivial]] [[principal U(1)-bundle]]:


#### Worldvolume and self-duality

Let 

$$
  (\Sigma^6, g)
$$ 

be a [[pseudo-Riemannian manifold]] of [[dimension]] 6 and
of [[signature of a quadratic form|signature]] $(-,+,+,+,+,+)$, to be called the _[[worldvolume]]_.

In this dimension and with this signature, the [[Hodge star operator]]
squares to $+1$. This allows to consider for a [[differential 3-form]]
$$
  H \;\in\; \Omega^3\big(\Sigma^6\big)
$$

the condition that it be self-dual ([PS 96 (2)](#PerrySchwarz96))

\[
  \label{SelfDualityIn6d}
  H
  \;=\;
  \star
  H
  \,.
\]

We will assume in the following that $H$ is [[exact differential form]], hence that there exists a [[differential 2-form]]

$$
  B \in \Omega^2\big( \Sigma^6 \big)
$$

such that ([PS 96 (4)](#PerrySchwarz96))

$$
  H = d B
  \,.
$$


#### $S^1$-compactification

Consider then on $\Sigma^6$ the structure of an 
$S^1 = U(1)$-[[circle principal bundle|principal bundle]]

\[
  \label{FibrationWorldvolume}
  \,
\]
\begin{xymatrix}
    S^1 \ar[r]
    &
    \Sigma^6
    \ar[d]
    \\
    & \Sigma^5 
\end{xymatrix}

Write

\[
  \label{FiberVectorField}
  v^5 \in \Gamma( T \Sigma^6 )
\]

for the [[vector field]] which reflects the infinitesimal [[circle group]]-[[action]] on (eq:FibrationWorldvolume). We will write

$$
  \mathcal{L}_{v^5}
  \;=\;
  \big[d, \iota_{v^5} \big]
  \;\colon\;
  \Omega^\bullet\big( \Sigma^6 \big)
  \longrightarrow
  \Omega^\bullet\big( \Sigma^6  \big)
$$

for the [[Lie derivative]] of [[differential forms]] along $v^5$, and make use of [[Cartan's magic formula]] expressing it as an [[anti-commutator]], as shown.


Next consider an [[Ehresmann connection]] on the $S^1$-bundle (eq:FibrationWorldvolume), hence a [[differential 1-form]]

$$
  \theta^5
  \;\in\;
  \Omega^1\big( \Sigma^6 \big)
$$

such that 

\[
  \label{EhresmannConditions}
  \iota_{v^5} \theta^5 = 1
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \mathcal{L}_{v^5} \theta^5 = 0
\]

So in particular

$$
  \theta^5 \wedge \iota_{v^5}
  \;:\;
  \Omega^\bullet\big( \Sigma^6\big)
  \longrightarrow
  \Omega^\bullet\big( \Sigma^6\big)
$$

is a [[projection operator]]:

$$
  \theta^5 \wedge \iota_{v^5}
  \circ
  \theta^5 \wedge \iota_{v^5}
  \;=\;
  \theta^5 \wedge \iota_{v^5}
$$

The complementary projection is that onto [[horizontal differential forms]]

$$
  (-)^{\mathrm{hor}}
  :=
  \big(\mathrm{id} - \theta^5 \iota_{v^5})
  \;:\;
  \Omega^\bullet\big( \Sigma^6\big)
  \longrightarrow
  \Omega^\bullet\big( \Sigma^6\big)
$$

We require $v^5$ (eq:FiberVectorField) to be a [[spacelike]] [[isometry]]. This means that

\[
  \label{HodgeStarCommutingWithIsometryContraction}
  \star \circ \iota_{v^5}
  =
  -
  \theta^5 \wedge \circ \star
  \;:\;
  \Omega^3\big( \Sigma^6\big)
  \longrightarrow
  \Omega^4\big( \Sigma^6 \big)
\]



#### Self-duality after $S^1$-compactification

Set ([PS 96 (5)](#PerrySchwarz96))

\[
  \label{DefOfCalF}
  \mathcal{F}
  \;\coloneqq\;
  \iota_{v^5} H
\]

and ([PS 96 (6)](#PerrySchwarz96))

\[
  \label{DefOfTildeH}
  \tilde H
  \;\coloneqq\;
  \iota_{v^5} \star H
\]

With this notation the self-duality condition (eq:SelfDualityIn6d)
is equivalently ([PS 96 (9)](#PerrySchwarz96), see (eq:EquivalentIncarnationsOfSelfDuality) below):

\[
  \label{SelfDualityIntermsOfcalF}
  \mathcal{F}
  \;=\;
  \tilde H
\]

To make this fully explicit, notice that we have the following chain of logical equivalences:

\[
  \label{EquivalentIncarnationsOfSelfDuality}
  \begin{aligned}
    \big(
      H = \star H
    \big)
    & \Leftrightarrow
    \left(
      \array{
         &
         \phantom{\text{and}\;}
         \iota_{v_5} H  = \iota_{v^5} \star H
         \\
         &
         \text{and}\;
         \theta^5 \wedge H = \theta^5 \wedge \star H
      }
    \right)
    \\
    & \Leftrightarrow
    \big(
      \iota_{v^5} H = \iota_{v^5} \star H
    \big)
    \\
    &\Leftrightarrow
    \big(
      \mathcal{F}
      \;=\;
      \widetilde H
    \big)
  \end{aligned}
\]

Here the first step is decomposition of the self-duality equation into components, the second step follows by (eq:HodgeStarCommutingWithIsometryContraction) and the third step invokes the definitions (eq:DefOfCalF) and (eq:DefOfTildeH) and the fourth step the equality (eq:DecompositionOfCalF).


#### The gauge field


Define the [[vector potential]] ([PS 96 above (4)](#PerrySchwarz96))

\[
  \label{AField}
  A
  \;\coloneqq\;
  -
  \iota_{v^5} B
\]

With this we have

$$
  B
  \;=\;
  A \wedge \theta^5 
  +
  B^{\mathrm{hor}}
  \,.
$$

Set also ([PS 96 above (4)](#PerrySchwarz96))

$$
  F
  \;\coloneqq\;
  \big( d A \big)^{\mathrm{hor}}
$$

then ([PS 96 (5)](#PerrySchwarz96))

\[
  \label{DecompositionOfCalF}
  \begin{aligned}
    \mathcal{F}
    &\coloneqq
    \iota_{v^5} H
    \\
    & =
    \iota_{v^5} d B
    \\
    & =
    - d \iota_{v^5} B + [\iota_{v^5}, d] B
    \\
    & =
    d A + \mathcal{L}_5 B
    \\
    & =
    F 
    + \theta^5 \wedge \iota_{v^5} d A  
    + \mathcal{L}_5 B^{\mathrm{hor}}
    +
    \underset{
      = -\theta^5 \wedge \mathcal{L}_{v^5} A
    }{ 
      \underbrace{
        \mathcal{L}_5 \theta^5 \wedge \iota_{v^5} B
      }
    }
    \\
    & 
    = 
    F 
    + 
    \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \end{aligned}
\]

where in the last step under the brace we used (eq:EhresmannConditions) and (eq:AField).

Hence in terms of $F$ and $B^{\mathrm{hor}}$ the self-duality condition 
(eq:SelfDualityIn6d), (eq:SelfDualityIntermsOfcalF)
is equivalently expressed as on the right of the following

\[
  \label{SelfDualityDecomposition}
  \big(
    H = \star H
  \big)
  \;\Leftrightarrow\;
  \big(
    \widetilde H
    \;=\;
    F + \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \big)
\]


#### Weak self-duality and PS-equations of motion

Notice that

$$
  \begin{aligned}
    \theta^5 \wedge d 
      \big( (d A)^{hor} \big)
    & =
    \theta^5 \wedge d 
       \big( d A - \theta^5 \wedge \iota_{v_5} d A\big)
    \\
    & =
    \theta^5 \wedge (d \theta^5) \wedge \iota_{v_5} d A
  \end{aligned}
  \,.
$$

Hence assume now hat the Ehresmann connection is [[flat connection|flat]],
hence $d \theta^5 = 0$.

Then the self-duality condition in the form (eq:SelfDualityDecomposition)

$$
  \widetilde H
  -
  \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \;=\;
  (d A)^{\mathrm{hor}}
$$

implies, after applying $\theta^5 \wedge d$ to both sides, the second-order equation ([PS 96 (16)](#PerrySchwarz96))

\[
  \label{TheEquationOfMotion}
  (H = \star H)
  \;\;\;\Rightarrow\;\;\;
  \theta^5 
  \wedge 
  d
  \big(
    \widetilde H
    -
    \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \big)
  \;=\;
  0
\]

This equation by itself is hence a weakened form of the self-duality condition, a kind of "self-duality up to horizontally closed terms".

The proposal of [Perry-Schwarz 96, Sec. 2](#PerrySchwarz96) is to take this as the relevant [[equation of motion]] for the theory on $S^1$.



#### Lagrangian density

Therefore one is looking now for a [[Lagrangian density]] whose [[Euler-Lagrange equations]] are (eq:TheEquationOfMotion):

The _Perry-Schwarz-Lagrangian_ is ([PS 96 (17)](#PerrySchwarz96))

\[
  \label{CartanCalculusPerrySchwarzLagrangian}
  L
  \;\coloneqq\;
  -
  \tfrac{1}{2}
  \big(
    \tilde H
    -
    \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \big)
  \wedge 
  \star 
  \tilde H
\]


With (eq:HodgeStarCommutingWithIsometryContraction) the Lagrangian  (eq:CartanCalculusPerrySchwarzLagrangian) becomes

\[
  \label{LagrangianUsingIsometry}
  \begin{aligned}
  L
  & =
  -
  \tfrac{1}{2}
  \big(
  \tilde H
  -
  \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \big)
  \wedge
  H
  \wedge \theta^5
  \\ 
  & =
  -
  \tfrac{1}{2}
  \big(
  \iota_{v^5} \star H
  -
  \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \big)
  \wedge
  H
  \wedge \theta^5  
  \end{aligned}
\]

where in the second line we inserted the definition  (eq:DefOfTildeH).


Notice that (eq:LagrangianUsingIsometry) is the quadratic part of the following form-valued [[bilinear form]] on 2-form fields:

$$
  (B, B^\prime)
  \;\mapsto\;
  -
  \tfrac{1}{2}
  \big(
  \iota_{v^5} \star (d B)
  -
  \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \big)
  \wedge
  (d B^\prime)
  \wedge \theta^5  
$$

Moreover, this bilinear form is _symmetric_ up to a total derivative. For the first summand this is manifest from its incarnation in (eq:CartanCalculusPerrySchwarzLagrangian), since the Hodge pairing is symmetric, and for the second term this follows by "local integration by parts".

As a consequence, the [[Euler-Lagrange equations]] of the Perry-Schwarz Lagrangian density (eq:LagrangianUsingIsometry) may be computed from twice the variation of just the second factor

$$
  \begin{aligned}
    \delta L_{\mathrm{sd}}
    & =
    2
    \Big(
      -
      \tfrac{1}{2}
      \big(
        \iota_{v^5} \star H
        -
        \mathcal{L}_{v^5} B^{\mathrm{hor}}
      \big)
      \wedge
      d(\delta B)
      \wedge 
      \theta^5  
    \Big)
    \\
    & =
    \Big(
    d 
    \big(
      \iota_{v^5} \star H
      -
      \mathcal{L}_{v^5} B^{\mathrm{hor}}
    \big)
    \Big)
    \wedge
    (\delta B)
    \wedge \theta^5
    + 
    d(\cdots)
  \end{aligned}
$$

to indeed be (eq:TheEquationOfMotion):

\[
  \label{EquationsOfMotion}
  \theta^5 \wedge 
  d 
  \big(
    \iota_{v^5} \star H
    -
    \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \big)
  \;=\;
  0
  \,.
\]


Notice that if we do use the self-duality condition (eq:SelfDualityIn6d)
on the Perry-Schwarz Lagrangian (eq:LagrangianUsingIsometry) it becomes

\[
  \label{NonCovariantLagrangianInFlatSpacetime}
  L_{\mathrm{sd}}
  \;=\;
  -
  \tfrac{1}{2}
  \big(
  \iota_{v^5} H
  -
  \mathcal{L}_{v^5} B^{\mathrm{hor}}
  \big)
  \wedge
  H
  \wedge \theta^5
  \phantom{AAAAA}
  \text{if} \;\; H = \star H
\]



#### Example: Reduction to 5d Maxwell theory

Consider the special case that 

$$
  \mathcal{L}_{v^5} B = 0
  \,,
$$

which corresponds to keeping only the 0-mode under [[KK-compactification]] along the circle fiber.

Then (eq:DecompositionOfCalF) becomes

$$
  \mathcal{F} = F
$$

and so the self-duality condition (eq:SelfDualityDecomposition) now becomes
 
$$
  \iota_{v^5} \star H \;=\; F
  \,.
$$

which means that 

$$
  H = F \wedge \theta^5 + \star_5 F
$$

> (check relative sign)

Since $d H = d \circ d B = 0$, this implies

$$
  \begin{aligned}
    \big( 
      d H = 0
    \big)
    & \Leftrightarrow
    \Big(
      d
      \big(
        F \wedge \theta^5 
        +
        \star_5 F
      \big)
      = 0
    \Big)
    \\
    & \Leftrightarrow
    \left(
    \left\{
      \array{
        d_5 F & = 0
        \\
        d_5 \star_5 F & = 0
      }
    \right.
    \right)
  \end{aligned}
$$

These are of course [[Maxwell's equations]] on $\Sigma^5$.

([PS 96 above (16)](#PerrySchwarz96))







### For the full interacting M5-brane sigma model
 {#TheFullInteractingModel}

The full interacting PS Lagrangian  ([PS 96 (63)](#PerrySchwarz96)) has more terms..

(...)


([Schwarz 97](#Schwarz97), [APPS 97](#APPS97))

(...)

## Related concepts

* [[D=5 super Yang-Mills theory]]

## References

The Perry-Schwarz action is due to

* {#PerrySchwarz96} [[Malcolm Perry]], [[John Schwarz]], _Interacting Chiral Gauge Fields in Six Dimensions and Born-Infeld Theory_, Nucl. Phys. B489 (1997) 47-64 ([arXiv:hep-th/9611065](http://arxiv.org/abs/hep-th/9611065))

* {#Schwarz97} [[John Schwarz]], _Coupling a Self-Dual Tensor to Gravity in Six Dimensions_, Phys. Lett. B395:191-195, 1997 ([cds:317663](http://cds.cern.ch/record/317663), <a href="https://doi.org/10.1016/S0370-2693(97)00094-4">doi:10.1016/S0370-2693(97)00094-4</a>)

* {#APPS97} [[Mina Aganagic]], Jaemo Park, Costin Popescu, [[John Schwarz]], _World-Volume Action of the M Theory Five-Brane_, Nucl.Phys. B496 (1997) 191-214 ([arXiv:hep-th/9701166](http://arxiv.org/abs/hep-th/9701166))

A similar construction but with compactification along the [[timelike]] direction is due to

* {#HenneauxTeitelboim88} [[Marc Henneaux]], [[Claudio Teitelboim]], _Dynamics of chiral (self-dual) $p$-forms_, Physics Letters B Volume 206, Issue 4, 2 June 1988, Pages 650-654 (<a href="https://doi.org/10.1016/0370-2693(88)90712-5">doi:10.1016/0370-2693(88)90712-5</a>)

The [[double dimensional reduction]] to the [[Green-Schwarz sigma-model]] of the [[D4-brane]]:

* [APPS 97, Section 6](#APPS97)

* {#APPS97b} [[Mina Aganagic]], Jaemo Park, Costin Popescu, [[John Schwarz]], Section 6 of _Dual D-Brane Actions_, Nucl. Phys. B496 (1997) 215-230 ([arXiv:hep-th/9702133](https://arxiv.org/abs/hep-th/9702133))


The covariant version via a [[scalar field|scalar]] [[auxiliary field]] is due to 

* [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _On Lorentz Invariant Actions for Chiral P-Forms_, Phys.Rev. D55 (1997) 6292-6298 ([arXiv:hep-th/9611100](https://arxiv.org/abs/hep-th/9611100))

* {#PST97} [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _Covariant Action for a D=11 Five-Brane with the Chiral Field_, Phys. Lett. B398 (1997) 41 ([arXiv:hep-th/9701037](https://arxiv.org/abs/hep-th/9701037))

* {#BLNPST97} [[Igor Bandos]], [[Kurt Lechner]], [[Alexei Nurmagambetov]], [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _Covariant Action for the Super-Five-Brane of M-Theory_, Phys. Rev. Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))

Speculations about non-abelian generalizations (for several coincident M5-branes):

* [[Chong-Sun Chu]], _A proposal for the worldvolume action of multiple M5-branes_, 2013 ([pdf](http://hep.phy.ntnu.edu.tw/old_version/talks/2013/2013-05-09Chong-SunChu.pdf))

The above text follows 

* {#FSS19c} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 2 of: _[[schreiber:Super-exceptional embedding construction of the M5-brane|Super-exceptional geometry: origin of heterotic M-theory and super-exceptional embedding construction of M5]]_ ([arXiv:1908.00042](https://arxiv.org/abs/1908.00042))


[[!redirects Perry-Schwarz actions]]

[[!redirects Perry-Schwarz action functional]]
[[!redirects Perry-Schwarz action functionals]]

[[!redirects Perry-Schwarz Lagrangian]]
[[!redirects Perry-Schwarz Lagrangians]]

[[!redirects Perry-Schwarz Lagrangian density]]
[[!redirects Perry-Schwarz Lagrangian densities]]

