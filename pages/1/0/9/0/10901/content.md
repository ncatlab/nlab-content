
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Linear type theory_ is the [[linear logic]]-version of [[type theory]]. In the definition of ([Seely 89, prop. 1.5](#Seely89)), following ([Girard 87](#Girard87)), this is the [[internal language]] of/has [[categorical semantics]] in [[star-autonomous categories]]. But more generally _linear type theory_ came to refer to the internal [[type theory]] of any possibly-non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal category|symmetric]] [[closed monoidal category]]. Indeed, this general notion still faithfully follows the original motivation for the term "linear" as introduced in ([Girard 87](#Girard87)), since the non-cartesianness of the [[tensor product]] means the absence of a [[diagonal]] map and hence the impossibility of [[functions]] to depend on more than a single (linear) copy of their [[variables]].

The [[dependent type theory]]-version of linear type theory should be _[[dependent linear type theory]]_.

## Related concepts

* [[modal type theory]]

* [[geometric homotopy type theory]]

* [[stable homotopy type]]

## References

The orginal notion of [[linear logic]] was introduced in 

*  [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))
 {#Girard87}

The [[categorical semantics]] of linear type theory in [[star-autonomous categories]] is due to 

*  [[R. A. G. Seely]],  _Linear logic, $\ast$-autonomous categories and cofree coalgebras_, _Contemporary Mathematics_ 92, 1989.  ([[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz))
 {#Seely89}

and reviewed/further discussed in

* [[Paul-André Melliès]] , _Categorial Semantics of Linear Logic_, in _Interactive models of computation and program behaviour_, Panoramas et synth&#232;ses 27, 2009 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf))

* Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))

Further discussion of linear type theory is for instance in

* _Capter 7, Linear type theory_ [pdf](http://www.cs.cmu.edu/~fp/courses/linear/handouts/lintt.pdf)

* Anders Schack-Nielsen, Carsten Sch&#252;rmann, _Linear contextual modal type theory_ [pdf](http://www.itu.dk/~carsten/papers/lcmtt.pdf)

* Bernardo Toninho, Lu&#237;s Caires, Frank Pfenning, _Dependent Session Types via Intuitionistic Linear Type Theory_ [pdf](http://ctp.di.fct.unl.pt/~lcaires/papers/dstypes.pdf)

* Iliano Cervesato, [[Frank Pfenning]], _A Linear Logical Framework_, 1996, ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.21.1152))

[[!redirects linear type theories]]

[[!redirects linear type]]
[[!redirects linear types]]

[[!redirects linear homotopy type]]
[[!redirects linear homotopy types]]