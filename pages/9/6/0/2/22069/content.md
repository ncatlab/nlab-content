

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In generalization of the notion of *[[equalizers]]* from [[category theory]] to [[homotopy theory]],
*homotopy coequalizers* are the special case of [[homotopy colimits]],
where the indexing [[diagram]] is the [[walking parallel pair]], consisting of a [[pair]] of [[parallel morphisms]], i.e., two [[objects]], 0 and 1, and exactly two nonidentity [[morphisms]], both of the form $0\to 1$.

Homotopy coequalizers can be defined in any [[relative category]],
just like [[homotopy colimits]],
but practical computations are typically carried out
in presence of additional structures such as [[model structures]].

## Computation
 {#Computation}

In any [[model category]], the homotopy coequalizer
of a pair of arrows $f,g\colon A\to B$ can be computed as a [[homotopy pushout]] as follows (compare the ordinary expression of [[coequalizer]] as [[pushouts]], [here](coequalizer#CoequalizedAsAPushout)).


First, if $A$ is not [[cofibrant]] and the [[model category]] is not [[left proper]], construct a [[cofibrant replacement]] $q\colon QA\to A$
and replace $(f,g)$ with $(f q,g q)$.

Assume now that $A$ is [[cofibrant]] or the [[model category]] is [[left proper]].

In the special case when the map

$$
  (f,g)
  \,\colon\, A\sqcup A \longrightarrow B
$$
happens to be a [[cofibration]],
one can compute the ordinary [[coequalizer]] of $f$ and $g$,
which is a homotopy coequalizer.

In the general case,
factor the [[codiagonal map]] $\nabla \,\colon\, A\sqcup A \longrightarrow A$
as a [[cofibration]] $A\sqcup A \longrightarrow C A$ followed by a [[weak equivalence]] $CA \longrightarrow A$,
then compute the (ordinary) [[pushout]] of
$$
  CA 
    \longleftarrow 
  A\sqcup A 
   \overset{(f,g)}{\longrightarrow} 
  B
  \,.
$$
This is the homotopy coequalizer of $f$ and $g$.


## Examples

In [[simplicial sets]] with [[simplicial weak equivalences]],
the homotopy coequalizer of $f,g\colon A\to B$
can be computed as the pushout
$$
  (\Delta^1 \times A)
    \overset{A\sqcup A}{\amalg} 
  B
  \,.
$$
The analogous formula works for [[topological spaces]] with [[weak homotopy equivalences]], then using the [[closed interval]] $\Delta=[0,1]$ and also known as the *[[double mapping cylinder]]*-construction, see for instance [Dwyer, Farjoun & Ravenel (1999), p. 1856](#DwyerFarjounRavenel99) (cf. *[[mapping cylinder]]*).

For [[chain complexes]] with [[quasi-isomorphisms]],
the homotopy coequalizer can be computed
(expanding the analogous formula with $C A =\mathrm{N} \mathbf{Z} [\Delta^1]\otimes A$)
as
$$
  B \oplus A[1]
  \,,
$$
where

$$
  d(b\oplus a)
   \;=\;
  d b+f(a)-g(a) \oplus d a
  \,.
$$

## Related notions

* [[mapping cylinder]]

* [[coproduct]]

* [[homotopy colimit]]

* [[homotopy pushout]]

* [[homotopy coproduct]]

* [[homotopy realization]]

* [[homotopy equalizer]]


## References

* {#DwyerFarjounRavenel99} [[William G. Dwyer]], [[Emmanuel Dror Farjoun]], [[Douglas C. Ravenel]], pp. 1856 in: *Bousfield Localizations of Classifying Spaces of Nilpotent Groups*, Proceedings of the American Mathematical Society **127** 6 (1999) &lbrack;[jstor:119499](https://www.jstor.org/stable/119499)&rbrack;



[[!redirects homotopy coequalizers]]


[[!redirects double mapping cylinder]]
[[!redirects double mapping cylinders]]
