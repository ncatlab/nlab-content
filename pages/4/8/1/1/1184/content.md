# Definition #

A [[set]] $S$ is **well-ordered** if it is [[order]]ed and every [[inhabited set|inhabited subset]] has a lowest element:

more precisely, if for all $U \subset I$ with $U \neq \emptyset$ there exists $\bottom_U \in U$ such that for all $u \in U$ we have $\bottom_U \leq u$.

# Successor #

A well-ordered set $S$ comes equipped with a **successor** map
$
  succ : S \to S  
  \,.
$
this sends $a \in S$ to the lowest element of the subset $S_a := \{ s \in S, s \gt a\}$.
