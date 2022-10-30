
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _$n$-fold complete Segal space_ is a [[homotopy theory]]-version of an [[n-fold category]]: an $n$-fold [[category object in an (infinity,1)-category|category object internal to]] [[∞Grpd]] hence an [[n-category object in an (∞,1)-category]], hence an object in  $Cat(Cat(\cdots Cat(\infty Grpd)))$. This is a model for an _[[(∞,n)-category]]_.


A [[complete Segal space]] is to be thought of as the [[nerve]] of a category which is _[[homotopy coherent category theory|homotopically]]_ [[enriched category|enriched]] over [[Top]]: it is a simplicial object in [[Top]], $X^\bullet : \Delta^{op} \to Top$ satisfying some conditions and thought of as a model for an $(\infty,1)$-[[(infinity,1)-category|category]]. 

An $(\infty,n)$-category is in its essence the $(n-1)$-fold iteration of this process: recursively, it is a category which is _[[homotopy coherent category theory|homotopically]]_ [[enriched category|enriched]] over $(\infty,n-1)$-categories.

This implies then in particular that an $(\infty,n)$-category in this sense is an $n$-fold simplicial topological space
$$
  X_\bullet : \Delta^{op} \times 
     \Delta^{op} \times \cdots \times \Delta^{op}
     \to Top
$$

which satisfies the condition of [[complete Segal space|Segal spaces]] -- the [[Segal condition]] (characterizing also [[nerves]] of [[categories]]) in each variable, in that all the squares

$$
  \array{
     X_{m+n,\bullet} &\to& X_{n,\bullet}
     \\
     \downarrow && \downarrow
     \\
     X_{m,\bullet} &\to& X_{0,\bullet}
  }
$$

are [[homotopy coherent category theory|homotopy pullbacks]] of $(n-1)$-fold Segal spaces.

In analogy of how it works for [[complete Segal spaces]], the completness condition on an $n$-fold complete Segal space demands that the $(n-1)$-fold complete Segal space in degree zero is (under suitable identifications) the 
[[infinity-groupoid]] which is the [[core]] of the [[(infinity,n)-category]] which is being presented. Since the embedding of $\infty$-groupoids into ($n-1$)-fold complete Segal spaces is by adding lots of degeneracies, this means that the completeness condition on an $n$-fold complete Segal space involves lots of degeneracy conditions in degree 0.

## Definition

(...)

## Related concepts

* [[Theta-spaces]], [[Segal n-categories]]

* [[higher Segal space]]

* [[semi-Segal space]]

## References

The definition originates in the thesis

* [[Clark Barwick]], _$(\infty,n)$-$Cat$ as a closed model category_ PhD (2005)

which however remains unpublished. It appears in print in section 12 of 

* [[Clark Barwick]], [[Chris Schommer-Pries]], _On the Unicity of the Homotopy Theory of Higher Categories_ ([arXiv:1112.0040](http://arxiv.org/abs/1112.0040), [slides](http://prezi.com/w0ykkhh5mxak/the-uniqueness-of-the-homotopy-theory-of-higher-categories/))
 {#BarwickSchommerPries}


The basic idea was being popularized and put to use in

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

A detailed discussion in the general context of [[internal categories in an (∞,1)-category]] is in section 1 of

* {#Lurie09} [[Jacob Lurie]], _$(\infty,2)$-Categories and the Goodwillie Calculus I_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 


For related references see at _[[(∞,n)-category]]_ .

[[!redirects n-fold Segal space]]

[[!redirects n-fold complete Segal spaces]]
[[!redirects n-fold Segal spaces]]
