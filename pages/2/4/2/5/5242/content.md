
# Choice functions
* table of contents
{: toc}

## Idea

Given a set $A$, a choice function for $A$ chooses an element of every subset of $A$, except for the [[empty subset]], of course.


## Definition

Let $A$ be a [[set]].  Let $\mathcal{P}^+A$ be the collection of [[inhabited subsets]] of $A$.  (So if $\mathcal{P}A$ is the [[power set]] of $A$, then $\mathcal{P}^+A$ is contained in $\mathcal{P}A$, and $\mathcal{P}A \setminus \mathcal{P}^+A = \{\empty\}$.)

A __choice function__ for $A$ is a [[function]] $c$ from $\mathcal{P}^+A$ to $A$ such that $c(x) \in x$ (for every inhabited subset $x$).


## Properties

$A$ is a __[[choice object|choice set]]__ if it has a choice function.  (The choice function need not be unique, and rarely is.)

The __[[axiom of choice]]__ states that every set has a choice function.


## Internalisation

In any [[topos]], the definition above can be [[internalisation|internalised]]; we get the notion of a __choice morphism__.


[[!redirects choice function]]
[[!redirects choice functions]]
[[!redirects choice morphism]]
[[!redirects choice morphisms]]
