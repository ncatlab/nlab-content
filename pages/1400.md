An **anabicategory** is a particular notion of _weak [[2-category]]_ appropriate in the absence of the [[axiom of choice]] (including in many [[internal category|internal]] contexts).  It is derived from the notion of [[bicategory]] by replacing the [[composition functor]]s $\circ: B(y,z) \times B(x,y) \to B(x,z)$ with [[anafunctor]]s (and therefore the [[associator]]s and [[unitor]]s with [[ananatural transformation]]s).

+-- {.query}
[[Zoran Škoda]]: I understand that there is a version of $Cat$ using anafunctors, but it is not clear to me 
what are the axioms for a variant of 2-category which this example belongs to. I do not understand what you mean by replacing hom-functor with anafunctor in that definition: I mean which definition of bicategory is phrased in terms of hom-functors; standard definition talks associators and so on...Please be more explicit. 

[[Mike Shulman|Mike]]: Is this version clearer?

_Toby_:  Or look at the complete definition in the reference that I just added.
=--

If [[Cat]] is defined as consisting of ([[small category|small]]) [[category|categories]], anafunctors, and [[ananatural transformation]]s (as is most appropriate in the absence of choice), then $Cat$ is naturally an anabicategory rather than any stricter notion.

+--{: .query}
[[Mike Shulman|Mike]]: Is that only because of the non-canonicity of pullbacks in $Set$?  If our version of $Set$ has canonical chosen pullbacks, do we get an ordinary bicategory?

_Toby_:  H\'m ... as I recall, you get an ordinary bicategory using canonical pullbacks and general anafunctors, but if you move to *saturated* anafunctors, then you still only get an anabicategory.  I should check this and then rewrite (here and at [[Cat]]) to say it correctly.  (Of course, if you really use anafunctors, then you should only *want* an anabicategory.)
=--

# Reference #

*  [[Michael Makkai]]; Avoiding the axiom of choice in general category theory; section 3 (which is part 4 [here](http://www.math.mcgill.ca/makkai/anafun/)).