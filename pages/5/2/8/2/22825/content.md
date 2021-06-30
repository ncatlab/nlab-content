[[!redirects Huan&#39;s inertia orbifold]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of an [[inertia orbifold]] is closely related to that of a [[free loop space]]/[[free loop stack]] of an orbifold. As such, one may expect there to be an [[action]] of the [[circle group]] $S^1$ on inertia orbifolds, corresponding to "rotation of loops". An explicit component-based modification of the inertia orbifold construction which builds in an $S^1$-action of sorts (akin to [[cyclic loop spaces]]/[[cyclic loop stacks]]) was highlighted in [Huan 18](#Huan18) (Def. \ref{HuanInertiaOrbifold} below), following [Ganter 07, Def. 2.3](#Ganter07) (and, apparently, following suggestions by [[Charles Rezk]]).

The [[orbifold K-theory]] of these modified inertia orbifolds ("quasi-elliptic cohomology") is closely related to [[equivariant elliptic cohomology]] at the [[Tate curve]] of the original orbifold (see also at *[[Tate K-theory]]*).


## Definition

In the following

* $G$ is a [[discrete group]];

* $\mathcal{X} \;\simeq\; X \!\sslash\! G$ is a [[good orbifold]] which is a [[global quotient orbifold]] of a [[smooth manifold]] $X$ by a [[smooth function|smooth]] [[proper action]] of $G$.

\begin{definition}\label{HuanCentralizer}
For $g \in G$ any element, with $C_g \subset G$ denoting its [[centralizer]], write
$$
  \Lambda_g 
    \;\coloneqq\; 
  \big(
    C_g \times \mathbb{R}
  \big)
  \,
  \big/
  \,
    \underset{
      \simeq \mathbb{Z}
    }{
    \underbrace{
      \langle (g^{-1},1) \rangle
    }}
$$

for the [[Lie group]] which is the [[quotient group]] of the [[direct product group]] of $G$ with the additive Lie group of [[real numbers]] by the [[subgroup]] ([[isomorphism|isomorphic]] to the [[natural numbers]]) which is generated from the [[pair]] $(g,-1) \in G \times \mathbb{R}$.

Hence this sits in a [[short exact sequence]] of [[Lie groups]] of this form:

\[
  1
  \to
  \mathbb{Z}
  \xhookrightarrow{ \; 1 \mapsto (g^{-1},1) \; }
  C_g \times \mathbb{R}
  \overset{\;p_g\;}{\twoheadrightarrow}
  \Lambda_g
  \to
  1
  \,.
\]

\end{definition}

\begin{remark}
  For $g \in G$ the [[group action]] of $G$ on $X$ restricts to an action of the [[centralizer]] $G$ on the [[fixed locus]] $X^g = X^{\langle g\rangle}$:

$$
  C_g \times X^g \xrightarrow{ (-) \cdot (-) } X^g
  \,.
$$

Moreover, since $g$ itself (a) commutes with all element in $C_g$ and (b) has trivial action on $X^g$, this [[lift|lifts]] to an action of $\Lambda_g$ (Def. \ref{HuanCentralizer})

\[
  \label{ActionOfHuanCentralizer}
  \array{
    \Lambda_g \times X^g 
      &\xrightarrow{\;\;\;}& 
    X^g
    \\
    ( [h,r], x ) &\mapsto& h \cdot x
    \,.
  }   
\]

\end{remark}

The following definition modifies the [skeletal presentation of inertia orbifolds](inertia+orbifold#SkeletonForGlobalQuotientOrbifolds):

\begin{definition}\label{HuanInertiaOrbifold}
Write
  $$
    \Lambda_{S^1} \mathcal{X}
    \;\coloneqq\;
    \underset{[g] \in ConjCl(G)}{\coprod}
    X^g \!\sslash\! \Lambda_g
  $$
for the [[orbifold]] which is the [[disjoint union]] over the [[conjugacy classes]] $[g]$ of $G$ of the [[global quotient orbifolds]] of the [[fixed loci]] $X^g = X^{\langle g\rangle}$ by the [[group action]] (eq:ActionOfHuanCentralizer) of the group from Def. \ref{HuanCentralizer}.
\end{definition}

([Huan 18, Def. 2.14](#Huan18), review in [Dove 19, p. 62](#Dove19))

\begin{remark}\label{GanterOrbifold}
A similar definition is obtained by restricting [Ganter 07, Def. 2.3](#Ganter07) to constant loops and to $k = 1$, which yields
$$
  \simeq
  \underset{[g] \in ConjCl(G)}{\coprod}
  X^g \!\sslash\! (C_g/\langle g\rangle)
$$
\end{remark}


## Properties

### Relation to inertia orbifold

The canonical group homomorphism (via Def. \ref{HuanCentralizer})

$$
  \array{
    C_g 
      &\xhookrightarrow{\;\;}& 
    \Lambda_g
      &\xrightarrow{\;\;}&
    C_g/\langle g \rangle
    \\
    h 
      &\mapsto& 
    (h,0)
    \\
    &&
    [h,n]
    &\mapsto&
    [h]
  }
$$

induce canonical morphism from the plain [[inertia orbifold]] to Huan's (Def. \ref{HuanInertiaOrbifold}) and Ganter's orbifolds (Def. \ref{GanterOrbifold}):

$$
  \array{
    \Lambda\mathcal{X}
    &\xrightarrow{\;\;\;}&
    \Lambda_{S^1} \mathcal{X}
    &\xrightarrow{\;\;\;}&
    \cdots
    \,.
  }
$$


## Related concepts

* [[inertia orbifold]], [[free loop orbifold]]

* [[cyclic loop space]]

* [[cyclic loop stack]]

* [[Tate K-theory]]

* [[equivariant elliptic cohomology]]



## References

The notion is highlighted in:

* {#Huan18} [[Zhen Huan]], Def. 2.14 in: _Quasi-Elliptic Cohomology I_, Advances in Mathematics, Volume 337, 15 October 2018, Pages 107-138 ([arXiv:1805.06305](https://arxiv.org/abs/1805.06305), [doi:10.1016/j.aim.2018.08.007](https://doi.org/10.1016/j.aim.2018.08.007))

following

* [[Zhen Huan]], Exp. 2.1.14 in: _Quasi-elliptic cohomology_, 2017 ([hdl:2142/97268](http://hdl.handle.net/2142/97268))

followiong, in turn, a similar construction in:

* {#Ganter07} [[Nora Ganter]], Def. 2.3 in: *Stringy power operations in Tate K-theory* ([arXiv:math/0701565](https://arxiv.org/abs/math/0701565))

and motivated (as made explicit on [p. 63](https://arxiv.org/pdf/1912.02374.pdf#page=69) of [Dove 19](#Dove19)) by the "[rotation condition](Tate+K-theory#RotationCondition)" on [[Tate K-theory]], due to 

* {#Ganter13} [[Nora Ganter]], Def. 2.6 in: _Power operations in orbifold Tate K-theory_, Homology Homotopy Appl. Volume 15, Number 1 (2013), 313-342. ([arXiv:1301.2754](https://arxiv.org/abs/1301.2754), [euclid:hha/1383943680](https://projecteuclid.org/euclid.hha/1383943680))

following [Ganter 07, Def. 3.1](#Ganter07).


Streamlined review is in:

* {#Dove19} [[Thomas Dove]], p. 62 in: _Twisted Equivariant Tate K-Theory_ ([arXiv:1912.02374](https://arxiv.org/abs/1912.02374))

* [[Zhen Huan]], [[Matthew Spong]], Def. 2.1 in: *Twisted Quasi-elliptic cohomology and twisted equivariant elliptic cohomology* ([arXiv:2006.00554](https://arxiv.org/abs/2006.00554))


[[!redirects Huan's inertia orbifolds]]
