
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[Kan fibration]] that at the same time is a [[weak homotopy equivalence]] is called an **acyclic Kan fibration**. (Also: a _trivial Kan fibration_.)

## Properties

Acyclic Kan fibrations are the [[acyclic fibrations]] in the [[classical model structure on simplicial sets]] $sSet_{Qu}$, hence those morphisms which have the [[right lifting property]] against [[monomorphisms]] (degreewise [[injections]]) of [[simplicial sets]].

In particular, this implies that:
\begin{proposition}\label{AcyclicKanFibrationsAreSurjective}
Acyclic Kan fibrations are  (degreewise) [[surjective]], in that they have the [[right lifting property]] against any [[empty bundle]] $\varnothing \xhookrightarrow{\;} S$.
\end{proposition}
\begin{remark}
Prop. \ref{AcyclicKanFibrationsAreSurjective} is in contrast to plain [[Kan fibrations]], see [this remark](horn#ZeroSimplexHasNoHorns) about the empty horn, and see the discussion on surjective Kan fibrations [there](Kan+fibration#SurjectiveKanFibrations).
\end{remark}

In fact:
\begin{prop}
Acyclic Kan fibrations are precisely the morphisms of [[simplicial sets]] that have the [[right lifting property]] against all [[boundary of a simplex|simplex boundary inclusions]].
\end{prop}
See [this Prop.](classical+model+structure+on+simplicial+sets#AcyclicKanFibrationsAsRLPAgainstBoundaryInclusions) at *[[classical model structure on simplicial sets]]*.
This is part of the statement that $sSet_{Qu}$  is a [[cofibrantly generated model category|cofibrantly generated]] (see [this Prop.](classical+model+structure+on+simplicial+sets#AsACofibrantlyGeneratedModelCategory)). 


## Related entries

* [[simplicial homotopy theory]]

[[!redirects acyclic Kan fibrations]]

[[!redirects trivial Kan fibration]]
[[!redirects trivial Kan fibrations]]
