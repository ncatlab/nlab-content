
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



\tableofcontents

## Idea

Given that the (degree-shifted, [[reduced cohomology|reduced]]) [[topological K-theory]] group of a [[topological space]] $X$ can be computed as a [[colimit]] over sets of [[homotopy classes]] of maps (cf. at *[[stable unitary group]]*)

$$
  \tilde{K}^1(X) 
  \;=\; 
  [X,U] 
  \;=\; 
  \underset{\underset{n}{\longrightarrow}}{lim}  
  \,
  \big[X,U(n)\big]
  \,
$$

one may think of this as a [[stabilization]] of generalized [[nonabelian cohomology]] theories (in the sense of [Lurie 14, Def. 6](nonabelian+cohomology#Lurie14), [FSS23, §2](nonabelian+cohomology#FSS20)) $U_n(X)$ whose classifying spaces are the [[unitary groups]] $U(n)$. For this reason, one may call the groups $[X,U(n)] \,\coloneqq\, \pi_0 Map\big(X,U(n)\big)$ the **unstable** $\tilde{K}^1$-theory groups of $X$, at stage $n$ ([Hamanaka & Kono 2003](#HamanakaKono2003), [2004](#HamanakaKono2004)).

Similarly, the [[infinite loop space]] representing [[algebraic K-theory]] of a suitable [[ring]] $R$ is the [[colimit]]

$$
  K_0(R) 
    \;\times\; 
  \underset{\underset{n}{\longrightarrow}}{\lim} B GL(n,R)^+
$$

of the [[Quillen plus construction]] on the [[classifying spaces]] of the [[general linear groups]] $GL(n,R)$, and considering this instead for finite $n$ is the topic of *unstable algebraic K-theory* ([vd Kallen 1980 §1.2](#vdKallen1980), [Clausen & Jansen 2024 §1.3](#ClausenJansen2024)).



## Definition

+-- {: .num_defn #UnstableKGroups}
###### Definition

Let $X$ be a [[topological space]] ([[CW-complex]]), and $U(n)$ the [[unitary group]] in dimension $n$. The $n$-*unstable*  $\tilde{K}^1$*-theory group* $U_n(X)$ of $X$ is defined as the [[homotopy classes]] of maps, hence the [[connected components]] of the [[mapping space|space of maps]] from $X$ to (the [[underlying]] topological space of) $U(n)$:

$$
  U_n(X) 
  \;\coloneqq\; 
  [X,U(n)]
  \,\coloneqq\,
  \pi_0 Map\big(X,\, U(n)\big)
  \,.
$$

=--

From this definition one can see that, if $X$ is a finite-[[dimension|dimensional]] [[CW complex]] then $U_n(X) = \tilde{K}^1 (X)$ for sufficiently large $n$.

## Properties

The following properties are proven in [Hamanaka & Kono 2003](#HamanakaKono2003):

+-- {: .num_defn #LimitToKtheory}
###### Proposition
(Theorem 1.1 of [op.cit.](#HamanakaKono2003)) 
\linebreak
Let $\text{dim}(X)\leq 2n$. Then there exists an [[exact sequence]] of the form:

$$
  \tilde{K}^0(X)
    \xrightarrow{\Theta} 
  H^{2n}(X;\mathbb{Z}) 
   \to 
  U_n(X)
   \to 
  \tilde{K}^1 (X) 
    \to 
  1
  \,,
$$

or, put differently, defining $N_n (X) \coloneqq coker(\Theta)$ (see Section 3 of [op.cit.](#HamanakaKono2003) for the definition of $\Theta$):

$$
  1 \to N_n (X) \to U_n(X) \to \tilde{K}^1 (X) \to 1
  \,.
$$

=--

In particular, Prop. \ref{LimitToKtheory} shows that in general $U_n(X)$ is neither abelian nor does it [[injection|inject]] into $\tilde{K}^1 (X)$.

+-- {: .num_defn #LimitToKtheory}
###### Proposition
(Theorem 1.2 of [op.cit.](#HamanakaKono2003)) 

For $dim(X)\leq 2n$, the [[cokernel]] group $N_n(X)$ is a [[finite group|finite]] [[abelian group]] where the order of any element divides $n!$.

=--

An example where not only do the unstable and stable K theory groups not coincide but the latter actually vanishes is provided by the even-dimensional [[sphere|spheres]].

+-- {: .num_defn #LimitToKtheory}
###### Proposition
(Lemma 4.1 of [Hamanaka 2003](#Ham03)) 

For $n\geq 3$, the $n$ unstable K-theory group of the $2n$-dimensional sphere $S^{2n}$ is

$$
U_n (S^{2n} ) = \mathbb{Z}/ n!\mathbb{Z},
$$

whereas $\tilde{K}^1 (S^{2n} ) =0$.

=--


## Related concepts

* [[topological K-theory]]

* [[unstable Cohomotopy]]

* [[D-brane charge quantization in K-theory]]


## References

On unstable [[topological K-theory]]:

* {#HamanakaKono2003} [[Hiroaki Hamanaka]], [[Akira Kono]]: *On $[X, U(n)]$ when $\text{dim}(X)$ is $2n$*, Journal of Mathematics of Kyoto University **43** 2 (2003) 333-348 &lbrack;[doi:10.1215/kjm/1250283730](https://doi.org/10.1215/kjm/1250283730)&rbrack;

* {#Ham03} [[Hiroaki Hamanaka]]: *Adams $ e $-invariant, Toda bracket and $[X, U (n)]$*, Journal of Mathematics of Kyoto University **43** 4 (2003) 815-827 &lbrack;[doi:10.1215/kjm/1250281737](https://doi.org/10.1215/kjm/1250281737)&rbrack;

* {#HamanakaKono2004} [[Hiroaki Hamanaka]], [[Akira Kono]]: *An application of unstable K-theory*, Journal of Mathematics of Kyoto University **44** 2 (2004) 451-456 &lbrack;[doi:10.1215/kjm/1250283560](https://doi.org/10.1215/kjm/1250283560)&rbrack;


On unstable [[algebraic K-theory]]:

* {#vdKallen1980} Wilberd van der Kallen: *Homology stability for linear groups*,  Invent Math **60** (1980) 269--295 \[<a href="https://doi.org/10.1007/BF01390018">doi:10.1007/BF01390018</a>\]

* [[Soren Galatius]], [[Alexander Kupers]], [[Oscar Randal-Williams]]: *$E_\infty$-cells and general linear groups of infinite fields*, Duke Math. J. **174** 14  (2025) 2927--3046 &lbrack;[arXiv:2005.05620](https://arxiv.org/abs/2005.05620)&rbrack;


* {#ClausenJansen2024} [[Dustin Clausen]], Mikala Ørsnes Jansen: *The reductive Borel-Serre compactification as a model for unstable algebraic K-theory*, Sel. Math. New Ser. **30** 10 (2024) &lbrack;[arXiv:2108.01924 math.KT](https://arxiv.org/abs/2108.01924), [doi:10.1007/s00029-023-00900-8](https://doi.org/10.1007/s00029-023-00900-8)&rbrack;

* {#Jansen24} Mikala Ørsnes Jansen: *Unstable algebraic K-theory: homological stability and other observations* &lbrack;[arXiv:2405.02065](https://arxiv.org/abs/2405.02065)&rbrack;


[[!redirects unstable topological K-theory]]

[[!redirects unstable algebraic K-theory]]
