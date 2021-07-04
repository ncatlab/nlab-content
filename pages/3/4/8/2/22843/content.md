
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

Write

* $Groups(sSet)$ for the [[category]] of [[simplicial groups]]

* $Groups(sSet)_{proj}$ for the [[model structure on simplicial groups]] whose [[weak equivalences]] and [[fibrations]] are those of the underlying morphisms in the [[classical model structure on simplicial sets]] (hence the underlying [[simplicial weak equivalences]] and [[Kan fibrations]], respectively);

* $sSet_{\geq 1}$ for the [[category]] of [[reduced simplicial sets]];

* $(sSet_{\geq 1})$ for the [[model structure on reduced simplicial sets]] whose [[weak equivalences]] and [[cofibrations]] are those of the underlying morphisms in the [[classical model structure on simplicial sets]].

\begin{proposition}\label{QuillenEquivalenceBetweenSimplicialGroupsAndReducedSimplicialSets}
**(Quillen equivalence between simplicial groups and reduced simplicial sets)** \linebreak

The 

* [[simplicial classifying space]]-construction $\overline{W}(-)$ is the [[right adjoint]] 

* [[simplicial loop space]]-construction $\Omega(-)$ is the [[left adjoint]]

in a [[Quillen equivalence]] between the projective [[model structure on simplicial groups]] and the injective [[model structure on reduced simplicial sets]]. 

$$
  Groups(sSet)_{proj}
  \underoverset
    {\underset{\overline{W}}{\longrightarrow}}
    {\overset{ \Omega }{\longleftarrow}}
    {\;\;\;\;\; \simeq_{\mathrlap{Qu}} \;\;\;\;\;}
  (sSet_{\geq 0})_{inj}
  \,.
$$

\end{proposition}

(e.g. [Goerss & Jardine 09, V Prop. 6.3](#GoerssJardine09))

## Related concepts

* [[looping and delooping]]

* [[May recognition theorem]]

## References

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.4 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

[[!redirects Quillen equivalence between reduced simplicial sets and simplicial groups]]


