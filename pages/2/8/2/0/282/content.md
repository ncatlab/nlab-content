[[!redirects nonabelian algebraic topology]]

This entry is about the book

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]], _Nonabelian Algebraic Topology_ Tracts in Mathematics 16, European Mathematical Society ([web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html), [full pdf](http://www.bangor.ac.uk/%7Emas010/arbrsbookb-e0410.pdf))

which treats [[algebraic topology]] using tools of [[strict ∞-groupoid]]-theory: notably the traditional use of [[chain complex]]es of abelian groups is generalized to [[crossed complex]]es of [[groupoid]]s, and emphasis is put on the notion of [[fundamental groupoid]] and its strict [[higher category theory|higher categorical]] generalizations. 

One of the main motivations for the development of Nonabelian Algebraic Topology was the observation that the [[Seifert-van Kampen theorem]] is most naturally understood as being not about [[homotopy group]]s, but about the [[fundamental ∞-groupoid]] of a space and may be generalized to the [[higher homotopy van Kampen theorem]] this way.


#Contents#
* automatic table of contents goes here
{:toc}

## History

Some comments from [[Ronnie Brown]] himself:

> I hope it is helpful to relate my experiences from the 1960s and later with [[nonabelian cohomology]].

> In writing my book on [[topology]] in the 1960s, I got offended by having to make a detour to get the [[fundamental group]] of the circle, and then was attracted by [[Paul Olum]]'s paper referenced below. I extended Olum's work to a [[Mayer-Vietoris sequence|Mayer?Vietoris type sequence]] in the second paper below, 
and this enabled one to compute the fundamental group of, for example,  a [[wedge product|wedge]] of circles.

> (I use an MV sequence in _Topology and Groupoids_ in connection with pullbacks of [[covering space]]s.)

> So I decided to use this account for the book, thus giving students the advantage, it seemed,  of an introduction to [[cohomology|cohomological]] ideas.

> The problem was that the account when written in detail came to 30 pages (or maybe 40) and when looked at  in the cold light of day seemed incredibly boring (a full account is different from Olum's research account).

> I was at the time looking for exercises and came across [[Philip Higgins]]' paper on [[presentation]]s of groupoids, which used free products with amalgamation of groupoids. So I decided to give an exercise on the fundamental groupoid of a union. Then I felt I ought to write out a solution. When I had done this, it seemed streets ahead in exposition of all that [[nonabelian cohomology]] stuff  and moreover, when souped up to the _[[fundamental groupoid]] on a set of
base points_, gave results not reachable by the MV sequence; for example you could not with the MV sequence deduce the _precise calculation_ of the fundamental group of a union of two open sets whose intersection had say 150 path components. (This anomaly is also significant, in illustrating  the limitations of exact sequences.) 

> So I decided to switch to an exposition of groupoids in
1-dimensional [[homotopy theory]]  (also spurred by a meeting with [[George Mackey]] in 1967 where he told me of his work on ergodic groupoids, which is now seen as a preliminary to [[noncommutative geometry|Noncommutative Geometry]]).

> It occurred to me that if one could come to the groupoid idea from two distinct directions, then there was likely to be more in this than met the eye.

At the same time, an examination of the proof of the [[van Kampen theorem]] for groupoids, suggested that the theorem should have an extension to all dimensions, if one could define homotopy gadgets with the right properties. Another stimulus was the proof (used in the book) by [[Frank Adams]] (circulated in handwritten lecture notes) of the
[[cellular approximation theorem]], which had analogies to  parts of the van Kampen proof, but failed to get algebraic results because, apparently, of the lack of an appropriate algebraic gadget in dimension $n \gt 1$.

> It took 9 years to find such a gadget  in dimension $2$, and another 3 to get them in all dimensions, in work with Philip Higgins.

> It seemed to me  unfortunate that this work aroused the opposition, for reasons never explained to me, of Frank Adams,  who told people the whole programme was "ridiculous". His opinion became the opposite only when I told him (1985?) of the extension to the non simply connected case of the Blakers-Massey description of $\pi_3$ of a triad, using the nonabelian tensor product (work with [[Jean-Louis Loday]]). 

> The higher order van Kampen theorems, and the often nonabelian calculations which result,  have not been obtained by cohomological methods, but only by working directly  with structures appropriate to the geometry of higher homotopies, i.e. forms of strict [[n-fold category|multiple]]
groupoids. This confirms the comment of [[Philip Hall]], Philip Higgins' supervisor, that one should not try to force the geometry into a given algebraic mode, but search for the algebra which models the geometry. So it seems to me that algebraic topology has  been mainly restricted to, or not got out of,  the single base point and "group", not "groupoid", mode, nor appreciated the possibilities of
[[colimit]] type theorems in algebraic (and geometric?) topology -- no algebraic or geometric topology text (except mine!) mentions the higher order van Kampen work with Philip Higgins.

> You can also see this restriction in the contrast between the unsymmetrical, choice laden,  definition of the second relative homotopy group, with its compositions in one direction (recall the limitations of "Lineland" described in "Flatland") and the definition of the fundamental [[double groupoid]] of a pointed pair of spaces $\rho_2(X,A)$, with its compositions in $2$ directions. 
This contrast gets more significant in higher dimensions.

> For all these reasons, my inclination is to look for the
applications of the "appropriate" (whatever that is!) structures rather than cohomology with coefficients in such structures, where lots of detail is likely to get lost. Also, in making calculations it is convenient to work with strict algebraic structures, where the notion of colimit is more comprehensible. Even there, it has been a problem to make say colimit calculations with [[crossed module]]s into a symbolic computer algebra format. See the work by [[Chris Wensley]] listed below. 

> These results could not have been obtained without the intuitions on multiple compositions easily allowed by a cubical approach.

> One of the key observations for this programme was that one could define a strict homotopy double groupoid for a _pointed pair of spaces_, and that this was closely related to the well known fundamental crossed module of a pair of spaces, first considered by J.H.C. [[Whitehead]]. His paper listed below was a key source of ideas. 

> The natural extension of this observation is to construct a [[strict cubical omega-groupoid|strict cubical ∞-groupoid]] $\rho X_*$ of a _[[filtered space]]_ $X_*$, and find its relation to the quite classical homotopically defined fundamental crossed complex functor $\Pi: (filtered spaces) \to (crossed complexes)$. The proofs here are non trivial. By proving using $\rho$ a colimit theorem for $\Pi$ one can shortcut [[singular homology]], and obtain old and new results in algebraic topology, including some explicit calculations of homotopy groups, even  as modules over the fundamental group. This working with filtered space is not unreasonable since they abound. For example, classifying spaces often come with convenient filtrations, as do [[geometric realisation]]s of [[simplicial set|simplicial]] or [[cubical set|cubical]] sets. These ideas generalise of course to [[multifiltered space]]s or $n$-cubes of spaces. It is not so clear that one _must_ work with a kind of bare topological space, and so have little handle on which to construct invariants, except say by first taking a singular complex, or using multipaths. 

> The main idea of the [[higher homotopy van Kampen Theorem]]s is to model algebraically the gluing of homotopy types, or limited models of such. 

> An indication of a beginnings of a &#268;ech type approach to nonabelian cohomology using groupoids and crossed complexes is given in the new book, Chapter 12. This has not been developed in terms of [[sheaf theory]]. 

> Another big gap in comparison with traditional algebraic topology is [[intersection theory]] and [[Poincare duality]], although the (quite complicated) machinery of tensor products is available in the crossed complex context. 

> An obvious gap is also that of extending [[Grothendieck]]'s work on the fundamental group! 







## Contents

### I 1 and 2-dimensional results

* [[groupoid]]

* [[2-groupoid]]

* [[2-group]]

* [[crossed module]]

* [[fundamental groupoid]]

### Crossed complexes

#### 7 The basics of crossed complexes

* [[crossed complex]]

##### 7.1 Our basic categories and functors

###### 7.1.i The category of filtered topological spaces

###### 7.1.ii Modules over groupoids

A _[[module over a groupoid]]_ is a collection of [[abelian group]]s equipped with a linear  [[action]] by a [[groupoid]].

+-- {: .un_def}
###### Definition
**(module over a groupoid)**

Let $\mathcal{G} = (\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0)$ be a [[groupoid]]. A **module over the groupoid** $\mathcal{G}$ is a collection $\{N_x\}_{x \in \mathcal{G}_0}$ of [[abelian group]]s equipped with a collection of maps

$$
  N_x \times \mathcal{G}(x,y) \to N_y
$$

that are linear and respect the groupoid composition in the obvious way.


=--

###### 7.1.iii The category of crossed complexes

* [[crossed complex]]


###### 7.1.iv Homotopy and homology groups of crossed complexes


(...)

###### 7.1.v The fundamental crossed complex functor {#FundamentalCrossedComplex}


+-- {: .un_def}
###### Definition
**(fundamental crossed complex)**

Let $X_\bullet$ be a [[filtered space]]. 

Write $\Pi_1(X_1,X_0)$ for the subgroupo&#238;d of the [[fundamental groupoid]] $\Pi_1(X_1)$ of $X_1$ on objects that are in $X_0$.

The **fundamental crossed complex** $\Pi X_\bullet$ of $X$ is the [[crossed complex]]

with 

$$
  (\Pi X_\bullet)_1 = \Pi_1(X_1,X_0)
$$

and

$$
  (\Pi X_\bullet)_n
  :=
  \coprod_{x \in X_0}
  \pi_n(X_n, X_{n-1}, x)
  \;\;\;\;
  for n \geq 2
  \,,
$$

where $\pi_n(X_n, X_{n-1}, x)$ is the [[relative homotopy group]] obtained by equivalence classes of maps from the pointed $n$-disk into $X$ such that the disk lands in $X_n$, its boundary in $X_{n-1}$ and its basepoint on $x$.


=--



##### 7.4 Crossed complexes and chain complexes {#CrsdAndChainCplx}

+-- {: .un_def}
###### Definition
**(groupoid module chain complexes)**

Write $Chn$ for the [[category]] of [[chain complex]]es of modules over a [[groupoid]].  

=--

This is Def. 7.4.1.

+-- {: .un_def}
###### Definition
**(groupoid module chain complexes)**

Write $Crs$ for the [[category]] of [[crossed complex]]es.

=--

###### 7.4.i Adjoint module and augmentation module

+-- {: .un_def}
###### Definition

Given a [[module over a groupoid]] $(N,\mathcal{G})$, the **semidirect product groupoid** $\mathcal{G} \ltimes N$ has the same objects as $\mathcal{G}$ and morphisms

$$
  (\mathcal{G} \ltimes N)(p,q) = \mathcal{G}(p,q) \ltimes N(q)
$$

with composition given by the action of $\mathcal{G}$ on $N$.


=--

This is def. 7.4.5


+-- {: .un_def}
###### Definition

For $(t : N \to \mathcal{G}_0,\mathcal{G})$ a [[module over a groupoid]], write $P(N,\mathcal{G})$ for the groupoid $\mathcal{G}$ pulled back to the underlying set of $N$:

an object of $P(N,\mathcal{G})$ is an element in $N$ and a morphism $n_1 \to n_2$ is a morphism $\mathcal{G}(t(n_1),t(n_2))$.

=--

This is def. 7.4.9.



###### 7.4.iii The derived chain complex of a crossed complex


+-- {: .un_def}
###### Definition
**(chain complex from a crossed complex)**

Define a functor $\nabla : Crs \to Chn$ from [[crossed complex]]es to [[modules over groupoids]] as follows:

For $C$ a [[crossed complex]] we set for $n \geq 3$ 

$$
  (\nabla C)_n := C_n \;\;\;\; for n \geq 3
$$

and for $n \leq 2$ it is given by ...

=--

This is definition 7.4.20.


+-- {: .un_example}
###### Example
**(ordinary abelian chain complex as crossed complex)**


Let $C_\bullet$ be an ordinary [[chain complex]] of abelian groups, i.e. a chain complex of [[module over a groupoid|modules over the trivial groupoid]].

Then $(\Theta C)_1$ is the groupoid with objects $C_0$ and morphisms $\{x \stackrel{b}{\to} x + \partial b\}$. And for $n \geq 2$ we have that $(\Theta C)_2$ is $\coprod_{x \in C_0} C_n$.


=--


###### 7.4.v The right adjoint of the derived functor {#CrsFromCh}


+-- {: .un_def}
###### Definition
**(crossed complex from a chain complex)**

For $A$ a [[chain complex]] of [[modules over a groupoid]] $\mathcal{H}$, let $\Theta A \in Crs$ be the [[crossed complex]]

$$
  \Theta A := \kappa^* \Theta' A
  \,,
$$

where

$$
  \Theta' A :=
  \left[
    A_n 
      \stackrel{\partial_n}{\to}
    A_{n-1}
     \stackrel{}{\to}
     \cdots
     \stackrel{}{\to}
    A_{3}
    \stackrel{\partial_3}{\to}
    A_2
    \stackrel{(0,\partial_2)}{\to}
    \mathcal{H}\ltimes A_1
  \right]
$$

and where 

$$
  \kappa : P(A_0, \mathcal{H}) \to \mathcal{H} \ltimes A_0
$$

is the canonical covering morphism from above.

$$
  \array{
    \cdots \to & 
    (\Theta A)_3
    &\to&
    (\Theta A)_2
    &\to&
    (\Theta A)_1
    &\to&
    P(A_0, \mathcal{H})
    \\
    & \doiwnarrow && \downarrow && \downarrow && \downarrow
    \\
    \cdots \to & 
    A_3
    &\stackrel{\parital_3}{\to}&
    A_2
    &\stackrel{(0,\partial_2)}{\to}&
    \mathcal{H} \ltimes A_1
    &\stackrel{(1, \partial_1)}{\to}&
    \mathcal{H} \ltimes A_0    
  }
  \,.
$$


Here $\mathcal{H} \ltimes A_1$ acts on $A_n$ for $n \geq 2$ via the projection $\mathcal{H} \ltimes A_1 \to \mathcal{H}$, i.e. $A_1$ acts trivially.
(...)

=--

+-- {: .un_prop}
###### Proposition

These form a pair of [[adjoint functor]]s

$$
  (\nabla \dashv \Theta)
  : 
  Chn
  \stackrel{\overset{\nabla}{\leftarrow}}{\underset{\Theta}{\to}}
  Crs
$$

where...

=--

This is proposition 7.4.29.

(...)

#### 8 The Higher Homotopy van Kampen Theorem and its applications

* [[higher homotopy van Kampen theorem]]

#### 9 Tensor products and homotopies of crossed complexes

##### 9.9 The homotopy addition lemma for a simplex {#HomotopyAdditionSimplex}

For $\Delta^n$ the topological $n$-simplex regarded as a [[filtered space]] in the canonical way, the fundamental crossed complex $\Pi X^n$ is a groupoid-version of the $n$-[[oriental]]: the free [[strict ∞-groupoid]] on a single $n$-simplex.



##### 9.10 Simplicial sets and crossed complexes {#SimpSetAndCrs}

By the discussion at [The homotopy addition lemma for a simplex](#HomotopyAdditionSimplex) the [fundamental crossed complex](#FundamentalCrossedComplex) $\Pi \Delta^n$ plays the role of the free strict $n$-groupoid on the $n$-[[simplex]].

The [[cosimplicial object|cosimplicial]] $\infty$-groupoid

$$
  \Pi \Delta^\bullet : 
  \Delta \to Crs \simeq Str \infty Grpd
$$

induced by the discussion at [[nerve and realization]] a simplicial [[nerve]] operation on [[strict ∞-groupoid]] -- an [[∞-nerve]]:


+-- {: .un_def}
###### Definition
**(simplicial nerve)**

Let $C$ be a [[crossed complex]]. Its **simplicial [[nerve]]** $N^\Delta C \in  $ [[sSet]] is

$$
  (N^\Delta C)_n := Crs(\Pi \Delta^n, C)
$$

=--

This is definition 9.10.2.

+-- {: .un_prop}
###### Proposition
**(Dold-Kan map)**

For $D \in Chn$ a [[chain complex]] (of [[abelian groups]]), we may regard it as a [[crossed complex]] $\Theta D$ as described at [Crossed complex from chain complex](#CrsFromCh), hence as a [[strict ∞-groupoid]]. 

The [[∞-nerve]] $N^\Delta \Theta D \in $ [[sSet]] (described in [Crossed complexes and simplicial sets](#SimpSetAndCrs)) of this is the [[Kan complex]] underlying the image of $D$ under the [[Dold-Kan correspondence]] $Chn \to sAb$.

$$
  \begin{aligned}
    N^\Delta (\Theta D)  &= \simeq Crs(\Pi \Delta^\bullet, \Theta D)
    \\
    & \simeq Chn( \nabla \Pi \Delta^\bullet, D)
    \\
    & \simeq Chn( C_\bullet \Delta^\bullet , D) 
  \end{aligned}
  \,.
$$

Here $C_\bullet \Delta^n$ is the standard [[chain complex]] of chains on the simplicial $r$-[[simplex]] as discussed at [[cochain on a simplicial set|chains on a simplicial set]].

=--

This appears as _Remark 9.10.6_ together with its _footnote 116_ .


+-- {: .un_remark}
###### Remark

In the [[cosmic cube]] of [[higher category theory]] this realizes two edges

$$
  \array{
    ChainCplx &\stackrel{\Theta}{\hookrightarrow}&
    CrossedCplx
    &\stackrel{N^\Delta}{\hookrightarrow}&
    KanCplx
    \\
    \downarrow^{\mathrlap{\simeq}}
    &&
    \downarrow^{\mathrlap{\simeq}}
    &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    StrAb Str\infty Grpd
    &\hookrightarrow&
    Str \infty Grpd
    &\hookrightarrow&
    \infty Grpd
  }
$$

including [[strict ∞-groupoid]]s with strict abelian [[∞-group]]-structure -- modeled as [[chain complex]]es of [[abelian group]]s -- into [[strict ∞-groupoid]]s -- modeled as [[crossed complex]]es -- into all [[∞-groupoid]]s
-- modeled as [[Kan complex]]es. The composite is the map $Ch_\bullet \to sAb \to KanCplx$ to [[simplicial group]]s from the [[Dold-Kan correspondence]].

=-- 

#### 10 Resolutions

#### 11 The cubical classifying space of a crossed complex

#### 12 Nonabelian cohomology: spaces, groupoids

* [[nonabelian cohomology]]

### Cubical $\omgea$-groupoids



## References ##

For an extensive list of relevant publications see

* [[Ronnie Brown9], _publication list_ ([web](http://www.bangor.ac.uk/~mas010/publicfull.htm))

Some selected references are:

1. Olum, P., _Non-abelian cohomology and van Kampen's theorem_, Ann. Math. 68 (1958) 658--667.

1.  Brown, R., _On a method of P. Olum_, J. London Math. Soc. 40 (1965) 303--304.

1.  Brown, R.,  _Elements of Modern Topology_, McGraw Hill, Maidenhead, 1968.

1. Brown, R., _Topology and Groupoids_, Booksurge, 2006. 

1.  Higgins, P.J., _Presentations of groupoids, with applications to groups_, Proc. Camb. Phil. Soc., 60 (1964) 7--20.

1. Brown, R. and Higgins, P.J., _On the connection between the second relative homotopy groups of some related spaces_, Proc.   London Math.  Soc.(3) 36 (1978) 193--212.

1.Brown, R. and Higgins, P.J., _Colimit theorems for relative homotopy groups_, J. Pure Appl. Algebra 22 (1981) 11--41.

1. Whitehead, J.H.C., _Combinatorial Homotopy II_, Bull.
Amer. Math. Soc., 55 (1949), 453--496.


1. Brown, R. _Crossed complexes and homotopy groupoids as non commutative tools for higher dimensional local-to-global problems_, in Handbook of Algebra 6, Edited M. Hazewinkel, Elsevier, 2009. 

1. Wensley, C.D. and Alp, M., XMOD, a GAP share package for
computation with crossed modules, _GAP Manual_, (1997), 1355--1420.

1. Brown, R., Higgins, P.J., and Sivera, R., _Nonabelian Algebraic Topology: Filtered spaces, Crossed Complexes, Cubical Homotopy Groupoids_, EMS Tracts in Mathematics, Vol. 15, (Autumn 2010).   


[[!redirects Nonabelian algebraic topology]]
[[!redirects Nonabelian Algebraic Topology]]