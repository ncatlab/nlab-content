
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

Generally in [[category theory]] a _coprojection_ is one of the canonical [[morphisms]] $p_i$ into a (categorical) [[coproduct]]:

$$
  p_i \colon X_i \to \coprod_j X_j
  \,.
$$


or, more generally into a [[colimit]] 

$$
  p_i \colon X_i \to \underset{\rightarrow_j}{\lim} X_j
  \,.
$$

Hence a coprojection is a component of a [[colimit|colimiting]] _[[cocone]]_ under a given [[diagram]].

Coprojections are also sometimes called *coproduct injections* or *inclusions*, though in general they are not [[monomorphisms]] (see below).

## Properties

### Monicity

In general, the coprojections of a coproduct need not be [[monomorphisms]].  However, they are in certain common situations, such as:

* In a [[distributive category]]; see [there](http://ncatlab.org/nlab/show/distributive+category#monic) for a proof.  

* In a category with [[zero morphisms]], since then they are [[split monomorphisms]].

It is easy to find examples of categories in which the coprojections of coproducts are not monic, e.g. the projection $\emptyset \times A\to A$ in $Set$ is not epic if $A$ is nonempty, so when regarded as a coprojection in $Set^{op}$ it is not monic.  It is somewhat trickier to find examples of [[closed monoidal categories]] with this property, but [[Chu spaces]] give an example; see [this MO question](http://mathoverflow.net/questions/208375/a-cosmos-where-coproduct-injections-are-not-monic).


[[!redirects coprojection]]
[[!redirects coprojections]]

[[!redirects coproduct coprojection]]
[[!redirects coproduct coprojections]]
[[!redirects coprojection morphism]]
[[!redirects coprojection morphisms]]

[[!redirects coprojection map]]
[[!redirects coprojection maps]]


[[!redirects co-projection]]
[[!redirects co-projections]]

[[!redirects co-product coprojection]]
[[!redirects co-product coprojections]]
[[!redirects co-projection morphism]]
[[!redirects co-projection morphisms]]

[[!redirects co-projection map]]
[[!redirects co-projection maps]]


[[!redirects coproduct injection]]
[[!redirects coproduct injections]]
[[!redirects coproduct inclusion]]
[[!redirects coproduct inclusions]]
