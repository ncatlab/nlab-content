
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Distributive monoidal categories

* table of contents
{: toc}

## Idea

A _distributive monoidal_ category is a [[monoidal category]] whose [[tensor product]] [[distributive law|distributes]] over [[coproducts]].

## Definition

A **distributive monoidal category** (this is not entirely standard terminology) is a [[monoidal category]] with [[coproducts]] whose tensor product preserves coproducts in each variable.  Thus, we have canonical isomorphisms
$$ X \otimes \coprod_i Y_i \cong \coprod_i (X\otimes Y_i)$$
$$ \coprod_i X_i \otimes Y \cong \coprod_i (X_i\otimes Y)$$
Depending on the arity of the coproducts in question, we may speak of a **finitary** or **infinitary** distributive monoidal category. 

A distributive [[cartesian monoidal category]] is a [[distributive category]], while any distributive monoidal category is a particular case of a [[rig category]].  See [[distributivity for monoidal structures]].

A more abstract way to say this, due to Weber and Batanin, is that if $M$ is the free monoidal category monad and $M V \xrightarrow{\otimes} V$ is the structure map of a monoidal category $V$, then $V$ is distributive if it admits left Kan extensions along functors $f:A\to B$ between [[discrete categories]] (of some size), and moreover if
$$\array{
  A && \xrightarrow{f} && B\\
  & \searrow & \xRightarrow{\phi} & \swarrow\\
  && V
}$$
is such a Kan extension, then so is
$$\array{
  M A && \xrightarrow{M f} && M B\\
  & \searrow & \xRightarrow{M \phi} & \swarrow\\
  && M V\\
  && \downarrow^\otimes\\
  && V.
}$$

## Examples
 {#Examples}

Beyond [[distributive categories]], examples of distributive monoidal categories include the following:

* [[Ab]], the category of [[abelian groups]] equipped with the [[tensor product of abelian groups]]

* $R$[[Mod]], the category of [[modules]] over a [[commutative ring]] $R$, equipped  with the [[tensor product of modules]]

* $k$[[Vect]] = $k$[[Mod]], the category of [[vector space]] over some [[field]] $k$, equipped with the [[tensor product of vector spaces]],

* $k$[[Vect(X)]], the category of ([[topological vector bundles|topological]]) [[vector bundles]] for $X$ some ([[topological space|topological]]) [[space]], equipped with the [[tensor product of vector bundles]].

In all these cases the coproduct is the respective [[direct sum]] (e.g. [[direct sum of vector bundles]] in the last case).

Also:

* the category of [[pointed topological spaces]] with respect to forming [[smash product]] and [[wedge sum]] (e.g. [Hatcher, Section 4.F](algebraic+topology#Hatcher)).


## Properties

### The weakly semicartesian case

+-- {: .num_remark} 
###### Remark 
A monoidal category is finitary distributive if its tensor product preserves binary coproducts in each variable and the monoidal unit $I$ is [[weak limit|weakly]] [[terminal object|terminal]] (e.g., if there is a morphism $1 \to I$ out of a terminal object). 
=-- 

+-- {: .proof} 
###### Proof 
There is a canonical isomorphism 
$$x \otimes 0 + x \otimes y \to x \otimes (0 + y)$$ 
and thus a canonical isomorphism 
$$\phi: x \otimes 0 + x \otimes y \to x \otimes y$$ 
whose restriction along the coproduct inclusion $x \otimes y \to x \otimes 0 + x \otimes y$ is the identity $1_{x \otimes y}$. Let $k: x \otimes 0 \to x \otimes y$ be the restriction of $\phi$ along the other coproduct inclusion. Then $\phi$ induces an evident bijection 
$$\hom(x \otimes y, y) \stackrel{\langle [k], id \rangle}{\to} \hom(x \otimes 0, y) \times \hom(x \otimes y, y).$$ 
Since $\hom(x \otimes y, y)$ is inhabited for all $x, y$ (with the help of some map $x \to I$, there is some map $x \otimes y \to I \otimes y \cong y$), this forces $\hom(x \otimes 0, y)$ to be a singleton for any $y$, so that $x \otimes 0$ is initial. 
=-- 


### Free monoids

A distinguishing feature of (infinitary) distributive monoidal categories is that the [[monad]] $T$ for [[monoid objects]] in such a category has a particularly simple expression:
$$ T X = \coprod_n X^{\otimes n}.$$
The same is true for the monad on enriched graphs whose algebras are categories enriched over such a monoidal category.  This also generalizes to [[lax monoidal categories]], a.k.a. "multitensors"; see [(Weber)](#Weber).

## Related concepts

* [[distributive law]]

* [[distributivity for monoidal structures]]

  * [[distributive monoidal category]]

  * [[bipermutative category]]

  * [[linearly distributive category]]

  * [[rig category]]


## References

* [[Mark Weber]], *Multitensors and monads on categories of enriched graphs*, [spnet](https://selectedpapers.net/arxiv/1106.1977)
 {#Weber}

[[!redirects distributive monoidal categories]]
