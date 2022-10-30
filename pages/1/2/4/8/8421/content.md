
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The framework of _natural deduction_ is a formalization of _deduction_ applied in formal [[logic]] and [[type theory]]. It is effectively the [[syntax]] of type theory.

A system of natural deduction consists of a collection of 4-step rules:

1. **Type-formation rules**, which declare on which basis a new [[type]] of [[terms]] can be introduced;

1. **term-introduction rules**, which declare how that new type can be inhabited by [[terms]];

1. **term-elimination rules**, which declare how from a term of the new type one gets terms of other types;

1. **computation rules** which constrain the result of combining term introduction with term elimination.

The rules are used to manipulate [[judgements]], which are expression of the form

$$
  x : X \vdash a(x) : A(x)
$$

to be read as 

> In a context where we have terms $x$ of a type $X$, there are terms a(x) of [[types in context]] $A(x)$.

In particular there is assumed to be a [[type of types]] $Type$ such that the [[judgement]]

$$
  \vdash A : Type
$$

is to be read as just 

> There is a type $A$ (a term of type $Type$).

and more generally 

$$
  x : X \vdash A(x) : Type
$$

> For each $x \in X$ there is a type $A(x)$. Or: $A$ is a _[[type in context]]_ $X$, a _[[dependent type]] on $X$.

A _deduction_ in natural deduction, an _inference_, then consists of repeated application of the declared formation/introduction/elimination/computation rules to a given collection of such judgements. This kind of reasoning can be automated, and is so in [[programming languages]] such as [[Coq]].

If the types are declared to be [[h-propositions]], then (by an identification of concepts called "[[propositions as types]]" and "[[proofs as programs]]") a term $a : A$ is a [[proof]] of the [[proposition]] $A$ and a judgement of the form

$$
  x : X \vdash t : A
$$

is to be understood as saying

> Under the hypothesis that $X$ has a proof / is true, there is a proof $t$ of $A$.

In this case natural deduction gives the ordinary notion of deduction in [[logic]]. 

More generally, natural deduction is a formulation of [[computation]]. See at _[[computational trinitarianism]]_ for discusison of this unification of concepts.


## Examples of type formation/introduction/elemination/computation rules

### Conjunction and product types

The notion of [[product type]] formalizes the [[logic]] of [[conjunction]] (logical "and") and the formation of [[cartesian products]] in [[category theory]]

1. **Type formation**

   $$
     \frac{\vdash A : Type, \;\;\;\; B : Type}{\vdash A \times B : Type}
   $$
   
   "Given two types $A$ and $B$, there is a new type $A \times B$."

   "Given two propositions $A$ and $B$, there is a new proposition $A and B$,"

1. **Term introduction**

   $$
     \frac{
         \vdash A : Type, \;\;\; B : Type
      }{ 
          a : A,\; b : B \vdash (a,b) : A \times B
      }
   $$

   "Given two types $A$ and $B$ and whenever we are in a context where terms $a \in A$ and $b \in B$ are given, there is a term called $(a,b)$ of $A \times B$".

   "Given a proof $a$ of proposition $A$ and a proof $b$ of proposition $B$, there is a proof $(a,b)$ of proposition $A and B$."

1. **Term elimination**
  
   $$
     \frac{ 
        \vdash A : Type, \;\;\; B : Type
     }{ 
        q  : A \times B  \vdash p_1(q) : A 
     }
   $$

   $$
     \frac{ 
        \vdash A : Type, \;\;\; B : Type
     }{ 
        q  : A \times B \vdash  p_2(q) : A 
     }
   $$

   "Given types $A$ and $B$ and whenever we are in a context with a term $q$ of $A \times B$ given, there is a term $p_1(q)$ of type $A$ and a term $p_2(q)$ of type $B$."

   "Given a proof $q$ of $A and B$ there is a proof $p_1(q)$ of $A$ and a proof $p_2(q)$ of $B$."

1. **Computation**

   $p_1(a,b) = a$

   $p_2(a,b) = b$

   "If we use the term introduction rule to first build the term called $(a,b) \in A \times B$ from terms $a \in A$ and $b \in B$ and then use the term elimination rule to produce from that terms $p_1(a,b) \in A$ and $p_2(a,b) \in B$, then the result has to be equal to the original two terms. "

   "If $(a,b)$ is the proof of $A and B$ obtained from a proof $a$ of $A$ and a proof $b$ of $B$, then $p_1(a,b)$ and $p_2(a,b)$ are these original two proofs. "

### Disjunction and sum types

(...)

### Implication and and function types

(...)

### Existential quantification and dependent sum types

(...)

### Existential quantification and dependent product types

(...)

## Properties

### Relation to category theory

The 4-step rules of natural deduction are close to being specifications of [[universal constructions]] in [[category theory]]. In [[categorical semantics]] one considers categories which are such that their [[objetcs]] are regarded as [[types]] and their [[generalized elements]] as [[terms]], then the rules of natural deductions describe the poissble construction of [[morphisms]] in that category.

(...)

### Decidability

## References

The original source is

* [[Gerhard Gentzen]], _Untersuchungen uber das logische Schlie&#223;en_ (English translation _Investigations into Logical Deduction_ in Szabo) 1934/5. 

An introductory lecture is

* [[Per Martin-Löf]], _On the meaning of logical constants and the justifications of the logical laws_, leture series in Siena (1983) ([web](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf))

A good account is at

* Wikipedia, _[Natural deduction](http://en.wikipedia.org/wiki/Natural_deduction#Introduction_and_elimination)_

