+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What are called _half-spin groups_ or _semi-spin groups_ ([McInnes 99a](#McInnes99a), [McInnes 99b](#McInnes99b)) are [[quotient groups]] of [[spin groups]] $Spin(n)$ by a _non-standard_ [[Z/2]]-[[subgroup]]:

Generally, every [[spin group]] $Spin(n)$ is, essentially by definition, a $\mathbb{Z}/2$-[[group extension]] of the corresponding [[special orthogonal group]], so that the [[quotient group]] by the resulting canonical [[subgroup]] inclusion $\mathbb{Z}/2 \overset{\iota}{\hookrightarrow} Spin(n)$ recovers [[SO(n)]]

$$
  Spin(n)/_{\iota}(\mathbb{Z}/2) \simeq SO(n)
  \,.
$$

But in the special case that the [[dimension]] $n = 4k$ is a [[positive number|positive]] multiple of 4 distinct from 8 (i.e. $k \in \mathbb{N}_{\gt 0}, k \neq 2$), there is _another_ $\mathbb{Z}/2$-[[conjugacy class of subgroups]] $\mathbb{Z}/2 \overset{\iota_{s}}{\hookrightarrow} Spin(4k)$, which is distinct from the canonical $\iota$, and hence yields a [[quotient group]]

$$
  SemiSpin\big(4k \big)
  \;\coloneqq\;
  Spin\big(4k\big)/_{\iota_s} (\mathbb{Z}/2)
$$ 

which is distinct from (i.e. not [[isomorphism|isomorphic]] to) [[SO(n)]].

This is called the _semi-spin group_ or _half-spin_ group in that dimension.

## Examples

### SemiSpin(4)

The semi-spin group in [[dimension]] 4 is just the [[direct product group]] of [[SU(2)]] with [[SO(3)]]:

$$
  SemiSpin(4)
  \;\simeq\;
  SU(2) \times SO(3)
$$


### SemiSpin(8)
 {#SemiSpin8}

While also for [[Spin(8)]] it is the case that the [[center]] contains two copies of [[Z/2]], $Z\big( Spin(8)\big) \simeq  \mathbb{Z}_2 \times \mathbb{Z}_2$, in this case the existence of [[triality]] [[automorphisms]] actually makes these two copies behave identically, so that here the would-be semi-spin groups happens to coincide with [[SO(8)]] after all:

$$
  Spin(8)/_{\iota_s} \mathbb{Z}_2
  \;\simeq\;
  SO(8)
  \;\simeq\;  
  Spin(8)/_{\iota} \mathbb{Z}_2
$$

(e.g. [McInnes 99a, p. 9](#McInnes99a))

### SemiSpin(16)

The [[subgroup]] of the [[exceptional Lie group]] [[E8]] which corresponds to the [[Lie algebra]]-inclusion $\mathfrak{so}(16) \hookrightarrow \mathfrak{e}_8$ is the [[semi-spin group]] [[SemiSpin(16)]]:

$$
  SemiSpin(16)
  \;\subset\;
  E_8
$$

On the other hand, the [[special orthogonal group]] $SO(16)$ is _not_ a [[subgroup]] of $E_8$ (e.g. [McInnes 99a, p. 11](#McInnes99a)).

In [[heterotic string theory]] with [[gauge group]] the [[direct product group]] $E_8 \times E_8$ it is typically this [[subgroup]] $Semispin(16) \times SemiSpin(16)$ which is considered (but typically denoted $Spin(16)/\mathbb{Z}_2$, see also [Distler-Sharpe 10, Sec. 1](parameterized+WZW+model#DistlerSharpe10)).

### SemiSpin(32)

In [[heterotic string theory]] precisely two ([[isomorphism classes]] of) [[gauge groups]] are consistent (give [[quantum anomaly cancellation]]): one is the [[direct product group]] $E_8 \times E_8$ of the [[exceptional Lie group]] [[E8]] with itself, the other is in fact the [[semi-spin group]] [[SemiSpin(32)]] (see [McInnes 99a, p. 5](#McInnes99a)). 

Beware  that the [[string theory]] literature often writes this as $Spin(32)/\mathbb{Z}_2$, which is at best ambiguous and misleading, or even as $SO(32)$, which is wrong. Of course this follows the general tradition in the [[physics]] literature to write identifications of [[Lie groups]] that are really only identifications of their [[Lie algebras]], see also ["SO(10)-GUT theory"](GUT#TheGUTKnownAsSO10).


## Related entries

* [[spin group]]

* [[Spin(n1).Spin(n2)]]

* [[heterotic string theory]], [[Green-Schwarz anomaly cancellation]]


[[!include low dimensional rotation groups -- table]]


## References

* {#McInnes99a} [[Brett McInnes]], _The Semispin Groups in String Theory_, J. Math. Phys. **40** (1999) 4699-4712 \[<a href="https://arxiv.org/abs/hep-th/9906059">arXiv:hep-th/9906059</a>, [doi:10.1063/1.532999](https://doi.org/10.1063/1.532999)\]

* {#McInnes99b} [[Brett McInnes]], _Gauge Spinors and String Duality_,  Nucl. Phys. B577:439-460, 2000 ([arXiv:hep-th/9910100](https://arxiv.org/abs/hep-th/9910100))

* Mboyo Esole, Monica Jinwoo Kang, _Flopping and Slicing: $SO(4)$ and $Spin(4)$-models_ ([arXiv:1802.04802](https://arxiv.org/abs/1802.04802))

[[!redirects semi-spin groups]]

[[!redirects semispin group]]
[[!redirects semispin groups]]

[[!redirects half-spin group]]
[[!redirects half-spin groups]]