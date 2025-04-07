

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[canonical model structure]] on the 1-[[category]] [[Grpd]] of [[groupoids]] (with [[functors]] between them) is a presentation of the [[(2,1)-category]] of [[groupoids]], [[functors]] and [[natural isomorphisms]].

This is one flavor of the various [[canonical model structures]] on classes of [[categories]] and [[higher categories]].

## Definition


\begin{definition}
\label{TheDefinition}
Let [[Grpd]] be the 1-[[category]] of [[small category|small]] [[groupoids]] with [[functors]] between them. Say that a morphism in $Grpd$ --- a [[functor]] $f \colon C \longrightarrow D$ --- is: 

* a _[[weak equivalence]]_ iff it is an [[equivalence of categories]] hence a [[weak homotopy equivalence]] of groupoids,

* a _[[fibration]]_ iff it is an [[isofibration]],

* a _[[cofibration]]_ iff it is an [[isocofibration]], hence  [[injective-on-objects functor|injective on objects]].

\end{definition}

\begin{proposition}
\label{ExistenceAndBasicProperties}

Equipped with the classes from Def. \ref{TheDefinition} [[Grpd]] is a [[model category]] $Grpd_{can}$, which is

* [[combinatorial model category|combinatorial]] 

  (in particular [[cofibrantly generated model category|cofibrantly generated]]),

* [[proper model category|proper]],

* [[simplicial model category|simplicial]] 

  (induced under the [[simplicial nerve]] by the canonical enrichment over itself),

* [[cartesian monoidal model category|cartesian monoidal]].

\end{proposition}
The claim that the classes in Def. \ref{TheDefinition} indeed give a model structure is due to [Anderson 1978](#Anderson78), repeated by [Bousfield 1989](#Bousfield89), both without proof. Proofs appear in [Joyal & Tierney 1991, Thm. 2](#JoyalTierney91) (there in the generality of [[internal groupoid|groupoids internal to]] [[topoi]], hence: of [[stacks]]) and [Strickland 2000](#Strickland00). Properness follows immediately (by [this Prop.](proper+model+category#AllObjectsFibrantImpliesRightProper)) because all objects are evidently [[bifibrant objects|bifibrant]]. In the context of the [[model structure for (2,1)-sheaves]] the structure  is considered, [Hollander 2001, theorem 2.1](#Hollander01) who states also the [[cofibrantly generated model category|cofibrant generation]] and [[simplicial model category|simplicial enrichment]], without proof. 
Since [[Grpd]] is a [[locally presentable category]] (for instance by [this Prop](sketch#LimitSketchableCategoriesAreLocallyPresentable), observing that groupoids are the models of a [[limit sketch]], namely given by diagrams as shown at *[[internal category]]*) this implies that $Grpd_{can}$ is [[combinatorial model category|combinatorial]].
Finally the [[cartesian monoidal model category|cartesian model structure]] follows just as for the [[canonical model structure on Cat]], see [there](canonical+model+structure+on+Cat#CartesianMonoidalModelStructure).

## Properties

### Relation to canonical model structure on $Cat$

+-- {: .num_remark}
###### Remark

The model structure $Grpd_{nat}$ is the restriction of the
[[canonical model structure on Cat]] from [[categories]] to groupoids.

=--

See at *[[canonical model structure]]* for more.


### Relation to classical model structure on $sSet$

Consider the pair of [[adjoint functors]]
\[
  \label{NerveAdjunction}
  (\tau \dashv N) 
  \,\colon\, 
  Grpd 
    \underoverset
      { \underset{N}{\longrightarrow} }
      { \overset{\tau}{\longleftarrow} }
      { \bot }
  sSet
\]
where $N$ is the [[simplicial nerve]] with values in the category [[sSet]] of [[simplicial sets]].

One readily checks that: 

\begin{proposition}
With the canonical model structure on $Grpd$ (from Prop. \ref{ExistenceAndBasicProperties}) and the [[classical model structure on simplicial sets]], (eq:)NerveAdjunction is a [[Quillen adjunction]]
$$
  (\tau \dashv N) 
  \,\colon\, 
  Grpd_{can} 
    \underoverset
      { \underset{N}{\longrightarrow} }
      { \overset{\tau}{\longleftarrow} }
      { \bot_{\mathrlap{Qu}} }
  sSet_{Qu}
  \,.
$$
\end{proposition}
(cf. [Hollander 2001, Cor. 2.3](#Hollander01))

In fact:
\begin{proposition}
$Grpd_{can}$ is the [[transferred model structure]] obtained from [[classical model structure on simplicial sets|$sSet_{Qu}$]] under (eq:NerveAdjunction).
\end{proposition}
(cf. [Hollander 2001, Lem. 2.4](#Hollander01))


## Related concepts

* [[canonical model structure]]

* [[canonical model structure on Cat]]

* **canonical model structure on $Grpd$**

  * [[model structure for n-groupoids]]

  * [[model structure for ∞-groupoids]]

* [[canonical model structure on Operad]]


## References

Some aspects (like the pullback stability of fibrations of groupoids in its prop. 2.8) appeared in 

* {#Brown70} [[Ronnie Brown]], *Fibrations of groupoids*, Journal of Algebra **15** 1 (1970) 103-132 \[<a href="https://doi.org/10.1016/0021-8693(70)90089-X">doi:10.1016/0021-8693(70)90089-X</a>, [pdf](https://groupoids.org.uk/pdffiles/fibrationsgpds.pdf)\]

The existence of the model structure is stated (without proof) in:

* {#Anderson78} [[Donald W. Anderson]], p. 783 (12 of 37) in: *Fibrations and geometric realization*,  Bull. Amer. Math. Soc. **84** 5 (1978) 765-788 &lbrack;[euclid:1183541139](http://projecteuclid.org/euclid.bams/1183541139)&rbrack;

and (by referencing Anderson, still without proof) in:

* {#Bousfield89} [[Aldridge Bousfield]], _Homotopy Spectral Sequences and Obstructions_ , Israel Journal of Math., **66** 1-3 (1989) 54-105 &lbrack;[doi:10.1007/BF02765886](https://doi.org/10.1007/BF02765886)

Proofs are spelled out in:

* {#JoyalTierney91} [[André Joyal]], [[Myles Tierney]], Thm. 2 (p. 221) *Strong stacks and classifying spaces*, in: *Category Theory* Lecture Notes in Mathematics **1488**, Springer (1991) 213-236 &lbrack;[doi:10.1007/BFb0084222](https://doi.org/10.1007/BFb0084222)&rbrack;

  > (in the generality of [[internal groupoids]] in a [[topos]], hence of *[[stacks]]*)


* {#Strickland00} [[Neil Strickland]], §6.1 of: _$K(n)$-local duality for finite groups and groupoids_ , Topology **39** 4 (2000) &lbrack;[arXiv:math/0011109](https://arxiv.org/abs/math/0011109), <a href="https://doi.org/10.1016/S0040-9383(99)00031-2">doi:10.1016/S0040-9383(99)00031-2</a>&rbrack;


The model structure on functors with values in $Grpd_{nat}$ (a [[model structure for (2,1)-sheaves]]):

* {#Hollander01} [[Sharon Hollander]], §2.1 in: *A homotopy theory for stacks*, Israel Journal of Mathematics **163** 1 (2008) 93-124 &lbrack;[arXiv:math.AT/0110247](http://arxiv.org/abs/math.AT/0110247), [doi:10.1007/s11856-008-0006-5](https://doi.org/10.1007/s11856-008-0006-5)&rbrack;

A model structure on $Cat$ but localized such as to make the fibrant objects be groupoids:

* {#Sharma23} [[Amit Sharma]], *Picard groupoids and $\Gamma$-categories*, [[Cahiers]] **LXIV** 3 (2023) &lbrack;[arXiv:2002.05811](https://arxiv.org/abs/2002.05811), [pdf](http://cahierstgdc.com/wp-content/uploads/2023/07/SHARMA_LXIV-3.pdf)&rbrack;

(insert description of article here):

* {#Hughes25} [[Calum Hughes]], *The algebraic internal groupoid model of Martin-Löf type theory* ([arXiv:2503.17319](https://arxiv.org/abs/2503.17319))

[[!redirects natural model structure on groupoids]]


[[!redirects canonical model structure on Grpd]]

[[!redirects model structure on groupoids]]
[[!redirects model structures on groupoids]]


