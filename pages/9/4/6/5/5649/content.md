
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

For $C$ a [[category]], a [[class]] $K \subset Mor(C)$ of [[morphism]]s in $C$ is said to satisfy **2-out-of-3** if for all composable $f,g \in Mor(C)$ we have that if two of the three morphisms $f$, $g$ and the composite $g \circ f$ is in $K$, then so is the third.

$$
  \array{
    \\
    {}^{\mathllap{f}}\nearrow \searrow^{\mathrlap{g}}
    \\
    \stackrel{g \circ f}{\to}
  }
  \,.
$$

So in particular this means that $K$ is closed under composition of morphisms. 

This definition has immediate generalization also to [[higher category theory]]. For instance in [[(∞,1)-category theory]] its says that:

a class of 1-morphisms in an [[(∞,1)-category]] satisfies two out of 3, if for every [[2-morphism]] of the form

$$
  \array{
    & {}^{\mathllap{}f}\nearrow &\Downarrow^{\simeq}& \searrow^{\mathrlap{g}}
    \\
    &&\stackrel{h}{\to}&&
  }
$$

we have that if two of $f$, $g$ and $h$ are in $C$, then so is the third.

## Examples

* The class of [[isomorphism]]s in any category satisfies 2-out-of-3. This case is the archetype of most of the cases in which the property is invoked: 2-out-of-3 is characteristic of morphisms that have a notion of [[inverse]].

* A [[category with weak equivalences]] is defined as a category with a subcategory that contains all [[isomorphism]]s and satisfies 2-out-of-3. 



## Related concepts

* [[category with weak equivalences]]
* [[weak factorization system]]
* [[2-out-of-6 property]]



[[!redirects 2-out-of-3]]
[[!redirects 2-out-of-3 property]]
[[!redirects 2 out of 3]]
[[!redirects 2 out of 3 property]]
[[!redirects two out of three property]]
[[!redirects two-out-of-three property]]
