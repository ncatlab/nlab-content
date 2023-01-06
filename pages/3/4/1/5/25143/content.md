
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[dependent type theory]], given types $A$ and $B$, a **multivalued partial function** or **partial multivalued function** from $A$ to $B$ is a type family $x:A \vdash P(x)$ with a function 

$$f:\left(\sum_{x:A} P(x)\right) \to B$$

or equivalently 

$$x:A, p:P(x) \vdash f(x, p):B$$

## Properties

In dependent type theory, [[correspondences]] are [[type families]] $x:A, y:B \vdash R(x, y)$, and [[spans]] are types $C$ with functions $x:C \vdash g_A(x):A$ and $x:C \vdash g_B(x):B$. Correspondences and spans are interdefinable with multivalued partial functions:

* From every span one could get a multivalued partial function by defining the type family $x:A \vdash P(x)$ as $P(x) \coloneqq \sum_{y:C} g(y) =_A x$ and the family of elements $x:A, p:P(x) \vdash f(x, p):B$ as $f(x, p) \coloneqq h(\pi_1(p))$. 

* From every multivalued partial function one could get a span by defining the type $C$ as $C \coloneqq \sum_{x:A} P(x)$ and the family of elements $x:C \vdash g(x):A$ as $g(x) \coloneqq \pi_1(x)$. 

* From every multivalued partial function one could get a correspondence by defining the type family $x:A, y:B \vdash R(x, y)$ as $R(x, y) \coloneqq \sum_{p:P(x)} f(x, p) =_B y$. 

* From every correspondence one could get a multivalued partial function by defining the type family $x:A \vdash P(x)$ as $P(x) \coloneqq \sum_{y:B} R(x, y)$, and the family of elements $x:A, p:P(x) \vdash h(x, p):B$ as $h(x, p) \coloneqq \pi_1(p)$ 

* From every span one could get a correspondence by defining the type family $x:A, y:B \vdash R(x, y)$ as $R(x, y) \coloneqq \sum_{z:C} (g(z) =_A x) \times (h(z) =_B y)$. 

* From every correspondence one could get a span by defining the type $C$ as $C \coloneqq \sum_{x:A} \sum_{y:B} R(x, y)$, the family of elements $z:C \vdash g(z):A$ as $g(z) \coloneqq \pi_1(z)$, and the function $z:C \vdash h(z):B$ as $h(z) \coloneqq \pi_1(\pi_2(z))$ 

## Examples

* A multivalued partial function for which there is an element $p(x):P(x)$ for all $x:A$ is a [[multivalued function]]. 

* A multivalued partial function for which the dependent type $P(x)$ is a [[mere proposition]] for all $x:A$ is a [[partial function]]. 

* A multivalued partial function for which the dependent type $P(x)$ is a [[contractible type]] for all $x:A$ is a [[total function]]. 

## Dependent multivalued partial functions

In the same way that there is a notion of [[dependent function]] in addition to (non-dependent) function in dependent type theory, there is also a notion of dependent multivalued partial functions in addition to non-dependent multivalued partial functions. 

In [[dependent type theory]], given a type $A$ and a type family $x:A \vdash B(x)$, a **multivalued partial function** or **partial multivalued function** from $A$ to $B$ is a type family $x:A \vdash P(x)$ with a dependent function 

$$f:\prod_{x:A} \left(\sum_{x:A} P(x)\right) \to B(x)$$

or equivalently 

$$x:A, p:P(x) \vdash f(x, p):B(x)$$

## See also

* [[correspondence]], [[correspondence type]]
* [[multivalued function]]
* [[partial function]]

[[!redirects multivalued partial function]]
[[!redirects multivalued partial functions]]
[[!redirects partial multivalued function]]
[[!redirects partial multivalued functions]]