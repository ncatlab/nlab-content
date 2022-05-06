
# Relative complements
* table of contents
{: toc}

## Idea

The relative complement of $A$ in $B$ is like the [[complement]] of $A$, but relative to $B$.


## Definitions

### For subsets

Given two [[subset]]s $S$ and $T$ of a given ambient [[set]] $X$, the __relative complement__ of $S$ in $T$ is the set
$$ T \setminus S = \{ a \;|\; a \in T \;\wedge\; a \notin S \} .$$
That is, $T \setminus S$ consists of those elements of $T$ that are not elements of $S$.  This is also called the __difference__ of the sets; $T \setminus S$ may even be written $T - S$.  (Compare the [[symmetric difference]].)


Note that the relative complement of $S$ in the ambient set $X$ is simply the [[complement]] $\setminus S$ of $S$; sometimes this is called the _absolute_ complement.  Conversely, $T \setminus S$ is the [[intersection]] of $T$ and $\setminus S$.


### In material set theory

In [[material set theory]], all sets are subsets of the [[proper class]] $V$ of all sets (or all small things, if we might have atoms).  In this case, there is no absolute complement (except as a proper class), but we can still form the relative complement:
$$ T \setminus S = \{ a \in T \;|\; a \notin S \} .$$


### In a lattice

Given a [[lattice]] $L$ and two elements $x$ and $y$ of $L$, a __relative complement__ of $x$ relative to $y$ is an element $y \setminus x$ such that:

*  $ x \wedge (y \setminus x) = \bot $ (where $\wedge$ is the [[meet]] in the lattice and $\bot$ is the [[bottom]] of the lattice) and
*  $ y \leq x \vee (y \setminus x) $ (where $\vee$ is the [[join]] in the lattice).

In a [[poset]] that is not a lattice, the same definition applies, with the existence of the relevant meet, join, and bottom bring required for the complement to exist.  In any case, complements are unique.  In a [[proset]], we may speak of *a* complement, or [[the]] complement up to equivalence.


The term _Boolean ring_ is sometimes used for something like a [[Boolean algebra]] in which there may be no [[top]] element (and therefore no complements) but still relative complements; compare the notions of _ring_ vs _algebra_ at [[sigma-algebra]].  That is, a Boolean ring is a [[bounded lattice|bounded-below]] [[distributive lattice]] in which all relative complements exist.


In [[classical mathematics]], this definition includes the previous ones; the [[power set]] of $X$ is a Boolean algebra, while the class of all sets is (in the sense above) a large Boolean ring.


### Relative pseudocomplements

Given a [[lattice]] $L$ and two elements $x$ and $y$ of $L$, a __relative pseudocomplement__ of $x$ relative to $y$ is an element $y \setminus x$ such that:

*  $ x \wedge (y \setminus x) = \bot $ and
*  given any $z$ such that $ x \wedge z = \bot $, $ y \wedge z \leq y \setminus x $.

The same issues apply about posets, uniqueness, and prosets.  A [[bounded lattice|bounded-below]] [[distributive lattice]] in which all relative pseudocomplements exist may be called a [[Heyting algebra|Heyting ring]], although I don't know if anybody does.  The set-theoretic examples are now valid even in [[constructive mathematics]] (although constructivists don't add ‘pseudo’ in that context).


If a relative complement exists, then every relative pseudocomplement is a relative complement (and vice versa), so the same notation may be used.  (Of course, some authors may intend for the notation to *imply* existence of a relative complement, so some care is still needed.)


[[!redirects relative complement]]
[[!redirects relative complements]]

[[!redirects relative pseudocomplement]]
[[!redirects relative pseudocomplements]]

[[!redirects set difference]]
[[!redirects set differences]]
