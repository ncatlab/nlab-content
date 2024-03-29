
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
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

## Idea ##

In [[type theory]], under a *pure type system* one understand and explicitly typed [[lambda calculus]]
using [[dependent product]] as the type of lambda expressions:
the basic idea is that
$$\Gamma, x:A \vdash b:B$$
implies
$$\Gamma \vdash (\lambda x:A . b) : (\prod x:A . B).$$

In other words a _pure type system_ is

1. a system of [[natural deduction]];

1. for [[dependent types]];

1. and with (only) the [[dependent product type]] [[type formation|formation]] rule specified.


## Definition ##

A _pure type system_ is defined by

* a set $S$ of _sorts_, all of which are constants,
* a set $A$ of _axioms_ of the form $c : s$ with $c$ a constant and $s$ a sort,
* a set $R \hookrightarrow S \times S \times S$ of _rules_: triples $(s_{1}, s_{2}, s_{3}) $ of sorts.

  Rules $(s_{1}, s_{2}, s_{2})$ are abbreviated as $(s_{1}, s_{2})$.

+-- {: .num_remark }
###### Remark

These _rules_ will appear in the [[type formation]] rule for [[dependent product types]] below. They will say that for a type of sort $s_2$ [[dependent type|depending]] on a type of sort $s_1$ its dependent product is a type of sort $s_3$.

=--

+-- {: .num_remark }
###### Remark

In fact all rules $(s_{1}, s_{2}, s_{2})$ appearing in the following have $s_2 = s_3$. So we can just as well regard $R$ as a binary relation $R \hookrightarrow S\times S$ (rather than a ternary one).

=--

From the above input data we derive the following 

1. The **terms** of a pure type system are the following (recursive definition):
   * variables and constants
   * $(\lambda x : A . B)$ (abstraction)
   * $(\prod x : A . B)$ (product)
   * $A B$ (application)

   Here $x$ is a variable and $A$, $B$ are terms. The operators $\lambda$ and $\prod$ bind the variable $x$.

1. The **typing of terms** is inductively defined by the following rules.

   A typing is of the form 

   $$
     x_{1} : A_{1}, \dots, x_{n} : A_{n} \vdash A : B
   $$ 
 
   meaning that the types of the variables declared on the left induces the term $A$ has type $B$. Note that types are also terms.

   The order of variable  declarations is significant:
the declaration $x_{i} : A_{i}$ may depend on declarations to its left.

The [[natural deduction]] rules are defined to be the following, for all $s \in S$ and where $x$ ranges over the set of variables.

name          | rule                                                                                                                      | condition                         |
--------------|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
(axioms)      | $\vdash c : s$                                                                                                     | if $(c : s)$ is an axiom;         |
(start)       | $\frac{\Gamma \vdash A:s}{\Gamma, x : A \vdash x : A}$                                                             | if $x \notin \Gamma$              |
(weakening)   | $\frac{\Gamma \vdash A:B; \quad \Gamma \vdash C:s}{\Gamma, x : C \vdash A : B}$                                           | if $x \notin \Gamma$              |
(product)     | $\frac{\Gamma \vdash A : s_{1}; \quad \Gamma, x:A \vdash B : s_{2}}{\Gamma \vdash (\prod x:A . B) : s_{3}}$                | if $(s_{1}, s_{2}, s_{3}) \in R$; |
(application) | $\frac{\Gamma \vdash F : (\prod x:A . B); \quad \Gamma \vdash a : A}{\Gamma \vdash Fa : B [x := a]}$                      |                                   |
(abstraction) | $\frac{\Gamma, x:A \vdash b : B; \quad \Gamma \vdash (\prod x:A . B) : s}{\Gamma \vdash (\lambda x:A.b) : (\prod x:A.B)}$ |                                   |
(conversion)  | $\frac{\Gamma \vdash A : B; \quad \Gamma \vdash B' : s; \quad B =_{\beta} B'}{\Gamma \vdash A : B'}$                                   |                                   |


## Examples ##

### Strongly normalizing systems ###

#### Intuitionistic (higher-order) logic ####

#### Lambda cube #### 

The _lambda cube_ ([Barendregt 91](#Barendregt91)) consists of eight systems arranged in a cube. The most expressive is given by the following choice of sorts, axioms and rules:

| symbol | actual value
|--------|-------------
| $S = $ | $\{\ast, \square\}$
| $A =$  | $\{(\ast : \square)\}$
| $R =$  | $\{(\ast, \ast), (\ast, \square), (\square, \ast), (\square, \square)\}$ 

(Here $\{\ast, \Box\}$ denotes the 2-element set, see [Barendregt 91, 2.1](#Barendregt91))

The other systems omit some of the last three rules.
Some specific systems are the following:

name | $(\ast, \ast)$ | $(\ast, \square)$ | $(\square, \ast)$ | $(\square, \square)$ |
-----|----------------|-------------------|-------------------|-----------------------|
$\lambda\rightarrow$ [[simply typed lambda calculus]] | yes |   |   |   |
${\lambda}P$ [[logical framework]] | yes | yes |   |   |
$\lambda2$ [[System F]] | yes |   | yes |   |
$\lambda\underline{\omega}$ | yes |   |   | yes |
${\lambda}C$ [[calculus of constructions]] | yes | yes | yes | yes |

#### Calculus of constructions {#CalculusOfConstructions}

For instance for the [[calculus of constructions]] we have 

* $* =$ [[Prop]], the _[[type of propositions]]_

* $\Box = $ [[Type]], the _[[type of types]]_.

The single axiom $* \colon \Box$ hence says that $Prop \colon Type$, hence that [[Prop]] is a [[type]]. 

The rules express the usual rule for [[dependent product type]]: 

* a dependent product over a generic [[dependent type]] is itself some type;

* but the dependent product of a dependent [[proposition]] is itself a proposition, namely the [[universal quantifier|universal quantification]].
 

### Inconsistent systems ### 

The most permissive pure type system:

| symbol | actual value
|--------|-------------
| $S = $ | $\{\ast\}$
| $A = $ | $\{(\ast : \ast)\}$
| $R = $ | $\{(\ast, \ast)\}$

But there is an example with even non-circular system of axioms (System $\mathsf{U}^-$):

| symbol | actual value
|--------|-------------
| $S =$  | $\{ \ast, \square, \triangle\}$
| $A =$  | $\{(\ast : \square), (\square : \triangle)\}$
| $R = $ | $\{(\ast, \ast), (\square, \ast), (\square, \square), (\triangle, \square)\}$

## Related concepts

* [[simple type theory]]

* Pure type systems can be augmented with a *cumulativity* relation between sorts, so that if $s_1 \preceq s_2$, then any type in $s_1$ is also in $s_2$; see [Barras-Gregoire](#BG05).

* The _[[calculus of inductive constructions]]_ can be formulated as a particular pure type system (with a hierarchy of [[type of types]]) augmented by rules for introducing [[inductive types]].

## References ##

* {#Barendregt91} Henk Barendregt, _Introduction to generalized type systems_, J. Funct. Program. 1(2), 1991 ([pdf](http://patryshev.com/books/barendregt.pdf))

* Henk Barendregt (Catholic University Nijmegen), _[[Lambda calculi with types]]_, To appear in [[Samson Abramsky]], D.M. Gabbay and T.S.E. Maibaum
(eds.) _Handbook of Logic in Computer Science_, Volume II,
Oxford University Press. ([preprint pdf](http://ttic.uchicago.edu/~dreyer/course/papers/barendregt.pdf))

Survey includes

* Frade, _Calculus of inductive constructions_ ([pdf](http://www4.di.uminho.pt/~mjf/pub/SFV-CIC-2up.pdf))

* {#Cody15} [[Cody Roux]], _Pure type systems: Dependents when you need them_, talk at Boston Haskell Meetup 2015 ([slides](http://de.slideshare.net/imalsogreg/cody-roux-pure-type-systems-boston-haskell-meetup),[video](https://www.youtube.com/watch?v=ZGqKsalJi4s))

A generalization to cumulativity can be found in

* Bruno Barras and Benjamin Gregoire, *On the role of type decorations in the Calculus of Inductive Constructions*, Lecture Notes in Computer Science Volume 3634, 2005, pp 151-166, [PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.61.2666&rep=rep1&type=pdf)
 {#BG05}

[[!redirects pure type systems]]