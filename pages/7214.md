
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

+-- {: .num_defn #DeltaGeneratedSpace} 
###### Definition
**($\Delta$-Generated spaces)**

A **$\Delta$-generated space** ([Smith](#Smith), [Dugger 03](#Dugger03)) is a [[topological space]] $X$ whose topology is the [[weak topology|final topology]] induced by all [[continuous functions]] of the form $\Delta^n_{top} \to X$, hence whose [[domain]] $\Delta^n_{top}$ is one of the standard [[topological simplices]], for $n \in \mathbb{N}$.

A [[morphism]] between $\Delta$-generated spaces is just a [[continuous function]], hence the [[category]] of $\Delta$-generated spaces is the [[full subcategory]] on these spaces inside all [[Top|TopologicalSpaces]], 

=--

+-- {: .num_remark #AsColimitsOfTopologicalSimplices} 
###### Remark
**(as colimits of topological simplices)**

Equivalently, the [[class]] of $\Delta$-generated spaces is the closure of the set of [[topological simplices]] $\Delta^n_{top}$ under [[small colimits]] in [[topological spaces]] (see at _[[Top]] -- [universal constructions](Top#UniversalConstructions)_).

=--

+-- {: .num_remark #AsEuclideanGeneratedSpaces} 
###### Remark
**(as Euclidean-generated spaces)**

For each $n$ the [[topological simplex]] $\Delta^n$ is a [[retract]] of the ambient [[Euclidean space]]/[[Cartesian space]] $\mathbb{R}^n$ (as a [[inhabited|non-empty]] [[convex subset]] of a [[Euclidean space]] it is in fact an [[absolute retract]]). Hence the [[identity function]] on $\Delta^n$ factors as

$$
  id 
  \;\colon\; 
  \Delta^n_{top}
  \overset{i_n}{\hookrightarrow}
  \mathbb{R}^n
  \overset{p_n}{\longrightarrow}
  \Delta^n_{top}
  \,.
$$

It follows that every [[continuous function]] $f$ with [[domain]] the [[topological simplex]] [[extension|extends]] as a [[continuous function]] to [[Euclidean space]]:

$$
  \array{
    \Delta^m_{top}
    &\overset{f}{\longrightarrow}&
    X
    \\
    \mathllap{{}^{i_n}}\big\downarrow & \nearrow _{\mathrlap{\exists}}
    \\
    \mathbb{R}^n
  }
$$

Therefore the condition that a topological space $X$ be $\Delta$-generated (Def. \ref{DeltaGeneratedSpace}) is equivalent to saying that its topology is [[final topology|final]] with respect to all continuous functions $\mathbb{R}^n \to X$ out of [[Euclidean spaces|Euclidean]]/[[Cartesian spaces]]. 

=--

+-- {: .num_remark #AsDTopologicalSpaces} 
###### Remark
**(as D-topological spaces)**

By Prop. \ref{AdjunctionBetweenTopologicalSpacesAndDiffeologicalSpaces} below, the Euclidean-generated spaces and hence, by Remark \ref{AsEuclideanGeneratedSpaces}, the $\Delta$-generated spaces, are equivalently those that arise from equipping a [[diffeological space]] with its [[D-topology]], hence are, in this precise sense, the _D-topological spaces_. Luckily, "D-topological space" may also serve as an abbreviation for "Delta-generated topological space".

=--


## Properties

### As a convenient category of topological spaces

+-- {: .num_prop #EuclideanGeneratedSpacesAreConvenient}
###### Proposition
**([[Euclidean-generated spaces]] are [[convenient category of topological spaces|convenient]])**

The [[category]] of [[Euclidean-generated spaces]]/$\Delta$-generated spaces (Def. \ref{DeltaGeneratedSpace}) is 
a [[convenient category of topological spaces]] in that:

* it contains all [[CW-complexes]] ([SYH 10, Cor. 4.4](#SYH10)),

* it is [[complete category|complete]] and [[cocomplete category]] ([SYH 10, Prop. 3.4](#SYH10)),

* it is [[locally presentable category|locally presentable]] ([FR 08, Cor. 3.7](#FajstrupRosicky08))

* it is [[cartesian closed]] ([SYH 10, Cor. 4.6](#SYH10)):

  its [[mapping space]] [[internal homs]] $Maps(X,Y)$ are given by the [[D-topology]] of the [[internal homs]] in [[diffeological spaces]] (i.e. [[closed monoidal structure on presheaves|in presheaves]]) between [[continuous diffeologies]] ([SYH 10, Prop. 4.7](#SYH10)):

  $$
    Maps(X,Y) \;\coloneqq\; Dtplg\big( [ Cdfflg(X), Cdfflg(Y) ] \big) 
  $$



=--



### Coreflection into all topological spaces


[[!include adjunction between topological spaces and diffeological spaces]]


### Topological homotopy type and diffeological shape
 {#OnTopologicalHomotopyTypeAndDiffeologicalShape}


[[!include diffeological singular simplicial set -- definition]]



[[!include topological homotopy type is cohesive shape of continuous diffeology -- proposition]]



### Model category structure

+-- {: .num_prop }
###### Proposition

The category of $\Delta$-generated spaces carries the [[mathematical structure|structure]] of a [[cofibrantly generated model category]] with the same generating (acyclic) cofibrations as for the [[classical model structure on topological spaces]] and such that the [[coreflective subcategory|coreflection]] into all [[Top|TopologicalSpaces]] (Prop. \ref{AdjunctionBetweenTopologicalSpacesAndDiffeologicalSpaces}) is a [[Quillen equivalence]] to the [[classical model structure on topological spaces]].

=--

([Haraguchi 13, Theorem 3.3](#Haraguchi13))


## Related concepts

* [[Euclidean-generated ∞-groupoid]]

* [[compactly generated topological space]]

## References

### General

$\Delta$-generated spaces were originally proposed by [[Jeff Smith]] as a [[nice category of spaces]] for [[homotopy theory]].  

* {#Smith} [[Jeff Smith]], _A really convenient category of topological spaces_ (unpublished and possibly non-existent, according to [Dugger 03, p. 4](#Dugger03))

* {#Dugger03} [[Daniel Dugger]], _Notes on Delta-generated spaces_, 2003 ([web](https://pages.uoregon.edu/ddugger/delta.html), [[DuggerDeltaGenerated.pdf:file]])

A [[proof]] that the category of $\Delta$-generated spaces is [[locally presentable category|locally presentable]] is in:

* {#FajstrupRosicky08} [[Lisbeth Fajstrup]], [[Jiří Rosický]], _A convenient category for directed homotopy_, Theory and Applications of Categories, Vol. 21, 2008, No. 1, pp 7-20. ([arXiv:0708.3937](https://arxiv.org/abs/0708.3937), [tac:21-01](http://www.tac.mta.ca/tac/volumes/21/1/21-01abs.html))

See also at _[[directed homotopy theory]]_.

The [[model structure on Delta-generated topological spaces]] [[Quillen equivalence|Quillen equivalent]] to the [[classical model structure on topological spaces]] is due to 

*  {#Haraguchi13} [[Tadayuki Haraguchi]], _On model structure for coreflective subcategories of a model category_, Math. J. Okayama Univ.57(2015), 79–84 ([arXiv:1304.3622](http://arxiv.org/abs/1304.3622), MR3289294, Zbl 1311.55027)

### Relation to diffeological spaces

Relation to [[diffeological spaces]]:

* {#SYH10} [[Kazuhisa Shimakawa]], K. Yoshida, [[Tadayuki Haraguchi]], _Homology and cohomology via enriched bifunctors_, Kyushu Journal of Mathematics, 2018 Volume 72 Issue 2 Pages 239-252 ([arXiv:1010.3336](https://arxiv.org/abs/1010.3336), [doi:10.2206/kyushujm.72.239]( https://doi.org/10.2206/kyushujm.72.239))

* {#CSW13} [[J. Daniel Christensen]], Gord Sinnamon, [[Enxin Wu]], _The $D$-topology for diffeological spaces_, Pacific Journal of Mathematics 272 (1), 87-110, 2014 ([arXiv:1302.2935](http://arxiv.org/abs/1302.2935), [doi:10.2140/pjm.2014.272.87](https://msp.org/pjm/2014/272-1/p04.xhtml))


[[!redirects Delta-generated topological spaces]]

[[!redirects Delta-generated space]]
[[!redirects Delta-generated spaces]]

[[!redirects Euclidean-generated space]]
[[!redirects Euclidean-generated spaces]]

[[!redirects Euclidean-generated topological space]]
[[!redirects Euclidean-generated topological spaces]]

[[!redirects D-topological space]]
[[!redirects D-topological spaces]]

[[!redirects ∞-generated space]]
[[!redirects ∞-generated spaces]]

[[!redirects ∞-generated topological space]]
[[!redirects ∞-generated topological spaces]]
