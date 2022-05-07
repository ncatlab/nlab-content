
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The *simplicial identities* encode the relationships between the face and degeneracy maps in a [[simplicial object]], in particular, in a [[simplicial set]].

## Definition

The **simplicial identities** are the duals to the _simplicial relations_  of coface and codegeneracy maps described at [[simplex category]]:

Let $S \in $ [[sSet]] with

* face maps  $\partial_i : S_n \to S_{n-1}$ obtained by omitting the $i$th vertex;

* degeneracy maps $s_i : S_n \to S_{n+1}$ obtained by repeating the $i$th vertex.


+-- {: .num_defn #SimplicialIdentities}
###### Definition

The **simplicial identities** satisfied by face and degeneracy maps as above are (whenever these maps are composable as indicated):

$$
\array{
  \partial_i 
    \circ 
  \partial_j  
  \;=\; 
  \partial_{j-1} 
    \circ 
  \partial_i
  & 
  \text{if}
  & 
  i \lt j
  \\
  s_i 
    \circ 
  s_j  
  \;=\; 
  s_j 
    \circ 
  s_{i-1} 
  &
  \text{if} 
  &
  i \gt j
}
$$

$$
  {\phantom{AAAAA}}
  \partial_i 
    \circ 
  s_j 
  \;=\;  
  \left\{ 
    \array{ 
      s_{j-1} 
        \circ 
      \partial_i 
      &  
      \text{if} 
      &  
      i \lt j 
      \\ 
      id 
      & 
      \text{if}
      &  
      i \in \{j, j+1\} 
      \\ 
      s_j 
        \circ 
      \partial_{i-1} 
      &  
      \text{if} 
      &
      i \gt j+1 
    } 
  \right. 
$$

=--

(e.g. [Goerss & Jardine 1999/2009, I.1. (1.3)](#GoerssJardine09))

## Properties

### Relation to nilpotency of differentials
 {#RelationToNilpotencyOfDifferentials}

The simplicial identities of def. \ref{SimplicialIdentities} can be understood as a non-abelian or "unstable" generalization of the identity

$$
  \partial \circ \partial = 0
$$

satisfied by [[differentials]] in [[chain complexes]] (in [[homological algebra]]). 

Write $\mathbb{Z}[S]$ be the [[simplicial abelian group]] obtained form $S$ by forming degreewise the [[free abelian group]] on the set of $n$-simplices, as discussed at _[[chains on a simplicial set]]_.

Then using these [[formal linear combinations]] we can sum up all the $(n+1)$ face maps $\partial_i : S_n \to S_{n-1}$ into a single map:

+-- {: .num_defn #TheAlternatingFaceMapDifferential}
###### Definition

The **alternating face map differential** in degree $n$ of the simplicial set $S$ 
is the linear map 

$$
  \partial : \mathbb{Z}[S_n] \to \mathbb{Z}[S_{n-1}]
$$ 

defined on [[basis]] elements $\sigma \in S_n$ to be the alternating sum of the simplicial face maps:

\[
  \label{AlternatingFaceMapDifferential}
  \partial \sigma \coloneqq \sum_{k = 0}^n (-1)^k \partial_k \sigma
  \,.
\]

=--

This is the [[differential]] of the _[[alternating face map complex]]_ of $S$:

+-- {: .num_prop }
###### Proposition

The simplicial identity def. \ref{SimplicialIdentities} (1) implies that def. \ref{TheAlternatingFaceMapDifferential} indeed defines a [[differential]] in that $\partial \circ \partial = 0$.

=--

+-- {: .proof}
###### Proof

By linearity, it is sufficient to check this on a basis element $\sigma \in S_n$. There we compute as follows:

$$
  \begin{aligned}
    \partial \partial \sigma
    & = 
    \partial \left(
      \sum_{j = 0}^n (-1)^j \partial_j \sigma
    \right)
    \\
    & =
    \sum_{j=0}^n \sum_{i = 0}^{n-1} (-1)^{i+j} \partial_i \partial_j \sigma
    \\
     & =
     \sum_{0 \leq i \lt j \leq n} (-1)^{i+j} \partial_i \partial_j \sigma
     + 
     \sum_{0 \leq j \leq i \lt n} (-1)^{i + j} \partial_i \partial_j \sigma
     \\
     & = 
     \sum_{0 \leq i \lt j \leq n} (-1)^{i+j} \partial_{j-1} \partial_i \sigma
     + 
     \sum_{0 \leq j \leq i \lt n} (-1)^{i + j} \partial_i \partial_j \sigma
     \\
     & = 
     - 
     \sum_{0 \leq i \leq j \lt n} (-1)^{i+j} \partial_{j} \partial_i \sigma
     + 
     \sum_{0 \leq j \leq i \lt n} (-1)^{i + j} \partial_i \partial_j \sigma
     \\
     & = 0
  \end{aligned}
  \,.
$$

Here 

1. the first equality is (eq:AlternatingFaceMapDifferential);

1. the second is (eq:AlternatingFaceMapDifferential) together with the linearity of $d$;

1. the third is obtained by decomposing the sum into two summands;

1. the fourth finally uses the simplicial identity def. \ref{SimplicialIdentities} (1) in the first summand;

1. the fifth relabels the summation index $j$ by $j +1$;

1. the last one observes that the resulting two summands are negatives of each other.

=--

## Related concepts

* [[simplicial map]]

## References

For original references see at *[[simplicial set]]*.

Review includes:

* {#May67} [[Peter May]], Def. 1.1 in: _Simplicial objects in algebraic topology_, University of Chicago Press 1967 ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]])

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Eq. (1.3) in Section I.1 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))


[[!redirects simplicial identity]]