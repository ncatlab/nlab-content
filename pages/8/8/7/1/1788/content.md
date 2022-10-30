
+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--


***


| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| There is... | $\vdash \ldots$ | We speak in the context of a ([[(∞,1)-topos|higher]]) [[topos]] $\mathbf{H}$, a _place where things may be_. (For the time being a ([[locally cartesian closed (infinity,1)-category|higher]]) [[locally cartesian closed category]] is sufficient.) | A [[topos]] for [[synthetic differential geometry|synthetic]] [[differential geometry]], such as $\mathbf{H} = $ [[sheaf topos|Sh]]$($[[SmthMfd]]$)$. Eventually a [[(∞,1)-topos|higher]] such topos: $\mathbf{H} = $ [[Smooth∞Grpd]] or [[SynthDiff∞Grpd]] or [[SmoothSuper∞Grpd]] or ... | _[Smooth spaces](#SmoothSpaces)_ and _[Smooth homotopy types](#SmoothnGroupoids)_  |
| There is a thing $x$ of type $X$. | $\vdash\; x \colon X$ | An [[element]] $\left(* \stackrel{x}{\to} X\right) \in Mor(\mathbf{H})$ of an [[object]] $X$ of $\mathbf{H}$. | A point $x$ in a [[smooth infinity-groupoid|smooth moduli stack]] $X$. | _[Judgements about types and terms](#Judgments)_ |
| There is a type $X$ of things $x$. | $\vdash\; X \colon Type$ | An [[element]] $(* \stackrel{\vdash X}{\to} Obj) \in Mor(\mathbf{H})$ of the [[small object|small]]-[[object classifier]] $Obj$ of $\mathbf{H}$. | A point in the _[[moduli stack]] of all [[small object|small]] moduli stacks_. | _[Judgements about types and terms](#Judgments)_  |
| Given a thing $x$ of type $X$ there is a thing $a(x)$ of type $A(x).$ | $x \colon X\;\vdash\; a(x) \colon A(x)$ | An [[element]] of a morphism $(A \to X)$ $\left(\array{ X &&\stackrel{a}{\to}&& A \\ & {}_{\mathllap{id}}\searrow &\swArrow& \swarrow_{} \\ && X }\right)$ in the [[slice (infinity,1)-topos|slice topos]] $\mathbf{H}_{/X}$. | An $X$-family  in a moduli stack [[bundle]] $A$ over $X$. | _[Slice categories](#SliceCategories)_ and _[Slice toposes](#SliceToposes)_ and _[Slice ∞-Toposes](#SlicedInfinityToposes)_ |
|  There is the collection of all things $a(x)$ for all $x$. | $\vdash\; \left(\sum_{x \colon X} A\left(x\right)\right) \colon Type$ | The [[dependent sum]]/[[left adjoint]] to the [[product]]: $\array{ \mathbf{H}_{/X} &\stackrel{X_!}{\to} & \mathbf{H} \\ (A \to X) &\mapsto& A \in \mathbf{H}} $ | The total space of a [[bundle]]. | _[Natural deduction rules for dependent sum types](#DependentSumTypes)_ |
| There is a thing $t$ in the collection of all things $a(x)$ for all $x$. | $\vdash\; t \colon \sum_{x \colon X} A(x)$ |  An element $*\stackrel{t}{\to} A$ of the total space object. | A point in the [[moduli stack]] $A$ over $X$. | |  
| There is an assignment $f$ of an $a(x)$ to each $x$. | $\vdash \; f \colon \prod_{x \colon X} A(x)$. | An [[element]] in the [[internal hom|internal]] [[object]] of [[sections]] $* \stackrel{f}{\to} [X,A]_X$  | A [[point]] in the smooth relative [[mapping space]] of smooth [[sections]].  | _[Natural deduction rules for dependent product types](#NaturalDeductionForDependentProduct)_ |   
| There is the collection of assignments of an $a(x)$ to each $x$. | $\vdash\; \left( \prod_{x \colon X} A\left(x\right) \right) \colon Type$ | [[internal hom|internal]] space of [[sections]] $[X,A]_X \in \mathbf{H}$ | A smooth relative [[mapping space]] of smooth [[sections]]. |  |
| In particular, there is the collection of such assignments when $A$ does not depend on $x$, the collection of _functions_ from $X$ to $A$. |  $\vdash \; \left(X \to A\right) \coloneqq \left(\prod_{x \colon X} A\right) \colon Type$ | The [[internal hom]] [[object]] $[X,A] \in \mathbf{H}$.  | A smooth [[mapping space]]. |  _[Smooth mapping spaces and smooth moduli spaces](#SmoothMappingSpaces)_ |
| There is a proof $p$ that it is true that there is $x$ of type $X$. | $ \vdash \;  p \colon [X] $ | An [[element]]  $* \stackrel{p}{\to}\tau_{-1}(X)$ of the [[truncated object of an (infinity,1)-topos|(-1)-truncation]] of the object $X$. | A point in the [[smooth space]] of [[equivalence classes]] of points in $X$. | _[Subobjects](#Subobjects)_ |
| There is a proof $p$ that it is true that there is an $a(x)$ for some $x$. | $\vdash\; p \colon \left(\exists_{x \colon X} A\left(x\right) \right) \coloneqq \left[ \sum_{x \colon X} A\left(x\right)\right]$ | | |  |


***


category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects ??? ????]]
[[!redirects Featured math : Quora]]
