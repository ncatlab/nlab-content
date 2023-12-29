
* table of contents
{: toc}

## Definition

Given an element $a$ of a [[Boolean algebra]] (or other [[poset]]) $A$, recall that $a$ is an **[[atom]]** in $A$ if $a$ is [[minimal element|minimal]] among non-trivial (non-[[bottom]]) elements of $A$.  That is, given any $b \in A$ such that $b \leq a$, either $b = 0$ or $b = a$.

### For a complete Boolean algebra

Suppose that $A$ is a [[complete Boolean algebra]] i.e. a Boolean algebra which admits arbitrary joins. 

$A$ is __atomic__ if we have $b = \bigvee_I a_i$ for every $b \in A$, where $\{a_i\}_I$ is some set of atoms in $A$.

Equivalently: if for every $b \in A$, we have $b = \bigvee \mathcal{A}(b)$ where $\mathcal{A}(b)$ is the set of all the atoms $a$ in $A$ such that $a \leq b$.

Or: for every $b \in A$, we have $b \le \bigvee \mathcal{A}(b)$.

### For an arbitrary Boolean algebra

The preceding definition no longer makes sense if $A$ doesn't possess at least all the [[joins]] of the form $\bigvee \mathcal{A}(b)$.

We say that an (arbitrary) Boolean algebra $A$ is atomic if for every $b \in A$, b contains an atom i.e. $\exists a \in \mathcal{A}(b)$ such that $a \le b$.

## Properties

* A [[complete lattice|complete]] atomic Boolean algebra is necessarily a [[power set]]; see [[CABA]].

## References

The definition of atomic Boolean algebra in the general case is from: 

* [[R. S. Pierce]],  _A generalization of atomic Boolean algebras_ (1959) &lbrack;[doi:10.2307/2963720](https://doi.org/10.2307/2963720)&rbrack;, &lbrack;[on Project Euclid](https://projecteuclid.org/journals/pacific-journal-of-mathematics/volume-9/issue-1/A-generalization-of-atomic-Boolean-algebras/pjm/1103039463.full)&rbrack;

[[!redirects atomic Boolean algebra]]
[[!redirects atomic Boolean algebras]]
