
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of  _monomorphism_ is the generalization of the notion of _injective map of  sets_ from the [[category]] [[Set]] to arbitrary [[category|categories]].

## Definition

A **monomorphism** in a [[category]] $C$ is a [[morphism]] $f : X \to Y$ such that, equivalently,

* $f$ is an [[epimorphism]] in the [[opposite category]] $C^{op}$.

* for any object $A$ the induced morphism $f_* : C(A,X) \to C(A,Y)$ is injective.

The last condition here states the usual arrow-theoretic way to say monomorphism:

The morphism $f : X \to Y$ is mono precisely if for all $g,h  : A \to X$ such that $f_*(h) : A \stackrel{h}{\to} X \stackrel{f}{\to}Y $ equals
$f_*(g) : A \stackrel{g}{\to} X \stackrel{f}{\to}Y $ we have $g = h$.

## Properties

We list the following properties without their (easy) proof. The proofs can be found spelled out (dually) at [[epimorphism]].

+-- {: .num_prop}
###### Proposition

Every [[equalizer]]

$$
  t \to x \stackrel{\longrightarrow}{\longrightarrow} y 
$$

is a monomorphism.

=--


+-- {: .num_prop}
###### Proposition

Monomorphisms are preserved by [[pullback]].

=--


+-- {: .num_prop}
###### Proposition

Monomorphisms are preserved by [[right adjoint]] [[functors]].

=--

+-- {: .num_prop}
###### Proposition

Monomorphisms are [[reflected limit|reflected]] by [[faithful functors]].

=--



## Variations

At [epimorphism](/nlab/show/epimorphism#Variations) there is a long list of variations on the concept of epimorphism.  Each of these, of course, has a dual notion for monomorphism, but the ones most commonly used are:

* [[split monomorphism]] = morphism which has a [[retraction]]
* [[normal monomorphism]] = a [[kernel]] of some morphism (in a category with [[zero morphisms]])
* [[regular monomorphism]] = an [[equalizer]] of some [[parallel pair]]
* [[strong monomorphism]] = a monomorphism [[orthogonality|right orthogonal]] to [[epimorphisms]]
* monomorphism

Frequently, regular and strong monics coincide.  For instance, this is the case in any [[quasitopos]], and also in [[Top]], where they are the subspace inclusions (the plain monomorphisms are the injective functions).

Sometimes, all monomorphisms are regular---this seems to happen a bit more frequently than for epimorphisms.  For instance, this is the case in any [[pretopos]] (including any [[topos]], such as [[Set]]), but also in any [[abelian category]], and also in the category [[Grp]].

In [[Ab]] and in any [[abelian category]], all monomorphisms are normal.  But this is not so in [[Grp]], where (despite the fact that all monomorphisms are regular), the normal monics are the inclusions of [[normal subgroups]] (hence the name).  In any [[Ab-enriched category]], all regular monics are normal, but not all monics need be regular.

In a [[Boolean topos]], such as [[Set]] (in [[classical mathematics]]), any monomorphism with [[inhabited set|inhabited]] domain is split.  Of course, no monic with empty domain and inhabited codomain can be split (in contrast to the dual case, where it can happen that all epimorphisms split -- the [[axiom of choice]]).


## Related concepts 

* [[isomorphism]] classes of monomorphism define [[subobject]]s.

* [[monomorphism in an (∞,1)-category]], [[n-monomorphism]]

* [[image]], [[coimage]]

[[!redirects monomorphisms]]
[[!redirects monic]]
[[!redirects monics]]
[[!redirects mono]]
[[!redirects monos]]
[[!redirects Monomorphism]]
[[!redirects Monomorphisms]]
[[!redirects Monic]]
[[!redirects Monics]]
[[!redirects Mono]]
[[!redirects Monos]]
