
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _Calabi-Yau category_ is a [[horizontal categorification]] of that of [[Frobenius algebra]] -- a _Frobenius [[algebroid]]_ .

## Definition

### 1-categorical

A **Calabi-Yau category** is a [[Vect]]-[[enriched category]] $C$ equipped for each object $c \in C$ with a [[trace]]-like map

$$
  Tr_C : C(c,c) \to k
$$

to the ground field, such that for all objects $d \in C$ the induced pairing

$$
  \langle -,-\rangle_{c,d} :
  C(c,d) \otimes C(d,c) \to k  
$$

given by 

$$
  \langle f,g \rangle = Tr(g \circ f)
$$

is symmetric and non-degenerate.

A Calabi-Yau category with a single object is the same (or rather the [[delooping]]) of a [[Frobenius algebra]].


### $(\infty,1)$-categorical

A **Calabi-Yau $A_\infty$-category** is an [[A-infinity category]] with the evident non-degenerate trace maps on hom-complexes, as above.


## Properties

Calabi-Yau $A_\infty$-categories classify [[TCFT]]s. This is where they get there name from, because these TCFTs in turn may be constructed from [[sigma-model]]s whose targets ar [[Calabi-Yau space]]s.

## References

For instance section 7.1 and 7.2 of

* [[Kevin Costello]], _Topological conformal field theories and Calabi-Yau categories_ ([atXiv:math/0509264](http://arxiv.org/abs/math/0509264))

[[!redirects Calabi-Yau categories]]

[[!redirects Calabi-Yau A-infinity category]]
[[!redirects Calabi-Yau A-infinity categories]]

[[!redirects Calabi-Yau A-∞ category]]
[[!redirects Calabi-Yau A-∞ categories]]