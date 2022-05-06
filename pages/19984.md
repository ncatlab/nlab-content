<div style="float:right;margin:0 20px 10px 20px;"><img width = "450" src="https://www.cs.bham.ac.uk/~vicaryjo/images/face_of_pentagon.jpg" alt="Screenshot of homotopy.io" /></div>

## Introduction ##

### Overview ###

This page describes _homotopy.io_, a web-based [[proof assistant]] for finitely-presented [[globular set|globular]] [[higher categories|_n_-categories]], for arbitrary _n_. It is based on the theory of [[associative n-categories|associative _n_-categories (ANCs)]], which provides a strictly associative and unital model of composition that minimizes proof bureaucracy, with all the weak structure in homotopies of composites. The proof assistant allows the user to define generators for a higher category, compose them, apply homotopies, and visualize the resulting composites as [[string diagrams]] in 2 dimensions or [[surface diagrams]] in 3 dimensions. Interaction with the proof assistant is entirely by direct manipulation using the mouse.

The proof assistant is still under development, and is not yet released for general use. It can be considered a successor to the existing proof assistant [[Globular]], which allows the construction of formal proofs in a strictly associative and unital model of 4-categories.

Homotopy construction in _homotopy.io_ enabled by two basic mechanisms: _contraction_, which makes the geometry locally more singular; and _expansion_, which makes the geometry locally more generic. These local moves are then propagated to the surrounding geometry by pushout and pullback constructions, 'dragging' neighbouring parts of the composite, and allowing the construction of nontrivial homotopies. It is an open question whether these contraction and expansion moves are capable of generating all possible homotopies in every dimension.

The image at the top-right shows a 3d surface diagram of one side of the pentagon equation.

### Contributors ###

The underlying formal theory of [[associative n-categories|associative _n_-categories]] is due to [Christoph Dorn](https://www.cs.ox.ac.uk/people/christoph.dorn/), [Christopher Douglas](https://www.maths.ox.ac.uk/people/christopher.douglas) and [Jamie Vicary](https://www.cs.bham.ac.uk/~vicaryjo/). The proof assistant has been implemented by [Lukas Heidemann](https://github.com/zrho) and [Jamie Vicary](https://www.cs.bham.ac.uk/~vicaryjo/), based on further theoretical work by [Christoph Dorn](https://www.cs.ox.ac.uk/people/christoph.dorn/), [David Reutter](https://www.cs.ox.ac.uk/people/david.reutter/) and 
[Jamie Vicary](https://www.cs.bham.ac.uk/~vicaryjo/).