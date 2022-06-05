
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 
 {#Idea}

In [[dependent type theory]], sometimes one could [[inductive definition|inductively define]] an equality type directly on an [[inductive type]], rather than using Martin-Loef's [[identity types]] using the j-rule. This equality type is called **observational equality**. 

## Examples
 {#Examples}

### Empty type
 {#EmptyType}

Observational equality for the [[empty type]] $\mathrm{Eq}_\mathbb{0}(x, y)$ is an indexed [[inductive type]] on the empty type $\mathbb{0}$ inductively defined by no constructors

### Unit type

Observational equality for the [[unit type]] $\mathrm{Eq}_\mathbb{1}(x, y)$ is an indexed inductive type on the unit type $\mathbb{1}$ inductively defined by the following constructor

$$\mathrm{eq}_*: \mathrm{Eq}_\mathbb{1}(*, *)$$

### Booleans

Observational equality for the [[booleans]] $\mathrm{Eq}_\mathbb{2}(x, y)$ is an indexed inductive type on the booleans $\mathbb{2}$ inductively defined by the following constructors

$$\mathrm{eq}_0: \mathrm{Eq}_\mathbb{2}(0, 0)$$
$$\mathrm{eq}_1: \mathrm{Eq}_\mathbb{2}(1, 1)$$

### Natural numbers

Observational equality for the [[natural numbers]] $\mathrm{Eq}_\mathbb{N}(x, y)$ is an indexed inductive type on the natural numbers $\mathbb{N}$ inductively defined by the following constructors

$$\mathrm{eq}_0: \mathrm{Eq}_\mathbb{N}(0, 0)$$
$$\mathrm{eq}_s: \prod_{x:\mathbb{N}} \prod_{y:\mathbb{N}} \mathrm{Eq}_\mathbb{N}(x, y) \to \mathrm{Eq}_\mathbb{N}(s(x), s(y))$$

## See also

* [[identity type]]

## References

* {#Rijke19} [[Egbert Rijke]], _[[Introduction to Homotopy Type Theory]]_ (2019)  ([web](http://www.andrew.cmu.edu/user/erijke/hott/), [pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [GitHub](https://github.com/EgbertRijke/HoTT-Intro)) 

* [Univalent mathematics in Agda](https://github.com/UniMath/agda-unimath)

[[!redirects observational equalities]]