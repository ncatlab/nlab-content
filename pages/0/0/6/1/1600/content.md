
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _orbispace_ is a [[space]], specifically a [[topological stack]],  that is locally modeled on the [[homotopy quotient]]/[[action groupoid]] of a [[locally compact topological space]] by a rigid [[group]] [[action]].

Orbispaces are to [[topological spaces]] what [[orbifolds]] are to [[manifolds]]. 

## Definition

Write $Orb$ for the [[global orbit category]]. Then its [[(∞,1)-presheaf (∞,1)-category]] $PSh_\infty(Orb)$ is the [[(∞,1)-category]] of _orbispaces_. ([Henriques-Gepner 07](#HenriquesGepner07), [Rezk 14, remark 1.5.1](#Rezk14))



## Properties

### Relation of global equivariant homotopy theory

By the main theorem of ([Henriques-Gepner 07, (4)](#HenriquesGepner07)) the [[(∞,1)-presheaves]] on the global [[orbit category]] are equivalently "cellular" [[topological stacks]]/[[topological groupoids]] ("[[orbispaces]]"), we might write this as

$$
  TopGrpd^{cell} \simeq PSh_\infty(Orb)
  \,.
$$

Hence cellular topological stacks are equivalently the objects of [[equivariant homotopy theory]].

See also ([Rezk 14, p. 4 and section 7](#Rezk14))


### Relation to $G$-equivariant homotopy theory

Fixing a [[compact topological group]] $G$ and writing $\mathbf{B}G \simeq \ast // G$ for its [[delooping]] stack (the moduli stack of $G$-[[principal bundles]]), then the [[slice (infinity,1)-category|slice]] homotopy theory of topological stacks over $\mathbf{B}G$ on the [[representable morphisms]] (those inducing closed monos on isotropy groups) is equivalently that of [[topological G-spaces]] (with their G-equivariant homotoy theoretical structure, see at _[[equivariant Whitehead theorem]]_):

$$
  TopGrpd_{/\mathbf{B}G}^{reprs.} \simeq G Spaces
$$

([Henriques-Gepner 07, p.7](#HenriquesGepner07))


## Related concepts

* [[Elmendorf's theorem]]

[[!include equivariant homotopy theory -- table]]


## References

A detailed but elementary approach via [[atlases]] can be found in 

* Weimin Chen, _A homotopy theory of orbispaces_ ([arXiv:math/0102020](http://arxiv.org/abs/math/0102020))

and another approach is discussed in

* [[André Henriques]], _Orbispaces and orbifolds from the point of view of the Borel construction, a new definition_ ([arXiv:0112006](http://arxiv.org/abs/math/0112006))

* [[André Henriques]], _Vector bundles on orbispaces_ (2005) ([pdf](http://www.staff.science.uu.nl/~henri105/PDF/orbiabstract.pdf))

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)


[[!redirects orbispaces]]
