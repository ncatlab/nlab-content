
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Contents#
* table of contents
{: toc}


## Idea

The notion of **accessible $(\infty,1)$-category** is the generalization of the notion of [[accessible category]] from [[category theory]] to [[(∞,1)-category]] theory.

It is a means to handle $(\infty,1)$-categories that are not [[essentially small (∞,1)-category|essentially small]] in terms of small data.

An _accessible_ $(\infty,1)$-category is one which may be [[large category|large]], but can entirely be _accessed_ as an $(\infty,1)$-category of "conglomerates of objects" in a small $(\infty,1)$-category -- precisely: that it is a category of $\kappa$-small [[ind-object]]s in some small $(\infty,1)$-category $C$.

A $\kappa$-accessible $(\infty,1)$-category which in addition has all [[(∞,1)-colimits]] is called a  _[[locally presentable (∞,1)-category|locally ∞-presentable]]_ or a _$\kappa$-[[compactly generated (∞,1)-category]]_.

## Definition 

Let $\kappa$ be a [[regular cardinal]]. 
 
+-- {: .num_defn}
###### Definition

A [[(∞,1)-category]] $\mathcal{C}$ is **$\kappa$-accessible** if it satisfies the following equivalent conditions:

1. There is a [[small (∞,1)-category]] $\mathcal{C}^0$ and an [[equivalence of (∞,1)-categories]] 

   $$
     \mathcal{C} \simeq Ind_\kappa(C^0)
   $$ 
  
   of $\mathcal{C}$ with the  [[(∞,1)-category of ind-objects]], relative $\kappa$, in $\mathcal{C}^0$.

1. The $(\infty,1)$-category $\mathcal{C}$ 

   1. is [[locally small (∞,1)-category|locally small]] 

   1. has all $\kappa$-[[filtered colimits]]

   1. the full [[sub-(∞,1)-category]] $\mathcal{C}^\kappa \hookrightarrow \mathcal{C}$ of $\kappa$-[[compact objects]] is an [[essentially small (∞,1)-category]];

   1. $\mathcal{C}^\kappa \hookrightarrow \mathcal{C}$ generates $\mathcal{C}$ under $\kappa$-[[filtered (∞,1)-colimits]].


1. The $(\infty,1)$-category $\mathcal{C}$ 

   1. is [[locally small (∞,1)-category|locally small]] 

   1. has all $\kappa$-[[filtered colimits]]

   1. there is _some_ [[essentially small (∞,1)-category|essentially small]]$\,$ [[sub-(∞,1)-category]] $\mathcal{C}' \hookrightarrow \mathcal{C}$ of $\kappa$-[[compact objects]] which generates $\mathcal{C}$ under $\kappa$-[[filtered (∞,1)-colimits]].

The notion of accessibility is mostly interesting for _large_ (∞,1)-categories. For

* If $\mathcal{C}$ is small, then there exists a $\kappa$ such that $\mathcal{C}$ is $\kappa$-accessible if and only if $\mathcal{C}$ is an [[idempotent-complete (∞,1)-category]].

Generally, $\mathcal{C}$ is called an **accessible $(\infty,1)$-category** if it is $\kappa$-accessible for some regular cardinal $\kappa$.

=--

+-- {: .num_prop}
###### Proposition

These conditions are indeed equivalent.

=--

For the first few this is [[Higher Topos Theory|HTT, prop. 5.4.2.2]]. The last one is in [[HTT|HTT, section 5.4.3]].

+-- {: .num_defn}
###### Definition

An [[(∞,1)-functor]] between accessible $(\infty,1)$-categories that preserves $\kappa$-filtered colimits is called an **[[accessible (∞,1)-functor]]** .

=--

+-- {: .num_defn}
###### Definition


Write $(\infty,1)AccCat \subset (\infty,1)Cat$ for the 2-[[sub-(∞,1)-category]] of [[(∞,1)Cat]] on

* those objects that are accessible $(\infty,1)$-categories;

* those morphisms for which there is a $\kappa$ such that the [[(∞,1)-functor]] is $\kappa$-continuous and preserves $\kappa$-[[compact object]]s.

=--

So morphisms are the [[accessible (∞,1)-functor]]s that also preserves [[compact object]]s. (?)

This is [[Higher Topos Theory|HTT, def. 5.4.2.16]].




## Properties




### Stability under various operations 
 {#StabilityUnderOperations}

+-- {: .num_theorem}
###### Theorem

If $C$ is an accessible $(\infty,1)$-category then so are

* for $K$ a small simplicial set the [[(∞,1)-category of (∞,1)-functors]] $Func(K,C)$;

* for $p : K \to C$ a small [[diagram]], the [[over quasi-category]] $C_{/p}$ and under-quasi-category $C_{p/}$.

=--


This is [[Higher Topos Theory|HTT]] section 5.4.4, 5.4.5 and 5.4.6.



+-- {: .num_theorem}
###### Theorem

The [[(∞,1)-pullback]] of accessible $(\infty,1)$-categories in [[(∞,1)Cat]] is again accessible.

=--


This is [[Higher Topos Theory|HTT, section 5.4.6]].


Generally:

+-- {: .num_theorem}
###### Theorem

The $(\infty,1)$-category $(\infty,1)AccCat$ has all small [[(∞,1)-limit]]s and the inclusion

$$
  (\infty,1)AccCAT \hookrightarrow (\infty,1)CAT
$$

preserves these.

=--

This is [[Higher Topos Theory|HTT, proposition 5.4.7.3]].


## Related concepts

* [[compactly generated (∞,1)-category]]

[[!include locally presentable categories - table]]



## References 

Theory of [[accessible categories|accessible 1-categories]]:

* {#AdamekRosicky} [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 

Theory of accessible $(\infty,1)$-categories:

* [[Jacob Lurie]], Section 5.4 of _[[Higher Topos Theory]]_

See also:

* {#Rezk2021} [[Charles Rezk]], *Generalizing accessible ∞-categories*, 2021 ([pdf](https://faculty.math.illinois.edu/~rezk/accessible-cat-thoughts.pdf)).


[[!redirects accessible (infinity,1)-categories]]
[[!redirects accessible (∞,1)-category]]
[[!redirects accessible (∞,1)-categories]]