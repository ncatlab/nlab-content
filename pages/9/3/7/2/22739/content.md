+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A quasigroup with a two-sided [[inverse]]

## Definition
An __invertible quasigroup__ is a [[quasigroup]] $(G,\cdot,\backslash,/)$ with a unary operation $(-)^{-1}:G \to G$ called the __[[inverse]]__ such that

* $a \cdot (b^{-1} \cdot b) = a$
* $(b^{-1} \cdot b) \cdot a = a$
* $a \cdot (b \cdot b^{-1}) = a$
* $(b \cdot b^{-1}) \cdot a = a$

for all $a,b \in G$. 


### Without division

An __invertible quasigroup__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __[[inverse]]__ such that

* $a \cdot (b^{-1} \cdot b) = a$
* $(b^{-1} \cdot b) \cdot a = a$
* $a \cdot (b \cdot b^{-1}) = a$
* $(b \cdot b^{-1}) \cdot a = a$

and

* $b \cdot (b^{-1} \cdot a) = a$ 
* $b^{-1} \cdot (b \cdot a) = a$
* $(a \cdot b) \cdot b^{-1} = a$
* $(a \cdot b^{-1}) \cdot b = a$ 

for all $a,b \in G$. 

## Examples

* Every group is an invertible quasigroup. 

* Every [[associative quasigroup]] and [[nonassociative group]] is an invertible quasigroup. 

## Related concepts

* [[quasigroup]] (noninvertible version)

* [[nonassociative group]] (unital version)

* [[commutative invertible quasigroup]] (commutative version)

* [[associative quasigroup]] (associative version)

* [[invertible magma]] (nondivisible version)

* [[Malcev variety]]

* [[centipede mathematics]]

[[!redirects invertible magmas]]