
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
{: toc}

## Idea

This is the generalization of [[end]] to (∞,1)-categories.

## Definition

### End of a space-valued functor

Given a functor $F : J^{op} \times J \to \infty Gpd$, we define the end to be

$$ 
  \int_J F \simeq\infty Gpd^{J^{op} \times J}( J(-,-), F(-,-) )
$$


### Ends and coends as a weighted (co)limit

Let $F : J^{op} \times J \to C$ be a functor between locally small (∞,1)-categories.
We define the (co)end, when it exists, as (co)representing object of

$$ 
  C\left(c, \int_J F \right) \simeq
  \int_J C(c, F) \simeq
  \infty Gpd^{J^{op} \times J}( J(-,-), C(c, F(-,-)) )
$$
$$ 
  C\left(\int^J F, c \right) \simeq
  \int_{J^{op}} C(F, c) \simeq
  \infty Gpd^{J \times J^{op}}( J^{op}(-,-), C(F(-,-), c) )
$$

When $C = \infty Gpd$, this definition agrees with the previous.

### As (co)limits over the twisted arrow category

Let $F : J^{op} \times J \to C$ be a functor between (∞,1)-categories.
We can express the (co)end as (co)limits over the [[twisted arrow (∞,1)-category]] by

$$
  \int_J F \simeq \lim \left( Tw(J) \xrightarrow{(src, tgt)} J^{op} \times J
  \xrightarrow{F} C \right)
$$
$$
  \int^J F \simeq \colim \left( Tw(J^{op})^{op} \xrightarrow{(src, tgt)}  J^{op} \times J
  \xrightarrow{F} C \right) 
$$

The second of these, for example, follows from the fact the projection
$p : Tw(J^{op}) \to J \times J^{op}$ is the left fibration classified by $J^{op}(-,-)$, and so we can write the hom-functor as the left Kan extension $p_!(1) = J^{op}(-,-)$ and take an adjoint transpose.

## Properties


+-- {: .num_prop }
###### Proposition

Given functors $F,G : X \to Y$ between two (∞,1)-categories, the space of natural transformations between them is given by the end

$$ Y^X(F, G) \simeq \int_{x \in X} Y(F(x), G(x)) $$
=--

This is proposition 5.1 of [Gepner-Haugseng-Nikolaus 15](#GepnerHaugsengNikolaus15).


## Related concepts

* [[twisted arrow (∞,1)-category]]
* [[lax (∞,1)-colimit]]

#References

* {#GepnerHaugsengNikolaus15} [[David Gepner]], [[Rune Haugseng]], [[Thomas Nikolaus]], _Lax colimits and free fibrations in $\infty$-categories_ ([arXiv:1501.02161](http://arxiv.org/abs/1501.02161))


[[!redirects (∞,1)-ends]]
[[!redirects (∞,1)-coend]]
[[!redirects (∞,1)-coends]]