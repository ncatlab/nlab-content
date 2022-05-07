
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

In _[[algebraic topology]]_ by a _CW-pair_ $(X,A)$ is meant a [[CW-complex]] $X$ equipped with a sub-complex inclusion $A \hookrightarrow X$.

The concept appears prominently in the discussion of [[ordinary homology|ordinary]] [[relative homology]] and generally in the [[Eilenberg-Steenrod axioms]] for [[generalized homology]]/[[generalized cohomology]].

## Properties

+-- {: .num_prop }
###### Proposition

For $X$ a [[CW complex]], the inclusion $A \hookrightarrow X$ of any subcomplex has an [[open neighbourhood]] in $X$ which is a [[deformation retract]] of $A$. In particular such an inclusion is a _[good pair](relative+homology#GoodPair)_ in the sense of [[relative homology]].

=--

For instance ([Hatcher, prop. A.5](#Hatcher)).

+-- {: .num_prop #HomologyOfQuotientSpace}
###### Proposition

For $(X,A)$ a CW-pair, then the $A$-[[relative singular homology]] of $X$ coincides with the [[reduced singular homology]] of the [[quotient space]] $X/A$: 

$$
  H_n(X , A)
  \simeq
  \tilde H_n(X/A)
 \,.
$$

=--

For instance ([Hatcher, prop. 2.22](#Hatcher)).

+-- {: .proof}
###### Proof

By assumption we can find a [[neighbourhood]] $A \stackrel{j}{\to} U \hookrightarrow X$ such that $A \hookrightarrow U$ has a [[deformation retract]] and hence in particular is a [[homotopy equivalence]] and so induces also isomorphisms on all [[singular homology]] groups. 

It follows in particular that for all $n \in \mathbb{N}$ the canonical morphism $H_n(X,A) \stackrel{H_n(id,j)}{\to} H_n(X,U)$ is an [[isomorphism]], by [homotopy invariance](relative+homology#HomotopyInvariance) of [[relative singular homology]].

Given such $U$ we have an evident [[commuting diagram]] of pairs of [[topological spaces]]

\begin{center}
    \begin{tikzcd}
        {(X,A)} \arrow[r, "{(\mathrm{id}, j)}"] \arrow[d] & {(X,U)} \arrow[d] & {(X - A, U - A)} \arrow[l] \arrow[d, "\simeq"] \\
        {(X/A, A/A)} \arrow[r, "{(\mathrm{id}, j/A)}"]    & {(X/A, U/A)}      &{(X/A-A/A, U/A- A/A)} \arrow[l]     
        \end{tikzcd}
\end{center}

Here the right vertical morphism is in fact a [[homeomorphism]].

Applying relative singular homology to this diagram yields for each $n \in \mathbb{N}$ the [[commuting diagram]] of abelian groups

\begin{center}
    \begin{tikzcd}
        {H_n(X,A)} \arrow[r, "{H_n(\mathrm{id}, j)}", "\simeq"'] \arrow[d] & {H_n(X,U)} \arrow[d] & {H_n(X - A, U - A)} \arrow[l, "\simeq"'] \arrow[d, "\simeq"] \\
        {H_n(X/A, A/A)} \arrow[r, "{H_n(\mathrm{id}, j/A)}", "\simeq"']    & {H_n(X/A, U/A)}      &{H_n(X/A-A/A, U/A- A/A)} \arrow[l, "\simeq"']     
        \end{tikzcd}
\end{center}

Here the left horizontal morphisms are the above isomorphims induced from the deformation retract. The right horizontal morphisms are isomorphisms by [excision](relative%20homology#Excision) and the right vertical morphism is an isomorphism since it is induced by a homeomorphism. Hence the left vertical morphism is an isomorphism ([[2-out-of-3]] for isomorphisms).

=--

## References

* {#Hatcher} [[Allen Hatcher]], _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_, 2002
  
* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 5.1 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc 
pdf](http://pi.math.cornell.edu/~hatcher/AT/AT.pdf))

[[!redirects CW-pairs]]

[[!redirects CW pair]]
[[!redirects CW pairs]]
