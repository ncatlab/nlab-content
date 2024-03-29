
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given any notion of _[[cohomology]]_ defined on [[pointed objects]], the corresponding _reduced cohomology_ is that part of the cohomology which vanishes on the basepoint. 

Specifically for [[Whitehead-generalized cohomology theories]] the reduced cohomology is the cohomology relative to the base point, hence is the [[kernel]] of the operation of [[pullback in cohomology|pullback]] to the base point See [below](#RelationToUnreducedCohomology) and see at _[generalized cohomology -- Relation between reduced and unreduced](generalized+Eilenberg-Steenrod+cohomology#RelationBetweenReducedAndUnreduced)_ for more.



## Definition

+-- {: .num_defn #ReducedGeneralizedCohomology}
###### Definition

A **reduced [[cohomology theory]]** is a [[functor]]

$$
  \tilde E^\bullet 
   \;\colon\; 
  \big(
    Top^{\ast/}_{CW}
  \big)^{op} 
    \longrightarrow 
  Ab^{\mathbb{Z}}
$$

from the [[opposite category|opposite]] of [[pointed topological spaces]] ([[CW-complexes]]) to $\mathbb{Z}$-[[graded abelian groups]] ("[[cohomology groups]]"), in components

$$
  \tilde E 
    \;\colon\; 
  \big(
    X \stackrel{f}{\longrightarrow} Y
  \big)
    \;\mapsto\;
  \big(
    \tilde E^\bullet(Y) 
      \stackrel{f^\ast}{\longrightarrow}
    \tilde E^\bullet(X)
  \big)
  \,,
$$

and equipped with a [[natural isomorphism]] of degree +1, to be called the **[[suspension isomorphism]]**, of the form

$$
  \sigma
    \;\colon\;
  \tilde E^{\bullet +1}(\Sigma -) 
    \overset{\simeq}{\longrightarrow} 
  \tilde E^\bullet(-) 
$$

such that:

1. **([[homotopy invariance]])** If $f_1,f_2 \colon X \longrightarrow Y$ are two morphisms of pointed topological spaces such that there is a (base point preserving) [[homotopy]] $f_1 \simeq f_2$ between them, then the induced [[homomorphisms]] of abelian groups are [[equality|equal]] 

   $$
     f_1^\ast = f_2^\ast
     \,.
   $$

1. {#ReducedExactnessAxiom} **(exactness)** For $i \colon A \hookrightarrow X$ an inclusion of pointed topological spaces, with $j \colon X \longrightarrow Cone(i)$ the induced [[mapping cone]], then this gives an [[exact sequence]] of graded abelian groups

   $$
     \tilde E^\bullet(Cone(i)) 
      \overset{j^\ast}{\longrightarrow} 
     \tilde E^\bullet(X)
       \overset{i^\ast}{\longrightarrow}
     \tilde E^\bullet(A)
     \,.
   $$

We say $\tilde E^\bullet$ is **additive** if in addition

* **([[wedge axiom]])** For $\{X_i\}_{i \in I} $ any set of pointed CW-complexes, then the canonical comparison morphism

  $$
    \tilde E^\bullet(\vee_{i \in I} X_i) 
     \longrightarrow
    \prod_{i \in I} \tilde E^\bullet(X_i)
  $$

  is an [[isomorphism]], from the functor applied to their [[wedge sum]], example \ref{WedgeSumAsCoproduct}, to the [[product]] of its values on the wedge summands, .

We say $\tilde E^\bullet$ is **ordinary** if its value on the [[0-sphere]] $S^0$ is concentrated in degree 0:

* **(Dimension)**  $\tilde E^{\bullet\neq 0}(\mathbb{S}^0) \simeq 0$.

A [[homomorphism]] of reduced cohomology theories

$$
  \eta \;\colon\; \tilde E^\bullet \longrightarrow \tilde F^\bullet
$$

is a [[natural transformation]] between the underlying functors which is compatible with the suspension isomorphisms in that all the following [[commuting square|squares commute]]

$$
  \array{
    \tilde E^\bullet(X) &\overset{\eta_X}{\longrightarrow}&  \tilde F^\bullet(X)
    \\
    {}^{\mathllap{\sigma_E}}\downarrow && \downarrow^{\mathrlap{\sigma_F}}
    \\
    \tilde E^{\bullet + 1}(\Sigma X) 
    &\overset{\eta_{\Sigma X}}{\longrightarrow}&
    \tilde F^{\bullet + 1}(\Sigma X)
  }
  \,.
$$

=--

(e.g. [AGP 02, def. 12.1.4](#AGP02))

## Properties

### Brown representability 

The [[Brown representability theorem]] says that for any reduced cohomology theory $\tilde E^\bullet$ there is an [[Omega-spectrum]] $E$ which [[representable functor|represents]] $\tilde E^\bullet$ on pointed connected CW-complex $X$, in that

$$
  \tilde E^n(X) \simeq [X,E_n]_\ast
  \,.
$$

### Relation to unreduced cohomology
 {#RelationToUnreducedCohomology}

For an unreduced [[cohomology theory]] $E^\bullet$  the induced **reduced cohomology** is the [[kernel]] of operation of [[pullback in cohomology|pullback]] to the base point.

$$
  \tilde E^k(X,x_0) 
    \;\coloneqq\; 
  E^k(X,\{x_0\}) 
    \;=\; 
  ker\big(
    H^k(X) \to H^k(\{x_0\}) 
  \big)
$$

(e.g. [AGP 02, theorem 12.1.12](#AGP02)).

For more see at _[generalized cohomology -- Relation between reduced and unreduced](generalized+Eilenberg-Steenrod+cohomology#RelationBetweenReducedAndUnreduced)_.

## Related entries

* [[reduced homology]]

* [[vanishing at infinity]]

## References

See the references at _[[generalized (Eilenberg-Steenrod) cohomology]]_.

* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of: _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))


* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology - cohomology theories]]_


[[!redirects reduced cohomology theory]]