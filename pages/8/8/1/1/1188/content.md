
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Coontents#
* tic
{: toc}


## Idea

The notion of **accessible $(\infty,1)$-category** is the generalization of the notion of [[accessible category]] from [[category theory]] to [[(∞,1)-category]] theory.

It is a means to handle $(\infty,1)$-categories that are not [[essentially small (∞,1)-category|essentially small]] in terms of small data.

An _accessible_ $(\infty,1)$-category is one which may be [[large category|large]], but can entirely be _accessed_ as an $(\infty,1)$-category of "conglomerates of objects" in a small $(\infty,1)$-category -- precisely: that it is a category of $\kappa$-small [[ind-object]]s in some small $(\infty,1)$-category $C$.


## Definition 

+-- {: .un_defn}
###### Definition

A [[quasi-category]] $C$ is **accessible** if it satisfies the following equivalent conditions

* for some [[regular cardinal]] $\kappa$ $C$ is equivalent to the quasi-category  $Ind_\kappa(C^0)$ of [[ind-object in an (infinity,1)-category|ind-objects]] for a small $(\infty,1)$-category $C^0$;

* it is [[locally small (∞,1)-category|locally small]] and for some [[regular cardinal]] $\kappa$ it admits $\kappa$-[[filtered colimit]]s and is generated under such from the full [[sub-quasi-category]] of $\kappa$-[[compact object]]s, which is itself an [[essentially small (∞,1)-category]];

* for some [[regular cardinal]] $\kappa$,  $C$ admits small $\kappa$-[[filtered colimits]] and contains an [[essentially small (∞,1)-category|essentially small]] [[sub-quasi-category|full subcategory]] which consists of $\kappa$-[[compact object in an (infinity,1)-category|compact]] objects and generates $C$ under small $\kappa$-[[filtered colimit]]s;

* it is an [[idempotent-complete quasi-category]].

=--

The equivalence of these conditions is discussed below.

An [[(∞,1)-functor]] between accessible $(\infty,1)$-categories that preserves $\kappa$-filtered colimits is called an **[[accessible (∞,1)-functor]]** .


## Properties


### Equivalent characterizations

+-- {: .un_theorem}
###### Theorem

The characterizations of accessible $(\infty,1)$-categories are indeed all equivalent.

=--

+-- {: .proof}
###### Proof

For the first few this is [[Higher Topos Theory|HTT, prop. 5.4.2.2]]. For the last one this is in section 5.4.3.

=--

### Stability under various operations

+-- {: .un_theorem}
###### Theorem

If $C$ is an accessible quasi-category then so are

* for $K$ a small simplicial set the [[(∞,1)-category of (∞,1)-functors]] $Func(K,C)$;

* for $p : K \to C$ a small [[diagram]], the [[over quasi-category]] $C_{/p}$ and under-quasi-category $C_{p/}$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT]] section 5.4.4, 5.4.5 and 5.4.6.

=--


+-- {: .un_theorem}
###### Theorem

The [[homotopy pullback]] of accessible quasi-categories (in the [[model structure for quasi-categories]]) is again accessible.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, section 5.4.6]].

=--

## The $(\infty,1)$-category of accessible $(\infty,1)$-categories


+-- {: .un_def}
###### Definition


Write $Acc(\infty,1)Cat \subset (\infty,1)Cat$ for the 2-[[sub-(∞,1)-category]] of [[(∞,1)Cat]] on

* those objects that are accessible $(\infty,1)$-categories;

* those morphisms for which there is a $\kappa$ such that the [[(∞,1)-functor]] is $\kappa$-continuous and preserves $\kappa$-[[compact object]]s.

=--

So morphisms are the [[accessible (∞,1)-functor]]s that also preserves [[compact object]]s. (?)

This is [[Higher Topos Theory|HTT, def. 5.4.2.16]].

+-- {: .un_prop}
###### Proposition

The full [[sub-quasi-category]] $Acc(\infty,1)Cat \hookrightarrow (\infty,1)Cat$ is a [[reflective sub-(∞,1)-category]]

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, section 5.4.2.18]].

=--


## References 

The theory of accessible 1-categories is described in 

* Adamek and Rosicky, _Locally presentable and accessible categories_, Cambridge University Press (1994)

The theory of accessible $(\infty,1)$-categories is the topic of section 5.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects accessible (infinity,1)-categories]]
[[!redirects accessible (∞,1)-category]]
[[!redirects accessible (∞,1)-categories]]