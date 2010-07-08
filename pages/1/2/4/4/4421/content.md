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
  \,,
$$

where $F_A \in \Omega^2(X,\mathfrak{g})$ is the [[curvature]] 2-form of $A$.

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

If the differential form $A \in \Omega^1(P,\mathfrak{g})$ is _flat_ in that $F_A = 0$ the curvature invariant $\langle F_A \wedge \cdots \wedge F_A\rangle$ is uninteresting, but now the Chern-Simons form is closed and hence now it represents a class in [[de Rham cohomology]] encoded by $A$. This is often called a _secondary curvature invariant_ .

...


### Chern-Simons theory

In particular on a 3-dimensional [[smooth manifold]] $X$ necessarily the Chern-Simons 3-form is closed. The [[functional]]

$$
  (A \in \Omega^1(X,\mathfrak{g}))
  \mapsto
  \int_X CS(A)
$$

is the [[action functional]] of the [[quantum field theory]] called [[Chern-Simons theory]].

More generally, for $X$ a $(2n-1)$-dimensional [[smooth manifold]] and $\langle -,\cdots, -\rangle$ an invariant polynomial of arity $n$, the analous formula defines the [[action functional]] of  $(2n+1)$-dimensional Chern-Simons theory.

## In terms of $\infty$-Lie algebroids

As discussed at [[invariant polynomial]], Chern-Simons elements int the [[Weil algebra]] $W(\mathfrak{g})$ of a [[Lie algebra]] $\mathfrak{g}$ induce the transgression between invariant polynomials and cocycles in [[Lie algebra cohomology]].

For 

$$
  \array{
    T_{vert} P &\stackrel{A_{vert}}{\to}& \mathfrak{g}
    \\
    \downarrow && \downarrow
    \\
    T P &\stackrel{(A,F_A)}{\to}& inn(\mathfrak{g})
    \\
    \downarrow && \downarrow
    \\
    T X &\stackrel{(P_i(F_A))}{\to}& \prod_i b^{n_i} \mathfrak{u}(1)
  }
$$

the data of an [[Ehresmann connection]] on a $G$-[[principal bundle]] expressed as a diagram of [[∞-Lie algebroid]]s with the [[curvature characteristic form]]s on the bottom, a choice of transgression element $cs_P$ for an [[invariant polynomial]] $P$ in transgression with a Lie algebra cocycle $\mu$ induces a diagram

$$
  \array{
    \mathfrak{g} &\stackrel{\mu}{\to}& b^n \mathfrak{u}(1)
    \\
    \downarrow && \downarrow
    \\
    inn(\mathfrak{g}) &\stackrel{(cs_P,P)}{\to}& e b^{n} \mathfrak{u}(1)
    \\
    \downarrow && \downarrow
    \\
    \prod_i b^{n_i}\mathfrak{u}(1) &\stackrel{p_i}{\to}& b^{n+1} \mathfrak{u}(1)
  }
  \,.
$$

The [[pasting]] of this to the above [[Ehresmann connection]] expresses in the middle horizontal morphism the Chern-Simons form $cs_P(A)$ and its [[curvature characteristic form]] $P(F_A)$

$$
  \array{
    T_{vert} P &\stackrel{A_{vert}}{\to}& \mathfrak{g} &\stackrel{\mu}{\to}& 
    b^n \mathfrak{u}(1)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    T P &\stackrel{A}{\to}& inn(\mathfrak{g})
    &\stackrel{(cs_P,P)}{\to}&
    e b^n \mathfrak{u}(1)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    T X &\stackrel{(P_i)}{\to}& \prod_i b^{n_i} \mathfrak{u}(1)
    &\stackrel{p_i}{\to}&
    b^{n+1} \mathfrak{u}(1)
  }
  \,.
$$



## References

The article introducing  the concept is 

* [[Shiing-Shen Chern]], [[James Simons]], _Characteristic forms and geometric invariants_  The Annals of Mathematics, Second Series, Vol. 99, No. 1 (Jan., 1974), pp. 48-69  ([jstor](http://www.jstor.org/pss/1971013)) ([pdf](http://www.dpmms.cam.ac.uk/~hk244/chern-simons.cp.pdf))

As it says in the introduction of this article, it was motivated by an attempt to find a combinatorial formula for the [[Pontrjagin class]] of a [[Riemannian manifold]] (i.e. that associated to the [[orthogonal group|O(n)]]-[[principal bundle]] to which the [[tangent bundle]] is associated) and the Chern-Simons form appeared as a boundary term that obstructed to original attempt to derive the Pontrrjagin class by integrating curvature classes simplex-by-simplex. But 
A combinatorial formula of the kind these authors were looking for was however (nevertheless) given later in

* [[Jean-Luc Brylinski]], [[Dennis McLaughlin]] _&#268;ech cocycles for characteristic classes_ , Comm. Math. Phys.  178  (1996) ([pdf](http://www.springerlink.com/content/762g1m76jp6425x5/))

The [[L-∞-algebra]]-formulation is discussed in [SSS08](http://arxiv.org/abs/0801.3480).

[[!redirects Chern-Simons forms]]