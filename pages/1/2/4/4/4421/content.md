
<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _Chern-Simons form_ $CS(A)$ is a [[differential form]] naturally associated to a differential form $A \in \Omega^1(P,\mathfrak{g})$ with values in a [[Lie algebra]] $\mathfrak{g}$: it is the form trivializing a [[curvature characteristic form]] $\langle F_A \wedge \cdots \wedge F_A \rangle$ of $A$, for $\langle \cdots \rangle$ an [[invariant polynomial]]: 

$$
  d_{dR} CS(A) = \langle F_A \wedge \cdots \wedge F_A \rangle
  \,.
$$

More generally, for $A,A' \in \Omega^1(P, \mathfrak{g})$ two $\mathfrak{g}$-valued 1-forms and for $\hat A \in \Omega^1(P \times [0,1],\mathfrak{g})$ a "path of connections", the Chern-Simons form relative to $A$ and $A'$ is a form that trivializes the _difference_ between the two curvature characteristic forms

$$
  d_{dR}CS(A,A') = \langle (F_A)^k \rangle - \langle (F_{A'})^k \rangle
  \,.
$$

Chern-Simons forms are of interest notably when the differential forms $A,A'$ are (local representatives of) [[connection on a bundle|connections]] on a $G$-[[principal bundle]] $P \to X$, for instance if $A \in \Omega^1(P,\mathfrak{g})$ is an [[Ehresmann connection]] 1-form.

Often the term _Chern-Simons form_ is taken to refer to the case where $\mathfrak{g}$ is a [[semisimple Lie algebra]] with binary [[invariant polynomial]] $\langle -, -\rangle$ (e.g. the [[Killing form]]) in which case $CS(A)$ is the 3-form

$$
  \langle A \wedge d_{dR} A\rangle
  + 
  c
  \langle
    A \wedge [A \wedge A]
  \rangle
  \,.
$$

 Even more specifically, often the term is understood to refer to the case where $\mathfrak{g} \subset \mathfrak{gl}(n)$ is a [[matrix Lie algebra]], for instance $\mathfrak{o}(n)$ (for the [[orthogonal group]]) or notably $\mathfrak{u}(n)$ (for the [[unitary group]]). In that case the invariant polynomials may be taken to be given by matrix [[trace]]s: $\langle \cdots \rangle = tr(\cdots )$.

## Details

(...)


## As secondary characteristic forms

If the differential form $A \in \Omega^1(P,\mathfrak{g})$ is _flat_ in that $F_A = 0$ the curvature invariant $\langle F_A \wedge \cdots \wedge F_A\rangle$ is uninteresting, but now the the Chern-Simons form is closed and hence now it represents a class in [[de Rham cohomology]] encoded by $A$. This is often called a _secondary curvature invariant_ .

...


### Chern-Simons theory

In particular on a 3-dimensionak [[smooth manifold]] $X$ necessarily the Chern-Simons 3-form is closed. The [[functional]]

$$
  (A \in \Omega^1(X,\mathfrak{g}))
  \mapsto
  \int_X CS(A)
$$

is the [[action functional]] of the [[quantum field theory]] called [[Chern-Simons theory]].

More generally, for $X$ a $(2n-1)$-dimensional [[smooth manifold]] and $\langle -,\cdots, -\rangle$ an invariant polynomial of arity $n$, the analous formula defines the [[action functional]] of  $(2n+1)$-dimensional Chern-Simons theory.

## References

The article introducing  the concept is 

* [[Shiing-Shen Chern]], [[James Simons]], _Characteristic forms and geometric invariant_  The Annals of Mathematics, Second Series, Vol. 99, No. 1 (Jan., 1974), pp. 48-69  ([jstor](http://www.jstor.org/pss/1971013))

As it says in the introduction of this article, it was motivated by an attempt to find a combinatorial formula for the [[Pontrjagin class]] of a [[Riemannian manifold]] (i.e. that associated to the [[orthogonal group|O(n)]]-[[principal bundle]] to which the [[tangent bundle]] is associated) and the Chern-Simons form appeared as a boundary term that obstructed to original attempt to derive the Pontrrjagin class by integrating curvature classes simplex-by-simplex. But 
A combinatorial formula of the kind these authors were looking for was however (nevertheless) given later in

* [[Jean-Luc Brylinski]], [[Dennis McLaughlin]] _&#268;ech cocycles for characteristic classes_ , Comm. Math. Phys.  178  (1996) ([pdf](http://www.springerlink.com/content/762g1m76jp6425x5/))

