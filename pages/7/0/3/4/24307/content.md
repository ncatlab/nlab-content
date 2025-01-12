
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

## Idea ##

Similar to how [[rational vector spaces]] could be defined without using the [[rational numbers]], as a [[torsion-free]] [[divisible group]], there is a definition of an [[associative]] [[unital]] rational [[associative algebras|algebra]] without using the rational numbers. 

## Definition ##

By the [[universal property]] of the [[ring]] of [[integers]], every ring $R$ has a [[ring homomorphism]] $h:\mathbb{Z} \to R$ from the integers to $R$ which lands in the [[center]] of $R$, and there is an injection $i:\mathbb{Z}_+ \to \mathbb{Z}$ from the positive integers to the integers. 

A ring $R$ is a **rational algebra** or **$\mathbb{Q}$-algebra** if there is a function $j:\mathbb{Z}_+ \to R$ such that for all positive integers $a\in\mathbb{Z}_+$ and elements $b \in R$, $h(i(a)) \cdot j(a) = 1$ and  $j(a) \cdot b = b \cdot j(a)$. 

The [[rational numbers]] $\mathbb{Q}$ are the initial $\mathbb{Q}$-algebra. As a result, every $\mathbb{Q}$-algebra $R$ has a [[ring homomorphism]] $h:\mathbb{Q}\to R$, which corresponds to the definition of $\mathbb{Q}$-algebra in terms of ring homomorphisms. 

## Examples ##

* Every [[ordered field]] is a $\mathbb{Q}$-algebra. 

## See also ##

* [[rational vector space]]
* [[rational numbers]]
* [[ordered field]]
* [[associative unital algebra]]

[[!redirects Q-algebra]]
[[!redirects Q-algebras]]
[[!redirects rational algebra]]
[[!redirects rational algebras]]