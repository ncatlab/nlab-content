
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Quantum Field Theory
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

Classical double copy is the counterpart in [[classical field theory]] of [[double copy]] for [[scattering amplitudes]] in [[perturbative quantum field theory]]. It relates classical solutions of the field equations of a [[gauge theory]] with solutions of the [[Einstein equation]] in [[general relativity]].

## Double copy and classical field theory

### Double copy and Kerr-Schild metric

A Kerr-Schild metric is a perturbation of a flat Minkowski metric $\eta_{\mu\nu}$ of the form

$$ g_{\mu\nu} = \eta_{\mu\nu} + \kappa \phi k_{\mu}k_{\nu} $$

where $\kappa=\sqrt{32\pi G_{\mathrm{N}}}$ is a constant with $G_{\mathrm{N}}$ Newton constant, $\phi$ is a scalar field and $k_\mu$ is a null covector satisfying the geodesic property, i.e.

$$ \eta_{\mu\nu}k^\mu k^\nu = g_{\mu\nu}k^\mu k^\nu =0, \quad (k\cdot\partial)k^\mu =0.$$

The _single copy_ gauge field ([MOW 15](#MOW15)) of this gravitational field is defined for any [[gauge group]] $G$ by

$$A_{\mu} = (c^a \mathbf{T}_a) \phi k_\mu$$

where $c^a\mathbf{T}_a \in \mathfrak{g}$ is an arbitrary constant [[color charge]], specified by a vector $c^a$ in the basis $\{\mathbf{T}_a\}$ of $\mathfrak{g}$. We thus call the gravitational field $g_{\mu\nu}$ the _double copy_ ([MOW 15](#MOW15)) of any such gauge field $A_{\mu}$.

## Examples

Examples of classical double copy of gauge fields:

| [[gauge theory]] solution | [[gravity]] solution | ref. |
|--|--|--|
| electric monopole | [[Schwarzschild spacetime]] | ([MOW 15](#MOW15)) |
| magnetic monopole | massless [[Taub-NUT space]] | ([LMOW 15](#LMOW15)) |
| planar wave | pp-wave | ([MOW 15](#MOW15)) |
|planar shockwave | Aichelburg-Sexl shockwave | ([BSW 20](#BSW20)) |

In terms of [[charges]] we have the following correspondence:

| [[gauge theory]] solution | [[gravity]] solution |
|--|--|
| [[electric charge]] | [[mass]] |
| [[magnetic charge]] | NUT charge |

## Double copy and [[S-duality]]

In ([ABSP 19](#ABSP19)) it was proved that an electromagnetic duality ([[S-duality]]) transformation on the single copy gauge fields corresponds to an [[Ehlers transformation]] on the double copy gravitational field. In other words the following ideal diagram commutes:

$$\array{{electric \; monopole} & \overset{{\;\; double \; copy \;\;}}{\to} & {Schwarzschild \; black \; hole}\\
& \\
  ^{{S-duality}}\downarrow && \downarrow^{{Ehlers \; transformation}}\\
& \\
  {magnetic \; monopole}& \underset{{\;\; double \; copy \;\;}}{\to} & {NUT-charged \; spacetime}}$$

## Related entries

* [[KLT relations]]

* [[Schwarzschild spacetime]], [[Taub-NUT space]]

* [[duality in physics]]

* [[string theory results applied elsewhere]], [[open/closed string duality]]

* [[magic pyramid]], [[magic supergravity]]

* [[Kaluza-Klein mechanism]], [[Kaluza-Klein monopole]]

## References

* {#MOW15} Ricardo Monteiro, Donal O'Connell, Chris D. White, _Black holes and the double copy_ ([arXiv:1410.0239](https://arxiv.org/abs/1410.0239))

* {#LMOW15} Andrés Luna, Ricardo Monteiro, Donal O'Connell, Chris D. White, _The classical double copy for Taub-NUT spacetime_ ([arXiv:1507.01869](https://arxiv.org/abs/1507.01869))

* Chris D. White, _The double copy: gravity from gluons_ ([arXiv:1708.07056](https://arxiv.org/abs/1708.07056))

* [[David Berman]], Erick Chacón, Andrés Luna, Chris D. White, _The self-dual classical double copy, and the Eguchi-Hanson instanton_ ([arXiv:1809.04063](https://arxiv.org/abs/1809.04063))

* Kwangeon Kim, Kanghoon Lee, Ricardo Monteiro, Isobel Nicholson, David Peinador Veiga, _The Classical Double Copy of a Point Charge_ ([arXiv:1912.02177](https://arxiv.org/abs/1912.02177))

* {#BSW20} Nadia Bahjat-Abbas, Ricardo Stark-Muchão, Chris D. White, _Monopoles, shockwaves and the classical double copy_ ([arXiv:2001.09918](https://arxiv.org/abs/2001.09918))

In the following paper it is shown that a [[S-duality]] on a gauge field corresponds to an [[Ehlers transformation]] on its double copy:

* {#ABSP19} Rashid Alawadhi, [[David Berman]], Bill Spence, David Peinador Veiga, _S-duality and the Double Copy_ ([arXiv:1911.06797](https://arxiv.org/abs/1911.06797))

The following paper is a proposal of extension of [[classical double copy]] to [[double field theory]]:

* Kanghoon Le, _Kerr-Schild Double Field Theory and Classical Double Copy_ ([arXiv:1807.08443](https://arxiv.org/abs/1807.08443))