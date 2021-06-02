
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Definition

Given a unital (typically noncommutative) [[ring]] $R$, the __Jacobson radical__ $J(R)$ is defined as the set of elements $r\in R$ satisfying the following equivalent properties:

1. For each [[simple object|simple]] left $R$-[[module]] $M$, $r M =0$.
2. Each [[maximal ideal|maximal]] left [[ideal]] of $R$ contains $r$.
3. For all $x\in R$, $1 - r x$ is left [[invertible element|invertible]] in $R$.

Alternatively,

4. $J(R)$ is the intersection of all maximal left ideals of $R$.
5. $J(R)$ is the intersection of all maximal right ideals of $R$. 

The properties required remain the same if one interchanges left and right (modules, invertibility etc.) i.e. $J(R)=J(R^{op})$.

$J(R)$ is a $2$-sided [[ideal]] in $R$. The rings for which $J(R)=0$ are called __semiprimitive rings__. In other words, for each nonzero element $r$ in a semiprimitive ring, by the definition, there is a simple module **not** left annihilated by $r$.
Given any ring $R$, the [[quotient object|quotient]] $R/J(R)$ is semiprimitive. 

## Examples

+-- {: .num_example #JacobsonRadicalOfFormalPowerSeriesAlgebra}
###### Example
**(Jacobson radical of [[formal power series algebra]])**

The Jacobson radical of a [[formal power series algebra]] consists of those formal power series whose constant term vanishes.

=--

## Related concepts

* [[radical]]

* [[scale]]

## References

See also

* Wikipedia, _[Jacobson radical](https://en.wikipedia.org/wiki/Jacobson_radical#Examples)_

[[!redirects Jacobson radicals]]

[[!redirects semiprimitive ring]]
[[!redirects semiprimitive rings]]
