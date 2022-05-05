

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop #MatricesOverPrincipalIdealDomainsHaveSmithNormalForm}
###### Proposition
**([[matrices]] over [[principal ideal domains]] [[matrix equivalence|equivalent]] to [[Smith normal form]])**

For $R$ a [[commutative ring]] which is a [[principal ideal domain]] (for instance $R = \mathbb{Z}$ the [[integers]]), every [[matrix]] $A \in Mat_{n \times m}(R)$ with entries in $R$ is [[matrix equivalence|matrix equivalent]] to a [[diagonal matrix]] filled up with zeros:

There exist [[invertible matrices]] $P \in Mat_{n \times n}(R)$ and $Q \in Mat_{m \times m}(R)$ such that the [[matrix product|product matrix]] $P A Q$ is of the following form:

$$
  P A Q
  \;=\;  
$$
<center>
<img src="https://ncatlab.org/nlab/files/SmithNormalForm.jpg" width="300">
</center>

such that, moreover, each $a_i$ [[divisor|divides]] $a_{i+1}$.

=--

## Related concepts

* [[Hermite normal form]]

## References

Lecture notes include

* [[Patrick Morandi]], _The Smith Normal Form of a Matrix_, 2005 ([pdf](http://sierra.nmsu.edu/morandi/notes/SmithNormalForm.pdf))

* Sam Evans, _Smith normal form over the integers_ ([pdf](https://www3.nd.edu/~sevens/smithform.pdf))

* Bill Casselman, _Hermite and Smith forms_, 2011 ([pdf](http://www.math.ubc.ca/~cass/siegel/Smith.pdf))

See also 

* Wikipedia, _[Smith normal form](https://en.wikipedia.org/wiki/Smith_normal_form)_

[[!redirects Smith normal forms]]
