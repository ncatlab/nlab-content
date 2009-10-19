<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The notion of _principal $\infty$-bundle_ is a [[vertical categorification|categorification]] of [[principal bundle]] from [[groups]] and [[groupoids]] to [[∞-groupoids]], or rather from parameterized groupoids (generalized spaces called [[stacks]]) to parameterized $\infty$-groupoids (generalized spaces called [[∞-stacks]]).



For motivation, background and further details see 

* [[motivation for sheaves, cohomology and higher stacks]]
* [[principal bundle]]
* [[gerbe]]
* [[principal 2-bundle]].

#Definition in general $(\infty,1)$-topos #

We define $G$-principal $\infty$-bundles in the general context of an [[∞-stack]] [[(∞,1)-topos]] $\mathbf{H}$, with $G$ a [[groupoid object in an (∞,1)-category|group object in the (∞,1)-topos]].

Recall that for $A \in \mathbf{H}$ an object equipped with a point $pt_A : {*} \to A $, its corresponding [[loop space object]] $\Omega A$ is the [[homotopy pullback]]

$$
  \array{
    \Omega A &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& A
  }
  \,.
$$

Conversely, for $G \in \mathbf{H}$ we say an object $\mathbf{B}G$ is a [[delooping]] of $\mathbf{H}$ if it has an essentially unique point and if $G \simeq \Omega \mathbf{B}G$. We call $G$ an **$\infty$-group**. More in detail, its structure as a [[groupoid object in an (∞,1)-category|group object in an (∞,1)-category]] is exhibited by the [[Cech nerve]] 

$$
 \left(
 \array{
   &\cdots&
   {*} \times_{\mathbf{B}G} {*} 
   \times_{\mathbf{B}G} {*}
   &\stackrel{\to}{\stackrel{\to}{\to}}&
   {*} \times_{\mathbf{B}G} {*} 
   &\stackrel{\to}{\to}& 
   {*} 
 }
 \right)
 \simeq
 \left(
  \array{
   &\cdots&
   G \times G
   &\stackrel{\to}{\stackrel{\to}{\to}}&
   G 
   &\stackrel{\to}{\to}&
   {*} 
  }
 \right)
$$

of ${*} \to \mathbf{B}G$.

## $G$-principal $\infty$-bundles ##

By the general reasoning discussed at [[cohomology]], a cocycle for nonabelian $G$-cohomology on $X \in \mathbf{H}$ is just a morphism $g : X \to \mathbf{B}G$ in $\mathbf{H}$. 

To this is canonically associated its [[homotopy fiber]]

$$
  \array{
    P &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{B}G
    \,.
  }
$$

and we claim that $P \to X$ canonically extends to the structure of a [[groupoid object in an (∞,1)-category|groupoid object in an (∞,1)-topos]] 
that exhibits the action of $G$ on $P$ in that it is a groupoid object _over_ $G$: it fits naturally into a diagram

$$
  \array{
    \vdots && \vdots && \vdots
    \\
    P \times_X P \times_X P 
    &\stackrel{\simeq}{\to}& P \times G \times G
    &\to& G \times G
    \\
    \downarrow\downarrow\downarrow
    && 
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times_X P &\stackrel{\simeq}{\to}& P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow
    && \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{=}{\to}& P &\stackrel{}{\to}& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\stackrel{=}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

+-- {: .un_prop }
###### Proposition

Here the horizontal morphisms on the left are indeed equivalences, as indicated.

=--

+-- {: .proof}
###### Proof

The definition homotopy pullback square for $P \times_X P$ is

$$
  \array{
    P \times_X P &\to& P
    \\
    \downarrow && \downarrow
    \\
    P &\to& X
  }
$$

To compute this, we may attach the defining homotopy pullback square of $P$ to obtain

$$
  \array{
    P \times_X P &\to& P &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P &\to& X &\to& \mathbf{B}G
    \,.
  }
$$

Since homotopy pullback squares paste to homotopy pullback squares, this says that $P \times_X P$ is the homotopy limit 

$$
  \array{
    P \times_X P &\to& &\to& {*}
    \\
    \downarrow && && \downarrow
    \\
    P &\to& X &\to& \mathbf{B}G
    \,.
  }
$$

But again by the defnition of $P$, the lower horizontal morphism is homotopic to $P \to {*} \to \mathbf{B}G$, so that $P \times_X P$ is also (equivalent to) the homotopy pullback

$$
  \array{
    P \times_X P &\to& &\to& {*}
    \\
    \downarrow && && \downarrow
    \\
    P &\to& {*} &\to& \mathbf{B}G
    \,.
  }
$$

This finally may be computed in turn as the pasting of two homotopy pullbacks

$$
  \array{
    P \times_X P\simeq P \times G &\to& G &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P &\to& {*} &\to& \mathbf{B}G
    \,.
  }
$$

of which the one on the right is the defining one of $G$ and the remaining one on the left is just a [[product]].

=--


+-- {: .un_remark}
###### Remark
**(terminology)**

For ordinary [[principal bundle]]s the following terminology is standard:

* the morphism $P \times_X P \stackrel{}{\to} P \times G$ is the **division map**;

* the fact that the division map is an equivalence is the **principality condition** on the action;

* the image $\rho : P \times G \to P$ of the projection to the second factor $p_2 : P \times_X P \to P$ under this equaivelence is the **action** of $G$ on $P$.

=--

The above shows how every cocycle $X \to \mathbf{B}G$ induces a map $P \to X$ equipped with a $G$-action. Conversely, we may _define_ a $G$-action on an object $V$ to be a [[groupoid object in an (∞,1)-category|groupoid object in an (∞,1)-topos]] sitting over $G$.


+-- {: .un_defn}
###### Definition
**($G$-action)**

Let $G$ be a [[groupoid object in an (∞,1)-category|group object in the (∞,1)-topos]] $\mathbf{H}$. An [[action]] of $G$ on another object $V \in \mathbf{H}$ is a [[groupoid object in an (∞,1)-category|group object in the (∞,1)-topos]] $V//G \to G$ _over $G$_ in that we have a morphism of simplicial diagrams

$$
  \array{
    \vdots && \vdots
    \\
    V \times G \times G
    &\to& G \times G
    \\
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    V \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{}{\to}& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$


such that the corresponding diagram of [[effective epimorphism]]s

$$
   \array{
      & V &\to& {*}
      \\
      & \downarrow && \downarrow
      \\
      V//G := & \lim_\to V\times G^{\times n} &\to&
      \mathbf{B}G
   }
$$

(recalling that by the axioms of [[(∞,1)-topos]] every groupoid object _is effective_) is a [[homotopy pullback]].

We call the object $V//G$ with this structure of a
[[groupoid object in an (∞,1)-category|group object in the (∞,1)-topos]] the [[action groupoid]] of $G$ acting on $V$.

=--


 
## Morphisms of $G$-principal $\infty$-bundles ##

The morphisms of $G$-principal $\infty$-bundles are to be such that they respect the G$-action, so that the [[∞-groupoid]] $G Bund(X)$ of $G$-principal $\infty$-bundles on $X$ is naturally equivalent to the cocycle $\infty$-groupoid $Hom_C(X, \mathbf{B} G)$

$$
  G Bund(X) \simeq Hom_C(X, \mathbf{B} G)
  \,.
$$

Then this says that $G$-principal bundles are classified by $G$-[[cohomology]]

$$
  G Bund(X)/_\simeq = H(X,\mathbf{B}G) := Ho_C(X, \mathbf{B}G)
$$

given by the [[hom-set]] in the [[homotopy category of an (infinity,1)-category|homotopy category of the (∞,1)-category]] $C$.

## Connections on $G$-principal $\infty$-bundles ##

By refining the classifying [[nonabelian cohomology|cocycles]] $g : X \to \mathbf{B} G$ to cocycles 
$\Pi(X) \to \mathbf{B} G$
on higher [[path groupoids]] of $X$, one obtains higher versions of the notion of [[connection on a bundle]]. This is described in more detail at [[schreiber:Differential Nonabelian Cohomology|Differential Nonabelian Cohomology]].

# Concrete realizations #

We discuss realizations of the general idea in various
[[(∞,1)-toposes]].

## In topological spaces  ##

The following general construction was originally due to
Quillen and defines principal _groupoid_ $\infty$-bundles in the [[(∞,1)-topos]] [[Top]] 
in its [[presentable (infinity,1)-category|presentation]]
by the [[model structure on simplicial sets]].

Let $C$ be a small [[category]] and let 

$$
  \rho_P : C \to SSet
$$

be a functor with values in [[SSet]] such that
it sends all morphisms in $C$ to weak equivalences in
[[SSet]] ([[simplicial homotopy group|weak homotopy equivalences]] of simplicial sets).

Consider first the case that $C$ has a single object, so that it is the [[delooping]] $\mathbf{B}G$ of a [[monoid]]
or [[group]] $G$. Then

Let 

$$
  P := \rho_P(\bullet)
$$ 

be the simplicial set assigned to this single object and let 

$$
  X := P//G := hocolim \rho_P
$$ 

be the corresponding [[action groupoid]] (see there for the description as a weak colimit). 

Notice that, as every [[action group]], this comes with 
a canonical map $P//G \to \mathbf{B}G$.

+-- {: .un_theorem }
###### Theorem

Given the above, the diagram

$$
  \array{  
     P &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

is a homotopy pullback 
(i.e. defines a [[fibration sequence]]).

=--

+-- {: .proof}
###### Proof

This is originally due to

* D. Quillen, _Higher algebraic K-theory I_,
Springer Lecture notes in Math. 341 (1973)
85--147.

The statement is reproduced in section IV of

* P. G. Goerss and J. F. Jardine, 1999, _Simplicial Homotopy Theory_, number 174 in Progress in Mathematics, Birkhauser. ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

=--

+-- {: .un_remark}
######Remark

For the simple case that 
$G$ is [[group]],
in which case $\rho_C$ necessarily takes values not
just inweak equivalences but is isomorphisms of 
simplicial sets, this says that
$P \to X$ is a  $G$-principal $\infty$-bundle.
In particular the _principality_
of the action is manifestly exhibited by the fact that
the base space $X$ is the (weak) quotient of $P$ by the
action of $G$.

The above reproduces manifest the description of ordinary 
$G$-principal topological bundles in the incarnation 
as groupoids as described in detail at
[[generalized universal bundle]].

More generally, when $G$ is just a [[monoid]]
the above descibes something a bit more general than
an ordinary $G$-[[principal bundle]] 
(as then the action of $G$ on the total space may
be by weak equivalences that are not isomorphisms).
=--

Quillen's original construction is more general than
this, concerning in fact 1-[[groupoid]]-principal
$\infty$-bundles:

+-- {: .un_theorem }
###### Theorem 

Let now $C$ be a [[category]] and for 

$$
  \rho_P : C \to SSet
$$

a functor that sends all morphisms to weak
equivalences of simplicial sets.

+--{: .query}
[[David Roberts]]: Do you mean ordinary functor or something weaker? Unless you have something weaker, then all those weak equivalences are actually isomorphisms. Also cf [[simplicial localization]].

[[Urs Schreiber|Urs]]: right, $C$ is allowed to be a _category_, not required to be a groupoid. I have corrected that now. See the beginning of [Jardine's article](http://www.math.uiuc.edu/K-theory/0723/diagrams3.pdf).

=--

Let now for each object $c \in C$

$$
  P_c := \rho_C(c)
$$

be the "bundle of $c$-fibers".

Then for each $c$ the diagram

$$
  \array{  
     P_c &\to& {*}
     \\
     \downarrow && \downarrow^{{*} \mapsto c}
     \\
     X &\stackrel{g}{\to}& C
  }
$$

is a homotopy pullback 
(i.e. defines a [[fibration sequence]]).


=--

This classical construction is recalled in the introduction of

* Jardine, _Diagrams and torsors_ ([pdf](http://www.math.uiuc.edu/K-theory/0723/diagrams3.pdf))



## In simplicial presheaves ##

For a small [[site]] $C$, let $\mathbf{H}$
be the [[(∞,1)-topos]]  of [[∞-stacks]]
on $C$, in its [[presentable (infinity,1)-category|presentation]] by the
[[model structure on simplicial presheaves]].

In 

* Jardine, _Diagrams and torsors_ ([pdf](http://www.math.uiuc.edu/K-theory/0723/diagrams3.pdf))

the discussion of $\infty$-principal bundles
is discussed in this context.

Notice however that this means placing oneself 
always in the [[petit topos]] of sheaves on $C$, 
which will describe always $\infty$-bundles over $C$.
So if $C = Op(X)$ is the [[category of open subsets]]
of some [[topological space]] $X$, then this is 
$\infty$-bundles over $X$.

Notably in this [[(∞,1)-topos]] $(\infty,1)Sh(X)$
the [[terminal object]]  is not the expected abstract
point, but rather the space $X$ itself. 

As a consequence, the above simple picture of a
principal $\infty$-bundle being just the homotopy
pullback of the point is no longer directly available.
To circumvent this Jardine introduces the notion of 
_diagrams_ (not meant in the simple conventional sense).

...

Alternatively, one can consider simplicial presheaves
on a [[gros topos]], say on some version of the [[site]] of
[[Diff]] of [[manifolds]] as discussed for instance in some detail in

* Daniel Dugger, _Sheaves and homotop theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf)).

That gives a notion of _smooth_ $\infty$-bundles.
And in that case the the desrption of principal 
$\infty$-bundles as homotopy pullbacks of the point continues to be valid.

In low degree this is then, more or less explicitly, the description of higher principal bundles
by Bartels, Bakovi&cacute;, Wockel, etc., as referenced at [[principal 2-bundle]].

#References#

The notion of principal $\infty$-bundle (often addressed in the relevant literature in the language of [[torsors]]) appears in the context of the [[simplicial presheaf]] [[model structure on simplicial presheaves|model]] for generalized spaces in

* Jardine, Luo, _Higher order principal bundles_ ([pdf](http://www.math.uiuc.edu/K-theory/0681/cocycles6.pdf)).

* Jardine, _Cocycle categories_ ([pdf](http://arxiv.org/abs/math.AT/0605198)).

An earlier description in terms of simplicial objects is

* P. Glenn, _Realization of cohomology classes in arbitrary exact categories_, J. Pure Appl. Algebra 25, 1982, no. 1, 33--105.

In article not the total space of the bundle $P \to X$ is axiomatized, but the $\infty$-[[action groupoid]] of the action of $G$ on it.

See the remarks at [[principal 2-bundle]].

[[Note on Formatting|?]]

[[!redirects principal infinity-bundles]]
[[!redirects principal ∞-bundle]]
[[!redirects principal ∞-bundles]]