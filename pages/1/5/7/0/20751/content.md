
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

For $X$ a [[topological space]] and $n \in \mathbb{N}$ a [[natural number]], the space of [[finite set|finite]] [[subsets]] of [[cardinality]] $\leq n$ in $X$ is the suitably topologized [[set]] of [[finite set|finite]] [[subsets]] $S \subset X$ of [[cardinality]] $\left\vert S\right\vert \leq n$, often denoted $\exp^n X$ or similar (e.g. [Félix-Tanré 10](#FelixTanre10)).

## Properties

### Relation to unordered configuration space of points

The [[topological subspace]]  of finite subsets of cardinality exactly equal to $n$ is the [[unordered configuration space of points]] in $X$

\[
  \label{InjectionOfUnorderedConfigurationSpaceOfPoints}
  Conf_n(X)
  \hookrightarrow
  \exp^n(X)
\]


+-- {: .num_prop #UnorderedConfigurationSpaceInSpaceOfFiniteSubsets}
###### Proposition

Let $X$ be an [[inhabited set|non-empty]] [[regular topological space]] and $n \geq 2 \in \mathbb{N}$.

Then the injection (eq:InjectionOfUnorderedConfigurationSpaceOfPoints)

\[
  \label{UnorderedConfigurationSpaceOpenSubsetInQuotientOfSpacesOfFiniteSubsets}
  Conf_n(X)
  \hookrightarrow
  \exp^n(X)/\exp^{n-1}(X)
\]

of the [[unordered configuration space of n points]] of $X$ into the [[quotient space]] of the [[space of finite subsets]] of cardinality $\leq n$ by its subspace of subsets of cardinality $\leq n-1$ is an [[open subspace]]-inclusion.

Moreover, if $X$ is [[compact topological space|compact]], then so is $\exp^n(X)/\exp^{n-1}(X)$ and the inclusion (eq:UnorderedConfigurationSpaceOpenSubsetInQuotientOfSpacesOfFiniteSubsets) exhibits the [[one-point compactification]] $\big(  Conf_n(X) \big)^{+} $ of the configuration space:

$$
  \big( 
    Conf_n(X)
  \big)^{+}
  \;\simeq\;
  \exp^n(X)/\exp^{n-1}(X)
  \,.
$$

=--

([Handel 00, Prop. 2.23](#Handel00), see also [Félix-Tanré 10](#FelixTanre10))

## References


* {#Handel00} David Handel, _Some Homotopy Properties of Spaces of Finite Subsets of Topological Spaces_, Houston Journal of Mathematics, Electronic Edition Vol. 26, No. 4, 2000 (<a href="https://www.math.uh.edu/~hjm/pdf26(4)/08handel.pdf">pdf</a>[hjm:Vol26-4](https://www.math.uh.edu/~hjm/Vol26-4.html))

* {#FelixTanre2010} [[Yves Félix]], [[Daniel Tanré]] _Rational homotopy of symmetric products and Spaces of finite subsets_, Contemp. Math 519 (2010): 77-92 ([pdf](http://tanre.org/Pro/Articles_files/SpnFiniteDef.pdf))

* Jacob Mostovoy, Rustam Sadykov, _On the connectivity of finite subset spaces_ ([arXiv:1203.5180](https://arxiv.org/abs/1203.5180))