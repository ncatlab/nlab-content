A __directed join__ is simply a [[join]] of a [[directed set]].

More precisely, if $P$ is a [[poset]] and $D$ is a [[subset]] of $P$, then we can consider the join $\bigvee D$ (if it exists) of $D$ in $P$.  Since $D$ is a poset in its own right, we can also consider whether $D$ is directed set.  If so, then $\bigvee D$ (if it exists) is a __directed join__ in $P$.  Sometimes one denotes that $\bigvee D$ is a directed join by making a little arrow out of the upper-right flank of the symbol (so it\'s a mix of '$\bigvee$' and '$\nearrow$').  Unfortunately, I haven\'t found that symbol in iTeX or Unicode.

A __codirected meet__ in $P$ is a directed join in $P^\op$, but people don\'t talk about those so much.

If $P$ has all finitary joins (a [[bottom element]] and binary joins are enough) and all directed joins, then it has all joins.

[[Directed colimits]] and [[filtered colimits]] are two slightly different [[categorifications]] of directed joins.

A [[topological space]] (or [[locale]]) $X$ is [[compact space|compact]] if and only if $X$ may be expressed as a directed join of open subsets only trivially.  That is, whenever $D$ is a directed collection of opens, if $X = \bigcup D$, then $X \in D$.


[[!redirects directed join]]
[[!redirects directed meet]]
[[!redirects codirected meet]]