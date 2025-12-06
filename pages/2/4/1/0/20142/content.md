
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


\tableofcontents

## Idea

A cartesian closed enriched category is an [[enriched category]] that is simultaneously [[cartesian monoidal category|cartesian monoidal]] and [[closed monoidal category|monoidal closed]].

## Definitions

The generalization of [[closed monoidal category]] to the enriched setting is standard.

There are multiple inequivalent definitions we could make for what it means for an enriched category to be cartesian monoidal.

\begin{definition}
In [Street 14](#Street14), a cartesian monoidal enriched category is an [[enriched monoidal category]] $(C,\otimes, I)$ such that the functors $I : I \to C$ and $(-\otimes -) : C\otimes C \to C$ have [[enriched adjunction|$V$-enriched]] [[left adjoint|left adjoints]].

A cartesian closed enriched category is a cartesian monoidal enriched category in which all the $V$-functors $(X\otimes -) \colon C \to C$ and $(-\otimes X) \colon C \to C$ have [[enriched adjunction|$V$-enriched]] [[right adjoint|right adjoints]].
\end{definition}

\begin{definition}
If we want the monoidal product to literally be the [[products|categorical product]], we need, in general, $V$ to be [[semicartesian monoidal category|semicartesian]].

Let $V$ be a [[semicartesian monoidal category]] with [[products]] and $C$ a $V$-[[enriched category]] with [[products]], in the enriched sense that we have a [[enriched natural transformation|$V$-natural]] [[natural isomorphism|isomorphisms]] of [[hom-objects]] in $V$:

$$ 
  C(Z, X\times Y) 
  \;\cong\; 
  C(Z,X) \times C(Z,Y)
  \,. 
$$

We say that $C$ is **$V$-cartesian-closed** if each [[enriched functor|$V$-functor]] $(X\times -) \colon C \to C$ has a [[enriched adjunction|$V$-enriched]] [[right adjoint]].
\end{definition}


## Relation to ordinary cartesian closedness

For the following, we use the second definition given above.

If $C$ is $V$-cartesian-closed, then its [[underlying ordinary category]] $C_0$ is [[cartesian closed category|cartesian closed]] in the usual sense, since $V$-enriched right adjoints have underlying ordinary right adjoints.

The converse is true in some cases, such as the following:

* When $V=Set$, trivially.

* More generally, whenever the underlying-set functor $V(I,-) : V\to Set$ is [[conservative functor|conservative]], since the morphism of hom-objects $C(X,Y^Z) \to C(X\times Y,Z)$ induced by the evaluation morphism $Y^Z\times Y \to Z$ has invertible image in $Set$, hence is itself invertible if $V(I,-)$ is conservative.

* When $V$ is cartesian monoidal and $C=V$: a cartesian closed category is automatically enriched-cartesian-closed over itself.  In other words, the defining isomorphisms $V_0(X\times Y,Z) \cong V_0(X, Z^Y)$ induce, by the [[Yoneda lemma]], isomorphisms of [[exponential objects]] $Z^{X\times Y} \cong (Z^Y)^X$.

However, the converse is false in general.  [[counterexample|Counterexamples]] can be found in [this mathoverflow discussion](#MO).

## Related concepts

* [[cartesian closed category]]

* [[locally cartesian closed enriched category]]

* [[monoidal enriched category]]

* [[cartesian closed model category]]

## References

* {#MO} [Enriched cartesian closed categories on MO](https://mathoverflow.net/q/322085)

* {#MO2} [Simplicial cartesian closed categories on MO](https://mathoverflow.net/q/322917)

* {#Street14} [[Ross Street]], _Kan extensions and cartesian monoidal categories_ [arXiv:1409.6405](https://arxiv.org/abs/1409.6405)


[[!redirects cartesian closed enriched category]]
[[!redirects cartesian closed enriched categories]]
[[!redirects enriched cartesian closed category]]
[[!redirects enriched cartesian closed categories]]
[[!redirects simplicially cartesian closed category]]
[[!redirects simplicially cartesian closed categories]]
