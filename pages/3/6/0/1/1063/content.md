#Definition#

A **pre-abelian category** is an [[additive category]] (an [[Ab]]-enriched category with finite biproducts) such that every morphism has a [[kernel]] and a [[cokernel]].  Equivalently, it is an additive category with all finite [[limit]]s and colimits, since an equalizer of $f$ and $g$ in a (pre-)additive category is the same as a kernel of $f-g$, and dually.

If $C$ is pre-abelian and $c\in C$, the operations $\ker$ and $\coker$ define a [[Galois connection]] between the [[preorder]]s $Sub(c)$ of monomorphisms into $c$ and $Quot(c)$ of epimorphisms out of $c$.  In particular, $f:b\to c$ is a kernel iff $f = ker(coker(f))$ and dually.  Furthermore, every morphism $f:A\to B$ in a pre-abelian category has a canonical decomposition
$$
A\stackrel{p}\to \coker(\ker f)\stackrel{\bar{f}}\to\ker(\coker f)\stackrel{i}\to B
$$
where $p$ is a cokernel, hence [[epimorphism|epic]], and $i$ is a kernel, and hence [[monomorphism|monic]].

#Remarks#

* The concept "pre-abelian category" is part of a sequence of concepts of [[additive and abelian categories]].