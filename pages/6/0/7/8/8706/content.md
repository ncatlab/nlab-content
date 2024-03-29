
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In general, the [[homology]] of a [[point]] is not trivial but is concentrated in degree 0 on the given [[coefficient]] object. For some applications, though, it is convenient to divide out that contribution such as to have the homology of the point be entirely trivial. This is called _reduced homology_.

## Definition

### Reduced singular homology

We discuss the reduced version of [[singular homology]].

Let $X$ be a [[topological space]]. Write $C_\bullet(X)$ for its [[singular chain complex]].

+-- {: .num_defn}
###### Definition

The **augmentation map** is the homomorphism of abelian groups

$$
  \epsilon \colon C_0(X) \to \mathbb{Z}
$$

which adds up all the coefficients of all 0-chains:

$$
  \epsilon \colon \colon \sum_{i} n_i \sigma_i \mapsto \sum_i n_i
  \,.
$$

Since the boundary of a 1-chain is in the [[kernel]] of this map, it constitutes a [[chain map]]

$$
  \epsilon \colon C_\bullet(X) \to \mathbb{Z}
  \,,
$$

where now $\mathbb{Z}$ is regarded as a chain complex concentrated in degree 0.

=--

+-- {: .num_defn #ReducedSingularChainComplex}
###### Definition

The **reduced singular chain complex** $\tilde C_\bullet(X)$ of $X$ is the [[kernel]] of the augmentation map, the chain complex sitting in the [[short exact sequence]]

$$
  0 \to \tilde C_\bullet(X) \to C_\bullet(X) \stackrel{\epsilon}{\to} \mathbb{Z} \to 0
  \,.
$$

The **reduced singular homology** $\tilde H_\bullet(X)$ of $X$ is the [[chain homology]] of the reduced singular chain complex

$$
  \tilde H_\bullet(X) \coloneqq H_\bullet(\tilde C_\bullet(X))
  \,.
$$

=--

Equivalently:

+-- {: .num_defn}
###### Definition

The **reduced singular homology** of $X$, denoted $\tilde H_\bullet(X)$, is the [[chain homology]] of the [[augmentation|augmented]] chain complex

$$
  \cdots \to C_2(X) \stackrel{\partial_2}{\to} C_1(X) \stackrel{\partial_1}{\to} C_0(X) \stackrel{\epsilon}{\to}
  \mathbb{Z} \to 0
  \,.
$$

=--

## Properties

### Relation to ordinary homology
 {#RelationToOrdinaryHomology}

Let $X$ be a [[topological space]], $H_\bullet(X)$ its [[singular homology]] and $\tilde H_\bullet(X)$ its reduced singular homology, def. \ref{ReducedSingularChainComplex}.

+-- {: .num_prop #RelationBetweenReducedSingularAndSingular}
###### Proposition

For $n \in \mathbb{N}$ there is an [[isomorphism]]

$$
  H_n(X)
  \simeq
  \left\{
    \array{
      \tilde H_n(X) & for \; n \geq 1
      \\
      \tilde H_0(X) \oplus \mathbb{Z} & for\; n = 0
    }
  \right.
$$

=--

+-- {: .proof}
###### Proof

The [[homology long exact sequence]] of the defining short exact sequence $\tilde C_\bullet(C) \to C_\bullet(X) \stackrel{\epsilon}{\to} \mathbb{Z}$ is, since $\mathbb{Z}$ here is concentrated in degree 0, of the form

$$
  \cdots \to \tilde H_n(X) \to H_n(X) \to 0 \to \cdots \to 
  0 \to 
  \cdots \to \tilde H_1(X) \to H_1(X) \to 0 \to 
  \tilde H_0(X) \to H_0(X) \stackrel{\epsilon}{\to}  \mathbb{Z} \to 0 
  \,.
$$

Here [[exact sequence|exactness]] says that all the morphisms $\tilde H_n(X) \to H_n(X)$ for positive $n$ are [[isomorphisms]]. Moreover, since $\mathbb{Z}$ is a [[free abelian group]], hence a [[projective object]], the remaining [[short exact sequence]]

$$
  0 \to \tilde H_0(X) \to H_0(X) \to \mathbb{Z} \to 0
$$

is [[split exact sequence|split]] (as discussed there) and hence $H_0(X) \simeq \tilde H_0(X) \oplus \mathbb{Z}$.
 
=--

+-- {: .num_prop}
###### Proposition

For $X = *$ the [[point]], the morphism

$$
  H_0(\epsilon) \colon H_0(X) \to \mathbb{Z}
$$

is an [[isomorphism]]. Accordingly the reduced homology of the point vanishes in every degree:

$$
  \tilde H_\bullet(*) \simeq 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion at _[Singular homology -- Relation to homotopy groups](singular%20homology#RelationToHomotopyGroups)_ we have that 

$$
  H_n(*) \simeq
  \left\{
    \array{
       \mathbb{Z} & for \; n = 0
       \\
       0 & otherwise
    }
  \right.
  \,.
$$

Moreover, it is clear that $\epsilon \colon C_0(*) \to \mathbb{Z}$ is the [[identity]] map. 

=--


### Relation to relative homology
 {#RelationToRelativeHomology}

+-- {: .num_prop}
###### Proposition

For $X$ an [[inhabited set|inhabited]] [[topological space]], its reduced singular homology, def. \ref{ReducedSingularChainComplex}, coincides with its [[relative singular homology]] relative to any base point $x \colon * \to X$:

$$
  \tilde H_\bullet(X)
  \simeq
   H_\bullet(X,*)
  \,.
$$


=--

+-- {: .proof}
###### Proof

Consider the sequence of [[topological subspace]] inclusions

$$
  \emptyset \hookrightarrow * \stackrel{x}{\hookrightarrow} X
  \,.
$$

By the discussion at _[Relative homology - long exact sequences](relative%20homology#LongExactSequences)_ this induces a [[long exact sequence]] of the form

$$
  \cdots
  \to
  H_{n+1}(*) \to H_{n+1}(X) \to H_{n+1}(X,*)
  \to
  H_n(*) \to H_n(X) \to H_n(X,*)
  \to 
  \cdots
  \to 
  H_1(X) \to H_1(X,*) \to  H_0(*) \stackrel{H_0(x)}{\to}  H_0(X) \to H_0(X,*)
  \to 0
  \,.
$$

Here in positive degrees we have $H_n(*) \simeq 0$ and therefore [[exact sequence|exactness]] gives [[isomorphisms]]

$$
  H_n(X) \stackrel{\simeq}{\to} H_n(X,*)\;\; \forall_{n \geq 1}
$$

and hence with prop. \ref{RelationBetweenReducedSingularAndSingular} isomorphisms

$$
  \tilde H_n(X) \stackrel{\simeq}{\to} H_n(X,*)\;\; \forall_{n \geq 1}  
  \,.
$$

It remains to deal with the case in degree 0. To that end, observe that $H_0(x) \colon H_0(*) \to H_0(X)$ is a [[monomorphism]]: for this notice that we have a [[commuting diagram]]

$$
  \array{
     H_0(*) &\stackrel{id}{\to}& H_0(*)
     \\
     {}^{\mathllap{H_0(x)}}\downarrow &{}^{\mathllap{H_0(f)}}\nearrow& \downarrow^{\mathrlap{H_0(\epsilon)}}_\simeq
     \\
     H_0(X) &\stackrel{H_0(\epsilon)}{\to}& \mathbb{Z}
  }
  \,,
$$

where $f \colon X \to *$ is the terminal map. 
That the outer square commutes means that $H_0(\epsilon) \circ H_0(x) = H_0(\epsilon)$ and hence the composite on the left is an [[isomorphism]]. This implies that $H_0(x)$ is an injection.

Therefore we have a [[short exact sequence]] as shown in the top of this diagram

$$
  \array{
    0 &\to& H_0(*) &\stackrel{H_0(x)}{\hookrightarrow}&
    H_0(X) &\stackrel{}{\to}& H_0(X,*)
    &\to&
    0
    \\
    && & {}_{\mathllap{\simeq}}\searrow & \downarrow^{\mathrlap{H_0(\epsilon)}} & 
   \\
   && && \mathbb{Z}
  }
  \,.
$$

Using this we finally compute

$$
  \begin{aligned}
    \tilde H_0(X)
    & \coloneqq 
    ker H_0(\epsilon)
    \\
    & \simeq coker( H_0(x) )
    \\
    & \simeq H_0(X,*)
  \end{aligned}
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

Moreover, for "good" inclusions $A \hookrightarrow X$ of topological space, the reduced singular homology of the quotient $X/A$ is isomorphic to the $A$-[[relative singular homology]] of $X$. 

See at _[Relative homology - Relation to reduced homology of quotient topological spaces](relative+homology#RelationToQuotientTopologicalSpaces)_.

=--

### Relation to wedge sums
 {#RelationToWedgeSums}

Let $\{* \to X_i\}_i$ be a set of [[pointed object|pointed]] [[topological spaces]]. Write $\vee_i X_i \in Top$ for their [[wedge sum]] and write
$\iota_i \colon X_i \to \vee_i X_i$ for the canonical inclusion functions.

+-- {: .num_prop}
###### Proposition

For each $n \in \mathbb{N}$ the homomorphism

$$
  (\tilde H_n(\iota_i))_i \colon \oplus_i \tilde H_n(X_i) \to \tilde H_n(\vee_i X_i)
$$

is an [[isomorphism]].

=--

For instance ([Hatcher, cor. 2.25](#Hatcher)).

+-- {: .proof}
###### Proof

This follows with _[this proposition](relative+homology#HomologyOfQuotientSpace)_ at _[[relative homology]]_.

=--

## Examples

### For singular homology

For $X$ a [[topological space]], write $H_n(X)$ for its [[singular homology]] with integer coefficients.


+-- {: .num_example #ReducedHomologyOfPoints}
###### Example

If $X$ is a [[contractible topological space]], then for all $n \in \mathbb{N}$

$$
  \tilde H_n(X) \simeq 0
  \,.
$$

=--

+-- {: .num_example #ReducedHomologyOf0Sphere}
###### Example

The reduced singular homology of the 0-[[sphere]] $S^0 \simeq {*} \coprod {*}$ is

$$
  \tilde H_n(S^0) \simeq 
  \left\{
    \array{
       \mathbb{Z} & if \; n = 0
       \\
       0 & otherwise
    }
  \right.
  \,.
$$ 

=--

## Related concepts

* [[reduced cohomology]]


## References

Reduced singular homology is discussed for instance around p. 119 of 

* [[Alan Hatcher]], _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_


[[!redirects reduced singular homology]]

