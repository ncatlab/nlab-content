
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



#Contents#
* table of contents
{:toc}

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

one may think of this as a [[stabilization]] of generalized [[nonabelian cohomology]] theories (in the sense of [FSS23, §2](nonabelian+cohomology#FSS20)) $U_n(X)$ whose classifying spaces are the [[unitary groups]] $U(n)$. For this reason, we may call the groups $[X,U(n)] \,\coloneqq\, \pi_0 Map\big(X,U(n)\big)$ the **unstable** $\tilde{K}^1$-theory groups of $X$, at stage $n$.


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

The following properties are proven in [Hamanaka and Kono 2003](#HK03):

+-- {: .num_defn #LimitToKtheory}
###### Proposition
(Theorem 1.1 of [op.cit.](#HK03)) 
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

or, put differently, defining $N_n (X) \coloneqq coker(\Theta)$ (see Section 3 of [op.cit.](#HK03) for the definition of $\Theta$):

$$
  1 \to N_n (X) \to U_n(X) \to \tilde{K}^1 (X) \to 1
  \,.
$$

=--

In particular, Prop. \ref{LimitToKtheory} shows that in general $U_n(X)$ is neither abelian nor does it [[injection|inject]] into $\tilde{K}^1 (X)$.

+-- {: .num_defn #LimitToKtheory}
###### Proposition
(Theorem 1.2 of [op.cit.](#HK03)) 

For $dim(X)\leq 2n$, the [[cokernel]] group $N_n(X)$ is a [[finite group|finite]] [[abelian group]] where the order of any element divides $n!$.

=--

## Related concepts

* [[topological K-theory]]

* [[unstable Cohomotopy]]

## References

* {#HK03} [[Hiroaki Hamanaka]], [[Akira Kono]]: *On $[X, U(n)]$ when $\text{dim}(X)$ is $2n$*, Journal of Mathematics of Kyoto University **43** 2 (2003) 333-348 &lbrack;[doi:10.1215/kjm/1250283730](https://doi.org/10.1215/kjm/1250283730)&lbrack;

* [[Hiroaki Hamanaka]], [[Akira Kono]]: *An application of unstable K-theory*, Journal of Mathematics of Kyoto University **44** 2 (2004) 451-456 &lbrack;[doi:10.1215/kjm/1250283560](https://doi.org/10.1215/kjm/1250283560)&rbrack;

* [[Hiroaki Hamanaka]]: *Adams $ e $-invariant, Toda bracket and $[X, U (n)]$*, Journal of Mathematics of Kyoto University **43** 4 (2003) 815-827 &lbrack;[doi:10.1215/kjm/1250281737](https://doi.org/10.1215/kjm/1250281737)&rbrack;


[[!redirects unstable topological K-theory]]
