
#Contents#
* table of contents
{:toc}

## Idea

A prominent idea in the effort to isolate what are the properly [[logic|logical]] concepts we deploy has been to use the notion of [[invariant|invariance]]. The thought here is that logical concepts are those that remain invariant under arbitrary [[permutations]] of the corresponding domain of objects of the universe of discourse. This approach has been seen by some, notably [[Friederich Mautner]] and [[Alfred Tarski]], as an extension of the [[Erlangen program]] of [[Felix Klein]], which looked to distinguish geometries by their invariance under different [transformation groups](action#ActionsOfAGroup). Just as [[Euclidean geometry|Euclidean]] concepts are preserved by Euclidean transformations of space, and [[topology|topological]] ones are preserved by [[homeomorphisms]], so here logical concepts are those preserved by any permutation. 

Tarski's informal definition ([Ln](#Ln)) is reproduced here,
>Now suppose we continue this idea, and consider still wider classes of transformations.
>In the extreme case, we would consider the class of all one-one transformations
>of the space, or universe of discourse, or 'world', onto itself. What will be the
>science which deals with the notions invariant under this widest class of transformations?
>Here we will have very few notions, all of a very general character. I suggest that
>they are the logical notions, that we call a notion 'logical' if it is invariant under all
>possible one-one transformations of the world onto itself.

Logic is now to be seen as the maximally invariant theory.

Tarski goes on to point out that using this method to distinguish between logical and mathematical concepts, the result is dependent on the chosen foundational theory. When [[Bertrand Russell|Russell's]] theory of types is chosen, as used by Whitehead and him in _Principia Mathematica_, then the membership relation is a logical concept. However, using a [[material set theory]], such as [[ZFC]], then it is not. 

## Cases of invariance in logical systems

### Propositional logic

In the [[propositional logic|propositional]] case, consider the [[symmetric group]], $S_n$, [[group action|acting]] on a [[set]], $X$, of [[cardinality]] $n$. Then it also acts on all [[Cartesian product|cartesian powers]], $X^k$. Subsets of $X^k$ are $k$-ary [[relations]], and those invariant (as [[subsets]]) under $S_n$ are [[unions]] of the [[orbits]] of its action. The idea then is that such relations are invariant if and only if they are definable using only logical constants.


### Simple type theory

Johan van Benthem proposed ([JvB](#JvB)) such a treatment for a certain [[simple type theory]]. Here there is a type of individuals, $e$, a type of truth values, $t$, and it is closed under function types. For instance, invariant elements of the type $((e, t), t)$ include the [[quantifiers]].

Van Benthem demonstrates that types possessing an invariant element are precisely those of either of the forms

1. $(a_1, (a_2, \ldots,(a_n, t)\ldots)),$

1. $(a_1, (a_2, \ldots,(a_n, e)\ldots)),$ where at least one of the $a_i$ fails to have an invariant element.

### Homotopy type theory

[[Steve Awodey]] ([ULL](#ULL)) has argued that [[homotopy type theory]] should be seen in a similar light as expressing invariance under the broader notion of [[equivalence]] (see also at *[[principle of equivalence]]*). In ([UPL](#UPL)) he speaks of what he calls the _Tarski-Grothendieck Thesis_:

> If a statement, concept, or construction is purely logical, then it should  be invariant under all equivalences of the structures involved. A statement that is not invariant must involve some non-logical specifics, pertaining not to general logical form but to some particular aspects of the objects bearing the structure.  If it is the hallmark of a logical concept that it should pertain only to general, formal structure and not to any specific features of  the objects bearing that structure, then this formal character may be witnessed  by the fact that the concept is invariant under all equivalence transformations.

One way to understand this formally is in terms of type formation that is invariant under type equivalence. So given a type $A: \mathcal{U}$, we have for instance

* [[dependent sum type]] and [[dependent product type]] formation in 
$$(X: BAut(A)) \to (X \to \mathcal{U}) \to \mathcal{U},$$

* list type formation and [[n-truncation modality|truncation]] $\| X\|_n$ in 
$$(X: BAut(A)) \to \mathcal{U},$$

* [[identity type]] formation in 
$$(X: BAut(A)) \to X \to (X \to \mathcal{U}),$$

and so on.

Types formed from two or more types may be treated similarly, so that the formation of [[sum type]], [[product type]] and [[function type]] are invariant elements of 

* $(X: BAut(A)) \to (Y: BAut(B)) \to \mathcal{U}.$

In this way, any concept expressible in [[homotopy type theory]], and compatible with the [[univalence axiom]], is to be counted as logical.

## Related concepts

* [[principle of equivalence]]


## References

* John MacFarlane, _Logical Constants:Permutation invariance_, [SEP](http://plato.stanford.edu/entries/logical-constants/#PerInv)

* F. I. Mautner, _An Extension of Klein's Erlanger Program: Logic as Invariant-Theory_, American Journal of Mathematics, Vol. 68, No. 3 (Jul., 1946), pp. 345-384 (based on [[Hermann Weyl]]'s formulation of the program in _Classical Groups_, pp. 13-18) ([JSTOR](https://www.jstor.org/stable/2371821)).

* {#Ln} [[Alfred Tarski]], 1986, _What are Logical Notions?_, History and Philosophy of Logic, 7: 143&#8211;154. (Transcript of a 1966 talk, ed. J. Corcoran.) doi:[10.1080/01445348608837096](http://dx.doi.org/10.1080/01445348608837096)

* {#Quine51} [[Willard Quine]], 1951, _Two Dogmas of Empiricism_, The Philosophical Review, 60(1): 20–43. Reprinted in Quine _From a Logical Point of View_, New York: Harper, 1953, pp. 20–46.

* V. McGee, 1996, _Logical Operations_, Journal of Philosophical Logic, 25: 567&#8211;580

* Denis Bonnay, _Logicality and Invariance_, [lecture series](http://lumiere.ens.fr/~dbonnay/) (under 'Enseignement')

* Denis Bonnay, _Logicality and Invariance_, Bulletin of Symbolic Logic 14 (1):29-68 (2006), [pdf](http://lumiere.ens.fr/~dbonnay/files/Papers/bonnaylogicalityandinvariance.pdf)

* {#JvB} Johan van Benthem, _Logical constants across varying types_, Notre Dame J. Formal Logic 30 (1989), no. 3, 315--342, ([pdf](http://www.illc.uva.nl/lgc/translation/papers/LogicalConstants.pdf))

* {#ULL} [[Steve Awodey]], _Univalence as a logical law_, talk at [conference](https://hottatbristol.wordpress.com/), Bristol 15 Sept 2016.

* {#UPL} [[Steve Awodey]], _Univalence as a Principle of Logic_, ([preprint](https://www.andrew.cmu.edu/user/awodey/preprints/uapl.pdf))
