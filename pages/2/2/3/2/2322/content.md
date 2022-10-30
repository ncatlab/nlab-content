
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A crucial ingredient in a [[topos]] is a [[subobject classifier]]. That this has to do with [[subobjects]] turns out to the a coincidence of low dimensions: subobjects are [[(-1)-truncated]] morphisms. 

As discussed also at [[stuff, structure, property]], the classifying objects in [[higher topos theory]] classify more general morphisms.

When one passes all the way to $\infty$-toposes, there should be objects that classify _all_ morphisms, subject to some bound on size. This is made precise in the context of [[(∞,1)-topos theory]].

One way to characterize an [[(∞,1)-topos]] is as 

* a [[presentable (∞,1)-category]]

* with [[universal colimits]]

* such that for all sufficiently large [[regular cardinal]]s $\kappa$ there is a **classifying object** for the class of all $\kappa$-compact morphisms in $X$.

This statement is originally due to [[Charles Rezk]]. It is reproduced as theorem 6.1.6.8 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

In terms of [[homotopy type theory]] these object classifiers are _[[types of types]]_.

## Details

### Subobject classifier {#DetailsSubObjClassf}

+-- {: .num_defn}
###### Definition

Let $C$ be an [[(∞,1)-category]] and $S \in C_1$ a class of [[morphisms]] that is stable under [[(∞,1)-pullback]] in $C$.

Let $Cod_C$ be the [[codomain fibration]] of $X$, i.e. the [[(∞,1)-category of (∞,1)-functors]]

$$
  Cod_C := Func(\Delta[1], C)
$$

equipped with the [[Cartesian fibration]] $Cod_C \to C$ induced from the endpoint inclusion $Delta[0] \to \Delta[1]$.

Write

* $Cod_C^S$ for the full [[sub-(∞,1)-category]] of $Cod_C$ on the object in $S$;

* $Cod_C^{(S)}$ the non-full subcategory whose objects are the elements of $S$, and whose morphisms are squares that are pullback diagrams.

Then evaluation at $\Delta[0] \to \Delta[1]$ yields

* a [[Cartesian fibration]] $Cod_C^S \to C$;

* a [[right fibration]] $Cod_C^{(S)} \to C$.

We say a morphism $f :x \to y$ in $C$ _classifies_ $S$ -- or simply that $y$ classifies $S$ -- if it is the [[terminal object]] in $Cod_C^{(S)}$.

=--

This is [[Higher Topos Theory|HTT, notation 6.1.3.4]] and [[Higher Topos Theory|HTT, def. 6.1.6.1 ]].

+-- {: .num_defn}
###### Definition

A **subobject classifier** for $C$ is an object that classifies the class $S$ of [[monomorphism in an (∞,1)-category|monomorphisms]]/[[(-1)-truncated]] morphisms in $C$.

=--

This is ([[Higher Topos Theory|HTT, def. 6.1.6.1 ]]).


+-- {: .num_example}
###### Example

The $(\infty,1)$-category [[∞Grpd]] has a a subobject classifier: the [[0-groupoid]]/[[set]] $\{\emptyset,*\}$ with two elements (the two [[(-1)-truncated]] $\infty$-groupoids).

=--

+-- {: .num_prop}
###### Proposition

Every [[(∞,1)-topos]] has a [[subobject classifier]].

=--



This appears as ([[Higher Topos Theory|HTT, prop. 6.1.6.3]]) and the remark below that.


### Object classifier {#DetailsObjClassf}


**Remark/Warning.** However, the point of having [[subobject]]s and hence [[monomorphism]]s classified by an object in an ordinary [[topos]] may be thought of as being solely due to the fact that in a 1-[[topos]], any object necessarily classifies a _set_  (or rather a [[poset]] i.e. a [[0-category]] or rather a [[(0,1)-category]]) of morphisms, and the point of subobjects/monomorphisms of a given object is that they don't have [[automorphism]]s and hence indeed form a set (or rather: [[poset]]).

In an $(\infty,1)$-topos we might thus expect an object that classifies _all_ morphisms, in that the assignment

$$
  c \mapsto Core(C_{/c})
$$

of an object $c\in C$ to the [[core]] of its [[over quasi-category|over (∞,1)-category]] yields a [[(∞,1)-functor]] $C^{op} \to \infty Grpd$ that is [[representable functor|representable]].

Indeed, this is _essentially_ the case -- up to size issues, that the following definitions take care of.

+-- {: .num_defn #RelativelyKappaCompact}
###### Definition

For $\kappa$ some [[cardinal]], say a morphism $f : x \to y$ in $C$ is **relatively $\kappa$-compact** if for all [[(∞-1)-pullbacks]] along $h : y' \to y$ to $\kappa$-[[compact object in an (∞,1)-category|compact object]]s, $y'$, the pulled back object $h^* x'$ is itself a $\kappa$-compact object.

=--


+-- {: .num_theorem}
###### Theorem

A [[presentable (∞,1)-category]] $C$  is an [[(∞,1)-topos]] precisely if

1. it has [[universal colimits]];

1. for sufficiently large regular [[cardinal]]s $\kappa$, $C$ has a classifying object for relatively $\kappa$-compact morphisms.

=--


This is due to [[Charles Rezk]]. The statement appears as [[Higher Topos Theory|HTT, theorem 6.1.6.8]].



## Examples

### Object classifier in $\infty Grpd$
  {#ObjectClassifierInInfinityGroupoid}

Let $Z|_{\infty Grpd} \to \infty Grpd$ be the 
[[universal right fibration]].

Let 

$$
  Type_\kappa := Core(\infty Grpd_\kappa) \to \infty Grpd
$$ 

be the [[core]] of the full [[sub-(∞,1)-category]] of [[∞Grpd]] on the 
$\kappa$-[[compact object in an (infinity,1)-category|compact ∞-groupoids]], regarded as a [[Kan complex]].

Let 

$$
  \array{
    \widehat Type_\kappa &\to& Z_{\infty Grpd}
    \\
    \downarrow && \downarrow
    \\  
    Type_\kappa &\to& \infty Grpd 
  }
$$

be the [[pullback]] (of [[simplicial sets]]) of the universal right fibration along this inclusion.

Since [[right fibrations]] are stable under pullback (see [here](http://ncatlab.org/nlab/show/right%2Fleft+Kan+fibration#PreservationByPullback)), this is still a right fibration. Since, up to equivalence, every morphism into a [[Kan complex]] is a 
right fibration (see [here](http://ncatlab.org/nlab/show/right%2Fleft+Kan+fibration#OverKanComplex)), and since every
morphism out of a Kan complex into $\infty Grpd_\kappa$ factors
through the core $Type_\kappa$ it follows that
$Type_\kappa$ classifies all morphisms $X \to Y$ in [[∞Grpd]]
whose [[homotopy fibers]] 

$$
  X_y \simeq X \times_Y \{y\}
$$ 

are $\kappa$-[[compact object in an (∞,1)-category|compact]].

Every such morphism $X \to Y$ is also relatively $\kappa$-compact, def. \ref{RelativelyKappaCompact}.
Because, we may write $Y$ as an [[(∞,1)-colimit]] over itself (see there)

$$
  Y \simeq {\lim_{\to}}_{y \in Y} \{y\} 
$$

and then use the fact that [[∞Grpd]] -- being an [[(∞,1)-topos]] -- has 
[[universal colimits]], to obtain the [[(∞,1)-pullback]] diagram

$$
  \array{
    {\lim_{\to}}_{y \in Y} X_y 
      &\stackrel{\simeq}{\to}
     & X
    \\
    \downarrow && \downarrow
    \\
    {\lim_{\to}}_{y \in Y} \{y\}
    &\stackrel{\simeq}{\to}&
    Y
  }
$$

exhibiting $X$ as an $(\infty,1)$-colimit of $\kappa$-small objects
over $Y$. By stability of $\kappa$-compact objects under
$\kappa$-small colimits (see [here](http://ncatlab.org/nlab/show/compact+object+in+an+%28infinity%2C1%29-category#StabilityUnderColimits))
it follows that $X$ is $\kappa$-compact if $Y$ is. 

## Related concepts

* [[type of propositions]], [[subobject classifier]]

* [[type of types]]




[[!redirects object classifier]]
[[!redirects object classifiers]]
[[!redirects (sub)object classifier in an (∞,1)-topos]]
[[!redirects (sub)object classifiers in an (∞,1)-topos]]
[[!redirects (sub)object classifiers in an (infinity,1)-topos]]
