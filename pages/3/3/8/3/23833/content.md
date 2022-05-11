+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Group theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition 

An **inner product abelian group** is an [[abelian group]] $G$ with a binary function $q: G \times G \to \mathbb{Z}$ called the *inner product* such that the following properties hold:

* for all $a \in G$, $ \langle 0, a \rangle = 0 $ and $ \langle a, 0 \rangle = 0 $;
* for all $a, b, c \in G$, $ \langle a + b, c \rangle = \langle a, c \rangle + \langle b, c \rangle $ and $ \langle a, b + c \rangle = \langle a, b \rangle + \langle a, c \rangle $
* for all $a, b \in G$ and $ \langle a, b \rangle = \overline{\langle b, a \rangle}$.

where $\overline{(-)}:\mathbb{Z} \to \mathbb{Z}$ is an [[involution]] on the integers. 

Typically, the inner product is defined with another axiom

* for all $a, b \in G$ and $c \in \mathbb{Z}$, $ \langle c a, b \rangle = c \langle a, b \rangle $ and 
$\langle a, \overline{c} b \rangle = \langle a, b \rangle \overline{c}$

but this is provable for any binary function which is left and right distributive over the abelian group operations. 

## Properties

* Every inner product abelian group is a [[quadratic abelian group]] with $q(x) \coloneqq \langle x, x \rangle$. 

## See also

* [[inner product]]

* [[abelian group]]

* [[ring]]

* [[quadratic abelian group]]

* [[Clifford ring]]

[[!redirects inner product abelian groups]]