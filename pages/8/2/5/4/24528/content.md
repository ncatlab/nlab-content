
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Overview

*Schanuel's lemma* is basic [[lemma]] in [[homological algebra]], useful in the study of [[projective resolutions]].

## Statement

Let $R$ be a [[commutative ring]].

Given two [[short exact sequences]] of $R$-[[modules]],

$$
  0 
  \rightarrow 
  P_0
  \rightarrow 
  P_1
  \rightarrow 
  M
  \rightarrow 
  0
$$
$$
  0
  \rightarrow 
  P_0'
  \rightarrow 
  P_1'
  \rightarrow 
  M
  \rightarrow 
  0
$$

with $P_0,P_1,P_0',P_1'$ [[projective module|projective]], there is 
an [[isomorphism]] of the [[direct sums]]

$$
  P_0 \oplus P_1' \;\cong\; P_0'\oplus P_1
  \,.
$$

## Proof

Observe the following commutative diagram 

$$
  \array{   
     &&  && 0 && 0 &&
     \\
     &&  && \downarrow && \downarrow && 
     \\
      & &  & & P_0' &\to& P_0'&\to& 0
     \\
     &&  && \downarrow && \downarrow && 
     \\
     0 & \to & P_0 &\to& Q &\to& P_1' &\to& 0
     \\
     && \downarrow && \downarrow && \downarrow && 
     \\
     0 & \to & P_0 &\to& P_1 &\to& M &\to& 0
     \\
     &&  && \downarrow && \downarrow && 
     \\
     && && 0 && 0 &&
  }
$$
where the square $Q-P_1'-M-P_1$ is cartesian and the morphisms
$P_0\to Q$ and $P_0'\to Q$ are obtained by the universal property of cartesian square. These morphisms are then necessarily monic and the rows and columns are also exact at $Q$. Thus rows and columns of the diagram are exact. Now, by the projectivity of $P_1'$ and $P_1$ the upper and the left  short exact sequences split, hence
$P_0\oplus P_1' = Q = P_0'\oplus P_1$.


## Literature

Textbook accounts:

* [[Carl Faith]], _Algebra: Rings, Modules, Categories_, vol. 1,  Grundlehren der mathematischen Wissenschaften **190**, Springer (1973) &lbrack;[doi:10.1007/978-3-642-80634-6](https://doi.org/10.1007/978-3-642-80634-6)&rbrack;

It is Proposition 2.8.26 in 

* Louis Rowen, _Ring theory_, student edition.

See also

* Wikipedia, *[Schanuel's lemma](https://en.wikipedia.org/wiki/Schanuel%27s_lemma)*

[[!redirects Schanuel lemma]]

category: algebra
