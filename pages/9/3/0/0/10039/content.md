

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of dual morphism is the generalization to arbitrary [[monoidal categories]] of the notion of [[dual linear map]] in the [[category]] [[Vect]] of [[vector spaces]].

## Definition
 {#Definition}

+-- {: .num_defn}
###### Definition

Given a [[morphism]] $f \colon X \to Y$ between two [[dualizable objects]] in a [[monoidal category]] $(\mathcal{C}, \otimes)$, the corresponding **dual morphism**

$$
  f^\ast \colon Y^\ast \to X^\ast
$$

is the one obtained by $f$ by using the duality [[unit of an adjunction|unit]] of $X$ (the [[coevaluation map]]) and the duality [[counit of an adjunction|counit]] of $Y$ (the [[evaluation map]]) as follows:

$$
  Y^*
  \to Y^*\otimes I
  \to Y^*\otimes X\otimes X^*
  \to Y^*\otimes Y\otimes X^*
  \to I\otimes X^*
  \to X^*
$$

=--

+-- {: .num_remark}
###### Remark

This notion is a special case of the the notion of _[[mate]]_ in a [[2-category]]. 

Namely if $K \coloneqq \mathbf{B}_\otimes \mathcal{C}$ is the [[delooping]] [[2-category]] of the [[monoidal category]] $(\mathcal{C}, \otimes)$, then [[objects]] of $\mathcal{C}$ correspond to [[morphisms]] of $K$, [[dual objects]] correspond to [[adjunctions]] and [[morphisms]] in $\mathcal{C}$ correspond to [[2-morphisms]] in $K$. Under this identification a morphism $f \colon X \to Y$ in $\mathcal{C}$ may be depicted as a [[2-morphism]] of the form

$$
  \array{
     \ast &\stackrel{\mathbb{1}}{\to}& \ast
     \\
     {}^{\mathllap{Y}}\downarrow &\swArrow_{\mathrlap{f}}& \downarrow^{\mathrlap{X}}
     \\
     \ast &\underset{\mathbb{1}}{\to}& \ast
  }
$$

and duality on morphisms is then given by the [[mate]] [[bijection]]

$$
  \array{
    \ast & \overset{\mathbb{1}}{\to} & \ast 
    \\
    {}^{\mathllap{Y}} \downarrow & \swArrow_{\mathrlap{f}} & \downarrow^{\mathrlap{X}} 
    \\
    \ast & \underset{\mathbb{1}}{\to} & \ast
  }
  \;\;\;\;\;
    \mapsto
  \;\;\;\;\;
  \array{
    \ast & \overset{\mathbb{1}}{\to} & \ast 
    \\
    {}^{\mathllap{X^\ast}} \downarrow & \swArrow_{\mathrlap{f^\ast}} & \downarrow^{\mathrlap{Y^\ast}} 
    \\
    \ast & \underset{\mathbb{1}}{\to} & \ast
  }
  \;\;\;\;
  \coloneqq 
  \;\;\;\;
  \array{
    \ast & \overset{Y^\ast}{\to} & \ast & \overset{\mathbb{1}}{\to} 
    & \ast &   \overset{\mathbb{1}}{\to} &    \ast 
   \\
    {}^\mathllap{\mathbb{1}}\downarrow & 
   \swArrow_{\epsilon_Y} & {}^{\mathllap{Y}} \downarrow &  
    \swArrow_{f}     & \downarrow^{\mathrlap{X}} & 
    \swArrow_{\eta_X} 
    & \downarrow \mathrlap{1} 
    \\
    \ast & \underset{\mathbb{1}}{\to} & \ast & \underset{\mathbb{1}}{\to} 
    & \ast & \underset{X^\ast}{\to}    & \ast
  }
  \,.
$$


=--

## Examples

+-- {: .num_example}
###### Example

In $\mathcal{C} = $ [[Vect]] with its standard [[tensor product]] monoidal structure, a [[dual object]] is a [[dual vector space]] and a dual morphism is a [[dual linear map]]. 

=--

+-- {: .num_example}
###### Example

If $A$, $B$ are [[C*-algebras]] which are [[Poincaré duality algebras]], hence [[dualizable objects]] in the [[KK-theory]]-category, then for $f \colon A \to B$ a morphism it is [[K-orientation|K-oriented]], the corresponding [[Umkehr map]] is (postcomposition) with the dual morphism of its [[opposite algebra]] version:

$$
  f! \coloneqq (f^op)^\ast
  \,.
$$

=--

See at _[KK-theory -- Push-forward in KK-theory](KK-theory#UmkehrMap)_.

+-- {: .num_example}
###### Example

More generally, [[twisted Umkehr maps]] in [[generalized cohomology theory]] are given by dual morphisms in [[(∞,1)-category of (∞,1)-modules]]. See at _[[twisted Umkehr map]]_ for more.

=--

## Related concepts

* [[trace]]

[[!redirects dual morphisms]]
