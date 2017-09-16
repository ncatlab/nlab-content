# Idea #

Cardinals are one generalization of [[natural numbers object|natural numbers]] to non-finite numbers.


# Definition ##

The  **cardinals** or **cardinal numbers** are the [[isomorphism]] classes in the [[category]] [[Set]].

The cardinality of a finite set is a **finite cardinal**, that of a non-finite set is a **transfinite cardinal**.



# Cardinal arithmetic #

For $S$ a [[set]], write $|S|$ for its cardinality. Then the standard operations in the [[cartesian closed category]] [[Set]] induced arithmetic operations on cardinals:

for $S_1$ and $S_2$ two sets, the  *product** of their cardinalities is the cardinality of their [[product]] in [[Set]]

$$
  |S_1| \cdot |S_2| := | S_1 \times S_2|
  \,.
$$

The exponentiation of $|S_1|$ by $|S_2|$ is the cardinality of the [[hom-set]]

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

A transfinite cardinal $\pi$ is **regular** if for $P \to X$ a function of sets with $|X| \lt \pi$ and $|P_x| \lt \pi$ for all $x \in X$ then $|P| \lt \pi$.


# Properties #

* With the [[order]]ing as above, cardinals are [[well-order|well-ordered]].

* For every cardinal $\pi$, we have $2^\pi \gt \pi$.

* For every transfinite cardinal $\pi$ we have $\pi \cdot \pi = \pi$.

* The [[well-order|succesor]] of an infinite cardinal is a regular cardinal.

#References#

For a generalization of cardinality from sets to [[groupoid]]s see [[groupoid cardinality]].