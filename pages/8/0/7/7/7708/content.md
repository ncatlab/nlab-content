
> This entry is about a general concepts of "mathematical structure" such as formalized by [[category theory]] and/or [[dependent type theory]]. This subsumes but is more general than the concept of [[structure in model theory]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

It is common in informal language to speak of mathematical objects "equipped with [[extra structure]]" of some sort. The archetypical examples are [[algebras over a Lawvere theory]] in [[Set]]: these are [[sets]] equipped with the structure of certain algebraic operations. For instance a [[group]] $(G, e, {\cdot})$ is a [[set]] $G$ equipped with a binary operation ${\cdot} : G \times G \to G$, etc.

One may formalize the notion of structure using the language of [[category theory]]. This is discussed at _[[stuff, structure, property]]_. In that formalization [[objects]] in some [[category]] $D$ are objects in some category $C$ _equipped with extra structure_ if there is a [[functor]] $p \colon D \to C$ such that

* $p$ is a [[faithful functor]].

{#InCategoryTheory} Depending on author and situation, more properties are required of this functor ([Ehresmann 57](#Ehresmann57), [Ehresmann 65](#Ehresmann65), [Adamek-Rosicky-Vitale 09, remark 13.18](#AdamekRosickyVitale)):

* $p$ is an [[amnestic functor]] ($p$-vertical [[isomorphisms]] are [[identities]]),

* $p$ is an [[isofibration]] (isomorphisms can be lifted along $p$).

{#StrictStructure} However, notice that these two conditions violate the [[principle of equivalence]] for [[categories]]. In the terminology of _[[strict categories]]_ one might hence refer to these conditions as expressing "strict extra structure".


## Notions of structure 

A special class of examples of this is the notion of [[structure in model theory]]. In this case one defines a "language" $L$ that describes the constants, functions (say operations) and relations with which we want to equip sets, and then sets equipped with those operations and relations are called $L$-[[structure in model theory|structures]] for that language. (Equivalently one might say "sets with $L$-structure". Or one might generally say "$X$-structure" for "set with $X$-structure".) In this case there is a [[faithful functor]] from $L$-structures to their underlying sets, and so this is a special case of the general definition.

We instead say [[model]] of a [[theory]] when we restrict to those structures which satisfy the axioms of a theory (in other words, satisfy _properties_ specified by the axioms). In this case there is a full and faithful functor from the category of models of a theory $T$ to the category of structures of the underlying language $L(T)$, while the composition of forgetful functors 

$$Mod_T \to Struct_{L(T)} \to Set$$ 

is again faithful. 

+-- {: .num_remark}
###### Remarks 
Thus, the English word "structure" is used in several slightly differing mathematical senses. 

1. Within category theory itself, "structure" can function as a kind of mass noun, as in a phrase like "forgetting structure". Here it refers to data comprising operations, relations, constants, and _also properties_ borne by models of a theory or relative theory, considered abstractly (for example, the functor $Grp \to Set$ which forgets group structure, or the functor $Ring \to Ab$ which forgets multiplicative structure). On the other hand, it can also operate in the singular, where one says for example "a topological group is a topological space equipped with a group structure, such that..." 

1. In model theory, however, the term _structure_ is not a mass noun; it refers to a _particular_ set (or "structures" for a family of sets) together with functions, relations, and elements that interpret the symbols of operations, predicates, and constants of a _language_. When one adds axioms to a language to make a _theory_, then a structure of the language where those axioms get interpreted as properties _satisfied_ by the structure is called a _model_ of the theory. Thus, in summary, the category theorist might refer to "the structure of a group" as consisting of a multiplication, a unit, etc., satisfying group axioms, while the model theorist would say that each particular group (like $\mathbb{Z}$) is a model of a theory of groups.  For a model theorist, being a model does entail being a structure for the language of groups, but she would also say that a structure for the language of groups need not satisfy any of the axioms of a group (like associativity or unitality).
=-- 

## Examples

There are gazillions of examples of objects equipped with extra structure. The most familiar is maybe

* [[algebraic structure]].

Generally the [[forgetful functor]] from a category of algebras over an [[algebraic theory]] down to the base category exhibits the equipment with the corresponding algebraic structure.

## Structures in dependent type theory
 {#InDependentTypeTheory}

In [[dependent type theory]] the notion of "mathematical structure" and/or *data structure* on a base $B \,\colon\, Type$ is given by iterated [[dependent pairs|dependent pairings]] (hence forming "[[type telescopes]]" also called  "records" in [[Coq]]) with $B$-dependent types encoding operations on/with this type together with their behavioural specification.


The following shows some examples, using the notation for [[dependent pairs]] from [[dependent functions and dependent pairs -- table|here]].


{#StructureIdentityPrinciple} Via the [[extension (semantics)|extensionality]] principles for [[dependent pairs]] ([here](dependent+sum+type#ExtensionalityPrinciple)) and for [[dependent functions]] ([here](function+extensionality#StatementForDependentFunctions)) such type theoretic structure automatically obey the *[[structure identity principle]]*:

<img src="/nlab/files/DependentPairExtensionality-230121.jpg" width="600">

<img src="/nlab/files/DependentFunctionExtensionality-230121.jpg" width="600">

In that any equivalence/identification between pairs of data of the following types are isomorphisms in the sense of bijective [[homomorphisms]].



### Lensed data structure

To say that a given data (base) type $B \,\colon\, Set$ is

1. equipped with

   1. a [[function type|function]] $read_D \,\colon\, B \to D $ reading out $D$-data;

   1. a [[function type|function]] $write_D \,\colon\, D \times B \to B$ (over-)writing $D$-data;

1. such that this does behave as expected, namely as a [well-behaved](lens+in+computer+science#LensesAreCostateCoalgebras) $D$-[[lens (in computer science)|lens]]-structure on $B$

means to declare it to be of the following iterated [[dependent pair]]-[[telescope]] [[type]]:

<img src="/nlab/files/WellBehavedLensDataStructure-230130.jpg" width="740">



### Group data structure
 {#GroupDataStructure}

The [[dependent pair]]-[[telescope]] [[type]] declaration of [[group objects|group structure]]:

<img src="/nlab/files/GroupDataType-230130.jpg" width="710">

Further restriction to [[abelian groups]]:

<img src="/nlab/files/AbelianGroupData-230129.jpg" width="620">

Via the [[structure identity principle]] ([above](#StructureIdentityPrinciple)), the [[identification type|identitifications]]/[[type equivalence|equivalences]] between such group data types are indeed bijective [[group homomorphisms]], hence group-[[isomorphisms]]:

<img src="/nlab/files/GroupDataIsomorphism-230131.jpg" width="820">

The structure of [[subgroups]] of a given group structure:

<img src="/nlab/files/SubgroupDataStructure-230201.jpg" width="900">

and their [[underlying]] abstract group structure:

<img src="/nlab/files/UnderlyingGroupOfSubgroupStructure-230201.jpg" width="900">


### Group action structure
 {#GroupActionStructure}

The [[dependent pair]]-[[telescope]] [[type]] declaration of [[group actions]] on [[sets]] ([[G-sets]]):


<img src="/nlab/files/GroupActionDataStructure-230220.jpg" width="900">


Specialization to [[torsors]]:

<img src="/nlab/files/TorsorDataStructure-230220.jpg" width="900">





### Ring data structure
 {#RingDataStructure}

The [[dependent pair]]-[[telescope]] [[type]] declaration of [[unital ring|unital]] [[ring objects|ring structure]]:

<img src="/nlab/files/RingDataStruture-230129.jpg" width="740">

For examples see at *[[numbers]]* -- *[In dependent type theory](https://ncatlab.org/nlab/show/number#InDependentTypeTheory)*.

### Module data structure
 {#ModuleDataStructure}

Given a [[unital ring|unital]] [[ring]] type $R \colon Ring$ (as [above](#RingDataStructure)), the type of $R$-[[module objects]] is the following [[dependent pair]]-[[telescope]]:


<img src="/nlab/files/ModuleDataStructure-230129.jpg" width="740">

## Higher structures in homotopy type theory
 {#HigherStructuresInHoTT}

The [above](#InDependentTypeTheory) examples of structures formulated in dependent type theory all had data [[h-set|sets]] as their base, which is the classical situation. But in [[dependent type theory]] with untruncated [[identification types]], hence in [[homotopy type theory]], we may simply drop this constraint and consider structures whose base is any higher [[homotopy type]]: This yields the notion of *[[higher structures]]*.

### Delooping

Given a set-based [[group object|group structure]] (as [above](#GroupDataStructure)), [[delooping]] structure is 

(...)


### Higher delooping

More generally, one may consider delooping of [[n-groups|$n$-groups]], but this is a lot of (higher) structure if spelled out in detail. Yet more generally and again more readily axiomatized there is the notion of deloopings of any [[pointed object|
pointed]] types (cf. [Wärn (2023, §2)](delooping#Wärn23), [BCFR23](delooping#BCFR23)), which we may write as follows:

<img src="/nlab/files/PointedHigherDeloopingStructure-230131.jpg" width="700">

Similarly there is [[iterated loop space|iterated delooping structure]]:

<img src="/nlab/files/PointedIteratedDeloopingStructure-230131.jpg" width="740">



## Related entries

* Evident as the notion of _mathematical structure_ may seem these days, it was at least not made explicit until the middle of the 20th century. Then it was the influence of the _[[Bourbaki]]_-project (see there for more) and then later the development of [[category theory]] which made the notion explicit and finally led to the above formalization.

* [[functions]] that preserves extra structure are called _[[homomorphisms]]_; [[relations]] that preserve extra structure are called [[logical relations]]_

* [[Birkhoff's HSP theorem]]

* [[structuralism]], [[structure identity principle]]

* [[exceptional structure]]


## References

### General

On the history of the notion of "mathematical structure" with some focus on what [[Bourbaki]] did and did not contribute to the subject:

* [[Leo Corry]], *Mathematical Structures from Hilbert to Bourbaki: The Evolution of an Image of Mathematics*, in: *Changing Images of Mathematics in History. From the French Revolution to the new Millenium* Harwood Academic Publishers (2001) 167-186 &lbrack;[ISBN:9780415868273](https://www.routledge.com/Changing-Images-in-Mathematics-From-the-French-Revolution-to-the-New-Millennium/Bottazini-Dalmedico/p/book/9780415868273), [pdf](https://www.leocorry.com/_files/ugd/e6fef7_15c7077b08ec4f249fb40eb961256ced.pdf)&rbrack;

* [[Leo Corry]], *Modern Algebra and the Rise of Mathematical Structures*, Springer (2004) &lbrack;[doi:10.1007/978-3-0348-7917-0](https://doi.org/10.1007/978-3-0348-7917-0)&rbrack;

See also 

* Wikipedia, *[Mathematical structure](https://en.wikipedia.org/wiki/Mathematical_structure)*

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Structure_(mathematical_logic)">Structure_(mathematical_logic)</a>*


Early proposal to grasp the notion of mathematical structures via [[category theory]] (specifically via [[forgetful functors]] between [[groupoids]]):

* {#Ehresmann57} [[Charles Ehresmann]], *Gattungen in Lokalen Strukturen*, Jahresbericht der Deutschen Mathematiker-Vereinigung **60** (1958) 49-77 &lbrack;[dml:146434](https://eudml.org/doc/146434)&rbrack;

* {#Ehresmann65} [[Charles Ehresmann]], _Cat&#233;gories et Structures_, Séminaire Ehresmann. Topologie et géométrie différentielle **6** (1964) 1-31 &lbrack;[numdam:SE_1964__6__A8_0](http://www.numdam.org/item?id=SE_1964__6__A8_0), [dml:112200](https://eudml.org/doc/112200)&rbrack;

For modern accounts on mathematical structures via [[categorical algebra]] see also at *[[algebraic theory]]*, *[[monad]]*, *[[sketch]]*.


### In dependent type theory
 {#ReferencesInDependentTypeTheory} 

Discussion of mathematical structures via [[dependent type theory]]:

the general idea of representing mathematical structures as [[type telescopes]]:

* [[Jeffery Zucker]], *Formalization of Classical Mathematics in Automath*, Colloques Internationaux du Centre National de la Recherche Scientifique **249** (1975) 135-145 &lbrack;[web](https://www.win.tue.nl/automath/archive/webversion/aut042/aut042.html), [pdf](https://www.win.tue.nl/automath/archive/pdf/aut042.pdf)&rbrack;

  also in: Studies in Logic and the Foundations of Mathematics **133** (1994) 127-139 &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)70202-7">doi:10.1016/S0049-237X(08)70202-7</a>&rbrack;

* [[Nicolaas de Bruijn]], *Telescopic mappings in typed lambda calculus*, Information and Computation **91** 2 (1991) 189-204 &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90066-B">doi:10.1016/0890-5401(91)90066-B</a>&rbrack;

and with emphasis of the notion of [[isomorphism]] between such structures:

* [[David McAllester]], *Dependent Type Theory as Related to the Bourbaki Notions of Structure and Isomorphism* &lbrack;[arXiv:2104.08958](https://arxiv.org/abs/2104.08958)&rbrack;


in [[Coq]]:

* [[Herman Geuvers]], [[Randy Pollack]], [[Freek Wiedijk]], [[Jan Zwanenburg]], *A Constructive Algebraic Hierarchy in Coq*, Journal of Symbolic Computation **34** 4 (2002) 271-286 &lbrack;[doi:10.1006/jsco.2002.0552](https://doi.org/10.1006/jsco.2002.0552), [pdf](http://www.cs.ru.nl/~herman/PUBS/JSC2002-GeuversPollackWiedijkZwanenburg-alghier1.pdf)&rbrack;

* Claudio Sacerdoti Coen, Enrico Tassi, *Working with Mathematical Structures in Type Theory*, in: *Types for Proofs and Programs. TYPES 2007*, Lecture Notes in Computer Science **4941** Springer (2008) &lbrack;[doi:10.1007/978-3-540-68103-8_11](https://doi.org/10.1007/978-3-540-68103-8_11), [pdf](https://www.cs.unibo.it/~sacerdot/PAPERS/types07.pdf)&rbrack;

* François Garillot, [[Georges Gonthier]], Assia Mahboubi & Laurence Rideau, *Packaging Mathematical Structures*, in: *Theorem Proving in Higher Order Logics. TPHOLs 2009*, Lecture Notes in Computer Science **5674**, Springer (2009) &lbrack;[doi:10.1007/978-3-642-03359-9_23](https://doi.org/10.1007/978-3-642-03359-9_23)&rbrack;

* [[Bas Spitters]], Eelis van der Wegen *Type classes for mathematics in type theory*, Mathematical Structures in Computer Science **21** 4 "Interactive Theorem Proving and the Formalisation of Mathematics" (2011) 795-825 &lbrack;[doi:10.1017/S0960129511000119](https://doi.org/10.1017/S0960129511000119), [arXiv:1102.1323](https://arxiv.org/abs/1102.1323)&rbrack;

  > (via [[ufias2012:Type classes]])

* Kazuhiko Sakaguchi, *Validating Mathematical Structures*, in *Automated Reasoning. IJCAR 2020*, Lecture Notes in Computer Science **12167**, Springer (2020) &lbrack;[doi:10.1007/978-3-030-51054-1_8](https://doi.org/10.1007/978-3-030-51054-1_8)&rbrack;

in [[Lean]]:

* [The mathlib Community](https://leanprover-community.github.io/mathlib-overview.html), §4 in: *The Lean mathematical library*, in *CPP 2020: Proceedings of the 9th ACM SIGPLAN International Conference on Certified Programs and Proofs* (2020) 367–381 &lbrack;[arXiv:1910.09336](https://arxiv.org/abs/1910.09336), [doi:10.1145/3372885.3373824](https://doi.org/10.1145/3372885.3373824)&rbrack;

Discussion of classes of mathematical structures in [[univalence|univalent]] [[homotopy type theory]] ([[univalent foundations of mathematics]]) which satisfy a [[structure identity principle]]: 

* {#CoquandDanielsson13} [[Thierry Coquand]], [[Nils Anders Danielsson]], *Isomorphism is equality*, Indagationes Mathematicae **24** 4 (2013) 1105-1120 &lbrack;[doi:10.1016/j.indag.2013.09.002](https://doi.org/10.1016/j.indag.2013.09.002)&rbrack;

* {#UFP13} [[Univalent Foundations Project]], §9.8 but also §2 of: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Escardó19} [[Martín Escardó]], *[A structure identity principle for a standard notion of structure](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#sns)*, §3.33.1 in: *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580),  [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html)&rbrack;

  > (formalized in the [[Agda]] [[proof assistant]])

* [[Benedikt Ahrens]], [[Paige Randall North]], [[Michael Shulman]], [[Dimitris Tsementzis]], *A Higher Structure Identity Principle*, LICS '20 (2020) 53–66 &lbrack;[arXiv:2004.06572](https://arxiv.org/abs/2004.06572), [doi:10.1145/3373718.3394755](https://doi.org/10.1145/3373718.3394755)&rbrack;

Discussion in the context of the [[philosophy]] of [[structuralism]]:

* [[Dimitris Tsementzis]], §5.1 in: *Univalent foundations as structuralist foundations*, Synthese **194** 9 (2017) 3583–3617 &lbrack;[jstor:26748765](https://www.jstor.org/stable/26748765), [doi:10.1007/s11229-016-1109-x](https://doi.org/10.1007/s11229-016-1109-x), [pdf](https://core.ac.uk/download/pdf/157866891.pdf)&rbrack;

Expressions towards the notion that, thereby the notions of *mathematical structures* are *data structures* may be understood to coincide (just along the lines of *[[types]]* being *[[data types]]*):

* [[Thomas Kehrenberg]], *Basic building blocks of dependent type theory* (Dec. 2022) &lbrack;[post on LessWrong](https://www.lesswrong.com/posts/ccbsYSpTcTqXwukH8/basic-building-blocks-of-dependent-type-theory), [post on personal blog](https://tm.kehrenberg.net/a/type-theory1/)&rbrack;

> "An example of a use case for non-binary sum types is the definition of mathematical “data structures” like a ring or a group. These data structures are usually defined as..."




[[!redirects structure]]
[[!redirects structures]]

[[!redirects mathematical structure]]
[[!redirects mathematical structures]]


