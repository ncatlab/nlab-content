
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

A **$\Delta$-generated space** is a [[topological space]] $X$ whose topology is the [[final structure|final topology]] induced by all [[continuous functions]] $\Delta^n_{top} \to X$, where $\Delta^n_{top}$ are the standard [[topological simplices]].

Equivalently, the class of $\Delta$-generated spaces is the closure of the set of [[topological simplices]] $\Delta^n_{top}$ under [[small colimits]] in [[topological spaces]] (see at _[[Top]] -- [universal constructions](Top#UniversalConstructions)_).

## Properties

### A nice category of topological spaces

+-- {: .num_prop }
###### Proposition

The category of $\Delta$-generated spaces is 

* [[coreflective subcategory|coreflective]] in [[Top]].

* [[locally presentable category|locally presentable]] 

* [[cartesian closed]],

* thus a [[nice category of spaces]],

=--

([Fajstrup-Rosický 08](#FajstrupRosicky08), [Shimakawa-Yoshida-Haraguchi 10](#SYH10))


### Coreflection into all topological spaces


[[!include adjunction between topological spaces and diffeological spaces]]



### Model category structure

+-- {: .num_prop }
###### Proposition

The category of $\Delta$-generated spaces carries the [[mathematical structure|structure]] of a [[cofibrantly generated model category]] with the same generating (acyclic) cofibrations as for the [[classical model structure on topological spaces]] and such that the [[coreflective subcategory|coreflection]] (Prop. \ref{AdjunctionBetweenTopologicalSpacesAndDiffeologicalSpaces}) is a [[Quillen equivalence]] to the [[classical model structure on topological spaces]].

=--

([Haraguchi 13, Theorem 3.3](#Haraguchi13))



## References

### General

$\Delta$-generated spaces were originally proposed by [[Jeff Smith]] as a [[nice category of spaces]] for [[homotopy theory]].  An account is in

* [[Daniel Dugger]], _Notes on Delta-generated spaces_, 2003 ([web](https://pages.uoregon.edu/ddugger/delta.html), [[DuggerDeltaGenerated.pdf:file]])

A [[proof]] that the category of $\Delta$-generated spaces is [[locally presentable category|locally presentable]] is in:

* {#FajstrupRosicky08} [[Lisbeth Fajstrup]], [[Jiří Rosický]], _A convenient category for directed homotopy_, Theory and Applications of Categories, Vol. 21, 2008, No. 1, pp 7-20. ([tac:21-01](http://www.tac.mta.ca/tac/volumes/21/1/21-01abs.html))

See also at _[[directed homotopy theory]]_.

The [[model structure on Delta-generated topological spaces]] [[Quillen equivalence|Quillen equivalent]] to the [[classical model structure on topological spaces]] is due to 

*  {#Haraguchi13} [[Tadayuki Haraguchi]], _On model structure for coreflective subcategories of a model category_ ([arXiv:1304.3622](http://arxiv.org/abs/1304.3622), MR3289294, Zbl 1311.55027)

### Relation to diffeological spaces

Relation to [[diffeological spaces]]:

* {#SYH10} [[Kazuhisa Shimakawa]], K. Yoshida, [[Tadayuki Haraguchi]], _Homology and cohomology via enriched bifunctors_, Kyushu Journal of Mathematics, 2018 Volume 72 Issue 2 Pages 239-252 ([arXiv:1010.3336](https://arxiv.org/abs/1010.3336), [doi:10.2206/kyushujm.72.239]( https://doi.org/10.2206/kyushujm.72.239))

* {#CSW13} [[J. Daniel Christensen]], Gord Sinnamon, [[Enxin Wu]], _The $D$-topology for diffeological spaces_, Pacific Journal of Mathematics 272 (1), 87-110, 2014 ([arXiv:1302.2935](http://arxiv.org/abs/1302.2935), [doi:10.2140/pjm.2014.272.87](https://msp.org/pjm/2014/272-1/p04.xhtml))


[[!redirects Delta-generated topological spaces]]

[[!redirects Delta-generated space]]
[[!redirects Delta-generated spaces]]

[[!redirects ∞-generated space]]
[[!redirects ∞-generated spaces]]

[[!redirects ∞-generated topological space]]
[[!redirects ∞-generated topological spaces]]
