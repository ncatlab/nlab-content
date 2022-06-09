[[!redirects pointed connected groupoids]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
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

## Definition

A **pointed connected groupoid** is a [[groupoid]] that is [[pointed object|pointed]] and [[connected]]. 

Under the [[looping and delooping]]-[[equivalence of (infinity,1)-categories|equivalence]], this is equivalently the *[[delooping groupoid]]* of a [[group]].

### In homotopy type theory

In [[homotopy type theory]], a __pointed connected groupoid__ consists of

* A type $G$
* A basepoint $e:G$
* A 0-connector 
$$\kappa_1:\prod_{f:G \to \mathbb{1}} \prod_{a:\mathbb{1}} \mathrm{isContr}(\left[\mathrm{fiber}(f, a)\right]_{0})$$
* A 1-truncator:
$$\tau_2:\mathrm{isGroupoid}(G)$$

## See also ##

* [[delooping groupoid]]

* [[group]]

* [[groupoid]]

* [[infinity-group]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], and [[Daniel R. Grayson]], [Symmetry book](https://unimath.github.io/SymmetryBook/book.pdf) (2021) 


