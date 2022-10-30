
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _symmetric monoidal $(\infty,1)$-category_ is the analog of a [[symmetric monoidal (∞,1)-category]] for [[(∞,n)-category]] theory.


## Properties

### Dualizable objects

+-- {: .num_defn}
###### Definition

An object $X$ in a symmetric monoidal $(\infty,n)$-category is called **dualizable** if ...

=--

+-- {: .num_prop}
###### Claim

Let $C$ be a symmetric monoidal $(\infty,n)$-category. Then there exists another symmetric monoidal $(\infty,n)$-category $C^{fd}$ and a symmetric monoidal functor 

$$
  C^{fd} \to C
$$

such that $C^{fd}$ has duals and is [[universal property|universal]] with these properties:

for any symmetric monoidal [[(∞,n)-category with duals]] $D$ and any symmetric monoidal functor $F : D \to C$ there exists a symmetric monoidal functor $f : D \to C^{fd}$, unique up to equivalence, and an equivalence

$$
  \array{
     && C^{fd}
     \\
     & {}^{\mathllap{f}}\nearrow &\Downarrow^{\simeq}& \searrow
     \\
     D &&\stackrel{F}{\to}&& C
  }
  \,.
$$

=--

This appears as ([Lurie, claim 2.3.19](#Lurie)).

+-- {: .num_remark}
###### Remark

$C^{fd}$ is obtained from $C$ by discarding all objects that do not have duals and all [[k-morphism]]s that do not admit right and left adjoints. 

=--

+-- {: .num_def}
###### Definition

An object $X \in C$ is called a **[[fully dualizable object]]** if it is in the essential [[image]] of $C^{fd} \to C$.

=--

## Examples

* For all $n \in \mathbb{N}$, the [[(∞,n)-category of cobordisms]] $Bord_n$ is symmetric monoidal. By the [[cobordism hypothesis]] this should be the [[free functor|free]] symmetric monoidal $(\infty,n)$-category on the [[point]].

* For all $n$ and $C$ any symmetric monoidal $(\infty,n)$-category, there is a symmetric monoidal [[(∞,n)-category of spans]] of [[∞-groupoid]]s over $C$.

## Related concepts

* [[monoidal category]], [[monoidal (∞,1)-category]]

  * [[symmetric monoidal category]], [[symmetric monoidal (∞,1)-category]], **symmetric monoidal $(\infty,n)$-category** 

  * [[closed monoidal category]] ,  [[closed monoidal (∞,1)-category]]

* [[symmetric monoidal 2-category]]

* [[(∞,n)-category with adjoints]]

* [[(∞,n)-category with duals]]


## References

A discussion of dualizable objects is in section 2.3 of 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_
{#Lurie}

[[!redirects symmetric monoidal (infinity,n)-categories]]

[[!redirects symmetric monoidal (∞,n)-category]]
[[!redirects symmetric monoidal (∞,n)-categories]]

[[!redirects monoidal (∞,n)-category]]
[[!redirects monoidal (infinity,n)-category]]
[[!redirects monoidal (∞,n)-categories]]
[[!redirects monoidal (infinity,n)-categories]]
