
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Relations
* table of contents
{: toc}

## Idea

A _relation_ is the extension of a _[[predicate]]_.  That is, if you have a statement whose [[truth value]] may depend on some [[variables]], then you get a relation that consists of those instantiations of the variables that make the statement [[true]].  Equivalently, you can think of a relation as a [[function]] whose [[target]] is the set of truth values.


## Definitions

### General case
 {#DefinitionGeneralCase}

+-- {: .num_defn }
###### Definition

Given a [[family of sets|family]] $(A_i)_{i: I}$ of [[sets]], a **relation** on that family is a [[subset]] $R$ of the [[cartesian product]] $\prod_{i: I} A_i$.  

Equivalently, this is a [[function]] from $\prod_{i: I} A_i$ to the set $\TV$ of [[truth values]] (because $\TV$ is the [[subobject classifier]] in [[Set]]).

Also equivalently, this is a [[monomorphism]] in/[[subobject]] of the [[cartesian product]]

$$
  R \hookrightarrow \prod_{i \colon I} A_i
  \,.
$$

=--


+-- {: .num_remark }
###### Remark

For $I$ the 2-element set (a _binary relation_) this is in particular a binary [[correspondence]]

$$
  \array{
     && R
     \\
     & \swarrow && \searrow
     \\
    A_1 && && A_1
  }
  \,.
$$

Hence relations are precisely the [[(-1)-truncated]] [[correspondences]].

This identification induces a natural notion of [[composition]] of relations from the composition in the [[category of correspondences]], see below at _[The 2-poset of binary relations](#The2PosetOfBinaryRelations)_.

Formulated this way, the notion of relation generalizes to [[categories]] other than [[Set]] and to [[higher category theory]]. For more on this see at _[Generalizations](#Generalization)_ below.

=--

### Special cases

A __nullary relation__ is a relation on the empty family of sets.  This is the same as a [[truth value]].

A __unary relation on $A$__ is a relation on the singleton family $(A)$.  This is the same as a [[subset]] of $A$.

A __binary relation on $A$ and $B$__ is a relation on the family $(A,B)$, that is a subset of $A \times B$.  This is also called a __relation from $A$ to $B$__, especially in the context of the $2$-category [[Rel]] described below, or sometimes called a __heterogenous relation__.

A __binary relation on $A$__ is a relation on $(A,A)$, that is a relation from $A$ to itself.  This is sometimes called a __homogenous relation__ on $A$, simply a __relation on $A$__, or just an __endorelation__ with its set implicit as a property if not explicitly mentioned.

An __$n$-ary relation__ on $A$ is a relation on a family of $n$ copies of $A$, that is a subset of $A^n$.

For a binary relation, one often uses a symbol such as $\sim$ and writes $a \sim b$ instead of $(a,b) \in \sim$.  Actually, even when a relation is given by a letter such as $R$, one often sees $a R b$ instead of $(a,b) \in R$, although now that does not look so good.

### Internal and external relations

In foundations of mathematics with a [[sort]] of [[propositions]] and a separate sort of [[sets]], such as most presentations of [[set theory]] in [[first-order logic]] with [[equality]], there are actually two notions of relation. The definition given above is the notion of **internal relation**, defined as a [[subset]] of the [[Cartesian product]] of a [[family of sets]]. There is a second definition of relation on a set: external relations, which are not defined purely inside of the set theory. Since each set has a type of elements inside of the set, an **external relation** is simply a [[proposition]] in the [[context]] of a family of [[variables]] $x_i$ inside of a family of sets $A_i$
$$\Gamma, x_0 \in A_0, x_1 \in A_1, x_2 \in A_2, \ldots, x_n \in A_n \vdash P \; \mathrm{prop}$$
In any [[unsorted set theory]], those variables would be expressed as
$$\Gamma, x_0, A_0, x_0 \in A_0 \; \mathrm{true}, x_1, A_1, x_1 \in A_1 \; \mathrm{true}, x_2, A_2, x_2 \in A_2 \; \mathrm{true}, \ldots, x_n, A_n, x_n \in A_n \; \mathrm{true} \vdash P \; \mathrm{prop}$$
It is in this second sense of external relation that [[equality]] in [[first-order logic with equality]] is an [[equivalence relation]], and [[inequality]] is a [[tight apartness relation]] in a first-order theory with equality presented in [[classical logic]]. 

In [[dependent type theory]], where propositions are considered to be the [[subsingletons]] or the [[sets]]/[[types]] themselves, there is only one notion of relation, the internal notion given above. 

## Morphisms

If $A$ and $B$ are each sets equipped with a relation, then what makes a [[function]] $f: A \to B$ a _morphism_ of sets so equipped?

There are really two ways to do this, shown below.  (We will write these as if each set is equipped with a binary relation $\sim$, but any fixed arity would work.)

*  $f$ __preserves__ the relation if $x \sim y \;\Rightarrow\; f(x) \sim f(y)$ always;
*  *f* __reflects__ the relation if $x \sim y \;\Leftarrow\; f(x) \sim f(y)$ always.

Now, if $f$ is a [[bijection]], then it preserves the relation if and only if its inverse reflects it, so clearly an [[isomorphism]] of relation-equipped sets should do both.  What about a mere morphism?

In general, it\'s more natural to require only preservation; these are the morphisms you get if you consider a set with a relation as a models of a [[algebraic theory|finite-limit theory]] or a simply [[directed graph]].

But in some contexts, particularly when dealing only with [[irreflexive relation]]s, we instead require (only) that a morphism reflect the relation.  Sometimes an even stricter condition is imposed, as for [[well-order]]s.  But even in these cases, the definition of isomorphism comes out the same.


## Binary relations

Binary relations are especially widely used.


### Kinds of binary relations

Special kinds of relations from $A$ to $B$ include:

* [[functional relations]],
* [[entire relations]],
* [[difunctional relation|difunctional relations]]
* [[one-to-one relation]]s,
* [[onto relation]]s.

Combinations of the above properties of binary relations produce:

* [[functions]],
* [[partial functions]],
* [[injections]],
* [[surjections]],
* [[bijections]].

Special kinds of binary relations on $A$ (so from $A$ to itself) additionally include:

* [[reflexive relation|reflexive]] and [[irreflexive relation|irreflexive]] relations;
* [[symmetric relation|symmetric]], [[antisymmetric relation|antisymmetric]], and [[asymmetric relation|asymmetric]] relations;
* [[transitive relations]] and [[comparisons]];
* left and right [[euclidean relations]];
* [[total relation|total]] and [[connected relation|connected]] relations;
* [[extensional relation|extensional]] and [[well-founded relation|well-founded]] relations.

Combinations of the above properties of binary relations produce:

* [[equivalence relations]],
* [[partial equivalence relations]],
* [[apartness relations]],
* the various kinds of [[orders]] (which see).

### Structure preserving relations

Given [[pointed sets]] $(A, a)$ and $(B, b)$, a binary relation $R$ from $A$ to $B$ is said to preserve the point if $R(a, b)$. 

Given sets with endofunctions $(A, f_A)$ and $(B, f_B)$, a binary relation $R$ from $A$ to $B$ is said to preserve the endofunction if for every $a \in A$ and $b \in B$, if $R(a, b)$, then $R(f(a), f(b))$. 

Given [[magmas]] $(A, \mu_A)$ and $(B, \mu_b)$, a binary relation $R$ from $A$ to $B$ is said to preserve the binary operation if for every $a \in A$, $c \in A$, $b \in B$ and $d \in B$, if $R(a, b)$ and $R(c, d)$, then $R(\mu_A(a, c), \mu_B(b, d))$. 

And so forth. 

### Properties

Every binary endorelation $R$ has an [[equivalence relation]] $\sim_R$ generated by $R$. 

### Binary relations as a coalgebra

By [[currying]] the binary relation $R: \mathcal{P}(X \times X) \cong X \times X \rightarrow \Omega$, one gets a [[coalgebra for an endofunctor|coalgebra]] $\theta: X \rightarrow (X \rightarrow \Omega) \cong X \rightarrow \mathcal{P}(X)$ for the [[powerset]] [[endofunctor]] on [[Set]].  

### The $2$-poset of binary relations
 {#The2PosetOfBinaryRelations}

Binary relations form a $2$-[[2-category|category]] (in fact a $2$-[[2-poset|poset]]) [[Rel]], which is the basic example of an [[allegory]].

The [[objects]] are [[sets]], the [[morphisms]] from $A$ to $B$ are the binary relations on $A$ and $B$, and there is a [[2-morphism]] from $R$ to $S$ (both from $A$ to $B$) if $R$ implies $S$ (that is, when $(a,b) \in R$, then $(a,b) \in S$).

The interesting definition is [[composition]] 

+-- {: .num_defn #CompositionOfRelations}
###### Defintion

If $R$ is a relation from $A$ to $B$ and $S$ is a relation from $B$ to $C$, then their _composite relation_  -- written $S \circ R$ or $R;S$ -- from $A$ to $C$ is defined as follows:
$$(a,c) \in R;S \;\Leftrightarrow\; \exists b: B,\; (a,b) \in R \;\wedge\; (b,c) \in S.$$

The identity morphism is given by [[equality]].

=--

+-- {: .num_remark}
###### Remark

The [[composition]] operation of relation from def. \ref{CompositionOfRelations} is induced by the composition of the underlying [[correspondences]], followed by [[(-1)-truncated|(-1)-truncation]].

=--

The special properties of the kinds of binary relations listed earlier can all be described in terms internal to [[Rel]]; most of them make sense in any [[allegory]].  Irreflexive and asymmetric relations are most useful if the allegory\'s [[hom-object|hom-poset]]s have [[bottom]] elements, and linear relations require this.  Comparisons require the hom-posets to have finite [[union|unions]], and well-founded relations require some sort of higher-order structure.

As a [[function]] may be seen as a functional, entire relation, so the category [[Set]] of sets and functions is a [[subcategory]] of [[Rel]] (in fact a [[replete subcategory|replete]] and locally [[full subcategory|full]] sub-$2$-category).

### The quasitopos of endorelations {#endorel}

Endorelations on sets are the objects of the [[quasitopos]] __$EndoRel$__ or __$Bin$__. It is a  [[reflective subcategory]] of [[Quiv]] the [[category of presheaves|presheaf topos]] of quivers and its morphisms are quiver morphisms. Endorelations are the [[separated presheaf|separated presheaves]] for the [[double negation#in_topos_theory|double negation topology]] on $Quiv$. "Separated" here translates to a quiver having  at most one arc between pairs of verticies. The [[reflective subcategory|reflector]] $Quiv \to EndoRel$ collapses parallel arcs together. Such quivers might also be called __singular__ or __simple__  though sometimes "simple" also means "no loops".

#### Relation closures as reflective subcategories of $EndoRel$

All of the sub-types  of endorelations with positive conditions ([[reflexive relation|reflexive]], [[symmetric relation|symmetric]], [[transitive relations|transitive]], and left and right [[euclidean relations|euclidean]]) and their combinations have an associated [[Moore closure|closure]] that can produce one from an arbitrary relation. Such a closure [[completion|completes]] a relation by adding the least number of arcs such that the conditions are satisfied.
Within $EndoRel$ these closures are reflectors that produce reflective subcategories.
For example the __symmetric closure__ $sym: EndoRel \to EndoSym$ will (possibly) enlarge  a quiver that contains any arc $v_a \to v_b$ to one that also contains  $v_b \to v_a$. The __transitive and reflexive closure__ $transRef: EndoRel \to EndoTransRef$ produces a category which is isomorphic to [[preorder|PreOrd]] though its objects are the underlying quivers of the preorders which are the objects of $PreOrd$.

In addition to being reflective, the categories from the _symmetric_, _reflexive_, and _symmetric and reflexive_  closures are also quasitoposes that can be [[quasitopos#exampsep|directly defined]] through  double negation separation. The _symmetric and reflexive_ closure ([[category of simple graphs|SimpGph]]) is also a [[quasitopos|Grothendieck quasitopos]]. On the other hand $PreOrd$ is not a quasitopos because it is not a [[regular category]].

## Ternary relations 

Apart from binary relations, there are important ternary relations used in mathematics, which for the most part are [[families]] of binary relations indexed by a third set:

* [[uniformity]], where the index set is the set of [[entourages]]. 
* [[premetric]], where the index set is the set of [[real numbers]], or in some cases, the set of [[rational numbers]]. 

## Generalisation
 {#Generalization}

Most of the preceding makes sense in any [[category]] with enough [[products]]; giving rise to [[internal relation|internal relations]], for instance _[[congruences]]_ in the case of internal equivalence relations. 

Probably the trickiest bit is the definition of [[composition]] of binary relations, so not every category with [[finite products]] has an [[allegory]] of relations.  In fact, in a certain precise sense, a category has an allegory of relations if and only if it is [[regular category|regular]].  It can then be recovered from this allegory by looking at the functional entire relations.


## Related concepts

* [[Rel]]

* [[graph]]

* [[logical relation]]

* [[quantum relation]]

* [[corelation]]


[[!include flavors of modal logics and relations -- table]]



[[!redirects relation]]
[[!redirects relations]]
[[!redirects relation theory]]
[[!redirects theory of relations]]

[[!redirects nullary relation]]
[[!redirects nullary relations]]

[[!redirects unary relation]]
[[!redirects unary relations]]

[[!redirects binary relation]]
[[!redirects binary relations]]

[[!redirects binary endorelation]]
[[!redirects binary endorelations]]

[[!redirects internal relation]]
[[!redirects internal relations]]

[[!redirects external relation]]
[[!redirects external relations]]
