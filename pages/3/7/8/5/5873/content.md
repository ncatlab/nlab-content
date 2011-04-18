Introduced by [[Lawvere]] in [Adjointness in Foundations](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html), Dialectica 23 (1969), 281-296, and developed in 'Equality in hyperdoctrines and
comprehension schema as an adjoint functor', Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14.

Taken from [slides](http://www.cse.chalmers.se/~peterd/papers/historyidentitytype.pdf) by Peter Dybjer.

A hyperdoctrine is a category $T$ of "types", whose morphisms are called "terms", and which is assumed to be cartesian closed. For each type $X$ there is a cartesian closed category $P(X)$ of "attributes of type $X$, whose morphisms are called "deductions
over $X$" for each term $f : X \to Y$ there is a functor $f \cdot ( ) : P(Y)\to P(X)$, called "substitution". For each term $f : X \to Y$, there are two functors $( )\Sigma f$ and $( )\Pi f$, respectively left and right adjoint to substitution, called
"ex&#237;stential, respectively universal, quantification along $f$".

A hyperdoctrine is a kind of [[indexed category|indexed]] or [[Grothendieck fibration|fibered]] category.

Examples,
* $T$ = the category of contexts, $P(X)$ is the category of formulas. "Given any theory (several sorted, intuitionistic or [[first-order hyperdoctrine|classical]]) ..."
* $T$ = the category of small sets, $P(X) = 2^X =$ the partially ordered
set of all propositional functions "or one may take suitable
'homotopy classes' of deductions".
* $T$ = the category of small sets, $P(X) = Set^X$ ... "This hyperdoctrine
may be viewed as a kind of set-theoretical surrogate of proof
theory"
* "honest proof theory would presumably yield a hyperdoctrine with
nontrivial $P(X)$, but a syntactically presented one".
* $T$ = the category of small categories, $P(B) = 2^B$
* $T$ = the category of small categories, $P(B) = Set^B$
* $T$ = the category of small groupoids, $P(B) = Set^B$

See [[Frobenius reciprocity]].