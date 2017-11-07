
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[Lagrangian field theory]] for fields defined by some [[field bundle]] is called _locally variational_ if its [[equations of motion]] is determined by a [[source form]] on the [[jet bundle]] which is _locally_, i.e. over some [[neighbourhood]] of any point of the base space, the [[Euler-Lagrange variational derivative]] of a [[Lagrangian density]] on this neighbourhood, but not necessarily globally so.

Some common examples of [[Lagrangian field theories]] are in fact globally variational (such as the plain [[scalar field]] or the uncharged [[Dirac field]]), but other common example of Lagrangian field theories are indeed only locally variational (see the _[Examples](#Examples)_ below).

## Example
 {#Examples}

Field theories with [[WZW terms]] and [[higher WZW terms]] are (only) locally variational: the WZW term is the pullback to the [[jet bundle]] of a [[circle n-bundle with connection]] on the base space (e.g. a [[line bundle with connection]], [[bundle gerbe with connection]], etc.) and the corresponding [[Euler-Lagrange form]] is proportional to the [[horizontal form]]-projection of the [[curvature]] $(n+1)$-form. This is locally [[exact differential form|exact]], but, crucially, not globally so, unless the [[principal infinity-bundle|higher bundle]] is [[flat infinity-bundle]].

Beware that this is not an exotic situation: already the Lagrangian density for the [[charged particle]], regarded as a field theory on its [[worldline]], coupled to an [[electromagnetic field]] with non-trivial [[magnetic charge]] ([[first Chern class]]) is of this form: the [[interaction]] term which gives the [[Lorentz force]] is an example of a non-trivial [[WZW term]] as above.

## References

Exposition is in

* {#Schreiber16} [[Urs Schreiber]], _[[schreiber:Higher Structures|Higher structures in Mathematics and Physics]]_, lecture at [Oberwolfach Workshop 1651a](https://www.mfo.de/occasion/1651a/www_view), 2016 Dec. 18-23


[[!redirects locally variational field theories]]

[[!redirects locally variational quantum field theory]]
[[!redirects locally variational quantum field theories]]
