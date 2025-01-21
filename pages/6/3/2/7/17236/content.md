
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

In _[[algebraic topology]]_, by a _CW-pair_ $(X,A)$ is meant a [[CW-complex]] $X$ equipped with a sub-complex inclusion $A \hookrightarrow X$.

The concept appears prominently in the discussion of [[ordinary homology|ordinary]] [[relative homology]] and generally in the [[Eilenberg-Steenrod axioms]] for [[generalized homology]]/[[generalized cohomology]].


## Properties

### General

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

### Collapsing contractible subcomplexes
 {#CollapsingContractibleSubcomplexes}

\begin{proposition}\label{Pinching}
  If the sub-complex $A$ is [[contractible homotopy type|contractible]], then the [[topological quotient space|quotient]] [[coprojection]] is a [[homotopy equivalence]].

$$
  \ast \overset{\sim}{\longrightarrow} A
  \phantom{---}
  \Rightarrow
  \phantom{---}
  X \overset{\sim}{\longrightarrow} X/A
  \,.
$$
\end{proposition}
(e.g. [Hatcher](#Hatcher) [p 11](https://pi.math.cornell.edu/~hatcher/AT/AT.pdf#page=20)).

\begin{example}
  Let  $X$ be the [[pushout]] (in [[Top]]) which attaches an arc --- identified as $A \subset X$ --- to the [[2-sphere]], connecting a pair of distinct points:

\begin{imagefromfile}
    "file_name": "PinchingSphereAtTwoPoints.png",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Hatcher](#Hatcher)"
\end{imagefromfile}


\begin{tikzcd}
  &
  S^0 
  \ar[r, hook] 
  \ar[d, hook]
  \ar[
    dr, 
    phantom, 
    "{ \mbox{ (po) } }"{pos=.8,gray, scale=.7}
  ]
    & 
    S^2
  \ar[d, hook]
  \\
  &
  \mathllap{ A := \, }
  D^1 
  \ar[r]
  &
  X
\end{tikzcd}

and let $B$ be any arc *inside* $S^2$ connecting these two distinct points. Then Prop. \ref{Pinching} gives homotopy equivalences

$$
  S^2 / S^0
  \,=\,
  X/A
  \overset{\sim}{\longrightarrow}
  X
  \overset{\sim}{\longrightarrow}
  X/B
  \,=\,
  S^2 \vee S^1
  \,.
$$

\end{example}
(e.g. [Hatcher](#Hatcher) [p 11](https://pi.math.cornell.edu/~hatcher/AT/AT.pdf#page=20)).

In generalization of this example:

\begin{example}
  For $\Sigma^2_{g,n}$ the result of equipping a [[closed manifold|closed]] [[surface]] $\Sigma^2_g$ with $n \geq 2$ [[punctures]], the [[one-point compactification]] $\big(\Sigma^2_{g,n}\big)^\ast$ is [[homotopy equivalence|homotopy equivalent]] to the [[wedge sum]] of the original surface with $n-1$ [[circles]]:

$$
  \big(\Sigma^2_{g,n}\big)^\ast
  \;\simeq\;
  \Sigma^2_g \,\vee\, \textstyle{\bigvee_{n-1}} S^1
  \,.
$$

\end{example}



## References

* {#Hatcher} [[Allen Hatcher]]: *[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)* (2002)
 
* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 5.1 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://pi.math.cornell.edu/~hatcher/AT/AT.pdf))

[[!redirects CW-pairs]]

[[!redirects CW pair]]
[[!redirects CW pairs]]
