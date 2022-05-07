+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
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

A __decimal rational number__ or __decimal fraction__ is a [[rational number]] $r \in \mathbb{Q}$ such that the [[decimal number|decimal]] expansion of $r$ has finitely many digits. 

## Definition

### As a subset of the rational numbers

A __decimal rational number__ or __decimal fraction__ is a [[rational number]] $r \in \mathbb{Q}$ such that there exists $n \in \mathbb{N}$ and $a \in \mathbb{Z}$ such that $r = \frac{a}{10^n}$.

### As the localisation of the integers at 10

The [[commutative ring]] of decimal rational numbers $\mathbb{Z}[1/10]$ is the [[localization of a commutative ring|localization]] of the [[integers]] $\mathbb{Z}$ [[localisation of a commutative ring away from an element|away from]] $10$.

### As an initial object of a category

For lack of a better name, let us define a *decimal fraction algebra* to be a set $A$ with a function $\iota \in \mathbb{Z} \times \mathbb{N} \to A$ with domain the Cartesian product $\mathbb{Z} \times \mathbb{N}$ and codomain $A$, such that 

$$\forall a \in \mathbb{Z}. \forall b \in \mathbb{N}. \forall c \in \mathbb{Z}. \forall d \in \mathbb{N}. (a \cdot 10^d = c \cdot 10^b) \implies (\iota(a, b) = \iota(c, d))$$

A *decimal fraction algebra homomorphism* between two decimal fraction algebras $A$ and $B$ is a function $f \in B^A$ such that 

$$\forall a \in \mathbb{Z}. \forall b \in \mathbb{N}. f(\iota_A(a, b)) = \iota_B(a, b)$$

The *category of decimal fraction algebras* is the category $DFA$ whose objects $Ob(DFA)$ are decimal fraction algebras and whose morphisms $Mor(DFA)$ are decimal fraction algebra homomorphisms. The set of **decimal fractions**, denoted $\mathbb{Z}[1/10]$, is defined as the initial object in the category of decimal fraction algebras. 

## Properties ##

### Commutative ring structure ###

+-- {: .num_defn}
###### Definition
**(Addition)

There exists a binary operation $(-)+(-):\mathbb{Z}[1/10] \times \mathbb{Z}[1/10] \to \mathbb{Z}[1/10]$ called **addition** defined as 

$$a/10^b + c/10^d \coloneqq (a \cdot 10^d + c \cdot 10^b)/10^{(b + d)}$$

for $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$. 
=--

+-- {: .num_prop} 
###### Proposition
**(Associativity of addition)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $q \in \mathbb{Z}[1/10]$, and $r \in \mathbb{Z}[1/10]$, $(p + q) + r = p + (q + r)$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$, $e \in \mathbb{Z}$, $f \in \mathbb{N}$ such that $a/10^b = p$, $c/10^d = q$, and $e/10^f = q$. Thus, 

$$p + q = a/10^b + c/10^d = (a \cdot 10^d + c \cdot 10^b)/10^{(b + d)}$$ 

$$(p + q) + r = (a \cdot 10^d + c \cdot 10^b)/10^{(b + d)} + e/10^f = ((a \cdot 10^d + c \cdot 10^b) \cdot 10^f + e \cdot 10^{(b + d)})/10^{(b + d) + f}$$ 

$$q + r = c/10^d + e/10^f = (c \cdot 10^f + e \cdot 10^d)/10^{(d + f)}$$ 

$$p + (q + r) = a/10^b + (c \cdot 10^f + e \cdot 10^d)/10^{(d + f)} = (a \cdot 10^{(d + f)} + (c \cdot 10^f + e \cdot 10^d) \cdot 10^b)/10^{b + (d + f)}$$ 

by definition of addition. By the distributive property of multiplication of integers

$$((a \cdot 10^d + c \cdot 10^b) \cdot 10^f + e \cdot 10^{(b + d)})/10^{(b + d) + f} = (a \cdot 10^d \cdot 10^f + c \cdot 10^b \cdot 10^f) + e \cdot 10^{(b + d)})/10^{(b + d) + f}$$

$$(a \cdot 10^{(d + f)} + (c \cdot 10^f + e \cdot 10^d) \cdot 10^b)/10^{b + (d + f)} = (a \cdot 10^{(d + f)} + (c \cdot 10^f \cdot 10^b + e \cdot 10^d \cdot 10^b)/10^{b + (d + f)}$$ 

and by the fact that exponentiation is an $\mathbb{N}$-[[action]] with respect to multiplication and by the commutative property of addition of natural numbers, 

$$(a \cdot 10^d \cdot 10^f + c \cdot 10^b \cdot 10^f) + e \cdot 10^{(b + d)})/10^{(b + d) + f} = (a \cdot 10^{d + f} + c \cdot 10^{b + f}) + e \cdot 10^{(b + d)})/10^{(b + d) + f}$$

$$(a \cdot 10^{(d + f)} + (c \cdot 10^f \cdot 10^b + e \cdot 10^d \cdot 10^b)/10^{b + (d + f)} = (a \cdot 10^{d + f} + (c \cdot 10^{b + f} + e \cdot 10^{b + d})/10^{b + (d + f)}$$ 

Finally, by the associative property of addition of integers and natural numbers, 

$$(a \cdot 10^{d + f} + c \cdot 10^{b + f}) + e \cdot 10^{(b + d)})/10^{(b + d) + f} = (a \cdot 10^{d + f} + (c \cdot 10^{b + f} + e \cdot 10^{b + d})/10^{b + (d + f)}$$

Thus, $(p + q) + r = p + (q + r)$. 

=-- 

+-- {: .num_prop} 
###### Proposition
**(Commutativity of addition)

For every decimal fraction $p \in \mathbb{Z}[1/10]$ and $q \in \mathbb{Z}[1/10]$, $p + q = q + p$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$ such that $a/10^b = p$ and $c/10^d = q$. Thus, 

$$p + q = a/10^b + c/10^d = (a \cdot 10^d + c \cdot 10^b)/10^{(b + d)}$$ 

and

$$q + p = c/10^d + a/10^b = (c \cdot 10^b + a \cdot 10^d)/10^{(d + b)}$$ 

by definition of addition. By the commutativity of addition in the integers and the natural numbers, 

$$(a \cdot 10^d + c \cdot 10^b)/10^{(b + d)} = (c \cdot 10^b + a \cdot 10^d)/10^{(d + b)}$$

Thus, $p + q = q + p$. 

=-- 

+-- {: .num_defn}
###### Definition
**(Zero)

There exists an element $0 \in \mathbb{Z}[1/10]$ called **zero** and defined as $0 \coloneqq 0/10^0$. 
=--

+-- {: .num_prop} 
###### Proposition
**(Zero is a left identity of addition)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $0 + p = p$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$ such that $a/10^b = p$. Thus, 

$$0 + p = 0/10^0 + a/10^b = (0 \cdot 10^b + a \cdot 10^0)/10^{(0 + b)}$$ 

by definition of addition. By the absorption property of $0$ with respect to multiplication in the integers, 

$$(0 \cdot 10^b + a \cdot 10^0)/10^{(0 + b)} = (a \cdot 10^0)/10^{(0 + b)}$$

by the fact that exponentiation is an $\mathbb{N}$-[[action]] with respect to multiplication in the integers, 

$$(a \cdot 10^0)/10^{(0 + b)} = (a \cdot 1)/10^{(0 + b)}$$

by the fact that 1 is a right identity element with respect to multiplication in the integers, 

$$(a \cdot 1)/10^{(0 + b)} = a/10^{(0 + b)}$$

and by the fact that 0 is a left identity element with respect to addition in the natural numbers,

$$a/10^{(0 + b)} = a/10^{b}$$

Thus, $0 + p = p$. 

=-- 

+-- {: .num_prop} 
###### Proposition
**(Zero is a right identity of addition)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $p + 0 = p$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$ such that $a/10^b = p$. Thus, 

$$p + 0 = a/10^b + 0/10^0 = (a \cdot 10^0 + 0 \cdot 10^b)/10^{(b + 0)}$$ 

by definition of addition. By the absorption property of $0$ with respect to multiplication in the integers, 

$$(a \cdot 10^0 + 0 \cdot 10^b)/10^{(b + 0)} = (a \cdot 10^0)/10^{(b + 0)}$$

by the fact that exponentiation is an $\mathbb{N}$-[[action]] with respect to multiplication in the integers, 

$$(a \cdot 10^0)/10^{(b + 0)} = (a \cdot 1)/10^{(b + 0)}$$

by the fact that 1 is a right identity element with respect to multiplication in the integers, 

$$(a \cdot 1)/10^{(b + 0)} = a/10^{(b + 0)}$$

and by that 0 is a left identity element with respect to addition in the natural numbers,

$$a/10^{(b + 0)} = a/10^{b}$$

Thus, $p + 0 = p$. 

=-- 

+-- {: .num_defn}
###### Definition
**(Negation)

There exists a function $-(-):\mathbb{Z}[1/10] \to \mathbb{Z}[1/10]$ called **negation** and defined as 

$$-(a/10^b) \coloneqq (-a)/10^b$$

for $a \in \mathbb{Z}$, $b \in \mathbb{N}$. 
=--

+-- {: .num_prop} 
###### Proposition
**(Negation is a left inverse of addition)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $-p + p = 0$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$ such that $a/10^b = p$. Thus, 

$$-p + p = (-a)/10^b + a/10^0 = ((-a) \cdot 10^b + a \cdot 10^b)/10^{(b + b)}$$ 

by definition of addition. By the fact that multiplication is a [[bilinear function]] in the integers,

$$((-a) \cdot 10^b + a \cdot 10^b)/10^{(b + b)} = (-(a \cdot 10^b) + a \cdot 10^b)/10^{(b + b)}$$ 

and by the fact that negation is a left inverse of addition in the integers, 

$$(-(a \cdot 10^b) + a \cdot 10^b)/10^{(b + b)}/10^{(b + b)} = 0/10^{(b + b)}$$

and by definition of equality of decimal fractions, since 

$$0 \cdot 10^{(b + b)} = 0 \cdot 10^0$$

this means that 

$$0/10^{(b + b)} = 0/10^0$$

Thus, $-p + p = 0$. 

=-- 

+-- {: .num_prop} 
###### Proposition
**(Negation is a right inverse of addition)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $p + (-p) = 0$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$ such that $a/10^b = p$. Thus, 

$$p + -p = a/10^b + (-a)/10^0 = (a \cdot 10^b + (-a) \cdot 10^b)/10^{(b + b)}$$ 

by definition of addition. By the fact that multiplication is a [[bilinear function]] in the integers,

$$(a \cdot 10^b + (-a) \cdot 10^b)/10^{(b + b)} = (a \cdot 10^b + -(a \cdot 10^b))/10^{(b + b)}$$ 

and by the fact that negation is a right inverse of addition in the integers, 

$$(a \cdot 10^b + -(a \cdot 10^b))/10^{(b + b)} = 0/10^{(b + b)}$$

and by definition of equality of decimal fractions, since 

$$0 \cdot 10^{(b + b)} = 0 \cdot 10^0$$

this means that 

$$0/10^{(b + b)} = 0/10^0$$

Thus, $p + -p = 0$. 

=-- 

+-- {: .num_defn}
###### Definition
**(Subtraction)

There exists a binary operation $(-)-(-):\mathbb{Z}[1/10] \times \mathbb{Z}[1/10] \to \mathbb{Z}[1/10]$ called **subtraction** defined as 

$$a/10^b - c/10^d \coloneqq (a \cdot 10^d - c \cdot 10^b)/10^{(b + d)}$$

for $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$. 
=--

+-- {: .num_prop} 
###### Proposition
**(Abelian group)

The decimal fractions $(\mathbb{Z}[1/10], 0, +, -)$ form an [[abelian group]]. 
=--

+-- {: .num_defn}
###### Definition
**(Multiplication)

There exists a binary operation $(-)\cdot (-):\mathbb{Z}[1/10] \times \mathbb{Z}[1/10] \to \mathbb{Z}[1/10]$ called **multiplication** defined as 

$$a/10^b \cdot c/10^d \coloneqq (a \cdot c)/10^{(b + d)}$$

for $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$. 
=--

+-- {: .num_prop} 
###### Proposition
**(Left distributivity of multiplication over addition)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $q \in \mathbb{Z}[1/10]$, and $r \in \mathbb{Z}[1/10]$, $p \cdot (q + r) = p \cdot q + p \cdot r$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$, $e \in \mathbb{Z}$, $f \in \mathbb{N}$ such that $a/10^b = p$, $c/10^d = q$, and $e/10^f = q$. Thus, 

$$q + r = c/10^d + e/10^f = (c \cdot 10^f + e \cdot 10^d)/10^{(d + f)}$$ 

$$p \cdot (q + r) = a/10^b \cdot (c \cdot 10^f + e \cdot 10^d)/10^{(d + f)} = (a \cdot (c \cdot 10^f + e \cdot 10^d))/10^{b + (d + f)}$$ 

$$p \cdot q = a/10^b \cdot c/10^d = (a \cdot c)/10^{(b + d)}$$ 

$$p \cdot r = a/10^b \cdot e/10^f = (a \cdot e)/10^{(b + f)}$$ 

$$p \cdot q + p \cdot r = (a \cdot c)/10^{(b + d)} + (a \cdot e)/10^{(b + f)} = ((a \cdot c) \cdot 10^{(b + f)} + (a \cdot e) \cdot 10^{(b + d)})/10^{(b + d) + (b + f)}$$ 

by definition of addition and multiplication. By left distributivity of multiplication over addition of integers, 

$$(a \cdot (c \cdot 10^f + e \cdot 10^d))/10^{b + (d + f)} = (a \cdot (c \cdot 10^f) + a \cdot (e \cdot 10^d))/10^{b + (d + f)}$$

and by associativity of multiplication of integers, 

$$(a \cdot (c \cdot 10^f) + a \cdot (e \cdot 10^d))/10^{b + (d + f)} = ((a \cdot c) \cdot 10^f + (a \cdot e) \cdot 10^d)/10^{b + (d + f)}$$

Now we consider the following integer expressions: by the right distributive property of multiplication over addition in integers, 

$$((a \cdot c) \cdot 10^f + (a \cdot e) \cdot 10^d) \cdot 10^{(b + d) + (b + f)} = ((a \cdot c) \cdot 10^f) \cdot 10^{(b + d) + (b + f)} + ((a \cdot e) \cdot 10^d) \cdot 10^{(b + d) + (b + f)}$$

$$((a \cdot c) \cdot 10^{(b + f)} + (a \cdot e) \cdot 10^{(b + d)}) \cdot 10^{b + (d + f)} = ((a \cdot c) \cdot 10^{(b + f)}) \cdot 10^{b + (d + f)} + ((a \cdot e) \cdot 10^{(b + d)}) \cdot 10^{b + (d + f)}$$

and by the associative property of multiplication in integers,

$$((a \cdot c) \cdot 10^f) \cdot 10^{(b + d) + (b + f)} + ((a \cdot e) \cdot 10^d) \cdot 10^{(b + d) + (b + f)} = (a \cdot c) \cdot (10^f \cdot 10^{(b + d) + (b + f)}) + (a \cdot e) \cdot (10^d \cdot 10^{(b + d) + (b + f)})$$

$$((a \cdot c) \cdot 10^{(b + f)}) \cdot 10^{b + (d + f)} + ((a \cdot e) \cdot 10^{(b + d)}) \cdot 10^{b + (d + f)} = (a \cdot c) \cdot (10^{(b + f)} \cdot 10^{b + (d + f)}) + (a \cdot e) \cdot (10^{(b + d)} \cdot 10^{b + (d + f)})$$

By the fact that exponentiation is an $\mathbb{N}$-action over multiplication on the integers, 

$$(a \cdot c) \cdot (10^f \cdot 10^{(b + d) + (b + f)}) + (a \cdot e) \cdot (10^d \cdot 10^{(b + d) + (b + f)}) = (a \cdot c) \cdot 10^{f + ((b + d) + (b + f))} + (a \cdot e) \cdot (10^{d + ((b + d) + (b + f))}$$

$$(a \cdot c) \cdot (10^{(b + f)} \cdot 10^{b + (d + f)}) + (a \cdot e) \cdot (10^{(b + d)} \cdot 10^{b + (d + f)}) = (a \cdot c) \cdot 10^{(b + f) + (b + (d + f))} + (a \cdot e) \cdot 10^{(b + d) + (b + (d + f))}$$

and by the associativity and commutativity of addition on the natural numbers, 

$$(a \cdot c) \cdot 10^{f + ((b + d) + (b + f))} + (a \cdot e) \cdot (10^{d + ((b + d) + (b + f))} = (a \cdot c) \cdot 10^{(f + (b + d)) + (b + f)} + (a \cdot e) \cdot (10^{d + ((b + f) + (b + d))}$$

$$(a \cdot c) \cdot 10^{(f + (b + d)) + (b + f)} + (a \cdot e) \cdot (10^{d + ((b + f) + (b + d))} = (a \cdot c) \cdot 10^{(b + f) + ((b + d) + f)} + (a \cdot e) \cdot (10^{(d + (b + f)) + (b + d)}$$

$$(a \cdot c) \cdot 10^{(b + f) + ((b + d) + f)} + (a \cdot e) \cdot (10^{(d + (b + f)) + (b + d)} = (a \cdot c) \cdot 10^{(b + f) + (b + (d + f))} + (a \cdot e) \cdot (10^{(b + d) + ((b + f) + d)}$$

$$(a \cdot c) \cdot 10^{(b + f) + (b + (d + f))} + (a \cdot e) \cdot (10^{(b + d) + ((b + f) + d)} = (a \cdot c) \cdot 10^{(b + f) + (b + (d + f))} + (a \cdot e) \cdot (10^{(b + d) + (b + (f + d))}$$

$$(a \cdot c) \cdot 10^{(b + f) + (b + (d + f))} + (a \cdot e) \cdot (10^{(b + d) + (b + (f + d))} = (a \cdot c) \cdot 10^{(b + f) + (b + (d + f))} + (a \cdot e) \cdot (10^{(b + d) + (b + (d + f))}$$

Thus, 

$$((a \cdot c) \cdot 10^f + (a \cdot e) \cdot 10^d) \cdot 10^{(b + d) + (b + f)} = ((a \cdot c) \cdot 10^{(b + f)} + (a \cdot e) \cdot 10^{(b + d)}) \cdot 10^{b + (d + f)}$$

By definition of equality of decimal fractions, since 

$$((a \cdot c) \cdot 10^f + (a \cdot e) \cdot 10^d) \cdot 10^{(b + d) + (b + f)} = ((a \cdot c) \cdot 10^{(b + f)} + (a \cdot e) \cdot 10^{(b + d)}) \cdot 10^{b + (d + f)}$$

then

$$((a \cdot c) \cdot 10^f) + (a \cdot e) \cdot 10^d))/10^{b + (d + f)} = ((a \cdot c) \cdot 10^{(b + f)} + (a \cdot e) \cdot 10^{(b + d)})/10^{(b + d) + (b + f)}$$

Thus, $p \cdot (q + r) = p \cdot q + p \cdot r$. 

=-- 

+-- {: .num_prop} 
###### Proposition
**(Right distributivity of multiplication over addition)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $q \in \mathbb{Z}[1/10]$, and $r \in \mathbb{Z}[1/10]$, $(p + q) \cdot r = p \cdot r + q \cdot r$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$, $e \in \mathbb{Z}$, $f \in \mathbb{N}$ such that $a/10^b = p$, $c/10^d = q$, and $e/10^f = q$. Thus, 

$$p + q = a/10^b + c/10^d = (a \cdot 10^d + c \cdot 10^b)/10^{(b + d)}$$ 

$$(p + q) \cdot r = (a \cdot 10^d + c \cdot 10^b)/10^{(b + d)} \cdot e/10^f = ((a \cdot 10^d + c \cdot 10^b) \cdot e)/10^{(b + d) + f)}$$ 

$$p \cdot r = a/10^b \cdot e/10^f = (a \cdot e)/10^{(b + f)}$$ 

$$q \cdot r = c/10^d \cdot c/10^d = (c \cdot e)/10^{(d + f)}$$ 

$$p \cdot r + q \cdot r = (a \cdot e)/10^{(b + f)} + (c \cdot e)/10^{(d + f)} = ((a \cdot e) \cdot 10^{(d + f)} + (c \cdot e) \cdot 10^{(b + f)})/10^{(b + f) + (d + f)}$$ 

by definition of addition and multiplication. By right distributivity of multiplication over addition of integers, 

$$((a \cdot 10^d + c \cdot 10^b) \cdot e)/10^{(b + d) + f)} = ((a \cdot 10^d) \cdot e + (c \cdot 10^b) \cdot e)/10^{(b + d) + f)}$$

and by associativity of multiplication of integers, 

$$((a \cdot 10^d) \cdot e + (c \cdot 10^b) \cdot e)/10^{(b + d) + f)} = (a \cdot (10^d \cdot e) + c \cdot (10^b \cdot e))/10^{(b + d) + f)}$$

and by commutativity of multiplication of integers,

$$(a \cdot (10^d \cdot e) + c \cdot (10^b \cdot e))/10^{(b + d) + f)} = (a \cdot (e \cdot 10^d) + c \cdot (e \cdot 10^b))/10^{(b + d) + f)}$$

and by associativity of multiplication of integers, 

$$(a \cdot (e \cdot 10^d) + c \cdot (e \cdot 10^b))/10^{(b + d) + f)} = ((a \cdot e) \cdot 10^d + (c \cdot e) \cdot 10^b)/10^{(b + d) + f)}$$

Now we consider the following integer expressions: by the right distributive property of multiplication over addition in integers, 

$$((a \cdot e) \cdot 10^d + (c \cdot e) \cdot 10^b) \cdot 10^{(b + f) + (d + f)} = ((a \cdot e) \cdot 10^d) \cdot 10^{(b + f) + (d + f)} + ((c \cdot e) \cdot 10^b) \cdot 10^{(b + f) + (d + f)}$$

$$((a \cdot e) \cdot 10^{(d + f)} + (c \cdot e) \cdot 10^{(b + f)}) \cdot 10^{(b + d) + f)} = ((a \cdot e) \cdot 10^{(d + f)}) \cdot 10^{(b + d) + f)} + ((c \cdot e) \cdot 10^{(b + f)}) \cdot 10^{(b + d) + f)}$$

and by the associative property of multiplication in integers,

$$((a \cdot e) \cdot 10^d) \cdot 10^{(b + f) + (d + f)} + ((c \cdot e) \cdot 10^b) \cdot 10^{(b + f) + (d + f)} = (a \cdot e) \cdot (10^d \cdot 10^{(b + f) + (d + f)}) + (c \cdot e) \cdot (10^b \cdot 10^{(b + f) + (d + f)})$$

$$((a \cdot e) \cdot 10^{(d + f)}) \cdot 10^{(b + d) + f)} + (c \cdot e) \cdot 10^{(b + f)}) \cdot 10^{(b + d) + f)} = (a \cdot e) \cdot (10^{(d + f)} \cdot 10^{(b + d) + f)}) + (c \cdot e) \cdot (10^{(b + f)} \cdot 10^{(b + d) + f)})$$

By the fact that exponentiation is an $\mathbb{N}$-action over multiplication on the integers, 

$$(a \cdot e) \cdot (10^d \cdot 10^{(b + f) + (d + f)}) + (c \cdot e) \cdot (10^b \cdot 10^{(b + f) + (d + f)}) = (a \cdot e) \cdot 10^{d + ((b + f) + (d + f))} + (c \cdot e) \cdot (10^{b + ((b + f) + (d + f))}$$

$$(a \cdot e) \cdot (10^{(d + f)} \cdot 10^{(b + d) + f)}) + (c \cdot e) \cdot (10^{(b + f)} \cdot 10^{(b + d) + f)}) = (a \cdot e) \cdot 10^{(d + f) + ((b + d) + f)} + (c \cdot e) \cdot 10^{(b + f) + ((b + d) + f)}$$

and by the associativity and commutativity of addition on the natural numbers, 

$$(a \cdot e) \cdot 10^{d + ((b + f) + (d + f))} + (c \cdot e) \cdot (10^{b + ((b + f) + (d + f))} = (a \cdot e) \cdot 10^{(d + (b + f)) + (d + f)} + (c \cdot e) \cdot (10^{b + ((d + f) + (b + f))}$$

$$(a \cdot e) \cdot 10^{(d + (b + f)) + (d + f)} + (c \cdot e) \cdot (10^{b + ((d + f) + (b + f))} = (a \cdot e) \cdot 10^{(d + f) + (d + (b + f))} + (c \cdot e) \cdot (10^{(b + (d + f)) + (b + f)}$$

$$(a \cdot e) \cdot 10^{(d + (b + f)) + (d + f)} + (c \cdot e) \cdot (10^{b + ((d + f) + (b + f))} = (a \cdot e) \cdot 10^{(d + f) + ((d + b) + f)} + (c \cdot e) \cdot (10^{(b + f) + (b + (d + f))}$$

$$(a \cdot e) \cdot 10^{(d + f) + ((d + b) + f)} + (c \cdot e) \cdot (10^{(b + f) + (b + (d + f))} = (a \cdot e) \cdot 10^{(d + f) + ((b +d) + f)} + (c \cdot e) \cdot (10^{(b + f) + ((b + d) + f)}$$

Thus, 

$$((a \cdot e) \cdot 10^d + (c \cdot e) \cdot 10^b) \cdot 10^{(b + f) + (d + f)} = ((a \cdot e) \cdot 10^{(d + f)} + (c \cdot e) \cdot 10^{(b + f)}) \cdot 10^{(b + d) + f)}$$

By definition of equality of decimal fractions, since 

$$((a \cdot e) \cdot 10^d + (c \cdot e) \cdot 10^b) \cdot 10^{(b + f) + (d + f)} = ((a \cdot e) \cdot 10^{(d + f)} + (c \cdot e) \cdot 10^{(b + f)}) \cdot 10^{(b + d) + f)}$$

then

$$((a \cdot e) \cdot 10^d + (c \cdot e) \cdot 10^b)/10^{(b + d) + f)} = ((a \cdot e) \cdot 10^{(d + f)} + (c \cdot e) \cdot 10^{(b + f)})/10^{(b + f) + (d + f)}$$

Thus, $(p + q) \cdot r = p \cdot r + q \cdot r$. 

=-- 

+-- {: .num_prop} 
###### Proposition
**(Associativity of multiplication)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $q \in \mathbb{Z}[1/10]$, and $r \in \mathbb{Z}[1/10]$, $(p \cdot q) \cdot r = p \cdot (q \cdot r)$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$, $e \in \mathbb{Z}$, $f \in \mathbb{N}$ such that $a/10^b = p$, $c/10^d = q$, and $e/10^f = q$. Thus, 

$$p \cdot q = a/10^b \cdot c/10^d = (a \cdot c)/10^{(b + d)}$$ 

$$(p \cdot q) \cdot r = (a \cdot c)/10^{(b + d)} + e/10^f = ((a \cdot c) \cdot e)/10^{(b + d) + f}$$ 

$$q \cdot r = c/10^d \cdot e/10^f = (c \cdot e)/10^{(d + f)}$$ 

$$p \cdot (q \cdot r) = a/10^b + (c \cdot e)/10^{(d + f)} = (a \cdot (c \cdot e))/10^{b + (d + f)}$$ 

by definition of addition. By the associative property of multiplication of integers and addition of natural numbers, 

$$((a \cdot c) \cdot e)/10^{(b + d) + f} = (a \cdot (c \cdot e))/10^{b + (d + f)}$$

Thus, $(p \cdot q) \cdot r = p \cdot (q \cdot r)$. 

=-- 

+-- {: .num_prop} 
###### Proposition
**(Commutativity of multiplication)

For every decimal fraction $p \in \mathbb{Z}[1/10]$ and $q \in \mathbb{Z}[1/10]$, $p \cdot q = q \cdot p$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$, $c \in \mathbb{Z}$, $d \in \mathbb{N}$ such that $a/10^b = p$ and $c/10^d = q$. Thus, 

$$p \cdot q = a/10^b \cdot c/10^d = (a \cdot c)/10^{(b + d)}$$ 

and

$$q \cdot p = c/10^d \cdot a/10^b = (c \cdot a)/10^{(d + b)}$$ 

by definition of addition. By the commutativity of multiplication in the integers and the commutativity of addition in the natural numbers, 

$$(a \cdot c)/10^{(b + d)} = (c \cdot a)/10^{(d + b)}$$

Thus, $p \cdot q = q \cdot p$. 

=-- 

+-- {: .num_defn}
###### Definition
**(One)

There exists an element $1 \in \mathbb{Z}[1/10]$ called **one** and defined as $1 \coloneqq 1/10^0$. 
=--

+-- {: .num_prop} 
###### Proposition
**(One is a left identity of multiplication)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $1 \cdot p = p$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$ such that $a/10^b = p$. Thus, 

$$1 \cdot p = 1/10^0 \cdot a/10^b = (1 \cdot a)/10^{(0 + b)}$$ 

by the fact that 1 is a left identity element with respect to multiplication in the integers, 

$$(1 \cdot a)/10^{(0 + b)} = a/10^{(0 + b)}$$

and by the fact that 0 is a left identity element with respect to addition in the natural numbers,

$$a/10^{(0 + b)} = a/10^{b}$$

Thus, $1 \cdot p = p$. 

=-- 

+-- {: .num_prop} 
###### Proposition
**(One is a right identity of multiplication)

For every decimal fraction $p \in \mathbb{Z}[1/10]$, $p \cdot 1 = p$. 
=--

+-- {: .proof} 
###### Proof 

By definition of the set of decimal fractions, there exist numbers $a \in \mathbb{Z}$, $b \in \mathbb{N}$ such that $a/10^b = p$. Thus, 

$$p \cdot 1 = a/10^b \cdot 1/10^0 = (a \cdot 1)/10^{(b + 0)}$$ 

by the fact that 1 is a right identity element with respect to multiplication in the integers, 

$$(a \cdot 1)/10^{(b + 0)} = a/10^{(b + 0)}$$

and by the fact that 0 is a right identity element with respect to addition in the natural numbers,

$$a/10^{(b + 0)} = a/10^{b}$$

Thus, $p \cdot 1 = p$. 

=-- 

+-- {: .num_prop} 
###### Proposition
**(Commutative ring)

The decimal fractions $(\mathbb{Z}[1/10], 0, +, -)$ form a [[commutative ring]]. 
=--

### Sign 

...

## Related entries

* [[dyadic rational number]]

## References

* Wikipedia, _[Decimal](https://en.wikipedia.org/wiki/Decimal#Decimal_fractions)_

[[!redirects decimal rational numbers]]

[[!redirects decimal rational]]
[[!redirects decimal rationals]]

[[!redirects decimal fraction]]
[[!redirects decimal fractions]]