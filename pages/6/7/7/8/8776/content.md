
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

### Black holes and black rings

The first [[black ring]] solution in 5d sugra was found in ([Elvang-Emparan-Mateos-Reall 04](#ElvangEmparanMateosReall04), [Elvang-Emparan-Mateos-Reall 05](#ElvangEmparanMateosReall05)).



### Via Calabi-Yau compactification of M-theory

([Hull-Townsend 95, p.30-31](#HullTownsend95), [Ferrara-Khuria-Minasian 96](#FerraraKhuriaMinasian96))


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

### General

Basic discussion includes

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter III.5 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

  (in [[D'Auria-Fre formulation of supergravity]])

* W. D. Linch III, Markus A. Luty, J. Phillips, _Five dimensional supergravity in $N = 1$ superspace_, Phys.Rev.D68:025008,2003 ([arXiv:hep-th/0209060](https://arxiv.org/abs/hep-th/0209060))

* {#GGHPR02} [[Jerome Gauntlett]], [[Jan Gutowski]], [[Christopher Hull]], Stathis Pakis, Harvey S. Reall, _All supersymmetric solutions of minimal supergravity in five dimensions_, Class.Quant.Grav. 20 (2003) 4587-4634 ([arXiv:hep-th/0209114](http://arxiv.org/abs/hep-th/0209114))

* [[Eric Bergshoeff]], Sorin Cucu, Tim de Wit, Jos Gheerardyn, Stefan Vandoren, [[Antoine Van Proeyen]], _$N=2$ supergravity in five dimensions revisited_ ([arXiv:hep-th/0403045](http://arxiv.org/abs/hep-th/0403045))

### Via M-theory on Calabi-Yau 3-folds

Discussion via [[KK-compactification]] as [[M-theory on Calabi-Yau manifolds]] includes

* {#HullTownsend95} [[Chris Hull]], [[Paul Townsend]], pages 30 and 31 od _Unity of Superstring Dualities_, Nucl.Phys.B438:109-137,1995 ([arXiv:hep-th/9410167](https://arxiv.org/abs/hep-th/9410167))

* {#FerraraKhuriaMinasian96} [[Sergio Ferrara]], Ramzi R. Khuria,  [[Ruben Minasian]], _M-theory on a Calabi-Yau manifold_, Phys.Lett.B375:81-88,1996 ([arXiv:hep-th/9602102](https://arxiv.org/abs/hep-th/9602102))

Further discussion of the [[5d Chern-Simons theory|5d Chern-Simons term]] includes

* {#BonettiGrimmHohenegger13} Federico Bonetti, [[Thomas Grimm]], [[Stefan Hohenegger]], _One-loop Chern-Simons terms in five dimensions_ ([arXiv:1302.2918](http://arxiv.org/abs/1302.2918)) 

(one-loop corrections).

### Gauged sugra

For 5d [[gauged supergravity]]:

* M. Pernici, K. Pilch, [[Peter van Nieuwenhuizen]], _Gauged $N=8$ $D=5$ Supergravity_, Nucl.Phys. B259 (1985) 460 ([spire](https://inspirehep.net/record/16067?ln=en))

* M. Gunaydin,  L.J. Romans, N.P. Warner, _Compact and Noncompact Gauged Supergravity Theories in Five-Dimensions_, Nucl.Phys. B272 (1986) 598-646 ([spire](https://inspirehep.net/record/219727?ln=en))

* Murat Gunaydin, Marco Zagermann, _The Gauging of Five-dimensional, $N=2$ Maxwell-Einstein Supergravity Theories coupled to Tensor Multiplets_,  	Nucl.Phys.B572:131-150,2000 ([arXiv:hep-th/9912027](https://arxiv.org/abs/hep-th/9912027))

* Murat Gunaydin, Marco Zagermann, _The Vacua of 5d, $N=2$ Gauged Yang-Mills/Einstein/Tensor Supergravity: Abelian Case_, Phys.Rev.D62:044028,2000 ([arXiv:hep-th/0002228](http://arxiv.org/abs/hep-th/0002228))

* A. Ceresole, [[Gianguido Dall'Agata]], _General matter coupled $N=2$, $D=5$ gauged supergravity_, Nucl.Phys. B585 (2000) 143-170 ([arXiv:hep-th/0004111](http://arxiv.org/abs/hep-th/0004111))

### Horava-Witten compactification
 {#ReferencesHWCompactification}

Discussion of [[KK-compactification]] on $S^1/(\mathbb{Z}/2)$-orbifolds (the version of [[Horava-Witten theory]] after dimensional reduction) is discussed in

* Filipe Paccetti Correia, Michael G. Schmidt, Zurab Tavartkiladze, _4D Superfield Reduction of 5D Orbifold SUGRA and Heterotic M-theory_ ([arXiv:hep-th/0602173](https://arxiv.org/abs/hep-th/0602173))

### Black hole solutions

Discussion of lifts of 4d black holes to 5d black holes and embedding as [[black holes in string theory]] includes

* {#ElvangEmparanMateosReall04} Henriette Elvang, Roberto Emparan, David Mateos, [[Harvey Reall]], _A supersymmetric black ring_, Phys.Rev.Lett.93:211302,2004 ([arXiv:hep-th/0407065](http://arxiv.org/abs/hep-th/0407065))

* {#ElvangEmparanMateosReall05} Henriette Elvang, Roberto Emparan, David Mateos, [[Harvey Reall]], _Supersymmetric 4D Rotating Black Holes from 5D Black Rings_, JHEP0508:042,2005 ([arXiv:hep-th/0504125](http://arxiv.org/abs/hep-th/0504125))


* I. Bena, [[Per Kraus]], _Microscopic description of black rings in AdS/CFT_ JHEP 12 (2004) 070 ([hep-th/0408186](http://arxiv.org/abs/hep-th/0408186))

* I. Bena and P. Kraus, _Microstates of the D1-D5-KK system_ Phys. Rev. D72 (2005) 025007 ([hep-th/0503053](http://arxiv.org/abs/hep-th/0503053))

* [[Davide Gaiotto]], [[Andrew Strominger]], and X. Yin, _5D black rings and 4D black holes_ JHEP 02 (2006) 023 ([hep-th/0504126](http://arxiv.org/abs/hep-th/0504126))

* [[Davide Gaiotto]], [[Andrew Strominger]], and X. Yin, _New connections between 4D and 5D black holes_, JHEP 02 (2006) 024 ([hep-th/0503217](https://arxiv.org/abs/hep-th/0503217))

* Alejandra Castro, Joshua L. Davis, [[Per Kraus]], Finn Larsen, _String Theory Effects on Five-Dimensional Black Hole Physics_ ([arXiv:0801.1863](http://arxiv.org/abs/0801.1863))

* Minkyu Park, Masaki Shigemori, _Codimension-2 Solutions in Five-Dimensional Supergravity_, JHEP 1510 (2015) 011 ([arXiv:1505.05169](http://arxiv.org/abs/1505.05169))

Review includes

* [[Per Kraus]], _Lectures on black holes and the AdS_3 / CFT_2 correspondence_ ([arXiv:hep-th/0609074](http://arxiv.org/abs/hep-th/0609074))

  _Stringy black holes in five dimensions_, 2007 ([pdf slides](http://hep.ps.uci.edu/~arajaram/Irvine.07.pdf))

[[!redirects 5d supergravity]]