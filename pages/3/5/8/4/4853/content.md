
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* the following line creates the automatic table of contents
{: toc}

## Idea

A **link** is a generalisation of a [[knot]] where one is allowed more than one component.  Many [[knot invariants]] extend to [[link invariant]]s and for many such invariants, one needs to know this extension to compute it even for a knot.  Thus the study of links and knots is inextricably intertwined.


## Basics

+-- {: .num_defn #link}
###### Definition
A **link** is an [[embedding]] of a finite number of copies of the [[circle]].  The embedding is usually taken in $\mathbb{R}^3$, or its [[one-point compactification]], $S^3$.
=--

It is possible to generalise this to more varied sources and targets.

Links can be studied in a number of ways depending on the notion of equivalence that is used.  Coming from knot theory, one considers equivalence up to [[isotopy]]; that is, two links are equivalent if there is a homotopy between them which is an embedding for all times.  A weaker notion was consider by [Milnor](#jmLinkGroups) wherein the components of the link are allowed to pass through themselves, but not through other components.  That is, when restricted to each component it must be an immersion for all times, and the images of the components must always be disjoint.


## Examples

### Trivial links

Any [[knot]] is a link, and any [[disjoint union]] of [[unknot]]s (called an __unlink__) is a link.  We may call these 'trivial' (hopefully this name isn\'t standard for something different), in the sense of what you would know about before you study links.


### The Hopf Link

The [[Hopf link]] is the simplest non-trivial (in the sense above) link, consisting of two components linked once.

[[!include Hopf link - SVG]]


### The Borromean Link

It is possible to link together $n$ circles in such a way that removing any one makes the others fall apart.  For $n = 2$, we have the Hopf link above; for $n = 3$, we have the [[Borromean link]], or Borromean Rings.

[[!include Borromean link - SVG]]


### The Whitehead Link

The [[Whitehead link]] is an example of a link that shows the difference between the two notions of equivalence.  If the links are only allowed to move by isotopies, then the two components are linked.  However, if a link is allowed to pass through itself, then they can be unlinked.

[[!include Whitehead link - SVG]]


### Brunnian links

A __Brunnian link__ is a link which is not an unlink but which has the property that the removal of any of its components results in an unlink.  Technically, this includes the Hopf link and any knot (thanks to [this MO question](http://mathoverflow.net/questions/40724/is-the-hopf-link-a-brunnian-link) for settling that issue). The Borromean rings above are an example of a Brunnian link with three components.


## References

* Milnor, J. (1954). Link groups. _Ann. of Math. (2)_, _59_, 177&#8211;195. [MR](http://www.ams.org/mathscinet-getitem?mr=71020){: #jmLinkGroups}


[[!redirects link]]
[[!redirects links]]
[[!redirects Link]]
[[!redirects Links]]

[[!redirects Brunnian link]]
[[!redirects Brunnian links]]
