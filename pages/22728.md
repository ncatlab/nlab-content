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

A non-associative [[group]], or a [[loop (algebra)|loop]] whose left and right [[inverses]] are the same. 

## Definition

### With division only

A __nonassociative left group__ or __left loop__ is a [[pointed]] [[magma]] $(G,(-)\backslash(-):G \times G \to G,1)$ such that:

  * For all $a$ in $G$, $a\backslash a=1$
  * For all $a$ in $G$, $(a\backslash 1)\backslash 1=a$

For any element $a$ in a nonassociative left group $G$, the element $a\backslash 1$ is called the __right inverse element__ of $a$. For all elements $a$ and $b$ in $G$, __left multiplication__ of $a$ and $b$ is defined as $(a\backslash 1)\backslash b$. 

A __nonassociative right group__ or __right loop__ is a [[pointed]] [[magma]] $(G,(-)/(-):G \times G \to G,1)$ such that:

  * For all $a$ in $G$, $a/a=1$
  * For all $a$ in $G$, $1/(1/a)=a$

For any element $a$ in a nonassociative right group $G$, element $1/a$ is called the __left inverse element__ of $a$. For all elements $a$ and $b$, __right multiplication__ of $a$ and $b$ is defined as $a/(1/b)$. 

A __nonassociative group__ is a nonassociative left and right group as defined above such that the following are true:

* left and right inverse elements are equal (i.e. $1/a = a\backslash 1$) for all $a$ in $G$

* left and right multiplications are equal (i.e. $a/(1/b) = (a\backslash 1)\backslash b$) for all $a$ and $b$ in $G$. 

### With multiplication and inverses

A __nonassociative left group__ or a __left loop__ is a [[unital magma]] $(G,(-)\cdot(-):G\times G\to G),1:G$ and a unary operation called the __left inverse__ $^{-1}(-):G \to G$ such that 

* ${^{-1}a} \cdot a = 1$
* $b \cdot ({^{-1}b} \cdot a) = a$ 
* ${^{-1}b} \cdot (b \cdot a) = a$

for all $a,b \in G$. For any element $a$ in a nonassociative left group $G$, the element ${^{-1}a} \cdot a$ is called a __right identity element__, and for all elements $a$ and $b$ in $G$, __left division__ is defined as $b \backslash a = {^{-1}}b \cdot a$.

A __nonassociative right group__ or a __right loop__ is a [[unital magma]] $G,(-)\cdot(-):G\times G\to G),1:G$ and a unary operation called the __right inverse__ $(-)^{-1}:G \to G$ such that 

* $a \cdot a^{-1} = 1$
* $(a \cdot b^{-1}) \cdot b = a$ 
* $(a \cdot b) \cdot b^{-1} = a$

for all $a,b \in G$. For any element $a$ in a nonassociative right group $G$, the element $a \cdot a^{-1}$ is called a __right identity element__, and for all elements $a$ and $b$ in $G$, __left division__ is defined as $a / b = a \cdot b^{-1}$.

A __nonassociative group__ is a unital magma $(G,(-)\cdot(-):G\times G\to G,1:G)$ that is both a nonassociative left group and a nonassociative right group such that left and right inverse elements are the same: $a^{-1} = {^{-1}a}$ for all $a$ in $G$.

## Examples

* Every group is a nonassociative group. 

## Related concepts

* [[group]]

* [[unital magma]]

* [[loop (algebra)|loop]]

* [[centipede mathematics]]