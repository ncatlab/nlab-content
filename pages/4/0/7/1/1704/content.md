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

#Definition#

Let $\mathbf{H}$ be an [[(∞,1)-topos]], i.e. an [[(∞,1)-category of (∞,1)-sheaves]] whose objects behave as used to from [[topological spaces]], but are actually _parameterized_ topological spaces (for instance [[generalized smooth space|smooth]] spaces), namely [[∞-stacks]].

Let $\mathbf{B} G$ be a one-object $\infty$-groupoid in $\mathbf{H}$, defining an $\infty$-group $G$. 

Then for $X$ any object in $\mathbf{H}$, a $G$-principal $\infty$-bundle $P \to X$ is a [[fibration sequence|homotopy fiber]] of a morphism  $X \to \mathbf{B} G$

$$
  \array{
    P &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B} G
  }
$$

for some classifying morphism $g : X \to \mathbf{B} G$.

Notice that $g$ is a cocycle in the [[nonabelian cohomology|nonabelian]] [[cohomology]] on $X$ with coefficients in $G$.

Also notice that every such object naturally comes equipped with a coherent [[action]] of $G$ obtained by further pulling back $P \to X$ along the [[simplicial object]] in $\mathbf{H}$ given by the [[homotopy pullback|homotopy fiber product]] of ${*} \to \mathbf{B}G$ along itself -- the [[groupoid object in an (∞,1)-category]] given by the [[Cech nerve]] of ${*} \to \mathbf{B}G$ --

$$
 \array{
   &\cdots&
   {*} \times_{\mathbf{B}G} {*} 
   \times_{\mathbf{B}G} {*}
   &\stackrel{\to}{\stackrel{\to}{\to}}&
   {*} \times_{\mathbf{B}G} {*} 
   &\stackrel{\to}{\to}& 
   {*} 
   &\to& 
   \mathbf{B}G
 }
$$

which by the discussion at [[fibration sequence]] is

$$
 \array{
  &\cdots&
  G \times G
  &\stackrel{\to}{\stackrel{\to}{\to}}&
  G 
  &\stackrel{\to}{\to}&
  {*} 
  &\to& 
  \mathbf{B}G
 }
  \,.
$$

See [[principal bundle]] for details on how this works for 1-bundles.

Now from any $X \to \mathbf{B} G$ we obtain another simplicial object $P \times G^{\times n-1}$ with a map to the above of the form

$$
 \array{
  &\cdots&
  P \times G \times G
  &\stackrel{\to}{\stackrel{\to}{\to}}&
  P \times G 
  &\stackrel{\to}{\to}& 
  P 
  &\to& 
  X
  \\
  &\cdots&
  \downarrow
  &&
  \downarrow
  &&
  \downarrow
  &&
  \downarrow
  \\
  &\cdots&
  G \times G
  &\stackrel{\to}{\stackrel{\to}{\to}}&
  G 
  &\stackrel{\to}{\to}& 
  {*} 
  &\to& 
  \mathbf{B}G
 }
  \,.
$$

This encodes the action of $G$ on $P$.

The morphisms of principal $\infty$-bundles are to be such that they respect this action, so that the [[∞-groupoid]] $G Bund(X)$ of $G$-principal $\infty$-bundles on $X$ is naturally equivalent to the cocycle $\infty$-groupoid $Hom_C(X, \mathbf{B} G)$

$$
  G Bund(X) \simeq Hom_C(X, \mathbf{B} G)
  \,.
$$

Then this says that $G$-principal bundles are classified by $G$-[[cohomology]]

$$
  G Bund(X)/_\simeq = H(X,\mathbf{B}G) := Ho_C(X, \mathbf{B}G)
$$

given by the [[hom-set]] in the [[homotopy category of an (infinity,1)-category|homotopy category of the (∞,1)-category]] $C$.

#Connection#

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