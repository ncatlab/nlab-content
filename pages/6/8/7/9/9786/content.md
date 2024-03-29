+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Convergence vector space
* table of contents
{: toc}

## Idea

A **convergence vector space** is a generalisation of a [[topological vector space]] where the topological structure is replaced by a [[convergence space|convergence structure]].

## Definition

+-- {: .num_defn #cvsp}
###### Definition
A **convergence vector space** is a [[vector space]], say $V$, together with the structure of a [[convergence space]], say $\Lambda$, which is compatible with the vector space structure in that both addition and scalar multiplication are jointly continuous.
=--

Some authors may impose the condition that the convergence structure be separated.  Any [[topological vector space]] defines a convergence vector space.


## Multilinear Mappings

Convergence structures become particularly useful when considering evaluation mappings in functional analysis.  For a [[locally convex topological vector space]] $E$ with continuous dual $E^*$, the evaluation mapping $E \times E^* \to \mathbb{F}$ is continuous with respect to the product topology if and only if $E$ is normable.  This proves to be somewhat of a limitation when one works outside the category of normable [[LCTVS]].  However, there is a convergence structure on $E \times E^*$ which makes the evaluation mapping continuous.

+-- {: .num_defn #cmulti}
###### Definition
Let $E$ and $F$ be convergence vector spaces and $n \in \mathbb{N}$.  Let $\mathcal{L}^n(E,F)$ be the space of continuous mappings $E^n \to F$ which are linear in each argument (see [[continuous multilinear operator]]).  The **continuous convergence structure** on $\mathcal{L}^n(E,F)$ is the coarsest convergence structure which makes the evaluation map $\mathcal{L}^n(E,F) \times E^n \to F$ continuous.

We write $\mathcal{L}_c^n(E,F)$ for the resulting convergence space.
=--

+-- {: .num_lemma #cmultlem}
###### Lemma
The convergence space $\mathcal{L}_c^n(E,F)$ is a convergence vector space.  It satisfies the following universal property for a [[convergence space]] $X$ then a mapping $X \to \mathcal{L}_c^n(E,F)$ is continuous if and only if the associated map $X \times E^n \to F$ is continuous.
=--


[[!redirects convergence vector spaces]]