\tableofcontents

## Idea

In the same way that a [[local ring]] is a [[Heyting field]] whose [[apartness relation]] is not [[tight apartness relation|tight]], an ordered local ring is an [[ordered field]] whose [[strict order]] is not necessarily [[linear relation|linear]]. 

## Definition

### With an order relation

Let $R$ be a [[commutative ring]]. $R$ is an **ordered local ring** if there is a [[binary relation]] $\lt$ such that 

* for all $a \in R$, $\neg(a \lt a)$ 

* for all $a \in R$ and $b \in R$, if $a \lt b$, then $\neg(b \lt a)$

* for all $a \in R$, $b \in R$, and $c \in R$, if $a \lt c$, then $a \lt b$ or $b \lt c$

* $0 \lt 1$

* for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a + b$

* for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a \cdot b$

* for all $a \in R$, $a$ is invertible if and only if $a \lt 0$ or $0 \lt a$

We define the predicate $\mathrm{isPositive}$ as 

$$\mathrm{isPositive}(a) \coloneqq 0 \lt a$$

### With a positivity predicate

Let $R$ be a [[commutative ring]]. $R$ is an **ordered local ring** if there is a [[predicate]] $\mathrm{isPositive}$ stating an element $a$ is positive, such that 

* 0 is not positive
* given element $a \in R$, if $a$ is positive, then $-a$ is not positive
* given elements $a \in R$ and $b \in R$; if $a$ is positive, then either $b$ is positive or $a - b$ is positive
* 1 is positive
* given elements $a \in R$ and $b \in R$, if $a$ is positive and $b$ is positive, $a + b$ is positive
* given elements $a \in R$ and $b \in R$, if $a$ is positive and $b$ is positive, $a \cdot b$ is positive
* for all $a \in R$, $a$ is invertible if and only if $a$ is positive or $-a$ is positive

We define the order relation $\lt$ as 

$$a \lt b \coloneqq \mathrm{isPositive}(b - a)$$

## Properties

Every ordered local ring is a local ring with the apartness relation given by 
$$a \# b \coloneqq a \lt b \vee b \lt a$$ 

Every ordered local ring has a [[preorder]] given by $a \leq b \coloneqq \neg (b \lt a)$. 

### Quotient ordered field

Let $D$ be the [[ideal]] of all non-invertible elements in $R$. Then the quotient ring $R/D$ is an [[ordered field]]. 

### Ordered local Artinian real algebras

In synthetic differential geometry, one uses ordered local rings which are also [[commutative algebra|commutative $\mathbb{R}$-algebras]] whose ideal of zero divisors is a [[nilradical]] and which have no infinite elements. 

Given such an $\mathbb{R}$-algebra $A$, since $A$ is a [[local ring]], the quotient $A/I$ is the real numbers $\mathbb{R}$, and the canonical function used in defining the quotient is the function $\Re:A \to \mathbb{R}$ which takes a number $a \in A$ to its purely real component $\Re(a) \in \mathbb{R}$. Since $A$ is an ordered $\mathbb{R}$-algebra, there is a [[strictly monotone]] [[ring homomorphism]] $h:\mathbb{R} \to A$. A number $a \in A$ is purely real if $h(\Re(a)) = a$, and a number $a \in A$ is purely [[infinitesimal]] if it is in the [[fiber]] of $\Re$ at the real number $0$. Zero is the only number in $A$ which is both purely real and purely infinitesimal. 

## Examples

* Every [[ordered field]] is an ordered local ring where every non-positive non-negative element is equal to zero. 

* Every [[ordered Kock field]] is an ordered local ring. 

* The [[dual numbers]] $\mathbb{R}[\epsilon]/\epsilon^2$ are an ordered local ring where the [[nilpotent]] [[infinitesimal]] $\epsilon \in \mathbb{R}[\epsilon]/\epsilon^2$ is a non-zero non-positive non-negative element. 

## See also

* [[local ring]]

* [[ordered field]]

[[!redirects ordered local ring]]
[[!redirects ordered local rings]]