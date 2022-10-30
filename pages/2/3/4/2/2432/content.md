
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
## Between topological spaces

While every [[continuous map]] sends compact sets to compact sets, it is not true in general that the preimage of a compact set along a continuous map is compact.

A [[continuous function]] $f : X \to Y$ between [[topological space]]s is **proper** if the [[inverse image]] of any [[compact space|compact]] subset is itself compact.

A notion of proper homotopy between proper maps leads to [[proper homotopy theory]].

Similarly, one can consider the conditions on morphisms in other geometric situations, like [[algebraic geometry]], and properness often either reflects or implies good behaviour with respect to the compact objects (cf. also proper push-forward). 

## Between schemes

A __proper morphism of [[scheme]]s__ is by a definition a morphism $f:X\to Y$ which is 

1. [[separated morphism|separated]], 

1. of [[finite type morphism|finite type]]

1.  [[universally closed morphism|universally closed]] (the latter means that for every $h: Z\to Y$ the pullback $h^*(f): Z\times_Y X\to Z$ is closed). 

There is a classical and very practical [[valuative criterion of properness]] due Chevalley. 

We say that a scheme $X$ is __proper__ if the canonical map $X \to \operatorname{Spec} \mathbb{Z}$ to the [[terminal object]] is proper. 

Proper schemes are analogous to [[compact topological spaces]]. This is one reason why one uses the terminology "quasi-compact" when referring to schemes whose underlying topological space is compact.

The [[base change]] formulas for [[cohomology]] for proper and for smooth morphisms of schemes motivated [[Alexander Grothendieck|Grothendieck]] (in [[Pursuing Stacks]]) to define abstract proper and smooth functors in the setting of [[fibered categories]]; this is further expanded on in 
([Maltsiniotis](#Maltsiniotis)).

## References

* [[Georges Maltsiniotis]], _Structures d'asph&#233;ricit&#233;, foncteurs lisses, et fibrations_, Ann. Math. Blaise Pascal __12__, pp. 1-39 (2005) ([ps](http://people.math.jussieu.fr/~maltsin/ps/asphbl.ps)).
 {#Maltsiniotis}
(TO ADD: The definition of a proper dg algebra, proper dg category, proper A-inf cat ???)

* wikipedia [proper morphism](http://en.wikipedia.org/wiki/Proper_morphism)

[[!redirects proper map]]
[[!redirects proper maps]]

[[!redirects proper morphism]]
[[!redirects proper morphisms]]
[[!redirects proper scheme]]
[[!redirects proper schemes]]

[[!redirects proper functor]]
[[!redirects proper functors]]
