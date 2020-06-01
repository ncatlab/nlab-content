
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

Selection theory asks if given a [[multi-valued function]] $F\colon X \to Y$ does there exist a continuous selector $f\colon X \to Y$, i.e. a single-valued [[continuous function]] such that $f(x) \in F(x)$ for all $x \in X$. A _selection theorem_ states that under certain assumptions on $X, Y, F$ there is indeed a selector. Normally, such assumptions include that $X$ is [[paracompact topological space|paracompact]], $Y$ is some subset of a [[topological vector space]], $F$ is a [[lower semicontinuous map]] (also called hemicontinuous), and $F(x)$ is [[convex set|convex]] for each $x \in X$.

## Selection theorems

\begin{theorem}[Michael selection theorem]
  Let $X$ be [[paracompact topological space|paracompact]], $Y$ a [[Banach space]], $F$ a [[lower semicontinuous map]], and $F(x)$ [[inhabited set|nonempty]], [[convex set|convex]], and [[closed subset|closed]] for every $x\in X$. Then $F$ admits a selector.
\end{theorem}

## Related entries

* [[multi-valued function]]
* [[Michael's theorem]]

## References

* [[Ernest Michael]], _Continuous selections. I_, Annals of Math. __63__ (2): 361&#8211;382 ([doi:10.2307/1969615](http://dx.doi.org/10.2307/1969615), MR0077107)

See also

* Wikipedia, _[Selection theorem](https://en.wikipedia.org/wiki/Selection_theorem)_


[[!redirects selection theory]]
[[!redirects selector]]