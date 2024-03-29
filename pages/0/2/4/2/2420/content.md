
> This entry is about *partition functions* in the sense of [[statistical mechanics]] and [[quantum field theory]]. For the function in [[number theory]]/[[combinatorics]] that assigns to a [[natural number]] the number of its [[partitions]] see at *[[partition function (number theory)]]*.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _partition function_ is a certain assignment that may be extracted from a system in [[statistical mechanics]], or in [[quantum field theory]]. 

If the quantum field theory $Z$ is presented as an [[FQFT]], that is as a [[functor]] on a category of $d$-dimensional [[cobordisms]], then the partition function is the assignment to $d$-dimensional [[torus|tori]] $T$ of the values $Z(T)$ assigned to these by the QFT.

By the axioms of functoriality and symmetric monoidalness of a QFT, this means that the partition function is the [[trace]] over the value of the QFT in the cylinder obtained by cutting the torus open.

This is where the partition function originally derives its name from: typically for QFTs on _[[Riemannian metric|Riemannian]]_ [[cobordisms]] the  value of the QFT on a cylinder of _length_ $t$ is a [[linear operator]] of the form $\exp(- t H)$ for some operator $H$.

## Origin of the term 

When one thinks of the QFT --- under [[Wick rotation]] --- as describing a physical system in [[statistical mechanics]], then the vector space that $H$ acts on is the vector space of all states of the system and $H$ is the operator whose eigenstates are the states of definite energy. The expression

$$
  tr(exp(-t H))
$$

then is interpreted as 

> sum over all states $\Psi$ of the system and weigh each one by its energy $E_\Psi$.

This involves, conversely, counting for each fixed energy $E_\Psi$ the number of states of that energy. This will typically be a sum over certain partitions of various particles of an ensemble into various "bins" of partial energies. Therefore the term _partition_ function.

In fact, the common letter $Z$ uses to denote QFTs (or at least [[TQFT]]s) also derives from this: in German the partition function is called _Zustandssumme_ --- from German _Zustand_ for "state" .

The [[Mellin transform]] of the partition function is known in [[quantum field theory]] as the [[Schwinger parameter]]-formulation which takes the [[worldline theory]] to its [[zeta function regularization|zeta regulated]] [[Feynman propagator]].

## Examples 

Partition function for the [[superparticle]]: [[K-theory]] [[index]].

Partition function for the [[type II superstring]]: [[elliptic genus]].

Partition function for the [[heterotic string]]: [[Witten genus]].


For some discussion of partition functions of 1-dimensional QFTs see [[(1,1)-dimensional Euclidean field theories and K-theory]].

For some discussion of partition functions of 2-dimensional QFTs see [[(2,1)-dimensional Euclidean field theories and tmf]]

## Related concepts

* [[functional determinant]], [[zeta function of an elliptic differential operator]]

* [[vacuum amplitude]], [[vacuum energy]]

* [[Witten index]]

* [[Riemann hypothesis and physics]]


[[!include genera and partition functions - table]]


## References

### General

* Addison Ault, "The partition function: If that's what it is _Why don't they say so!_" ([pdf](http://people.cornellcollege.edu/aault/Chemistry/PartitionFunction1.pdf))


[[!include elliptic genera as partition functions -- references]]


[[!redirects partition functions]]