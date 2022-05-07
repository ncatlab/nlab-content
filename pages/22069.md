## Idea

__Homotopy coequalizers__ are a special case of [[homotopy colimits]],
when the indexing diagram is the [[walking coequalizer category]],
which has two objects, 0 and 1, and exactly two nonidentity morphisms,
both of the form $0\to 1$.

Homotopy coequalizers can be defined in any [[relative category]],
just like [[homotopy colimits]],
but practical computations are typically carried out
in presence of additional structures such as [[model structures]].

## Computation

In any [[model category]], the homotopy coequalizer
of a pair of arrows $f,g\colon A\to B$ can be computed as follows.
First, if $A$ is not [[cofibrant]] and the [[model category]] is not [[left proper]], construct a [[cofibrant replacement]] $q\colon QA\to A$
and replace $(f,g)$ with $(f q,g q)$.

Assume now that $A$ is [[cofibrant]] or the [[model category]] is [[left proper]].

In the special case when the map
$$[f,g]\colon A\sqcup A\to B$$
happens to be a [[cofibration]],
we can compute the ordinary [[coequalizer]] of $f$ and $g$,
which is a homotopy coequalizer.

In the general case,
factor the [[codiagonal map]] $\nabla\colon A\sqcup A\to A$
as a [[cofibration]] $A\sqcup A\to C A$ followed by a [[weak equivalence]] $CA\to A$,
then compute the (ordinary) [[pushout]] of
$$CA\leftarrow A\sqcup A \to B.$$
This is the homotopy coequalizer of $f$ and $g$.

## Examples

In [[simplicial sets]] with [[simplicial weak equivalences]],
the homotopy coequalizer of $f,g\colon A\to B$
can be computed as the pushout
$$\Delta^1\times A\sqcup_{A\sqcup A} B.$$
The same formula works for [[topological spaces]] with [[weak homotopy equivalences]], using $\Delta=[0,1]$.

For [[chain complexes]] with [[quasi-isomorphisms]],
the homotopy coequalizer can be computed
(expanding the analogous formula with $C A =\mathrm{N} \mathbf{Z} [\Delta^1]\otimes A$)
as
$$B\oplus A[1],$$
where
$$d(b\oplus a)=d b+f(a)-g(a)\oplus d a.$$

## Related notions

* [[coproduct]]

* [[homotopy colimit]]

* [[homotopy pushout]]

* [[homotopy coproduct]]

* [[homotopy realization]]

* [[homotopy equalizer]]

[[!redirects homotopy coequalizers]]