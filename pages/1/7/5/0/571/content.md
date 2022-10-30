
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

The [[formal duality|formally dual]] concept is that of _[[epimorphism]]_, which similarly generalizes (or strengthens) the concept of [[surjective function]].
 
## Definition

A [[morphism]] $f \colon X \to Y$ is some [[category]] is called a _monomorphism_ if for every [[object]] $Z$ and every [[pair of parallel morphisms]] $g_1,g_2 \colon Z \to X$ then

$$
  \left(
    g_1 \circ f
    \,=\,
    g_2 \circ f
  \right)
  \;\Rightarrow \;
  \left(
    g_1 \,=\, g_2
  \right)
  \,.
$$

Stated more abstractly, this says that $f$ is a monomorphism if for every $Z$ the [[hom-functor]] $Hom(Z,-)$ takes it to an [[injective function]] between [[hom-sets]]

$$
  Hom(Z,X) 
    \overset{\phantom{AA} f_\ast \phantom{AA}}{\hookrightarrow} 
  Hom(Z,Y)
  \,.
$$

Since injective functions are precisely the monomorphisms in [[Set]] (example \ref{MonomorphismsInSet} below) this may be stated as saying that $f$ is a monomorphisms if for all objects $Z$ then $Hom(Z,f)$ is a monomorphisms. 

Finally, $f$ being a monomorphism in a [[category]] $\mathcal{C}$ means equivalently that it is an [[epimorphism]] in the [[opposite category]] $\mathcal{C}^{op}$.

## Examples

+-- {: .num_example #MonomorphismsInSet}
###### Example
**(monomorphisms in $Set$)

The monomorphisms in the category [[Set]] of [[sets]] and [[functions]] between them are precisely the [[injective functions]].

=--

+-- {: .num_example}
###### Example

Every [[isomorphism]] is both a monomorphism and an [[epimorphism]]. 

=--

But beware that the converse fails:

+-- {: .num_example}
###### Example

A morphism that is both a monomorphism and an [[epimorphism]] need not be an [[isomorphism]].

For instance in the categories [[Ring]] or [[CRing]], then the defining inclusion $\mathbb{Z} \hookrightarrow \mathbb{Q}$ of the ring of [[integers]] into that of [[rational numbers]] is both a monomorphism and an epimorphism, but clearly not an isomorphism.

=--


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
