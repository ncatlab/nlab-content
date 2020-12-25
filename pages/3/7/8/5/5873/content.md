
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of a _hyperdoctrine_ is essentially an axiomatization of the collection of [[slice category|slices]] of a [[locally cartesian closed category]] (or something similar): a [[category]] $T$ together with a functorial assignment of "slice-like"-categories to each of its objects, satisfying some conditions.

In its use in [[mathematical logic]] ("categorical logic" ([Lawvere 69](#Lawvere69))) a hyperdoctrine is thought of (under [[categorical semantics]] of [[logic]]/[[type theory]]) as a collection of [[contexts]] together with the operations of [[context extension]]/[[substitution]] and [[quantifier|quantification]] on the categories of [[propositions]] or [[types]] in each context.  Therefore specifying the structure of a hyperdoctrine over a given [[category]] is a way of equipping that with a given kind of [[logic]].  

Specifically, a hyperdoctrine on a category $T$ for a given notion of logic $L$ is a [[functor]]

$$
  P \colon T^{op} \to \mathbf{C}
$$

to some [[2-category]] (or even [[higher category]]) $\mathbf{C}$, whose objects are categories whose [[internal logic]] corresponds to $L$.  Thus, each object $A$ of $T$ is assigned an "$L$-logic" (the internal logic of $P(A)$).

In the most classical case, $L$ is [[propositional logic]], and $\mathbf{C}$ is a 2-category of [[posets]] (e.g. [[lattices]], [[Heyting algebras]], or [[frames]]).  A hyperdoctrine is then an incarnation of [[first-order logic|first-order]] [[predicate logic]].  A canonical class of examples of this case is where $P$ sends $A \in T$ to the [[poset of subobjects]] $Sub_T(A)$ of $A$.  The predicate logic we obtain in this way is the usual sort of [[internal logic]] of $T$.

We generally require also that for every morphism $f \colon A \to B$ the morphism $P(f)$ has both a [[left adjoint]] as well as a [[right adjoint]], typically required to satisfy [[Frobenius reciprocity]] and the [[Beck-Chevalley condition]].  These adjoints are regarded as the action of [[quantifiers]] along $f$.  Thus, a hyperdoctrine can also be regarded as a way of "adding quantifiers" to a given kind of logic.

More precisely, one thinks of 

* $T$ as a category of [[types]] or rather [[contexts]];

* $P$ as assigning 

  * to each context $X \in T$ the [[lattice]] of [[propositions]] in this context;

  * to each morphism $f \colon X \to Y$ in $T$ the operation of  "substitution of variables" / "extension of contexts" for propositions $P(Y) \to P(X)$;

* the left adjoint to $P(f)$ gives the application of the [[existential quantifier]];
 
* the right adjoint to $P(f)$ gives the application of the [[universal quantifier]] (see there for the interpretation of quantifiers in terms of adjoints).

* The Beck-Chevalley condition ensures that quantification interacts with substitution of variables as expected

* Frobenius reciprocity expresses the derivation rules.

So, in particular, a hyperdoctrine is a kind of [[indexed category]] or [[Grothendieck fibration|fibered category]].

The general concept of hyperdoctrines does for [[predicate logic]] precisely what [[Lindenbaum-Tarski algebras]] do for [[propositional logic]], positioning the [[categorical semantics|categorical formulation]] of [[logic]] as a natural extension of the algebraicization of logic. 

## Properties
 {#Properties}

+-- {: .num_theorem}
###### Theorem

The [[functors]] 

* $Cont$, that form a [[category of contexts]] of a [[first-order logic|first-order theory]];

* $Lang$ that forms the [[internal language]] of a [[hyperdoctrine]]

constitute an [[equivalence of categories]]

$$
  FirstOrderTheories
    \stackrel{\overset{Lang}{\leftarrow}}{\underset{Cont}{\to}}
  Hyperdoctrines
  \,.
$$

=--

This is due to ([Seely, 1984a](#SeelyA)). For more details see _[[relation between type theory and category theory]]_.


## Examples

### Classes of hyperdoctrines

* [[first-order hyperdoctrine]]

* [[modal hyperdoctrine]]

* [[coherent hyperdoctrine]]

* [[Boolean hyperdoctrine]]

* [[linear hyperdoctrine]]

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

## Related notions

* [[comprehension]]

* [[tripos]]

* [[modal hyperdoctrine]]

## References

The notion was introduced in 

* {#Lawvere69} [[Bill Lawvere]], _Adjointness in Foundations_, ([TAC](http://www.tac.mta.ca/tac/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296
 


and further developed in 

* [[Bill Lawvere]], _[[Equality in hyperdoctrines and comprehension schema as an adjoint functor]]_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14. ([pdf](https://ncatlab.org/nlab/files/LawvereComprehension.pdf))

* {#SeelyA} [[R. A. G. Seely]], _Hyperdoctrines, natural deduction, and the Beck condition_, Zeitschrift f&#252;r math. Logik und Grundlagen der Math., Band 29, 505-542 (1983). ([pdf](http://www.math.mcgill.ca/~rags/ZML/ZML.PDF))
 

Surveys and reviews include

* [[Anders Kock]], [[Gonzalo Reyes]], _Doctrines in categorical logic_, in J. Barwise (ed.) _Handbook of Mathematical Logic_ (North Holland, Amsterdam, 1977) 283-313

* [[Peter Dybjer]], _(What I know about) the history of the identity type_ (2006) ([pdf slides](http://www.cse.chalmers.se/~peterd/papers/historyidentitytype.pdf))

A [[string diagram]] calculus for monoidal hyperdoctrines is discussed in

* Geraldine Brady, [[Todd Trimble]], _[[A string diagram calculus for predicate logic]]_

[[!redirects hyperdoctrines]]