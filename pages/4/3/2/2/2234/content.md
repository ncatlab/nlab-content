
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Definition

\begin{definition}\label{CentralizerSubgroup}
Given a [[group]] $G$ and a [[subset]] $S \,\subset\, G$ of its [[underlying]] [[set]], 
the *centralizer subgroup* (also: the *[[commutant]]*) of $S$ in $G$ is the [[subgroup]] 

$$
  C_G(S) 
  \;\coloneqq\;
  \big\{
    g \in G 
    \,\vert\,
    \underset{s \in S}{\forall}
    (
      g \cdot s \,=\, s \cdot g
    )
  \big\}
  \;\subset\;
  G
$$ 

of all [[elements]] $c \in G$ which commute with the elements of $S$.
\end{definition}

Equivalently, the centralizer is the joint [[fixed point subgroup]] of the [[inner automorphisms]] on $G$ given by [[conjugation action|conjugation]] with the elements $s \in S$. 

Notice the similarity with but the difference to the concept of _[[normalizer subgroup]]_, cf. Prop. \ref{RelationToNormalizer}.


## Properties

\begin{proposition}\label{RelationToNormalizer}
Given a [[subset]] $S \subset G$ of a [[group]] $G$,
the *centralizer subgroup* of $S$ (Def. \ref{CentralizerSubgroup})
is a [[subgroup]] of the [[normalizer subgroup]]:

$$
  C_G(S)
  \;
  \subset
  \;
  N_G(S)
  \,.
$$
\end{proposition}
\begin{proof}
  Since an element $g \in G$ which fixes each element $s \in S$ separately
  already fixes the entire subset as such:
  $$
    \underset{s \in S}{\forall}
    \big(
      g \cdot s
      \,=\,
      s \cdot g 
    \big)
    \;\;\;\;\;
    \Rightarrow
    \;\;\;\;\;
    \big(
      g \cdot S
      \,=\,
      S \cdot g 
    \big)
    \,.
  $$
\end{proof}

\begin{prop}\label{CentralizersInT1GroupsAreClosed}
**(centralizers in [[T1-space|$T_1$]]-[[topological group|groups]] are [[closed subgroup|closed]])** 
\linebreak
  If $G$ is a [[T1-space|$T_1$]]-[[topological group]], then all its centralizer subgroups are [[closed subgroups]].
\end{prop}
\begin{proof}
  First consider a [[singleton set]]  $S = \{s\}$.
  By definition, the centralizer of a single element $s \in G$ is the [[preimage]] of itself under the [[function]]
  $$
    \array{
      G &\xrightarrow{\;\;}& G
      \\
      g &\mapsto& g \cdot s \cdot g^{-1}
      \,.
    }
  $$
  (the [[adjoint action]] of $G$ on itself).

Noticing here that:

1. this is [[continuous function]], by the axioms on a topological group;

1. $\{s\} \subset G$ is a [[closed subset]], by the assumption that $G$ is a [[T1-space|$T_1$-space]] (by [this Prop.](separation+axioms#T1InTermsOfClosureOfPoints))

it follows that $C_G(\{s\}) \subset G$ is the continuous [[preimage]] of a [[closed subset]] and hence is itself closed (by [this Prop.](Introduction+to+Topology+--+1#ClosedSubsetContinuity)).

Now for a general set $S$, its centralizer is clearly the [[intersection]] of the centralizers of (the [[singleton sets]] on) its elements:

$$
  C_G(S) 
    \;=\; 
  \underset{
    s \in S
  }{\cap}
  C_G\big(\{s\}\big)
 \,.
$$

Since each of the factors on the right isclosed, by the previous argument, the general centralizer subgroup is an [[intersection]] of [[closed subsets]] and hence itself a closed subset.
\end{proof}


## Examples

### In homotopy long exact sequences
 {#ExampleInHomotopyLES}

Consider a [[path-connected topological space]] $X$ admitting the [[structure]] of a [[CW-complex]].

Fixing any [[base points]] $0 \in X$ and $0 \in S^1$,
we will be concerned with the *[[free loop space]]*
$$
  \mathcal{L}
  X
  \coloneqq
  \mathrm{Map}({
    S^1, 
    X
  })
$$
and the *[[based loop space]]*
$$
  \Omega
  X
  \coloneqq
  \mathrm{Map}^\ast({
    S^1, 
    X
  })
  \mathrlap{\,.}
$$

Their [[sets]] of [[connected components]] are
the *[[fundamental group]] of $X$
$$
  G
  \coloneqq
  \pi_1(X)
  \equiv
  \pi_0({\Omega X})
$$
and its set of [[conjugacy classes]]: 
$$
  \mathrm{Conj}(G)
  \simeq
  \pi_0({\mathcal{L}X})
  \mathrlap{\,.}
$$

\begin{proposition}\label{CentralizerInHomotopyLES}
  In every [[connected component]] $[g] \in \mathrm{Conj}(G) \simeq \pi_0(\mathcal{L}X)$, the [[image]] of $\pi_1({\mathcal{L}X})$ in $G$ is the centralizer group of $g$:
  \[
    \label{ImageOfTopologicalMonodromyInG}
    \pi_1(\mathrm{ev})
    \big({
      \pi_1({
        \mathcal{L}X
      })
    }\big)
    \simeq
    C_G(g)
    \subset 
    G
    \mathrlap{\,.}
  \]
  Moreover, when $X$ has trivial $\pi_2$, then $\pi_1({\mathcal{L}X})$ is isomorphic to the centralizer 
  \[
    \label{ParameterMonodromyCoindicingWithCentralizer}
    \mathllap{
    \pi_2(X) \simeq \ast
    \;\;\;\;\;
    \Rightarrow
    \;\;\;\;\;
    }
    \pi_1({
      \mathcal{L}X
    })
    \simeq
    C_G(g)
    \mathrlap{\,.}
  \]
\end{proposition}
\begin{proof}
Consider any loop $\gamma \in \Omega X$ which represents the conjugacy class $[g]$: 

\begin{tikzcd}[sep=0pt]
    G
    \ar[rr, "{ \sim }"]
    &&
    \pi_0({\Omega X})
    \ar[rr]
    &&
    \pi_0({
      \mathcal{L}X
    })
    \ar[rr, "{ \sim }"]
    &&
    \mathrm{Conj}(G)
    \\
    g
    &\leftrightarrow&
    {[\gamma]}
    &\mapsto&
    {[\gamma]} 
      &\leftrightarrow& 
    {[g]}
    \mathrlap{\,,}
\end{tikzcd}


and with that used as the base point, consider the homotopy long exact sequence 
induced by the map $\mathrm{ev}$ that evaluates a loop at its base point:
$$
  \Omega X
  \longrightarrow
  \mathcal{L}X
  \xrightarrow{\phantom{-} ev \phantom{-}}
  X
  \mathrlap{\,,}
$$
of this form:

\begin{imagefromfile}
    "file_name": "CentralizerInHomotopyLES.png",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

On the right we are claiming that the [[connecting homomorphism]] $\partial$ [[conjugation action|acts by conjugation]] on $g \in G$. To see this, recall that $\partial$ is generally given on the class of a based loop $\ell \in P_0 X$ by first lifting it through $\mathrm{ev}$ to a based path $\widehat \ell \in P_{[g]} \mathcal{L}X$ and then evaluating that at its endpoint:
$$
  \partial({[\ell]})
  =
  \big[{\widehat{\ell}_1}\big]
  \mathrlap{\,.}
$$
Here we may take $\widehat{\ell}$ to be given by 
$$
  \widehat{\ell}_t
  \coloneqq
  \mathrm{conc}\big({
    \overline{\ell}(t-),
    \gamma, 
    \ell(t-)
  }\big)
$$
(where "$\mathrm{conc}$" denotes [[concatenation]] and an overline denotes reversal of paths $[0,1] \to X$), which implies the above equality of exact sequences.

From this, the first claim (eq:ImageOfTopologicalMonodromyInG) follows by [[exact sequence|exactness]]: The [[image]] of $\pi_1(\mathrm{ev})$ is now identified with the [[kernel]] of $\mathrm{Ad}_{(-)}(g)$, and that is the centralizer $C_G(g)$, by definition. (Beware here that the copy of "$G$" in the bottom right above is the [[underlying set]] of the group, pointed by the element $g$.)

Similarly for the second claim (eq:ParameterMonodromyCoindicingWithCentralizer): If $\pi_2(X) = \pi_1(\Omega X)$ is trivial, then exactness gives that $\pi_1(\mathrm{ev})$ is [[injective]] and hence an [[isomorphism]] onto its image.
\end{proof}

\begin{example}
Given any group $G$, we may consider the [[Eilenberg-MacLane space]] $X \coloneqq K(G,1)$. By definition, this has $\pi_1(X) \simeq G$ and $\pi_2(X) \simeq \ast$, and hence Prop. \ref{CentralizerInHomotopyLES} gives that the centralizers of elements of $G$ are obtained as the fundamental groups
$
  \pi_1\big( \mathcal{L}X, \gamma \big)
  \simeq
  C_G(g)
  \mathrlap{\,.}
$
\end{example}



## Related concepts

* [[stabilizer subgroup]]

* [[normalizer subgroup]]

## References

See also:

* Wikipedia: _[Centralizer and normalizer](https://en.wikipedia.org/wiki/Centralizer_and_normalizer)_

[[!redirects centralizers]]

[[!redirects centralizer group]]
[[!redirects centralizer groups]]

[[!redirects centralizer subgroup]]
[[!redirects centralizer subgroups]]


