
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory - contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A [[functor]] $F: \mathcal{A} \to \mathcal{B}$ between [[additive category|additive categories]] is itself called __additive__ if it preserves finite [[biproducts]].

That is, 

1. $F$ maps a [[zero object]] to a zero object, $F(0) \simeq 0 \in \mathcal{B}$; 

1. given any two [[objects]] $x, y \in \mathcal{A}$, there is an [[isomorphism]] $F(x \oplus y) \cong F(x) \oplus F(y)$, and this respects the inclusion and projection maps of the [[direct sum]]:

$$
\array { x &          &            &          & y \\
           & {}_{\mathllap{i_x}}\searrow &            & \swarrow_{\mathrlap{i_y}} \\
           &          & x \oplus y \\
           & {}^{\mathllap{p_x}}\swarrow &            & \searrow^{\mathrlap{p_y}} \\
         x &          &            &          & y }
\quad\quad\stackrel{F}{\mapsto}\quad\quad
\array { F(x) &          &                                      &          & F(y) \\
              & {}_{\mathllap{i_{F(x)}}}\searrow &   & \swarrow_{\mathrlap{i_{F(y)}}} \\
              &          & F(x \oplus y) \cong F(x) \oplus F(y) \\
              & {}^{\mathllap{p_{F(X)}}}\swarrow &                                      & \searrow^{\mathrlap{p_{F(y)}}} \\
         F(x) &          &                                      &          & F(y) }
$$

=--


+-- {: .num_remark}
###### Remark

In practice, functors between additive categories are generally assumed to be additive.

=--

+-- {: .num_remark #SufficientConditions}
###### Remark

Each of the following conditions is sufficient for guaranteeing that a functor $\mathcal{A} \to \mathcal{B}$ preserves biproducts (where $\mathcal{A}$ and $\mathcal{B}$ are categories with a zero object):

* The functor preserves finite products (for instance, because it's a right adjoint) and any product in $\mathcal{B}$ is a biproduct.
* The functor preserves finite coproducts (for instance, because it's a left adjoint) and any coproduct in $\mathcal{B}$ is a biproduct.
* The functor preserves finite products and coproducts.

=--

## Examples

\begin{example}
\label{HomFunctor}
The [[hom-functor]] $Hom(-,-) \colon \mathcal{A}^{op}\times \mathcal{A} \to Ab$ is additive in both arguments separately (using the nature of [[biproducts]] and that [[hom-functors preserve limits]] in each variable separately).
\end{example}


+-- {: .num_example}
###### Example

For $\mathcal{A} = R$[[Mod]] and $N \in \mathcal{A}$, the  functor that forms [[tensor product of modules]] $(-)\otimes N \colon \mathcal{A} \to \mathcal{A}$.

=--

In fact these examples are generic, see prop. \ref{RightExactAdditiveIsTensor} below.

+-- {: .num_example}
###### Example

Every [[solid abelian group]] is by definition an [[additive functor]]. 
=--


## Properties

### Relation to $Ab$-enriched functors

An [[additive category]] canonically carries the structure of an [[Ab-enriched category]] where the $Ab$-enrichment structure is induced from the biproducts as described at _[[biproduct]]_. 

+-- {: .num_prop #AdditiveIsAbEnriched}
###### Proposition

With respect to the canonical [[Ab-enriched category]]-structure on additive categories $\mathcal{A}$, $\mathcal{B}$, additive functors $F : \mathcal{A} \to \mathcal{B}$ are equivalently [[Ab]]-[[enriched functors]].

=--

+-- {: .proof}
###### Proof

An $Ab$-enriched functor preserves all finite biproducts that exist, since finite biproducts in [[Ab-enriched category|Ab-enriched categories]] are [[Cauchy complete category|Cauchy colimits]].

=--


### Characterization of right exact additive functors
 {#CharacterizationByExactness}

Let $R, R'$ be [[rings]].

The following is the _[[Eilenberg-Watts theorem]]_. See there for more.

+-- {: .num_prop #RightExactAdditiveIsTensor}
###### Proposition

If an additive functor $F : R$[[Mod]] $\to R'$[[Mod]] is a [[right exact functor]], then there exists an $R'$-$R$-[[bimodule]] $B$ and a [[natural isomorphism]]

$$
  F \simeq B \otimes_R (-)
$$

with the functor that forms the [[tensor product]] with $B$.

=--

This is ([Watts, theorem 1](#Watts)),


## Related concepts

* [[additive monad]]

* [[enriched functor]]

* In the context of [[derived functors in homological algebra]] one considers functors that are additive and in addition left/right [[exact functors]], as discussed above in _[Characterization by exactness](#CharacterizationByExactness)_.

* [[satellite]]

## References

* {#Watts} Charles Watts, _Intrinsic characterizations of some additive functors_, Proceedings of the American Mathematical Society, **11** 1 (1960) 5-8 (1959) &lbrack;[jstor:2032707](http://www.jstor.org/stable/2032707)&rbrack;
 

[[!redirects additive functors]]