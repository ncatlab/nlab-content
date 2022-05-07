
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


## Definition

### In 1-category theory
 {#In1CategoryTheory}


A [[functor]] $F \colon \mathcal{C} \to \mathcal{D}$ from a [[category]] $\mathcal{C}$ to a category $\mathcal{D}$ is called _faithful_, if for each [[pair]] of [[objects]] $x, y \in \mathcal{C}$, its [[function]] $F_{x,y}$ on [[hom-sets]] is [[injection|injective]]:

$$
  \array{
    \mathcal{C}(x,y) 
    &\xhookrightarrow{\;\; F_{x,y} \;\;}&
    \mathcal{D}(F(x), F(y))
    \\
    (x \overset{\phi}{\to} y)
    &\mapsto&
    \big(
      F(x)\overset{F(\phi)}{\to} F(y)
    \big)
    \,.
  }
$$

More abstractly, we may say that a functor is faithful if it is $2$-[[k-surjective functor|surjective]] &#8211; or loosely speaking, 'surjective on equations between given morphisms'. 



### In higher category theory
 {#InHigherCategoryTheory}

See also _[[faithful morphism]]_ for a generalization to an arbitrary [[2-category]].

And see [[0-truncated morphism of an (∞,1)-category|0-truncated morphism]] for generalization to [[(∞,1)-categories]] (see <a href="n-truncated+object+of+an+(infinity,1)-category#TruncatedMorphismsBetweenGroupoids">there</a>).

+-- {: .num_remark }
###### Warning

This generalization is about extending to morphisms in general (∞,1)-categories the fact that in $\infty{}Grpd$, $0$-truncated morphisms give a reasonable notion of faithful functor.

In particular, the notion of a "faithful morphism in the (∞,1)-category of (∞,1)-categories" does _not_ give the right notion of a "faithful functor between (∞,1)-categories".

=--

## Properties

+-- {: .num_prop }
###### Proposition

A faithful functor [[reflected limit|reflects]] [[epimorphisms]] and [[monomorphisms]].

=--

(The simple proof is spelled out for instance at _[[epimorphism]]_.)


## Related concepts

* [[embedding of categories]]

[[!include properties of functors -- contents]]




[[!redirects faithful]]
[[!redirects faithful functors]]
