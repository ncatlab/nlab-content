
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The refinement of the concept of [[lax colimits]] from [[category theory]] to [[(infinity,1)-category theory]].

## Properties

In the special case of functors $f : C \to (\infty,1)Cat$, lax (co)limits can be given by the [[(∞,1)-end]] and coend.

$$
  laxcolim(f)   \simeq \int^{c \in C} (C_{c/})^{op} \times f(c)
$$
$$
  oplaxcolim(f)   \simeq \int^{c \in C} C_{c/} \times f(c)
$$
$$
  laxlim(f)  \simeq \int_{c \in C} Fun(C_{/c}, f(c))
$$
$$
  oplaxlim(f)  \simeq \int_{c \in C} Fun((C_{/c})^{op}, f(c))
$$

Take care to note that lax colimits correspond to _oplax_ cones, just as in the 2-categorical case.

## Examples

* If $J : [1] \to (\infty,1)Cat$ is the diagram depicting a functor $f : A \to B$, then $laxlim(J) \simeq (f \downarrow B)$ and $oplaxlim(J) \simeq (B \downarrow f)$.

* The covariant [[(∞,1)-Grothendieck construction]] sends any $F : C \to (\infty,1)Cat$ to $oplaxcolim(F)$, and the contravariant version sends $F : C^{op} \to (\infty,1)Cat$ to $laxcolim(F)$.

## Related concepts

* [[(infinity,1)-limit]]

## References

* {#GepnerHaugsengNikolaus15} [[David Gepner]], [[Rune Haugseng]], [[Thomas Nikolaus]], _Lax colimits and free fibrations in $\infty$-categories_ ([arXiv:1501.02161](http://arxiv.org/abs/1501.02161))

[[!redirects lax (∞,1)-colimits]]

[[!redirects lax (∞,1)-limit]]
[[!redirects lax (∞,1)-limits]]


[[!redirects lax (infinity,1)-colimit]]
[[!redirects lax (infinity,1)-colimits]]

[[!redirects lax (infinity,1)-limit]]
[[!redirects lax (infinity,1)-limits]]
