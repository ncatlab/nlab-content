[[!redirects sheaves on a topological space]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea


In general, the concept of _[[sheaf]]_ is relative to a choice of _[[site]]_, hence to a choice of [[small category]] $\mathcal{C}$ equipped with a [[coverage]]. Given this, the [[category of sheaves]] on $\mathcal{C}$ is the [[full subcategory]] of the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ on those presheaves which satisfy the sheaf condition:

$$
  Sh(\mathcal{C})
  \overset{\phantom{AAA}}{\hookrightarrow}
  [\mathcal{C}^{op}, Set]
  \,.
$$

Often sheaves are introduced and discussed in the more restrictive sense of _sheaves on a topological space_. This is indeed a special case: A sheaf on a [[topological space]] $X$ is a sheaf on the [[site]] $Op(X)$ whose underlying [[category]] is the [[category of open subsets]] of $X$, and whose [[coverage]] consists of the [[open covers]] of topological spaces. It is usual to write $Sh(X)$ as shorthand for the resulting category of sheaves, but the more systematic name is "$Sh(Op(X))$":

$$
  Sh(X) \;\coloneqq\; Sh(Op(X)) 
    \overset{\phantom{AAA}}{\hookrightarrow}
  [Op(X)^{op}, X]
  \,.
$$ 

A [[topos]] which is [[equivalence of categories|equivalent]] to a category of sheaves on a topological spaces, this way, is called a _spatial topos_.


## Properties

### Localic reflection

Similarly, if $X$ is a [[locale]], there is its [[frame of opens]] $Op(X)$ and one obtains the [[sheaf topos]] $Sh(X) \coloneqq Sh(Op(X))$ as above. A [[topos]] in the [[essential image]] of this construction is called a _[[localic topos]]_.  A _[[sober topological space]]_ is canonically identified as a [[locale]], and hence the category of sheaves over a sober topological space is a [[localic topos]].

Restricted to [[sober topological spaces]], the construction of forming [[categories of sheaves]] is a [[fully faithful functor]] to the category [[Topos]] of [[toposes]] with [[geometric morphisms]] between them:

$$
  Sh(-)
  \;\colon\;
  SoberTopologicalSpace
  \overset{ \phantom{AA} }{\hookrightarrow}
  Topos
  \,.
$$

([MacLaneMoerdijk, theorem IX.3 1](#MacLaneMoerdijk)) or as ([Johnstone, lemma C.1.2.2](#Johnstone))

For more see at _[[locale]]_ the section _[Localic reflection](locale#RelationToToposes)_.


## Examples

Examples of spatial toposes which are not _manifestly_ spatial, by usual their definition, include the following:

* The [[Bohr topos]] of a [[C*-algebra]]

* The category of [[hypergraphs]]

* The [[Sierpinski topos]]


## Related concepts


* [[étendue]]

* [[localic topos]], [[spatial locale]]

* [[abelian sheaf]], [[sheaf of abelian groups]]

* [[sheaves on a simplicial topological space]]

## References

* {#Johnstone} [[Peter Johnstone]], part C (volume 2) _[[Elephant|Sketches of an elephant: a topos theory compendium]]_.

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_


[[!redirects category of sheaves on a locale]]
[[!redirects categories of sheaves on a locale]]

[[!redirects category of sheaves on a topological space]]
[[!redirects categories of sheaves on a topological space]]
[[!redirects categories of sheaves on topological spaces]]

[[!redirects spatial topos]]
[[!redirects spatial toposes]]
[[!redirects spatial topoi]]

