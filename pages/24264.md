
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

Given a set $T$ with a [[dense linear order]] $\lt$, a pair of [[subsets]] $(L, R)$ of $T$ with [[injections]] $i_L:L \to T$ and $i_R:R \to T$ is a **Dedekind cut structure** if it comes equipped with the following structure

* an [[element]] $l \in L$
* an element $r \in R$
* for every element $a \in L$ and $b \in T$, a [[function]]
$$c_d(a, b):]b, a[ \to \{c \in L \vert i_L(c) = b\}$$
* for every element $a \in R$ and $b \in T$, a function
$$c_u(a, b):]a, b[ \to \{c \in R \vert i_R(c) = b\}$$
* for every element $a \in L$, an element
$$o_d(a) \in \{b \in L \vert i_L(a) \lt i_L(b)\}$$
* for every element $a \in R$, an element
$$o_u(a) \in \{b \in R \vert i_R(b) \lt i_R(a)\}$$
* for every element $a \in L$ and $b \in R$, an element
$$t(a, b) \in ]i_L(a), i_R(b)[$$
* for every element $a \in T$ and $b \in T$, a function
$$L(a, b):]a,b[ \to (\{c \in L \vert i_L(c) = a\} \uplus \{c \in R \vert i_R(c) = b\})$$

where $]a, b[$ is the [[open interval]] bounded by $a$ from below and by $b$ from above. 

## See also ##

* [[Dedekind cut]]
* [[locator]]
* [[dense linear order]]

## References

* Auke Booij, *Extensional constructive real analysis via locators*, ([abs:1805.06781](https://arxiv.org/abs/1805.06781))

[[!redirects Dedekind cut structures]]