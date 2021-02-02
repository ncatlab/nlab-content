
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

An _[[embedding]] of [[topological spaces]]_ is a [[continuous function]] which is a [[homeomorphism]] onto its [[image]].

## Definition

+-- {: .num_defn #EmbeddingOfTopologicalSpaces}
###### Definition
**(embedding of topological spaces)**

Let $(X,\tau_X)$ and $(Y,\tau_Y)$ be [[topological spaces]]. A [[continuous function]] $f \;\colon\; X \longrightarrow Y$ is called an _embedding_ if  
in its [[image factorization]] 

$$
  f 
    \;\colon\;
  X
    \overset{\phantom{A}\simeq\phantom{A}}{\longrightarrow}
  f(X)
    \overset{\phantom{AAA}}{\hookrightarrow}
  Y
$$

with the [[image]] $f(X) \hookrightarrow Y$ equipped with the [[subspace topology]], we have that $X \to f(X)$ is a [[homeomorphism]].

=--

## Properties

+-- {: .num_prop #OpenClosedContinuousInjectionsAreEmbeddings}
###### Proposition
**([[closed injections are embeddings|open/closed continuous injections are embeddings]])**

A [[continuous function]] $f \colon (X, \tau_X) \to (Y,\tau_Y)$
which is

1. an [[injective function]]

1. an [[open map]] or a [[closed map]]

is an embedding (def. \ref{EmbeddingOfTopologicalSpaces}).

This is called a _closed embedding_ if the [[image]] $f(X) \subset Y$ is a [[closed subset]].

=--

+-- {: .proof}
###### Proof

If $f$ is injective, then the map onto its [[image]] $X \to f(X) \subset Y$ is a [[bijection]]. Moreover, it is still [[continuous function|continuous]] with respect to the [[subspace topology]] on $f(X)$. Now a bijective continuous function is a homeomorphism precisely if it is an [[open map]] or a [[closed map]] (by [this prop.](homeomorphism#HomeoContinuousOpenBijection)). But the image projection of $f$ has this property, respectively, if $f$ does (by [this prop.](open+map#OpenClosedImageProjection)).

=--


+-- {: .num_prop #TopologicalEmbeddingsAreTheRegularMonos} 
###### Proposition 

Embeddings of topological spaces are precisely the [[regular monomorphisms]] in the [[category]] [[Top]] of all [[topological spaces]]. 

=-- 

For **proof** see at _[[Top]]_ [this proposition](Top#MonoEpiMorphisms).


+-- {: .num_lemma #poclosed} 
###### Lemma 
In $Top$, the pushout $j$ of a (closed/open) embedding $i$ along any continuous map $f$, 

$$\array{
A & \stackrel{i}{\hookrightarrow} & B \\ 
\mathllap{f} \downarrow & po & \downarrow \mathrlap{g} \\ 
C & \underset{j}{\hookrightarrow} & D,
}$$ 

is again a (closed/open) embedding. 
=-- 

For **proof** see at _[[subspace topology]]_ [here](subspace+topology#pushout).


+-- {: .num_prop #InjectiveProperMapsAreEquivalentlyTheClosedEmbeddings}
###### Proposition
**(injective proper maps to locally compact spaces are equivalently the closed embeddings)**

Let 

1. $X$ be a [[topological space]] 

1. $Y$ a [[locally compact topological space]] 

1. $f \colon X \to Y$ be a [[continuous function]]. 

Then the following are equivalent

1. $f$ is an [[injective function|injective]] [[proper map]], 

1. $f$ is a closed embedding (def. \ref{EmbeddingOfTopologicalSpaces}).

=--

+-- {: .proof}
###### Proof

In one direction, if $f$ is an injective proper map, 
then since [[proper maps to locally compact spaces are closed]], it follows that $f$ is also  [[closed map]]. The claim then follows since [[closed injections are embeddings]], and since the image of a closed map is closed.

Conversely, if $f$ is a closed embedding, we only need to show that the embedding map is proper. So for $C \subset Y$ a [[compact subspace]], we need to show that the [[pre-image]] $f^{-1}(C) \subset X$ is also compact. But since $f$ is an injection (being an embedding), that pre-image is just the intersection $f^{-1}(C) \simeq C \cap f(X)$. 

To see that this is compact, let $\{V_i \subset X\}_{i \in I}$ be an open cover of the subspace $C \cap f(X)$,
hence, by the nature of the [[subspace topology]], let $\{U_i \subset Y\}_{i \in I}$ be a set of open subsets of
$Y$, which cover $C \cap f(X) \subset Y$ and with $V_i$ the restriction of $U_i$ to $C \cap f(X)$.
Now since $f(X) \subset Y$ is closed by assumption, it follows that the complement $Y \setminus f(X)$ is open
and hence that

$$
  \{ U_i \subset Y \}_{i \in  I} \sqcup \{ Y \setminus f(X) \}
$$

is an open cover of $C \subset Y$. By compactness of $C$ this has a finite subcover. Since restricting that
finite subcover back to $C \cap f(X)$ makes the potential element $Y \setminus f(X)$ disappear, this
restriction is a finite subcover of $\{V_i \subset C \cap f(X)\}$. This shows that $C \cap f(X)$ is compact.

=--



## Related concepts

* [[embedding]]

* [[embedding of smooth manifolds]]

[[!redirects embeddings of topological spaces]]

[[!redirects topological embedding]]
[[!redirects topological embeddings]]

[[!redirects topological subspace embedding]]
[[!redirects topological subspace embeddings]]

[[!redirects closed embedding of topological spaces]]
[[!redirects closed embeddings of topological spaces]]
