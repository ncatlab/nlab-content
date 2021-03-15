
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _classical double copy_-method is the counterpart in [[classical field theory]] of the [[double copy]]-phenomenon for [[scattering amplitudes]] in [[perturbative quantum field theory]]. It relates classical solutions of the [[equation of motion|field equations]] of a [[Yang-Mills theory|Yang-Mills]] [[gauge theory]] with solutions of the [[Einstein equation]] in [[general relativity]].

## Double copy and classical field theory

### Double copy and Kerr-Schild metric

#### Definitions

* A [[Kerr-Schild spacetime|Kerr-Schild metric]] is a [[perturbation]] of a flat [[Minkowski metric]] $\eta_{\mu\nu}$ of the form

  $$ g_{\mu\nu} = \eta_{\mu\nu} + \kappa \phi k_{\mu}k_{\nu} $$

  where $\kappa=\sqrt{32\pi G_{\mathrm{N}}}$ is a constant with $G_{\mathrm{N}}$ [[Newton's constant]], $\phi$ is a [[scalar field]] and $k_\mu$ is a [[lightlike|null]] [[covector]] satisfying the [[geodesic]] property, i.e.

  $$ \eta_{\mu\nu}k^\mu k^\nu = g_{\mu\nu}k^\mu k^\nu =0, \quad (k\cdot\partial)k^\mu =0.$$

* The _single copy_ gauge field ([MOW 15](#MOW15)) of this gravitational field is defined for any [[gauge group]] $G$ by

  $$A_{\mu} = (c^a \mathbf{T}_a) \phi k_\mu$$

  where $c^a\mathbf{T}_a \in \mathfrak{g}$ is an arbitrary constant [[color charge]], specified by a [[vector]] $c^a$ in the [[linear basis|basis]] $\{\mathbf{T}_a\}$ of the [[Lie algebra]] $\mathfrak{g}$. 

* Conversely, if we start from a gauge field of the form $A_{\mu} = (c^a \mathbf{T}_a) \phi k_\mu$ for any constant [[color charge]] $c^a\mathbf{T}_a \in \mathfrak{g}$ and [[lightlike|null]] [[covector]] $k_\mu$ satisfying the [[geodesic]] property, we can define its _double copy_ gravitational field by the [[Kerr-Schild spacetime|Kerr-Schild metric]] $g_{\mu\nu}=\eta_{\mu\nu} + \kappa \phi k_{\mu}k_{\nu}$.

* Otherwise, if we repeat the procedure of replacing a covector $k_\mu$ with any fixed [[color charge]] $(\tilde{c}^b \tilde{\mathbf{T}}_b)\in\tilde{\mathfrak{g}}$ we can get a _zeroth copy_ [[scalar field]], defined by

  $$\Phi = (c^a \mathbf{T}_a)\otimes(\tilde{c}^b \tilde{\mathbf{T}}_b)\phi $$

  where the new [[gauge group]] $\tilde{G}$ can be chosen different from the previous $G$.

#### Field equations

By following ([MOW 15](#MOW15)) we have a comparison of the field equations. Assume without loss of generality that $k^0=1$. We get the following:

* The vacuum [[Einstein equations]] for the metric $g_{\mu\nu}$ are $R=0$ (where $R$ is the [[Ricci curvature]]), which reduce to
$$\begin{aligned}
R^0_{\;0} &= \frac{1}{2}\nabla^2\phi && = 0 \\
R^i_{\;0} &= \frac{1}{2}\partial_j \left(\partial^j(\phi k^i)-\partial^i(\phi k^j)\right) && =0 \\
R^i_{\;j} &= \frac{1}{2}\partial_l \left(\partial^i(\phi k^l k^j)+\partial_j(\phi k^l k^i)-\partial^l(\phi k^i k_j)\right) && =0
\end{aligned}$$

* The [[Maxwell equations]] for the gauge field $A$ are $\mathrm{d} F = 0$, which reduce to
$$\begin{aligned}
(\mathrm{d}F)^0 &= \nabla^2\phi && = 0 \\
(\mathrm{d}F)^i &= \partial_j \left(\partial^j(\phi k^i)-\partial^i(\phi k^j)\right) && = 0
\end{aligned}$$

* The [[Klein-Gordon equation]] for the scalar field $\Phi$ are
$$\nabla^2\Phi = 0$$

#### Outlook

Summarizing, we have the following table:

| zeroth copy | single copy | double copy |
|--|--|--|
| $\;\Phi = (c^a \mathbf{T}_a)\otimes(\tilde{c}^b \tilde{\mathbf{T}}_b)\phi\;$ | $\;A_{\mu} = (c^a \mathbf{T}_a) \phi k_\mu\;$ | $\;g_{\mu\nu} = \eta_{\mu\nu} + \kappa \phi k_{\mu}k_{\nu}\;$ |

\begin{imagefromfile}
"file_name": "doublecopy.png",
"width": 700,
"unit": "px",
"caption": "Picture grabbed from ([BSW 20](#BSW20))."
\end{imagefromfile}


## Examples

Examples of classical double copy of gauge fields:

| [[gauge theory]] solution | [[gravity]] solution | ref. |
|--|--|--|
| electric monopole | [[Schwarzschild spacetime]] | ([MOW 15](#MOW15)) |
| magnetic monopole | massless [[Taub-NUT spacetime]] | ([LMOW 15](#LMOW15)) |
| planar wave | [[pp-wave]] | ([MOW 15](#MOW15)) |
|planar shockwave | Aichelburg-Sexl shockwave | ([BSW 20](#BSW20)) |

## Double copy and topology

From ([LMOW 15](#LMOW15)) we know that in terms of [[charges]] we have the following correspondence:

| [[gauge theory]] solution | [[gravity]] solution |
|--|--|
| [[electric charge]] | [[mass]] |
| [[magnetic charge]] | [[NUT charge]] |

The topological consequences were explored by ([AWW 20](#AWW20)):

* A [[magnetic monopole]] is geometrically a [[principal bundle]] of the form 
$$\underset{ \text{worldline} }\underbrace{\mathbb{R}^{1}} \times \underset{ \text{transverse space} }\underbrace{ (\mathbb{R}^3-\{0\}) } \;\,\simeq_{\mathrm{diff}}\;\,  \underset{ \text{worldline} }\underbrace{\mathbb{R}^{1}} \times \underset{ \text{radial dir.} }\underbrace{\mathbb{R}^+} \times \underset{ \text{angular dir.} }\underbrace{S^2} \longrightarrow B U(1) $$
which is trivial only on the worldline $\mathbb{R}^{1}$ of the monopole. Therefore, since we have the homotopy $\mathbb{R}^3-\{0\} \simeq S^2$, the [[first Chern class]] of the bundle will be an element $[F] \in H^2(S^2,\mathbb{Z})\cong \mathbb{Z}$. In other words we have
$$ [F] = \tilde{g} [\mathrm{Vol}_{S^2}] $$
where $\mathrm{Vol}_{S^2}$ is the volume form of $S^2$ and $\tilde{g}\in\mathbb{Z}$ is the quantized [[magnetic charge]].

* The massless [[Taub-NUT spacetime]] with [[NUT charge]] $N$ is a [[circle bundle]] too. In fact it is diffeomorphic to the manifold $\mathbb{R}^+\times L(1,N)$, where $\times L(1,N)$ is the $3$-dimensional Lens space with quantized [[first Chern class]] $N\in\mathbb{Z}\cong H^2(S^2,\mathbb{Z})$. In this case the $S^1$ fiber has the interpretation of [[time]] direction, which is periodic and non-trivially fibrated on the sphere $S^2$ of the angular directions.

Therefore the double copy procedure exchange the [[first Chern class]] of the [[magnetic monopole]] with the one of [[Taub-NUT spacetime]], i.e.
$$ \tilde{g} \mapsto N. $$


## Double copy and Wilson lines

The classical double copy of [[Wilson lines]] was introduced by ([AWW 20](#AWW20)). We can use as gravitational [[Wilson lines]] on spacetime $M$ the [[action functional]] $e^{i S_{\mathrm{kin}}}: [S^1, M]\rightarrow U(1)$ of a test particle. For any loop $\gamma\in[S^1, M]$ we can then write

$$ W_{\mathrm{grav}}(\gamma) = e^{i S_{\mathrm{kin}}}(\gamma) = \exp \left(i m \int_\gamma \mathrm{d}s \left(g_{\mu\nu}\frac{\mathrm{d}x^\mu}{\mathrm{d}s}\frac{\mathrm{d}x^\nu}{\mathrm{d}s}\right)^{\frac{1}{2}} \right) \;\in\, U(1) $$

If we assume that the metric is of the form $g_{\mu\nu} = \eta_{\mu\nu} + \kappa h_{\mu\nu}$, we can expand $W_{\mathrm{grav}}(\gamma)$ at first order in $\kappa$ and obtain

$$ W_{\mathrm{grav}}(\gamma) = \exp \left(\frac{i \kappa}{2} \int_\gamma \mathrm{d}s\, h_{\mu\nu}\frac{\mathrm{d}x^\mu}{\mathrm{d}s}\frac{\mathrm{d}x^\nu}{\mathrm{d}s} \right) \;\in\, U(1) $$

where the mass $m$ is absorbed into the new parameter $s$. If now we write the [[holonomy]] of the _single copy_ gauge field along the same path $\gamma$ we get

$$ W_{\mathrm{gauge}}(\gamma) = \mathcal{P}\exp \left(i g \int_\gamma \mathrm{d}s\, A_{\mu}^a \frac{\mathrm{d}x^\mu}{\mathrm{d}s}\mathbf{T}_a \right) \;\in\, G$$

Thus we immediately see that the double copy rules for a [[Wilson line]] are the following:

$$ \mathbf{T}_a \mapsto  \frac{\mathrm{d}x^\nu}{\mathrm{d}s}, \quad\; g \mapsto  \frac{\kappa}{2}$$

Notice that they precisely mirror the BCJ prescription of [[double copy]] for [[scattering amplitudes]] by exchanging color data with kinematic data and gauge coupling constant with its gravitational analogue. 

This suggests that this formulation can be a bridge to formally connect [[classical double copy]] with [[double copy]] for [[scattering amplitudes]].

## Double copy and S-duality

In ([ABSP 19](#ABSP19)) it was proved that an [[electric-magnetic duality]] (i.e. [[S-duality]]) transformation on the single copy gauge fields corresponds to an [[Ehlers transformation]] on the double copy gravitational field. In other words the following ideal diagram commutes:

$$\array{{electric \; monopole} & \overset{{\;\; double \; copy \;\;}}{\to} & {Schwarzschild \; black \; hole}\\
& \\
  ^{{S-duality}}\downarrow && \downarrow^{{Ehlers \; transformation}}\\
& \\
  {magnetic \; monopole}& \underset{{\;\; double \; copy \;\;}}{\to} & {NUT-charged \; spacetime}}$$

## Related concepts

* [[KLT relations]]

* [[Schwarzschild spacetime]], [[Taub-NUT space]]

* [[duality in physics]]

* [[string theory results applied elsewhere]], [[open/closed string duality]]

* [[magic pyramid]], [[magic supergravity]]

* [[Kaluza-Klein mechanism]], [[Kaluza-Klein monopole]]

* [[effective QFT]] incarnations of [[open/closed string duality]], 
  
  relating ([[supergravity|super]]-)[[gravity]] to ([[super Yang-Mills theory|super]]-)[[Yang-Mills theory]]:

  * [[KLT relations]]

  * [[BCJ relations]]

  * [[classical double copy]] 



## References

Fundamental bibliography:

* {#MOW15} Ricardo Monteiro, Donal O'Connell, Chris D. White, _Black holes and the double copy_ ([arXiv:1410.0239](https://arxiv.org/abs/1410.0239))

* {#LMOW15} Andrés Luna, Ricardo Monteiro, Donal O'Connell, Chris D. White, _The classical double copy for Taub-NUT spacetime_ ([arXiv:1507.01869](https://arxiv.org/abs/1507.01869))

* Chris D. White, _The double copy: gravity from gluons_ ([arXiv:1708.07056](https://arxiv.org/abs/1708.07056))

* [[David Berman]], Erick Chacón, Andrés Luna, Chris D. White, _The self-dual classical double copy, and the Eguchi-Hanson instanton_ ([arXiv:1809.04063](https://arxiv.org/abs/1809.04063))

* Kwangeon Kim, Kanghoon Lee, Ricardo Monteiro, Isobel Nicholson, David Peinador Veiga, _The Classical Double Copy of a Point Charge_ ([arXiv:1912.02177](https://arxiv.org/abs/1912.02177))

* {#BSW20} Nadia Bahjat-Abbas, Ricardo Stark-Muchão, Chris D. White, _Monopoles, shockwaves and the classical double copy_ ([arXiv:2001.09918](https://arxiv.org/abs/2001.09918))

Foundational issues:

* Chris D. White, _A Twistorial Foundation for the Classical Double Copy_ ([arXiv:2012.02479](https://arxiv.org/abs/2012.02479))


Some global aspects of the [[classical double copy]] were explored in the following paper:

* {#AWW20} [[Luigi Alfonsi]], Chris D. White, Sam Wikeley, _Topology and Wilson lines: global aspects of the double copy_ ([arXiv:2004.07181](https://arxiv.org/abs/2004.07181))

In the following paper it is shown that a [[S-duality]] on a gauge field corresponds to an [[Ehlers transformation]] on its double copy:

* {#ABSP19} Rashid Alawadhi, [[David Berman]], Bill Spence, David Peinador Veiga, _S-duality and the Double Copy_ ([arXiv:1911.06797](https://arxiv.org/abs/1911.06797))

The following paper is a proposal of extension of [[classical double copy]] to [[double field theory]]:

* Kanghoon Lee, _Kerr-Schild Double Field Theory and Classical Double Copy_ ([arXiv:1807.08443](https://arxiv.org/abs/1807.08443))

See also:

* Andres Luna, Silvia Nagy, Chris White, _The convolutional double copy: a case study with a point_ ([arXiv:2004.11254](https://arxiv.org/abs/2004.11254))

Discussion for [[D=11 supergravity]]:

* [[David Berman]], Kwangeon Kim, Kanghoon Lee, _The Classical Double Copy for M-theory from a Kerr-Schild Ansatz for Exceptional Field Theory_ ([arXiv:2010.08255](https://arxiv.org/abs/2010.08255))

Discussion via [[L-infinity algebras]]:

* [[Leron Borsten]], [[Branislav Jurco]], [[Hyungrok Kim]], [[Tommaso Macrelli]], [[Christian Saemann]], [[Martin Wolf]], _Double Copy from Homotopy Algebras_ ([arXiv:2102.11390](https://arxiv.org/abs/2102.11390))

For curved spacetimes:

* Gokhan Alkac, Mehmet Kemal Gumus, Mustafa Tek, _The Classical Double Copy in Curved Spacetime_ ([arXiv:2103.06986](https://arxiv.org/abs/2103.06986))





