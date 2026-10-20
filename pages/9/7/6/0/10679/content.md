
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


\tableofcontents


## Definition

The [[forgetful functor]]/[[full and faithful functor|full and faithful]] [[subcategory|subcategory inclusion]]  from [[compact topological spaces|compact]] [[Hausdorff topological spaces]]  into all [[topological spaces]] 

$$
  U \;\colon\; Top_{CHaus} \hookrightarrow Top
$$ 

has a [[left adjoint]]

$$ 
  \beta \;\colon\; Top \longrightarrow Top_{CHaus}
$$

which sends a general [[topological space]] to a [[compact Hausdorff space]], called its _Stone-Čech compactification_. This hence exhibits $Top_{CHaus}$ as a [[reflective subcategory]] of all of [[Top|$Top$]].

The Stone-Čech compactification is in general "very large", even for "ordinary" non-compact spaces such as the [[real line]].

For more details see at _[compact Hausdorff space -- Stone-&#268;ech compactification](compact+Hausdorff+space#StoneCechCompactification)_

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

The Stone-Čech compactification of a [[discrete topological space]]
is an [[extremally disconnected topological space]].
By a theorem by Gleason, these are precisely the [[projective objects]]
in the [[category]] of [[compact topological space|compact]]
[[Hausdorff topological spaces]].

Such spaces appear for instance as connected components of [[w-contractible rings]] as objects in the [[pro-étale site]]. See [Bhatt & Scholze 2013](#BhattScholze13).

=--

## Related concepts

* [[compactification]]

* [[one-point compactification]]

* [[end compactification]]

* [[Bohr compactification]]

* [[Kaluza-Klein compactification]]

## References

Lecture notes include

* Tarun Chitra: _The Stone-Cech Compactification_ (2009) &lbrack;[[Chitra-StoneCech.pdf|pdf:file]]&rbrack;

* Brian Bockelman: *The Stone-Cech compactification* &lbrack;[archive](https://web.archive.org/web/20150322234843/http://www.math.unl.edu/~s-bbockel1/929/node16.html)&rbrack;

Discussion in the context of the [[pro-etale site]] is in 

* {#BhattScholze13} [[Bhargav Bhatt]], [[Peter Scholze]], _The pro-&#233;tale topology for schemes_ ([arXiv:1309.1198](https://arxiv.org/abs/1309.1198))
 


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