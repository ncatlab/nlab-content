
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

[[Serre fibration]] $\Leftarrow$ **Hurewicz fibration** $\Rightarrow$ [[Dold fibration]] $\Leftarrow$ [[shrinkable map]]

***

# Contents
* table of contents
{:toc}


## Definition

+-- {: .num_defn}
###### Definition

A [[continuous map]] $p \;\colon\; E\longrightarrow B$ of [[topological space]] is called a **Hurewicz fibration**  if it satisfies the [[right lifting property]] against all [[continuous functions]]

$$ 
  \sigma_0 
  \;\colon\; 
  X \cong X \times\{0\} 
    \xhookrightarrow{\phantom{---}} 
  X \times I
$$ 

including any [[topological space]] $X$ as one end of the [[cylinder]] over it (where $I \coloneqq [0,1]$ denotes the [[topological interval]]).

=--

+-- {: .num_remark}
###### Remark

In this context, the defining [[right lifting property]] is called the *[[homotopy lifting property]]*, because the maps from $X\times I$ are understood as [[homotopies]]. In more detail, for every space $X$, any homotopy $F:X\times I\to B$, and a continuous map $f:X\to E$, there is a homotopy $\tilde{F}:X\times I\to E$ such that $f =\tilde{F}
\circ\sigma_0 :=\tilde{F}_0$ and $F=p\circ\tilde{F}$: 

$$
  \array{
    X &\stackrel{f}\longrightarrow& E
    \\
    {}^{\mathllap{\sigma_0}}
    \big\downarrow 
      &{}^{\tilde{F}}\nearrow&  
    \big\downarrow {}^{\mathrlap{p}}
    \\
    X\times I &\stackrel{F}{\to}& B
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Strictly speaking, the "all" in this context should be interpreted to refer to all spaces in whatever ambient [[category]] of [[TopologicalSpaces]] one is working in, since frequently this is a [[convenient category of spaces]].  In theory, therefore, a map in such a category could be a Hurewicz fibration in that category without necessarily being a Hurewicz fibration in the category of *all* topological spaces, but in practice this usually doesn't make a whole lot of difference.

=--

Instead of checking the homotopy lifting property, one can instead solve a universal problem:


+-- {: .num_theorem}
###### Theorem

A map is a Hurewicz fibration precisely if it admits a [[Hurewicz connection]]. (See there for details.)

=--

## Properties

### Appearance in a model structure

There is a [[Quillen model category]] structure on [[Top]] where fibrations are Hurewicz fibrations, cofibrations are closed [[Hurewicz cofibrations]] and weak equivalences are [[homotopy equivalences]] -- see at *[[model structure on topological spaces]]* and specifically at *[[Strøm's model category]]*. 

There is a version of Hurewicz fibrations for [[pointed spaces]], as well as in the [[slice category]] $Top/B_0$ where $B_0$ is a fixed base (the [[slice model structure]]).

There is also a model category whose fibrations are the Hurewicz fibrations and whose weak equivalences are the [[weak homotopy equivalences]], obtained by [[mixed model structure|mixing]] the above model structure with the [[classical model structure on topological spaces]].

### Relation to Serre fibrations

Every Hurewicz fibration is a [[Serre fibration]].  Conversely, [[a Serre fibration between CW-complexes is a Hurewicz fibration]].

### Local recognition over numerable open covers
 {#LocalRecognition}

The following proposition says that being a Hurewicz fibration is a *local property* with respect to the [[codomain]] space, at least as long as the local [[open cover]] used is [[numerable open cover|numerable]].

\begin{prop}\label{MapIsHurewiczFibrationIfPullbackToNumerableCoverIsSo}
**(Local recognition of Hurewicz fibrations over numerable open covers)**\linebreak
  
Let $p \colon E \to B$ be a continuous function such that there exists a [[numerable open cover]] $U \overset{\phi}{\longrightarrow} B$ over which $E$ is a Hurewicz fibration, hence such that the [[pullback]] $\phi^\ast p$ is a Hurewicz fibration.

Then $p$ is a Hurewicz fibration

\end{prop}

A proof may be found spelled out in e.g. [May 99, Sec. 7.4](#May99)

## Abstract Hurewicz fibrations
 {#Abstractly}

The concept of Hurewicz fibrations makes sense also more generally in the presence of a (well behaved) [[interval object]], see for instance the early example of such in ([Kamps 72](#Kamps72)) and see ([Williamson 13](#Williamson13)) for review and further developments. Discussion with a view towards [[homotopy type theory]] is in ([Warren 08](#Warren08)).

## Examples
 {#Examples}

### Empty bundles

\begin{example}\label{EmptyBundlesAreHurewiczFibrations}
**([[empty bundles]] are [[Hurewicz fibrations]])** \linebreak
 All [[empty bundles]] $\varnothing \longrightarrow B$ are Hurewicz fibrations,  because none of the [[commuting squares]] that one would have to non-trivially [[lifting property|lift in]] actually exist:

$$
  \array{
    X &\overset{ \not \exists }{\longrightarrow}& \varnothing
    \\
    \big\downarrow && \big\downarrow
    \\
    X \times I &\longrightarrow& B
    \mathrlap{\,,}
  }
$$

since the [[empty topological space]] is a [[strict initial object]]: There is *no* morphism to it from any [[inhabited space]] $X$ 

(If $X$ itself is [[empty topological space|empty]], then so is $X \times I$ and then a square only exists if $B$ in turn is empty. This square, consisting entirely of empty spaces, does have a unique lift, trivially, and hence also the empty bundle over the empty space is a Hurewicz fibration -- for what it's worth.)

\end{example}

### Covering spaces

+-- {: .num_example #CoveringSpaceIsHurewiczFibration}
###### Example
**([[covering spaces]] are Hurewicz fibrations)**

Every [[covering space]] projection is a Hurewicz fibration, by [this prop.](covering#space#HomotopyLiftingPropertyOfCoveringSpaces).

=--


### Fiber bundles
 {#FiberBundles}

\begin{prop}\label{NumerableFiberBundlesAreSerreFibrations}
**([[numerable fiber bundles]] are Hurewicz fibrations)** \linebreak

Every [[numerable fiber bundle]], hence in particular every [[fiber bundle]] over a [[paracompact topological space]], is a Serre fibration.

\end{prop}
\begin{proof}
  By definition of local triviality, 
  for a [[numerable fiber bundle]] $p \colon E \to B$ -- such as a [[fiber bundle]] over a [[paracompact topological space]] -- there exists a [[numerable open cover]] $\phi \colon U \to B$ such that the [[pullback bundle]] $\phi^\ast p$ is trivial, i.e. is the [[Cartesian product]] [[projection]]

$$
  \phi^\ast p \;\colon\; U \times F \longrightarrow U
$$

(for $F$ the [[typical fiber]]). Since such a projection is clearly a Hurewicz fibration the claim follows by the local recognition of Hurewicz fibrations over numerable open covers, from Prop. \ref{MapIsHurewiczFibrationIfPullbackToNumerableCoverIsSo}.
\end{proof}

Notice that the example of [[empty bundles]] (Example \ref{EmptyBundlesAreHurewiczFibrations}) is a special case of a [[fiber bundle]]: With [[typical fiber]] the [[empty topological space]].

## Related concept

* [[Hurewicz cofibration]]

* [[Strøm model structure]]

* [[Serre fibration]]

## References

The original article:

* [[Witold Hurewicz]], _On the concept of fiber space_, Proc. Nat. Acad. Sci. USA __41__ (1955) 956--961; ([doi:10.1073%2Fpnas.41.11.956](https://dx.doi.org/10.1073%2Fpnas.41.11.956), [jstor:89187](https://www.jstor.org/stable/89187), [pdf](http://www.pnas.org/content/41/11/956.full.pdf). MR0073987)


Review of Hurewicz fibrations, [[Hurewicz connections]] and related issues:

* [[James Eells]], Jr.: *Fibring spaces of maps*, in: Richard Anderson (ed.) *Symposium on infinite-dimensional topology*, Annals of Mathematics Studies **69**, Princeton University Press (1972, 2016) 43-57 &lbrack;[ISBN:9780691080871](https://press.princeton.edu/books/paperback/9780691080871/symposium-on-infinite-dimensional-topology-am-69-volume-69), [[Eells-FibringSpaces.pdf:file]]&rbrack;


Textbook accounts:

* {#tDKP70} [[Tammo tom Dieck]], [[Klaus Heiner Kamps]], [[Dieter Puppe]], Chapter II of: *Homotopietheorie*, Lecture Notes in Mathematics **157** Springer 1970 ([doi:10.1007/BFb0059721](https://link.springer.com/book/10.1007/BFb0059721))


* [[Alan Hatcher]], from p. 61 on in _Algebraic Topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html))

See also 

* [[R. Schwänzl]], [[R. Vogt]], _Strong cofibrations and fibrations in enriched categories_, 2002.

* the textbooks on algebraic topology by Whitehead and Spanier.

* {#May99} [[Peter May]], _[[A concise course in algebraic topology]]_,   University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

* {#Cutler20} [[Tyrone Cutler]], _Fibrations III -- Locally trivial maps and bundles_, 2020 ([pdf](https://www.math.uni-bielefeld.de/~tcutler/pdf/Fibrations%20III.pdf), [[CutlerFibrationsIII.pdf:file]])

Abstract analogues of Hurewicz fibrations can be found in 

* {#Kamps72} [[K.H.Kamps]], _Kan-Bedingungen und abstrakte Homotopietheorie_, Math. Z. 124,1972, 215 -236

summarised in 

* [[K. H. Kamps]], [[Tim Porter]], _Abstract Homotopy and Simple Homotopy Theory_ ([GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))

and further developed in 

* {#Williamson13} [[Richard Williamson]], _Cylindrical model structures_ ([arXiv:1304.0867](http://arxiv.org/abs/1304.0867), [web](http://rwilliamson-mathematics.info/cylindrical_model_structures.html))

Discussion with an eye towards [[homotopy type theory]] is in

* {#Warren08} [[Michael Warren]], _Homotopy theoretic aspects of constructive type theory_, 2008 ([PDF](http://mawarren.net/papers/phd.pdf)) {#Warren}

[[!redirects Hurewicz fibration]]
[[!redirects Hurewicz fibrations]]