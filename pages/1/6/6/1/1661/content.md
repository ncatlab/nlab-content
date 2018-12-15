
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

Given a [[lattice]] $L$ and two elements $x$ and $y$ of $L$, a __relative complement__ of $x$ in $y$ in an element $y \setminus x$ such that:

*  $ x \wedge (y \setminus x) = \bot $ (where $\wedge$ is the [[meet]] in the lattice and $\bot$ is the [[bottom]] of the lattice) and
*  $ y \leq x \vee (y \setminus x) $ (where $\vee$ is the [[join]] in the lattice).


The term _Boolean ring_ is sometimes used for something like a [[Boolean algebra]] in which there may be no [[top]] element (and therefore no complements) but still relative complements; compare the notions of _ring_ vs _algebra_ at [[sigma-algebra]].


In [[classical mathematics]], this definition includes the previous ones; the [[power set]] of $X$ is a Boolean algebra, while the class of all sets is (in the sense above) a Boolean ring.


[[!redirects relative complement]]

[[!redirects set difference]]
