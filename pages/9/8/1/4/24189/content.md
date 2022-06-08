+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

In [[homotopy type theory]], a **prespectrum type** is a [[dependent type|dependent]] [[bi-infinite sequence]] of [[types]] $n:\mathbb{Z} \vdash E_n\;\mathrm{type}$ with a dependent [[bi-infinite sequence]] of [[types]] $n:\mathbb{Z} \vdash *_n:E_n$ and a dependent bi-infinite sequence of [[functions]] $n:\mathbb{Z} \vdash e_n:E_n \to \Omega E_{n+1}$ which preserves the point, where $\Omega A$ is the loop space type of $A$. 

In [[Coq]] pseudocode, this becomes

    Definition prespectrum :=
      {X : int -> Type & 
       { pt : forall n, X n &
        { glue : forall n, X n -> pt (S n) == pt (S n) &
          forall n, glue n (pt n) == idpath (pt (S n)) }}}.

## See also ##

* [[pointed type]]
* [[spectrum type]]
* [[spectrification]]

## References ##

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* [[Floris van Doorn]] (2018), _On the Formalization of Higher Inductive Types and Synthetic Homotopy Theory_, ([arXiv:1808.10690](https://arxiv.org/abs/1808.10690), [web](http://florisvandoorn.com/papers/dissertation.pdf))