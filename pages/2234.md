
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The __centralizer subgroup__ (also: _[[commutant]]_) of a [[subset]] $S$ in (the [[set]] [[forgetful functor|underlying]]) a [[group]] $G$ is the [[subgroup]] 

$$
  C_G(S) \subset G
$$ 

of all [[elements]] $c \in G$ which commute with $S$, hence such that $c \cdot s = s \cdot c$ for all $s \in S$.  

Notice the similarity with but difference to the concept of _[[normalizer subgroup]]_.

The centralizer of $S$ is clearly a [[subgroup]] of its [[normalizer]]

$$
  C_G(S)
  \subset
  N_G(S)
$$

as fixing the set $g H = H g$ is a weaker requirement than  $g h=h g$ for all $h\in H$.

## Related concepts

* [[stabilizer subgroup]]

* [[normalizer subgroup]]

## References

See also 

* Wikipedia, _[Centralizer and normalizer](https://en.wikipedia.org/wiki/Centralizer_and_normalizer)_

[[!redirects centralizers]]

[[!redirects centralizer subgroup]]
[[!redirects centralizer subgroups]]