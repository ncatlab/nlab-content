
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Introduction ##

### Overview ###

<div style="float:right;margin:0 20px 10px 20px;"><img width = "450" src="https://www.cs.bham.ac.uk/~vicaryjo/images/face_of_pentagon.jpg" alt="Screenshot of homotopy.io" />
</div>

This page describes _homotopy.io_, a web-based [[proof assistant]] for finitely-presented [[globular set|globular]] [[n-category|_n_-categories]], for arbitrary $n$. It is available at the following address:

* [homotopy.io](https://homotopy.io)

* [github.com/homotopy-io](https://github.com/homotopy-io)

It is based on the theory of [[associative n-categories|associative _n_-categories (ANCs)]], which provides a strictly associative and unital model of [[composition]]. This reduces proof bureaucracy, with all the remaining weak structure in [[homotopies]] of composites, which have a direct geometrical interpretation. The proof assistant allows the user to define [[generators and relations|generators]] for a [[higher category]], [[composition|compose]] them, apply [[homotopies]], and visualize the resulting composites as [[string diagrams]] in 2 dimensions or [[surface diagrams]] in 3 dimensions. Interaction with the proof assistant is entirely by direct manipulation using the mouse.

It can be considered a successor to the existing proof assistant [[Globular]], which allows the construction of formal proofs in a strictly associative and unital model of [[4-categories]].

Homotopy construction in _homotopy.io_ is enabled by two basic mechanisms: _contraction_, which makes the geometry locally more singular; and _expansion_, which makes the geometry locally more generic. These local moves 'drag' neighbouring parts of the composite, and allow the construction of nontrivial [[homotopies]]. It is an open question whether these contraction and expansion moves are capable of generating all possible homotopies in every dimension.

The image at the top-right shows a 3d surface diagram of one side of the [[pentagon equation]] ([_live workspace_](https://homotopy.io/?id=kzmugNEGMPBF8BbB5FAm)).

### Contributors ###

The proof assistant is based on the theory of [[associative n-categories|associative _n_-categories]], which has been worked on by [Christoph Dorn](https://www.cs.ox.ac.uk/people/christoph.dorn/), [Christopher Douglas](https://www.maths.ox.ac.uk/people/christopher.douglas), [David Reutter](https://www.cs.ox.ac.uk/people/david.reutter/) and [Jamie Vicary](https://www.cs.bham.ac.uk/~vicaryjo/). The proof assistant has been implemented by [Lukas Heidemann](https://github.com/zrho), [Nick Hu](https://github.com/NickHu) and [Jamie Vicary](https://www.cs.bham.ac.uk/~vicaryjo/).

## Overview of functionality
 {#OverviewOfFunctionality}

Using _homotopy.io_ involves building a signature listing the types available to work with, composing them to form diagrams, and then deforming these diagrams with homotopies. The fundamental idea is that an $n$-diagram corresponds to an $n$-morphism in the free associative $n$-category over the signature.

**Signatures.** In dimension 0, generating cells can be constructed by clicking the "+" symbol next to the heading "0-cells". In dimension $n+1$, a cell is defined by two pieces of data: its source $n$-diagram, and its target $n$-diagram. We add such a cell by building an $n$-diagram $S$, clicking 'Source' to choose it as the source of the new generator, then building a $n$-diagram $T$, and clicking 'Target' to choose it as the target of the new generator. The new cell will then appear in the signature. A pair of $n$-diagrams $S,T$ can serve as the source and target of a new generator just when they satisfy the globularity condition, saying that their sources are the same, and their targets are the same.

**Diagrams.** An $n$-diagram is a composite of $k$-cells from the signature, for $k \leq n$. To build a diagram, we first click on the thumbnail of a cell in the signature, which will display it in the central window. We can _compose_ it with other cells by clicking near the boundary. These compositions are always [[whiskering|whiskerings]], with a $k$-cell generator attached to an $n$-diagram along a common $\text{min}(k,n)$-dimensional boundary. Non-whiskered composites can be obtained by first building whiskered composites, and then rewriting the interior of the diagram using homotopies. We can _rewrite_ parts of an $n$-diagram by clicking in the diagram interior, which will apply an $n+1$-cell, or clicking and dragging, which will apply a homotopy.

**Homotopies.** Once a diagram has been constructed, we can modify it by applying a _homotopy_, which we trigger by clicking and dragging on the diagram. If this is performed on the boundary of the diagram, it will attach the homotopy to the boundary; if this is performed in the interior of the diagram, it will rewrite it.

**Renderer (experimental).** Diagrams can be rendered in both 2d and 3d. At the moment, only the 2d renderer is interactive, allowing diagrams to be manipulated directly using the mouse; the 3d renderer is for display only, and is currently quite buggy, only working reliably for small diagrams with a connected geometry. It is hoped that _homotopy.io_ will soon allow rendering and smooth animation of arbitrary 3d composites.

**Projection.** Diagrams can be high-dimensional, and hence hard to display on a computer screen. _Projection_ causes lower dimensions of the diagram to be ignored; for example, given a 5-dimensional diagram with projection set to 3, you will see a single $(5-3=2)$-dimensional diagram, in which the vertices represent 5-cells, the wires represent 4-cells, and the regions represent 3-cells. Note that projection loses information in general.

**Slice.** For an $n$-diagram with $n \gt 2$, projection will always lose some information about the diagram. _Slicing_ allows an $(n+1)$-dimensional diagram to be viewed as a movie of $n$-dimensional diagrams, in a way which preserves all information about the diagram. For example, for a 9-dimensional diagram with projection set to 3, there are still 6 remaining dimensions to display. With the renderer set to 2d, this leaves 4 dimensions to be handled with slice controls, which allows us to investigate the 6d displayed geometry as a movie of movies of movies of movies of 2d diagrams.

**Undo and redo.** Use the browser back and forward buttons to undo and redo your interactions with the proof assistant.

**Server.** The proof assistant has a backend that lets you log in and save proofs to the server. You can also make proofs shareable, and obtain a short URL suitable for sharing with others, or embedding in a research paper. In the future you will also be able to publish proofs, obtaining a permanent date-stamped URL.

## Homotopies

A composite diagram can be deformed by clicking and dragging in its interior. If the indicated deformation would be geometrically invalid, an error message is displayed in the lower-right corner, and the diagram does not change. Otherwise, a new diagram is displayed, which is homotopic to the original diagram.

Conjecturally, homotopies can be used to construct arbitrary progressive deformations of the $n$-diagram as a subcomplex of $\mathbb{R}^n$. Informally, homotopies can move parts of the diagram around, but they can't change the local neighbourhoods of the generating cells inhabiting the diagram.

Of course, the proof assistant manipulates finite combinatorial structures, and we use the word 'homotopic' with reference to their presumed geometrical realization. We do not make this precise here, nor has it yet been made precise in the literature; for this reason, our use of the term 'homotopy' is not yet well connected to the standard notion.

Every homotopy is either a _contraction_, which make the geometry locally more singular, or an _expansion_, which make it locally more generic. If we view our original diagram $D$ as a zigzag (see [Combinatorial foundation](#CombinatorialFoundation), a contraction is encoded as a zigzag map $D \to D'$, and an expansion as a zigzag map $D' \to D$, for some other diagram $D'$.

### Base cases ###

A homotopy is triggered by choosing an $n$-diagram for $n \geq 2$, choosing some vertex that it contains, and dragging that vertex _vertically_; that is, either up or down.

If the chosen vertex is in _generic position_, meaning that it is the unique vertex at its height, a contraction will be triggered; otherwise, an expansion will be triggered. In the base case, a contraction decreases the height of a diagram by 1, and an expansion increases it by 1. Expansions always succeed, but contractions will only succeed if the diagram is actually locally contractible, in the sense of homotopy theory. Mathematically, contractions are performed by taking the colimit of part of the zigzag diagram (see the [Combinatorial Foundation](#CombinatorialFoundation) section.)

To illustrate this, we suppose we have the following diagram, where for convenience we label the vertices with numbers ([<i>live workspace</i>](https://homotopy.io/?id=QMw1sG1p4yCpsgL3Xh7K)):

<img width="250" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/contraction-expansion-labelled.png"/>

Vertices 1 and 4 are in generic position, so dragging them will trigger contractions, while dragging vertices 2 and 3, which are in singular position, would trigger expansions. We illustrate the resulting diagrams as follows:

<style> table>tr>td { border:none!important } </style>
<table style="border-style:hidden !important; padding:0px!important">
<tr>
<td>
<img width="200" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/2-up.png"/>
</td>
<td>
<img width="200" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/2-down.png"/>
</td>
<td>
<img width="200" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/4-down.png"/>
</td>
<td>
<img width="200" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/1-up.png"/>
</td>
</tr>
<tr><td><i>Expansion</i></td><td><i>Expansion</i></td><td><i>Contraction</i></td><td><i>Contraction</i></td></tr>
<tr>
<td><i>2 up or 3 down</i></td>
<td><i>2 down or 3 up</i></td>
<td><i>1 down</i></td>
<td><i>4 up</i></td>
</tr>
</table>

Dragging vertex 1 up, or vertex 4 down, has no effect, as vertices cannot be dragged off the top or bottom edge of a diagram.

The contractions illustrated above are unique. However, in some cases, contractions are non-unique, as illustrated here ([<i>live workspace</i>](https://homotopy.io/?id=9DDbCH0V7xdKULkqroIz)):
<table style="border-style:hidden !important; padding:0px!important">
<tr>
<td>
<img height="88" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/unitcounit-2.png"/>
</td>
<td>→</td>
<td>
<img height="133" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/unitcounit-1.png"/>
</td>
<td>←</td>
<td>
<img height="88" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/unitcounit-3.png"/>
</td>
</tr>
</table>
Starting with the central diagram, we produce the leftmost diagram by dragging the upper vertex south-east or the lower vertex north-west, and produce the rightmost diagram by dragging the upper vertex south-west or the lower vertex north-east.


Contraction is not always possible. The following images illustrate non-contractible scenarios:

<table style="border-style:hidden !important; padding:5px!important">
<tr>
<td>
<img height="133" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/noncontractible-1.png"/>
</td>
<td>
<img height="133" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/noncontractible-2.png"/>
</td>
</tr>
<tr>
<td>
(<a href="https://homotopy.io/?id=HWcBiyNFuYg3dGrlOqZh"><i>live workspace</i></a>)
</td>
<td>
(<a href="https://homotopy.io/?id=2JlXs4ei0lGsUGeHWJtr"><i>live workspace</i></a>)
</td>
</table>

In both of these cases, attempting to perform the contraction will give an error message. In the first case, the contraction fails because there is no canonical ordering on the rear wires; this is analogous to the nonunique contraction case given above, but here, because of the projection, we cannot give extra data to break the symmetry. In the second case, the contraction is successful at the level of the untyped diagram, but it is rejected by the type checker, since it merges two distinct generating cells, changing their neighbourhoods in a way which is not allowed by the type system.


If there are no slice controls displayed, then the homotopy is being performed at codimension 0 (that is, at the top level), and the diagram will be rewritten according to the homotopy. If every slice control shows S or T, then we are viewing a boundary of the main diagram, and the homotopy we are building will be attached to that boundary. Otherwise, we are in the interior of the diagram, working in some positive codimension, and the homotopy must now be propagated to lower codimension, using the recursive scheme detailed in the next section.

### Recursive cases ###

When we apply a homotopy to an interior slice of the main diagram, it is propagated up to the top level. A homotopy can be either a contraction or an expansion, and we can be in a regular or singular subslice; this gives 4 cases, which we consider separately.

## Combinatorial foundation
 {#CombinatorialFoundation}

The combinatorial data stored by the proof assistant can be understood in terms of zigzags.

+-- {: .num_defn}
###### Definition
In a category $C$, a _zigzag_ is a finite diagram of the following sort:

<img height="120" style="margin-left:auto; margin-right:auto;" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/zigzag.png" alt="A zigzag" />

We write $Z_r = \{ r_0, \ldots, r_n \}$ for the set of _regular slices_, and $Z_s = \{ s_0, \ldots, s_{n-1} \}$ for the set of _singular slices_.
=--

+-- {: .num_defn}
###### Definition
Given zigzags $Z,Z'$ in a category $C$, a _zigzag map_ $f:Z \to Z'$ comprises a monotone function $f_\text{s} : Z_\text{s} \to Z'_\text{s}$, and for each $i \in Z_\text{s}$ a morphism $f_i : s_i \to s' _{f_\text{s}(i)}$, such that the diagram built as follows is commutative:

* Take the disjoint union of $Z$ and $Z'$ as diagrams in $C$.
* Add the arrows $f_i$ between singular objects.
* In between these arrows, add equalities between regular objects.

The idea is illustrated in the following picture:

<img height="200" style="margin-left:auto; margin-right:auto;" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/zigzagmap.png" alt="A zigzag" />
=--

+-- {: .num_defn}
###### Definition
Given a category $C$, its _zigzag category_ $Z_C$ has zigzags as objects, and zigzag maps as morphisms.
=--

+-- {: .num_defn}
###### Definition
An _untyped $n$-diagram_ is an object of the category obtained by starting with the terminal category $1$, and applying the zigzag category construction $n$ times.
=--

For a signature $\Sigma$, we write $|\Sigma|$ for its set of generating types, which is equipped with a dimension function $\text{dim}:|\Sigma| \to \mathbb{N}$. We write $\mathcal{P}_\Sigma$ for the poset with objects given by elements of $|\Sigma|$, and a nonidentity morphism $x \to y$ just when $\text{dim}(x) \lt \text{dim}(y)$.

+-- {: .num_defn}
###### Definition
A _$|\Sigma|$-typed $n$-diagram_ is an object of the category obtained by starting with the category $\mathcal{P}_\Sigma$, and applying the zigzag category construction $n$ times.
=--

## Type checking and normalization

Given a $|\Sigma|$-typed $n$-diagram $D$, we can then ask if it is _well-typed_ with respect to $\Sigma$. This involves identifying the neighbourhoods of every point, and checking that they agree with the standard type neighbourhoods defined in $\Sigma$. This procedure is explained in Christoph Dorn's PhD thesis referenced below.

## Related entries

* [[associative n-category]]

* [[Globular]]

[[!include proof assistants and formalization projects -- list]]

## References

Background on [[associative n-categories]]:

* [[Christoph Dorn]], _Associative $n$-categories_, talk at _[103rd Peripatetic Seminar on Sheaves and Logic](https://www.math.muni.cz/~loregianf/PSSL103/PSSL103.php)_ &lbrack;[pdf](https://www.math.muni.cz/~loregianf/PSSL103/slides/Dorn.pdf)&rbrack;

* [[Christoph Dorn]], _Associative $n$-categories_, PhD thesis &lbrack;[arXiv:1812.10586](https://arxiv.org/abs/1812.10586)&rbrack;

In relation to `homotopy.io`:

* [[Jamie Vicary]], _Strictly associative and unital higher categories_, talk at the _[2018 Midland Graduate School Christmas Seminar](http://www.cs.bham.ac.uk/~axj/2018-mgs-xmas.html)_ ([pdf](http://www.cs.bham.ac.uk/~axj/files/mgs-xmas-2018-Jamie.pdf)).

* [[David Reutter]], [[Jamie Vicary]], _High-level methods for homotopy construction in associative $n$-categories_, LICS '19: Proceedings of the 34th Annual ACM/IEEE Symposium on Logic in Computer ScienceJune **62** (2019) 1–13 &lbrack;[arXiv:1902.03831](https://arxiv.org/abs/1902.03831), [doi:10.1109/LICS52264.2021.9470575](https://doi.org/10.1109/LICS52264.2021.9470575)&rbrack;

* [[Lukas Heidemann]], [[David Reutter]], [[Jamie Vicary]], *Zigzag normalisation for associative $n$-categories*, Proceedings of the Thirty-Seventh Annual ACM/IEEE Symposium on Logic in Computer Science (LICS 2022) &lbrack;[arXiv:2205.08952](https://arxiv.org/abs/2205.08952), [doi:10.1145/3531130.3533352](https://dl.acm.org/doi/10.1145/3531130.3533352)&rbrack;


category: software