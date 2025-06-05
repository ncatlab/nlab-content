

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

\begin{definition}\label{MainDefinition}
A [[topological space]] $X$ is called __irreducible__ if it cannot be expressed as a [[finite colimit|finite]] [[union]] of proper [[closed subsets]], or equivalently if any finite collection of [[inhabited set|inhabited]] [[open subsets]] has inhabited [[intersection]].
\end{definition}

If $X$ is irreducible according to Def. \ref{MainDefinition}, then:

* $X$ cannot be expressed as the [[union]] of two proper [[closed subsets]]. Equivalently, any two [[inhabited set|inhabited]] [[open subsets]] have inhabited intersection.

* $X$ cannot be expressed as the [[union]] of the empty collection of proper [[closed subsets]], which implies that $X$ must be [[inhabited set|inhabited]]. Equivalently, the intersection of the empty collection of [[inhabited set|inhabited]] [[open subsets]] has inhabited intersection, which means exactly that $X$ is inhabited.

\begin{remark}\label{CaseOfTheemptySet}
**(role of the empty set)**
\linebreak
  Another common version of Def. \ref{MainDefinition} (cf. [Wikipedia](#Wikipedia)) is to have it speak just about binary unions, as opposed to finite unions. With that definition the [[empty set]] would be irreducible, while according to Def. \ref{MainDefinition} it is not: The empty set is the *empty union* and hence a finite union of proper closed subsets, but not a binary union of such, since it has no proper subsets!

But having the empty set count as reducible is useful, cf. Ex. \ref{SoberTopologicalSpaces} below.
\end{remark}

\begin{definition}
A subset $S$ of a topological space $X$ is an __irreducible subset__ if $S$ is an irreducible topological space with the [[subspace topology]].
\end{definition}


## Examples

\begin{example}
An [[algebraic variety]] is irreducible if its underlying topological space (in the [[Zariski topology]]) is irreducible.
\end{example}

\begin{example}
\label{SoberTopologicalSpaces}
A _[[sober topological space]]_, is one whose only irreducible closed subsets are the [[closures]] of single points.
\end{example}


## Related concepts

* [[separation axiom]]

## References

See also: 

* {#Wikipedia} Wikipedia: *[Irreducible components -- In topology](https://en.wikipedia.org/wiki/Irreducible_component#In_topology)*


[[!redirects irreducible topological spaces]]

[[!redirects irreducible space]]
[[!redirects irreducible spaces]]
