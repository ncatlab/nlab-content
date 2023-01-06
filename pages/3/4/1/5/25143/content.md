
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

Correspondences are [[type families]] $x:A, y:B \vdash R(x, y)$. From every correspondence, one could derive the [[multivalued partial function]] 
$$x:A, p:\sum_{y:B} R(x, y) \vdash f(x, p):B$$
and for every type family $x:A \vdash P(x)$ and every [[multivalued partial function]] $x:A, p:P(x) \vdash f(x, p):B$, one could define the [[correspondence]] $x:A, y:B \vdash R(x, y)$ as
$$R(x, y) \coloneqq \sum_{p:P(x)} f(x, p) =_B y$$

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