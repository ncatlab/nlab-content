
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]


=--
=--
=--


*Disambiguation: For axiom K as a principle of [[type theory]], see [[axiom K (type theory)]]*

# Contents
* table of contents
{: toc}

## Idea

In [[modal logic]], axiom K, named after [[Saul Kripke]], is a basic principle which almost all versions of propositional modal logic satisfy

$$K \colon \Box(p \to q) \to \Box p \to \Box q.$$


## Developments

It is possible to consider a variant in [[dependent type theory]] ([Spitters](#Spitters))

$$
Dependent\; K \colon \Box \Pi_{y:A} B(y) \to \Pi_{x: \Box A} \Box B [open\; x/y].
$$

## Related concepts

* [[K modal logic]]

## References

* {#Spitters} [[Bas Spitters]] et al., _Modal Dependent Type Theory and Dependent Right Adjoints_, ([slides](http://www.cs.au.dk/~spitters/floc.pdf))

Axiom K is discussed in Example 6.1.7 of:

* [[Daniel Gratzer]], *Syntax and semantics of modal type theory* ([pdf](https://jozefg.github.io/papers/phd-thesis.pdf))