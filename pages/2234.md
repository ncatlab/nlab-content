
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


