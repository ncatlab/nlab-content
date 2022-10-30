
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The **odd line** is the [[supermanifold]] $\mathbb{R}^{0|1}$ -- a [[super Cartesian space]] and in particular a [[superpoint]]  -- characterized by the fact that its $\mathbb{Z}_2$-graded algebra of functions is the algebra free on a single odd generator $\theta$: $C^\infty(\mathbb{R}^{0|1}) = \mathbb{R}[\theta] = \mathbb{R} \oplus \theta\cdot \mathbb{R}$.

This algebra is essentially the [[ring of dual numbers]], but with the single generator in odd degree.

## Properties

### The automorphism super-group
 {#TheAutomorphismSuperGroup}

The internal [[automorphism group]] of the odd line in the [[topos]] of [[smooth super infinity-groupoids|smooth super spaces]] is the [[supergroup]]

$$
  \mathbf{Aut}(\mathbb{A}^{0|1})
  \simeq
  \mathbb{G}_m \ltimes (\Pi \mathbb{G}_{ad})
$$

which is the [[semidirect product group]] of the [[multiplicative group]] (the [[group of units]], hence $\mathbb{R}^\times$ when working over the real numbers) with the [[additive group]] shifted into odd degree. (See at _[References -- Automorphism group](#ReferencesAutomorphismGroup)_ for the origin of this observation.)

In the [[topos]] over [[superpoints]] $\mathbb{R}^{0|q}$ this is seen over the test space $\mathbb{R}^{0|1}$ itself with canonical odd coordinate $\theta$ by taking the canonical odd coordinate of the odd line that we are taking automorphism of to be $\epsilon$ and observing that maps

$$
  \mathbb{R}^{0|1} \to \mathbf{Aut}(\mathbb{R}^{0|1})
$$

are then given, under the [[evaluation map]]-isomorphism and via the [[Yoneda lemma]] by [[Grassmann algebra]] [[homomorphisms]] of the form

$$
  \langle \epsilon, \theta\rangle
  \leftarrow
   \langle \epsilon\rangle
$$

that send

$$
  \epsilon \mapsto x \epsilon + y \theta
$$

with $x \neq 0$ in even degree and arbitrary $y$ in odd degree. Notice that the [[inverse]] of this map exists and is given by

$$
  \epsilon \mapsto x^{-1}\epsilon - y x^{-1} \theta
  \,.
$$

Moreover, observe that an [[action]] of $\mathbf{Aut}(\mathbb{R}^{0|1})$ on a [[supermanifold]] corresponds to a choice of [[graded object|grading]] and a choice of [[differential]]. A clean account of this statement is in ([Carchedi-Roytenberg 12](#CarchediRoytenberg12)). (At least for the grading this is essentially the classical statement about graded rings, see at _[[affine line]]_ the section  _[Properties -- Grading](affine+line#Grading)_).

## Related concepts

* [[Cartesian space]]

* [[infinitesimal space]]

* [[synthetic differential supergeometry]]


## References

### Automorphism group
 {#ReferencesAutomorphismGroup}

That an action of the endomorphism/automorphism supergroup of the odd line on a supermanifold is equivalent to a choice of grading and a [[differential]] first observed in

* {#Kontsevich97} [[Maxim Kontsevich]], _Deformation quantization of Poisson manifolds, I_, Lett. Math. Phys. 66:157-216,2003 ([arXiv:q-alg/9709040](http://arxiv.org/abs/q-alg/9709040))

It was later amplified in section 3.2 of

* {#KochanSevera03} Denis Kochan, [[Pavol Ševera]], _Differential gorms, differential worms_ ([arXiv:math/0307303](http://arxiv.org/abs/math/0307303)),

where it is used to exhibit the canonical [[de Rham differential]] action on the [[odd tangent bundle]] $Maps(\mathbb{R}^{0|1}, X)$ of a [[supermanifold]] $X$.

The same mechanism is amplified further in the discussion of [[derived differential geometry]] in 

* [[David Carchedi]], [[Dmitry Roytenberg]], _Homological Algebra for Superalgebras of Differentiable Functions_ ([arXiv:1212.3745](http://arxiv.org/abs/1212.3745))
 {#CarchediRoytenberg12}

An interpretation of an $\mathbb{G}_m \ltimes \Pi \mathbb{G}_{ad}$-[[action]] on a [[supermanifold]] of local [[quantum observables]] of a [[supersymmetry|supersymmetric]] [[field theory]] as the formalization of the concept of [[topologically twisted super Yang-Mills theory]] is in section 15 of 

* [[Kevin Costello]], _Notes on supersymmetric and holomorphic field theories in dimensions 2 and 4_ ([arXiv:1111.4234](http://arxiv.org/abs/1111.4234))

For more on this see at _[topologically twisted super Yang-Mills theory -- Formalization](topologically+twisted+D%3D4+super+Yang-Mills+theory#Formalization)_.

