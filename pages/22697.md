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

There should be a version of a [[loop (algebra)|loop]] that may be empty, similar to how a [[possibly empty group]] is a [[group]] that may be empty. That leads to the concept of a _possibly empty loop_, which is an example of [[centipede mathematics]].

## Definition

### As a quasigroup

A __possibly empty loop__ is a [[quasigroup]] $(G,(-)\cdot(-):G\times G\to G,(-)\backslash(-):G\times G\to G,(-)/(-):G\times G\to G)$ that satisfies the following laws: 

* $a \cdot (b \backslash b) = a$
* $(b \backslash b) \cdot a = a$
* $a \cdot (b / b) = a$
* $(b / b) \cdot a = a$

for all $a$ and $b$ in $G$.

### With multiplication and inverses

A __possibly empty loop__ is a set $G$ with a binary operation, __multiplication__ $(-)\cdot(-):G\times G\to G$, and two unary operations, the __left inverse__ ${^{-1}(-)}:G \to G$ and the __right inverse__ $(-)^{-1}:G \to G$, such that $G$ with multiplication and the left inverse is a left [[invertible magma]] and $G$ with multiplication and the right inverse is a right [[invertible magma]]. 

### With division only

A __possibly empty left loop__ is a [[magma]] $(G,(-)\backslash(-):G\times G\to G)$ such that:

  * For all $a$ and $b$ in $G$, $a\backslash a=b\backslash b$
  * For all $a$ in $G$, $(a\backslash (a\backslash a))\backslash (a\backslash a)=a$

For any element $a$ in a possibly empty left loop $G$, the element $a\backslash a$ is called a __right identity element__, and the element $a\backslash (a\backslash a)$ is called the __right inverse element__ of $a$. For all elements $a$ and $b$ in $G$, __left multiplication__ of $a$ and $b$ is defined as $(a\backslash (a\backslash a))\backslash b$. The multiplication operation is __associative__ if for all $a$, $b$, and $c$ in $G$, $(a\backslash b)\backslash c= b\backslash ((a\backslash (a\backslash a))\backslash c)$, __unital__ if for all $a$ in $G$, $a\backslash a = 1$, and __commutative__ if for all $a$ and $b$ in $G$, $(a\backslash (a\backslash a))\backslash b = (b\backslash (b\backslash b))\backslash a$. 

A __possibly empty right loop__ is a [[magma]] $(G,(-)/(-):G\times G\to G)$ such that:

  * For all $a$ and $b$ in $G$, $a/a=b/b$
  * For all $a$ in $G$, $(a/a)/((a/a)/a)=a$

For any element $a$ in a possibly empty right loop $G$, the element $a/a$ is called a __left identity element__, and the element $(a/a)/a$ is called the __left inverse element__ of $a$. For all elements $a$ and $b$, __right multiplication__ of $a$ and $b$ is defined as $a/((b/b)/b)$. The multiplication operation is __associative__ if for all $a$, $b$, and $c$ in $G$, $a/(b/c)=(a/((c/c)/c)/b$, __unital__ if for all $a$ in $G$, $a/a=1$, and __commutative__ if for all $a$ and $b$ in $G$, $a/((b/b)/b) = b/((a/a)/a)$. 

A __possibly empty loop__ is a set that  above such that the following are true:

* left and right identity elements are equal (i.e. $a/a = a \backslash a$) for all $a$ in $G$

* left and right multiplications are equal (i.e. $a/((b/b)/b) = (a\backslash (a\backslash a))\backslash b$) for all $a$ and $b$ in $G$. 

## Properties

* Every __possibly empty commutative loop__ is a [[commutative invertible magma]]. 

## Examples

* Every [[loop (algebra)|loop]] is a possibly empty loop. 

* Every possibly empty group is a possibly empty loop. 

* The empty possibly empty loop is an possibly empty loop that is not a loop. 

## Related concepts

* [[quasigroup]]

* [[invertible magma]], [[commutative invertible magma]]

* [[possibly empty group]] (associative version)

* [[loop (algebra)|loop]]

[[!redirects possibly empty abelian loop]]

[[!redirects possibly empty commutative loop]]