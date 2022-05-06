
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #LinearExtensionOfAPartialOrder}
###### Definition
**(linear extension)**

Given a [[set]] $X$ equipped with a [[partial ordering]] $\leq$, then a _linear extension_ is a [[linear order]] $\leq_{lin}$ on the same set $S$, such that the [[identity function]] $id_S$ is order-preserving

$$
  (S,\leq) \overset{ id_S }{\longrightarrow} \left(S,\leq_{lin}\right)
  \,.
$$

=--

## Properties

+-- {: .num_prop #ExistenceOfLinearExtensions}
###### Proposition
**(existence of linear extensions)**

For [[finite sets]] linear extensions (Def. \ref{LinearExtensionOfAPartialOrder}) always exist. For non-finite sets this is still the case using the [[axiom of choice]].

=--

([Marczewski 30](#Marczewski30))


## References

* {#Marczewski30} Edward Marczewski, _Sur l'extension de l'ordre partiel_, Fundamenta Mathematicae, 16: 386–389 (1930) ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm16/fm16125.pdf))

See also

* Wikipedia, _[Linear extension](https://en.wikipedia.org/wiki/Linear_extension)_

[[!redirects linear extensions of partial orders]]

[[!redirects linear extensions of partial orders]]
