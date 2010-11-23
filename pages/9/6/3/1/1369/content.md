

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
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

Another is in terms of [[(∞,1)-operad]]s (see there). This approach has been taken in ([Fracis](#Francis)) 

Both are described below.


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
that conversely suitable such fibrations are equivlent to monoidal
categoriesy. Alternatively, one can read pages 5 and 6 of
_LurieNonCom_ cited below.

In any case, this motivates the following definition.



## Definition

### Simplicial/geometric definition 

A **monoidal ($\infty,1$)-category** $(C, \otimes)$
is 

* a [[simplicial set]] $C^\otimes$;

* and a coCartesian fibration of simplicial 
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

## Higher monoidal structure 

While for an ordinary [[monoid]] there is just one notion of commutativity (either it is or it is not commutative), already a [[monoidal category]] distinguishes between being just [[braided monoidal category|braided monoidal]] or fully [[symmetric monoidal category|symmetric monoidal]].

This pattern continues, as expressed by the [[k-tuply monoidal n-category|periodic table of k-tuply monoidal categories]].

A [[higher category theory|higher category]] may be a [[k-tuply monoidal n-category]] or more generally [[k-tuply monoidal (n,r)-category]] for different values of $k$. The lowest value of $k= 1$ (since for $k = 0$ there is no monoidal structure at all) corresponds to monoidal product which is $\infty$-associative, i.e.  associative up to higher coherent homotopies, but need not have any degree of _commutativity_. 

One says that an $n$-category is _symmetric monoiodal_ if it is "as monoidal as possible", i.e. $\infty$-tuply monoidal. In particular, in [[higher algebra|Noncommutative algebra]] and [[higher algebra|Commutative algebra]] we have

* the 1-fold monoidal (∞,1)-categories described here;

* [[symmetric monoidal (infinity,1)-category|∞-tuply monoidal (∞,1)-categories]].

### Operadic/algebraic definition of monoidal structure

For each $1 \leq n \leq \infty$ let $E_n$ denote the [[little n-disk operad|little n-disk]] [[operad]] whose [[topological space]] of $E_n^k$ of $k$-ary operations is the space of embeddings of $k$ $n$-dimensional disks (balls) in one $n$-dimensional disk without intersection, and whose composition operation is the obvious one obtained from gluing the big outer disks into given inner disks.

In [John Francis' PhD thesis](http://dspace.mit.edu/handle/1721.1/43792)  the theory of [[(∞,1)-categories]] equipped with an action of the $E_n$-[[operad]] is established, so that

* $(\infty,1)$-categories with an $E_1$-action are precisely [[monoidal (∞,1)-categories]]  -- 1-fold monoidal $(\infty,1)$-categories;

* $(\infty,1)$-categories with an $E_\infty$-action are precisely [[symmetric monoidal (∞,1)-categories]] -- $\infty$-tuply monoidal $(\infty,1)$-categories;

* $(\infty,1)$-categories with an $E_n$-action for $1 \lt n \lt \infty$ are the corresponding $n$-tuply monoidal $(\infty,1)$-categories in between.

>**Remark** The second statement is example 2.3.8 in [EnAction](http://dspace.mit.edu/handle/1721.1/43792). The first seems to be clear but is maybe not in the literature. Jacob Lurie is currently rewriting [[higher algebra|Higher Algebra]] such as to build in a discussion of $E_n$-operadic structures in the definition of $k$-tuply monoidal $(\infty,1)$-categories.

## Related concepts

* [[monoidal category]], **monoidal $(\infty,1)$-category**

* [[symmetric monoidal category]], [[symmetric monoidal (∞,1)-category]]

* [[closed monoidal category]] ,  [[closed monoidal (∞,1)-category]]



## References

the simplicial definition is definition 1.1.2 in 

* [[Jacob Lurie]], _Noncommutative algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))

John Francis' work on [[little cubes operad]]-actions on  $(\infty,1)$-categories is in

* [[John Francis]], PhD thesis ([web](http://dspace.mit.edu/handle/1721.1/43792))
{#Francis}


[[!redirects monoidal (infinity,1)-categories]]
[[!redirects monoidal (∞,1)-category]]
[[!redirects monoidal (∞,1)-categories]]