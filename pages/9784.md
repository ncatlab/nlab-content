
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

A _precompact space_ is one whose [[complete space|completion]] is compact.  This makes sense for [[uniform spaces]] (and more generally for [[Cauchy spaces]]) but not for [[topological spaces]].

There is an alternative definition, apparently having nothing to do with completion of compactness, but equivalent (at least in [[classical mathematics]]).  When necessary to distinguish this, we may call this alternative a _totally bounded space_.

Precompact subsets (using the [[induced uniformity]]) are one of the useful types of subset of a [[locally convex topological vector space]], particularly with regard to defining topologies on [[dual vector space|dual spaces]].


## Definitions

Let $X$ be (in the most general situation) a [[Cauchy space]]; this includes [[uniform convergence spaces]], [[uniform spaces]], [[topological groups]], [[topological vector spaces]], and [[metric spaces]] (among other things) as special cases.

The following definitions are all equivalent even in weak [[constructive mathematics|constructive]] [[foundations]] (such as the [[internal logic]] of a [[predicative topos]], [[ETCS|CETCS]], [[SEAR|CSEAR]], or [[CZF]]):

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

The following definition is equivalent for [[metric spaces]] (or even [[Lawvere metric spaces]]), assuming [[weak countable choice]] (which is very weak):

+-- {: .num_defn #sequences}
###### Definition
The space $X$ is __sequentially precompact__ if every [[sequence]] in $X$ has a [[Cauchy sequence|Cauchy]] [[subsequence]].
=--

Of course, this definition makes sense for any Cauchy space, but in general it is not equivalent, so useful to distinguish regardless of one\'s foundations.

The following notion is equivalent for [[uniform spaces]] assuming the [[ultrafilter principle]], [[dependent choice]], and [[excluded middle]] (a combination which is not quite as strong as the full [[axiom of choice]] but pretty close):

+-- {: .num_defn #totbound}
###### Definition
The space $X$ is __totally bounded__ if every [[uniform cover]] has a finite subcover.
=--

Since this definition only makes sense for uniform spaces, there is no need to distinguish it from precompactness when doing [[classical analysis]].

Even in weak foundations, a precompact space is still totally bounded.  Conversely, the ultrafilter principle *follows* if every totally bounded uniform space is precompact (because the generalised [[Cantor space]] $2^K$ is complete and totally bounded for any [[cardinal number]] $K$).  On the other hand, DC and EM alone are enough to show that every totally bounded *metric* space is precompact.  (I don\'t know to what extent DC and EM are actually relevant to any of this; my reference _[[HAF]]_ tacitly assumes them most of the time.)

In any case, we also have this subsidiary notion:

+-- {: .num_defn #subspace}
###### Definition

A [[subset]] of $X$ is **precompact** (or sequentially so, or totally bounded) if it is precompact (or ...) for the inherited structure.
=--

## See also ##

* [[totally bounded space]]

[[!redirects precompact space]]
[[!redirects precompact spaces]]

[[!redirects precompact set]]
[[!redirects precompact sets]]
[[!redirects precompact subset]]
[[!redirects precompact subsets]]
[[!redirects precompact subspace]]
[[!redirects precompact subspaces]]
