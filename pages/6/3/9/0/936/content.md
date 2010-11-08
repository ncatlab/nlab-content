
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

#Contents#
* automatic table of contents
{:toc}

## Definition 

A **homotopy equivalence** between [[topological space]]s $X$ and $Y$ is a continuous map $f:X\to Y$  such that there exists a continuous map $g:Y\to X$ and [[homotopy|homotopies]] $g \circ f \sim 1_X$ and $f \circ g \sim 1_Y$. (Note the similarity with the strict notion of [[equivalence of categories]].)

The [[homotopy category]] of [[Top]] with respect to homotopy equivalences is [[Ho(Top)]]${}_{he}$.

More generally, in any [[(∞,1)-category]] $C$ other than [[Top]], a homotopy equivalence in $C$ is just an equivalence in $C$.

If there exists a homotopy equivalence between $X$ and $Y$ we say that $X$ and $Y$ are **homotopy equivalent** or that they have the same **[[homotopy type]]**.  Being homotopy equivalent is evidently an [[equivalence relation]].

For many purposes, one wants instead [[weak homotopy equivalence]]s.  Often when speaking of a homotopy equivalence or a homotopy type, one actually means the weak version.  (This is especially likely on this wiki, due to the relationship to $\infty$-[[infinity-groupoid]]s suggested by the [[homotopy hypothesis]].)

## Properties 

Any homotopy equivalence is also a [[weak homotopy equivalence]].  Conversely, any weak homotopy equivalence between [[m-cofibrant space]]s (spaces that are homotopy equivalent to [[CW complex]]es) is a homotopy equivalence. This is the [[Whitehead theorem]].

The homotopy equivalences are the [[weak equivalence]]s in the Str&#248;m [[model structure on topological spaces]].  The [[homotopy category]] resulting from inverting all homotopy equivalences in [[Top]] is the same as that resulting from identifying homotopic maps.

##  Strong homotopy equivalences

Sometimes an apparently stronger form of homotopy equivalence is needed.  These seem to have been first noticed by [[Richard Lashof]] in 1970 in work on triangulation and smoothing. The point is one of the interaction between the two homotopies, which are not made explicit in the definition above. Let us set this up slightly differently:

In a homotopy equivalence there are the two maps $f: X\to Y$ and $g: Y\to X$, then two [[homotopy|homotopies]]

$$H : X\times I \to X,   H:g \circ f \sim 1_X$$

and 

$$K: Y\times I \to Y,   K : f \circ g \sim 1_Y.$$
 
The [[whiskering]] actions of maps on homotopies (and more generally in any [[(∞,1)-category]] or category with a [[cylinder functor]]) gives
two homotopies $f\circ g \circ f \sim f$, namely $f_*H = f\circ H : X\times I \to Y$ and $f^*K = K\circ (f\times I)$.  Similarly, of course, there are two homotopies $g\circ f \circ g \sim g$, namely $g_*K$ and $g^*H$.  In the usual definition of homotopy equivalence, there is no coherence required between these. That is handled precisely by the notion of **stong homotopy equivalence**. More precisely Lashof defined

+-- {: .un_defn}
###### Definition
A **strong homotopy equivalence** between spaces $X$ and $Y$ is a quadruple $(f,g,H,K)$,
as above, such that $f_*H \sim f^*K$ and $g_*K\sim g^*H$.
=--

Thus this imposes a minimal coherence condition on the data making up the homotopy equivalence.  The definition clearly can be generalised to any reasonable setting with a notion of homotopy.

For example, in a [[2-category]] where a homotopy is a [[natural isomorphism]], and a homotopy between homotopies is just an [[equality]], a homotopy equivalence is simply an [[equivalence]], while a strong homotopy equivalence is the same as an [[adjoint equivalence]].

The question naturally arises as to whether all homotopy equivalences are strong. [[Rainer Vogt]](1972) proved

+-- {: .un_lemma}
###### Vogt's Lemma
If $f: X\to Y$ be a morphism that is a homotopy equivalence in $Top$, let $g: Y\to X$ be a homotopy inverse and $H:g \circ f \sim 1_X$ a homotopy.  Then there is a homotopy $K: f \circ g \sim 1_Y$ such that $(f,g,H,K)$ is a strong homotopy equivalence.
=--

Various versions of this are known in other settings, e.g. $SSet$-enriched categories.  In a 2-category the corresponding fact is that any equivalence can be improved to an adjoint equivalence, by changing at most one of the 2-cell isomorphisms involved.

Note, though, that the coherence supplied by Vogt's lemma is not required to continue to higher levels. There is no condition of compatibilty between the two 'homotopies between the homotopies'.  In some situations, at least, some higher compatibility is known to be derivable; for instance, any biequivalence in a [[3-category]] can be improved to an adjoint biequivalence.

+--{.query}
[[Tim]]: I do not know if there is a neat formulation of the full homotopy coherent version of this, nor exactly in what settings the analogous abstract versions of Vogt's lemma go across

[[Mike Shulman]]: I think there's a "full coherentification" version for quasicategories in HTT somewhere.
=--


Vogt's Lemma plays a key role in the proof of Vogt's theorem (cf. [[homotopy coherent diagram]]s).

## Related notions

* [[weak homotopy equivalence]]

* [[homotopy equivalence of toposes]].

[[!redirects homotopy equivalences]]
[[!redirects homotopy equivalent]]
