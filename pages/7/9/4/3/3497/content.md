
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An $(n,1)$-topos is the [[(n,r)-category|(n,1)-category]] version of a [[topos]].



It is equivalently the truncation of an [[(∞,1)-topos]] to [[n-truncated object of an (infinity,1)-category|(n-1)-truncated objects]].

+--{: .query}
[[Mike Shulman]]: I'm not sure I believe that.  First of all I think the numbering is off---objects of an $(n,1)$-category are $(n-1)$-truncated (right?)---but that's trivial.

My intuition for $(\infty,1)$-things needs work, but I know what a 1-topos and a (Grothendieck) (2,1)-topos is, and I'm pretty sure a 1-topos is not the same as a (2,1)-topos in which all objects are 0-truncated.  In fact, there are no (2,1)-topoi in which all objects are 0-truncated.  What is true is that if $E$ is a (2,1)-topos in which every object is *covered* by a 0-truncated object, then $E$ is equivalent to the category of (2,1)-sheaves on a 1-site (rather than merely a (2,1)-site, as is the case for general (2,1)-topoi), and is thus canonically *associated* to a 1-topos, namely the category of 1-sheaves on that same 1-site.  And in fact, $E$ can be recovered from this 1-topos as the category of (2,1)-sheaves for its canonical topology.  See [[michaelshulman:truncated 2-topos|here]].

[[Urs Schreiber|Urs]]: right, badly formulated. I fixed both problems in the formulation. See HTT, theorem 6.4.1.5 for the full statement.

=--

A collection of $(n-1)$-groupoid-valued [[sheaf|sheaves]]/[[stack]]s.


## Definition

> The equivalent characterizations are in HTT, theorem 6.4.1.5. 

## References

Section 6.4 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 