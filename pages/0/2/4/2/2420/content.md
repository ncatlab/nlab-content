[[!redirects partition functions]]

# Idea #

The _partition function_ is a certain assignment that may be extracted from a [[quantum field theory]]. It the quantum field theory $Z$ is presented as an [[FQFT]] that is a [[functor]] on a category of $d$-dimensional [[cobordism]]s, then the partition function is the assignment of $d$-dimensional [[torus|tori]] $T$ to the valued $Z(T)$ assigned to these by the QFT.

By the axioms of functoriality and symmetric monoidalness of a QFT, this means that the partition functoin is the [[trace]] over the value of the QFT in the cylinder obtained by cutting the torus open.

This is where the partition function originally derives its name from: typically for QFTs on _[[Riemannian mentric|Riemannian]]_ [[cobordism]]s the  value of the QFT on a cylinder of _length_ $t$ is a linear [[operator]] of the form $\exp(- t H)$ for some operator $H$.

# Origin of the term #

When one thinks of the QFT --- under [[Wick rotation]] --- as describing a physical system in [[statistical mechanics]], then vector space that $H$ acts on is the vector space of all states of the system and $H$ is the operator whose eigenstates are the states of definite energy, and then the expression

$$
  tr(exp(-t H))
$$

interprets as 

> sum over all states $\Psi$ of the system and weigh each one by its energy $E_\Psi$.

This involves, conversely, counting for each fixed energy $E_\Psi$ the number of states of that energy. This will typically be a sum over certain partitions of various particles of an ensemble into various "bins" of partial energies. Therefore the term _partition_ function.

In fact, the common letter $Z$ uses to denote QFTs (or at least [[TQFT]]s) also derives from this: in German the partition function is called _Zustandssumme_ --- from German _Zustand_ for "state" .

# Examples #

For some discussion of partition functions of 1-dimensional QFTs see [[(1,1)-dimensional Euclidean field theories and K-theory]].

For some discussion of partition functions of 2-dimensional QFTs see [[(2,1)-dimensional Euclidean field theories and tmf]]
