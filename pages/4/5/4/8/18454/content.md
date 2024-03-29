
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $X$ a [[topological space]], the _category of covering spaces_ $Cov(X)$ is the [[category]] whose 

* [[objects]] are [[covering spaces]] $E \overset{p}{\to} X$ over $X$;

* [[morphisms]] are [[homomorphisms]] of covering spaces, hence [[continuous functions]] $f \colon E_1 \longrightarrow E_2$ such that we have a [[commuting diagram]]

  $$
    \array{
      E_1 && \overset{f}{\longrightarrow} && E_2
      \\
      & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
      \\
      && X
    }
  $$

This is equivalently the [[full subcategory]] of the [[slice category]] $Top_{/X}$ of the [[category of topological spaces]] over $X$ on those objects which are covering spaces.

## Properties


+-- {: .num_prop }
###### Proposition
**([[fundamental theorem of covering spaces]])**

For $X$ a [[topological space]] then forming [[monodromy]] is a [[functor]] from the category of covering spaces over $X$ to that of [[permutation representations|permutation]] [[groupoid representations]] of the [[fundamental groupoid]] of $X$:

$$
  Fib \;\colon\; Cov(X)  \longrightarrow Set^{\Pi_1(X)}
  \,.
$$

If $X$ is [[locally path-connected topological space|locally path connected]] and [[semi-locally simply connected topological space|semi-locally simply connected]], then this is an [[equivalence of categories]]. 

=--

See at _[[fundamental theorem of covering spaces]]_ for details.

## Related concepts

* [[category of vector bundles]]

