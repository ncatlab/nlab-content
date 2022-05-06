
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

The notion of  _monomorphism_ is the generalization of the notion of _injective map of sets_ from the [[category]] [[Set]] to arbitrary [[category|categories]].

The [[formal duality|formally dual]] concept is that of _[[epimorphism]]_, which similarly generalizes (or strengthens) the concept of [[surjective function]].

Common jargon includes "is a mono" or "is monic" for "is a monomorphism", and "is an epi" or "is epic" for "is an epimorphism", and "is an iso" for "is an isomorphism".
 
## Definition

A [[morphism]] $f \colon X \to Y$ in some [[category]] is called a _monomorphism_ (sometimes abbrieviated to _mono_, or described as being _monic_), if for every [[object]] $Z$ and every [[pair of parallel morphisms]] $g_1,g_2 \colon Z \to X$ then

$$
  \left(
    f \circ g_1
    \,=\,
    f \circ g_2
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

Since injective functions are precisely the monomorphisms in [[Set]] (example \ref{MonomorphismsInSet} below) this may be stated as saying that $f$ is a monomorphism if $Hom(Z,f)$ is a monomorphism for all objects $Z$. 

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

The following are equivalent

* $f : x \to y$ is an monmorphism in $C$;

* $f$ is an [[epimorphism]] in the [[opposite category]] $C^{op}$;

* for all $z$, $Hom(z,f)$ is a [[monomorphism]] in [[Set]] -- an [[injection]];

* the [[commuting diagram]] 
  $$
    \array{
      x &\stackrel{Id}{\to}& x
      \\
      {}^{Id}\downarrow && \downarrow^{f}
     \\
     x &\underset{f}{\to}& y
    }
  $$

  is a [[pushout]] diagram.

=--


+-- {: .num_prop}
###### Proposition

If $f \colon x \to y$ and $g \colon y \to z$ are monomorphisms, so is their composite $g f$.  If $g f$ is an monomorphism, so is $f$.

=--

+-- {: .num_prop}
###### Proposition

Every [[equalizer]]

$$
  t \to x \stackrel{\longrightarrow}{\longrightarrow} y 
$$

is a monomorphism.

=--

The converse of the above proposition fails, and a mononomorphism that is the equalizer of some pair of morphisms is called a [[regular monomorphism]].


+-- {: .num_prop}
###### Proposition

Monomorphisms are preserved by [[pullback]].

=--


+-- {: .num_prop}
###### Proposition

Monomorphisms are preserved by any [[right adjoint]] [[functor]], or more generally any functors that preserves pullbacks.

=--

The reason is that that a monomorphism is a morphism $f: X \to Y$ whose pullback along itself is $X$.

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

Frequently, regular and strong monos coincide.  For instance, this is the case in any [[quasitopos]], and also in [[Top]], where they are the subspace inclusions (the plain monomorphisms are the injective functions).

Sometimes, all monomorphisms are regular---this seems to happen a bit more frequently than for epimorphisms.  For instance, this is the case in any [[pretopos]] (including any [[topos]], such as [[Set]]), but also in any [[abelian category]], and also in the category [[Grp]].

In [[Ab]] and in any [[abelian category]], all monomorphisms are normal.  But this is not so in [[Grp]], where (despite the fact that all monomorphisms are regular), the normal monos are the inclusions of [[normal subgroups]] (hence the name).  In any [[Ab-enriched category]], all regular monos are normal, but not all monos need be regular.

In a [[Boolean topos]], such as [[Set]] (in [[classical mathematics]]), any monomorphism with [[inhabited set|inhabited]] domain is split.  Of course, no mono with empty domain and inhabited codomain can be split (in contrast to the dual case, where it can happen that all epimorphisms split -- the [[axiom of choice]]).


## Related concepts 

* [[isomorphism]] classes of monomorphism define [[subobject]]s.

* [[monomorphism in an (∞,1)-category]], [[n-monomorphism]]

* [[image]], [[coimage]]

* a category in which all morphisms are monomorphisms is called a _[[left cancellative category]]_

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
