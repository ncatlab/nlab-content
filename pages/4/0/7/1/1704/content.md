
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _principal $\infty$-bundle_ is a [[vertical categorification|categorification]] of [[principal bundle]] from [[groups]] and [[groupoids]] to [[∞-groupoids]], or rather from parameterized groupoids (generalized spaces called [[stacks]]) to parameterized $\infty$-groupoids (generalized spaces called [[∞-stacks]]).



For motivation, background and further details see 

* [[motivation for sheaves, cohomology and higher stacks]]
* [[principal bundle]]
* [[gerbe]]
* [[principal 2-bundle]].

A model for principal $\infty$-bundles is given by 

* [[simplicial principal bundle]]s.

See also

* [[universal principal ∞-bundle]]

* [[groupal model for universal principal ∞-bundles]].


## Definition in a general $(\infty,1)$-topos 

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

Conversely, for $G \in \mathbf{H}$ we say an object $\mathbf{B}G$ is a [[delooping]] of $\mathbf{H}$ if it has an essentially unique point and if $G \simeq \Omega \mathbf{B}G$. We call $G$ an **[[∞-group]]**. More in detail, its structure as a [[groupoid object in an (∞,1)-category|group object in an (∞,1)-category]] is exhibited by the [[?ech nerve]] 

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

### $G$-principal $\infty$-bundles {#GeneralPrincBund}

By the general reasoning discussed at [[cohomology]], a [[cocycle]] for $G$-[[nonabelian cohomology]] on $X \in \mathbf{H}$ is just a morphism $g : X \to \mathbf{B}G$ in $\mathbf{H}$. 

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

The defining [[limit in a quasi-category|(∞,1)-pullback]] square for $P \times_X$ is 

$$
  \array{
    P \times_X P &\to& P
    \\
    \downarrow && \downarrow
    \\
    P &\to& X
  }
$$

To compute this, we may attach the defining $(\infty,1)$-pullback square of $P$ to obtain the [[pasting]] diagram

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

By the [pasting law for pullbacks](http://ncatlab.org/nlab/show/pullback#Pasting), this says that $P \times_X P$ is the pullback

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

Again by defnition of $P$, the lower horizontal morphism is equivbalent to $P \to {*} \to \mathbf{B}G$, so that $P \times_X P$ is also (equivalent to) the pullback

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

This finally may be computed as the pasting of two pullbacks

$$
  \array{
    P \times_X P &\simeq& P \times G &\to& G &\to& {*}
    \\
    &&\downarrow && \downarrow && \downarrow
    \\
    &&P &\to& {*} &\to& \mathbf{B}G
    \,.
  }
$$

of which the one on the right is the defining one for $G$ and the remaining one on the left is just a [[product]].

Proceeding by induction from this case one finds analogousy that $P^{\times_X^{n+1}} \simeq P \times G^{\times_n}$: suppose this has been shown for $(n-1)$, then the defining pullback square for $P^{\times_X^{n+1}}$ is

$$
  \array{
    P \times_X P^{\times_X^n}
    &\to&
    P
    \\
    \downarrow && \downarrow
    \\
    P^{\times_X^n}&\to& X
  }
  \,.
$$

We may again paste this to obtain

$$
  \array{
    P \times_X P^{\times_X^n}
    &\to&
    P
    &\to&
    *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P^{\times_X^n}&\to& X &\to& \mathbf{B}G
  }
$$

and use from the previous induction step that

$$
  (P^{\times_X^n} \to X \to \mathbf{B}G) 
  \simeq
  (P^{\times_X^n} \to * \to \mathbf{B}G)
$$

to conclude the induction step with the same arguments as before.

=--



+-- {: .un_remark}
###### Remark
**(terminology)**

For ordinary [[principal bundle]]s the following terminology is standard:

* the morphism $P \times_X P \stackrel{}{\to} P \times G$ is the **division map**;

* the fact that the division map is an equivalence is the **principality condition** on the $G$-action;

* the image $\rho : P \times G \to P$ under the division map of the projection $p_2 : P \times_X P \to P$ is the **[[action]]** of $G$ on $P$.

=--

The above shows how every cocycle $X \to \mathbf{B}G$ induces a map $P \to X$ equipped with a $G$-action. Conversely, we may _define_ a $G$-action on an object $V$ to be a [[groupoid object in an (∞,1)-category|groupoid object in an (∞,1)-topos]] sitting over $G$.


+-- {: .un_defn}
###### Definition
**(principal $G$-action)**

Let $G$ be a [[groupoid object in an (∞,1)-category|group object in the (∞,1)-topos]] $\mathbf{H}$. A principal [[action]] of $G$ on another object $V \in \mathbf{H}$ is a [[groupoid object in an (∞,1)-category|groupoid object in the (∞,1)-topos]] $V//G \to G$ _over $G$_ in that we have a morphism of [[simplicial object]]s

$$
  \array{
    \vdots && \vdots
    \\
    V \times G \times G
    &\stackrel{(p_2, p_3)}{\to}& G \times G
    \\
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    V \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow && \downarrow\downarrow
    \\
    V &\stackrel{}{\to}& {*}
  }
$$

in $mathbf{H}$.

We call the [[groupoid object in an (infinity,1)-category|groupoid object]] $(V \times G^\bullet)$ the **[[action groupoid]]** of the $G$-action on $V$. (For us it _defines_ this $G$-action.)

=--

+-- {: .un_remark}
###### Remark

Since by one of the Giraud's axioms that hold in the [[(∞,1)-topos]] $\mathbf{H}$ all groupoid objects are <a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity%2C1)-category#Effective">effective</a> we have:

1. we may essentially identify the simplicial object $(V \times G^\bullet)$
   with its [[limit in a quasi-category|(∞,1)-colimit]]

   $$
     {\lim_\to}_n V \times G^{n} \;\;\; \in \mathbf{H}
   $$

   and we shall denote both by $V//G$.

1. The above definition of $G$-action indeed _implies_ the principality condition

   $$
     \array{
       \vdots && \vdots
       \\
       V \times_X V \times_X V
       &\stackrel{\simeq}{\to}& 
       V \times G \times G
       \\
      \downarrow\downarrow\downarrow 
       && \downarrow\downarrow\downarrow
       \\
       V \times_X V
       &\stackrel{\simeq}{\to}& 
       V \times G
       \\
       \downarrow\downarrow && \downarrow\downarrow
       \\
       V &\stackrel{}{\to}& {*}
     }
   $$

   where the base space $X := V//G$ is precisely the quotient object
   in $\mathbf{H}$. This equivalence is precisely what effectivity means.


=--

+-- {: .un_lemma}
###### Lemma

If $V \times G^\bullet $ is a principal action groupoid as above  then the
induced diagram

$$
   \array{
      & V &\to& {*}
      \\
      & \downarrow && \downarrow
      \\
      V//G := & \lim_\to V\times G^{\times \bullet} &\to&
      \mathbf{B}G 
   }
$$

is a [[limit in a quasi-category|(∞,1)-pullback diagram]].

=--

+-- {: .proof}
###### Proof

Consider the [[pasting]] [[diagram]]

$$
  \array{
    V \times_X V &\to& V &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    V &\to& X &\to& \mathbf{B}G
  }
  \,.
$$

The left square is a pullback by definition. By principality the top left object is $\simeq V \times G$, which says that also the outer rectangle is a pullback (as in the above lemma). Therefore by the pasting property of [[pullback]]s, also the right square is a pullback.


=--


+-- {: .un_def}
###### Definition
**($G$-$\infty$-torsor / $G$-principal $\infty$-bundle)**

The above shows that every $G$-cocycle induces 

1. an **$\infty$-[[bundle]]** $P \to X$ 

1. equipped with a **$G$-[[action]]** on $P$

1. which is **principal** in that $X \simeq P//G$

Conversely, any such collection we call
a **$G$-principal $\infty$-bundle** or a **$G$-$\infty$-torsor** 
over $X$ in the given [[(∞,1)-topos]] $\mathbf{H}$.

=--

+-- {: .un_remark}
###### Remark
**(classification of $G$-principal $\infty$-bundles)**

The ambient [[∞-stack]] [[(∞,1)-topos]] $\mathbf{H}$ 
satisfies (as described there) the analog of Giraud's axioms.
These serve to show that $G$-principal $\infty$-bundles are
indeed _classified_ by their corresponding cocycles:

one of the axioms says that every 
[[groupoid object in an (∞,1)-category|groupoid object]] in $\mathbf{H}$
is [[quotient object|effective]], in that the morphism to its
[[homotopy colimit]] is an [[effective epimorphism]].

But this means that starting with the $G$-action on $P$, 
passing to the [[cocycle]] $g$ obtained from the quotient

$$
  \array{
     P &\to& {*}
     \\
     \downarrow  && \downarrow
     \\
     X \stackrel{\simeq}{\to} P//G &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

and then reconstructing from this cocycle its [[homotopy fiber]]
with the induced $G$-action as above, we do reproduce, up  to equivalence
the $G$-principal bundle that we started with.

=--




 
### Morphisms of $G$-principal $\infty$-bundles

The morphisms of $G$-principal $\infty$-bundles are to be such that they respect the $G$-action, so that the [[∞-groupoid]] $G Bund(X)$ of $G$-principal $\infty$-bundles on $X$ is naturally equivalent to the cocycle $\infty$-groupoid $Hom_C(X, \mathbf{B} G)$

$$
  G Bund(X) \simeq Hom_C(X, \mathbf{B} G)
  \,.
$$

Then this says that $G$-principal bundles are classified by $G$-[[cohomology]]

$$
  G Bund(X)/_\simeq = H(X,\mathbf{B}G) := Ho_C(X, \mathbf{B}G)
$$

given by the [[hom-set]] in the [[homotopy category of an (infinity,1)-category|homotopy category of the (∞,1)-category]] $C$.

### Connections on $G$-principal $\infty$-bundles

For some comments on the generalization of the notion of [[connection on a bundle]] to principal $\infty$-bundles see [[schreiber:differential cohomology in an (∞,1)-topos -- survey]].

## Concrete realizations 

We discuss realizations of the general idea in various
[[(∞,1)-toposes]].

### In topological spaces 

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

### In simplicial sets / Kan complexes

See [[simplicial principal bundle]].



### In simplicial presheaves

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


## Examples

### Ordinary principal bundles

For $G$ an ordinary [[Lie group]], a $G$-principal bundle in the $(\infty,1)$-topos $\mathbf{H} = $ [[?LieGrpd]] is an ordinary $G$-[[principal bundle]].

### Circle $n$-bundles

For $G = \mathbf{B}^{n-1} U(1) \in $ [[?LieGrpd]], the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle Lie n-group</a>, a $G$-principal $\infty$-bundle is a **circle $n$-bundle**.

See [[circle n-bundle with connection]].

Classes of examples include

* the [[Chern-Simons circle 3-bundle]].

### Bundle gerbes

* A [[bundle gerbe]]  is a concrete model for the total space [[groupoid]] of the total space of a $\mathbf{B}U(1)$-[[principal 2-bundle]]. 

  More generally, a [[nonabelian bundle gerbe]] is a concrete model for the [[groupoid]] of the total space of a general [[principal 2-bundle]].

* A [[bundle 2-gerbe]]  is a concrete model for the total space [[2-groupoid]] of the total space of a $\mathbf{B}^2 U(1)$-principal 3-bundle. 

  More generally, a [[nonabelian bundle 2-gerbe]] is a concrete model for the [[2-groupoid]] of the total space of a general principal 3-bundle.

  Classes of examples include

  * the [[Chern-Simons bundle 2-gerbe]].
 

## References

The notion of principal $\infty$-bundle (often addressed in the relevant literature in the language of [[torsors]]) appears in the context of the [[simplicial presheaf]] [[model structure on simplicial presheaves|model]] for generalized spaces in

* Jardine, Luo, _Higher order principal bundles_ ([pdf](http://www.math.uiuc.edu/K-theory/0681/cocycles6.pdf)).

* Jardine, _Cocycle categories_ ([pdf](http://arxiv.org/abs/math.AT/0605198)).

An earlier description in terms of simplicial objects is

* P. Glenn, _Realization of cohomology classes in arbitrary exact categories_, J. Pure Appl. Algebra 25, 1982, no. 1, 33--105.

In that article not the total space of the bundle $P \to X$ is axiomatized, but the $\infty$-[[action groupoid]] of the action of $G$ on it.

See the remarks at [[principal 2-bundle]].


[[!redirects principal infinity-bundles]]
[[!redirects principal ∞-bundle]]
[[!redirects principal ∞-bundles]]