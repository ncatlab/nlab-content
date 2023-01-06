
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

In [[dependent type theory]], given types $A$ and $B$, a **multivalued partial function** or **partial multivalued function** between $A$ and $B$ is a type family $x:A \vdash P(x)$ with a function 

$$f:\left(\sum_{x:A} P(x)\right) \to B$$

or equivalently 

$$x:A, p:P(x) \vdash f(x, p):B$$

## Properties

In dependent type theory, [[correspondences]] are [[type families]] $x:A, y:B \vdash R(x, y)$, and [[spans]] are types $C$ with functions $x:C \vdash g_A(x):A$ and $x:C \vdash g_B(x):B$. Correspondences and spans are interdefinable with multivalued partial functions:

* From every span one could get a multivalued partial function by defining the type family $x:A \vdash P(x)$ as $P(x) \coloneqq \sum_{y:C} g(y) =_A x$ and the function $f:\left(\sum_{x:A} P(x)\right) \to B$ as $f(z) \coloneqq h(\pi_1(\pi_2(\pi_1(z))(z)))$. 

* From every multivalued partial function one could get a span by defining the type $C$ as $C \coloneqq \sum_{x:A} P(x)$ and the function $g:C \to A$ as $g(x) \coloneqq \pi_1(x)$. 

* From every multivalued partial function one could get a correspondence by defining the type family $x:A, y:B \vdash R(x, y)$ as $R(x, y) \coloneqq \sum_{p:P(x)} f(x, p) =_B y$. 

* From every correspondence one could get a multivalued partial function by defining the type family $x:A \vdash P(x)$ as $P(x) \coloneqq \sum_{y:B} R(x, y)$, and the function $h:\left(\sum_{x:A} P(x)\right) \to B$ as $h(z) \coloneqq \pi_1(\pi_2(z))$ 

* From every span one could get a correspondence by defining the type family $x:A, y:B \vdash R(x, y)$ as $R(x, y) \coloneqq \sum_{z:C} (g(z) =_A x) \times (h(z) =_B y)$. 

* From every correspondence one could get a span by defining the type $C$ as $C \coloneqq \sum_{x:A} \sum_{y:B} R(x, y)$, the function $g:C \to A$ as $g(z) \coloneqq \pi_1(z)$, and the function $h:C \to B$ as $h(z) \coloneqq \pi_1(\pi_2(z))$ 

## Examples

* A multivalued partial function for which there is an element $p(x):P(x)$ for all $x:A$ is a [[multivalued function]]. 

* A multivalued partial function for which the dependent type $P(x)$ is a [[mere proposition]] for all $x:A$ is a [[partial function]]. 

* A multivalued partial function for which the dependent type $P(x)$ is a [[contractible type]] for all $x:A$ is a [[total function]]. 

## See also

* [[correspondence]], [[correspondence type]]
* [[multivalued function]]
* [[partial function]]

[[!redirects multivalued partial function]]
[[!redirects multivalued partial functions]]
[[!redirects partial multivalued function]]
[[!redirects partial multivalued functions]]