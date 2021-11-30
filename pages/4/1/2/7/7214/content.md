
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

A **$\Delta$-generated space** (alias **numerically generated space**) ([Smith](#Smith), [Dugger 03](#Dugger03)) is a [[topological space]] $X$ whose topology is the [[weak topology|final topology]] induced by all [[continuous functions]] of the form $\Delta^n_{top} \to X$, hence whose [[domain]] $\Delta^n_{top}$ is one of the standard [[topological simplices]], for $n \in \mathbb{N}$.

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



### Coreflection into all topological spaces
 {#CoreflectionIntoAllTopologicalSpaces}


[[!include adjunction between topological spaces and diffeological spaces]]


### Topological homotopy type and diffeological shape
 {#OnTopologicalHomotopyTypeAndDiffeologicalShape}


[[!include diffeological singular simplicial set -- definition]]



[[!include topological homotopy type is cohesive shape of continuous diffeology -- proposition]]



### Model category structure
 {#ModelCategoryStructure}


\begin{prop}
**([[model structure on Delta-generated topological spaces]])**
\linebreak
The category of $\Delta$-generated spaces carries the [[mathematical structure|structure]] of a [[cofibrantly generated model category]] with the same generating (acyclic) cofibrations as for the [[classical model structure on topological spaces]] and such that the [[coreflective subcategory|coreflection]] into all [[Top|TopologicalSpaces]] (Prop. \ref{AdjunctionBetweenTopologicalSpacesAndDiffeologicalSpaces}) is a [[Quillen equivalence]] to the [[classical model structure on topological spaces]].
\end{prop}

([Haraguchi 13, Theorem 3.3](#Haraguchi13))

This [[Quillen equivalence]] factors through the [[model structure on compactly generated topological spaces]] (e.g. [Gaucher 2007, p. 7](#Gaucher07)):


$$
  Top_{Qu}
  \underoverset
    { \underset{ k }{\longrightarrow} }
    { {\hookleftarrow} }
    { \;\;\;\;\;\;\simeq_{\mathrlap{Qu}}\;\;\;\;\;\; }
  k Top_{Qu}
  \underoverset
    { \underset{ D }{\longrightarrow} }
    { {\hookleftarrow} }
    { \;\;\;\;\;\;\simeq_{\mathrlap{Qu}}\;\;\;\;\;\; }
  D Top_{Qu}
  \,.
$$



### As a convenient category of topological spaces
 {#AsAConvenientCategoryOfTopologicalSpaces}

\begin{prop}\label{CartesianClosure}
  The [[category]] of [[Euclidean-generated spaces]]/$\Delta$-generated spaces (Def. \ref{DeltaGeneratedSpace}) is a [[Cartesian closed category]]. 

Explicitly, the [[internal hom]] $Maps_{DTop}$ is, equivalently:

* the image under $Cdfflg$  (eq:AdjointFunctorsBetweenTopSpAndDifflgSp) of the [[mapping space]] $Maps_{Top}(X,Y)$ with the [[compact-open topology]]:

  $$
    Maps_{DTop}(X,Y)
    \;\simeq\;   
    Cdfflg
    \big(
      Maps_{Top}
      (
        X
        ,\,
        Y
      )
    \big)
    \,,
  $$

* the image under [[D-topology|$Dtplg$]]  (eq:AdjointFunctorsBetweenTopSpAndDifflgSp) of the [[internal hom]] $Maps_{Dfflg}$ formed in [[diffeological spaces]]:

  $$
    Maps_{DTop}(X,Y) 
      \;\simeq\; 
    Dtplg
    \big(  
      Maps_{Dfflg}
      (
        X
        ,\, 
        Y
      )
    \big) 
    \,.
  $$


\end{prop}
The first statement is a special case of [Vogt 1971, Thm. 3.6](#Vogt71), as highlighted in [Gaucher 2007, Sec. 2](#Gaucher07).
The second statement is the image of [SYH 10, Prop. 4.7](#SYH10) under $Dtplg$ (using that $\nu = T \circ D$, in their notation from p. 4).

In fact, [SYH 10, Prop. 4.7](#SYH10) state something stronger, topologically characterizing $Maps_{Dfflg}(X,Y)$ even before applying $Dtplg$ to it. This stronger statement has a nice form when specialized to [[CW-complexes]]:


\begin{proposition}\label{CWComplexesAreDTopologicalSpaces}
  The [[category]] of [[Euclidean-generated spaces]]/$\Delta$-generated spaces (Def. \ref{DeltaGeneratedSpace}) contains all [[CW-complexes]].   
\end{proposition}
([SYH 10, Cor. 4.4](#SYH10))

\begin{proposition}\label{DiffeologicalMapsOutOfCWComplexes}
**([[diffeological space|diffeological]] [[internal hom]] out of [[CW-complexes]])**
\linebreak

If $X$ is a [[CW-complex]],
regarded as an object in $DTopSp$ via Prop. \ref{CWComplexesAreDTopologicalSpaces},
then for every $A \,\in\, DTopSp$
their [[internal hom]] formed in [[diffeological spaces]]
is [[isomorphism|isomorphic]] to the image under $Cdffl$
(eq:AdjointFunctorsBetweenTopSpAndDifflgSp)
of the [[mapping space]] $Maps_{Top}$ with its [[compact open topology]]: 
$$
  X \,\in\, CWComplex \hookrightarrow DTopSp
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  \underset{
    A \,\in\, DTopSp
  }{\forall}
  Maps_{Dfflg}
  \big(
    X
    ,\,
    A
  \big)
  \;\;
  \simeq
  Cdfflg
  \,
  Maps_{Top}
  \left(
    X
    ,\,
    A
  \right)
  \,.
$$
\end{proposition}
\begin{proof}
  This is the following combination of statements from [SYH 10](#SYH10):

1. Prop. 4.7 there says that, in general:
  
   $$
     Maps_{Dfflg}\big( X ,\, A\big)
     \;\simeq\;
     Cdfflgl
     \big(
       \mathbf{smap}(X,Y)
     \big)
   $$

   (where "$\mathbf{smap}$" is defined on their p. 6),

1. Prop. 4.3 there implies that, when $X$ is a CW-complex, as assumed here:

   $$
     Cdfflg 
     \big(
       \mathbf{smap}(X,Y)    
     \big)
     \;\simeq\;
     Cdfflg 
     \big(
       Maps_{Top}(X,Y)        
     \big) 
     \,.
   $$

\end{proof}


In summary:

+-- {: .num_prop #EuclideanGeneratedSpacesAreConvenient}
###### Proposition
**([[Euclidean-generated spaces]] are [[convenient category of topological spaces|convenient]])**

The [[category]] of [[Euclidean-generated spaces]]/$\Delta$-generated spaces (Def. \ref{DeltaGeneratedSpace}) is 
a [[convenient category of topological spaces]] in that:

* it is [[coreflective subcategory|coreflective]] in [[TopSp]] (by Prop. \ref{AdjunctionBetweenTopologicalSpacesAndDiffeologicalSpaces})

* it is [[complete category|complete]] and [[cocomplete category]]

(by [Vogt 1971](#Vogt71); [SYH 10, Prop. 3.4](#SYH10))

* it is [[locally presentable category|locally presentable]] ([FR 08, Cor. 3.7](#FajstrupRosicky08)),

* it contains all [[CW-complexes]] (Prop. \ref{CWComplexesAreDTopologicalSpaces}),

* it is [[cartesian closed]], with [[internal hom]] expressible as in Prop. \ref{CartesianClosure}.

=--

Moreover, in further summary of the discussion further above, this [[convenient category of topological spaces]] is:

1. a [[full subcategory]] of the [[quasi-topos]] of [[diffeological spaces]] (see [there](diffeological+space#RelationToTopologicalSpaces)), 

1. which is in turn a [[full subcategory]] of the [[cohesive topos]] of [[smooth sets]] (see [there](geometry+of+physics+--+smooth+sets#DiffeologicalSpacesAreTheConcreteSmoothSets));

1. which in turn is a [[full sub-(infinity,1)-category|full sub-$(\infty,1)$-category]] of the [[cohesive (infinity,1)-topos|cohesive $(\infty,1)$-topos]] of [[smooth infinity-groupoids|smooth $\infty$-groupoids]]

such that the canonical [[shape modality]] (the [[shape via cohesive path ∞-groupoid|smooth path ∞-groupoid construction]]) still sees the correct underlying [[homotopy type]] of topological spaces ([[schreiber:Proper Orbifold Cohomology|SS20, Ex. 3.18]], see also at [[model structure on Delta-generated topological spaces]]):

\begin{imagefromfile}
    "file_name": "TopologicalConvenienceBySmoothGroupoids210930.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [SS21](https://ncatlab.org/schreiber/show/Equivariant+principal+infinity-bundles)"
\end{imagefromfile}




## Related concepts

* [[Euclidean-generated ∞-groupoid]]

* [[compactly generated topological space]]

## References

### General

$\Delta$-generated spaces were originally proposed by [[Jeff Smith]] as a [[nice category of spaces]] for [[homotopy theory]].  

* {#Smith} [[Jeff Smith]], _A really convenient category of topological spaces_ (unpublished and possibly non-existent, according to [Dugger 03, p. 4](#Dugger03))

* {#Dugger03} [[Daniel Dugger]], _Notes on Delta-generated spaces_, 2003 ([web](https://pages.uoregon.edu/ddugger/delta.html), [[DuggerDeltaGenerated.pdf:file]])

A [[proof]] that the category of $\Delta$-generated spaces is [[locally presentable category|locally presentable]] is in:

* {#FajstrupRosicky08} [[Lisbeth Fajstrup]], [[Jiří Rosický]], Thm. 3.6 of: _A convenient category for directed homotopy_, Theory and Applications of Categories, Vol. 21, 2008, No. 1, pp 7-20. ([arXiv:0708.3937](https://arxiv.org/abs/0708.3937), [tac:21-01](http://www.tac.mta.ca/tac/volumes/21/1/21-01abs.html))

See also at _[[directed homotopy theory]]_.

The [[model structure on Delta-generated topological spaces]] [[Quillen equivalence|Quillen equivalent]] to the [[classical model structure on topological spaces]] is due to 

*  {#Haraguchi13} [[Tadayuki Haraguchi]], _On model structure for coreflective subcategories of a model category_, Math. J. Okayama Univ.57(2015), 79–84 ([arXiv:1304.3622](http://arxiv.org/abs/1304.3622), MR3289294, Zbl 1311.55027)


Discussion in the generality of subcategory-generated spaces, including [[compactly generated topological spaces]]:

* {#Gaucher07} [[Philippe Gaucher]], Section 2 of: *Homotopical interpretation of globular complex by multipointed d-space*, Theory and Applications of Categories, vol. 22, number 22, 588-621, 2009 ([arXiv:0710.3553](https://arxiv.org/abs/0710.3553))

along the lines of

* {#Vogt71} [[Rainer M. Vogt]], *Convenient categories of topological spaces for homotopy theory*,  Arch. Math 22, 545–555 (1971) ([doi:10.1007/BF01222616](https://doi.org/10.1007/BF01222616))

* {#EscardoLawsonSimpson04} [[Martín Escardó]], [[Jimmie Lawson]], [[Alex Simpson]], Section 3 of: *Comparing Cartesian closed categories of (core) compactly generated spaces*, Topology and its Applications Volume 143, Issues 1–3, 28 August 2004, Pages 105-145 ([doi:10.1016/j.topol.2004.02.011](https://doi.org/10.1016/j.topol.2004.02.011))

Discussion about the [[q-model structure]], the [[m-model structure]], the [[h-model structure]] and the notion of $\Delta$-Hausdorff $\Delta$-generated space (a natural separation condition for $\Delta$-generated spaces) in:

* {#Gaucher21} [[Philippe Gaucher]], Section 2 and Appendix B of: *Left properness of flows*, Theory and Applications of Categories, **37** 19 (2021) 562-612  ([arXiv:1907.01454](https://arxiv.org/abs/1907.01454), [TAC:37-19](http://www.tac.mta.ca/tac/volumes/37/19/37-19abs.html))

### Relation to diffeological spaces

Relation to [[diffeological spaces]]:

* {#SYH10} [[Kazuhisa Shimakawa]], K. Yoshida, [[Tadayuki Haraguchi]], _Homology and cohomology via enriched bifunctors_, Kyushu Journal of Mathematics, 2018 Volume 72 Issue 2 Pages 239-252 ([arXiv:1010.3336](https://arxiv.org/abs/1010.3336), [doi:10.2206/kyushujm.72.239]( https://doi.org/10.2206/kyushujm.72.239))

* {#CSW13} [[J. Daniel Christensen]], [[Gord Sinnamon]], [[Enxin Wu]], Sec. 3.2 of: _The $D$-topology for diffeological spaces_, Pacific Journal of Mathematics 272 (1), 87-110, 2014 ([arXiv:1302.2935](http://arxiv.org/abs/1302.2935), [doi:10.2140/pjm.2014.272.87](https://msp.org/pjm/2014/272-1/p04.xhtml))


[[!redirects Delta-generated topological spaces]]
[[!redirects Delta-generated space]]
[[!redirects Delta-generated spaces]]
[[!redirects Δ-generated topological space]]
[[!redirects Δ-generated topological spaces]]
[[!redirects Δ-generated space]]
[[!redirects Δ-generated spaces]]
[[!redirects numerically generated topological space]]
[[!redirects numerically generated topological spaces]]
[[!redirects numerically generated space]]
[[!redirects numerically generated spaces]]

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
