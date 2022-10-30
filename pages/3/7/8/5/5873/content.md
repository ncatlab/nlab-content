
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _hyperdoctrine_ for a given notion of [[logic]] $L$ is a [[functor]]

$$
  P : T^{op} \to \mathbf{C}
$$

to some [[category]] or [[higher category]] $\mathbf{C}$ whose [[internal logic]] corresponds to $L$, such that for every morphism $f : A \to B$ the morphism $P(f)$ has both a [[left adjoint]] as well as a [[right adjoint]].

Moreover, the left adjoint is typically required to satisfy  [[Frobenius reciprocity]] and the [[Beck-Chevalley condition]].

Here one thinks of 

* $T$ as a category of [[types]] or rather [[contexts]];

* $P$ as assigning 

  * to each context $X \in T$ the [[lattice]] of [[propositions]] in this context;

  * to each morphsm $f : X \to Y$ in $T$ the operation of  "substitution of variables" / "extension of contexts" for propositions $P(Y) \to P(X)$;

* the images of a proposition under the required left adjoints being the application of the [[existential quantifier]];
 
* the images of a proposition under the right adjoints being the [[universal quantifier]] (see there for the interpretation of quantifiers in terms of adjoints).

In this interpretation, the Beck-Chevalley condition ensures that quantification interacts with substitution of variables as expects, and Frobenius reciprocity expresses the derivation rules.

So, in particular, a hyperdoctrine is a kind of [[indexed category]] or [[Grothendieck fibration|fibered category]].

The general concept of hyperdoctrines does for [[predicate logic]] precisely what [[Lindenbaum algebras]] do for [[propositional logic]], positioning the [[categorical semantics|categorical formulation]] of [[logic]] as a natural extension of the algebraicization of logic. 


## Examples

### Classes of hyperdoctrines

* [[first-order hyperdoctrine]]

* [[coherent hyperdoctrine]]

* [[Boolean hyperdoctrine]]

### Special cases

* $T$ = the category of contexts, $P(X)$ is the category of formulas. "Given any theory (several sorted, intuitionistic or [[first-order hyperdoctrine|classical]]) ..."

* $T$ = the category [[Set]] of [[small sets]], $P(X) = 2^X =$ the [[power set]] functor, assigning the [[poset]] of all propositional functions 

  ("or one may take suitable 'homotopy classes' of deductions").

* $T$ = the category of small sets, $P(X) = Set^X$ ... "This hyperdoctrine
may be viewed as a kind of set-theoretical surrogate of proof
theory"
* "honest proof theory would presumably yield a hyperdoctrine with
nontrivial $P(X)$, but a syntactically presented one".
* $T$ = [[Cat]], the category of small categories, $P(B) = 2^B$
* $T$ = [[Cat]] the category of small categories, $P(B) = Set^B$
* $T$ = [[Grpd]] the category of small groupoids, $P(B) = Set^B$


## References

The notion was introdcued in 

* [[Bill Lawvere]], _Adjointness in Foundations_, ([TAC](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

and developed in 

* [[Bill Lawvere]], _Equality in hyperdoctrines and
comprehension schema as an adjoint functor_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14.

* R.A.G. Seely, _Hyperdoctrines, natural deduction, and the Beck condition_, Zeitschrift f&#252;r math. Logik und Grundlagen der Math., Band 29, 505-542 (1983). ([pdf](http://www.math.mcgill.ca/~rags/ZML/ZML.PDF))

Surveys and reviews include

* Peter Dybje, _(What I know about) the history of the identity type_ (2006) ([pdf slides](http://www.cse.chalmers.se/~peterd/papers/historyidentitytype.pdf))

[[!redirects hyperdoctrines]]
