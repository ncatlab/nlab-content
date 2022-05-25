
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A ternary [[function]] which simultaneously exhibits an [[action]] on a [[set]] from both the left and the right side. 

Sets with biactions are the [[bimodule objects]] [[internalization|internal to]] [[Set]]. 



## Definition

Given a [[set]] $S$ and [[monoids]] $(M, e_M, \mu_M)$ and $(N, e_N, \mu_N)$, a **$M$-$N$-biaction** or **two-sided action** is a ternary function $\alpha:M \times S \times N \to S$ such that 

* for all $s \in S$, $\alpha(e_M, s, e_N) = s$

* for all $s \in S$, $a \in M$, $b \in M$, $c \in N$, and $d \in N$, $\alpha\big(a, \alpha(b, s, c), d\big) = \alpha\big(\mu_M(a, b), s, \mu_N(c, d)\big)$

## Left and right actions

The [[left action|left $M$-action]] is defined as 

$$\alpha_M(a, s) \coloneqq \alpha(a, s, e_N)$$

for all $a \in M$ and $s \in S$. It is a left action because 

$$\alpha_M(e_M, s) = \alpha(e_M, s, e_N) = s$$

$$\alpha_M\big(a, \alpha_L(b, s)\big) = \alpha\big(a, \alpha(b, s, e_N), e_N\big) = \alpha\big(\mu_M(a, b), s, \mu_N(e_N, e_N)\big) = \alpha\big(\mu_M(a, b), s, e_N\big) = \alpha_M\big(\mu_M(a, b), s\big)$$

The [[right action|right $N$-action]] is defined as 

$$\alpha_N(s, c) \coloneqq \alpha(e_M, s, c)$$

for all $c \in N$ and $s \in S$. It is a right action because 

$$\alpha_N(s, e_N) = \alpha(e_M, s, e_N) = s$$

$$\alpha_N\big(\alpha_N(s, c), d\big) = \alpha\big(e_M, \alpha(e_M, s, c), d\big) = \alpha\big(\mu_M(e_M, e_M), s, \mu_N(c, d)\big) = \alpha\big(e_M, s, \mu_N(c, d)\big) = \alpha_N\big(s, \mu_N(c, d)\big)$$

The left $M$-action and right $N$-action satisfy the following identity: 

* for all $s \in S$, $a \in M$ and $c \in N$, $\alpha_M\big(a, \alpha_N(s, c)\big) = \alpha_N\big(\alpha_M(a, s), c\big)$. 

This is because when expanded out, the identity becomes:

$$\alpha\big(a, \alpha(e_M, s, c), e_N\big) = \alpha\big(e_M, \alpha(a, s, e_N), c\big)$$

$$\alpha\big(\mu_M(a, e_M), s, \mu_N(c, e_N)\big) = \alpha\big(\mu_M(e_M, a), s, \mu_N(e_N, c)\big)$$

$$\alpha(a, s, c) = \alpha(a, s, c)$$

## See also

* [[action]]

* [[bimodule]]

[[!redirects biactions]]

[[!redirects two-sided action]]
[[!redirects two-sided actions]]
