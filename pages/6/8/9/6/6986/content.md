
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc} 

## Idea

In [[type theory]] the _empty type_ is the [[type]] with no [[term]].

In a [[model]] by [[categorical semantics]] (cf. [[relation between type theory and category theory]]), this is an [[initial object]]. In [[set theory]], it is an [[empty set]]. In [[logic]], especially via the [[propositions as types]] interpretation of type theory, it represents [[falsehood]]; and constructing a [[term]] of an empty type represents a [[contradiction]]; thus [[functions]] into the empty type are regarded as the [[negation]] of their [[domain]] [[proposition]]. 

## Definition

Like all [[type formation|type constructors]] in [[type theory]], to characterize the empty type we must specify how to build it, how to [[term introduction|construct elements]] of it, how to [[term elimination|use such elements]], and the [[computation rules]].

To start with, since the empty type is not [[dependent type|dependent]], its [[type formation]] rule just says that it exists:

$$\frac{ }{\emptyset\colon Type}$$


### As a positive type

The empty type is most naturally presented as a [[positive type]], so that the [[term introduction|constructor rules]] are primary.  However, since the empty type is supposed to contain no elements, there *are* no constructor rules.


In fact one may understand the positively defined empty type as that *[[inductive type]]* which is given by *no constructors*. 

Therefore, in [[programming languages]] supporting a [[calculus of constructions]], such as *[[Coq]]*,  the empty type may be defined by the following [[syntax]] for [[inductive type|inductive]] [[data types]] using literally an [[empty set|empty]] [[string (computer science)|string]] of constructors on the right:

    Inductive empty : Type :=


#### Recursion principle
 {#RecursionPrinciple}

We start by considering the [[recursion principle]] of the empty type, hence its un-[[dependent type|dependent]] [[elimination rule]]:

The [[term elimination|eliminator rules]] are derived from the constructor rules in the usual way: to use a term $x \,\colon\, \varnothing$, given any $D \,\colon\, Type$,
it suffices to specify what should be done for all the ways that $x \,\colon\, \varnothing$ could have been constructed. But for the empty type there are [[empty set|no such]] ways and hence -- *assuming* $x \,\colon\, \varnothing$ -- we obtain a term of any type $D$ under no further conditions:

$$
  \frac{ 
    D \,\colon\, Type
  }
  {
    x \,\colon\, \varnothing 
    \;\; \vdash \;\; 
    ind_D(x) \,\colon\, D
  }
$$

Some ways to read this recursion principle:

* Understood as a statement in [[propositional logic]] (regarding *[[propositions as types]]*), this says that from a [[false]] assumption every [[proposition]] $D$ is [[implication|implied]] (*[[ex falso quodlibet]]*):

$$
  False \;\Rightarrow\; D
  \,.
$$

* Understood in the [[categorical semantics]] (cf. the [[relation between type theory and category theory]]) this translates to the first part of the characterization of an [[initial object]], namely the existence of [[morphisms]] into any [[codomain]] [[object]]:

$$
  \varnothing \xrightarrow{\exists} D
  \,.
$$

What is not manifest from the above rule is the (essential) uniqueness of these morphisms; on that point see also the [eta conversion rule](#EtaConversion), below.


#### Induction principle
 {#InductionPrinciple}

In [[dependent type theory]] the elimination rule of an [[inductive type]] is a dependent [[induction principle]] which involves any $\varnothing$-[[dependent type]]. 

{#InferenceRules}  Applying the general rules for [[inductive types]] to the case of no generators, one obtains the following [[inference rules]]:

**[[type formation rule]]:**

$$
  \frac{
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    \varnothing \,\colon\, Type
  }
$$

\linebreak


**[[term introduction rule]]:**

$$
\text{--- none ---}
$$

\linebreak

**[[term elimination rule]]:**

$$
  \frac{
    x \,\colon\, \varnothing
    \;\vdash\;\;
    D(x) \,:\, Type
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{(D)}
    \,\colon\,
    \underset{x \colon \varnothing}{\prod}
    D(x)
  }
$$

\linebreak

**[[computation rule]]:**

$$
\text{--- none ---}
$$

Notice that the induction principle entails the recursion principle [above](#RecursionPrinciple) (cf. e.g. [MHE, §2.6](#MHE)), as for any inductive type:

$$
  \frac{
  \frac{
    D \,\colon\, Type
  }
  {
  \big(
    (x \,\colon\, \varnothing)
    \mapsto
    D
  \big)
  \,\colon\,
  (\varnothing \to Type)
  }
  }{
  ind_{ (x \mapsto D) }
  \,\colon\,
  (x \colon \varnothing) \to D
  }
$$


#### Eta-conversion
 {#EtaConversion}

Notice that there is no [[beta-reduction]] rule for the positive empty type, since there are no constructors to compose with the eliminator.  

However, one may consider an [[eta-conversion]] rule, which says that for any term $e \,\colon\, \varnothing \;\;\vdash\;\; c \,\colon\, C$ in a context including a term of type $\emptyset$, we have

$$ 
  abort_C(e) 
  \;\;\;
    \leftrightarrow_\eta 
  \;\;\; 
  c
  \,.
$$

As with the [[eta-conversion|$\eta$-conversion]] rule for the negative presentation of the [[unit type]], this is ill-defined as a *reduction* (since we cannot determine $c$ from $abort_C(e)$), but makes sense as an *expansion*.
   .
Notice that [[Coq]] implements the [[beta reduction]] rule, but not the [[eta conversion]] (although eta equivalence is provable for the inductively defined [[identity types]], using the dependent eliminator mentioned above).


### As a negative type

As for binary [[sum types]], it is possible to present the empty type as a [[negative type]] as well, but only if we allow [[sequents]] with multiple conclusions.  This is common in [[sequent calculus]] presentations of [[classical logic]], but not as common in type theory and almost unheard of in [[dependent type theory]].

The two definitions are provably equivalent, but only using the [[contraction rule]] and the [[weakening rule]].  Thus, in [[linear logic]] they become distinct; the positive empty type is "zero" $\mathbf{0}$ and the negative one is "bottom" $\bot$.

### Using a type of propositions 

Suppose that the [[dependent type theory]] has a [[type of propositions]] $\mathrm{Prop}$, such as the one derived from a type universe $U$ - $\sum_{A:U} \mathrm{isProp}(A)$. Then the empty type is defined as the [[dependent function type]]

$$\emptyset \equiv \prod_{P:\mathrm{Prop}} P$$

whose elements are witnesses that all propositions are [[pointed types]] (and thus [[contractible types]]). 

By [[weak function extensionality]], the empty type is a proposition, and if it has an element, then every proposition in $\mathrm{Prop}$ has an element and is contractible. 

This definition makes sense because the empty type is equivalent to its [[propositional truncation]], and the [[propositional truncation]] is defined using $\mathrm{Prop}$ by 

$$[A] \equiv \prod_{P:\mathrm{Prop}} (A \to P) \to P$$

Substituting the empty type for $A$, we have 

$$\prod_{P:\mathrm{Prop}} (\emptyset \to P) \to P$$

By the recursion principle of the empty type, for every type $P$, the type $\emptyset \to P$ is contractible, and for every contractible type $I$, the type $I \to P$ is equivalent to $P$. Thus, we have equivalences of types

$$\emptyset \simeq \left(\prod_{P:\mathrm{Prop}} (\emptyset \to P) \to P\right) \simeq \left(\prod_{P:\mathrm{Prop}} P\right)$$

## Properties

#### The empty type as a univalent universe

The empty type can be represented as a univalent universe. We [[inductive definition|inductively define]] the type family $x:\mathbb{0} \vdash \mathrm{El}_\mathbb{0}(x) \; \mathrm{type}$ by defining 
$$\mathrm{El}_\mathbb{0}(*) \coloneqq \mathbb{0}$$
The extensionality principle for the unit type then is simply the [[univalence axiom]]:
$$\mathrm{ext}_\mathbb{0}:\prod_{x:\mathbb{0}} \prod_{y:\mathbb{0}} (x =_\mathbb{0} y) \simeq (\mathrm{El}_\mathbb{0}(x) \simeq \mathrm{El}_\mathbb{0}(y))$$
The empty type $\mathbb{0}$ represents the empty universe, the universe with no elements up to identification and thus no small types. Thus, the univalence axiom is trivially true. 

## Related concepts

[[!include empty objects -- contents]]

* [[falsehood]], [[ex falso quodlibet]]

* [[sum type]]

* [[unit type]], [[contractible type]]

## References

* {#UFP13} [[Univalent Foundations Project]], §1.7 and §A.28 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* [[Egbert Rijke]], Def. 3.2.1 in: *Inductive types and the universe*, Lecture 3 in: *[Introduction to Homotopy Type Theory 2018](https://www.andrew.cmu.edu/user/erijke/hott/)* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/inductive.pdf)&rbrack;

The definition of the empty type from the type of propositions and dependent product types can be found in:

* Madeleine Birchfield, *Constructing coproduct types and boolean types from universes*, MathOverflow ([web](https://mathoverflow.net/questions/457904/constructing-coproduct-types-and-boolean-types-from-universes))

In [[Agda]]: 

* {#MHE} [[Martín Hötzel Escardó]], [§2.6](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#emptytype) in *[Introduction to Univalent Foundations of Mathematics with Agda](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/)* (2019-2022)

See also: 

* Wikipedia, *[Principle of explosion](https://en.wikipedia.org/wiki/Principle_of_explosion)*

[[!redirects bottom type]]
[[!redirects bottom types]]

[[!redirects empty type]]
[[!redirects empty typpe]]
[[!redirects empty types]]
