
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


## Idea

The **upper central series** of a [[group]], $G$, is an ascending [[sequence]] of [[subgroups]]

$$
  Z^0(G) \leq Z^1(G) \leq Z^2(G) \leq \ldots,
$$

where the zeroth member is the [[trivial group]], the first member is the [[center]], the second member is the second center, and so on. 

$$
  Z^0(G) 
  \,=\, 1, 
  \;\;
  Z^1(G) = Z(G), 
  \;\;
  Z^2(G)/Z^1(G) = Z(G/Z^1(G)), 
  \;\; 
  Z^3(G)/Z^2(G) = Z(G/Z^2(G)), 
  \;\;
  \ldots
$$

The indexing may be continued to the [[ordinals]], where the member indexed by a limiting ordinal is the union of all previous members.

For a [[nilpotent group]], the upper central series reaches the whole group in finitely many steps, and is the fastest ascending [[central series]]. It has the same length then as the [[lower central series]], although they need not coincide.

## Related concepts

* [[lower central series]]

## References

See also:

* Wikipedia, *[Central series](https://en.wikipedia.org/wiki/Central_series)*

* [Groupprops](http://groupprops.subwiki.org/wiki/Upper_central_series)



