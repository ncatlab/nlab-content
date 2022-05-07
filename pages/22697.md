+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There should be a version of a [[loop (algebra)|loop]] that may be empty, similar to how an [[associative quasigroup]] is a [[group]] that may be empty. That leads to the concept of a _possibly empty loop_, which is an example of [[centipede mathematics]].

## Definition

### As a quasigroup

A __possibly empty loop__ is a [[quasigroup]] $(G,(-)\cdot(-):G\times G\to G,(-)\backslash(-):G\times G\to G,(-)/(-):G\times G\to G)$ that satisfies the following laws: 

* $a \cdot (b \backslash b) = a$
* $(b \backslash b) \cdot a = a$
* $a \cdot (b / b) = a$
* $(b / b) \cdot a = a$

for all $a$ and $b$ in $G$.

### With division only

A __possibly empty left loop__ is a set $G$ with a binary operation $(-)\backslash(-):G\times G\to G$, such that:

  * For all $a$ and $b$ in $G$, $a\backslash a=b\backslash b$
  * For all $a$ in $G$, $(a\backslash (a\backslash a))\backslash (a\backslash a)=a$

For any element $a$ in $G$, the element $a\backslash a$ is called a __right identity element__, and the element $a\backslash (a\backslash a)$ is called the __right inverse element__ of $a$. For all elements $a$ and $b$ in $G$, __left multiplication__ of $a$ and $b$ is defined as $(a\backslash (a\backslash a))\backslash b$. 

A __right quotient__ on a set $G$ is a binary operation $(-)/(-):G\times G\to G$ such that:

  * For all $a$ and $b$ in $G$, $a/a=b/b$
  * For all $a$ in $G$, $(a/a)/((a/a)/a)=a$

For any element $a$ in $G$, the element $a/a$ is called a __left identity element__, and the element $(a/a)/a$ is called the __left inverse element__ of $a$. For all elements $a$ and $b$, __right multiplication__ of $a$ and $b$ is defined as $a/((b/b)/b)$.

A __possibly empty loop__ is a possibly empty left and right loop as defined above such that the following are true:

* left and right identity elements are equal (i.e. $a/a = a \backslash a$) for all $a$ in $G$

* left and right multiplications are equal (i.e. $a/((b/b)/b) = (a\backslash (a\backslash a))\backslash b$) for all $a$ and $b$ in $G$.

## Properties

* Every __possibly empty commutative loop__ is a [[commutative invertible magma]]. 

* Every __possibly empty associative loop__ is a [[associative quasigroup]]. 

## Examples

* Every [[loop (algebra)|loop]] is a possibly empty loop. 

* Every [[associative quasigroup]] is a possibly empty loop. 

* The empty quasigroup is a possibly empty loop. 

## Related concepts

* [[quasigroup]], [[associative quasigroup]]

* [[loop (algebra)|loop]]

[[!redirects possibly empty abelian loop]]

[[!redirects possibly empty commutative loop]]