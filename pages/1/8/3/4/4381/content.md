
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The ([[skeleton]] of the) [[core]] [[groupoid]] of [[FinSet]], hence the [[category]] of [[finite sets]] and [[bijections]] ([[permutations]]) between them, is sometimes called the _permutation category_  or the _permutation groupoid_ (e.g. [BMT 2021](#BMT21)). 

It deserves to be called the *symmetric groupoid*, because its [[connected components]] are the [[delooping groupoids]] of all the [[symmetric groups]] $Sym(n)$:

$$
  Core(FinSet)
  \;\simeq\;
  \textstyle{
    \underset{n \in \mathbb{N}}
    {\coprod}
  }
  \,
  \mathbf{B} Sym(n)
  \,.
$$

In its [[skeleton|skeletal]] incarnation on their right , this carries the [[structure]] of a [[strict monoidal category|strict]] [[symmetric monoidal category]] with [[addition]] of [[natural numbers]] as its [[tensor product]]. As such it is the [[free construction|free]] strict symmetric monoidal category on one object (namely on $1 \in \mathbb{N}$).  

The [[presheaves]] on the permutation groupoid are also known as *[[combinatorial species]]*.

## Related concept

* [[FinSet]]

* [[symmetric group]]

* [[combinatorial species]]

* [[braid category]]

## References

* Wikipedia, *[Permutation category](https://en.wikipedia.org/wiki/Permutation_category)*

* {#BMT21} [[John Baez]], [[Joe Moeller]], [[Todd Trimble]], *Schur functors and categorified plethysm* &lbrack;[arxiv:2106.00190](https://arxiv.org/abs/2106.00190)&rbrack;

[[!redirects permutation groupoids]]

[[!redirects permutation category]]
[[!redirects permutation categories]]

[[!redirects symmetric groupoid]]
[[!redirects symmetric groupoids]]





[[!redirects Bij]]
