
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

The [[image]] under a [[continuous function]] of a [[compact topological space]] is itself compact (cor. \ref{ContinuousImageOfACompactSpaceIsCompact} below.)

This is a generalization of the _[[extreme value theorem]]_ in [[analysis]].

## Statement

In fact the following more general statement holds

+-- {: .num_lemma #ContinuousSurjectionOutOfCompactSpaceHasCompactCodomain}
###### Lemma

Let $f \colon (X,\tau_X) \longrightarrow (Y,\tau_Y)$ be a [[continuous function]] between [[topological spaces]] such that

1. $(X,\tau_X)$ is a [[compact topological space]];

1. $f \colon X \to Y$ is a [[surjective function]].

Then also $(Y,\tau_Y)$ is [[compact topological space|compact]].

=--

+-- {: .proof}
###### Proof

Let $\{U_i \subset Y\}_{i \in I}$ be an [[open cover]] of $Y$. We need show that this has a finite sub-cover. 

By the continuity of $f$ the [[pre-images]] $f^{-1}(U_i)$ form an [[open cover]] $\{f^{-1}(U_i) \subset X\}_{i \in I}$ of $X$. Hence by compactness of $X$, there exists a [[finite set|finite]] [[subset]] $J \subset I$ such that 
$\{f^{-1}(U_i) \subset X\}_{i \in J \subset I}$ is still an open cover of $X$. Finally, by surjectivity of $f$ it follows that 

$$
  \begin{aligned}
    Y 
      & = f(X)
    \\
      & = f\left( \underset{i \in J}{\cup} f^{-1}(U_i) \right)
    \\
      & = \underset{i \in J}{\cup} U_i
  \end{aligned}
$$

where we used that [[images of unions are unions of images]].

This means that also $\{U_i \subset Y\}_{i \in J \subset I}$ is still an open cover of $Y$, and in particular a finite subcover of the original cover. 

=--


+-- {: .num_cor #ContinuousImageOfACompactSpaceIsCompact}
###### Corollary

If $f \colon X \longrightarrow Y$ is a [[continuous function]] out of a [[compact topological space]] $X$ which is not necessarily [[surjective function|surjective]], then we may consider its [[image]] factorization

$$
  f \;\colon\; X \longrightarrow im(f) \hookrightarrow Y
$$

with $im(f)$ regarded as a [[topological subspace]] of $Y$. Now by construction $X \to \im(f)$ is surjective, and so lemma \ref{ContinuousSurjectionOutOfCompactSpaceHasCompactCodomain} implies that $im(f)$ is compact.

=--

## Related statements

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]


[[!redirects continuous image of a compact space is compact]]

[[!redirects continuous surjections out of compact spaces have compact codomain]]
