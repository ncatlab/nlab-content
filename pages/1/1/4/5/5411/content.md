
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

A _symmetric monoidal $(\infty,n)$-category_ is the analog of a [[symmetric monoidal (∞,1)-category]] for [[(∞,n)-category]] theory.

##Definition

As [[Jacob Lurie]] says in [Lurie, Mathoverflow quote](#Lurie):

> {#Definition} There are many (equivalent) definitions for the notion of symmetric monoidal $(\infty,n)$-category. One approach is based on the observation that a monoidal category can be identified with a bicategory having only a single object. You can define a monoidal
$(\infty,n)$-category to be an $(\infty,n+1)$-category with a specified object,
such that all other objects are isomorphic to it (in the complete Segal space model, this means that the space of objects should be connected). Similarly you can define a braided monoidal $(\infty,n)$-category to be an $(\infty,n+2)$-category equipped with a distinguished object satisfying a simple connectivity condition, and so on and so forth. You get to the symmetric monoidal case by taking the homotopy inverse limit (that is, a symmetric monoidal
$(\infty,n)$-category is a collection of pointed $(\infty,n+k)$-categories, each of which is obtained by "looping" the next one). You might find this definition convenient in the context of bordism categories, since they are naturally related in this way (if you ``loop'' the a bordism category of $d$-manifolds, you get a bordism category of $d+1$-manifolds: and this is sensible even when $d$ is negative).

>Alternatively, you can define a symmetric monoidal $(\infty,n)$-category to be a commutative monoid in the setting of $(\infty,n)$-categories. There are many ways to formalize this. Since you're asking about specific models, let's suppose you start with some model category $\mathbf{A}$ for the homotopy theory of $(\infty,n)$-categories (higher-dimensional Segal spaces, for example). If you have a simplicial model category, you can do as Charles suggested and take algebras for some $E_{\infty}$-operad in simplicial sets. If you'd prefer not to mention operads, you can just copy Segal's definition of a $\Gamma$-space: take the category of functors $F$ from pointed finite sets into $\mathbf{A}$, and equip it with a model structure that enforces the relevant Segal condition.

>As Martin mentions in [his answer](http://mathoverflow.net/questions/81425/what-is-a-symmetric-monoidal-infty-n-category/81432#81432), there is an extensive discussion of the case $n=1$ in my book, and also of commutative monoids in an arbitrary $(\infty,1)$-category (of which this is a special case, since the collection of all $(\infty,n)$-categories can be regarded as an $(\infty,1)$-category). I don't know of references that address your question more specifically (though I would not be surprised if there were some).

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

* [[2d TQFT]], [[TCFT]]

  [[Calabi-Yau object]]

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

* {#Lurie} [[Jacob Lurie]], [Mathoverflow/81425 answer](http://mathoverflow.net/questions/81425/what-is-a-symmetric-monoidal-infty-n-category/81445#81445).

[[!redirects symmetric monoidal (infinity,n)-categories]]

[[!redirects symmetric monoidal (∞,n)-category]]
[[!redirects symmetric monoidal (∞,n)-categories]]

[[!redirects monoidal (∞,n)-category]]
[[!redirects monoidal (infinity,n)-category]]
[[!redirects monoidal (∞,n)-categories]]
[[!redirects monoidal (infinity,n)-categories]]
