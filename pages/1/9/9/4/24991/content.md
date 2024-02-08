\tableofcontents

## Idea

In the same way that a [[local ring]] is a [[Heyting field]] whose [[apartness relation]] is not [[tight apartness relation|tight]], an ordered local ring is an [[ordered field]] whose [[strict weak order]] is not necessarily [[connected relation|connected]]. 

## Definition

Let $R$ be a [[commutative ring]]. $R$ is an **ordered local ring** if there is a [[strict weak order]] $\lt$ such that 

* $0 \lt 1$

* for all $a \in R$ and $b \in R$, $0 \lt a$ and $0 \lt b$ implies that $0 \lt a + b$; alternatively, $0 \lt a + b$ implies that $0 \lt a$ or $0 \lt b$. 

* for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a \cdot b$

* for all $a \in R$, $a$ is invertible if and only if $a \lt 0$ or $0 \lt a$

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

## In analysis

Ordered local rings are important for modeling notions of [[infinitesimals]] and [[infinite elements]], including both the non-invertible infinitesimals common in [[synthetic differential geometry]] and the [[invertible]] infinitesimals whose reciprocals are the infinite elements common in [[nonstandard analysis]]. 

## See also

* [[local ring]]

* [[ordered field]]

* [[Archimedean ordered local ring]]

* [[ordered Artinian local ring]]

* [[ordered reduced local ring]]

* [[ordered local integral domain]]

[[!redirects ordered local ring]]
[[!redirects ordered local rings]]