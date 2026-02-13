
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

## Definition

A topological [[subspace]] $A$ of a [[topological space]] $X$ is a **neighborhood retract** if there is a [[neighborhood]] $U\supset A$ in $X$ such that $A$ is a [[retract]] of $U$. 

A [[metrisable space|metrisable]] topological space $Y$ is an _[[absolute neighborhood retract]]_ if for _any_ [[embedding of topological spaces|embedding]] $Y\subset Z$ as a [[closed subspace]] in a [[metrisable topological space]] $Z$, $Y$ is a neighborhood retract of $Z$.

A pair $(X,A)$ where $A$ is a [[closed subspace]] of $X$ is an **NDR-pair** (for 'Neighbourhood Deformation Retract') or a *closed Borsuk pair* if there is a function $u \colon X \to I=[0,1]$ and a [[homotopy]] $H \colon X\times I\to X$ such that $H(x,0)=x$, for all $x\in X$, $H(a,t)=a$ for all $a\in A$, $H(x,1)\in A$ for all $x\in X$ such that $u(x)\lt 1$ and $u^{-1}(0)\subset A$. (See _[[deformation retract]]_.)

## Properties

The canonical inclusion $i:A\hookrightarrow X$ corresponding to an NDR-pair $(X,A)$ is a closed [[Hurewicz cofibration]]. 

## Related concepts

* [[retract]], [[deformation retract]]

## References

Textbook accounts:

* [[Peter May]], Section 6.4 of: _[[A concise course in algebraic topology]]_, University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))


[[!redirects neighborhood retracts]]

[[!redirects neighbourhood retract]]
[[!redirects neighbourhood retracts]]



[[!redirects NDR-pair]]
[[!redirects NDR-pairs]]

[[!redirects NDR pair]]
[[!redirects NDR pairs]]
