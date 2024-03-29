
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents
* table of contents
{:toc}

## Idea

A **monoidal adjunction** is an [[adjunction]] between [[monoidal categories]] which respects the monoidal structure.

Since there are several types of [[monoidal functors]] (lax, colax, and strong) there are several types of "adjunctions between monoidal categories which respect the monoidal structure."  Namely, we could have:

* An adjunction in the [[2-category]] [[MonCat]] of [[monoidal categories]] and [[strong monoidal functors]].  In this case both the left and right adjoint are strong.  

  $$
    \array{
      \underoverset
        {\underset{R \, \text{strong monoidal}}{\longrightarrow}}
        {\overset{L \, \text{strong monoidal}}{\longleftarrow}}
        {}
    }
  $$  

  We call this a **strong monoidal adjunction**.

* {#MonoidalAdjnctionIdea} An adjunction in the 2-category [[MonCat]]${}_\ell$ of monoidal categories and [[lax monoidal functors]].  In this case the right adjoint is lax, while the left adjoint is necessarily strong (by [[doctrinal adjunction]]; see [here](/nlab/show/doctrinal+adjunction#strength)).  

  $$
    \array{
      \underoverset
        {\underset{R \, \text{lax monoidal}}{\longrightarrow}}
        {\overset{L \, \text{strong monoidal}}{\longleftarrow}}
        {}
    }
  $$  

  In fact, since the [[right adjoint]] of an [[oplax monoidal functor]] is necessarily a [[lax monoidal functor]] ([this prop.](oplax+monoidal+functor#OplaxAdjointToLax)), it is sufficient to demand that $L$ be strong monoidal.

  This version, which is one of the most frequently occurring, is often called simply a **monoidal adjunction**.

* The dual: an adjunction in the 2-category $MonCat_c$ of monoidal categories and colax monoidal functors, in which case the left adjoint is colax and the right adjoint is strong.  One might call this an **opmonoidal adjunction**.

* A mixed situation, in which the left adjoint is colax, the right adjoint is lax, and the lax and colax structure maps are [[mates]] under the adjunction.  This is a [[conjunction]] in the [[double category]] of monoidal categories and lax and colax monoidal functors, so we may call it a **monoidal conjunction** or a **lax/colax monoidal adjunction**.  By [[doctrinal adjunction]], given any adjunction between monoidal categories, if the right adjoint is lax monoidal, then the left adjoint automatically acquires a colax monoidal structure making the adjunction into a monoidal conjunction, and dually.

## Details
 {#Details}

As mentioned [above](#MonoidalAdjnctionIdea), the nature of monoidal adjunctions follows as a special case from generalities of [[doctrinal adjunctions]]. For the record, here is an explicit discussion:

+-- {: .num_prop #MonoidalAdjunctionElementary}
###### Proposition

Let 

$$
  \mathcal{C}
  \underoverset
    {\underset{R}{\longrightarrow}}
    {\overset{L}{\longleftarrow}}
    {\bot}
  \mathcal{D}
$$

be a pair of [[adjoint functors]] between [[monoidal categories]], such that the [[left adjoint]] $L$ is a [[strong monoidal functor]] by [[natural isomorphisms]]

$$
  \mu_L(X,Y)
  \;\colon\;
  L(X) \otimes L(Y) \overset{\simeq}{\longrightarrow} L(X \otimes Y)
$$

and

$$
  e_L 
    \;\colon\;
  1 \overset{\simeq}{\longrightarrow} L(1)
  \,.
$$


Then

1. the [[right adjoint]] $R$ becomes a [[lax monoidal functor]] via natural morphisms

   $$
     \mu_R(X,Y)
     \;\colon\;
     R (X) \otimes R(Y)
      \overset{\eta(R(X) \otimes R(Y))}{\longrightarrow}
     R L (R(X) \otimes R(Y))
      \underoverset{}{ R( {\mu_L^{-1}(R(X), R(Y))} ) }{\longrightarrow}
     R ( L  R(X) \otimes L R (Y) )
       \overset{R( \epsilon(X) \otimes \epsilon(Y) )}{\longrightarrow}
     R(X \otimes Y)
   $$
  
   and

   $$
     e_R
     \;\colon\;
     1 
       \overset{\eta(1)}{\longrightarrow} 
     R L(1) 
       \overset{R(e_L^{-1})}{\longrightarrow} 
     R(1)
     \,,
   $$

   where $\eta$ denotes the [[adjunction unit]] and $\epsilon$ denotes the [[adjunction counit]], as usual.

1. For any object $A \in \mathcal{D}$ carrying the structure of a [[monoid object]] $(A, \mu_A, e_A)$, then 

   1. the [[unit of the adjunction]] $\eta(A) \;\colon\; A \longrightarrow R L(A)$ is a monoid [[homomorphism]] with respect to the canonically induced monoid structure on $R L(A)$ ([this prop.](monoidal+functor#MonoidsToMonoidsByLaxMonoidal)) given by

      $$
        \mu_{R L(A)} 
          \;\colon\; 
        R L(A) \otimes R L(A)
          \overset{\mu_R(L(A))}{\longrightarrow}
        R( L(A) \otimes L(A))
          \overset{R(\mu_L(A))}{\longrightarrow}
        R L(A \otimes A)
          \overset{R L(\mu_A)}{\longrightarrow}
        R L(A)
      $$

      and

      $$  
        e_{R L(A)}
          \;\colon\;
        1
          \overset{e_R}{\longrightarrow}  
        R(1)
          \overset{R(e_L)}{\longrightarrow}
        R L(1) 
          \overset{R L(e_A)}{\longrightarrow}
        R L(A)
      $$

   1. similarly for the [[counit of the adjunction]].

=--

+-- {: .proof}
###### Proof

The first statement is discussed at _[[oplax monoidal functor]]_. 

For the second statement, we need first need to check that the following [[commuting square|square commutes]]:

$$
  \array{
    A \otimes A 
     &\overset{\eta(A) \otimes \eta(A)}{\longrightarrow}&
    R L (A) \otimes R L (A)
    \\
    {}^{\mathllap{\mu_A}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{R L(A)}}}
    \\
    A &\underset{\eta(A)}{\longrightarrow}& R L(A)
  }
$$


Now by definition, the composite of the top and right morphism here 
is the total diagonal composite in the following diagram:

$$
  \array{
  && A \otimes A
  &\overset{\eta(A \otimes A)}{\longrightarrow}&
  R L(A \otimes A)
  &\overset{R(\mu_L^{-1})}{\longrightarrow}&
  R( L(A) \otimes L(A) )
  \\
  && 
    {}^{\mathllap{\eta(A) \otimes \eta(A)}}\downarrow && {}^{\mathllap{ R L( \eta(A) \otimes \eta(A) ) }}\downarrow 
  && 
    {}^{\mathllap{R( L(\eta(A))  \otimes L(\eta(A)) )}}\downarrow
  & \searrow^{\mathrlap{R(id \otimes id)}}
  \\
  \mu_R(L(A))
  &\colon&
  R L (A) \otimes R L ( A)
   &\overset{\eta(R L (A) \otimes R L (A))}{\longrightarrow}&
  R L (R L ( A) \otimes R L (A))
   &\underoverset{}{ R( {\mu_L^{-1}(R L(A))} ) }{\longrightarrow}&
  R ( L  R L (A) \otimes L R L (A) )
    &\overset{R( \epsilon(L(A)) \otimes \epsilon(L(A)) )}{\longrightarrow}&
  R(L(A) \otimes L(A))
  \\
  && && && && \downarrow^{\mathrlap{ R( \mu_L(A)) }}
  \\
  && && && && R L( A \otimes A )
  \\
  && && && && \downarrow^{\mathrlap{ R L (\mu_A) }}
  \\
  && && && && R L (A)
 }
$$

Here the top sqaures commute by naturality of $\eta$ and $\mu_L$,
and top right diagonal morphism is the [[identity morphism]], as shown, by the [[zig-zag identity]] for the adjunction $(L \dashv R)$. Therfore $R(\mu_L^{-1})$ cancels agains $R(\mu_L)$. so that the composite morphism in question becomes just $A \otimes A \overset{\eta(A \otimes A)}{\longrightarrow} R L(A \otimes A) \overset{ R L(\mu_A) }{\longrightarrow} R L(A)$. Again by the naturality of the [[adjunction unit]] $\eta$

$$
  \array{
    A \otimes A 
      &\overset{\eta(A \otimes A)}{\longrightarrow}&
    R L (A \otimes A)
    \\
    {}^{\mathllap{ \mu_A }}\downarrow 
      &&  
    \downarrow^{\mathrlap{R L(\mu_A)}}
    \\
    A &\underset{\eta(A)}{\longrightarrow}& R L (A)
  }
$$

this equals $\eta(A) \circ \mu_A$, as required.

Finally we need to check that the following diagram commutes:

$$
  \array{
     && 1
     \\
     & {}^{\mathllap{e_A}}\swarrow && \searrow^{\mathrlap{ e_{R L (A)} }}
     \\
     A 
     &&
       \underset{\eta(A)}{\longrightarrow}
     &&
    R L(A)
  }
$$

Now unwinding the above definitions of $e_{R L}(A)$ in terms of the definition of $e_R$ we find that

$$
  e_{R L (A)}
  \;\colon\;
  1 
    \overset{\eta(1)}{\longrightarrow} 
  R L(1) 
    \overset{R(e_L^{-1})}{\longrightarrow} 
  R(1)
  \overset{R(e_L)}{\longrightarrow} R L(1) \overset{R L(e_a)}{\longrightarrow} R L(A)
  \,.
$$

Here the two morphisms in the middle cancel, so that we are left just with

$$
  e_{R L(A)}
  \;\colon\;
  1 
    \overset{\eta(1)}{\longrightarrow}
  R L(1)
   \overset{R L(e_A)}{\longrightarrow}
  R L (A)
  \,.
$$

That this equals $\eta(A)\circ e_A$, as required, follows by the naturality of $\eta$:

$$
  \array{
    1 
      &\overset{\eta(1)}{\longrightarrow}&
    R L(1)
    \\
    {}^{\mathllap{e_A}}\downarrow && \downarrow^{\mathrlap{R L(e_A)}}
    \\
    A &\underset{\eta(A)}{\longrightarrow}& R L(A)
  }
  \,.
$$

The argument for the homomorphism property of the counit should be formally dual to the above.

=--


## Examples

+-- {: .num_example #Stabilization}
###### Example
**([[stabilization]] in [[stable homotopy theory]])**


The [[stabilization]] adjunction 

  $$
    Ho(Spectra)
     \underoverset
       {\underset{\Omega^\infty}{\longrightarrow}}
       {\overset{\Sigma^\infty(-)}{\longleftarrow}}
       {\bot}
    Ho(Spaces^{\ast/})
       \underoverset
         {\underset{}{\longrightarrow}}
         {\overset{(-)_+}{\longleftarrow}}
         {}
    Ho(Spaces)
  $$

  between the [[classical homotopy categories]] $Ho(Spaces)$ and $Ho(Spaces^{\ast/})$ of ([[pointed topological space|pointed]]) [[topological spaces]] and the [[stable homotopy category]] $Ho(Spectra)$ is a monoidal adjunction, since the [[left adjoint]] $\Sigma^\infty(-)_+$ (forming the [[suspension spectrum]] of a space after freely [[pointed topological space|adjoining a basepoint]]) is [[strong monoidal functor|strong monoidal]] with respect to forming [[product topological spaces]] and forming [[smash  product of spectra]], respectively.

  In fact this is the [[derived functors]] of what is even a [[monoidal Quillen adjunction]] between the [[classical model structure on topological spaces]] and the stable [[model structure on orthogonal spectra]] ([this cor.](Introduction+to+Stable+homotopy+theory+--+1-2#StableMonoidalQuillenSuspensionSpectrumFunctor)), which implies (strong) monoidality of the derived functors on homotopy categories ([this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#StrongMonoidalDerivedFunctorFromStrongMonoidalQuillenAdjunction)).

In detail, let

$$
  (L \dashv R)
   \;\colon\;
  \mathbb{S}_{orth}Mod_{stable}
     \underoverset
      {\underset{\Omega^\infty_{orth}}{\longrightarrow}}
      {\overset{\Sigma^\infty_{orth}}{\longleftarrow}}
      {\bot}
  Top^{\ast/}_{Quillen}
    \underoverset
       {\underset{}{\longrightarrow}}
       {\overset{(-)_+}{\longleftarrow}}
       {\bot}
  Top_{Quillen}
$$

be the Quillen adjunction on orthogonal spectra ([here](Introduction+to+Stable+homotopy+theory+--+1-2#SuspensionSpectrumStructuredStrictQuillenAdjunction)).
The left adjoint $L$ is a strong monoidal functor, and hence so is its [[derived functor]] $\Sigma^\infty(-)_+ \colon Ho(Top) \to Ho(Spectra)$ (by [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#StrongMonoidalDerivedFunctorFromStrongMonoidalQuillenAdjunction)). 

{#DerivedLaxMonoidalStructure} We want to see that the structure of a lax monoidal functor which is induced on the derived right adjoint $\Omega^\infty(-) \colon Ho(Top) \to Ho(Spectra)$ via prop. \ref{MonoidalAdjunctionElementary} is the expected one, given on [[Omega-spectra]] $X$ and $Y$ by

$$
  \Omega^\infty(X) \wedge \Omega^\infty(X)
    =
   X_0 \wedge Y_0
    \overset{}{\to}
   (X \wedge Y)_0
    =
   \Omega^\infty( X \wedge Y )
  \,.
$$

To see this, observe that if $X$ and $Y$ are [[CW-spectrum|CW-]][[Omega-spectra]] and hence cofibrant and fibrant in $\mathbb{S}_{orth}Mod_{stable}$ then the derived lax monoidal structure is given by the total bottom composite in the following diagram
$$
  \array{     
     R (X) \otimes R(Y)
      &\overset{\eta(R(X) \otimes R(Y))}{\longrightarrow}&
     R L (R(X) \otimes R(Y))
      &\underoverset{}{ R( {\mu_L^{-1}(R(X), R(Y))} ) }{\longrightarrow}&
     R ( L  R(X) \otimes L R (Y) )
       &\overset{R( \epsilon(X) \otimes \epsilon(Y) )}{\longrightarrow}&
     R(X \otimes Y)
     \\
     &{}_{\mathllap{ \text{derived } \atop {\text{adjunction unit}} }}\searrow& 
     \downarrow^{\mathrlap{R j L (R(X) \otimes R(Y))}}
     &&
     \downarrow^{\mathrlap{R j ( L R (X) \otimes L R(Y) )}}
     &&
     \downarrow^{\mathrlap{ R j( X \otimes Y ) }}
     \\
      &&
     R P L (R(X) \otimes R(Y))
      &\underoverset{}{ R Q( {\mu_L^{-1}(R(X), R(Y))} ) }{\longrightarrow}&
     R P ( L  R(X) \otimes L R (Y) )
       &\overset{R Q( \epsilon(X) \otimes \epsilon(Y) )}{\longrightarrow}&
     R P (X \otimes Y)
  }
  \,,
$$

where we write for brevity $(L \dashv R) \coloneqq (\Sigma^\infty_{orth} \dashv \Omega^\infty_{orth})$, and  where $j \colon id \longrightarrow P$ denotes [[functorial factorization|functorial]] [[fibrant replacement]] (which exists since the [[small object argument]] applies in $\mathbb{S}_{orth}Mod_{stable}$). By functoriality of the replacement, all the squares commute, so that the derived lax monoidal structure on CW-Omega spectra is seen to be equivalently the underived one.

But that underived top horizontal composite is manifestly just the canonical isomorphism $X_0 \wedge Y_0 \simeq (X \wedge Y)_0$ (since $R$ simply picks the component space in degree-0  and $L$ preserves the component space in degree 0).


=--

+-- {: .num_example #ExponentialModality}
###### Example
**([[exponential modality]] in [[linear type theory]])**

In [[linear type theory]] (see there for more) the [[exponential modality]] $!$ may have [[categorical semantics]] as the [[comonad]] induced by a monoidal adjunction. 

=--

## Related concepts

* [[projection formula]]

* [[enriched adjunction]]

[[!redirects monoidal adjunctions]]
[[!redirects opmonoidal adjunction]]
[[!redirects opmonoidal adjunctions]]
[[!redirects comonoidal adjunction]]
[[!redirects comonoidal adjunctions]]
[[!redirects monoidal conjunction]]
[[!redirects monoidal conjunctions]]

[[!redirects strong monoidal adjunction]]
[[!redirects strong monoidal adjunctions]]
