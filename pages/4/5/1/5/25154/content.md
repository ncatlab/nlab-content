
\tableofcontents

## Definition

### In set theory

A __sequential net__ is a [[multi-valued function]] from $\mathbb{N}$ (or a [[decidable subset|decidable]] [[subset]] thereof) to $X$, that is a [[span]] $\mathbb{N} \leftarrow A \rightarrow X$ where the map $A \to \mathbb{N}$ is a [[surjection]] (or has a decidable range). 

### In type theory

A **sequential net** in a type $B$ can be defined as 

* a [[span]] with domain of the [[natural numbers]], whose function into the natural numbers is a surjection, which consists of
  * a type $C$
  * a family of elements $z:C \vdash g(z):\mathbb{N}$
  * a family of elements $z:C \vdash h(z):B$
  * a family of witnesses $x:\mathbb{N} \vdash \mathrm{isInhab}(x):\left[\sum_{z:B} g(z) =_\mathbb{N} x\right]$ that each dependent type $\sum_{z:B} g(z) =_\mathbb{N} x$ is [[inhabited]] for all natural numbers $x:\mathbb{N}$
* a [[multivalued function]] with domain of the [[natural numbers]], which consists of 
  * a type family $x:\mathbb{N} \vdash P(x)$ 
  * a family of elements $x:\mathbb{N}, p:P(x) \vdash f(x, p):B$ 
  * a family of witnesses $x:\mathbb{N} \vdash \mathrm{isInhab}(x):\left[P(x)\right]$ that each dependent type $P(x)$ is [[inhabited]] for all natural numbers $x:\mathbb{N}$
* a total [[correspondence]] with domain of the [[natural numbers]], consisting of 
  * a type family $x:\mathbb{N}, y:B \vdash R(x, y)$
  * a family of witnesses $x:\mathbb{N} \vdash \mathrm{isInhab}(x):\left[\sum_{y:B} R(x, y)\right]$ that each dependent type $\sum_{y:B} R(x, y)$ is [[inhabited]] for all natural numbers $x:\mathbb{N}$

## Properties

Given a sequential net $A$, $A$ inherits the structure of a directed set via $A \to \mathbb{N}$, so that $A \to X$ is a net. In the context of [[weak countable choice]], as a net, every sequential net is equivalent (in the sense of corresponding to the same [[filter]]) to some sequence. 

Without [[weak countable choice]], many of the usual properties of [[metric spaces]] and other [[sequential spaces]] fail, but they continue to hold using sequential nets in the place of sequences. For example, every (located Dedekind) [[real number]] may be represented as a sequential Cauchy net, even when they might not all be represented as Cauchy sequences; see [[Cauchy real number]].

## Dependent sequential nets

A dependent sequential net is like a sequential net, but where we generalize from a single type $B$ to a family of types $x:\mathbb{N} \vdash B(x)$ indexed by the natural numbers. 

A **dependent sequential net** in a type family $x:\mathbb{N} \vdash B(x)$ can be defined as 

* a dependent multivalued function with domain of the [[natural numbers]], which consists of 
  * a type family $x:\mathbb{N} \vdash P(x)$ 
  * a family of elements $x:\mathbb{N}, p:P(x) \vdash f(x, p):B(x)$ 
  * a family of witnesses $x:\mathbb{N} \vdash \mathrm{isInhab}(x):\left[P(x)\right]$ that each dependent type $P(x)$ is [[inhabited]] for all natural numbers $x:\mathbb{N}$
* a total [[dependent correspondence]] with domain of the [[natural numbers]], consisting of 
  * a type family $x:\mathbb{N}, y:B(x) \vdash R(x, y)$
  * a family of witnesses $x:\mathbb{N} \vdash \mathrm{isInhab}(x):\left[\sum_{y:B(x)} R(x, y)\right]$ that each dependent type $\sum_{y:B(x)} R(x, y)$ is [[inhabited]] for all natural numbers $x:\mathbb{N}$


## See also

* [[sequence]], [[dependent sequence]]

* [[net]]

* [[weak countable choice]], [[countable choice]], [[dependent choice]]

[[!redirects sequential net]]
[[!redirects sequential nets]]

[[!redirects dependent sequential net]]
[[!redirects dependent sequential nets]]