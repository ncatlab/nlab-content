
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
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

\tableofcontents

## Idea

In a formal language such as [[type theory]], one distinguishes various different notions of _equality_ or _equivalence_ of the terms of the language.

In [[type theory]], there are broadly three different notions of equality which could be distinguished: **judgmental equality**, **propositional equality**, and **typal equality**. Judgmental equality is defined as a basic judgment in type theory. Propositional equality is defined as a proposition in any [[predicate logic over type theory]]. Typal equality is defined as a type in type theory. 

**Note**: In this article, we use the term *propositional equality* in the sense of equality as a proposition and proposition as different from types. In [[dependent type theory]], there is a different notion of propositional equality where equality is a proposition, but in the sense of [[propositions as subsingletons]] or [[propositions as types]]. For that, see [[propositional equality#InDependentTypeTheory|propositional equality § In dependent type theory]]. 

### Judgmental equality

The first notion of equality is **[[judgmental equality]]**, where we simply judge two elements to be equal to each other. Judgmental equality is expressed in type theory by a separate [[judgment]]: in addition to typing judgments $\Gamma \vdash (t:A)$, we have equality judgments $\Gamma \vdash (t = t'): A$. The rules for manipulating such judgments then include reflexivity, symmetry, transitivity, making judgmental equality into a judgmental [[equivalence relation]]. 

However, not all type theories have judgmental equality; most [[first-order theories]] use propositional equality in place of judgmental equality, and [[objective type theories]] use typal equality in place of judgmental equality.

### Propositional equality

In any two-layer type theory with a layer of [[types]] and a layer of [[propositions]], or equivalently a [[first order logic]] over [[type theory]] or a [[first-order theory]], every type $A$ has a binary [[relation]] according to which two elements $x$ and $y$ of $A$ are related if and only if they are equal; in this case we write $x =_A y$. Since relations are propositions in the context of a term variable judgment in the type layer, this is called **[[propositional equality]]**. The formation and introduction rules for propositional equality is as follows

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, y:A \vdash x =_A y \; \mathrm{prop}} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash x =_A x \; \mathrm{true}}$$

Then we have the elimination rules for propositional equality:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A, x =_A y \; \mathrm{true} \vdash P(x, y) \; \mathrm{prop} \quad \Gamma, x:A \vdash P(x, x) \; \mathrm{true}}{\Gamma, x:A, y:A, x =_A y \; \mathrm{true} \vdash P(x, y) \; \mathrm{true}}$$

Propositional equality satisfies the [[principle of substitution]] and the [[identity of indiscernibles]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{prop}}{\Gamma, x:A, y:A \vdash (x =_A y) \implies (P(x) \iff P(y)) \; \mathrm{true}}$$

In addition, one could have propositional equality between the types themselves, with formation and introduction rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A = B \; \mathrm{prop}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A = A \; \mathrm{true}}$$

Notable examples of propositional equality include the equality in all flavors of [[set theory]], such as [[ZFC]] or [[ETCS]].  

The presence of propositional equality is part of the axiomatization of first-order theories, although this is usually swept under the rug by including propositional equality by default in all first-order theories.  (It has to be made more explicit in a structural set theory such as [[SEAR]], where there is no propositional equality on sets themselves, only on elements of a particular set.) By contrast, in a first order theory without propositional equality, propositional equality is an [[equivalence relation]] which has to be put onto a [[type]] or [[preset]].

### Typal equality

However, not all type theories are [[first order logic]] over [[type theory]], nor are they even two-layered type theories. In type theories with only one layer for types, equality is not a relation. Instead, we have what are called **[[typal equality]]**, as equality of both terms and types are represented by types.  Typal equality of terms is also called the **equality type**, **identity type**, **path type**, or **identification type**, and the terms of typal equality are called **equalities**, **identities**, **identifications**, **paths**. Notable examples of typal equality of terms include the [[identity type]] in [[Martin-Löf type theory]] and [[higher observational type theory]], and the [[cubical path type]] in [[cubical type theory]].

Type theories with only typal equality are called [[objective type theories]]. In type theories with both typal equality and either judgmental equality or propositional equality, one could distinguish between [[intensional type theories]] and [[extensional type theories]]: extensional type theories are type theories with an equality reflection rule, where one could derive judgmental or propositional equality of terms from typal equality of terms:

$$\frac{\Gamma \vdash p:a =_A b}{\Gamma \vdash a \equiv b:A} \qquad \frac{\Gamma \vdash p:a =_A b}{\Gamma \vdash a \equiv_A b \; \mathrm{true}}$$

Intensional type theories are then type theories with typal equality and one of either judgmental or propositional equality without an equality reflection rule. Note that this notion of extensionality is different from the [[axiom of extensionality]] or [[function extensionality]]. 

### Comparison of equalities

This table gives the six different notions of equality found in type theory. 

| Judgment | of types | of terms |
|--------|--------|--------|
| Judgmental equality | $\Gamma \vdash A = B \; \mathrm{type}$ | $\Gamma \vdash a = b:A$ |
| Propositional equality | $\Gamma \vdash A = B \; \mathrm{true}$ | $\Gamma \vdash a =_A b \; \mathrm{true}$ |
| Typal equality | $\Gamma \vdash P:A \equiv B$ | $\Gamma \vdash p:a =_A b$ |

## Structural rules of equalities

### Reflexivity

The reflexivity of equality is given by the following judgmental, propositional, and typal rules respectively:

* Reflexivity of judgmental equality

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A = A \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash a = a:A}$$

* Reflexivity of propositional equality
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A = A \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash a =_A a \; \mathrm{true}}$$

* Reflexitivity of typal equality (i.e. [[identity function]] and identity [[path]])
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash id_{A}:A \simeq A}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{refl}_{A}(a):a =_A a}$$

### Symmetry

The symmetry of equality is given by the following judgmental, propositional, and typal rules respectively:

* Symmetry of judgmental equality
$$\frac{\Gamma \vdash A = B \; \mathrm{type}}{\Gamma \vdash B = A \; \mathrm{type}}$$ 
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a = b:A}{\Gamma \vdash b = a:A}$$

* Symmetry of propositional equality
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash A = B \; \mathrm{true}}{\Gamma \vdash B = A \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash a =_A b \; \mathrm{true}}{\Gamma \vdash b =_A a \; \mathrm{true}}$$

* Symmetry of typal equality (i.e. [[inverse function]] and inverse path)
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash P:A \simeq B}{\Gamma \vdash P^{-1}:B \simeq A}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b}{\Gamma \vdash p^{-1}:b =_A a}$$

### Transitivity

The transitivity of equality is given by the following judgmental, propositional, and typal rules respectively:

* Transitivity of judgmental equality
$$\frac{\Gamma \vdash A = B \; \mathrm{type} \quad \Gamma \vdash B = C \; \mathrm{type} }{\Gamma \vdash A = C \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a = b:A \quad b = c:A }{\Gamma \vdash a = c:A}$$

* Transitivity of propositional equality
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash A = B \; \mathrm{true} \quad \Gamma \vdash B = C \; \mathrm{true}}{\Gamma \vdash A = C \; \mathrm{true}}$$ 
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash c:A \quad \Gamma \vdash a =_A b \; \mathrm{true} \quad \Gamma \vdash b =_A c \; \mathrm{true}}{\Gamma \vdash a =_A c \; \mathrm{true}}$$

* Transitivity of typal equality (i.e. [[composition]] of functions and path concatenation)
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash P:A \simeq B \quad \Gamma \vdash Q:B \simeq C}{\Gamma \vdash Q \circ P:A \simeq C}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash c:A \quad \Gamma \vdash p:a =_A b \quad \Gamma \vdash q:b =_A c}{\Gamma \vdash p \bullet q:a =_A c}$$

### Principle of substituting equals for equals 

The [[principle of substituting equals for equals]] is given by the following judgmental, propositional, and typal rules respectively:

* Substitution of judgmentally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a = b : A \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash B[a/x] = B[b/x] \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a = b : A \quad \Gamma, x:A, \Delta \vdash c:B}{\Gamma, \Delta[b/x] \vdash c[a/x] = c[b/x]: B[b/x]}$$

* Substitution of propositionally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a : A \quad \Gamma \vdash b : A \quad \Gamma \vdash a =_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash B[a/x] = B[b/x] \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a : A \quad \Gamma \vdash b : A \quad \Gamma \vdash a =_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash c:B}{\Gamma, \Delta[b/x] \vdash c[a/x] =_{B[b/x]} c[b/x] \; \mathrm{true}}$$

* Substitution of typally equal terms (i.e. [[transport]] and [[action on identifications]]):
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash \mathrm{tr}(x.B, a, b, p):B[a/x] \simeq B[b/x]}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vdash c:B}{\Gamma, \Delta[b/x] \vdash \mathrm{ap}(c, x.B, a, b, p):\mathrm{tr}(x.B, a, b, p)(c[a/x]) =_{B[b/x]} c[b/x]}$$

### Variable conversion

The variable conversion rule is given by the following judgmental, propositional, and typal rules respectively:

* Judgmental variable conversion rule:
$$\frac{\Gamma \vdash A = B \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

* Propositional variable conversion rule:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash A = B \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

* Typal variable conversion rule:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash P:A \simeq B \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, y:B, \Delta[P^{-1}(y)/x] \vdash \mathcal{J}[P^{-1}(y)/x]}$$

$\mathcal{J}$ is a generic judgment thesis. 

## Usages of equality

### In definitions of types and terms

The three different notions of equality above could be used in [[definitions]] of [[types]] and [[terms]], as well as in the rules for the [[single assignment operator]] $\coloneqq$. In [[Martin-Löf type theory]] and [[cubical type theory]], judgmental equality is used for definitional equality. In [[ZFC]] and [[ETCS]], propositional equality is used for definitional equality, and in [[objective type theories]], typal equality is used for definitional equality. 

### In conversion rules and inductive definitions

The three different notions of equality above could also be used in the [[conversion rules]] for the various type formers, such as [[beta conversion]] or [[eta conversion]], where the equality is called **[[conversional equality]]** or **computational equality**. Computational equality is important because it is the equality used in [[inductive definitions]]. In [[Martin-Löf type theory]] and [[cubical type theory]], judgmental equality is used for computational equality, and in [[objective type theories]], typal equality is used for computational equality. 

## Meta-equalities

There are also equalities in [[type theory]] which are not internal to the type theory itself, but rather equalities in the metatheory. These include **syntactic equality** of expressions, as well as **[[alpha-equivalence]]** and **[[definitional equality]]** of syntactical expressions. When using [[de Bruijn indices]], alpha-equivalence is the same as syntactic equality, but when using [[variables]], alpha-equivalence is different from syntactic equality: rather alpha-equivalence is equality up to the renaming of [[bound variables]]. All type theories, like [[MLTT]], [[cubical type theory]], [[ZFC]], and [[ETCS]], have syntactic equality, alpha-equivalence, and definitional equality of syntactical expressions, including the type theories which lack [[judgmental equality]] like [[objective type theories]]. 

## Related concepts

* [[alpha-equivalence]]

* [[definition]], [[assignment]]

* [[identity type]], 

* [[identity of indiscernibles]]

* [[inequality]]

  * [[denial inequality]] 
  
  * [[apartness relation]]

  * [[antithesis interpretation]]

* [[judgmental isomorphism]]

* [[equivalence of types]]

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

[[!redirects equality in type theory]]
[[!redirects equalities in type theory]]

[[!redirects equality in dependent type theory]]
[[!redirects equalities in dependent type theory]]

[[!redirects syntactic equality]]
[[!redirects syntactically equal]]