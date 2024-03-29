
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A _thin homotopy_ between paths $f,g: I \to X$ in a [[topological space]] $X$ (with $I = [0,1]$ the standard [[interval]]) is a [[homotopy (as a transformation)|homotopy]] $I\times I \to X$ which, roughly speaking, has zero area. 

## Definition

### Thin homotopies in smooth spaces ##  

A (smooth) [[homotopy (as a transformation)|homotopy]] $F: I \times I \to X$ between smooth paths in a [[smooth space]] $X$  is called **thin** if the rank of its differential $d F(s,t): T_{s,t} I \times I \to T_{F(s),F(t)} X$ is less than 2 for all $s,t \in I \times I$.

(More to go here...)

### Thin homotopies in topological spaces ##

The following is taken from

* [[K. A. Hardie]], [[K. H. Kamps]], [[R.W. Kieboom]], _A homotopy 2-groupoid of a Hausdorff space_, Appl. Cat. Str.**8** (2000).

We define a _finite tree_ to be a one-dimensional finite polyhedron.

A homotopy $F:I\times I \to X$ between paths $F(-,0)$ and $F(-,1)$ in the [[topological space]] $X$ is called **thin** if $F$ factors through a finite tree,
$$
  I\times I \stackrel{F_0}{\to} T \stackrel{F_1}{\to} X
$$
such that the paths $F_0(-,0):I\to T$, $F_0(-,1):I\to T$ are piecewise-linear.

When $X$ is [[Hausdorff space|Hausdorff]], points, paths and thin homotopies in $X$ form a [[bigroupoid]].

## Applications

### Path n-groupoids 

The definition of [[path groupoid]]s and [[path n-groupoid]]s as strict or [[semi-strict infinity-category|semi-strict]] [[n-category|n-groupoids]] typically involves taking morphisms to be thin homotopy classes of paths. See there for more details.

### Parallel transport

The [[parallel transport]] of a [[connection on a bundle]] is an assignment of fiber-homomorphisms to paths in a manifold that is invariant under thin homotopy. 

[[!redirects thin homotopies]]