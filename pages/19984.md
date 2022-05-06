
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

The image at the top-right shows a 3d surface diagram of one side of the [[pentagon equation]] ([_live workspace_](http://www.cs.bham.ac.uk/~vicaryjo/homotopy.io/nlab/side-of-pentagon.html)).

### Contributors ###

The proof assistant is based on the theory of [[associative n-categories|associative _n_-categories]], which has been worked on by [Christoph Dorn](https://www.cs.ox.ac.uk/people/christoph.dorn/), [Christopher Douglas](https://www.maths.ox.ac.uk/people/christopher.douglas), [David Reutter](https://www.cs.ox.ac.uk/people/david.reutter/) and [Jamie Vicary](https://www.cs.bham.ac.uk/~vicaryjo/). The proof assistant has been implemented by [Lukas Heidemann](https://github.com/zrho), [Nick Hu](https://github.com/NickHu) and [Jamie Vicary](https://www.cs.bham.ac.uk/~vicaryjo/).

## References

* [[Christoph Dorn]], _Associative $n$-categories_, talk at _[103rd Peripatetic Seminar on Sheaves and Logic](https://www.math.muni.cz/~loregianf/PSSL103/PSSL103.php)_ ([pdf](https://www.math.muni.cz/~loregianf/PSSL103/slides/Dorn.pdf)).

* [[Christoph Dorn]], _Associative $n$-categories_, PhD thesis ([pdf](https://www.dornchristoph.com/writing/dphil_intro.pdf), [arXiv:1812.10586](https://arxiv.org/abs/1812.10586)).

* [[Jamie Vicary]], _Strictly associative and unital higher categories_, talk at the _[2018 Midland Graduate School Christmas Seminar](http://www.cs.bham.ac.uk/~axj/2018-mgs-xmas.html)_ ([pdf](http://www.cs.bham.ac.uk/~axj/files/mgs-xmas-2018-Jamie.pdf)).

