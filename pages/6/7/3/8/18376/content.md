+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents


## Definition

The **isotropy group of a [[topos]]** $T$ is its [[free loop space object]] $I_T$ in [[Topos]], regarded as a group object over $T$.  It is therefore a [[group topos]] in the world of $T$-toposes.

Specifically, this means it is the [[pullback]] of the [[diagonal]] $T \to T\times T$ against itself, in the sense appropriate to $Topos$ as a higher category.

This definition makes sense for (Grothendieck) 1-toposes and also for [[(infinity,1)-topos|higher toposes]].  But in the 1-topos case, the map $I_T \to T$ is automatically [[localic geometric morphism|localic]], since it is a pullback of the diagonal $T\to T\times T$ which is localic, and therefore corresponds to a [[localic group]] internal to $T$.  (In general, if $T$ is an $n$-topos, then $I_T\to T$ will be $(n-1)$-[[n-localic geometric morphism|localic]].)  The group of points of this localic group is then a [[group object]] $Z_T$ in $T$, the **etale isotropy group** of $T$.  The latter captures some but not all of the information about $I_T$.

## Isotropy quotient

Like a free loop space object in any category, $I_T$ acts on all toposes over $T$.  In particular, it acts on [[etale geometric morphisms]] over $T$, and hence on objects of $T$.  The **isotropy quotient** of $T$ is the [[full subcategory]] of objects for which this action is trivial.

The isotropy quotient is contained in the **etale isotropy quotient**, namely the full subcategory of objects for which the action of the etale isotropy group $Z_T$ is trivial, but it may be strictly smaller.

## References

The etale isotropy group of a 1-topos (then called just the "isotropy group") was defined in

* [[Jonathon Funk]], [[Pieter Hofstra]], [[Benjamin Steinberg]]: *Isotropy and crossed toposes*, Theory and Applications of Categories **26** 24 (2012) 660-709 &lbrack;[tac:26-24](http://www.tac.mta.ca/tac/volumes/26/24/26-24abs.html)&rbrack;


It was shown to be the group of points of the localic isotropy group in

* [[Simon Henry]], _The localic isotropy group of a topos_, [arxiv](https://arxiv.org/abs/1706.04835)


[[!redirects isotropy groups of toposes]]


