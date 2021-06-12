+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-ategory theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given any [[object]] $X$ in any $(k,1)$-category $C$ for a [[natural number]] $k$, the $n$-[[truncated objects]] of $X$ for $n+1 \lt k$ form an $(n+1,1)$-category, an $(n+1)$-truncated $(k,1)$-category, (though in general it may be a [[large category|large]] one, cf. [[well-powered category]]). This is called the __$(n+1,1)$-category of $n$-truncated objects__ of $X$, or the __$n$-truncated object $(n+1,1)$-category__ of $X$.

## Properties

If $C$ is [[finitely complete category|finitely complete]], then the $n$-truncated objects form a finitely complete $(n+1,1)$-category, so we may speak of the __finitely complete $(n+1,1)$-category of $n$-truncated objects__.  

In any [[coherent category|coherent]] $(k,1)$-category, then the $n$-truncated objects form a coherent $(n+1,1)$-category, so we may speak of the __coherent $(n+1,1)$-category of $n$-truncated objects__.

In any $(k,1)$-[[topos]], the $n$-truncated objects of $X$ form a $(n+1,1)$-topos, so we may speak of the __$(n+1,1)$-topos of $n$-truncated objects__.

The reader can probably think of other variations on this theme.

If $f : X \to Y$ is a morphism that has pullbacks along $n$-truncated morphisms, then pullback along $f$ induces a $(n+1,1)$-category morphism $f^* : Trunc_n(Y) \to Trunc_n(X)$. This is functorial in the sense that if $g : Y \to Z$ also has this property, then there is an inhabited equivalence $n+1$-groupoid $f^* \circ g^* \cong (g \circ f)^*$. 

If $C$ has pullbacks of $n$-truncated morphisms, $Trunc_n$ is often used to denote the contravariant functor $C^{op} \to (n+1,1)Cat$ whose action on morphisms is $Trunc_n(f) = f^*$.

## Examples

* A [[(0,1)-category]] of (-1)-truncated objects of an object $X$ is a [[poset of subobjects]] of $X$. 

* A [[well-pointed category|well-pointed]] [[Heyting category|Heyting]] [[pretopos]] of 0-truncated objects of the [[terminal object]] $1$ is a (possibly) [[predicative mathematics|predicative]] model of the [[category of sets]]. 

* A [[well-pointed category|well-pointed]] [[Heyting category|Heyting]] [[Π-pretopos]] of 0-truncated objects of the [[terminal object]] of $1$ is a (possibly) [[predicative mathematics|weakly predicative]] model of the [[category of sets]]. 

* A [[well-pointed category|well-pointed]] [[topos]] of 0-truncated objects of the [[terminal object]] $1$ is an [[predicative mathematics|impredicative]] model of the [[category of sets]]. 

* A [[well-pointed category|well-pointed]] [[W-topos]] of 0-truncated objects of the [[terminal object]] $1$ whose 0-truncated (-1)-[[connected object|connected]] [[morphisms]] all have [[sections]] is a model of [[ETCS]]. 

## Related concepts

* If one opts for the alternative definition that $n$-truncated objects _are_ $n$-truncated morphisms into the object (not equivalence large $n+1$-groupoids thereof), then one gets a $(n+1,1)$-[[precategory]] of $n$-truncated objects instead. In any case, the *$(n+1,1)$-category* of $n$-[[truncated objects]] $Trunc_n(X)$ in our sense is the $(n+1,1)$-categorical reflection of the $(n+1,1)$-precategory $TruncMor_n(X)$ of $n$-truncated objects in the alternative sense, and of course the reflection [[Rezk completion]] map $TruncMor_n(X) \to Trunc_n(X)$ is an [[equivalence]]. 

* [[poset of subobjects]]

* [[n-truncated object classifier]]

[[!redirects $(n+1)$-category of $n$-truncated objects]]
[[!redirects $(n+1)$-categories of $n$-truncated objects]]
[[!redirects $n$-truncated object $(n+1)$-category]]
[[!redirects $n$-truncated object $(n+1)$-categories]]