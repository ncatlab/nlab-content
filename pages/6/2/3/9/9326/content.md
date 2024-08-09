
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #coCartesianFibrationOfInfinityOperads}
###### Definition

Let $\mathcal{O}^\otimes$ be an [[(∞,1)-operad]]. A **coCartesian fibration of (∞,1)-operads** is

1. a [[coCartesian fibration]] $p : \mathcal{C}^\otimes \to \mathcal{O}^\otimes$ of the underlying [[quasi-categories]];

1. such that the composite 

   $$
     \mathcal{C}^\otimes \stackrel{p}{\to} \mathcal{O}^\otimes \to FinSet^{*/} = Comm^\otimes
   $$

   exhibits $\mathcal{C}^\otimes$ as an [[(∞,1)-operad]].

In this case we say that the underlying [[(∞,1)-category]]

$$
  \mathcal{C}  = \mathcal{C}^\otimes \times_{\mathcal{O}^\otimes} \mathcal{O}
$$

is equipped by $p$ with the [[structure]] of an **$\mathcal{O}$-[[monoidal (∞,1)-category]]** (see remark \ref{EquivalenceToOMonoidsInInfinityCat} below).

=--

This is ([Lurie, def. 2.1.2.13](#Lurie)).

+-- {: .num_remark #EquivalenceToOMonoidsInInfinityCat}
###### Remark

For $\mathcal{C}^\otimes \to \mathcal{O}^\otimes$ a coCartesian fibration of $(\infty.1)$-operads by def. \ref{coCartesianFibrationOfInfinityOperads}, the underlying map

$$
  \mathcal{C} \to \mathcal{O}
$$

is a [[coCartesian fibration]] of [[(∞,1)-categories]]. Therefore by the [[(∞,1)-Grothendieck construction]] it is classified by an [[(∞,1)-functor]]

$$
  \chi \colon \mathcal{O} \to (\infty,1)Cat
  \,.
$$

In fact, this is restricted from the [[(∞,1)-Grothendieck construction]] $\mathcal{O}^{\otimes} \rightarrow (\infty,1)Cat$;
this functor is an [$\mathcal{O}$-monoid](https://ncatlab.org/nlab/show/cartesian+symmetric+monoidal+∞-category#O-monoids), and hence an $\mathcal{O}$-algebra with respect to the [[cartesian symmetric monoidal (∞,1)-category]] structure on [[(∞,1)Cat]]. 
This way coCartesian fibrations of $(\infty,1)$-operads over some $\mathcal{O}^\otimes$ are equivalently $\mathcal{O}$-algebras in [[(∞,1)Cat]], i.e. $\mathcal{O}$-[[monoidal (∞,1)-categories]].

=--

([Lurie, remark 2.1.2.17, 2.4.2.6](#Lurie))

## Related concepts

* [[monoidal (∞,1)-category]]

* [[morphism of (∞,1)-operads]]

  * [[fibration of (∞,1)-operads]]

  * **coCartesian fibration of (∞,1)-operads**

## References

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects coCartesian fibration of (infinity,1)-operads]]

[[!redirects coCartesian fibrations of (∞,1)-operads]]
[[!redirects coCartesian fibrations of (infinity,1)-operads]]
