#Contents#

* automatic table of contents goes here
{: toc}

#Idea#

A _scheme_ is a [[space]] that _locally_ looks like a particularly simple [[ringed space]]: an [[affine scheme]].
This can be formalised either within the category of [[locally ringed spaces]] or within the category of presheaves of sets on the category of affine schemes $Aff$.

The notion of scheme originated in [[algebraic geometry]] where it is, since [[Grothendieck]]'s revolution of that subject, a central notion. 

However, the idea that

+-- {: .standout}

A scheme is a ringed space that is locally isomorphic to an affine space.

=--

is much more general and need not be restricted to a notion of affine spaces that are [[duality|formal duals]] of rings.
But then one talks about locally affine *spaces*. 

+--{.query}
Zoran: this gives wrong impression that Grothendieck school was working with ringed spaces and not functor of points. This is true for EGA but not for most of works of Grothendieck school. The things about generalization called locally affine space should go under [[locally affine space]] and under [[functor of points] and not here. There is also redundancy in new text. 
=--

For instance a smooth [[manifold]] is a ringed space that is locally isomorphic to a "smooth affine space" $\mathbb{R}^n$, with its standard smooth structure.

The standard concept of scheme in [[algebraic geometry]] is therefore usefully understood as a special case of [[generalized scheme]]s that naturally appear for instance also in [[differential geometry]], in [[synthetic differential geometry]] and many other topics.


# Definition #

## As locally ringed spaces ##

A __scheme__ is a [[locally ringed space]] $(X, \mathcal{O}_X)$ with an open cover (as locally ringed spaces), by [[affine scheme]]s: the spectra $Spec A = (|Spec A|, \mathcal{O}_{Spec A})$ of unital commutative [[ring]]s.

A morphism $f : X \to Y$ of schemes is a morphism of the underlying [[ringed space]]s, such that for each point $x \in X$ the induced map of [[local ring]]s

$$
  (\mathcal{O}_Y)_{f(x)} \to  (\mathcal{O}_X)_x
$$

is _local_ (in that it carries the maximal ideal to the maximal ideal). See [[functor of points]].

+--{.query}
Zoran: This is superfluous: the definition of morphisms in the category of LOCALLY ringed spaces already asks for this condition, one does not need to introduce that as late as when introducing schemes. 
=--

[[Jacob Lurie]] argues that underlying locale point of view is better than underlying topological space point of view, see [[schemes as locally affine structured (∞,1)-toposes]].


## Functor of points approach: as sheaves on $CRing^{op}$ ##

The fundamental theorem on morphisms of schemes is a [[fully faithful functor]] from the category of schemes to the category of [[presheaf|presheaves]] on $Aff = CRing^{op}$ 
which sends $(X, \mathcal{O}_X)$ to the functor

$$
 h_X|_{Aff} : A \mapsto Hom_{Schemes}(Spec A , (X, \mathcal{O}_X))
  \,.
$$

This identifies schemes with those presheaves on [[CRing]]${}^{op}$ that

1. are [[sheaf|sheaves]] with respect to the Zariski [[Grothendieck topology]] on $CRing^{op}$;
2. have a [[cover]] by Zariski-open immersions of [[affine scheme]]s in the category of presheaves over $Aff$.

The standard reference for the functor-of-points approach to schemes is 

* M. Demazure, P. Gabriel, _Groupes algebriques_, tome 1 (later volumes never appeared), Mason and Cie, Paris 1970


#Generalizations#

In [[algebraic geometry]] this is a basic object of study, since the revolution of [[Grothendieck]]. There are generalizations like [[relative schemes]] (which are just objects in a [[slice category]] $Sch/S$), relative schemes in [[noncommutative algebraic geometry]] introduced by A. Rosenberg in terms of categories and covers defined using pairs of [[adjoint functors]], the generalized schemes of [[Nikolai Durov]], the [[algebraic stack]]s of [[Deligne-Mumford stack|Deligne-Mumford]] and Artin, the dg-schemes of Kapranov, the [[derived scheme]]s of [[Jacob Lurie]], the higher [[algebraic stack]]s of [[Bertrand Toen|Toën]]--Vezzosi, almost schemes (Ofer Gabber and Lorenzo Ramero), formal schemes (Cartier--Grothendieck), [[locally affine spaces]] in the fpqc, fppf or &#233;tale topology (Grothendieck), [[algebraic spaces]], etc. 

See also [wikipedia](http://en.wikipedia.org/wiki/Scheme_%28mathematics%29). [[EGA]] says prescheme, for what we call algebraic scheme, and says scheme for what we call [[separated scheme]].


#References#

A useful quick introduction that presents the concept in the light of its higher categorical generalizations is at the beginning of 

* [[Paul Goerss]], [[Topological Algebraic Geometry - A Workshop]]


[[!redirects schemes]]
[[!redirects algebraic scheme]]
[[!redirects algebraic schemes]]