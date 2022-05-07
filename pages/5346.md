

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _model structure on simplicial groups_ is a presentation of the 
[[(∞,1)-category]] of [[∞-groups]] in [[∞Grpd]] $\simeq$ [[Top]]. See [[group object in an (∞,1)-category]].

## Definition

+-- {: .num_prop #ModelStructureOnSimplicialGroups} 
###### Proposition

There is a projective [[model category]] structure on the [[category]] $sGrp$ of [[simplicial groups]] where a morphism is

* is a [[weak equivalence]] if the underlying morphism is a weak equivalence in the standard [[model structure on simplicial sets]];

* is a [[fibration]] if the underlying morphism is a [[Kan fibration]] of simplicial sets;

* is a [[cofibration]] if it has the [[left lifting property]] with respect to all trivial fibrations.

=--

([Quillen 67, II 3.7](#Quillen67), see also [Goerss-Jardine 99, V](#GoerssJardine99))

## Properties

\begin{proposition}\label{EveryObjectIsFibrant}
  Every object in the projective model structure (Prop. \ref{ModelStructureOnSimplicialGroups}) is [[fibrant object|fibrant]].
\end{proposition}
\begin{proof}
  This statement amounts to saying that the underlying simplicial set of any simplicial group is a [[Kan complex]]. That this is the case is Moore's theorem ([here](simplicial+group#EverySimplicialGroupIsAKanComplex)).
\end{proof}

+-- {: .num_prop #QuillenEquivalenceWithReducedSimplicialSets} 
###### Proposition
**([[Quillen equivalence between simplicial groups and reduced simplicial sets]])**

Forming [[simplicial loop space]] objects and [[simplicial classifying spaces]] gives a [[Quillen equivalence]]

$$
  \big(
    \Omega \dashv \overline{W}
  \big) 
  \;\colon\; 
  sGrp 
   \stackrel{\overset{}{\longleftarrow}}{\longrightarrow}
  sSet_0
$$

with the [[model structure on reduced simplicial sets]].

=--

([Goerss-Jardine 99, Chapter V, Prop. 6.3](#GoerssJardine99))

## Related concepts

* [[Borel model structure]] (presenting [[infinity-actions]] of simplicial groups)

## References

The model structure on simplicial groups is due to

* {#Quillen67} [[Daniel Quillen]], p. II 3.7 of: _Axiomatic homotopy theory_ in: _[[Homotopical Algebra]]_, Lecture Notes in Mathematics 43, Springer 1967([doi:10.1007/BFb0097438](https://doi.org/10.1007/BFb0097438))

Further discussion is in

* {#GoerssJardine99} [[Paul Goerss]], [[J. F. Jardine]], chapter V of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

