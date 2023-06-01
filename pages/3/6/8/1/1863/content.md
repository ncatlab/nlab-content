
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[functor]] is **cocontinuous** if it [[preserved colimit|preserves]] [[small category|small]] [[colimit|colimits]].  

Typically one only considers cocontinuous functors whose [[domain]] and [[codomain]] are [[cocomplete categories]] (have all small colimits).

Note that $F\colon C \to D$ is cocontinuous if and only if the functor $F^{op}: C^{op} \to D^{op}$ between [[opposite categories]] is a [[continuous functor]].

## Examples

\begin{example}
Every [[left adjoint functor]] is contontinuous, since [[left adjoints preserve colimits]]. 
\end{example}

Not every functor is cocontinuous:
\begin{example}
A [[counterexample]] of a dis-cocontinuous functor is the [[forgetful functor]] $F \colon Set_* \rightarrow Set$ from the category of [[pointed sets]] to the category [[Set]] of [[sets]].
\end{example}


## Related concepts

* [[continuous functor]]

* [[cocomplete category]]

* [[adjoint functor theorem]]

[[!include properties of functors -- contents]]


## References

See the references at *[[continuous functor]]*.


[[!redirects cocontinuous functors]]
