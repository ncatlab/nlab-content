
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

[[supergravity]] in [[dimension]] 5. For $N = 1$ this arises from [[11-dimensional supergravity]] by [[KK-compactification]] on a [[Calabi-Yau manifold]] of complex dimension 3 (see at _[[M-theory on Calabi-Yau manifolds]]_), hence serves as the low-energy [[effective field theory]] of the strong-coupling version of Calabi-Yau compactifications of [[type IIA string theory]] (see [[supersymmetry and Calabi-Yau manifolds]])

$$
  \array{
    11d \; SuGra\; on\; S^1 \times Y_6 \times X_4
      &\longrightarrow&
    5d \; SuGra\; on\; S^1 \times X_4 && strong \; coupling
    \\
    \downarrow && \downarrow
    \\
    10d\; tpye \;IIA\; Sugra\; on \; Y_6 \times X_4
      &\longrightarrow&
    10d\; Sugra\; on \; X_4 && weak \; coupling    
  }
$$

## Properties

### 5d Chern-Simons term

This theory has a 2-form field strength $F_2$, locally $F_2 = d A$, with a [[5d Chern-Simons theory]] [[action functional]] locally of the form $\propto \int_X F_2 \wedge F_2 \wedge A$ (e.g. [Castellani-D'Auria-Fre (III.5.70)](#CastellaniDAuriaFre), [GGHPR 02 (2.1)](#GGHPR02), [Bonetti-Grimm-Hohenegger 13](#BonettiGrimmHohenegger13)). Hence its [[equation of motion]] is of the non-linear form

$$
  d F_3 = F_2 \wedge F_2
$$

with $F_3 \coloneqq \star F_2$ the [[Hodge dual]] of $F_2$ ([GGHPR 02 (2.2)](#GGHPR02)).

This is a lower dimensional analogue to the situation for the [[C-field]] $G_4$ (locally $G_4 = d C$) in [[11-dimensional supergravity]], which has a Chern-Simons term locally of the form $\propto \int G_4 \wedge G_4 \wedge C$ and hence the equation of motion

$$
  d G_7 = G_4 \wedge G_4
$$

(up to prefactors) with $G_7 = \star G_4$.

## Properties

### U-duality

[[!include U-duality -- table]]


## Related concepts

* [[5-dimensional Chern-Simons theory]]

* [[11-dimensional supergravity]] 

* 10-dimensional [[type II supergravity]], [[heterotic supergravity]]

* [[7-dimensional supergravity]]

* **5-dimensional supergravity**

* [[4-dimensional supergravity]]

* [[3-dimensional supergravity]]

## References

Discussion in [[D'Auria-Fre formulation of supergravity]] is in

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter III.5 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

Other discussion includes

* W. D. Linch III, Markus A. Luty, J. Phillips, _Five dimensional supergravity in $N = 1$ superspace_, Phys.Rev.D68:025008,2003 ([arXiv:hep-th/0209060](https://arxiv.org/abs/hep-th/0209060))

* {#GGHPR02} [[Jerome Gauntlett]], [[Jan Gutowski]], [[Christopher Hull]], Stathis Pakis, Harvey S. Reall, _All supersymmetric solutions of minimal supergravity in five dimensions_, Class.Quant.Grav. 20 (2003) 4587-4634 ([arXiv:hep-th/0209114](http://arxiv.org/abs/hep-th/0209114))

* [[Eric Bergshoeff]], Sorin Cucu, Tim de Wit, Jos Gheerardyn, Stefan Vandoren, [[Antoine Van Proeyen]], _$N=2$ supergravity in five dimensions revisited_ ([arXiv:hep-th/0403045](http://arxiv.org/abs/hep-th/0403045))

Further discussion of the [[5d Chern-Simons theory|5d Chern-Simons term]] includes

* [[Sergio Ferrara]], Ramzi R. Khuria,  [[Ruben Minasian]], _M-theory on a Calabi-Yau manifold_, Phys.Lett.B375:81-88,1996 ([arXiv:hep-th/9602102](https://arxiv.org/abs/hep-th/9602102))

(from [[M-theory on Calabi-Yau manifolds]])

* {#BonettiGrimmHohenegger13} Federico Bonetti, [[Thomas Grimm]], [[Stefan Hohenegger]], _One-loop Chern-Simons terms in five dimensions_ ([arXiv:1302.2918](http://arxiv.org/abs/1302.2918)) 

(one-loop corrections).

For 5d [[gauged supergravity]]

* M. Pernici, K. Pilch, [[Peter van Nieuwenhuizen]], _Gauged $N=8$ $D=5$ Supergravity_, Nucl.Phys. B259 (1985) 460 ([spire](https://inspirehep.net/record/16067?ln=en))

* M. Gunaydin,  L.J. Romans, N.P. Warner, _Compact and Noncompact Gauged Supergravity Theories in Five-Dimensions_, Nucl.Phys. B272 (1986) 598-646 ([spire](https://inspirehep.net/record/219727?ln=en))

[[!redirects 5d supergravity]]