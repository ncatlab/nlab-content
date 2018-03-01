
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
_$n$-fold complete Segal spaces_ are a model for [[(∞,n)-category|(∞,n)-categories]], i.e. the [[homotopy theory|homotopical]] version of [[n-category|n-categories]].

We can view [[strict n-category|strict n-categories]] as [[n-fold category|n-fold categories]] where part of the structure is trivial; for example, strict 2-categories can be described as double categories where the only vertical morphisms are identities. 
$n$-fold Segal spaces similarly result from viewing $(\infty,n)$-categories as a special class of $n$-fold internal $\infty$-categories in [[∞Grpd|$\infty$-groupoids]].

If $\mathcal{C}$ is an $\infty$-category, then $\infty$-categories [[category object in an (infinity,1)-category|internal]] to $\mathcal{C}$ can be defined as certain simplicial objects in $\mathcal{C}$ (namely those satisfying the "Segal condition"). Thus $n$-fold internal $\infty$-categories in $\infty$-groupoids correspond to a class of $n$-simplicial $\infty$-groupoids, and  $n$-fold Segal spaces are defined by additionally specifying certain constancy conditions.

To describe the correct homotopy theory of $(\infty,n)$-categories we also want to regard the fully faithful and essentially surjective morphisms between $n$-fold Segal spaces as equivalences. It turns out that, just as in the case of [[Segal spaces]], the localization at these maps can be accomplished by restricting to a full subcategory of _complete_ objects.


## Definition

### $n$-fold Segal objects
If $\mathcal{C}$ is an $\infty$-category with pullbacks, we say that a simplicial object $X_\bullet : \Delta^{op} \to \mathcal{C}$ satisfies the [[Segal condition]] if 
the squares
$$
  \array{
     X_{m+n} &\to& X_{n}
     \\
     \downarrow && \downarrow
     \\
     X_{m} &\to& X_{0}
  }
$$
are all pullbacks. Such _Segal objects_ give the $\infty$-categorical version of [[internal category|internal categories]] as _algebraic_ structures. (I.e. we have not inverted a class of fully faithful and essentially surjective morphisms.)

If $Seg(\mathcal{C})$ denotes the full subcategory of $Fun(\Delta^{op}, \mathcal{C})$ spanned by the Segal objects, then this is again an $\infty$-category with pullbacks, so we can iterated the definition to obtain a full subcategory $Seg^{n}(\mathcal{C})$ of $Fun(\Delta^{n,op}, \mathcal{C})$ of _Segal $\Delta^{n}$-objects_ in $\mathcal{C}$.

We can now inductively define $n$-fold Segal objects by imposing constancy conditions:
An _$n$-fold Segal object_ in $\mathcal{C}$ is a Segal $\Delta^{n}$-object $X$ such that

1. The $(n-1)$-simplicial object $X_0 : \Delta^{n-1,op} \to \mathcal{C}$ is constant
1. The $(n-1)$-simplicial objects $X_i$ are $(n-1)$-fold Segal objects for all $i$.

When $\mathcal{C}$ is the $\infty$-category of spaces (or $\infty$-groupoids) we refer to $n$-fold Segal objects as _$n$-fold Segal spaces_.


### Complete $n$-fold Segal objects

(...)

### Definition via the model category of simplicial sets

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
