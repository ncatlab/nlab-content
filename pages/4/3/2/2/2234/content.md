
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

Notice the similarity with but the difference to the concept of _[[normalizer subgroup]]_, see Prop. \ref{RelationToNormalizer}.


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
      g &\mapsto& g \cdot s
      \,.
    }
  $$
  Noticing here that

1. this is [[continuous function]] by the axioms on a topological group;

1. $\{s\} \subset G$ is a [[closed subset]], by the assumption that $G$ is a [[T1-space|$T_1$-space]] (by [this Prop.](separation+axioms#T1InTermsOfClosureOfPoints))

it follows that $C_G(\{s\}) \subset G$ is the continuous [[preimage]] of a [[closed subset]] and hence is itself closed (by [this Prop.](Introduction+to+Topology+--+1#ClosedSubsetContinuity)).

Now for a general set $S$, its centralizer is clearly the [[intersection]] of the centralizers of (the [[singleton sets]] on) its elements:

$$
  C_G(S) 
    \;=\; 
  \underset{
    s \in S
  }{\cap}
  C_G(\{s\})
 \,.
$$

Since each of the factors on the right isclosed, by the previous argument, the general centralizer subgroup is an [[intersection]] of [[closed subsets]] and hence itself a closed subset.
\end{proof}

## Related concepts

* [[stabilizer subgroup]]

* [[normalizer subgroup]]

## References

See also 

* Wikipedia, _[Centralizer and normalizer](https://en.wikipedia.org/wiki/Centralizer_and_normalizer)_

[[!redirects centralizers]]

[[!redirects centralizer group]]
[[!redirects centralizer groups]]

[[!redirects centralizer subgroup]]
[[!redirects centralizer subgroups]]


