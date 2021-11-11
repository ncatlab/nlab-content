

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notions of *equivariant open cover* and of *equivariant good open cover* are the generalization of the notions of *[[open cover]]* and *[[good open cover]]* from [[differential topology]] to [[equivariant differential topology]], hence from [[topological spaces]] to [[topological G-spaces]] and [[G-manifolds]].

Accordingly, for some [[equivariance group]] $G$, an equivariant (good) open cover of a [[topological G-space]] is a ([[good open cover|good]]) [[open cover]] of its [[underlying]] [[topological space]] which is compatible with the [[group action]] in a suitable way. At a minimum this means that the cover is itself a [[topological G-space]] and that the covering map is an [[equivariant function]], but for purposes of [[proper equivariant homotopy theory|proper]] [[equivariant homotopy theory]] one will typically need that passage to $H$-[[fixed loci]], for suitable [[subgroups]] $H \subset G$, preserves the (good) covering properties.

## Definition

In the following, $kTopSp$ denotes the [[convenient category of topological spaces|convenient category]] of [[compactly generated weak Hausdorff spaces]].

For $G \,\in\, Grp(kTopSp)$ a (cgwh-)[[topological group]], and $H \,\subset\, G$ a [[subgroup]], we write

\[
  \label{HFixedLocusFunctor}
  G Act(kTopSp)
  \xrightarrow{\; (-)^H \;}
  kTopSp
\]

for the [[functor]] from the [[category]] of (cgwh-)[[topological G-spaces]] which assigns $H$-[[fixed loci]].

\begin{definition}
\label{ProperlyEquivariantOpenCover}
**(properly equivariant open covers)**
\linebreak
  For $G \,\in\, Grp(SmthMfd) \xhookrightarrow{\;} Grp(kTopSp)$ a [[topological group]] [[underlying]] a [[Lie group]], and $G \curvearrowright X \,\in\, G Act(kTopSp)$ a [[topological G-space]], say that a [[morphism]]

$$
  G \curvearrowright \widehat{X}
  \;\;
  \xrightarrow{\;\; p \;\;}
  \;\;
  G \curvearrowright \widehat{X}
  \;\;\;
  \in
  \;
  G Act(kTopSp)
$$

is

1. a *properly equivariant open cover* if for all [[compact subgroups]] $H \,\subset\, G$ its restriction (eq:HFixedLocusFunctor) to $H$-[[fixed loci]]  is a plain [[open cover]] of [[topological spaces]]:

   \[
     \label{OpenCoverOnAllFixedLoci}
     \underset{
       H \underset{cpt}{\subset} G
     }{\forall}
     \;\;\;
     \widehat{X}^H
     \underoverset
       { open\,cover }
       {p^H}
       {\longrightarrow}
     X^H
   \]

1. a *properly equivariant good open cover* if the restrictions (eq:OpenCoverOnAllFixedLoci) are all [[good open covers]].

\end{definition}

## Properties

### Existence

\begin{proposition}
  For $G \,\in\, Grp(FinSet) \xhookrightarrow{Grp(Dsc)} Grp(kTopSp)$ a [[finite group]], the [[topological G-space]] [[underlying]] a [[smooth manifold|smooth]] [[G-manifold]] admits a properly equivariant good open cover (Def. \ref{ProperlyEquivariantOpenCover}).
\end{proposition}

([Yang 2014, Thm. 2.11](#Yang14), using the [[equivariant triangulation theorem]])

## Related entries

* [[equivariant triangulation theorem]]

## References

* {#Yang14} Haibo Yang, *Equivariant cohomology and sheaves*, Journal of Algebra, **412** 2014, 230-254 ([doi:10.1016/j.jalgebra.2014.05.009](https://doi.org/10.1016/j.jalgebra.2014.05.009))


[[!redirects equivariant good open covers]]


[[!redirects equivariant open cover]]
[[!redirects equivariant open covers]]


[[!redirects equivariant good open cover]]
[[!redirects equivariant good open covers]]
