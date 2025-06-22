
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

(...)

## Definition

\begin{definition}
  For [[normed vector spaces]] $\big(V, {\Vert-\Vert_V}\big)$ and $\big(V, {\Vert-\Vert_W}\big)$ the *operator norm* $\Vert A \Vert$ of a [[bounded linear operator]] $A \,\colon\, V \longrightarrow W$ is the [[supremum]] of the norms of $A$-images of unit-norm vectors $v \in V$: 
\[
  \label{SupremumFormula}
  {\Vert A \Vert}
  \;\coloneqq\;
  \underset{v \neq 0}{sup}
  \frac{
    {\Vert A(v) \Vert_W}
  }{
    {\Vert v \Vert_V}  
  }
  \;=\;
  \underset{ {\Vert v \Vert_V} \leq 1 }{sup}
  {\Vert A(v) \Vert_W}
  \,.
\]
\end{definition}
(cf. [Murphy 1990 Ex. 1.1.7](#Murphy90))

\begin{remark}
  If $V$ is not the [[zero object|zero]] vector space, then the supremum in (eq:SupremumFormula) may equivalently be taken over the unit sphere ${\Vert v \Vert_V} = 1$, instead of the whole unit ball ${\Vert v \Vert_V} \leq 1$, but the latter makes sense also for the degenerate case that $V = 0$ which has no unit vectors.
\end{remark}

## Related concepts

* [[norm topology]]

* [[operator algebra]]

* [[operator spectrum]]

## References

In monographs on [[operator algebra]]:

* {#Murphy90} [[Gerard Murphy]]: *$C^\ast$-algebras and Operator Theory*, Academic Press (1990) &lbrack;[doi:10.1016/C2009-0-22289-6](https://doi.org/10.1016/C2009-0-22289-6)&rbrack;

See also:

* Wikipedia, *[Operator norm](https://en.wikipedia.org/wiki/Operator_norm)*

[[!redirects operator norms]]