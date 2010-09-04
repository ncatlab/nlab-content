# Directed joins
* table of contents
{: toc}

## Idea

A __directed join__ is simply a [[join]] of a [[directed set]].


## Definitions

More precisely, if $P$ is a [[poset]] and $D$ is a [[subset]] of $P$, then we can consider the join $\bigvee D$ (if it exists) of $D$ in $P$.  Since $D$ is a poset in its own right, we can also consider whether $D$ is directed set.  If so, then $\bigvee D$ (if it exists) is a __directed join__ in $P$.  Sometimes one denotes that $\bigvee D$ is a directed join by making a little arrow out of the upper-right flank of the symbol (so it\'s a mix of '$\bigvee$' and '$\nearrow$').  Unfortunately, I haven\'t found that symbol in LaTeX or Unicode.

A __codirected meet__ in $P$ is a directed join in $P^\op$, but people don\'t talk about those so much.

By default, we mean *finitely* directed sets, that is $\aleph_0$-directed.  If instead we take the join of a $\kappa$-directed set (for some [[regular cardinal]] $\kappa$), then we have a __$\kappa$-directed join__.


## Properties

If a join-[[semilattice]] (a poset with all finitary joins) has all directed joins, then it has all joins (and so is a [[suplattice]], equivalently a [[complete lattice]]).  More generally, if a poset has all joins of fewer than $\kappa$ elements and all $\kappa$-directed joins, then it is a suplattice.

A [[topological space]] (or [[locale]]) $X$ is [[compact space|compact]] if and only if $X$ may be expressed as a directed join of open subsets only trivially.  That is, whenever $D$ is a directed collection of opens, if $X = \bigcup D$, then $X \in D$.

[[Directed colimits]] and [[filtered colimits]] are two slightly different [[categorifications]] of directed joins.


## DCPOs

A poset which has all directed joins is called a __directed-complete partial order__, or __[[dcpo]]__.  The [[homomorphisms]] of DCPOs are those [[functions]] that preserve directed joins; these are also called __Scott-continuous__ because they are precisely the [[continuous maps]] relative to the [[Scott topology]] on the DCPOs.

A __pointed dcpo__ is a DCPO with a [[bottom element]] (which is rather more specific than a [[pointed object]] in the category of DCPOs).

DCPOs are studied widely in [[domain theory]].


[[!redirects directed join]]
[[!redirects directed joins]]

[[!redirects directed meet]]
[[!redirects directed meets]]
[[!redirects codirected meet]]
[[!redirects codirected meets]]
