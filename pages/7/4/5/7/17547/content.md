

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
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

_Milnor's theorem_ describes the dual mod-$p$ [[Steenrod algebra]] in terms of [[generators and relations]].


## Statement

In the following, we use for $p = 2$ the notation 

$$
  P^n \coloneqq Sq^{2n}
$$

$$
  \beta \coloneqq Sq^1
  \,.
$$

This serves to unify the expressions  for $p = 2$ and for $p \gt 2$ in the following. Notice that for all $p$

* $P^n$ has even degree $deg(P^n) = 2n(p-1)$;

* $\beta$ has odd degree $deg(\beta) = 1$.


+-- {: .num_theorem #MilnorTheoremOnDualSteenrodAlgebra}
###### Theorem
**(Milnor's theorem)**

The dual mod $p$-Steenrod algebra $\mathcal{A}^\ast_{\mathbb{F}_p}$ (def. \ref{DualSteenrodAlgebraForHPf}) is, as an [[associative algebra]], the free [[graded commutative algebra]]

$$
  \mathcal{A}^\ast_{\mathbb{F}_p}
    \simeq
  Sym_{\mathbb{F}_p}(\xi_1, \xi_2, \cdots, \;\tau_0, \tau_1, \cdots)
$$

on generators:

* $\xi_n$ being the linear dual to $P^{p^{n-1}} P^{p^{n-2}} \cdots P^p P^1$;

* $\tau_n$ being linear dual to $P^{p^{n-1}} P^{p^{n-2}} \cdots P^p P^1\beta$.

Moreover, the coproduct on $\mathcal{A}^\ast_{\mathbb{F}_p}$ is given by

$$
  \Psi(\xi_n)
  =
  \underoverset{k = 0}{n}{\sum} \xi_{n-k}^{p^k} \otimes \xi_k
$$

and

$$
  \Psi(\tau_n)
  =
  \tau_n \otimes 1
  + 
  \underoverset{k=0}{n}{\sum}
  \xi_{n-k}^{p^k} \xi_{n-k}^{p^k}\otimes \tau_k
  \,,
$$

where we set $\xi_0 \coloneqq 1$.

=--

This is due to ([Milnor 58](#Milnor58)). See for instance ([Kochman 96, theorem 2.5.1](#Kochman96))

## References

* {#Milnor58} [[John Milnor]], _The Steenrod algebra and its dual_, Ann. of Math. 67 (1958), 150&#8211;171.


* {#Kochman96} [[Stanley Kochman]], section 2.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

[[!redirects Milnor theorem]]
