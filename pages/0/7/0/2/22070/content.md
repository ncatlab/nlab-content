

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

__Homotopy equalizers__ are a special case of [[homotopy limits]],
when the indexing [[diagram]] is the [[walking parallel pair]],
which consists of a pair of [[parallel morphisms]],
i.e., two [[objects]], 0 and 1, and exactly two nonidentity [[morphisms]], both of the form $0\to 1$.

Homotopy equalizers can be defined in any [[relative category]],
just like [[homotopy colimits]],
but practical computations are typically carried out
in presence of additional structures such as [[model structures]].

In the absence of nontrivial [[homotopies]] (in a bare [[1-category]]), homotopy equalizers reduce to ordinary [[equalizers]].



## Properties

### Relation to homotopy pullbacks
 {#RelationToHomotopyPullbacks}

In any [[model category]], the homotopy equalizer
of a pair of arrows $f,g\colon A\to B$ can be computed as follows.

First, if $B$ is not [[fibrant]] and the [[model category]] is not [[right proper]], construct a [[fibrant replacement]] $r\colon B\to R B$
and replace $(f,g)$ with $(r f,r g)$.

Assume now that $B$ is [[fibrant]] or the [[model category]] is [[right proper]].

In the special case when the map
$$
  (f,g)
  \;\colon\; 
  A \longrightarrow B\times B
$$
happens to be a [[fibration]], we can compute the ordinary [[equalizer]] of $f$ and $g$, which is a homotopy equalizer.

In the general case,
factor the [[diagonal map]] $\Delta \;\colon\; B\to B\times B$
as a [[weak equivalence]] $B \to P B$ followed by a [[fibration]] $P B \longrightarrow B\times B$, then compute the (ordinary) [[pullback]] of
$$
  A \longrightarrow B\times B \longleftarrow P B
  \,.
$$
This is the homotopy equalizer of $f$ and $g$.

See also 

* [this Prop.](homotopy+pullback#HomotopyPullbackByFactorizationLemma) at *[[homotopy pullback]]*  

and 

* [this Prop](https://ncatlab.org/nlab/show/Mayer-Vietoris+sequence#SequenceFromDiagonal) at *[[Mayer-Vietoris sequence]]*.

### Relation to homotopy fibers

For [[pointed model categories]], the homotopy equalizer
of $f\colon A\to B$ and the [[zero morphism]] $0\colon A\to B$ is known as the __[[homotopy fiber]]__ of $f$.
See there for more information.


## Examples

In [[simplicial sets]] with [[simplicial weak equivalences]],
the homotopy equalizer of $f,g\colon A\to B$
can be computed as the pullback
$$A\times_{B\times B}B^{\Delta^1}$$
if $B$ is a [[Kan complex]].
(Otherwise, compose with a [[fibrant replacement]]
like $B\to Ex^\infty B$ first.)
The same formula works for [[topological spaces]] with [[weak homotopy equivalences]], using $\Delta=[0,1]$.

For [[chain complexes]] with [[quasi-isomorphisms]],
the homotopy equalizer can be computed
(expanding the analogous formula with $P B =B^{\mathrm{N} \mathbf{Z} [\Delta^1]}$)
as
$$A\oplus B[-1],$$
where
$$d(a\oplus b)=d a\oplus d b+f(a)-g(a).$$

## Related notions

* [[homotopy coequalizer]]

* [[product]]

* [[homotopy limit]]

* [[homotopy pullback]]

* [[homotopy product]]

* [[homotopy totalization]]

[[!redirects homotopy equalizers]]