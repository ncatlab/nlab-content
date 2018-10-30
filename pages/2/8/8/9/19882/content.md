# Initiality Project - The Term Model

This page is part of the [[Initiality Project]].

* table of contents
{: toc}

## Base Theory

We define a [[Initiality Project - Semantics|category with families]] as follows:

* Its objects are the [[Initiality Project - Type Theory|valid contexts]].  (Do we need to mod out by judgmental equality here?)
* Its types in context $\Gamma$ are the $A$ such that $\Gamma \vdash A\,type$ is derivable, modulo derivable judgmental equalities $\Gamma \vdash A\equiv B \, type$.
* Its terms of type $A$ in context $\Gamma$ are the $T$ such that $\Gamma \vdash T \Leftarrow A$ is derivable, modulo derivable judgmental equalities $\Gamma \vdash S \equiv T : A$.

TODO: prove that this defines a category with families.

## Type formers

### $\Pi$-types

[[!include Initiality Project - Term Model - Pi-types]]

category: Initiality Project