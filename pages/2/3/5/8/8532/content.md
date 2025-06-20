

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



# _TwoVect_: a Mathematica Package for 2-Vector Spaces #
* table of contents
{:toc}


## What is _TwoVect_? ##

_TwoVect_ is a [[Mathematica]] package for working with finite-dimensional [[complex numbers|complex]] [semisimple](semisimple+category) [[2-vector spaces]]. It implements all the basic operations of a skeletal version of **2Vect**, the [[symmetric monoidal bicategory]] of finite-dimensional 2-vector spaces.

2-vector space are categories with many of the same properties as ordinary [[vector spaces]]. There are two main types of 2-vector spaces; the sort we are concerned with here are [[Kapranov-Voevodsky 2-vector spaces]], closely related to the [2-Hilbert spaces](2-Hilbert+space) of [Baez](John+Baez). They have a range of applications in [quantum algebra](quantum+group), [[representation theory]], [[topological quantum field theory]] and [[quantum information]]. This package can help with calculations in these areas.

_TwoVect_ was developed by [Dan Roberts](http://ctpweb.lns.mit.edu/personnel.html) in 2011 as an MSc project, at the [Quantum Group](http://www.cs.ox.ac.uk/activities/quantum/) in the [Department of Computer Science](http://www.cs.ox.ac.uk/) of the [University of Oxford](http://www.cs.ox.ac.uk/), supervised by [Jamie Vicary](http://www.cs.ox.ac.uk/people/jamie.vicary). If you've got any questions, please get in touch.

## How can I get it? ##

Here are download links for the [packages](http://www.cs.ox.ac.uk/people/jamie.vicary/twovect/twovect.zip) and the [user guide](http://www.cs.ox.ac.uk/people/jamie.vicary/twovect/guide.pdf).

## What's it for? ##

The mathematics of 2-vector spaces is often referred to as _[higher linear algebra](higher+algebra)_, and extends the ordinary [[linear algebra]] required for calculations involving traditional vector spaces. This higher linear algebra can be difficult to work with by hand: whereas ordinary linear algebra involves [[matrices]] of [[complex numbers]], higher linear algebra involves matrices of _matrices_ of complex numbers. And whereas ordinary matrices can be composed in two different ways, ordinary composition and [[tensor product]], the theory of 2-vector spaces involves three types of composition: tensor product, [[horizontal composition]] and [[vertical composition]].

While the underlying mathematics of 2-vector spaces is elegant and natural, the combinatorics of these basic operations can make calculations difficult to perform by hand. _TwoVect_ implements the basic operations of higher linear algebra, and can make calculations a lot easier.

Here are some example uses for the package.

* You've worked out the associator and unitors for a [semisimple](semisimple+category) [[monoidal category]], and you want to check the pentagon and triangle equations.

* You've worked out other structure, like a [braiding](braided+monoidal+category), [symmetry](symmetric+monoidal+category) or [ribbon](ribbon+category) structure, and you want to check the defining equations are satisfied.

* You want to use Mathematica's built-in solvers to help find these structures.

* You want to calculate the value of a [[string diagram]] in a semisimple monoidal category.

* You want to check algebraic properties of a semisimple monoidal category. Does it have [duals for objects](dualizable+object)? Is it [modular](modular+tensor+category)?

* You want to check the axioms are satisfied for an [internal monoid object](monoid#inamonoidalcategory) in a semisimple monoidal category, or you want Mathematica to help you find such an object.

* You have chosen higher linear maps to associate to the generators of some [higher algebraic structure](higher+algebra), and want to check the relations are satisfied.

* You want to verify correctness of a quantum protocol, described in terms of the [2-categorical approach to quantum information](http://arxiv.org/abs/1207.4563).

## How does it work? ##

The basic package _TwoVect_ implements a completely skeletal version of **2Vect**, the symmetric monoidal bicategory of finite-dimensional semisimple complex 2-vector spaces, in the following way:

* **2-vector spaces** are represented by natural numbers.

* **[Linear functors](linear+functor)** between 2-vector spaces are represented by matrices of natural numbers.

* **[Natural transformations](natural+transformation)** between linear functors are represented by matrices of matrices of complex numbers.

The three primitive composition operations of **2Vect** are implemented:

* **Tensor product** $\odot$ is a binary operation for which the arguments can be 0-cells, 1-cells or 2-cells.

* **Horizontal composition** $\circ$ is a binary operation, for which the arguments must 1-cells or 2-cells.

* **Vertical composition** $\cdot$ is a binary operation for which the arguments must be 2-cells.

The nonidentity invertible structural 2-cells are also implemented, which account for weakness of horizontal composition and tensor product:

* The **interchanger**: $\tau_{f,g,h,i} : (f \circ g) \odot (h \circ i) \to (f \odot h) \circ (g \odot i)$

* The **compositer**: $\omega_{f,g,h} : f \circ (g \circ h) \to (f \circ g) \circ h$

* The **symmetrizer**: $\sigma_{f,g}: \mathrm{swap} \circ (f \odot g) \to (g \odot f) \circ \mathrm{swap}$

There are also two add-on packages:

* _MTCategories_ provides implementations of the equations for symmetric or braided semisimple monoidal categories.

* _MTCategory_ provides a simplified syntax for working 'inside' a particular choice of monoidal category. Once this is defined, the value of string diagrams can be computed by typing them in using ordinary string diagram syntax.

## How could this be developed? ##

There are several exciting ways this could evolve. If you want to help out, get in touch! Lots of things on this list would involve original research, and could form a part of a Masters or PhD dissertation.

* A graphical front end would be a powerful addition. Compare to [Quantomatic](https://sites.google.com/site/quantomatic/), a GUI for _ordinary_ linear algebra.

* Can _TwoVect_ be connected in a useful way to [computational methods in higher type theory](Rocq)?

* It should be possible to write code that inserts the structural isomorphisms $\tau$, $\omega$ and $\sigma$ _automatically_ where necessary. This would make the package enormously more powerful for certain applications.

* Many more things could be implemented - a test for modularity of a braided monoidal category, quantum doubles, Hopf algebra axioms, module category axioms ...

There are also some more mundane issues that need dealing with.

* The basic functions that perform 2-cell tensor product, horizontal composition and vertical composition haven't been optimized, and run slowly for large inputs. There should be a lot of scope for improving the code, and perhaps also for compilation, which Mathematica supports.

* There are some other strange issues around speed; different ways to tell Mathematica to compute the same thing can give rise to very different calculation times.

* We're not sure how to test systematically whether everything has been implemented correctly.

* There is probably some scope to restructure the packages and make them easier to use.

category: software
