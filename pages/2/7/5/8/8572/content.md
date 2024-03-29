
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### In singular homology

Let $X$ be a [[topological space]] and $A \hookrightarrow X$ a [[subspace]]. Write $C_\bullet(X)$ for the [[chain complex]] of [[singular homology]] on $X$ and $C_\bullet(A) \hookrightarrow C_\bullet(X)$ for the [[chain map]] induced by the subspace inclusion. 

+-- {: .num_defn}
###### Definition

The [[cokernel]] of this inclusion, hence the [[quotient]] $C_\bullet(X)/C_\bullet(A)$ of $C_\bullet(X)$ by the [[image]] of $C_\bullet(A)$ under the inclusion, is the **chain complex of $A$-relative singular chains**. 

* A [[boundary]] in this quotient is called an **$A$-relative singular boundary**, 

* a [[cycle]] is called an **$A$-relative singular cycle**.

* The [[chain homology]] of the quotient is the **$A$-relative singular homology of $X$**

  $$
    H_n(X , A)\coloneqq H_n(C_\bullet(X)/C_\bullet(A))
    \,.
  $$

=--

+-- {: .num_remark}
###### Remark

This means that a singular $(n+1)$-chain $c \in C_{n+1}(X)$ is an $A$-relative cycle if its [[boundary]] $\partial c \in C_{n}(X)$ is, while not necessarily 0, contained in the $n$-chains of $A$: $\partial c \in C_n(A) \hookrightarrow C_n(X)$. So it vanishes only "up to contributions coming from $A$".

=--


## Properties


### Long exact sequences
 {#LongExactSequences}

+-- {: .num_prop #RelativeHomologyLongExactSequence}
###### Proposition

Let $A \stackrel{i}{\hookrightarrow} X$. The corresponding 
relative homology sits in a [[long exact sequence]] of the form

$$
  \cdots
  \to 
  H_n(A)
   \stackrel{H_n(i)}{\to}
  H_n(X)
  \to 
  H_n(X, A)
   \stackrel{\delta_{n-1}}{\to}
  H_{n-1}(A)
   \stackrel{H_{n-1}(i)}{\to}
  H_{n-1}(X)
  \to 
  H_{n-1}(X, A)
  \to 
  \cdots
  \,.
$$

The [[connecting homomorphism]] $\delta_{n} \colon H_{n+1}(X, A) \to H_n(A)$ sends an element $[c] \in H_{n+1}(X, A)$ represented by an $A$-relative cycle $c \in C_{n+1}(X)$, to the class represented by the [[boundary]] $\partial^X c \in C_n(A) \hookrightarrow C_n(X)$.

=--

+-- {: .proof}
###### Proof

This is the _[[homology long exact sequence]]_ induced by the given [[short exact sequence]] $0 \to C_\bullet(A) \stackrel{i}{\hookrightarrow} C_\bullet(X) \to coker(i)  \simeq C_\bullet(X)/C_\bullet(A)  \to 0$ of chain complexes.

=--

+-- {: .num_prop #RelativeTripleHomologyLongExactSequence}
###### Proposition

Let $B \hookrightarrow A \hookrightarrow X$ be a sequence of two inclusions. Then there is a [[long exact sequence]] of relative homology groups of the form

$$
  \cdots \to H_n(A , B) \to H_n(X , B) \to H_n(X , A ) \to H_{n-1}(A , B) \to \cdots
  \,.
$$

=--

+-- {: .proof}
###### Proof

Observe that we have a (degreewise) [[short exact sequence]] of chain complexes

$$
  0 \to C_\bullet(A)/C_\bullet(B) \to C_\bullet(X)/C_\bullet(B) \to C_\bullet(X)/C_\bullet(A) \to 0
  \,.
$$

The corresponding [[homology long exact sequence]] is the long exact sequence in question.

=--


### Excision
 {#Excision}

Let $Z \hookrightarrow A \hookrightarrow X$ be a sequence of [[topological subspace]] inclusions such that the [[closure]] $\bar Z$ of $Z$ is still contained in the [[interior]] $A^\circ$ of $A$: $\bar Z \hookrightarrow A^\circ$. 


+-- {: .num_prop #ExcisionA}
###### Proposition

In the above situation, the inclusion $(X-Z, A-Z) \hookrightarrow (X,A)$ induces [[isomorphism]] in relative singular homology groups

$$
  H_n(X-Z, A-Z) \stackrel{\simeq}{\to} H_n(X,A)
$$

for all $n \in \mathbb{N}$.

=--

Let $A,B \hookrightarrow X$ be two [[topological subspaces]] such that their [[interior]] is a [[cover]] $A^\circ \coprod B^\circ \to X$ of $X$. 

+-- {: .num_prop #ExcisionB}
###### Proposition

In the above situation, the inclusion $(B, A \cap B) \hookrightarrow (X,A)$ induces [[isomorphisms]] in relative singular homology groups

$$
  H_n(B, A \cap B) \stackrel{\simeq}{\to} H_n(X,A)
$$

for all $n \in \mathbb{N}$. 

=--

A proof is spelled out in ([Hatcher, from p. 128 on](#Hatcher)).

+-- {: .num_remark }
###### Remark

These two propositions are equivalent to each other. To see this identify
$B = X - Z$.

=--

### Homotopy invariance
 {#HomotopyInvariance}

+-- {: .num_defn #HomotopyInvariance}
###### Definition

Relative homology is homotopy invariant in both arguments.


=--

(...)

### Relation to reduced homology of quotient topological spaces
 {#RelationToQuotientTopologicalSpaces}

+-- {: .num_defn #GoodPair}
###### Definition

A [[topological subspace]] inclusion $A \hookrightarrow X$ is called a **good pair** if 

1. $A$ is [[closed subset|closed]] inside $X$;

1. $A$ has an [[neighbourhood]] in $X$ which is a [[deformation retract]] of $A$.

=--

+-- {: .num_example }
###### Example

For $X$ a [[CW complex]], the inclusion of any subcomplex $A \hookrightarrow X$ is a good pair (called a _[[CW-pair]]_ $(X,A)$).

=--

This is discussed at  _[CW complex -- Subcomplexes](CW+complex#Subcomplexes)_.




+-- {: .num_prop #HomologyOfQuotientSpace}
###### Proposition

If $A \hookrightarrow X$ is a [[topological subspace]] inclusion which is _good_ in the sense of def. \ref{GoodPair}, then the $A$-relative singular homology of $X$ coincides with the [[reduced singular homology]] of the [[quotient space]] $X/A$: 

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

It follows in particular that for all $n \in \mathbb{N}$ the canonical morphism $H_n(X,A) \stackrel{H_n(id,j)}{\to} H_n(X,U)$ is an [[isomorphism]], by prop. \ref{HomotopyInvariance}.

Given such $U$ we have an evident [[commuting diagram]] of pairs of [[topological spaces]]

$$
  \array{
    (X,A) &\stackrel{(id,j)}{\to}& (X,U) &\leftarrow& (X-A, U - A)
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    (X/A, A/A) &\stackrel{(id,j/A)}{\to}& (X/A, U/A) &\leftarrow& (X/A - A/A, U/A - A/A)
  }
  \,.
$$

Here the right vertical morphism is in fact a [[homeomorphism]].

Applying relative singular homology to this diagram yields for each $n \in \mathbb{N}$ the [[commuting diagram]] of abelian groups

$$
  \array{
    H_n(X,A) &\underoverset{\simeq}{H_n(id,j)}{\to}& H_n(X,U) &\stackrel{\simeq}{\leftarrow}& H_n(X-A, U - A)
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    H_n(X/A, A/A) &\underoverset{\simeq}{H_n(id,j/A)}{\to}& H_n(X/A, U/A) &\stackrel{\simeq}{\leftarrow}& H_n(X/A - A/A, U/A - A/A)
  }
  \,.
$$

Here the left horizontal morphisms are the above isomorphims induced from the deformation retract. The right horizontal morphisms are isomorphisms by prop. \ref{ExcisionA} and the right vertical morphism is an isomorphism since it is induced by a homeomorphism. Hence the left vertical morphism is an isomorphism ([[2-out-of-3]] for isomorphisms).

=--

### Relation to reduced homology 
 {#RelationToReducedHomology}

+-- {: .num_prop }
###### Proposition

Let $X$ be a [[inhabited set|inhabited]] [[topological space]] and let $x \colon  * \hookrightarrow X$ any point. Then the relative singular homology $H_n(X , *)$ is isomorphic to the absolute [[reduced singular homology]] $\tilde H_n(X)$ of $X$

$$
  H_n(X , *) \simeq \tilde H_n(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is the special case of prop. \ref{HomologyOfQuotientSpace} for $A$ a point.

=--



## Examples

### Basic examples

+-- {: .num_example }
###### Example

The [[reduced singular homology]] of the $n$-[[sphere]] $S^{n}$  equals the $S^{n-1}$-relative homology of the $n$-[[disk]] with respect to the canonical [[boundary]] inclusion $S^{n-1} \hookrightarrow D^n$: for all $n \in \mathbb{N}$

$$
  \tilde H_\bullet(S^n) \simeq H_\bullet(D^n, S^{n-1})
 \,.
$$

=--

+-- {: .proof}
###### Proof

The $n$-[[sphere]] is [[homeomorphism|homeomorphic]] to the $n$-[[disk]] with its entire [[boundary]] identified with a point:

$$
  S^n \simeq D^n/S^{n-1}
  \,.
$$

Moreover the boundary inclusion is evidently a _good pair_ in the sense of def. \ref{GoodPair}. Therefore the example follows with prop. \ref{HomologyOfQuotientSpace}.

=--

### Detecting homology isomorphisms

+-- {: .num_example }
###### Example

If an inclusion $A \hookrightarrow X$ is such that all relative homology vanishes, $H_\bullet(X , A) \simeq 0$, then the inclusion induces isomorphisms on all singular homology groups.

=--

+-- {: .proof}
###### Proof

Under the given assumotion the long exact sequence in prop. \ref{RelativeHomologyLongExactSequence} secomposes into short exact pieces of the form

$$
  0 \to H_n(A) \to H_n(X) \to 0
  \,.
$$

Exactness says that the middle morphism here is an [[isomorphism]].

=--

### Relative homology of CW-complexes
 {#RelativeHomologyOfCWComplexes}


Let $X$ be a [[CW-complex]] and write 

$$
  X_0 \hookrightarrow X_1 \hookrightarrow X_2 \hookrightarrow \cdots \hookrightarrow X
$$

for its [[filtered topological space]]-structure with $X_{n+1}$ the topological space obtained from $X_n$ by gluing on $(n+1)$-cells.


+-- {: .num_prop }
###### Proposition

The relative singular homology of the filtering degrees is

$$
  H_n(X_k , X_{k-1})
  \simeq
  \left\{
    \array{
       \mathbb{Z}[Cells(X)_n] & if\; k = n
       \\
       0 & otherwise
    }
  \right.
  \,,
$$

where $Cells(X)_n \in Set$ denotes the set of $n$-cells of $X$ and $\mathbb{Z}[Cells(X)_n]$ denotes the [[free abelian group]] on this set.


=--

For instance ([Hatcher, lemma 2.34](#Hatcher)).

+-- {: .proof}
###### Proof

The inclusion $X_{k-1} \hookrightarrow X_k$ is clearly a _good pair_ in the sense of def. \ref{GoodPair}. The quotient $X_k/X_{k-1}$ is by definition of CW-complexes a [[wedge sum]] of $k$-[[spheres]], one for each element in $kCell$. Therefore by prop. \ref{HomologyOfQuotientSpace} we have an isomorphism $H_n(X_k , X_{k-1}) \simeq \tilde H_n( X_k / X_{k-1})$ with the [[reduced homology]] of this wedge sum. The statement then follows by the respect of reduced homology for wedge sums as discussed at _[Reduced homology - Respect for wedge sums](reduced+homology#RelationToWedgeSums)_.

=--

## Related concepts

* [[relative cohomology]]

* [[cellular homology]]

* [[Gauss-Manin connection]]


## References

A standard textbook account for relative singular homology is section 2.1 of

* [[Allen Hatcher]], _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_


[[!redirects relative singular homology]]
