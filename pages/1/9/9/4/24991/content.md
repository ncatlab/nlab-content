\tableofcontents

## Idea

In the same way that a [[local ring]] is a [[Heyting field]] whose [[apartness relation]] is not [[tight apartness relation|tight]], an ordered local ring is an [[ordered field]] whose [[strict order]] is not necessarily [[connected relation|connected]]. 

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

## Examples

* Every [[ordered field]] is an ordered local ring where every non-positive non-negative element is equal to zero. 

* Every [[ordered Kock field]] is an ordered local ring. 

* The [[dual numbers]] $\mathbb{R}[\epsilon]/\epsilon^2$ are an ordered local ring where the [[nilpotent]] [[infinitesimal]] $\epsilon \in \mathbb{R}[\epsilon]/\epsilon^2$ is a non-zero non-positive non-negative element. 

## See also

* [[local ring]]

* [[ordered field]]

* [[Archimedean ordered local ring]]

* [[ordered Artinian local ring]]

* [[ordered reduced local ring]]

* [[ordered local integral domain]]

[[!redirects ordered local ring]]
[[!redirects ordered local rings]]