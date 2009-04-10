# Idea #

Cardinals are one generalization of [[natural numbers object|natural numbers]] to non-finite numbers.


# Definition ##

In naive set theory, the  **cardinals** or **cardinal numbers** are the [[isomorphism]] classes in the [[category]] [[Set]]. This definition is unpleasant because each of them is then a proper class (and one could not make further sets using them as elements). For this reason, in axiomatic set theory one usually chooses the canonical representatives of cardinals among [[ordinal]]s. In this vein, a **cardinal** is an ordinal ([[well-order|well-ordered]] [[transitive set]]) which is not equipotent (bijective) to any smaller (with respect to the total order $\in$ on the class $\mathbf{Ord}$ of ordinals) ordinal. 

The cardinality of a finite set is a **finite cardinal**, that of a non-finite set is a **infinite** or **transfinite** cardinal.



# Cardinal arithmetic #

For $S$ a [[set]], write $|S|$ for its cardinality. Then the standard operations in the [[cartesian closed category]] [[Set]] induced arithmetic operations on cardinals:

for $S_1$ and $S_2$ two sets, the  **product** of their cardinalities is the cardinality of their [[product]] in [[Set]]

$$
  |S_1| \cdot |S_2| := | S_1 \times S_2|
  \,.
$$

In as far as the [[hom-set]] $S_1^{S_2}$ exists (as a set),
the exponentiation of $|S_1|$ by $|S_2|$ is the cardinality of the [[hom-set]]

$$
  |S_1|^{|S_2|} := | Set(S_1,S_2)  |
  \,.
$$

A cardinal $|S_1|$ is said to be **smaller or equal** to another cardinal $|S_2|$ precisely if there exists an [[monomorphism|injection]] of the corresponding sets

$$
  (|S_1| \leq |S_2|)
  \Leftrightarrow
  (\exist (S_1 \hookrightarrow S_2))
  \,.
$$

# Regular cardinals #

A transfinite cardinal $\pi$ is **regular** if given a function of sets $P \to X$ where $|X| \lt \pi$ and $|P_x| \lt \pi$ for all $x \in X$, then $|P| \lt \pi$.

In ordinal picture, a cardinal $\pi$ is **regular** if it is not a union of $\lt\pi$ cardinals. A cardinal is a **strongly limiting cardinal** if $\lambda\lt \pi$ implies $2^\lambda\lt\pi$ (hence, in ordinal picture, if $A\in\pi$ then the partitive (=power) set $P(A)\in\pi$). An [[inaccessible cardinal]] is any uncountable strongly limiting regular cardinal. 


# Properties #

* With the [[order]]ing as above, cardinals are [[well-order|well-ordered]].

* For every cardinal $\pi$, we have $2^\pi \gt \pi$.

* For every transfinite cardinal $\pi$ we have $\pi \cdot \pi = \pi$.

* The [[well-order|succesor]] of an infinite cardinal is a regular cardinal.

#References#

For a generalization of cardinality from sets to [[groupoid]]s see [[groupoid cardinality]].