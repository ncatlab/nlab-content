[[!redirects M-theory on Spin(8)-manifolds]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[KK-compactification]] of [[M-theory]] on [[fibers]] which are [[8-manifolds]]. In the low-energy limiting  [[11-dimensional supergravity]] this is KK-compactification to [[3d supergravity]].

Typically this is considered with a [[reduction of the structure group]] on the compactification fiber from [[Spin(8)]] to [[Spin(7)]], in which case one speaks of _M-theory on [[Spin(7)-manifolds]]_. Further reduction to [[G2-structure]] yields [[M-theory on G2-manifolds]].


## Properties

### C-field tadpole cancellation condition

In [[M-theory]] [[KK-compactification|compactified]]  [[compact topological space|compact]] [[8-manifold]] [[fibers]],  [[tadpole cancellation]] for the [[supergravity C-field]] (see also at _[[C-field tadpole cancellation]]_) is equivalently the condition

$$
  N_{M2}
  \;+\;
  \tfrac{1}{2} \big( G_4[X^{(8)}]\big)^2
  \;=\;
  \underset{
    I_8(X^8)
  }{
    \underbrace{
      \tfrac{1}{48}\big( p_2 - \tfrac{1}{2}p_1^2  \big)[X^{8}]
    }
  }
  \;\;\;\;
  \in
  \mathbb{Z}
  \,,
$$

where

1. $N_{M2}$ is the net number of [[M2-branes]] in the spacetime (whose [[worldvolume]] appears as points in $X^{(8)}$);

1. $G_4$ is the [[field strength]]/flux of the [[supergravity C-field]]

1. $p_1$ is the [[first Pontryagin class]] and $p_2$ the [[second Pontryagin class]] combining to [[I8]], all regarded here in [[rational homotopy theory]].

If $X^{8}$ has 

* [[Spin(7)-structure]] (hence in particular if it is a [[Calabi-Yau manifold]], which has $SU(4) = $ [[Spin(6)]]-structure) 

or 

* [[Spin(3) x Spin(5)-structure]] 

then

$$
  \tfrac{1}{2}\big( p_2 - \tfrac{1}{4}(p_1)^2  \big)
  \;=\;
  \chi
$$

is the [[Euler class]] (see [this Prop.](Spin7-manifold#CharacteristicClassesForSpinStructure) and [this Prop.](quaternion-Kähler+manifold#CharacteristicClassesForSpin5Spin3Structure), respectively), hence in these cases the condition is equivalently

$$
  N_{M2}
  \;+\;
  \tfrac{1}{2} \big( G_4[X^{(8)}]\big)^2
  \;=\;
  \tfrac{1}{24}\chi[X^8]
  \;\;\;\;
  \in
  \mathbb{Z}
  \,,
$$

where $\chi[X]$ is the [[Euler characteristic]] of $X$.

For references see [there](C-field+tadpole+cancellation#References).

\linebreak

### Relation to F-theory 
 {#RelationToFTheory}

If the 8-dimensional [[fibers]] themselves are [[elliptic fibrations]], then [[M-theory]] on these 8-manifolds this is supposedly [[T-duality|T-dual]] to [[F-theory]] [[KK-compactification|KK-compactified]] to $3+1$ [[spacetime]]-[[dimensions]]. 

In particular, if there is an [[M2-brane]] [[wrapped brane|filling]] the base 2+1-dimensional spacetime, this is supposedly [[T-duality|T-dual]] to a 3+1-dimensional spacetime filling [[D3-brane]] in [[F-theory]] (e.g. [Condeescu-Micu-Palti 14, p. 2](#CondeescuMicuPalti14))

For more on this see at _[[F/M-theory on elliptically fibered Calabi-Yau 4-folds]]_.

\linebreak

### Black M2-branes and Exotic 7-spheres
 {#BlackM2BranesAndExotic7Spheres}

The discovery of [[exotic 7-spheres]] proceeded via [[8-manifolds]] $X$ [[manifold with boundary|with boundary]] [[homeomorphism|homeomorphic]] to the [[7-sphere]] $\partial X \simeq_{homeo} S^7$, but not necessarily [[diffeomorphism|diffeomorphic]] to $S^7$ with its canonical [[smooth structure]] (for more see [there](8-manifold#ExoticBoundary7Spheres)).

Hence when regarded from the point of view of [[M-theory on 8-manifolds]], exotic 7-spheres arise as [[near horizon limits]] of peculiar [[black brane|black]] [[M2-brane]] [[spacetimes]] $\mathbb{R}^{2,1} \times X$.

See also [Morrison-Plesser 99, section 3.2](#MorrisonRPlesser99).


## Related concepts

* [[M-theory on G2-manifolds]]

* [[F/M-theory on elliptically fibered Calabi-Yau 4-folds]]

## References

### General

* {#Witten95} [[Edward Witten]], _Strong Coupling and the Cosmological Constant_, Mod.Phys.Lett.A10:2153-2156, 1995 ([arXiv:hep-th/9506101](https://arxiv.org/abs/hep-th/9506101))

  (on possible relation to the [[cosmological constant]])

* [[Katrin Becker]], [[Melanie Becker]], _M-Theory on Eight-Manifolds_, Nucl.Phys. B477 (1996) 155-167 ([arXiv:hep-th/9605053](https://arxiv.org/abs/hep-th/9605053))

* [[Savdeep Sethi]], [[Cumrun Vafa]], [[Edward Witten]], _Constraints on Low-Dimensional String Compactifications_, Nucl.Phys.B480:213-224, 1996 ([arXiv:hep-th/9606122](https://arxiv.org/abs/hep-th/9606122))

* {#GukovSparks02} [[Sergei Gukov]], James Sparks, _M-Theory on $Spin(7)$ Manifolds_, Nucl.Phys. B625 (2002) 3-69 ([arXiv:hep-th/0109025](https://arxiv.org/abs/hep-th/0109025))

* [[Sergei Gukov]], James Sparks, David Tong, _Conifold Transitions and Five-Brane Condensation in M-Theory on $Spin(7)$ Manifolds_, Class.Quant.Grav.20:665-706, 2003 ([arXiv:hep-th/0207244](https://arxiv.org/abs/hep-th/0207244))

* [[Dimitrios Tsimpis]], _M-theory on eight-manifolds revisited: N=1 supersymmetry and generalized $Spin(7)$ structures_, JHEP 0604 (2006) 027 ([arXiv:hep-th/0511047](https://arxiv.org/abs/hep-th/0511047))

* {#CondeescuMicuPalti14} Cezar Condeescu, Andrei Micu, Eran Palti, _M-theory Compactifications to Three Dimensions with M2-brane Potentials_, JHEP04(2014)026 ([arXiv:1311.5901](https://arxiv.org/abs/1311.5901))

* Daniël Prins, [[Dimitrios Tsimpis]], _IIA supergravity and M-theory on manifolds with SU(4) structure_, PhysRevD.89.064030 ([arXiv:1312.1692](https://arxiv.org/abs/1312.1692))

* [[Mariana Graña]], C. S. Shahbazi, [[Marco Zambon]], _$Spin(7)$-manifolds in compactifications to four dimensions_, JHEP11(2014)046 ([arXiv:1405.3698](http://arxiv.org/abs/1405.3698))

* Elena Mirela Babalic, [[Calin Lazaroiu]], _Foliated eight-manifolds for M-theory compactification_, JHEP01(2015)140 ([arXiv:1411.3148](https://arxiv.org/abs/1411.3148))

* C. S. Shahbazi, _M-theory on non-Kähler manifolds_, JHEP09(2015)178 ([arXiv:1503.00733](https://arxiv.org/abs/1503.00733))

* Elena Mirela Babalic, [[Calin Lazaroiu]], _The landscape of G-structures in eight-manifold compactifications of M-theory_, JHEP11 (2015) 007 ([arXiv:1505.02270](https://arxiv.org/abs/1505.02270))

* Elena Mirela Babalic, [[Calin Lazaroiu]], _Internal circle uplifts, transversality and stratified G-structures_, JHEP11(2015)174 ([arXiv:1505.05238](https://arxiv.org/abs/1505.05238))

### M2-brane spacetimes

* {#MorrisonPlesser99} [[David Morrison]], [[M. Ronen Plesser]], section 3.2 of _Non-Spherical Horizons, I_, Adv.Theor.Math.Phys.3:1-81, 1999 ([arXiv:hep-th/9810201](https://arxiv.org/abs/hep-th/9810201))


[[!redirects M-theory on Spin(7)-manifolds]]
