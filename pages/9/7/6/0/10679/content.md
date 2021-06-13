
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

## Definition

The [[forgetful functor]]/[[full and faithful functor|full and faithful]] [[subcategory]] embedding from [[compact topological spaces|compact]] [[Hausdorff topological spaces]] 
into all [[topological spaces]] 

$$
  U \;\colon\; Top_{CHaus} \hookrightarrow Top
$$ 

has a [[left adjoint]]

$$ 
  \beta \;\colon\; Top \longrightarrow Top_{CHaus}
$$

which sends a general [[topological space]] to a [[compact topological spaces|compact]] [[Hausdorff topological space]], called its _Stone-&#268;ech compactification_. This hence exhibits $Top_{CHaus}$ as a [[reflective subcategory]] of all of $Top$.

The Stone-Cech compactification is in general "very large", even for "ordinary" non-compact spaces such as the [[real line]].

For more details see at _[compactum -- Stone-&#268;ech compactification](compactum#StoneCechCompactification)_

## Properties

+-- {: .num_prop}
###### Proposition

The [[unit of an adjunction|unit]] 

$$
  X \longrightarrow \beta X
$$

of the compactification [[adjunction]] $(\beta \dashv U)$ is an [[embedding]] precisely for $X$ a [[Tychonoff space]].

=--

## Examples

+-- {: .num_example}
###### Example

The Stone-Cech compactification of a [[discrete topological space]]
is an [[extremally disconnected topological space]].
By a theorem by Gleason, these are precisely the [[projective objects]]
in the [[category]] of [[compact topological space|compact]]
[[Hausdorff topological spaces]].

Such spaces appear for instance as connected components of [[w-contractible rings]] as objects in the [[pro-étale site]]. See ([Bhatt-Scholze 13](#BhattScholze13)).

=--

## Related concepts

* [[compactification]]

* [[one-point compactification]]

* [[end compactification]]

* [[Bohr compactification]]

* [[Kaluza-Klein compactification]]

## References

Lecture notes include

* Tarun Chitra, _The Stone-Cech Compactification_ 2009 [pdf](httP://www.math.cornell.edu/~riley/Teaching/Topology2009/essays/chitra.pdf)

* Brian Bockelman, _Functional Analysis Notes, [The Stone-Cech compactification](http://www.math.unl.edu/~s-bbockel1/929/node16.html)_

Discussion in the context of the [[pro-etale site]] is in 

* [[Bhargav Bhatt]], [[Peter Scholze]], _The pro-&#233;tale topology for schemes_ ([arXiv:1309.1198](http://arxiv.org/abs/1309.1198))
 {#BhattScholze13}


See also

* Wikipedia, _[Stone&#8211;&#268;ech compactification](https://en.wikipedia.org/wiki/Stone%E2%80%93%C4%8Cech_compactification)_

[[!redirects Stone-Cech compactification]]
[[!redirects Stone-Cech compactifications]]
[[!redirects Stone-Čech compactification]]
[[!redirects Stone-Čech compactifications]]
[[!redirects Stone–Cech compactification]]
[[!redirects Stone–Cech compactifications]]
[[!redirects Stone–Čech compactification]]
[[!redirects Stone–Čech compactifications]]
[[!redirects Stone--Cech compactification]]
[[!redirects Stone--Cech compactifications]]
[[!redirects Stone--Čech compactification]]
[[!redirects Stone--Čech compactifications]]