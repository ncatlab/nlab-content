
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #IntegralSteenrodSquares}
###### Definition
**([[integral Steenrod squares]])**

For [[odd natural numbers|odd]] $2n + 1 \in \mathbb{N}$ the _integral Steenrod square_ $Sq^{2n + 1}_{\mathbb{Z}}$ is the [[composition]] of the mod-2 [[Steenrod square]] $Sq^{2n}$ with the [[Bockstein homomorphism]] $\beta$ associated with the sequence $\mathbb{Z} \overset{\cdot 2}{\to} \mathbb{Z} \overset{mod\, 2}{\longrightarrow} \mathbb{Z}/2\mathbb{Z}$:

$$
  Sq^{2n + 1}_{\mathbb{Z}}
  \;\coloneqq\;
  \beta \circ Sq^{2n}
  \,.
$$

=--

## Properties


+-- {: .num_prop}
###### Proposition

The odd-degree integral Steenrod squares from def. \ref{IntegralSteenrodSquares} are indeed integral lifts of the mod-2 Steenrod squares in that 

$$
  (mod\, 2) \circ Sq^{2n + 1}_{\mathbb{Z}}
  \;=\;
  Sq^{2n+1}
  \,,
$$


=--

+-- {: .proof}
###### Proof

This follows from the relation of the [[Bockstein homomorphism]] to the first [[Steenrod square]]

$$
  (mod, 2) \circ  \beta = Sq^1
$$

([this example](Bockstein+homomorphism#Mod2BocksteinIntoMod2Cohomology)) together with the first [[Adem relation]] 

$$
  Sq^1 \circ Sq^{2n} = Sq^{2n+1}
$$ 

([this example](Steenrod+square#CompositionWithSq1)):

$$
  \array{
    Sq^{2n+1}_{\mathbb{Z}}
    &\colon&
    B^{\bullet} (\mathbb{Z}/2\mathbb{Z})
      &\overset{Sk^{2n}}{\longrightarrow}&      
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
      &\overset{ \beta }{\longrightarrow}&
    B^{\bullet + 2n + 1} \mathbb{Z}
    \\
    &&
    \downarrow^{ id }  
    &&
    \downarrow^{ id }
      &&
    \downarrow^{\mathrlap{B^{k + 2 n + 1}(mod\, 2)}}
    \\
    Sq^{2n+1}
    &\colon&
    B^{\bullet} (\mathbb{Z}/2\mathbb{Z})
      &\underset{Sk^{2n}}{\longrightarrow}&   
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
       &\underset{  Sq^1 }{\longrightarrow}&
    B^{\bullet + 2n + 1} (\mathbb{Z}/2\mathbb{Z})
  }
$$

=--


+-- {: .num_prop #IntegralSteenrodSquareInTermsOfBocksteinForExponentialSequence}
###### Proposition
**([[integral Steenrod square]] in terms of [[Bockstein homomorphism]] for [[exponential sequence]])**

The integral Steenrod squares (def. \ref{IntegralSteenrodSquares}) may equivalently be written in terms of the [[Bockstein homomorphism]] $\delta$ of the [[exponential sequence]] $\mathbb{Z} \overset{\cdot 2\pi}{\longrightarrow} \mathbb{R} \overset{mod\, 2 \pi}{\longrightarrow} U(1)$ as

$$
  \label{IntegralSteenrodSquareViaBocksteinOfExponentialSequence}
  Sq^{2n+1}_{\mathbb{Z}}
  \;\colon\;
  B^{\bullet} (\mathbb{Z}/2\mathbb{Z})
    \overset{
      Sq^{2 n}
    }{\longrightarrow}
  B^{\bullet + 2n } (\mathbb{Z}/2\mathbb{Z})
  \overset{
    \iota    
  }{\longrightarrow}
  B^{\bullet + 2n} U(1)
   \overset{\delta}{\longrightarrow}
  B^{\bullet + 2n + 1} \mathbb{Z}
  \,.
$$

=--


+-- {: .proof}
###### Proof

Since $\beta = \delta \circ \iota$, by [this example](Bockstein+homomorphism#Mod2BocksteinAndExponentialExactSequence).

=--


## Examples
 {#Examples}

+-- {: .num_example #IntegralSteenrodSquareRefinedToOrdinaryDifferentialCohomology}
###### Example
**([[integral Steenrod square]] refined to [[ordinary differential cohomology]])**

Let $\hat G_{2n+2} \colon X \to \mathbf{B}^{2n+1} U(1)_{conn}$ be a [[cocycle]] in [[ordinary differential cohomology]] of degree $2n + 2$.

By inserting the bottom triangle of the ordinary [[differential cohomology hexagon]] ([this diagram](differential+cohomology+diagram#eq:OrdinarCohomologyHexagon)) into the factorization in (eq:IntegralSteenrodSquareViaBocksteinOfExponentialSequence) we obtain a canonical refinement of the [[integral Steenrod square]] $Sq^{2n+1}_{\mathbb{Z}} [G_{2n + 2}]$ to a cocycle $\widehat{Sq}^{2n+1}_{\mathbb{Z}} \hat G_{2n+2}$ in [[ordinary differential cohomology]], which happens to be [[flat infinity-bundle|flat]]

$$
  \array{
     && && \mathbf{B}^{4n+2} \flat U(1)
     &\longrightarrow&
     \mathbf{B}^{4n+2}U(1)_{conn}
     \\
     && 
     & {}^{\mathllap{ \iota \circ Sq^{2n} }}\nearrow 
     &
     &
     {}_{\mathllap{\delta}}\searrow
     &
     \downarrow^{\chi}
     \\
     X 
     &\underset{G_{2n + 2}}{\longrightarrow}&
     B^{2n+2} \mathbb{Z}
     &&
       \underset{ Sq^{2n+1}_{\mathbb{Z}} }{\longrightarrow}
     &&
     B^{4n+3} \mathbb{Z}
  }
  \,.
$$

If one moreover asks that the integral Steenrod square vanishes

$$
  [ Sq^{2n+1}_{\mathbb{Z}} G_{2n+2}]
  \;=\;
  0
  \;\in\;
  H^{4n+3}(X,\mathbb{Z})
$$

(as in [Diaconescu-Moore-Witten 00, around (6.9)](#DiaconescuMooreWitten00) for $n = 1$) then the curvature exact sequence and characteristic class exact sequence in [[ordinary differential cohomology]] ([this prop.](ordinary+differential+cohomology#ExactSequencesForOrdDiffCohomology)) imply that the class of $\widehat{Sq}^{2n+1}_{\mathbb{Z}} \hat G_{2n + 2}$ is identified with a class in [[de Rham cohomology]] in degree $4n+3$:

$$
  H^{2n+2}_{diff}(X)|_{Sq^{2n+1}_{\mathbb{Z}} = 0}
    \overset{\widehat{Sq}_{\mathbb{Z}}^{2n+1}}{\longrightarrow}
  H^{4n+3}_{dR}(X)
  \,.
$$


=--



## Related concepts

* [[integral Stiefel-Whitney classes]]

* [[integral Wu structure]]

## References

The third integral Steenrod square $Sq^3_{\mathbb{Z}}$ plays a central role in the discussion of the [[supergravity C-field]] in

* {#DiaconescuMooreWitten00} [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv. Theor. Math. Phys. 6:1031-1134, 2003 ([arXiv:hep-th/0005090](https://arxiv.org/abs/hep-th/0005090))


[[!redirects integral Steenrod squares]]
