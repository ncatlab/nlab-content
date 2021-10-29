
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[synthetic differential geometry]], the _[[tangent bundle]]_ of an [[object]] $X$ is the [[internal hom]] $X^{\mathbb{D}^1}$ out of the 1d first order [[infinitesimal disk]] $\mathbb{D}^1$, equipped with the projection to $X$ induced from the unique point $\ast \to \mathbb{D}^1$:

$$
  X^{(\ast \to \mathbb{D}^1)} \;\colon\; X^{(\mathbb{D}^1)} \longrightarrow X
  \,.
$$

(Here we are using that the [[internal hom|internal]] [[hom-functor]] $(-)^{(-)}$ is a [[contravariant functor]] in its "exponent" variable.)

This makes manifest and precise the intuitive idea that a [[tangent vector]] on $X$ is an "[[infinitesimal object|infinitesimal]] [[curve]]" in $X$, see also the [Examples](#Examples) below.

In this formulation the operation of [[differentiation]] is simply the [[internal hom]]-[[functor]]:

Given a function: 

$$
  X \overset{f}{\longrightarrow} Y
  \,.
$$

its [[differential]] is its image under the [[internal hom]] $(-)^{(\mathbb{D}^1)}$:

$$
  X^{(\mathbb{D}^1)}
   \overset{ \phantom{AA} f^{(\mathbb{D}^1)} \phantom{AA} }{\longrightarrow}
  Y^{(\mathbb{D}^1)}
  \,.
$$

## Examples
 {#Examples}

In a standard model for [[synthetic differential geometry]]/[[differential cohesion]] such as the [[Cahiers topos]] $\mathbf{H}$, for $X \in SmthMfd \overset{y}{\hookrightarrow} \mathbf{H}$ an ordinary [[smooth manifold]], its [[synthetic tangent bundle]] coincides with the traditional [[tangent bundle]] $T X \overset{p}{\to} X$:

$$
  \array{
    X^{(\mathbb{D}^1)} & \simeq & T X
    \\
    {}^{\mathllap{ X^{ (\ast \to \mathbb{D}^1) } }}\big\downarrow 
      && 
    \big\downarrow{}^{ \mathrlap{p_X} }
    \\
    X^{\ast} & \simeq & X
  }
$$

Moreover, if $Y \in SmthMfd \hookrightarrow \mathbf{H}$ is another [[smooth manifold]], then a [[morphism]] 

$$
  X \overset{\phantom{AA} f \phantom{AA} }{\longrightarrow} Y
$$

is equivalently a [[smooth function]] in the traditional sense (i.e. the external [[Yoneda embedding]]-[[functor]] $SmthMfd \overset{y}{\hookrightarrow} \mathbf{H}$ is [[fully faithful functor|fully faithful]] ) and its [[image]] under the [[internal hom]] is its traditional [[differentiation]] $d f$:

$$
  \array{
    X^{(\mathbb{D}^1)} 
      &\overset{ \phantom{AA} f^{(\mathbb{D}^1)} \phantom{AA} }{\longrightarrow}&
    Y^{(\mathbb{D}^1)}
    \\
    {}^\simeq\big\downarrow && \big\downarrow{}^\simeq
    \\
    T X &\overset{ \phantom{AA} d f \phantom{AA} }{\longrightarrow}& 
    T Y
  }
$$

This way the evident [[functor|functoriality]] of the [[internal hom]] $(-)^{(\mathbb{D}^1)}$ is identified with the [[chain rule]] of traditional [[differentiation]].

For more on this see 

* at _[Cahiers topos -- Synthetic tangent spaces](Cahiers+topos#RelationToSyntheticTangentSpaces)_.

* at _[[geometry of physics -- supergeometry]]_ the section _[Super mapping spaces](geometry+of+physics+--+supergeometry#SuperMappingSpaces)_


## Properties

### For Microlinear spaces

For $X$ a [[microlinear space]] the synthetic tangent bundle shares many of the expected properties of a [[tangent bundle]].




## Related concepts

* [[odd tangent bundle]] (analog in [[supergeometry]])

* [[kinematic tangent bundle]], [[operational tangent bundle]]

* [[jet bundle]] via [[jet comonad]]

## References

For lecture notes see

* [[geometry of physics -- supergeometry]] the section _[Super mapping spaces](geometry+of+physics+--+supergeometry#SuperMappingSpaces)_


[[!redirects synthetic tangent bundles]]
[[!redirects synthetic tangent space]]
[[!redirects synthetic tangent spaces]]

