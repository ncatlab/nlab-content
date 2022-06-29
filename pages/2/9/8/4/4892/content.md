
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--


#&#268;ech homology#
* table of contents
{:toc}

## Idea

Given a [[topological space]] $X$, its *Čech homology* is the [[limit]] of [[simplicial homology]]-[[homology group|groups]] of the [[Čech nerves]] of its [[open covers]], under [[refinement of open covers]].

Compare to the [[singular homology]] of $X$, which is the [[simplicial homology]] of its [[singular simplicial complex]]. For well behaved topological spaces the two notions agree and are jointly known as computing the *[[ordinary homology]]* of $X$. 

## Definition

Given a [[topological space]] $X$ with an [[open cover]], 

$$  
  \mathcal{U}
  \;=\;
  \Big\{
    U_i \xhookrightarrow{open} X
  \Big\}_{i \in I}
$$

we write

\[
  \label{CechNerve}
  C(X,\mathcal{U})
  \;\coloneqq\;
  \pi_0
  \big(
    U^{\times^\bullet_X}
  \big)
  \;\in\;
  sSet
\] 

for the [[simplicial set]] which is its [Čech+nerve](Čech+nerve#FromACover):
whose $n$-[[simplex|simplices]] are the [[inhabited set|inhabited]] $(n + 1)$-fold [[intersections]] of the [[open subsets]] $U_i$ in $\mathcal{U}$. 

\begin{remark}
For sufficiently well-behaved topological spaces $X$ ([[paracompact spaces]]) and *[[good open cover|good]]* open covers, the Čech nerve (eq:CechNerve) is [[simplicial homotopy equivalence|simplicially homotopy equivalent]] to the [[singular simplicial complex]] of $X$ -- this is the statement of the *[[nerve theorem]]*.

However, in general $C(X,\mathcal{U})$ may differ from the [[weak homotopy type]] of $X$ (even in the [[limit]] below) in which case Čech homology may *differ* from the [[singular homology]] of $X$. (See for instance the discussion at *[[well group]]*.)
\end{remark}


If $\mathcal{U}$ is a [[refinement of an open cover|refinement]] open cover, i.e. such that for each $U' \in \mathcal{U}$, there is a $U \in \mathcal{U}$ with $U \subseteq U$, then these inclusions induce a [[morphism]] of [[simplicial sets]]


$$
  C(X,\mathcal{U}) \longrightarrow C(X,\mathcal{U}')
$$

This yields an [[inverse system]] of [[simplicial sets]].


\begin{definition}
The $n$th **Čech homology group** of the space $X$ is the [[limit]] 
$$
  \check{H}_n(X) 
  \;\coloneqq\; 
  \underset{
    \underset{\mathcal{U}}{\longleftarrow}
  }{lim} 
  H_n(X,\,\mathcal{U})
$$
over the [[inverse system]] of [[open covers]] $\alpha$, of the [[simplicial homology]] [[homology group|groups]] of the [Čech nerve](Čech+nerve#FromACover) $C(X,\alpha)$:
$$
  H_n(X,\,\mathcal{U})
  \;\coloneqq\;
  H_n\big(C(X,\,\mathcal{U})\big)
  \,.
$$
\end{definition}

\begin{remark}
It is to be noted that these groups do not constitute a [[homology theory]] in the sense of the [[Eilenberg-Steenrod axioms]] as the _exactness axiom_ fails in general. There is a "corrected" theory known under the name [[strong homology]]. 
\end{remark}

## Related concepts

* [[Čech methods]], [[nerve theorem]]

* [[singular homology]], [[cellular homology]]

* [[ordinary homology]]

* [[étale homotopy type]]

* [[well group]]


## References

Exposition:

* [[David H. Fremlin]], Section 2 of: _Singular homology for amateurs_ (2016) $[$[pdf](https://www1.essex.ac.uk/maths/people/fremlin/n16703.pdf), [[FremlinSIngularHomology.pdf:file]]$]$

On [[closed covers]] in Čech homology:

* [[Edwin E. Floyd]], *Closed coverings in Čech homology theory*, Trans. Amer. Math. Soc. **84** (1957) 319-337  &lbrack;[doi:10.1090/S0002-9947-1957-0087100-2](https://doi.org/10.1090/S0002-9947-1957-0087100-2), [pdf](http://www.ams.org/journals/tran/1957-084-02/S0002-9947-1957-0087100-2/S0002-9947-1957-0087100-2.pdf)&rbrack;

[[!redirects Cech homology]]
[[!redirects Čech homology]]


[[!redirects Čech homology theory]]
[[!redirects Cech homology]]