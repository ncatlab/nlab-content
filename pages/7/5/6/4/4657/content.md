
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $\{U_i \to X\}$ a [[cover]] of a [[space]] $X$, the corresponding **&#268;ech groupoid** is the [[internal groupoid]]

$$
  C(\{U_i\}) = (\coprod_{i j} U_i \cap U_j \rightrightarrows \coprod_i U_i)
$$

whose set of objects is the [[disjoint union]] $\coprod_i U_i$ of the covering patches, and the set of morphisms is the disjoint union of the [[intersections]] $U_i \cap U_j$ of these patches.

This is the $2$-[[coskeleton]] of the full [[Čech nerve]]. See there for more details.

If we speak about [[generalized element|generalized points]] of the $U_i$ (which are often just ordinary points, in applications), then 

* an [[object]] of $C(\{U_i\})$ is a pair $(x,i)$ where $x$ is a point in $U_i$;

* there is a unique [[morphism]] $(x,i) \to (x,j)$ for all pairs of objects labeled by the same $x$ such that $x \in U_i \cap U_j$;

* hence the composition of morphism is of the form

  $$
    \array{
       && (x,j)
       \\
       & \nearrow &=& \searrow
       \\
      (x,i) &&\to&& (x,k)
    }
    \,.
  $$

## Examples

For $X$ a [[smooth manifold]] and $\{U_i \to X\}$ an [[atlas]] by [[coordinate chart]]s, the &#268;ech groupoid is a [[Lie groupoid]] which is equivalent to $X$ as a Lie groupoid:
$C(\{U_i\}) \stackrel{\simeq}{\to} X$

For $\mathbf{B}G$ the Lie groupoid with one object coming from a [[Lie group]] $G$ morphisms of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
$$

are also called [[anafunctor]]s from $X$ to $\mathbf{B}G$. They correspond to smooth $G$-[[principal bundle]]s on $X$.

## Related concepts

* [[Cech nerve]]

[[!redirects Cech groupoid]]
[[!redirects Cech groupoids]]
[[!redirects Čech groupoids]]
