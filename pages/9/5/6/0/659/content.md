
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[crossed module]] is a bit like a [[normal subgroup]] ... without being a [[subgroup]]. In fact if a crossed module has a boundary map which is a monomorphism then it is isomorphic to the inclusion crossed module of a normal subgroup.

Crossed modules model all connected [[homotopy 2-type]]s.  _Crossed squares_ model all connected [[homotopy 3-type]]s and correspond to pairs of normal subgroups. Suppose $G$ is a group and $M$ and $N$ are normal subgroups of $G$; then of course, so is $M \cap N$.  Put these groups in a square, with the inclusion maps between them. Finally note that if $m \in M$ and $n \in N$, then $[m,n]$ is in the intersection $M \cap N$. This gives you a crossed square with $h$-map $h(m,n) = [m,n]$.  Removing the  condition that the inclusions are inclusions (!) gives the general form.

(The definition that follows is that given by Guin-Valery and Loday in their paper (see references).  Another definition can be given that is just the case $n = 2$ of that of [[crossed n-cube]], for which see that entry.
 

## Definition

A **crossed square** 

$$\array{& L & {\to}^\lambda & M & \\
         \lambda^\prime & \downarrow &&\downarrow & \mu\\
          &N & {\to}_{\nu}& P & \\
}$$

consists of four morphisms of groups $\lambda: L \to M$, $\lambda': L \to N$, $\mu: M \to P$, $\nu: N \to P$,  such that $\nu \lambda'= \mu \lambda$ together with [[action]]s of the group $P$ on $L, M, N$ on the left, conventionally, (and hence actions of $M$ on $L$ and $N$ via $\mu$ and of $N$ on $L$ and $M$ via $\mu$) and a function $h: M \times N \to L$. 

This structure
shall satisfy the following axioms:

1. the maps $\lambda, \lambda '$ preserve the actions of $P$; further, with the
given actions, the maps $\lambda, \lambda',\mu, \nu$ and $\kappa = \mu\lambda = \mu
'\lambda '$ are crossed modules;
1. $\lambda h(m,n)=m^n m^{-1},\lambda 'h(m,n)= {^m}n\,n^{-1}$
1. $h(\lambda l, n)= l^n l^{-1}, h(m,\lambda 'l)= {^m}l\, l^{-1}$
1. $ h(mm',n) = {^m}h(m',n) h(m,n), h(m,nn') = h(m,n) ^n h(m,n')$;
1. $h(^p m, {^p n})= {^p}h(m,n)$;

for all $l\in L, \,m, m'\in M,\, n,n'\in N$ and $p\in P$. 

The similarity of these axioms to [[commutator]] identities is no accident (see below).

This should be thought of as a _crossed module of crossed modules_ (in either direction!). For instance horizontally:
$$\array{& L & & M & \\
         \lambda^\prime & \downarrow &\to &\downarrow & \mu\\
          &N & & P & \\
}$$
The image of this morphism is a normal sub-crossed module of $(M,P,\mu)$, so we can form a quotient
$$\overline{\mu} : M/\lambda L \to P/\nu N,$$
and this is a crossed module, as is the kernal crossed module of this (horizontal) morphism.


## Examples
 
### Homotopical example

The classical homotopical example $\Pi(X;A,B)$ is determined by a pointed [[triad]] $(X; A,B)$ where $A,B \subseteq X$, and $P = \pi_1(A \cap B)$, $M = \pi_2(A, A \cap B), N = \pi_2(B, A \cap B)$ and $L=\pi_3(X; A,B)$. The operations of $P$ are the standard ones and  $h$ is the generalised [[Whitehead product]]. (The conventions may be slightly different from the standard ones in homotopy theory.)  This can be generalised to a functor $\Pi$ from squares of pointed spaces to crossed squares.

Ellis uses this construction in 

* G.J. Ellis, Crossed squares and combinatorial homotopy, Math. Z., 461 (1993) 93&#8211;110,

where the fact that that the crossed square associated to a triad is defined directly in terms of certain homotopy classes is important. 

The fact that there is a [[van Kampen theorem|van Kampen type theorem]] for $\Pi$ implies that one calculates some nonabelian groups. It also implies that one is calculating some (pointed) homotopy 3-types. 

### Algebraic example

The example hinted at above has $P$ a group, $M$ and $N$ normal subgroups, and $L = M \cap N$,

$$\array{& M\cap N & {\to}^\lambda & M & \\
         \lambda^\prime & \downarrow &&\downarrow & \mu\\
          &N & {\to}_{\nu}& P & \\
}$$

with all maps the evident inclusions, all actions by conjugation, and $h : M \times N \to M\cap N$ given by $h(m,n) = [m,n]$.

### Simplicial group example

If we replace each group in the algebraic example by a simplicial group, we would have a simplicial crossed square, now apply the connected component functor to that and you get a crossed square, and in fact any crossed square can be constructed up to isomorphism in this way.

If we start with a simplicial group, $G$, using the [[decalage]] functor we can construct a simplicial group and two normal subgroups and thus get to the previous situation. The result can be interpreted in terms of the [[Moore complex]] as follows:
$$\array{& \frac{NG_2}{d_0(NG_3)}& {\to} & Ker d_1 & \\
          & \downarrow &&\downarrow & \\
          &Ker d_2 & {\to}& G_1 & \\
}$$

The two morphisms with codomain $G_1$ are inclusions, the other two are induced by $d_0$. The $h$-map can be explicitly given. It can be found in 

T. Porter, _n-types of simplicial groups and crossed n-cubes_, Topology, 32, (1993), 5 &#8211; 24,

which also contains the discussion of the generalisation to [[crossed n-cube|crossed n-cubes]]


## Properties

### Relation to $cat^2$-groups

A crossed module $\mu: M \to P$ determines a $cat^1$-structure on the [[semidirect product]] group $M \rtimes P$. Thus to say that the above crossed square is a _crossed module of crossed modules_ suggests that we should ask for $L \rtimes N \to M \rtimes P$ to be a crossed module, so that there is an action which allows the _big group_ $G = (L \rtimes N) \rtimes (M \rtimes P)$ to be a $cat^1$-group. Then $G$ becomes a _$cat^2$-[[cat-2-group|group]]_. The $h$-map of the crossed square derives from a commutator in $G$.

This equivalence between crossed squares and $cat^2$-groups confirms the completeness of the axioms for crossed squares. Notice also that to prove a diagram of crossed squares is a [[colimit]] diagram, it looks as if you have to make appallingly detailed verifications of axioms. It is much easier to prove the corresponding diagram of $cat^2$-groups is a colimit!

This theme of using two equivalent categories, one for conjecture and proof, the other for calculation and application to traditional invariants, runs through the story of [[higher homotopy van Kampen theorems]].


## Related concepts

* [[crossed module]], [[differential crossed module]]

* [[2-crossed module]] / **crossed square**, [[differential 2-crossed module]]

* [[crossed complex]]

* [[hypercrossed complex]]



[[!redirects crossed squares]]