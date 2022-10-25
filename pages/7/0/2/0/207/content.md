
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

There is a lot of interesting stuff to be said about _equality_ in [[logic]], [[higher category theory]], and the [[foundations]] of mathematics, but it hasn\'t all been said here yet.

## Different kinds of equality
   {#DifferentKinds}

Here is a list of distinctions between different notions of _equality_, in different contexts, where possibly all the following pairs of notions are, in turn, "the same", just expressed in terms of different terminologies:

*  the difference between [[axiom|axiomatic]] and [[definition|defined]] equality;
*  the difference between identity and equality,
*  the difference between intensional and extensional equality,
*  the difference between equality [[judgements]] and equality [[propositions]],
*  the difference between equality and [[isomorphism]],
*  the difference between equality and [[equivalence]],
*  the possibility of operations that might not preserve equality.


## In type theory

In a formal language such as [[type theory]], one distinguishes various different notions of _equality_ or _equivalence_ of the terms of the language.

In [[type theory]], there are broadly three different notions of equality which could be distinguished: **judgmental equality**, **propositional equality**, and **typal equality**. Judgmental equality is defined as a basic judgment in type theory. Propositional equality is defined as a proposition in any two-layered type theory with a layer of types and a layer of propositions. Typal equality is the [[identity type]] or [[path type]] in type theory. 

### Judgmental equality

The first notion of equality is **judgmental equality**, where we simply judge two elements to be equal to each other. Judgmental equality is expressed in type theory by a separate [[judgment]]: in addition to typing judgments $\Gamma \vdash (t:A)$, we have equality judgments $\Gamma \vdash (t = t'): A$. The rules for manipulating such judgments then include reflexivity, symmetry, transitivity, making judgmental equality into a judgmental [[equivalence relation]]. 

However, not all type theories have judgmental equality; most [[first-order theories]] use propositional equality in place of judgmental equality, and [[objective type theories]] use typal equality in place of judgmental equality.

### Propositional equality

In any two-layer type theory with a layer of [[types]] and a layer of [[propositions]], or equivalently a [[first order logic]] over [[type theory]] or a [[first-order theory]], every type $A$ has a binary [[relation]] according to which two elements $x$ and $y$ of $A$ are related if and only if they are equal; in this case we write $x \equiv_A y$. Since relations are propositions in the context of a term variable judgment in the type layer, this is called **propositional equality**. Notable examples of propositional equality include the equality in all flavors of [[set theory]], such as [[ZFC]] or [[ETCS]].  

The presence of propositional equality is part of the axiomatization of first-order theories, although this is usually swept under the rug by including propositional equality by default in all first-order theories.  (It has to be made more explicit in a structural set theory such as [[SEAR]], where there is no propositional equality on sets themselves, only on elements of a particular set.) By contrast, in a first order theory without propositional equality, propositional equality is an [[equivalence relation]] which has to be put onto a [[type]] or [[preset]].

### Typal equality

However, not all type theories are [[first order logic]] over [[type theory]], nor are they even two-layered type theories. In type theories with only one layer for types, equality is not a relation, but rather a type family. Since type families are types in the context of a term variable judgment, this is called **typal equality**. Because typal equality is a type, it is usually also called the **equality type**, **identity type**, **path type**, or **identification type**, and the terms of typal equality are called **equalities**, **identities**, **identifications**, **paths**. Notable examples of typal equality include the [[identity type]] in [[Martin-Löf type theory]] and [[higher observational type theory]], and the [[cubical path type]] in [[cubical type theory]]. 

Type theories with only typal equality are called [[objective type theories]]. In type theories with both typal equality and either judgmental equality or propositional equality, one could distinguish between [[intensional type theories]] and [[extensional type theories]]: extensional type theories are type theories with an equality reflection rule, where one could derive judgmental or propositional equality from typal equality:

$$\frac{\Gamma \vdash p:a =_A b}{\Gamma \vdash a \equiv b:A} \qquad \frac{\Gamma \vert \Phi \vdash p:a =_A b}{\Gamma \vert \Phi \vdash a \equiv_A b \; \mathrm{true}}$$

Intensional type theories are then type theories with typal equality and one of either judgmental or propositional equality without an equality reflection rule. 

Note that this notion of extensionality is different from the [[axiom of extensionality]] or [[function extensionality]]. 

### Comparison of equalities

* Judgmental equality of terms: 
$$a \equiv b:A$$

* Propositional equality of terms
$$a \equiv_A b \; \mathrm{true}$$

* Typal equality of terms (i.e. [[identity type]]): 
$$p:a =_A b$$

* Judgmental equality of types: 
$$A \equiv B \; \mathrm{type}$$

* Propositional equality of types
$$A \equiv B \; \mathrm{true}$$

* Typal equality of types (i.e. [[equivalence of types]]): 
$$P:A \simeq B$$

* Substitution of judgmentally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta \vdash B[a/x] \equiv B[b/x] \; \mathrm{type}}$$

* Substitution of propositional equal terms:
$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a : A \quad \Gamma \vert \Phi \vdash b : A \quad \Gamma \vert \Phi \vdash a \equiv_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vert \Phi \vdash B \; \mathrm{type}}{\Gamma, \Delta \vert \Phi \vdash B[a/x] \equiv B[b/x] \; \mathrm{true}}$$

* Substitution of typally equal terms (i.e. [[transport]]):
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta \vdash \mathrm{tr}(x.B, a, b, p):B[a/x] \simeq B[b/x]}$$

## Usages of equality

The three different notions of equality above could be used in definitions, where the equality is called **definitional equality**, as well as in the computation and uniqueness rules of type formers, where the equality is called **computational equality**, **conversional equality**, or **reductional equality**. 

### Computational equality

One usage of equality is in the computation rules and uniqueness rules for the various type formers, such as [[∞-reduction]] or [[∞-conversion]] (the choice of rules depends on the type theory). The usage of equality in this manner is called *computational*, *conversional*, or *reductional* equality, and is the congruence on terms generated by the conversion or reduction rules. 

Computational equality comes in judgmental, propositional, and typal versions. For example, the computation rule for the [[dependent product type]] could be expressed in judgmental, propositional, and typal equality:

* Judgmental computation rules:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) \equiv b[a/x]:B[a/x]}$$

* Propositional computation rules:

$$\frac{\Gamma, x:A \vert \Phi \vdash b(x):B(x) \quad \Gamma \vert \Phi \vdash a:A}{\Gamma \vert \Phi \vdash \lambda(x:A).b(x)(a) \equiv_{B[a/x]} b[a/x] \; \mathrm{true}}$$

* Typal computation rules:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_\Pi:\lambda(x:A).b(x)(a) =_{B[a/x]} b[a/x]}$$

The paradigmatic example of computational equality is a pair of terms like "$(\lambda x. x+x)(2)$" and "$2+2$", where the second is obtained by $\beta$-reduction from the first.  In a type theory that includes definitions by [[recursion]], expansion of a recursor is also computational equality. For instance, if addition is defined by recursion, then "$2+2$" (that is, $s(s(0))+s(s(0))$) reduces via this rule to "$4$" (that is, $s(s(s(s(0))))$).

### Definitional equality

Another notion is _definitional equality_ or _intensional equality_.

According to [PML (1980), p. 31](#PML):

> Definitional equality is intensional equality, or equality of meaning (synonymy). [...] It is a relation between linguistic expressions [...] Definitional equality is the equivalence relation generated by abbreviatory definitions, changes of [[bound variables]] and the [[principle of substituting equals for equals]]. [...] Definitional equality can be used to rewrite expressions [...].

on p. 60:

> ... intensional (sameness of meaning) ...

For instance the symbols "$2$" and "$s(s(0))$" (meaning the successor of the successor of $0$) are definitionally/intensionally equal terms (of type the [[natural numbers]]): the first is merely an abbreviation for the second.

## History

The notion of definitional equality was introduced first in [[AUTOMATH]]. The following paper presents a suggestive explanation of this notion and how proof-checking was designed in this system (especially section 10):

[On the roles of types in mathematics](http://uf-ias-2012.wikispaces.com/file/view/deB1.pdf/401388596/deB1.pdf)

The notion of definitional equality was later introduced by [[Per Martin-Löf]], first in the context of normalization proofs for higher-order logic in the paper [Hauptsatz for Intuitionistic Simple Type Theory](http://www.sciencedirect.com/science/article/pii/S0049237X09703659) and generalized in Type Theory. He discusses this notion in the paper [About Models for Intuitionistic Type Theory and The notion of Definitional Equality](http://www.sciencedirect.com/science/article/pii/S0049237X08707274).

The extension from AUTOMATH is that one adds the notion of data type (natural number), of constructors (zero and successor) and primitive recursion as definitional equality. The motivation is that one can consider the schema of primitive recursion as a definition of a function.

This was also influenced by natural deduction, where constructors correspond to introduction rules and the work of Gödel on system T.

With this extension, one obtains a programming language with dependent types and where computations correspond to unfolding of definitions (that can be primitive recursive definitions). This programming language has the feature that all computations terminate. This has been also considered in functional programming, see e.g. the discussion in [this paper](http://uf-ias-2012.wikispaces.com/file/view/turner.pdf/401400700/turner.pdf).

A description of the evaluation algorithm using techniques from functional programming
can be found in [this work of Gregoire and Leroy](http://uf-ias-2012.wikispaces.com/file/view/strong-reduction.pdf/402005168/strong-reduction.pdf).  

## Internal equality in set theory

Relations and equality could be [[internal logic of set theory|internalized in any set theory]]: the internal equality in set theory is the smallest internal [[reflexive relation]] on $S$, and it is in fact an internal [[equivalence relation]]; it is the only internal equivalence relation on $S$ that is also a [[partial order]] (although that fact is somewhat circular).  This relation is often called the __identity relation__ on $S$, either because 'identity' can mean 'equality' or because it is the [[identity]] for [[composition]] of relations. 

In the [[category]] of reflexive relations on $S$, the [[equality relation]] on $S$ is an [[initial object|initial reflexive relation]]; when the equality relation is a [[type family]] instead of a family of propositions, then the equality relation is the initial type generated by reflexivity or the [[first law of thought]].

As a [[subset]] of $S \times S$, the equality relation is often called the __[[diagonal]]__ and written $\Delta_S$ or similarly.  As an abstract set, this subset is [[isomorphism|isomorphic]] to $S$ itself, so one also sees the diagonal as a map, the [[diagonal function]] $S \overset{\Delta_S}\to S \times S$, which maps $x$ to $(x,x)$; note that $x = x$.  This is in [[Set]]; analogous [[diagonal morphisms]] exist in any [[cartesian monoidal category]].

## Related concepts

* **equality**, [[equation]]

* [[identity type]], 

* [[identity of indiscernibles]]

* [[inequality]]

  * [[denial inequality]] 
  
  * [[apartness relation]]

* [[isomorphism]]

* [[equivalence]]

* [[weak equivalence]]

* [[homotopy equivalence]], [[weak homotopy equivalence]]

* [[equivalence in an (∞,1)-category]]

* [[equivalence of (∞,1)-categories]]

[[!include logic symbols -- table]]


## References

In 

* [[Georg Hegel]], _[[Science of Logic]]_, 1812

equality is the subject of volume 1, book 2 "Die Lehre vom Wesen" (The doctrine of essence). As discussed at _[[Science of Logic]]_, one can roughly identify in Hegel's text there the notion of intensional identity and of the reflector term in [[identity types]].

Texts on [[type theory]] typically deal with the subtleties of the notion of _equality_. For instance

* [[Per Martin-Löf]], _Intuitionistic type theory_, Lecture notes (1980)
  {#PML}

Besides 

* [[Kurt Gödel]], _Über eine bisher noch nicht benützte Erweiterung des finiten Standpunktes_. Dialectica (1958), pp. 280–287, 

which might be the first paper to mention intensional equality (and the fact that it should be decidable), there is

* [[Nicolaas de Bruijn]], _[[Automath]]_, 

where de Bruijn makes a distinction between definitional equality and "book" equality.


[[!redirects equal]]
[[!redirects equals]]
[[!redirects equality]]
[[!redirects equalities]]
[[!redirects equality predicate]]
[[!redirects equality predicates]]

[[!redirects equality relation]]
[[!redirects equality relations]]
[[!redirects identity relation]]
[[!redirects identity relations]]
[[!redirects diagonal relation]]
[[!redirects diagonal relations]]

[[!redirects definitional identity]]
[[!redirects definitional identities]]
[[!redirects definitional equality]]
[[!redirects definitional equalities]]

[[!redirects computational identity]]
[[!redirects computational identities]]
[[!redirects computational equality]]
[[!redirects computational equalities]]

[[!redirects intensional identity]]
[[!redirects intensional identities]]
[[!redirects intensional equality]]
[[!redirects intensional equalities]]
[[!redirects extensional equality]]
[[!redirects extensional equalities]]
