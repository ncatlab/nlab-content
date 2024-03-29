
* table of contents
{: toc}

## Definition

Given an element $a$ of a [[Boolean algebra]] (or other [[poset]]) $A$, recall that $a$ is an **[[atom]]** in $A$ if $a$ is [[minimal element|minimal]] among non-trivial (non-[[bottom]]) elements of $A$.  That is, given any $b \in A$ such that $b \leq a$, either $b = 0$ or $b = a$.

$A$ is __atomic__ if we have $b = \bigvee_I a_i$ for every $b \in A$, where $\{a_i\}_I$ is some set of atoms in $A$.

If $A$ is complete we can write it: if for every $b \in A$, we have $b = \bigvee \mathcal{A}(b)$ where $\mathcal{A}(b)$ is the set of all the atoms $a$ in $A$ such that $a \leq b$. Or: for every $b \in A$, we have $b \le \bigvee \mathcal{A}(b)$.

## Properties

* A [[complete lattice|complete]] atomic Boolean algebra is necessarily a [[power set]]; see [[CABA]].

[[!redirects atomic Boolean algebra]]
[[!redirects atomic Boolean algebras]]
