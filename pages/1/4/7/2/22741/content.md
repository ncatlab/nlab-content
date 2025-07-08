
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


\tableofcontents

## Definition

\begin{definition}\label{PointedEndofunctor}
An [[endofunctor]] $S \colon \mathcal{A}\to \mathcal{A}$ is called [[pointed endofunctor|pointed]] if it is equipped with a [[natural transformation]] $\sigma \colon Id_\mathcal{A} \to S$ from the [[identity functor]]. 
\end{definition}

(Beware that is *not* quite the notion of a [[pointed object]] in the endo-[[functor category]], since the [[identity functor]] is not in general a [[terminal object]] there. See the remark [there](pointed+endofunctor#MeaningOfPointedness).)

\begin{definition}
A pointed endofunctor $(S, \sigma)$ (Def. \ref{PointedEndofunctor}) is called **well-pointed** if $S\sigma = \sigma S$ as natural transformations $S \longrightarrow S \circ S$.
\end{definition}

The dual notion is known as a **well-copointed** endofunctor.


## Properties

Well-pointed endofunctors have a particularly well-behaved free algebra sequence; see *[[transfinite construction of free algebras]]*.

## Related concepts

* A [[monad]] is [[idempotent monad|idempotent]] iff its underlying [[pointed endofunctor]] is well-pointed.

## References

Well-pointed endofunctors are studied as "symmetric unads" in:

* K. A. Hardie, _Instances and ramifications of the semi-adjoint situation I. Prestable reflection and symmetric unads_, Quaestiones Mathematicae 2.1-3 (1977): 147-158.

The terminology is due to:

* {#Kelly} [[Max Kelly]], _A unified treatment of transfinite constructions for free algebras, free monoids, colimits, associated sheaves, and so on._  Bull. Austral. Math. Soc. 22 (1980), 1--83. doi:[10.1017/S0004972700006353](http://dx.doi.org/10.1017/S0004972700006353)
 

[[!redirects well-pointed endofunctors]]
