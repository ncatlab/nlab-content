

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

__Homotopy products__ are [[Cartesian products]] in [[homotopy theory]], hence are a special case of [[homotopy limits]] for the case that the the indexing [[diagram]] is a [[discrete category]].

## Computation

In any [[model category]], the homotopy product
of a family of objects $\{A_i\}_{i\in I}$
can be computed by [[fibrant resolution|fibrantly replacing]] each $A_i$
and computing the (ordinary) [[Cartesian product]]
of the resulting family $\{\mathrm{R}A_i\}_{i\in I}$ of [[fibrant objects]].

## Examples

\begin{example}
**(homotopy products of simplicial sets)**\linebreak
In [[simplicial sets]] with [[simplicial weak equivalences]] (as in the [[classical model structure on simplicial sets]]), finite homotopy products can be computed by taking their (ordinary) [[Cartesian product]], because [[finite products]] preserve [[simplicial weak equivalences]]. More generally, homotopy products can be computed by applying Kan's [[Ex^∞]] functor to each [[simplicial set]] and taking their (ordinary) [[Cartesian product]]. 
\end{example}

\begin{example}
**(homotopy products of topological space)**\linebreak
In [[topological spaces]] with [[weak homotopy equivalences]], as in the [[classical model structure on topological spaces]], every object is [[fibrant object|fibant]], so that
homotopy products can be computed as ordinary [[Cartesian products]], which here means [[product spaces]].
\end{example}

\begin{example}
The same applies to the [[relative category]]
of [[chain complexes]] of [[abelian groups]] and [[quasi-isomorphisms]]
([Grothendieck 1957](#Grothendieck1957), section 1.5), 

One way to see this is that in the *projective* [[model structure on chain complexes]] (when it exists) again every object is a [[fibrant object]].
\end{example}

## Related notions

* [[Cartesian product]]

* [[homotopy limit]]

* [[homotopy pullback]]

* [[homotopy equalizer]]

* [[homotopy totalization]]

## References

* {#Grothendieck1957} [[Alexander Grothendieck]], _[[Tohoku|Sur quelques points d'algèbre homologique]], T&#244;hoku Math. J. vol 9, n.2, 3, 1957.

[[!redirects homotopy products]]

