
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category Theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Just as a [[subobject classifier]] in a [[(1,1)-category]] classifies the [[monomorphisms]] or [[(-1)-truncated]] morphisms (and thus the [[subobjects]]) of the category, a _discrete object classifier_ in a [[(2,1)-category]] should classify the [[faithful functor|faithful]] or [[0-truncated]] morphisms (and thus the [[discrete morphism|discrete objects]]) in the (2,1)-category, see at _[n-truncated morphisms -- between groupoids](n-truncated+object+of+an+infinity-category#TruncatedMorphismsBetweenGroupoids)_. 

## Definition

In a (2,1)-category $C$ with [[terminal object]] $*$, [[interval object]] $I$, and finite [[2-pullback|(2,1)-pullbacks]], a __discrete object classifier__ is a morphism $inhabited: [I, Set] \rightarrow Set$ whose target is a nonterminal object $Set$ and whose source is the [[internal hom|internal]] [[hom-object]] $[I, Set]$ such that for every [[faithful morphism]] $B \colon U \rightarrow G$ in $C$, there is a unique morphism $F:G \rightarrow Set$ such that there is a (2,1)-pullback [[diagram]] of the form

$$\array{U & \to & [I,Set] \\
  ^{B}\downarrow & \cong & \downarrow^{inhabited}\\
  G & \underset{\chi_U}{\to} & Set}$$

+-- {: .num_remark}
###### Remark

If $Set$ exists, it is typically called the **[[universe]] of [[set]]s** or **[[groupoid]] of sets**. A global element $F:G \rightarrow Set$ is typically called an **[[indexed family]]**, an element $A:* \rightarrow Set$ is typically called a **set**, and a set $A:* \rightarrow Set$ is **[[inhabited object|inhabited]]** if there exists a morphism $B:* \rightarrow [I, Set]$ such that the $A$ [[factor]]s into $inhabited \circ B$. All these terms refer to the [[internal set theory]] of the (2,1)-category $C$. 

The morphism $\chi_U$ is also called the **[[classifying morphism]]** of the discrete object $U$ and morphism $B:U \rightarrow G$.

=--

## Examples

### In $Grpd$

In the (2,1)-category [[Grpd]] of groupoids and functors between groupoids, the discrete object classifier $Set$ is the groupoids of sets, or, as $Set$ is a groupoid with a category structure, more commonly known as the [[category of sets]].
 

## See also

* [[subobject classifier]]

* [[(sub)object classifier in an (infinity,1)-topos]]

* [[classifying morphism]]

* [[type of types]], [[universe in a topos]]

## References

* David Corfield: _101 things to do with a 2-classifier_ ([blog](http://golem.ph.utexas.edu/category/2008/01/101_things_to_do_with_a_2class.html))