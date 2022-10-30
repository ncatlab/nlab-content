

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **simplicial operad** is an [[operad]] over [[sSet]]. It has for each $k \in \mathbb{N}$ a [[simplicial set]] of $k$-ary operations.

## Structures on the category of simplicial operads

### Model structure

There is a [[model category]] structure on the [[category]] of simplicial operads that makes them [[presentable (∞,1)-category|present]] [[(∞,1)-operad]]s. See [[model structure on operads]].

There is a [[Quillen equivalence]] between this model structure and the [[model structure on dendroidal sets]], via the [dendroidal homotopy coherent nerve](http://ncatlab.org/nlab/show/dendroidal+set#HomotopyCoherentNerve).


## Examples

### Classes of examples

* Every operad over [[Set]] may be regarded as a simplicial operad, via the [[discrete object]] embedding $Disc : Set \to sSet$. 

* Every [[topological operad]] induces a simplicial operad by applying the [[singular simplicial complex]] functor $Sing : Top \to sSet$ degreewise.

* Every [[dendroidal set]] induces a simplicial operad via the [[right adjoint]] to the [dendroidal homotopy coherent nerve](http://ncatlab.org/nlab/show/dendroidal+set#HomotopyCoherentNerve).

### Specific examples

* The [[Barrat-Eccles operad]] has, as a simplicial operad, a single color, and its simplicial set of $n$-ary operations is the [[nerve]] $N(\Sigma_n//\Sigma_n)$ of the [[action groupoid]] $\Sigma_n // \Sigma_n$ of the [[symmetric group]] $\Sigma_n$ acting on itself. This is a [[contractible]] simplicial set in each degree, and, indeed, this operad is a [[resolution]] of [[Comm]], which has the point in each degree. 

## Related concepts

* [[topological operad]]

* [[dg-operad]]

* [[dendroidal set]]

[[!redirects simplicial operads]]
