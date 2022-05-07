[[!redirects coset space coprojections admitting local sections]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[topological group]] $G$ and a [[subgroup]] $H \subset G$ it is often oft interest to known that the [[coset space]] [[coprojection]] $G \to G/H$ admits [[local sections]]. For instance, these yield canonical examples of $H$-[[principal bundles]], of [[G-structure|H-structures]] and of [[equivariant bundles]].

## Recognition

\begin{prop}\label{SufficientConditionsforCosetSpaceCoprojectionsHavingLocalSections}
**(sufficient conditions for coset space coprojections having local sections)**\linebreak
Let $G$ be a [[topological group]] and $H \subset G$ a [[subgroup]].

Then sufficient conditions for the [[coset space]] [[coprojection]] $G \overset{q}{\to} G/H$ to admit [[local sections]], in that there is an [[open cover]] $\underset{i \in I}{\sqcup}U_i \to G/H$ and a [[continuous section]] $\sigma_{\mathcal{U}}$ of the [[pullback]] of $q$ to the cover,

$$
  \array{
    &&
    G_{\vert \mathcal{U}}
    &\longrightarrow&
    G
    \\
    &
    {}^{\mathllap{
      \exists \sigma
    }}
    \nearrow
    &
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow 
    \\
    \mathllap{ \exists \; } 
    \underset{i \in I}{\sqcup} U_i    
    &=&
    \underset{i \in I}{\sqcup} U_i
    &\longrightarrow&
    G/H
    \mathrlap{\,,}
  }
$$

include the following:


* $G$ is any [[topological group]] 

  and $H$ is a [[compact Lie group]]

  ([Gleason 50, Thm. 4.1](#Gleason50))

  \linebreak

or:

* $G$ is a [[locally compact topological groups]]

  which is moreover a [[separable metric space]] of [[finite number|finite]] [[dimension of a separable metric space|dimension]]

  and $H \subset G$ is a [[closed subgroup]].

  ([Mostert 53, Theorem 3](#Mostert53), see also [Karube 58, Theorem 2](#Karube58))

\end{prop}

\begin{example}
  A common special case of either condition in Prop. \ref{SufficientConditionsforCosetSpaceCoprojectionsHavingLocalSections} is:

* $G$ is a [[compact Lie group]]

  and $H$ is a [[closed subgroup]].

(This is a special case of Gleason's condition since [[Lie groups]] are [[Hausdorff spaces]] and [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]].)


\end{example}

## Counter examples
 {#Counterexamples}

Examples of quotient coprojections $ G \to G/H$ *without* local sections are given in [Karube 58, Sec. 3](#Karube58).



## Related concepts

* [[coset space]]

* [[principal bundle]]

* [[G-structure]]

* [[equivariant bundle]]

## References

* {#Samelson41} [[Hans Samelson]], _Beiträge zur Topologie der Gruppenmannigfaltigkeiten_, Ann. of Math. 2, 42, (1941), 1091 - 1137. ([jstor:1970463](https://www.jstor.org/stable/1970463), [doi:10.2307/1970463](https://doi.org/10.2307/1970463))


* {#Gleason50} [[Andrew Gleason]], _Spaces With a Compact Lie Group of Transformations_, Proceedings of the American Mathematical Society Vol. 1, No. 1 (Feb., 1950), pp. 35-43 ([jstor:2032430](https://www.jstor.org/stable/2032430), [doi:10.2307/2032430](https://doi.org/10.2307/2032430))

* {#Mostert53} [[Paul Mostert]], _Local Cross Sections in Locally Compact Groups_, Proceedings of the American Mathematical Society, Vol. 4, No. 4 (Aug., 1953), pp.645-649 ([jstor:2032540](https://www.jstor.org/stable/2032540), [doi:10.2307/2032540](https://doi.org/10.2307/2032540))

* {#Karube58} Takashi Karube, _On the local cross-sections in locally compact groups_,  J. Math. Soc. Japan 10(4): 343-347 (October, 1958) ([doi:10.2969/jmsj/01040343](https://projecteuclid.org/journals/journal-of-the-mathematical-society-of-japan/volume-10/issue-4/On-the-local-cross-sections-in-locally-compact-groups/10.2969/jmsj/01040343.full))

[[!redirects coset space coprojections with local sections]]

