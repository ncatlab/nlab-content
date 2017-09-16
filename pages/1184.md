# Definition #

A [[set]] $S$ is **well-ordered** if it is [[total order|totally ordered]] and every [[inhabited set|inhabited subset]] has a lowest element.  That is, for all $U \subset I$ with $U \neq \emptyset$ there exists $\bottom_U \in U$ such that for all $u \in U$ we have $\bottom_U \leq u$.

A total order on $S$ with this property is therefore called a "well-order" on $S$, the cringes of grammarians notwithstanding.  (The term is actually a back formation from the grammatically sensible 'well-ordered set' or 'well ordered set'.  As a noun in its own right, it should be 'well order' or, arguably, even 'good order'.)

+--{: .query}
I for one would be happy to move this to [[well order]].  ---Toby
=--


# Successor #

A well-ordered set $S$ comes equipped with a **[[successor]]** map
$
  succ : S \to S  
  \,.
$
this sends $a \in S$ to the lowest element of the subset $S_a := \{ s \in S, s \gt a\}$.
