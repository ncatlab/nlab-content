
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

This is the analog of a [[filtered category]] in the context of [[(∞,1)-categories]].

The main purpose of considering filtered (∞,1)-categories is to define [[filtered (∞,1)-colimits]], which are the colimits that commute with [[finite (∞,1)-limits]].

## Definition

+-- {: .num_defn}
###### Definition


Let $\kappa$ be a [[regular cardinal]], and let $C\in \sSet$ be an (∞,1)-category, incarnated as a [[quasicategory]].

$C$ is called **$\kappa$-filtered** if for all $\kappa$-small $K\in\sSet$ and every morphism $f\colon K\to C$ there is a morphism $\hat p\colon \rcone(K)\to C$ extending $f$, where $\rcone(K)$ denotes the (right) [[cone]] of the simplicial set $K$.  $C$ is called **filtered** if it is $\omega$-filtered.

=--

## Properties

+-- {: .num_prop}
###### Proposition

An [[(∞,1)-category]] $K$ is filtered precisely if [[(∞,1)-colimits]] of shape $K$ in [[∞Grpd]] commute with all [[finite (∞,1)-limits]], hence if

$$
  {\lim_\to} : Func(K, \infty Grpd) \to \infty Grpd
$$

is a left [[exact (∞,1)-functor]].

=--

This is [[Higher Topos Theory|HTT, prop. 5.3.3.3]].

+-- {: .num_prop}
###### Proposition

A filtered $(\infty,1)$-category is in particular a [[sifted (∞,1)-category]].

=--

This appears as ([Lurie, prop. 5.3.1.20](#Lurie)). Since [[sifted (∞,1)-colimits]] are precisely those that commute with finite [[products]], this is a direct reflection of the fact that finite products are a special kind of [[finite (∞,1)-limits]].

+-- {: .num_cor}
###### Corollary

For $C$ a filtered $(\infty,1)$-category, the [[diagonal]] [[(∞,1)-functor]] $\Delta : C \to C \times C$ if a [[cofinal (∞,1)-functor]].

=--

+-- {: .un_prop}
###### Proposition
A filtered $(\infty,1)$-category is weakly [[contractible]], i.e. when incarnated as a [[quasicategory]], it is [[weak homotopy equivalence|weakly equivalent]] to a [[point]] in the [[Kan-Quillen model structure]] on simplicial sets.
=--
+-- {: .proof}
###### Proof
This is ([Lurie, Lemma 5.3.1.20](#Lurie)).
=--

## Related concepts

* [[sifted category]], [[sifted colimit]], [[sifted (∞,1)-category]], [[sifted (∞,1)-colimit]]

* [[directed set]], [[filtered category]], **filtered (∞,1)-category**

* [[filtered homotopy colimit]]

## Reference

Section 5.3.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

[[!redirects filtered quasicategory]]
[[!redirects filtered (infinity,1)-categories]]
[[!redirects filtered (∞,1)-category]]
[[!redirects filtered (∞,1)-categories]]

[[!redirects cofiltered (∞,1)-category]]
[[!redirects cofiltered (∞,1)-categories]]

[[!redirects filtered (∞,1)-colimit]]
[[!redirects filtered (infinity,1)-colimit]]

[[!redirects filtered (∞,1)-colimits]]
[[!redirects filtered (infinity,1)-colimits]]
