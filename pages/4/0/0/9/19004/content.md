
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
**([[integral Steenrod square]] in terms of [[Bockstein homomorphism]] for [[exponential sequence]])**

The integral Steenrod squares (def. \ref{IntegralSteenrodSquares}) may equivalently be written in terms of the [[Bockstein homomorphism]] $\delta$ of the [[exponential sequence]] $\mathbb{Z} \overset{\cdot 2\pi}{\longrightarrow} \mathbb{R} \overset{mod\, 2 \pi}{\longrightarrow} U(1)$ as

$$
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
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
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
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
      &\underset{Sk^{2n}}{\longrightarrow}&   
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
       &\underset{  Sq^1 }{\longrightarrow}&
    B^{\bullet + 2n + 1} (\mathbb{Z}/2\mathbb{Z})
  }
$$

=--

## Related concepts

* [[integral Stiefel-Whitney classes]]

* [[integral Wu structure]]

## References

The third integral Steenrod square $Sq^3_{\mathbb{Z}}$ plays a central role in the discussion of the [[supergravity C-field]] in

* {#DiaconescuMooreWitten00} [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv. Theor. Math. Phys. 6:1031-1134, 2003 ([arXiv:hep-th/0005090](https://arxiv.org/abs/hep-th/0005090))


[[!redirects integral Steenrod squares]]
