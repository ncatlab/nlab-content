
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

This is the generalization of the notion of *[[ends]]* from [[category theory]] to [[(∞,1)-category theory]].

## Definition

### End of a space-valued functor

Given an [[(∞,1)-functor]] $F \colon J^{op} \times J \to \infty Gpd$ to [[∞Groupoids]] from the [[product category|product]] of a [[locally small (∞,1)-category]] $J$ with its [[opposite (∞,1)-category]], we define its *end* to be the [[(∞,1)-categorical hom-space]] in the [[(∞,1)-category of (∞,1)-functors]] from the [[hom-functor]] of $J$ to $F$:

$$ 
  \int_J F 
    \coloneqq
  \infty Gpd^{J^{op} \times J}
  \big( 
    J(-,-), F(-,-) 
  \big)
$$


### Ends and coends as a weighted (co)limit

More generally, given an [[(∞,1)-functor]] $F \colon J^{op} \times J \to C$ to [[∞Groupoids]] to any [[locally small (∞,1)-category]] $C$,
we define its (co)end, when it exists, as the (co)[[representing object]] of

$$ 
  C\left(c, \int_J F \right) 
   \simeq
  \int_J C(c, F) 
    \simeq
  \infty Gpd^{J^{op} \times J}
  \big( 
    J(-,-), C(c, F(-,-)) 
  \big)
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
###### Proposition (Fubini)

Given a functor $F : J^\op \times J \times K^\op \times K \to C$, if the relevant ends/coends exist, we have natural equivalences
$$
\int_J \int_K F \simeq \int_{J \times K} F
\qquad \qquad
\int^J \int^K F \simeq \int^{J \times K} F
$$

=--
+-- {: .proof}
###### Proof 
For ends, using the fact $Tw$ preserves products we can compute
$$
  \begin{aligned}
  \int_J \int_K F
   &\simeq \lim_{j \to j' \in Tw(J)} \lim_{k \to k' \in Tw(K)} F(j,j',k,k')
   \\&\simeq \lim_{(j,k) \to (j',k') \in \Tw(J \times K)} F(j,j',k,k')
   \\&\simeq \int_{J \times K} F
  \end{aligned}
$$
The same argument applies for coends.
=--

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