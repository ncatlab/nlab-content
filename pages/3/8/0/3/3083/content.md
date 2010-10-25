
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[homotopy]] between [[continuous function]]s between [[topological space]]s is called _delayed_ if it starts out being constant near one boundary of the interval.

(If it is constant near both boundaries we say it has [[sitting instant]]s).

## Definition

For $I = [0,1]$ the [[unit interval]] and $X$ and $Y$ any [[topological space]]s, a [[continuous map]] $F: X\times I\to Y$ is a **delayed homotopy** (between $F(-,0)$ and $F(-1))$  if there exist $t_0\gt 0$ such that $F(x,t)=F(x,0)$ for all $0\leq t\leq t_0$. 

## Properties

### In Dold-fibrations

Delayed homotopies appear in an alternative characterization of [[Dold fibration]]s.  See there for details.

### Smoothing of delayed homotopies

If a continuous homotopy between two [[smooth function]]s is delayed at both ends of the inerval it may be approximated by a _smooth homotopy_ . See [[Steenrod-Wockel approximation theorem]].

[[!redirects delayed homotopies]]