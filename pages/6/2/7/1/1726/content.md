
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
$n$-fold Segal spaces similarly result from viewing $(\infty,n)$-categories as a special class of $n$-fold internal $(\infty,1)$-categories in [[∞Grpd|∞-groupoids]].

If $\mathcal{C}$ is an $(\infty,1)$-category, then $(\infty,1)$-categories [[category object in an (infinity,1)-category|internal]] to $\mathcal{C}$ can be defined as certain simplicial objects in $\mathcal{C}$ (namely those satisfying the "Segal condition"). Thus $n$-fold internal $(\infty,1)$-categories in $\infty$-groupoids correspond to a class of $n$-simplicial $\infty$-groupoids, and  $n$-fold Segal spaces are defined by additionally specifying certain constancy conditions.

To describe the correct homotopy theory of $(\infty,n)$-categories we also want to regard the fully faithful and essentially surjective morphisms between $n$-fold Segal spaces as equivalences. It turns out that, just as in the case of [[Segal spaces]], the localization at these maps can be accomplished by restricting to a full subcategory of _complete_ objects.


## Definition

### $n$-fold Segal objects
If $\mathcal{C}$ is an $(\infty,1)$-category with pullbacks, we say that a simplicial object $X_\bullet : \Delta^{op} \to \mathcal{C}$ satisfies the [[Segal condition]] if 
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
are all pullbacks. Such _Segal objects_ give the $(\infty,1)$-categorical version of [[internal category|internal categories]] as _algebraic_ structures. (I.e. we have not inverted a class of fully faithful and essentially surjective morphisms.)

If $Seg(\mathcal{C})$ denotes the full subcategory of $Fun(\Delta^{op}, \mathcal{C})$ spanned by the Segal objects, then this is again an $(\infty,1)$-category with pullbacks, so we can iterated the definition to obtain a full subcategory $Seg^{n}(\mathcal{C})$ of $Fun(\Delta^{n,op}, \mathcal{C})$ of _Segal $\Delta^{n}$-objects_ in $\mathcal{C}$.

We can now inductively define $n$-fold Segal objects by imposing constancy conditions:
An _$n$-fold Segal object_ in $\mathcal{C}$ is a Segal $\Delta^{n}$-object $X$ such that

1. The $(n-1)$-simplicial object $X_0 : \Delta^{n-1,op} \to \mathcal{C}$ is constant
1. The $(n-1)$-simplicial objects $X_i$ are $(n-1)$-fold Segal objects for all $i$.

When $\mathcal{C}$ is the $(\infty,1)$-category of spaces (or $\infty$-groupoids) we refer to $n$-fold Segal objects as _$n$-fold Segal spaces_.


### Complete $n$-fold Segal spaces

We now define fully faithful and essentially surjective morphisms between $n$-fold Segal inductively in terms of the corresponding notions for [[Segal spaces]]:


+-- {: .num_defn}
###### Definition

A morphism $X \to Y$ between $n$-fold Segal spaces is _fully faithful and essentially surjective_ if:

1. $X_{\bullet,0,\ldots,0} \to Y_{\bullet,0,\ldots,0}$ is a fully faithful and essentially surjective morphism of Segal spaces
1. $X_{1,\bullet,\ldots,\bullet} \to Y_{1,\bullet,\ldots,\bullet}$ is a fully faithful and essentially surjective morphism of $(n-1)$-fold Segal spaces

=--

+-- {: .num_defn}
###### Definition

An $n$-fold Segal space $X$ is _complete_ if:

1. The Segal space $X_{\bullet,0,\ldots,0}$ is complete.
1. The $(n-1)$-fold Segal space $X_{1,\bullet,\ldots,\bullet}$ is complete.

=--


+-- {: .num_remark}
###### Remark

There are several equivalent ways to reformulate these inductive definitions. For example, a morphism $f : X \to Y$ is fully faithful and essentially surjective if and only if: 

1. $X_{\bullet,0,\ldots,0} \to Y_{\bullet,0,\ldots,0}$ is essentially surjective.
1. For all objects $x,x' \in X_{0,\ldots,0}$ the induced map on $(n-1)$-fold Segal spaces of morphisms $X(x,x') \to Y(fx,fx')$ is fully faithful and essentially surjective.


=--

+-- {: .num_theorem}
###### Theorem

The complete $n$-fold Segal spaces are precisely the $n$-fold Segal spaces that are local with respect to the fully faithful and essentially surjective morphisms. Thus the localization of the $(\infty,1)$-category of $n$-fold Segal spaces at this class of morphisms is equivalent to the full subcategory of complete $n$-fold Segal spaces.

=--


This was first proved in Barwick's [thesis](#BarwickThesis), generalizing Rezk's proof in the case $n=1$. Later, [Lurie](#Lurie09) extended the notion of complete Segal objects to more general contexts than spaces, which allows an inductive definition of complete $n$-fold Segal spaces as complete Segal objects in complete $(n-1)$-fold Segal spaces. 
The theorem for $n$-fold Segal spaces then follows by inductively applying the generalization of Rezk's theorem (for the case $n=1$) to this setting.


### Definition via the model category of simplicial sets

(...)

## Related concepts

* [[Theta-spaces]], [[Segal n-categories]]

* [[higher Segal space]]

* [[semi-Segal space]]

## References

The definition originates in the thesis

* {#BarwickThesis} [[Clark Barwick]], _$(\infty,n)$-$Cat$ as a closed model category_ PhD (2005)

which however remains unpublished. It appears in print in section 12 of 

* [[Clark Barwick]], [[Chris Schommer-Pries]], _On the Unicity of the Homotopy Theory of Higher Categories_ ([arXiv:1112.0040](http://arxiv.org/abs/1112.0040), [slides](http://prezi.com/w0ykkhh5mxak/the-uniqueness-of-the-homotopy-theory-of-higher-categories/))
 {#BarwickSchommerPries}


The basic idea was being popularized and put to use in

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

A detailed discussion in the general context of [[internal categories in an (∞,1)-category]] is in section 1 of

* {#Lurie09} [[Jacob Lurie]], _$(\infty,2)$-Categories and the Goodwillie Calculus I_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))

A textbook account is in

* {#Paoli19} [[Simona Paoli]], _Simplicial Methods for Higher Categories -- Segal-type Models of Weak $n$-Categories_, Springer 2019  ([doi:10.1007/978-3-030-05674-2](https://doi.org/10.1007/978-3-030-05674-2), [toc pdf](https://link.springer.com/content/pdf/bfm%3A978-3-030-05674-2%2F1.pdf))
 


For related references see at _[[(∞,n)-category]]_ .

[[!redirects n-fold Segal space]]

[[!redirects n-fold complete Segal spaces]]
[[!redirects n-fold Segal spaces]]

[[!redirects globular n-fold complete Segal space]]
[[!redirects globular n-fold complete Segal spaces]]


