
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Definition

### For locally small categories

Given [[object|objects]] $x$ and $y$ in a [[locally small category]], the __hom-set__ $hom(x,y)$ is the collection of all morphisms from $x$ to $y$.  In a [[closed category]], the hom-set may also be called the __external hom__ to distinguish it from the [[internal hom]].


* We say a category is [[locally small category|locally small]] if this collection is always actually a set instead of a proper class, or in the context of a [[Grothendieck universe]]: if this set is a $U$-small set.  This holds for many examples, but not for all. For example, if $C$ and $D$ are not [[small category|small categories]], then the [[functor category]] $C^D$ (whose morphisms are [[natural transformation]]s) will not be locally small.


### For enriched categories

For a category $C$ [[enriched category theory|enriched over]] a category $V$, the "hom-set" $C(x,y)$ is an object of $V$, the [[hom-object]].

### For internal categories

For $C = (C_0, C_1, s,t,e, c)$ an [[internal category]], the [[generalized element|generalized]] objects of $C$ are morphisms $x: X \to C_0$ and $y: Y \to C_0$, and the "hom-set" becomes the [[pullback]] $C(x,y)$ in

$$ \array{
C(x,y)     & \to          & Y            \\
\downarrow & \searrow     &              & \searrow^{y}    \\
X          &              & C_1          & \stackrel{t}\to & C_0 \\
           & \searrow^{x} & \downarrow_s \\
           &              & C_0
} $$

In particular, in a category with a [[terminal object|terminal]] [[generator]] $*$, we may identify morphisms $x,y: * \to C_0$ with [[global element|global]] objects of $C$ and form $C(x,y)$ as above.

## Related concepts


* [[hom-object]]

* **hom-set**, [[hom-group]]

  [[heteromorphism]]

* [[hom-category]]

* [[hom-space]]

* [[derived hom-space]]

* [[hom-functor]]

* [[enriched hom-functor]], [[internal hom-functor]]

* [[derived hom-functor]]

## References

Textbook accounts:

* [[Saunders MacLane]], §I.8 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;



[[!redirects homsets]]
[[!redirects homset]]
[[!redirects hom-sets]]
[[!redirects hom sets]]
[[!redirects external hom]]

[[!redirects hom set]]

[[!redirects set of morphisms]]
[[!redirects sets of morphisms]]
