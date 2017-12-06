

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### $(\infty,1)$-topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of _monoidal $(\infty,1)$-category_ is the analogue of the notion of [[monoidal category]] in the context of [[(infinity,1)-category|(∞,1)-categories]].

There are various ways to state the monoidal structure. One is in terms of fibrations over the [[simplex category]]. This is the approach taken in 

*  [[Jacob Lurie]], _Noncommutative algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))

Another is in terms of [[(∞,1)-operad]]s (see there). This approach has been taken in ([Francis](#Francis)).  Both are described below.

Just as many ordinary $(\infty,1)$-categories (particularly, all of those that are [[locally presentable (infinity,1)-category|locally presentable]]) can be presented by [[model categories]], many monoidal $(\infty,1)$-categories can be presented by [[monoidal model categories]].  See for instance [NikolausSagave15](#NikolausSagave15).


### Idea of the simplicial definition 

As discussed at the end of the entry on 
[[monoidal category]],
an ordinary [[monoidal category]] may be thought of as a lax functor

$$
  * \to \mathbf{B} Cat
$$

from the terminal category to the one-object 3-category whose single 
[[hom-object]] is the [[2-category]] [[Cat]] of all categories and for which composition is the [[cartesian monoidal category|cartesian monoidal structure]] on [[Cat]].

More concretely, as also described there, such a lax functor is a 
kind of [[descent]] object in 
a [[weighted limit]] $lim^{\Delta} const_{\mathbf{B}Cat}$, namely
a diagram

$$
  \array{
    F \Delta^4 &\stackrel{=}{\to}& \mathbf{B} Cat
    \\
    \uparrow && \uparrow^{Id} 
    \\
    F \Delta^3 &\stackrel{\alpha}{\to}& \mathbf{B} Cat
    \\
    \uparrow && \uparrow^{Id} 
    \\
    F \Delta^2 &\stackrel{\otimes}{\to}& \mathbf{B} Cat
    \\
    \uparrow && \uparrow^{Id} 
    \\
    F \Delta^1 &\stackrel{C}{\to}& \mathbf{B}Cat
    \\
    \uparrow && \uparrow^{Id} 
    \\
    F\Delta^0 &\stackrel{\bullet}{\to}& \mathbf{B}Cat
  }
$$

where $F \Delta^n$ is the free 3-category of the $n$-[[simplex]] 
(an [[oriental]]), where the horizontal morphisms are the chosen data 
 -- the category $C$, product $\otimes$, associator $\alpha$ and, 
in degree 4, the respect for the pentagon identity --
and the condition is that this commutes for all vertical morphisms 
$F(\Delta^n \to \Delta^m)$.

So this is a 4-functor

$$
  F(\Delta^4) \to \mathbf{B}Cat
$$

subject to a certain constraint. 

Using the general mechanism of [[generalized universal bundle]]s, this 
classifies a [[Cat]]-bundle

$$
  \array{
    C^\otimes \to F(\Delta^4)
  }
  \,.
$$

With a bit more time than I have on the train one can figure out
that conversely suitable such fibrations are equivalent to monoidal
categories. Alternatively, one can read pages 5 and 6 of
_LurieNonCom_ cited below.

In any case, this motivates the following definition.



## Definition

### Plain monoidal $(\infty,1)$-category 

+-- {: .num_defn}
###### Definition


A **monoidal ($\infty,1$)-category** $(C, \otimes)$
is 

* a [[simplicial set]] $C^\otimes$;

* and a [[coCartesian fibration]] of simplicial 
sets $ p_\otimes : C^\otimes \to N(\Delta)^{op}$

* such that for each $n \in \mathbb{N}$ the induced [[(infinity,1)-functor]]
$C^\otimes_{[n]} \to C^\otimes_{\{i,i+1\}}$ determines an
equivalence of [[(infinity,1)-category|(infinity,1)-categories]]

$$
  C^\otimes_{[n]}
  \to
  C^\otimes_{\{0,1\}}
  \times
  \cdots
  \times
  C^\otimes_{\{n-1,n\}}
  \simeq
  (C^\otimes_{[1]})^n
  \,.
$$

Here $\Delta$ is the [[simplex category]] and $N(\Delta)$ its [[nerve]].

=--

### $\mathcal{O}$-monoidal $(\infty,1)$-category

The following defines [[symmetric monoidal (∞,1)-categories]] and their variants, where the [[commutative operad]] is replaced by any other [[(∞,1)-operad]].

+-- {: .num_defn}
###### Definition

Let $\mathcal{O}^\otimes$ be an [[(∞,1)-operad]]. A **[[coCartesian fibration of (∞,1)-operads]]** is

1. a [[coCartesian fibration]] $p : \mathcal{C}^\otimes \to \mathcal{O}^\otimes$ of the underlying [[quasi-categories]];

1. such that the composite 

   $$
     \mathcal{C}^\otimes \stackrel{p}{\to} \mathcal{O}^\otimes \to Fin_* = Comm
   $$

   exhibits $\mathcal{C}^\otimes$ as an [[(∞,1)-operad]].

In this case we say that the underlying [[(∞,1)-category]]

$$
  \mathcal{C}  = \mathcal{C}^\otimes \times_{\mathcal{O}^\otimes} \mathcal{O}
$$

is equipped by $p$ with the [[structure]] of an **$\mathcal{O}$-monoidal $(\infty,1)$-category**.

=--

This is ([Lurie, def. 2.1.2.13](#Lurie)).

+-- {: .num_defn}
###### Definition

For $\mathcal{O}$ = [[commutative operad|Comm]], an $\mathcal{O}$-monoidal $(\infty,1)$-category is a [[symmetric monoidal (∞,1)-category]].

=--


## Higher monoidal structure 

While for an ordinary [[monoid]] there is just one notion of commutativity (either it is or it is not commutative), already a [[monoidal category]] distinguishes between being just [[braided monoidal category|braided monoidal]] or fully [[symmetric monoidal category|symmetric monoidal]].

This pattern continues, as expressed by the [[k-tuply monoidal n-category|periodic table of k-tuply monoidal categories]].

A [[higher category theory|higher category]] may be a [[k-tuply monoidal n-category]] or more generally [[k-tuply monoidal (n,r)-category]] for different values of $k$. The lowest value of $k= 1$ (since for $k = 0$ there is no monoidal structure at all) corresponds to monoidal product which is $\infty$-associative, i.e.  associative up to higher coherent homotopies, but need not have any degree of _commutativity_. 

One says that an $n$-category is _symmetric monoiodal_ if it is "as monoidal as possible", i.e. $\infty$-tuply monoidal. In particular, in [[higher algebra|Noncommutative algebra]] and [[higher algebra|Commutative algebra]] we have

* the 1-fold monoidal (∞,1)-categories described here;

* [[symmetric monoidal (infinity,1)-category|∞-tuply monoidal (∞,1)-categories]].

### Operadic/algebraic definition of monoidal structure

For each $1 \leq n \leq \infty$ let $E_n$ denote the [[little n-disk operad|little n-disk]] [[operad]] whose [[topological space]] of $E_n^k$ of $k$-ary operations is the space of embeddings of $k$ $n$-dimensional disks (balls) in one $n$-dimensional disk without intersection, and whose composition operation is the obvious one obtained from gluing the big outer disks into given inner disks.

In [John Francis' PhD thesis](#Francis)  the theory of [[(∞,1)-categories]] equipped with an action of the $E_n$-[[operad]] is established, so that

* $(\infty,1)$-categories with an $E_1$-action are precisely [[monoidal (∞,1)-categories]]  -- 1-fold monoidal $(\infty,1)$-categories;

* $(\infty,1)$-categories with an $E_\infty$-action are precisely [[symmetric monoidal (∞,1)-categories]] -- $\infty$-tuply monoidal $(\infty,1)$-categories;

* $(\infty,1)$-categories with an $E_n$-action for $1 \lt n \lt \infty$ are the corresponding $n$-tuply monoidal $(\infty,1)$-categories in between.

>**Remark** The second statement is example 2.3.8 in [EnAction](#Francis). The first seems to be clear but is maybe not in the literature. Jacob Lurie is currently rewriting [[higher algebra|Higher Algebra]] such as to build in a discussion of $E_n$-operadic structures in the definition of $k$-tuply monoidal $(\infty,1)$-categories.

## Related concepts

* [[monoidal category]], [[monoidal (2,1)-category]], **monoidal $(\infty,1)$-category**

  * [[monoidal (∞,1)-functor]]

  * [[Picard ∞-group]]

* [[braided monoidal category]], [[braided monoidal (∞,1)-category]]

  * [[braided ∞-group]]

* [[symmetric monoidal category]], [[symmetric monoidal (2,1)-category]], [[symmetric monoidal (∞,1)-category]]

  * [[abelian ∞-group]]

* [[closed monoidal category]] ,  [[closed monoidal (∞,1)-category]]

* [[prime spectrum of a monoidal stable (∞,1)-category]]

## References

The simplicial definition for plain monoidal $(\infty,1)$-categories is definition 1.1.2 in 

* [[Jacob Lurie]], _[[Noncommutative Algebra]]_ ([arXiv](http://arxiv.org/abs/math/0702299))

John Francis' work on [[little cubes operad]]-actions on  $(\infty,1)$-categories is in

* [[John Francis]], PhD thesis ([web](http://dspace.mit.edu/handle/1721.1/43792))
{#Francis}

The general notion of an $\mathcal{O}$-monoidal $(\infty,1)$-category is around definition 2.1.2.13 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_ .
 {#Lurie}

An introductory survey is in

* [[Moritz Groth]], _A short course on $\infty$-categories_ ([pdf](http://www.math.uni-bonn.de/~mgroth/InfinityCategories.pdf))

A relation to [[monoidal model categories]] (in particular, that every locally presentable symmetric monoidal $(\infty,1)$-category arises from a symmetric monoidal model category) is described in

* {#NikolausSagave15} [[Thomas Nikolaus]], [[Steffen Sagave]], _Presentably symmetric monoidal infinity-categories are represented by symmetric monoidal model categories_. Algebr. Geom. Topol. 17 (2017), no. 5, 3189--3212. ([arXiv:1506.01475](http://arxiv.org/abs/1506.01475))

[[!redirects monoidal (infinity,1)-categories]]
[[!redirects monoidal (∞,1)-category]]
[[!redirects monoidal (∞,1)-categories]]
