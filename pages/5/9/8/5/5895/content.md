
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of [[site]] may be [[internalization|internalized]] in any [[topos]] to yield a notion of _internal site_ .

## Definition

The definition of internal site is obvious and straightforward.

+-- {: .num_defn}
###### Definition

For $\mathcal{E}$ a [[topos]], an **internal site** in $\mathcal{E}$ is an [[internal category]] $\mathbb{C}$ equipped with an internal [[coverage]].

=--


Spelled out in components, this means the following:

(...)

## Properties

### Externalization

We discuss how to every internal site there is a corresponding external site such that the internal sheaf topos on the former agrees with the external sheaf topos on the latter.

+-- {: .num_defn #TheExternalizedSite}
###### Definition

Let $\mathcal{C}$ be a [[small category]] and let $\mathcal{E} := [\mathcal{C}^{op}, Set]$ be its [[presheaf topos]]. Let $\mathbb{D} \in \mathcal{E}$ be an internal site. Regarded, by the [[Yoneda lemma]], as a functor $\mathbb{D} : \mathcal{C}^{op} \to Cat$, this induces via the [[Grothendieck construction]] a [[fibered category]] which we denote

$$
  \mathcal{C} \rtimes \mathbb{D} \to \mathcal{C}
  \,.
$$

=--

This is reviewed for instance in ([Johnstone, p. 596](#Johnstone)).

The notation is motivated from the following example.

+-- {: .num_example}
###### Example

Let $G$ be a [[group]] (in [[Set]], hence a [[discrete group]]) and let $\mathcal{C} := \mathbf{B}G$ be its [[delooping]] [[groupoid]]. Then 

$$
  \mathcal{E} \simeq [\mathbf{B}G , Set]
$$

is the topos of [[permutation representation]]s of $G$. Let $H \in \mathcal{E}$ be a [[group object]]. This is equivalently a group in $Set$ equipped with a $G$-[[action]]. Its internal delooping gives the [[internal groupoid]] $\mathbb{D} := \mathcal{B}H$  in $\mathcal{E}$. 

In this case we have that 

$$
  \mathcal{C} \rtimes \mathbb{D} \simeq \mathbf{B}(G \rtimes H)
$$

is the delooping gorupoid of the [[semidirect product]] group of the $G$-action on $H$.

=--

Generally we have

+-- {: .num_note}
###### Note

The category $\mathcal{C} \rtimes \mathbb{D}$ from def. \ref{TheExternalizedSite} is described as follows:

* [[object]]s are pairs $(U,V)$ with $U \in Ob \mathcal{C}$ and $V \in Ob \mathbb{D}(U)$;

* [[morphism]]s $(U',V') \to (U,V)$ are pairs $(a,b)$ where $a : U' \to U$ is in $\mathcal{C}$ and $b : V' \to \mathbb{D}(a)(V)$ in $\mathbb{D}(U')$.


=--

+-- {: .num_prop}
###### Proposition

We have an [[equivalence of categories]]

$$
  [\mathbb{D}^{op}, [\mathcal{C}^{op}, Set]]
   \simeq
  [(\mathcal{C} \rtimes \mathbb{D})^{op}, Set]
$$

between the category of internal presheaves in $\mathcal{E}$ over the internal category $\mathbb{D}$, and external presheaves over the semidirect product site $\mathcal{C} \rtimes \mathbb{D}$.

=--

This appears as ([Johnstone, lemma 2.5.3](#Johnstone)).

This result generalizes straightforwardly to an analogous statement for internal sheaves.

(...)

## Related concepts

* [[internal locale]]

## References

Section C2.4

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

[[!redirects internal sites]]