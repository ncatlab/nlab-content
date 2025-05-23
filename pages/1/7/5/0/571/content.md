
> This entry is about the basic notion of "monic" in relation to [[morphisms]] in [[category theory]]. For the notion of "monic" in relation to [[polynomials]] in [[commutative algebra]], see at _[[monic polynomial]]_. 

***

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

### General

+-- {: .num_example}
###### Example
**(monomorphisms in preorders)

In a [[preorder]], all arrows are mono because they satisfy the required condition vacuously (any pair of parallel arrows is equal in a preorder).

=--

+-- {: .num_example #MonomorphismsInSet}
###### Example
**(monomorphisms in $Set$)

The monomorphisms in the category [[Set]] of [[sets]] and [[functions]] between them are precisely the [[injective functions]].

=--

+-- {: .num_example #MonomorphismsInCat}
###### Example
**(monomorphisms in $Cat$)

The monomorphisms in the category [[Cat]] of [[categories]] and [[functors]] between them are precisely the [[embeddings of categories]], i.e. the [[injective-on-objects functor|injective-on-objects]] [[faithful functors]].

=--

+-- {: .num_example}
###### Example

Every [[isomorphism]] is both a monomorphism and an [[epimorphism]]. 

=--

But beware that the converse fails:


### Examples of monos that are epi but not iso
 {#ExamplesOfMonosThatAreEpiButNotIso}

The following lists some examples of [[morphisms]] that are both [[monomorphisms]] and [[epimorphisms]], but not necessarily [[isomorphisms]].

\begin{example}

In the [[category]] of [[Hausdorff topological spaces]], the inclusion $A \hookrightarrow X$ of a [[dense subspace]] is an [[epimorphism]].

\end{example}

See [this Prop.](Hausdorff+space#DenseSubspaceInclusionsAreEpimorphismsAmongHausdorffSpaces) for proof.

\begin{example}
  
In [[unital ring|unital]] [[Rings]], the canonical inclusion $\mathbb{Z} \overset{i}{\hookrightarrow} \mathbb{Q}$ of the [[integers]] into the [[rational numbers]] is an [[epimorphism]].

\end{example}

See [this Prop.](Ring#InclusionOfIntegersIntoRationalsIsEpimorphismOfRings) for proof.


## Properties

We list the following properties without their (easy) proofs. The proofs can be found spelled out (dually) at [[epimorphism]].


\begin{prop}\label{BasicCharacterizationOfMonomorphisms}
The following are equivalent:

* $f : x \to y$ is a monomorphism in $C$;

* $f$ is an [[epimorphism]] in the [[opposite category]] $C^{op}$;

* postcomposition with $f$ is a [[monomorphism]] in [[Set]]: that is, for all $c \in C$, $f \circ -: Hom(c,x) \to Hom(c,y)$ is an [[injection]];

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

  is a [[pullback]] diagram.

\end{prop}


+-- {: .num_prop}
###### Proposition

If $f \colon x \to y$ and $g \colon y \to z$ are monomorphisms, so is their composite $g f$.  If $g f$ is a monomorphism, so is $f$.

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


+-- {: .num_prop #MonomorphismsArePreservedByPullback}
###### Proposition

Monomorphisms are preserved by [[pullback]].

=--

(In an [[adhesive category]] they are also preserved by [[pushout]].)


+-- {: .num_prop}
###### Proposition

Monomorphisms are preserved by any [[right adjoint]] [[functor]], or more generally any functors that preserves pullbacks.

=--


+-- {: .num_prop}
###### Proposition

Monomorphisms are [[reflected limit|reflected]] by [[faithful functors]].

=--

We have seen some ways in which monomorphisms get along with limits.  Here is another:

+-- {: .num_prop}
###### Proposition

Any morphism from a terminal  object is a monomorphism.  The product of monomorphisms is a monomorphism.
=--


Monomorphisms do not get along quite as well with colimits.  For example, the unique morphism from the initial object is not always a monomorphism, and the canonical morphisms from the summands into a coproduct, e.g. $i_1 : x_1 \to x_1 + x_2$, are not always monomorphisms (though these results do hold in $Set$). However, the unique morphism from the initial object is a monomorphism when the initial object is [[strict initial object|strict]], and the canonical morphisms into a coproduct are monomorphisms when the coproduct is a [[disjoint coproduct]]. 


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

* [[isomorphism]] classes of monomorphism define [[subobject|subobjects]].

* [[monomorphism in an (∞,1)-category]], [[n-monomorphism]]

* [[image]], [[coimage]]

* a category in which all morphisms are monomorphisms is called a _[[left cancellative category]]_

* [[jointly monic morphisms]]

## References

Textbook accounts:

* [[Saunders MacLane]], §I.5 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


* [[Francis Borceux]], Section 1.7 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory* &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;


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
