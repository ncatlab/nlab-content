## Idea

Steenrod Homology of a [[metric space|metric]] (or [[uniform space|uniform]], or [[Hausdorff space|Hausdorff]], or ...) space measures separations/holes by asking which _discrete_ or _approximate_ simplices can be filled-in to arbitrary fineness.

### Notation ###

The dimension-$p$ simplices of a simplicial complex $K$ will be noted $K_p$.  And, today, I feel like writing $A \ll X$ to say that $A$ is a compact subspace of $X$.

## The Definition

Given a metric space $(X,d)$, define the category $Reg (X,d)$, "of regular complexes", with objects pairs $(K,f)$ where

  * $ K $ is a locally-finite [simplicial complex]
  * $ f : K_0 \to X $ satisfies $ limsup_{e:K_1} d( \partial_0 e, \partial_1 e) = 0$ 

and with morphisms from $ (K,f)$ to $(L,g)$ being the inclusions of subcomplexes $ h : K \to L $ making $g$ an extension of $f$:
\[ Reg_d((K,f),(L,g)) = \{ h : hom(K,L) | f = g \circ h \} \]
Note that $Reg_d$ has finite pushouts.

The condition that $K$ be locally-finite means that arbitrary formal sums $\sum g_x x$ of $p$-simplices $x\in K_p$ have a well-defined boundary in the usual way:
\[ \partial \sum g_x x = \sum (-1)^j g_x \partial_j x \]
mentions a given simplex only finitely-many times.  Taking $g_x\in G$, for any abelian group $G$, this gives a functor $C_* : Reg(X,d) \to Ch $, valued in chain complexes.

**Definition** : *The Steenrod Homology $H_p(X,d)$ is the homology of the chain complex $\colim_{K,f} C_*$ in degree $p+1$.*

In pieces, this means that a Steenrod $p$-cycle may be represented by a 3ple $(K,f,\varphi)$ of a locally-finite complex $K$, a $K_1$-regular map $K_0 \to X$, and a formal sum $\varphi$ of simplices of dimension $p+1$ of $K$ with $\partial \varphi = 0$.  The group operations may as well be represented in terms of the chains $\varphi$ for a single $K$ and $f$.

### Historical note ###
what we have just called $H_p$, Steenrod himself notated $H^{p+1}$.  It was early days yet.

## Pairing with Alexander-Spanier Cohomology

A compactly-supported Alexander-Spanier Cocycle is a (compactly-supported) cochain $\chi : X^{p+1} \to G$ whose derivation $d \chi$ vanishes on tuples that are *small enough*.  For such a cochain, the sums 
\[ \varphi \frown \chi = \sum_{x :K_{p+1}} n_x (d\chi)(x) = \sum_x n_x \chi(\partial x)\]
are finite sums, and vanish for both coboundaries $\chi = d\omega$ and for boundaries $x = \partial y$ (because $d d = \partial \partial = 0$.  Thus the pairings descend to
\[ H_p( X,d ;\mathbb{Z}) \otimes H_c^p( X , G ) \to G \]
and all the reasonable variations you might consider.

## Continuities

### Colimits

Given a set $\{ X_i \}$ of metric spaces, their disjoint union can be given a metric in which separate summands are all distance $1$ from eachother.  This metric has 
$ Reg(\coprod X_i) = colim Reg(X_i) $ and therefore also 
\[ H_p(\coprod X_i) \simeq \bigoplus H_p( X_i ) \]

While $limsup d(\partial_0 x,\partial_1 x) = 0$ is a *topological* condition on *compact* metric spaces, it definitely is not so on noncompact spaces.  For this reason, one frequently considers the compactly-supported (compactly-generated?) homology as well,
\[ {}_c H_p(X) = \colim_{A \ll X } H_p(A) . \]

### Limits

Let $\dots \to X_{i+1} \to X_i \to \dots $ be a tower of *compact* metric spaces; in generous versions of Set-Theory, its limit again a compact metric space.  In contrast to $colim$, one can reasonably say $Reg(lim_i X_i) = lim_i Reg(X_i)$; and moreover, since the morphisms of $Reg(X_i)$ are *inclusions of subcomplexes*, it follows that
\[ \colim_{Reg(lim X)} C_* \simeq lim_i \colim_{Reg(X_i)} C_* \]
the usual Abstract Nonsense then gives short exact sequences
\[ 0 \to lim_i^1 H_{p+1}(X_i) \to H_p (lim X) \to lim_i H_p( X_i ) \to 0 \]

## References

N. E. Steenrod, Regular Cycles of Compact Metric Spaces,  Annals of Mathematics
Second Series, Vol. 41, No. 4 (Oct., 1940), pp. 833-851 [JSTOR](https://www.jstor.org/stable/1968863)