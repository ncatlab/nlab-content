

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



## Idea

Following the general concept of $(n,r)$-[[(n,r)-category|category]], a $(0,1)$-category is (up to [[equivalence of categories|equivalence]]) a [[poset]] or (up to [[isomorphism of categories|isomorphism]]) a [[proset]].  We may also call this a $1$-[[1-poset|poset]].



## Definition

+-- {: .num_defn}
###### Definition

An [[(n,1)-category]] is an [[(∞,1)-category]] such that every [[hom-space|hom ∞-groupoid]] is [[n-truncated|(n-1)-truncated]].

=--

Notice that

* a [[0-truncated]] [[∞-groupoid]] is equivalently a set;

* a [[(-1)-truncated]] [[∞-groupoid]] is either [[contractible]] or [[empty set|empty]].

+-- {: .num_prop}
###### Proposition

An $(0,1)$-category is equivalently a [[poset]].

=--

+-- {: .proof}
###### Proof

We may without restriction assume that every hom-$\infty$-groupoid is in fact a set on the nose. Then since this is [[(-1)-truncated]] it is either empty or the singleton. So there is at most one morphism from any object to any other.

=--

## Extra stuff, structure, property

* A $(0,1)$-category with the structure of a [[site]] is a [[(0,1)-site]]: a [[posite]].

* A $(0,1)$-category with the structure of a [[topos]] is a [[(0,1)-topos]]: a [[locale]].


## Related concepts

* [[0-category]], **(0,1)-category**

* [[category]]

* [[2-category]]

* [[3-category]]

* [[n-category]]

* [[(∞,0)-category]]

* [[(∞,1)-category]]

* [[(∞,2)-category]]

* [[(∞,n)-category]]

* [[(n,r)-category]]


[[!redirects (0,1)-categories]]