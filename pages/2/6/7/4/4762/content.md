
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

An _$n$-hypergroupoid_ is a model for an [[n-groupoid]]: it is an [[Kan complex]] that is like the [[nerve]] of a [[groupoid]] ($n= 1$), [[bigroupoid]] ($n = 2$) etc.

## Definition

An **$n$-hypergroupoid** is a [[Kan complex]] $K$ in which the [[horn]]-fillers are _unique_ in dimension greater than $n$:

$$
  (k \gt n) \Rightarrow
  \left(
     \array{
       \Lambda^i[k] &\to&  K
       \\
       \downarrow & \nearrow_{\exists !}
       \\
       \Delta[k]
     }
  \right)
  \,.
$$

The lower dimensional horn fillers of course also exist, but are not in general unique.

Equivalently, this are those [[Kan complex]]es which are $(n+1)$-[[coskeletal]] and such that the $(n+1)$-horns have unique fillers.

## Properties

* 1-hypergroupoids are precisely the [[nerve]]s of [[groupoid]]s.

* 2-hypergroupoids are precisely the [[Duskin nerve]]s of [[bigroupoids]].

## References

The term _hypergroupoid_ is due to Duskin and his student P. G. Glenn:

* Paul G. Glenn, Realization of cohomology classes in arbitrary exact categories, J. Pure Appl. Algebra 25, 1982, no. 1, 33-105, [MR83j:18016](http://www.ams.org/mathscinet-getitem?mr=83j:18016)

The term _exact $n$-type_ is used in

* [[Tibor Beke]], _Higher &#268;ech theory_ , K-Theory 32, 2004, 293-322.

[[!redirects hypergroupoids]]

[[!redirects n-hypergroupoid]]
[[!redirects 1-hypergroupoid]]
[[!redirects 2-hypergroupoid]]

[[!redirects n-hypergroupoids]]
[[!redirects 1-hypergroupoids]]
[[!redirects 2-hypergroupoids]]