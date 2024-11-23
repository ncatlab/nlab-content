+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



\tableofcontents


## Idea

In [[homological algebra]] one usually studies [[functors]] of the form $\mathcal{A}\to Ab, k-mod, \dots$ defined via [[derived functor in homological algebra|derived functors]] where $\mathcal{A}$ is some [[category]] of [[groups]], [[associative unital algebra|algebras over a ring]] $k$ etc., and [[Ab|$Ab$]], [[Mod|$k-Mod$]] are categories of [[abelian groups]] and [[module|$k$-modules]], where $k$ is some [[ground ring]]. 


For instance, for the category of [[groups]] $\mathcal{A}=$ [[Grp]], using the left derived functors $L_q(\mathbb{Z}\otimes_{\mathbb{Z}G}(-))$ of the functor of coinvariants $\mathbb{Z}\otimes_{\mathbb{Z}G}(-) \colon \mathbb{Z}G-mod\to Ab$ one usually defines [[group homology]] $H_q(G;A)  =L_q(\mathbb{Z}\otimes_{\mathbb{Z}G}(-))(A)$ of a group $G$ with [[coefficients]] in a $\mathbb{Z}G$-modules $A$. 


The idea of the *higher limit approach* of [Ivanov & Mikhailov 2015](#IvanovMikhailov15)
is to use categories $Pres(A)$ of [[extensions]] $0\to I\to P\to A\to 0$ where $P$ is a [[projective object]] in a category of algebraic objects $\mathcal{A}$ (e.g free presentations of groups) and describe such functors of homological nature $H:\mathcal{A}\to Ab, k-mod,\dots$ using derived/higher (co)limits of some simple functors $\mathcal{F}$ from the category $H\simeq lim^{*}, colim_{*}(\mathcal{F} \colon Pres(A)\to Ab, k-mod, \dots)$.  

This approach originates in the work &lbrack;[Quillen 1989](#QuillenCyclic89)&rbrack;, where, for instance, he derived the formula: 

\begin{equation}
  HC_{2n}(A)
  \;=\;
  lim\big(
    F/(I^{n+1}+[F,F])
  \big)
  \,,
\end{equation}
where $HC_{2n}(A)$ is [[cyclic homology]] of $A$ over a [[field]] of characteristic zero $k$ and $F/(I^{n+1}+[F,F])$ takes a free algebra extension $0\to I\to F\to A\to 0$ and sends it to the abelian group $F/(I^{n+1}+[F,F])$. 


## Related concepts

* [[fr-code]]


## References

The original articles

* {#QuillenCyclic89} [[Daniel Quillen]]: *Cyclic cohomology and algebra extensions*, K-Theory v. 3, n. 3 (1989): 205-246 &lbrack;[doi:10.1007/BF00533370](https://doi.org/10.1007/BF00533370)&rbrack;

* {#EmmanouilMikhailov08} [[Roman Mikhailov]], Ioannis Emmanouil: *A limit approach to group homology*, Journal of Algebra
Volume 319, Issue 4, 15 February 2008, Pages 1450-1461 &lbrack;[doi:10.1016/j.jalgebra.2007.12.006](https://doi.org/10.1016/j.jalgebra.2007.12.006)&rbrack;


* {#IvanovMikhailov15} [[Sergei O. Ivanov]], [[Roman Mikhailov]]: *A higher limit approach to homology theories*, Journal of Pure and Applied Algebra **219** 6 (2015) 1915-1939 &lbrack;[arXiv:1309.4920](https://arxiv.org/abs/1309.4920), [doi:10.1016/j.jpaa.2014.07.016](https://doi.org/10.1016/j.jpaa.2014.07.016)&rbrack;

