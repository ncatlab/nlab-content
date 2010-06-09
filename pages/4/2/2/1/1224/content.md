<div class="rightHandSide toc">
[[!include infinity-limits - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[functor]] $F : C \to D$ is **final** (often called **cofinal**), if we can restrict [[diagram]]s on $D$ to diagrams on $C$ along $F$ without changing their [[colimit]].  

Dually, a functor is **initial** (sometimes called **co-cofinal**) if pulling back diagrams along it does not change the [[limit]]s of these diagrams.

Beware that this property is pretty much unrelated to that of a functor being an [[initial object]] or [[terminal object]] in the [[functor category]] $[C,D]$.

## Definition

+-- {: .un_def}
###### Definition


A [[functor]] $F : C \to D$ is **final** if for every [[object]] $d \in D$ the [[comma category]] $(d/F)$ is non-empty and [[connected category|connected]].

A [[functor]] $F : C \to D$ is **initial** if the [[opposite category|opposite]] $F^{op} : C^{op} \to D^{op}$ is final, i.e. if for every [[object]] $d \in D$ the [[comma category]] $(F/d)$ is non-empty and [[connected category|connected]].

=--


## Properties

+-- {: .un_prop}
###### Proposition

Let $F : C \to D$ be a [[functor]]

The following conditions are equivalent.

1. $F$ is final.

1. For all functors $G : D \to Set$ the natural [[function]] between [[colimit]]s

   $$
     \lim_\to G \circ F \to \lim_{\to} G
   $$

   is a [[bijection]].


1. For all categories $E$ and all functors $G : D \to E$ the natural [[morphism]] between [[colimit]]s

   $$
     \lim_\to G \circ F \to \lim_{\to} G
   $$

   is a [[isomorphism]].
   


1. For all functors $G : D^{op} \to Set$ the natural [[function]] between [[limit]]s

   $$
     \lim_\leftarrow G \to \lim_\leftarrow G \circ F^{op}
   $$

   is a [[bijection]].

1. For all categories $E$ and all functors $G : D^{op} \to E$ the natural [[morphism]]

   $$
     \lim_\leftarrow G \to \lim_\leftarrow G \circ F^{op}
   $$

   is an [[isomorphism]].
   
1. For all $d \in D$ 

   $$
     {\lim_\to}_{c \in C} Hom_D(d,F(c)) \simeq *
     \,.
   $$


=--

+-- {: .un_prop}
###### Proposition

If $F : C \to D$ is final then $C$ is connected precisely if $D$ is.

=--


+-- {: .un_prop}
###### Proposition


If $F_1$ and $F_2$ are final, then so is their composite $F_1 \circ F_2$.

If $F_2$ and the composite $F_1 \circ F_2$ are final, then so is $F_1$.

If $F_1$ is a [[full and faithful functor]] and the composite is final, then both functors seperately are final.

=--


## Generalizations

The generalization of the notion of final functor from [[category theory]] to [[(∞,1)-category|(∞,1)]]-[[higher category theory]] is described at

* [[final (∞,1)-functor]].

The characterization of final functors is also a special case of the characterization of [[exact squares]].


## Examples

* If $D$ has a [[terminal object]] then the functor $F : {*} \to D$ that picks that terminal object is final: for every $d \in D$ the [[comma category]] $d/F$ is equivalent to $*$.  The converse is also true: if a functor $*\to D$ is final, then its image is a terminal object.

  In this case the statement about preservation of colimits states that the colimit over a category with a terminal object is the value of the diagram at that object. Which is also readily checked directly.



## References

For instance section 2.5 of

* Kashiwara, Shapira, _[[Categories and Sheaves]]_

[[!redirects cofinal functor]]
[[!redirects cofinal functors]]
[[!redirects final functor]]
[[!redirects final functors]]
[[!redirects initial functor]]
[[!redirects initial functors]]

