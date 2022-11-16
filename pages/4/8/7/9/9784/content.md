
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Precompact spaces
* table of contents
{: toc}

## Idea

A _precompact space_ is one whose [[complete space|completion]] is compact.  This makes sense for [[Cauchy spaces]], but not for [[topological spaces]]. In the context of [[uniform spaces]], precompact spaces are [[totally bounded spaces]]. 

Precompact subsets (using the [[induced uniformity]]) are one of the useful types of subset of a [[locally convex topological vector space]], particularly with regard to defining topologies on [[dual vector space|dual spaces]].


## Definitions

Let $X$ be (in the most general situation) a [[Cauchy space]]; this includes [[uniform convergence spaces]], [[uniform spaces]], [[topological groups]], [[topological vector spaces]], and [[metric spaces]] (among other things) as special cases.

The following definitions are all equivalent even in weak [[constructive mathematics|constructive]] [[foundations]]:

+-- {: .num_defn #completion}
###### Definition
The space $X$ is **precompact** if its [[complete space|completion]] is [[compact space|compact]].
=--

+-- {: .num_defn #filters}
###### Definition
The space $X$ is __precompact__ if every [[proper filter]] on $X$ has a (proper) [[Cauchy filter|Cauchy]] refinement.
=--

+-- {: .num_defn #nets}
###### Definition
The space $X$ is __precompact__ if every [[net]] in $X$ has a [[Cauchy net|Cauchy]] [[subnet]] (under any definition of 'subnet').
=--

We also have this subsidiary notion:

+-- {: .num_defn #subspace}
###### Definition
A [[subset]] of $X$ is **precompact** if it is precompact (or ...) for the inherited structure.
=--

### Sequential precompactness

\begin{definition}
The space $X$ is __sequentially precompact__ if every [[sequence]] in $X$ has a [[Cauchy sequence|Cauchy]] [[subsequence]].
\end{definition}

## Properties

\begin{theorem}
Assuming [[weak countable choice]], every sequentially precompact [[Lawvere metric space]] is a precompact Lawvere metric space. 
\end{theorem}

### Relation to totally bounded spaces

\begin{theorem}
Every precompact space is a [[totally bounded space]]. 
\end{theorem}

\begin{theorem}
That every [[totally bounded space|totally bounded]] [[uniform space]] is precompact is equivalent to the [[ultrafilter principle]], because the generalised [[Cantor space]] $2^K$ is complete and totally bounded for any [[cardinal number]] $K$. 
\end{theorem}

\begin{theorem}
Assuming [[excluded middle]] and [[dependent choice]], every totally bounded [[metric space]] is precompact. 
\end{theorem}

(I don\'t know to what extent DC and EM are actually relevant to any of this; my reference _[[HAF]]_ tacitly assumes them most of the time.)

## See also ##

* [[compact space]]

* [[totally bounded space]]

[[!redirects precompact space]]
[[!redirects precompact spaces]]

[[!redirects precompact set]]
[[!redirects precompact sets]]
[[!redirects precompact subset]]
[[!redirects precompact subsets]]
[[!redirects precompact subspace]]
[[!redirects precompact subspaces]]
