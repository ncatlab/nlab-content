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

There should be a non-associative version of a [[possibly empty group]], similar to how a [[loop (algebra)|loop]] is a non-associative [[group]]. That leads to the concept of a _possibly empty loop_, which is an example of [[centipede mathematics]].

## Definition

### With division only

A __possibly empty left loop__ is a [[magma]] $(G,(-)\backslash(-):G\times G\to G)$ such that:

  * For all $a$ and $b$ in $G$, $a\backslash a=b\backslash b$
  * For all $a$ in $G$, $(a\backslash (a\backslash a))\backslash (a\backslash a)=a$

For any element $a$ in a possibly empty left loop $G$, the element $a\backslash a$ is called a __right identity element__, and the element $a\backslash (a\backslash a)$ is called the __right inverse element__ of $a$. For all elements $a$ and $b$ in $G$, __left multiplication__ of $a$ and $b$ is defined as $(a\backslash (a\backslash a))\backslash b$. 

A __possibly empty right loop__ is a [[magma]] $(G,(-)/(-):G\times G\to G)$ such that:

  * For all $a$ and $b$ in $G$, $a/a=b/b$
  * For all $a$ in $G$, $(a/a)/((a/a)/a)=a$

For any element $a$ in a possibly empty right loop $G$, the element $a/a$ is called a __left identity element__, and the element $(a/a)/a$ is called the __left inverse element__ of $a$. For all elements $a$ and $b$, __right multiplication__ of $a$ and $b$ is defined as $a/((b/b)/b)$. 

A __possibly empty loop__ is a possibly empty left and right loop as defined above such that the following are true:

* left and right identity elements are equal (i.e. $a/a = a \backslash a$) for all $a$ in $G$

* left and right multiplications are equal (i.e. $a/((b/b)/b) = (a\backslash (a\backslash a))\backslash b$) for all $a$ and $b$ in $G$. 

### With multiplication and inverses

A __possibly empty left loop__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ and a unary operation called the __left inverse__ $^{-1}(-):G \to G$ such that 

* ${^{-1}a} \cdot a = {^{-1}b} \cdot b$
* $b \cdot ({^{-1}b} \cdot a) = a$ 
* ${^{-1}b} \cdot (b \cdot a) = a$

for all $a,b \in G$. For any element $a$ in a possibly empty left loop $G$, the element ${^{-1}a} \cdot a$ is called a __right identity element__, and for all elements $a$ and $b$ in $G$, __left division__ is defined as $b \backslash a = {^{-1}}b \cdot a$.

A __possibly empty right loop__ is a [[magma]] $G,(-)\cdot(-):G\times G\to G)$ and a unary operation called the __right inverse__ $(-)^{-1}:G \to G$ such that 

* $a \cdot a^{-1} = b \cdot b^{-1}$
* $(a \cdot b^{-1}) \cdot b = a$ 
* $(a \cdot b) \cdot b^{-1} = a$

for all $a,b \in G$. For any element $a$ in a possibly empty right loop $G$, the element $a \cdot a^{-1}$ is called a __right identity element__, and for all elements $a$ and $b$ in $G$, __left division__ is defined as $a / b = a \cdot b^{-1}$.

A __possibly empty two-sided loop__ or just __possibly empty loop__ is a magma $(G,(-)\cdot(-):G\times G\to G)$ that is both a possibly empty left loop and a possibly empty right loop such that left and right identity elements are the same: $a \cdot a^{-1} = {^{-1}a} \cdot a$ for all $a$ in $G$. 

## Examples

* Every [[loop (algebra)|loop]] is a possibly empty loop. 

* Every possibly empty group is a possibly empty loop. 

* The empty possibly empty loop is an possibly empty loop that is not a loop. 

## Related concepts

* [[possibly empty group]] (associative version)

* [[possibly empty abelian loop]] (commutative version)

* [[loop (algebra)|loop]]