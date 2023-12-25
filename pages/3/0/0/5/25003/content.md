
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

A definition of [[ordered field]] in [[constructive mathematics]] which uses [[denial inequality]]. It is primarily used in [[synthetic differential geometry]]. 

## Definition

An **ordered Kock field** is a [[Kock field]] $R$ with a [[strict weak order]] $\lt$ which is not necessarily [[connected relation|connected]]: 

1. for all $a \in R$, $\neg(a \lt a)$ 

2. for all $a \in R$ and $b \in R$, if $a \lt b$, then $\neg(b \lt a)$

3. for all $a \in R$, $b \in R$, and $c \in R$, if $a \lt c$, then $a \lt b$ or $b \lt c$

4. $0 \lt 1$

5. for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a + b$

6. for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a \cdot b$

7. for all $a \in R$, $a \neq 0$ if and only if $a \lt 0$ or $0 \lt a$

## See also

* [[Kock field]]

* [[ordered local ring]]

## References

* [[David Jaz Myers]], *Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory* ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))