
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

For $C$ a [[category]], a **cylinder functor** on $C$ is a [[functor]] denoted

$$
  (-)\times I : C \to C
$$

equipped with three [[natural transformations]]

$$
  e_0, e_1 : Id_C \to (-)\times I
$$

$$
 \sigma : (-)\times I \to Id_C
$$

such that $\sigma e_0 = \sigma e_1 = Id_C$.

## Remarks 

* A cylinder functor functorially provides _[[cylinder objects]]_ used for talking about [[homotopy]].

* The notation is supposed to be suggestive of a [[product]] with an object $I$. While this is the motivating example, the cylinder functor need not be of that form.

## Cylindrical model structures

[[Richard Williamson]] has developed a way to build a model structure from the simple point of departure of a structured interval in a monoidal category - more generally, a structured cylinder and a structured co-cylinder in a category. This is given in ([Williamson 2013](#Williamson13)).

## References

A very brief introduction to cylinder functors is given starting on page 9 of [[Abstract-Homotopy.pdf|Abstract Homotopy Theory:file]].


A fuller development of their properties is given in

* [[Klaus Heiner Kamps]], [[Timothy Porter]], _Abstract Homotopy and Simple Homotopy Theory_ ([GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))

Cylinder functors also form one of the key elements in Baues' approach to [[algebraic homotopy]]:


* [[Hans-Joachim Baues]], _Algebraic Homotopy_, Cambridge studies in advanced mathematics 15, Cambridge University Press, (1989). 

* [[Hans-Joachim Baues]], _Combinatorial Homotopy and 4-Dimensional Complexes_, de Gruyter Expositions in Mathematics 2, Walter de Gruyter, (1991).

* [[Hans-Joachim Baues]], _Homotopy Types_, in I.M.James, ed., _[[Handbook of Algebraic Topology]]_, 1--72, Elsevier, (1995).

Cylindrical model structures are discussed in

* {#Williamson13} [[Richard Williamson]], _Cylindrical model structure_, PhD thesis, 2012 ([arXiv:3104.0867](https://arxiv.org/abs/1304.0867)) 


[[!redirects cylinder functors]]

