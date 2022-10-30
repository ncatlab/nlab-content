[[!redirects categories with the same collection of objects]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}


## Idea

### Background comments

Despite the impression one may get from standard texts, the notion of a *[[category]]* (in [[category theory]]) exists in (at least) two distinct versions, which, while closely related, are crucially different in a way that matters when paying attention to fine-print. Namely, categories are traditionally introduced as being [[mathematical structures]] consisting of a [[class]] of [[objects]], etc. ("[[strict categories]]", see below)  but in further discussion these are eventually often regarded as being themselves the objects of the [[2-category]] [[Cat|$CAT$]] of [[categories]], [[functors]] and [[natural transformations]] between these. While this change of perspective may superficially seem to only increase the level of sophistication of the discussion, it actually loses information: By default of [[2-category theory]], the objects of a [[2-category]] like [[CAT]] are identifiable only up to [[equivalence in a 2-category|2-categorical equivalence]] -- which here means: up to [[equivalence of categories]] -- but under this relation the notion of "class of objects" of a category is not fixed (not fixed up to [[isomorphism]], that is) and hence makes no invariant sense: Regarding a category as an object of [[CAT]] (and nothing more), means to *forget* its precise class of objects.

For example, when assuming the relevant [[axiom of choice]], then the [[codiscrete category]] on any [[set]] $S$ (whose class of objects is $S$) is [[equivalence of categories|equivalent]] to the [[terminal category]] (whose class of objects is the [[singleton set]]). From the point of view of the "[[principle of equivalence]]" appropriate within [[CAT]], all these categories are effectively indistinguishable, and yet one finds a strict representative in this equivalence class with any imaginable class of objects.

In order to bring out this distinction, some authors say "[[strict category]]" for the notion of "category" where a class of objects is fixed. While this specific terminology is not common, the notion itself is tacitly ubiquituous: For example, when people say that the [[simplicial nerve]]-construction fully embeds [[small categories]] into [[simplicial sets]] (namely as those which satisfy the [[Segal conditions]]) then they are implicitly referring to such strict categories: Their fixed set of objects constitutes the degree-0 component of their nerve simplicial set.

The point of the following definition of "category with atlas" is to bring out the notion of "strict category" in a way that is itself intrinsic to [[2-category theory]] -- or rather: internal to [[2-topos theory]].

### Idea of the definition

By a *category with an atlas* we shall mean a [[category]] $\mathcal{C}$ which is equipped with an [[essentially surjective functor]] 

\[
  \label{AnAtlasOnACategory}
  C_0 
    \twoheadrightarrow 
  \mathcal{C}
\]

from a [[set]] (or [[class]]) $C_0$ regarded as a ([[large category|large]]) [[discrete category]]. This is an "invariant"  or "intrinsic" way of speaking (namely [[internal language|internal]] to the [[2-topos]] [[CAT]]) about categories which are equipped with a notion of a fixed class of objects. Another terminology for this is "[[strict categories]]", but saying "category with atlas" naturally connects to the well-established notion of *[[atlas]]* in the context of [[stacks]], maybe most commonly used in the literature on [[topological stacks]]: 

An [[atlas]] for a [[topological stack]] $\mathscr{X}$ is classically taken to be a [[topological space]] $X_0$ and an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] $X_0 \twoheadrightarrow \mathscr{X}$. Given this, its [[homotopy fiber product|homotopy]]-[[Cech nerve]] $X_0 \times_{\mathscr{X}} X_0 \rightrightarrows X_0$ is known as the corresponding *[[topological groupoid]]*, whose space of [[objects]] is nothing but $X_0$. 

By the [[Giraud-Rezk-Lurie theorem]], this state of affairs holds in any [[(2,1)-topos]] of [[stacks]]: The [[groupoid object in an (infinity,1)-category|groupoid objects]] in the underlying [[1-topos]] are equivalently the [[stacks]] equipped with an atlas, namely the objects in the [[(2,1)-topos]] which are equipped with an effective epimorphism out of a [[0-truncated]] object.

If here the the underlying [[site]] is the [[terminal category]], then "stacks" are groupoids regarded up to [[equivalence of groupoids]] and "stacks with atlas" are groupoids equipped with a choice of a fixed set of objects. This is just the notion of "category with an atlas" restricted to categories that happen to be groupoids. 

In short, we have the following dictionary:

| stack theory  | stack theory over the point | category theory |
|---------------|----------------------------|-----------------|
|  stack        |          groupoid          |    groupoid     |
| stack with atlas |  groupoid with atlas    | strict groupoid |

But it is common to understand "[[stacks]]" in the generality of category-valued stacks: [[2-sheaves]]. Now a stack/2-sheaf over the point is just a bare category, and this way the notion of "category with an atlas" blends seamlessly into established terminology in stack theory.


### Consequences of the definition
 {#ConsequencesOfTheDefinition}

The advantage of thinking of [[strict categories]] more intrinsically as *categories equipped with an atlas* (eq:AnAtlasOnACategory) is that it immediately implies natural definitions for a variety of related notions. 

For example, the correct category of categories-with-atlas is evidently the full sub 2-category of the $(2,1)$-[[comma category]] $SET/CAT$ on the essential surjections, whose morphisms from $(C_0 \twoheadrightarrow \mathcal{C})$ to $(D_0 \twoheadrightarrow \mathcal{D})$ are squares in $Ho_{(2,1)}(CAT)$ of the form

\begin{tikzcd}
  C_0
  \ar[d, ->>]
  \ar[rr, "{F_0}"]
  &&
  D_0
  \ar[d, ->>, "{\ }"{swap, name=s}]
  \\
  \mathcal{C}
  \ar[rr, "{\ }"{name=t}, "{F}"{swap}]
  &&
  \mathcal{D}
  \ar[from=s, to=t, Rightarrow, "\sim"{sloped}]
\end{tikzcd}

Similarly, for a given [[class]] $C_0$ of objects are naturally the morphisms in the analogous full sub-$(2,1)$-category of the [[co-slice category|co-slice]] of [[CAT]] under $C_0$ are of the form:

\begin{tikzcd}
  & 
  C_0
  \ar[dl, ->>]
  \ar[dr, ->>, "{\ }"{swap, name=s}]
  \\
  \mathcal{C}
  \ar[rr, "{\ }"{name=t}, "F"{swap}]
  &&
  \mathcal{C}'
  \ar[from=s, to=t, Rightarrow, "\sim"{sloped}]
\end{tikzcd}

Notice that this is slightly more general than what one might call an "[[identity-on-objects functor]]", but it naturally appears in practice. 


\linebreak




## See also

* [[atlas]]

* [[identity-on-objects functor]]

* [[Freyd category]]

* [[Freyd multicategory]]

* [[dagger category]]


## References

A generalization of the notion to [[higher category theory]] is considered (under the name "flagged categories") in

* [[David Ayala]], [[John Francis]], Def. 0.12 of: *Flagged higher categories*, in *Topology and Quantum Theory in Interaction*. Contemporary Mathematics **718** (2018) &lbrack[arXiv:1801.08973](https://arxiv.org/abs/1801.08973)&rbrack;





[[!redirects categories with the same type of objects]]
[[!redirects categories with the same class of objects]]
[[!redirects categories with the same set of objects]]

[[!redirects functor between categories with the same collection of objects]]
[[!redirects functor between categories with the same type of objects]]
[[!redirects functor between categories with the same class of objects]]
[[!redirects functor between categories with the same set of objects]]

[[!redirects functors between categories with the same collection of objects]]
[[!redirects functors between categories with the same type of objects]]
[[!redirects functors between categories with the same class of objects]]
[[!redirects functors between categories with the same set of objects]]