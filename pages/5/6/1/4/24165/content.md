
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

This page considers the [[homotopy type]] of the [[loop space]] of a [[wedge sum]] of [[circles]].
For the moment, the following is entirely geared towards the language of [[homotopy type theory]].

Let $A$ be a [[set]], and consider the [[HIT]] $W_A$ with constructors

* $base:W_A$
* $loop : A \to (base = base)$.

This is the "wedge of $A$ circles". It can also be defined as the [[suspension]] of $A+1$.

## Known facts

* If $A$ has [[decidable equality]], then the [[loop space]] $\Omega W_A$ is the [[nlab:free group]] on $A$.

* For general $A$, it is probably still true that the [[fundamental group]] $\pi_1 W_A$ is the free group on $A$.

## An open problem

For a general set $A$ without decidable equality, is $W_A$ even a 1-type?  What can be said about $\Omega W_A$?

In the classical [[simplicial set model]], $W_A$ is a 1-type for all $A$, since classically all sets have decidable equality.  Moreover, since $W_A$ is definable as a colimit, and being a 1-type is a finite-limit property, this fact is inherited by all [[Grothendieck (infinity,1)-topos|Grothendieck (infinity,1)-topoi]]. Thus, no counterexample to $W_A$ being a 1-type can be found in such models, but it is also not clear how to prove that $W_A$ is a  1-type.

category: homotopy theory


[[!redirects loop spaces of a wedge of circles]]
