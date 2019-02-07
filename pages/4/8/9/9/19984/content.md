
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

* [https://homotopy.io](https://homotopy.io)

It is based on the theory of [[associative n-categories|associative _n_-categories (ANCs)]], which provides a strictly associative and unital model of composition. This reduces proof bureaucracy, with all the remaining weak structure in homotopies of composites, which a direct geometrical interpretation. The proof assistant allows the user to define [[generators and relations|generators]] for a [[higher category]], [[composition|compose]] them, apply [[homotopies]], and visualize the resulting composites as [[string diagrams]] in 2 dimensions or [[surface diagrams]] in 3 dimensions. Interaction with the proof assistant is entirely by direct manipulation using the mouse.

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

**Homotopies.** Once a diagram has been constructed, we can modify it by applying homotopies, triggered by clicking and dragging on the diagram. If this is performed on the boundary of the diagram, it will attach the homotopy to the boundary of the diagram; if this is performed in the interior of the diagram, it will rewrite it.

**Renderer (experimental).** Diagrams can be rendered in both 2d and 3d. At the moment, only the 2d renderer is interactive, allowing diagrams to be manipulated directly using the mouse; the 3d renderer is for display only, and is currently quite buggy, only working reliably for small diagrams with a connected geometry. It is hoped that _homotopy.io_ will soon allow rendering and smooth animation of arbitrary 3d composites.

**Projection.** Diagrams can be high-dimensional, and hence hard to display on a computer screen. _Projection_ causes lower dimensions of the diagram to be ignored; for example, given a 5-dimensional diagram with projection set to 3, you will see a single $(5-3=2)$-dimensional diagram, in which the vertices represent 5-cells, the wires represent 4-cells, and the regions represent 3-cells. Note that projection loses information in general.

**Slice.** For an $n$-diagram with $n \gt 2$, projection will always lose some information about the diagram. _Slicing_ allows an $(n+1)$-dimensional diagram to be viewed as a movie of $n$-dimensional diagrams, in a way which preserves all information about the diagram. For example, for a 9-dimensional diagram with projection set to 3, there are still 6 remaining dimensions to display. With the renderer set to 2d, this leaves 4 dimensions to be handled with slice controls, which allows us to investigate the 6d displayed geometry as a movie of movies of movies of movies of 2d diagrams.

## Combinatorial foundation

The combinatorial data stored by the proof assistant can be understood in terms of zigzags.

+-- {: .num_defn}
###### Definition
In a category $C$, a _zigzag_ is a finite diagram of the following sort:

<img height="120" style="margin-left:auto; margin-right:auto;" src="https://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/zigzag.png" alt="A zigzag" />
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

Given a $|\Sigma|$-typed $n$-diagram $D$, we can then ask if it is _well-typed_ with respect to $\Sigma$. This involves identifying the neighbourhoods of every point, and checking that they agree with the standard type neighbourhoods defined in $\Sigma$. This procedure is explained in the references below.

## Constructing homotopies

A composite diagram can be deformed by clicking and dragging in its interior. If the indicated deformation would be geometrically invalid, an error message is displayed in the lower-right corner, and the diagram does not change. Otherwise, a new diagram is displayed, which is homotopic to the original diagram.

The proof assistant manipulates finite combinatorial structures, and we use the word 'homotopic' with reference to their geometrical realization. We do not make this precise here, nor has it yet been made precise in the literature; for this reason, our use of the term 'homotopy' is not yet well connected to the standard notion.

Every homotopy is either a _contraction_, which make the geometry locally more singular, or an _expansion_, which make it locally more generic. If a homotopy is performed on a diagram at the top level, it is directly constructed by one of the base case procedures given below. Alternatively, if it is performed in a slice of a diagram, the effect on the diagram as a whole is computed by a recursive scheme, which propagates the homotopy up from the slice where it was triggered.

### Triggering homotopies ###

Every homotopy is triggered by choosing an $n$-diagram for $n \geq 2$, choosing some vertex that it contains, and dragging that vertex _vertically_; that is, either up or down.

If the vertex is in _generic position_, meaning that it is the unique vertex at its height, a contraction will be triggered; otherwise, an expansion will be triggered.

The $n$-diagram that we choose could be the diagram as a whole, in which case one of the base cases will be triggered. Alternatively, it could be some slice of the diagram, in which case one of the recursive cases will be triggered.

If we are viewing an $n$-diagram $D$ for $n \geq 3$, then at each height $h$ of the diagram, there is a subdiagram $D_h$ with dimension $n-1 \geq 2$. If we drag a vertex or wire of $D$ _horizontally_ at some height $h$, this will trigger a homotopy in the subdiagram $D_h$, and the recursive case below will apply. This could alternatively be triggered by reducing the projection level by 1, and navigating to the subdiagram $D_h$ directly, and dragging the corresponding vertex up or down.

### Base cases ###

### Recursive cases ###

## Type checking and normalization

## References

* [[Christoph Dorn]], _Associative $n$-categories_, talk at _[103rd Peripatetic Seminar on Sheaves and Logic](https://www.math.muni.cz/~loregianf/PSSL103/PSSL103.php)_ ([pdf](https://www.math.muni.cz/~loregianf/PSSL103/slides/Dorn.pdf)).

* [[Christoph Dorn]], _Associative $n$-categories_, PhD thesis ([pdf](https://www.dornchristoph.com/writing/dphil_intro.pdf), [arXiv:1812.10586](https://arxiv.org/abs/1812.10586)).

* [[Jamie Vicary]], _Strictly associative and unital higher categories_, talk at the _[2018 Midland Graduate School Christmas Seminar](http://www.cs.bham.ac.uk/~axj/2018-mgs-xmas.html)_ ([pdf](http://www.cs.bham.ac.uk/~axj/files/mgs-xmas-2018-Jamie.pdf)).

