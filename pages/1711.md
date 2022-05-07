
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
* automatic table of contents goes here
{:toc}


## Idea

A **$k$-transfor** is an operation from one $n$-[[n-category|category]] $C$ to another $D$ (for some value of $n$) that takes [[object|objects]] of $C$ to $k$-[[k-morphism|morphisms]] of $D$ (and more generally $j$-morphisms in $C$ to $(j+k)$-morphisms in $D$) in a coherent way.  Equivalently, a $k$-transfor is a $k$-cell in an [[internal-hom]] $n$-category.  Transfors are a common generalisation of:

* $n$-[[n-functor|functor]]s, which are 0-transfors
* $n$-[[natural transformation]]s, which are 1-transfors
* [[modifications]], which are 2-transfors,
* perturbations, which are 3-transfors,
* and so on.

The word "transfor" was coined by Sjoerd Crans in [this paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.26.506&rep=rep1&type=pdf); it is a _portmanteau_ of "functor" and "transformation."  A collection of components which forms a transfor is said to be *transforial*, as a generalization of "functorial" and "natural."


## Terminology

Once upon a time, there were [[categories]], [[functor|functors]] between them, and natural transformations between them.  Then when $n$-categories came along, people called the arrows between them '$n$-functors' even though one could just as easily say 'functors'.  In the same vein, people said '$n$-transformations' for natural transformations (that is, 2-transfors) between $n$-categories.  At the same time, we saw that we needed modifications between $n$-transformations, and that there would have to be things between higher modifications, and so on.  However, due to the prior use of "$n$-transformation" for a 2-transfor between $n$-categories, the natural choice "$k$-transformation" is unavailable to mean a $k$-transfor.

Here are some other possible terms for a $k$-transfor between $n$-categories, which additionally notate the value of $n$ (although this is, strictly speaking, unnecessary).

* $(n,k)$-transformation
* $n$-$k$-transfor
* $n$-dimensional $k$-transfor
* $n$-categorical $k$-transfor
* $n$-natural $k$-transformation


## Definitions

We haven\'t gotten around to saying anything precise yet, but you can see something in the discussion below, or in Crans\'s paper.


## Special cases

See this [[periodic table]] of $k$-transfors between $n$-categories for common names for low values of $n$ and $k$.  On the $n$-Lab, we tend to omit the prefix $n$- whenever possible (as ironic as that may be).

<table><tr><th markdown="1">$k$&#8595;\$n$&#8594;</th><th markdown="1">$-1$</th><th markdown="1">$0$</th><th markdown="1">$1$</th><th markdown="1">$2$</th><th markdown="1">$3$</th><th>...</th></tr>
<tr><th markdown="1">$0$</th><td>[[implication]]</td><td>[[function]]</td><td>[[functor]]</td><td markdown="1">$2$-[[2-functor|functor]]</td><td markdown="1">$3$-[[n-functor|functor]]</td><td>...</td></tr>
<tr><th markdown="1">$1$</th><td>trivial</td><td>[[equality]] of functions</td><td>[[natural transformation]]</td><td markdown="1">$2$-transformation</td><td markdown="1">$3$-transformation</td><td>...</td></tr>
<tr><th markdown="1">$2$</th><td>"</td><td>trivial</td><td>equality of natural transformations</td><td>[[modification]]</td><td markdown="1">$3$-modification</td><td>...</td></tr>
<tr><th markdown="1">$3$</th><td>"</td><td>"</td><td>trivial</td><td>equality of modifications</td><td>perturbation</td><td>...</td></tr>
<tr><th markdown="1">$4$</th><td>"</td><td>"</td><td>"</td><td>trivial</td><td>equality of perturbations</td><td>...</td></tr>
<tr><th markdown="1">$5$</th><td>"</td><td>"</td><td>"</td><td>"</td><td>trivial</td><td>...</td></tr>
<tr><th>&#8942;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>"</td><td>&#8945;</td></tr></table>

Note that the [[source]] and [[target]] of a $k$-transfor (between $n$-categories) are $(k-1)$-transfors (between the same $n$-categories).  Given two fixed source and target $(k-1)$-transfors, the $k$-transfors between them (and the $(k+1)$-transfors between those, and so on) form an $(n-k)$-category.

### For n-posets

A similar table [[periodic table]] of $k$-transfors between $n$-posets exists for common names for low values of $n$ and $k$. 

<table><tr><th markdown="1">$k$&#8595;\$n$&#8594;</th><th markdown="1">$-1$</th><th markdown="1">$0$</th><th markdown="1">$1$</th><th markdown="1">$2$</th><th markdown="1">$3$</th><th>...</th></tr>
<tr><th markdown="1">$0$</th><td>[[implication]]</td><td>[[monotonic function]]</td><td>[[functor]]</td><td markdown="1">$2$-[[2-functor|functor]]</td><td markdown="1">$3$-[[n-functor|functor]]</td><td>...</td></tr>
<tr><th markdown="1">$1$</th><td>trivial</td><td>[[partial order]] of monotonic functions</td><td>[[natural transformation]]</td><td markdown="1">$2$-transformation</td><td markdown="1">$3$-transformation</td><td>...</td></tr>
<tr><th markdown="1">$2$</th><td>"</td><td>trivial</td><td>partial order of natural transformations</td><td>[[modification]]</td><td markdown="1">$3$-modification</td><td>...</td></tr>
<tr><th markdown="1">$3$</th><td>"</td><td>"</td><td>trivial</td><td>partial order of modifications</td><td>perturbation</td><td>...</td></tr>
<tr><th markdown="1">$4$</th><td>"</td><td>"</td><td>"</td><td>trivial</td><td>partial order of perturbations</td><td>...</td></tr>
<tr><th markdown="1">$5$</th><td>"</td><td>"</td><td>"</td><td>"</td><td>trivial</td><td>...</td></tr>
<tr><th>&#8942;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>"</td><td>&#8945;</td></tr></table>

## Discussion ##

This discussion was originally at [[modification]].  It discusses both terminology and definitions.

+-- {: .query}
[[Finn Lawler|Finn]]: There is a pattern here: functors
are indexed collections of objects, natural
transformations are i.c.s of 1-cells, modifications i.c.s
of 2-cells; and these are what make the collection of all
$n$-categories into an $n+1$-category, for $0 \leq n \leq
2$ anyway.  Any references for the pattern in higher
dimensions?

_Toby_:  Do you mean for the terminology or for the appropriate coherence laws? (the details that you\'ve been leaving out).  Not that I have either ...

Incidentally, I corrected 'function' to 'functor' in you question above; I hope that\'s OK.

[[Finn Lawler|Finn]]:  I meant terminology and/or an explanation for arbitrary $n$ (which Urs gives below).

Actually I was thinking of functions rather than functors, as they are the 1-cells in $0-Cat$.  But of course functions are just functors between discrete categories, and thinking of them as the latter probably makes more sense when moving to higher dimensions.

_Toby_:  Now, I would either have said 'functors are indexed collections of objects' or 'functions are indexed collections of elements'; your mixture confused me!  (^_^)

_Finn_:  Ah!  Point taken.  In any case, I should have said '0-cell' instead of 'object'.  But I think 'functor' is better anyway, as I said.

[[Urs Schreiber|Urs]]: the pattern that Finn is looking for is that embodied in the nature of the [[internal hom]] of the [[closed monoidal structure on presheaves]].

In its most general form, consider an [[infinity-category]] modeled as a [[simplicial set]] with certain properties. Being a simplicial set, this is a presheaf on the [[simplex category]]. Hence for $X$ and $Y$ such $\infty$-categories, the $\infty$-category of morphisms between them corresponds to the internal hom simplicial set
$$
  [X,Y] = Hom_{SSet}(X \times \Delta^\bullet, Y)
  \,.
$$

This simple formula encodes that pattern that Finn observed. It says that:

* [[functor]]s (the 0-cells in $[X,Y]$) are just maps $X \to Y$ from cells to cells;

* [[natural transformation]]s (the 1-cells in $[X,Y]$) are maps $X \times \Delta^1 \to Y$. Notice that $\Delta^1$ is the [[interval object]] in $SSet$ (or at least its Kanification is, but never mind that for the moment). Such maps send $n$-cells in $X$ to $(n+1)$-cells in $Y$.

* modifications are maps $X \times \Delta^2 \to Y$, that map $n$-cells in $X$ to $(n+2)$-cells in $Y$.

It may be helpful to realize the same pattern in the globular context of, for instance, [[strict omega-category]]. These are certain presheaves not on the [[simplex category]] but on the [[globe category]], but the pattern is the same: the [[internal hom]] strict $\omega$-category of morphisms between strict $\omega$-categories $X$ and $Y$ is
$$
  [X,Y] = Hom_{\omega Cat}(X \otimes G^\bullet , Y)
  \,,
$$
where now the tensor product appearing is no longer the cartesian one but the [[Crans-Gray tensor product]] and where $G^n$ is the standard globular $n$-globe. Again $G^1$ is a model for the [[interval object]] and we see that

* functors are morphisms $X \to Y$;

* transformations are morphisms $X \otimes G^1 \to Y$

* modifications are morphisms $X \otimes G^2 \to Y$

etc. Same logic as before.

When thinking about this, it may be useful to explicitly apply the hom-adjunction everywhere and think for instance of a natural transformation as a morphism

$$
  X \to [I,Y]
$$

from $X$ into the "category of cylinders in $Y$". This is maybe the most intuitive way: if for instance $Y$ happens to be just a 2-category, then this says that a transformation between functors between 2-categories is a 1-functor from the 1-category underlying $X$ to the category of cylinders in $Y$ (satisfying some property). Which is exactly what it is, in components.

When in a certain mood, I like to think of this basic fact, that $n$-fold transformations between $k$-functors are essentially (in components) $(k-n)$-functors with values in $n$-cylinders as the "holographic principle" in category theory. That may sound a bit silly, but it is true that in the case the $k$-functors in questions are $k$-functors on $Bord_k$ respresenting $k$-dimensional [[quantum field theory]], then teir transformations, being $(k-1)$-functors, represent $(k-1)$-dim QFT, and this relation between higher and lower dim QFT is called "holography" in phyiscs.

[[Finn Lawler|Finn]]:  Cool!  Thanks, Urs.  I might move this section to an article on $n$-[[n-transformation|transformations]] (if that's what they're called) once I get my head around it properly.

_Toby_:  Unfortunately, '$n$-transformation' already (following '$n$-functor') means a transformation between functors between $n$-categories.  See [Cheng--Gurski](http://cheng.staff.shef.ac.uk/degeneracy/cheng-gurski-degeneracy.pdf) for this, along with '$n$-modification' and even '$n$-perturbation' (gee, that doesn\'t conflict with anything else, does it?), along with the claim that there is 'no existing terminology' thereafter.

I would probably say '$n$-morphism in $n Cat$' (possibly with two different values of $n$); you can use '$n$-cell' in place of '$n$-morphism' if you like.  But it would be nice to find something more specific that\'s not already taken.  Or we could just throw out the Cheng--Gurski meaning of '$n$-transformation'; although it\'s not unique to them, it may not be too entrenched yet.

(But please let a transformation be a $1$-transformation, even though it is a $2$-morphism.)

[[Todd Trimble|Todd]]: I think what Urs and Crans both may be suggesting is that, at least in the context of strict $n$- and $\omega$-categories, there is a uniform notion of "transformation of depth k between n-functors", or just $(n, k)$-transformations, where $(n, 1)$-transformations are usual transformations between $n$-functors, $(n, 2)$-transformations are modifications, and so on. Surely this usage won't conflict with Cheng-Gurski. 

_Toby_:  Yeah, that would work, so we could write [[(n,k)-transformation]].  My only disgruntlement is that the $n$ is superfluous; the problem is all those other people that are already using it and preventing us from unambiguously saying simply '$k$-transformation'!

_Finn_: Probably tiros like me shouldn't have a say in this sort of thing, but I would tend to agree with Toby here, that the $k$ is at least more interesting than the $n$, in that you're more likely to vary the values of $k$ than those of $n$.  However, typing the few extra characters does seem a small price to pay to avoid horrible confusion.  I slightly reluctantly vote for $(n,k)$. 

_Todd_: I'm not crazy about it either, but I agree it's a small price. I'll note (in case it helps) that in the general theory of Crans-Gray tensor products, both variations in $n$ and $k$ come up, about equally often (e.g., the tensor of a 1-category and an $n$-category is an $(n+1)$-category). 

[[Urs Schreiber|Urs]]: yes, so to summarize what I think the main points are

* there is a systematic notion of "transformation of depth k between n-functors" for [[geometric definition of higher category]] in terms of simplicial sets;

* the corresponding notion in the (strict) globular context is formalized by Crans' construction;

* unwrapping what this says, it yields in particular that a transformation of depth $k$ between strict globular $n$-categories $X$ and $Y$ is an $(n-k)$-functor from the truncation $X{\leq k}$ of $X$ to an $(n-k)$-category (throwing all higher cells away) to the $(n-k)$-category of $k$-globes in $Y$ (also truncated)
$$
  \eta : X_{\leq k} \to [G^k, Y]|_{\leq k}
$$
satisfying certain naturality conditions (which ensure precisely that $\eta$ extends uniquely to an $n$-functor
$
  \eta : X \to [G^k,Y]
$). 

JCMcKeown: not meaning to cause annoyance, but how about calling them "$+k$-transformations", owing to their incrementing dimensions by $k$; or if we don't like the $+$ prefix, one might call them $k$-vexilors, because they tend to generate flags of period $k$.

_Toby_:  Interesting; can you explain more about how they generate flags?  (Maybe that\'s something to put in a new section here, or you could just give a reference.)

[[JCMcKeown]]: Just from reading above "... and more generally $j$-morphisms in $C$ to $(j+k)$-morphisms in $D$"... ahah! Now I see what you're getting at.  I've got my head fixed on _endo_-functors; where if you wanted to (I don't mean it's a *good* idea.  Who knows?) you can consider iterations of the underlying function that is the $+k$-transformation.

[[Mike Shulman]]: FWIW, Sjoerd Crans has called these things **k-transfors**, and speaks of something being *transforial* as a general term including both "functorial" and "natural."

_Toby_:  I\'m inclined to say that we should go with that!

[[Mike Shulman]]: I'm not sure how serious you are... but I've always thought it was a proposal that deserved to be taken more seriously than it seems to have been.  The reference is "Localizations of Transfors," _K-Theory_ 2004 (I can't find a free version online).

_Toby_:  I\'m perfectly serious.  The term *should* be indexed primarily by $k$, with $n$ only if one really insists.  I didn\'t want to make up my own word, but if Crans has published one, then why not use it?  I should be able to check that reference the next time that I visit the UCR library (about once a week).

[[Mike Shulman]]: No argument here (about indexing by $k$).  Also $(n,k)$-transformation sounds to me like something to do with [[(n,r)-categories]], but there of course the comma denotes something completely different. 

[[Todd Trimble]]: I like $k$-transfor. 

[[Mike Shulman]]: [Found it](http://home.tiscali.nl/secrans/papers/lotr.html)

_Toby_:  Excellent!  Since [[Finn Lawler|Finn]] and [[JCMcKeown]] have not been active lately, I\'ll move it over with that paper as a guide (or you can).

I would like to *also* mention '$(n,k)$-transformation' (or maybe '$n$-$k$-transfor'?) as a possible term, however, since some people might want to specify $n$ just as some people like to say '$n$-functor'.

_Toby_:  One could also say '$n$-natural $k$-transformation', which fits (what Crans claims on page 2 to be standard) '$2$-natural transformation' for a strict $(2,1)$-transformation.  But I still like '$k$-transfor' when $n$ is suppressed (which should be the default).

_Mike_: What about "$n$-categorical $k$-transfor" if it is necessary to specify $n$?

_Toby_:  That works too.  (Well, I don\'t like 'categorical', but that\'s a separate issue.)
=--


## Related concepts

* [[homotopy]]

* functors

  * [[functor]]

  * [[2-functor]]

  * [[(∞,1)-functor]]

* transformations

  * [[natural transformation]]

  * [[pseudonatural transformation]] / [[lax natural transformation]]

  * [[(∞,1)-natural transformation]]

  * [[(∞,n)-natural transformation]]

* modifications

  * [[modification]]

## References for the globular approach
[[Camell Kachour]]: Kamel Kachour, D&#233;finition alg&#233;brique des cellules non-strictes, Cahiers de Topologie et de G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;gorique (2008), volume 1, pages 1&#8211;68. 

[[Camell Kachour]]: Steps toward the Weak &#969;-category of the Weak &#969;-categories in the globular setting, Published Categories and General Algebraic Structures with Applications (2015). 



[[!redirects (n,j)-transformation]]
[[!redirects j-transformation]]
[[!redirects k-transformation]]
[[!redirects n-transformation]]
[[!redirects (n,j)-transformations]]
[[!redirects (n,k)-transformation]]
[[!redirects (n,k)-transformations]]
[[!redirects j-transformations]]
[[!redirects k-transformations]]
[[!redirects n-transformations]]
[[!redirects k-transfor]]
[[!redirects k-transfors]]
[[!redirects transfors]]

[[!redirects n-natural transformation]]
[[!redirects n-natural transformations]]
