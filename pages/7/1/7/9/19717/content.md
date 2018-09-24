
#Contents#
* table of contents
{:toc}

In [[computer science]], originally in database theory, **lenses** are used in situations where some structure is converted to a different form -- a *view* -- in such a way that changes made to the view can be reflected as updates to the original structure.

## Definition

Let $C$ be a [[category]] with [[finite products]]. A **lens** in C denoted $L =(S,V,g,p)$ has states $S$ and view states $V$ which are objects of $C$, and two arrows of C, a *Get* arrow $g:S \to V$ and a *Put* arrow $p:V \times S \to S$ satisfying the following equations:

1. (PutGet) the Get of a Put is the projection: $g p= \pi_0$.
1. (GetPut) the Put for a trivially updated state is trivial: $p \langle g, 1_S \rangle = 1_S$.
1. (PutPut) composing Puts does not depend on the first view update: $p(1_V \times p) = p \pi_{0,2}$.

##References

* Bohannon, A., Vaughan, J. and Pierce, B. (2006)  Relational Lenses: A language for updatable views. Proceedings of Principles of Database Systems (PODS) 2006


* Foster, J., Greenwald, M., Moore, J., Pierce, B. and Schmitt, A. (2007)  Combinators for bidirectional  tree  transformations:  A  linguistic  approach  to  the  view  update  problem. ACM Transactions on Programming Languages and Systems 29

* Michael Johnson, Robert Rosebrugh, and R. J. Wood.  Lenses, fibrations and universaltranslations.Math. Structures Comput. Sci., 22(1):25–42, 2012