
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

A [[Lagrangian density]]/[[action functional]] for the [[self-dual higher gauge field]] in 6d and/or the [[M5-brane]] [[Green-Schwarz sigma model]], after [[KK-compactification]] to 5 [[worldvolume]] [[dimensions]].

## Details

### For the self-dual field and trivial target space metric

We review the definitions from [Perry-Schwarz 96](#PerrySchwarz96),
for the [[worldvolume]] [[Lagrangian density]] of just the [[self-dual higher gauge field]] on a [[circle principal bundle]]-[[worldvolume]] for would-be [[target space]] being [[Minkowski spacetime]].
In doing so, we translate to [[coordinate chart|coordinate]]-invariant [[Cartan calculus]]-formalism and generalized to [[KK-compactification]] on possibly non-[[trivial bundle|trivial]] [[circle principal bundle]]:

\linebreak

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

for the [[vector field]] which reflects the infinitesimal [[circle group]]-[[action]] on (eq:FibrationWorldvolume).

With the notation ([PS 96 (5)](#PerrySchwarz96))

$$
  \mathcal{F}
  \;\coloneqq\;
  \iota_{v^5} H
$$

and ([PS 96 (6)](#PerrySchwarz96))

\[
  \label{DefOfTildeH}
  \tilde H
  \;\coloneqq\;
  \iota_{v^5} \star H
\]

the self-duality condition (eq:SelfDualityIn6d)
is equivalently ([PS 96 (9)](#PerrySchwarz96))

\[
  \label{SelfDualityIntermsOfcalF}
  \mathcal{F}
  \;=\;
  \tilde H
\]

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

Now suppose that there exists

$$
  B \in \Omega^2\big( \Sigma^6 \big)
$$

such that ([PS 96 (4)](#PerrySchwarz96))

$$
  H = d B
$$

Setting ([PS 96 above (4)](#PerrySchwarz96))

\[
  \label{AField}
  A
  \;\coloneqq\;
  -
  \iota_{v^5} B
\]

we have

$$
  B
  \;=\;
  A \wedge \theta^5 
  +
  B^{\mathrm{hor}}
$$

Set also ([PS 96 above (4)](#PerrySchwarz96))

$$
  F
  \;\coloneqq\;
  \big( d A \big)^{\mathrm{hor}}
$$

then ([PS 96 (5)](#PerrySchwarz96))

$$
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
$$
where in the last step under the brace we used 
(eq:EhresmannConditions) and (eq:AField).

Hence in terms of $F$ and $B^{\mathrm{hor}}$ the self-duality condition 
(eq:SelfDualityIn6d), (eq:SelfDualityIntermsOfcalF)
now reads

$$
  \widetilde H
  \;=\;
  F + \mathcal{L}_{v^5} B^{\mathrm{hor}}
$$

Finally, the Perry-Schwarz-Lagrangian is ([PS 96 (17)](#PerrySchwarz96))

\[
  \label{CartanCalculusPerrySchwarzLagrangian}
  L
  \;\coloneqq\;
  \tfrac{1}{2}
  \big(
  \mathcal{L}_{v^5} B^{\mathrm{hor}}
  -
  \tilde H
  \big)
  \wedge 
  \star 
  \tilde H
\]

Now we ask $v^5$ (eq:FiberVectorField) to be an [[isometry]]. This means that

\[
  \label{HodgeStarCommutingWithIsometryContraction}
  \star \circ \iota_{v^5}
  =
  -
  \theta^5 \wedge \star
  \;:\;
  \Omega^3\big( \Sigma^6\big)
  \longrightarrow
  \Omega^4\big( \Sigma^6 \big)
\]

and hence (eq:CartanCalculusPerrySchwarzLagrangian) becomes

\[
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

If we use the self-duality condition (eq:SelfDualityIn6d)
then this is

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


### For the full M5-brane sigma model

(...)

([Schwarz 97](#Schwarz97), [APPS 97](#APPS97))

(...)

## References

The Perry-Schwarz action is due to

* {#PerrySchwarz96} [[Malcolm Perry]], [[John Schwarz]], _Interacting Chiral Gauge Fields in Six Dimensions and Born-Infeld Theory_, Nucl. Phys. B489 (1997) 47-64 ([arXiv:hep-th/9611065](http://arxiv.org/abs/hep-th/9611065))

* {#Schwarz97} [[John Schwarz]], _Coupling a Self-Dual Tensor to Gravity in Six Dimensions_, Phys. Lett. B395:191-195, 1997 ([cds:317663](http://cds.cern.ch/record/317663), <a href="https://doi.org/10.1016/S0370-2693(97)00094-4">doi:10.1016/S0370-2693(97)00094-4</a>)

* {#APPS97} [[Mina Aganagic]], Jaemo Park, Costin Popescu, [[John Schwarz]], _World-Volume Action of the M Theory Five-Brane_, Nucl.Phys. B496 (1997) 191-214 ([arXiv:hep-th/9701166](http://arxiv.org/abs/hep-th/9701166))

Its covariantisations via a [[scalar field|scalar]] [[auxiliary field]] is due to 

* [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _On Lorentz Invariant Actions for Chiral P-Forms_, Phys.Rev. D55 (1997) 6292-6298 ([arXiv:hep-th/9611100](https://arxiv.org/abs/hep-th/9611100))

* {#PST97} [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _Covariant Action for a D=11 Five-Brane with the Chiral Field_, Phys. Lett. B398 (1997) 41 ([arXiv:hep-th/9701037](https://arxiv.org/abs/hep-th/9701037))

* {#BLNPST97} [[Igor Bandos]], [[Kurt Lechner]], [[Alexei Nurmagambetov]], [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _Covariant Action for the Super-Five-Brane of M-Theory_, Phys. Rev. Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))


[[!redirects Perry-Schwarz actions]]

[[!redirects Perry-Schwarz action functional]]
[[!redirects Perry-Schwarz action functionals]]

[[!redirects Perry-Schwarz Lagrangian]]
[[!redirects Perry-Schwarz Lagrangians]]

[[!redirects Perry-Schwarz Lagrangian density]]
[[!redirects Perry-Schwarz Lagrangian densities]]

