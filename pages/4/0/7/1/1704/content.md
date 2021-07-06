
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--




#Contents#
* table of contents
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


## Definition

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

Conversely, for $G \in \mathbf{H}$ we say an object $\mathbf{B}G$ is a [[delooping]] of $G$ if it has an essentially unique point and if $G \simeq \Omega \mathbf{B}G$. We call $G$ an **[[∞-group]]**. More in detail, its structure as a [[groupoid object in an (∞,1)-category|group object in an (∞,1)-category]] is exhibited by the [[?ech nerve]] 

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

To every cocycle $g : X \to \mathbf{B}G$ is canonically associated its [[homotopy fiber]] $P \to X$, the [[(∞,1)-pullback]]

$$
  \array{
    P &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
    \,.
  }
  \,.
$$

We discuss now that $P$ canonically has the structure of a $G$-[[principal ∞-bundle]] and that $\mathbf{B}G$ is the [[fine moduli space]] for $G$-principal $\infty$-bundles.


+-- {: .num_defn}
###### Definition
**(principal $G$-action)**

Let $G$ be a [[groupoid object in an (∞,1)-category|group object in the (∞,1)-topos]] $\mathbf{H}$. A **principal [[action]]** of $G$ on a morphism $(P \to X) \in \mathbf{H}$ is 
a [[groupoid object in an (∞,1)-category|groupoid object]] $P//G$ that sits over $*//G$ in that we have a 
  morphism of [[simplicial object|simplicial diagram]]s $\Delta^{op} \to \mathbf{H}$

$$
  \array{
    \vdots && \vdots
    \\
    P \times G \times G
    &\stackrel{(p_2, p_3)}{\to}& G \times G
    \\
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{}{\to}& {*}
  }
$$

in $\mathbf{H}$;

and such that $P \to X$ exhibits the [[(∞,1)-colimit]]

$$
  X \simeq \lim_\to (P//G : \Delta^{op} \to \mathbf{H})
$$

called the **base space** over which the action takes place.

=--

We may think of $P//G$ as the **[[action groupoid]]** of the $G$-action on $P$. For us it _defines_ this $G$-action.


+-- {: .num_prop}
###### Proposition

The $G$-principal action as defined above satisfies the 
**principality condition** in that we have an equivalence of
groupoid objects

 $$
   \array{
     \vdots && \vdots
     \\
     P \times_X P \times_X P
     &\stackrel{\simeq}{\to}& 
     P \times G \times G
     \\
    \downarrow\downarrow\downarrow 
     && \downarrow\downarrow\downarrow
     \\
     P \times_X P
     &\stackrel{\simeq}{\to}& 
     P \times G
     \\
     \downarrow\downarrow && \downarrow\downarrow
     \\
     P &\stackrel{\simeq}{\to}& P
   }
   \,.
 $$

=--

+-- {: .proof}
###### Proof

This principality condition asserts that the groupoid object $P//G$ is [[groupoid object in an (infinity,1)-category|effective]]. By [[(∞,1)-topos|Giraud's axioms characterizing (∞,1)-toposes]], every groupoid object in $\mathbf{H}$ is effective.

=--


+-- {: .un_prop}
###### Proposition

For $X \to \mathbf{B}G$ any morphism, its [[homotopy fiber]] $P \to X$
is canonically equipped with a principal $G$-action with base space $X$.

=--

+-- {: .proof}
###### Proof

First we show that we have a morphism of simplicial diagrams

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
  \,,
$$

with the right square swhere the left horizontal morphisms are equivalences, as indicated. We proceed by induction through the height of this diagram.

The defining [[(∞,1)-pullback]] square for $P \times_X P$ is 

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

and use the [pasting law for pullbacks](http://ncatlab.org/nlab/show/pullback#Pasting), to conclude that $P \times_X P$ is the pullback

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

By definition of $P$ as the homotopy fiber of $X \to \mathbf{B}G$, the lower horizontal morphism is equivbalent to $P \to {*} \to \mathbf{B}G$, so that $P \times_X P$ is also equivalent to the pullback

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

of which the one on the right is the defining one for $G$ and the remaining one on the left is just an [[(∞,1)-product]].  

Proceeding by induction from this case we find analogously that $P^{\times_X^{n+1}} \simeq P \times G^{\times_n}$: suppose this has been shown for $(n-1)$, then the defining pullback square for $P^{\times_X^{n+1}}$ is

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

This shows that $P//G$ is the [[Cech nerve]] of $P \to X$. It remains to show that
indeed $X = {\lim_\to}_n P \times G^{\times^n}$. 
For this notice that $* \to \mathbf{B}G$ is an [[effective epimorphism in an (infinity,1)-category]]. Hence so is $P \to X$. This proves the claim, by definition of effective epimorphism.


using this we have
$$
  \begin{aligned}
    X & \simeq \mathbf{B}G \prod_{\mathbf{B}G} X
    \\
      & \simeq \left({\lim_{\to}}_n G^{\times^n}\right) \prod_{\mathbf{B}G} X
      \\
      & \simeq {\lim_{\to}}_n ( G^{\times^n} \prod_{\mathbf{B}G} X )
      \\
      & \simeq {\lim_\to}_n ( P\times G^{\times^n} )
      \\
      & \simeq {\lim_\to} P//G
  \end{aligned}
  \,.
$$


=--

We have established that every [[cocycle]] $X \to \mathbf{B}G$ canonically induced a $G$-principal action on the homotopy fiber $P \to X$. The following definition declares the _$G$-principal $\infty$-bundles_ to be those $G$-principal actions that do arise this way.

+-- {: .num_defn}
###### Definition

We say a $G$-principal action of $G$ on $P$ over $X$ is a 
$G$-[[principal ∞-bundle]] if the colimit over $P//G \to *//G$
produces a pullback square: the bottom square in 


$$
  \array{
    \vdots && \vdots
    \\
    P \times G \times G
    &\to& G \times G
    \\
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{}{\to}& {*}
    \\
    \downarrow && \downarrow
    \\
    X = \lim_\to (P \times G^\bullet) &\stackrel{g}{\to}& 
   \mathbf{B}G = \lim_\to( G^\bullet)
  }
  \,.
$$


=--

+-- {: .num_defn}
###### Definition

For $G$ an [[infinity-group]] in $\mathbf{H}$ and $X \in \mathbf{H}$ any object, write

$$
  G Bund(X) \subset Grpd(\mathbf{H})/{*//G}
$$

for the [[sub-(infinity,1)-category]] on the [[over-(infinity,1)-category]] of the groupoid objects over $*//G$ on the $G$-principal $\infty$-bundles as above.

=--

+-- {: .num_prop}
###### Proposition

We have an [[equivalence of (∞,1)-categories]]

$$
  G Bund(X) \simeq \mathbf{H}(X, \mathbf{B}G)
$$

of $G$-principal $\infty$-bundles over $X$ with [[cocycles]] $X \to \mathbf{B}G$.


=-- 

+-- {: .proof}
###### Proof

The [[arrow category]] $\mathbf{H}^I$ is still an [[(infinity,1)-topos]] and hence the Giraud-Lurie axioms still hold. This means that by the discussion at [[groupoid object in an (infinity,1)-category]] (using the statement below [[Higher Topos Theory|HTT, cor. 6.2.3.5]]) we have an equivalence

$$
  Grpd(\mathbf{H}^I) \simeq 
  (\mathbf{H}^{I})^{I}_{eff}
$$

between groupoid objects in $\mathbf{H}^I$ and [[effective epimorphism in an (infinity,1)-category|effective epimorphisms]] in the arrow category. 

Notice that groupoid objects and effective epis in $\mathbf{H}^I$ are given objectwise over the two objects of the interval $I = \Delta[1]$.

Restricting this equivalence along the inclusion

$$
  \mathbf{H}(X, \mathbf{B}G)
    \hookrightarrow
  (\mathbf{H}^I)^I
$$ 

given by sending a cocycle to its homotopy fiber diagram

$$
 (X \to \mathbf{B}G)
  \mapsto 
  \left(
     \array{
        P &\to& * 
        \\
        \downarrow && \downarrow
        \\
        X &\to& \mathbf{B}G
     }
  \right)
$$

therefore yields precisely the equivalence in question

$$
  \array{
     G Bund(X) &\hookrightarrow& Grpd(\mathbf{H}^I)
     \\
     \downarrow^\simeq && \downarrow^\simeq
     \\
     \mathbf{H}(X, \mathbf{B}G)
     &\stackrel{hofib}{\hookrightarrow}&
     (\mathbf{H}^I)^I
  }
  \,.
$$

=--

In words this says that the [[cohomology]] on $X$ with coefficients in $G$ classified $G$-principal $\infty$-bundles, and in fact does so on the level of [[cocycle]]s.

### Connections on $G$-principal $\infty$-bundles

For some comments on the generalization of the notion of [[connection on a bundle]] to principal $\infty$-bundles see [[schreiber:differential cohomology in an (∞,1)-topos -- survey]].

## Concrete realizations 

We discuss realizations of the general definition in various
[[(∞,1)-toposes]] $\mathbf{H}$.

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
just in weak equivalences but is isomorphisms of 
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



### In a petit $(\infty,1)$-topos

For $X$ a [[topological space]] $C = Op(X)$ the [[category of open subsets]] of $X$, let $\mathbf{H} = Sh_{(\infty,1)}(X)$
be the [[(∞,1)-topos]]  of [[∞-stacks]]
on $C$. This is the [[petit topos]] incarnation of $X$.


In its [[presentable (infinity,1)-category|presentation]] by the
[[model structure on simplicial presheaves]] this is the context in which princpal $\infty$-bundles are discussed in

* Jardine, _Diagrams and torsors_ ([pdf](http://www.math.uiuc.edu/K-theory/0723/diagrams3.pdf))

### In a gros $(\infty,1)$-topos

For $C$ a [[site]] of test [[space]], -- for instance duals of [[algebras over a Lawvere theory]] as described at [[function algebras on infinity-stacks]] -- let $\mathbf{H} = Sh_{(\infty,1)}(C)$ be the [[(∞,1)-topos]]  of [[∞-stacks]] on $C$. This is a [[gros topos]].

#### Smooth principal $\infty$-bundles

Smooth principal $\infty$-bundles are realized in the $\infty$-[[Cahiers topos]] as described in some detail at [[∞-Lie groupoid]].

In this context there is a notion of [[connection on a principal ∞-bundle]].

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


### Normal morphisms of $\infty$-groups

A principal $\infty$-bundle over a [[0-connected]] object / [[delooping]] object $\mathf{B}K$ is a _[[normal morphism of ∞-groups]]_. See there for more details.

## Related concepts

* [[principal bundle]] / [[torsor]] / [[associated bundle]] / [[twisted bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[2-gerbe]] / [[bundle 2-gerbe]]

* **principal $\infty$-bundle** / [[associated ∞-bundle]] / [[∞-gerbe]], [[twisted ∞-bundle]], [[groupoid-principal ∞-bundle]]
 
* [[vector bundle]]

* [[(∞,1)-vector bundle]] / [[(∞,n)-vector bundle]]

## References
 {#References}

The notion of principal $\infty$-bundle (often addressed in the relevant literature in the language of [[torsors]]) appears in the context of the [[simplicial presheaf]] [[model structure on simplicial presheaves|model]] for generalized spaces in

* [[Rick Jardine]], Luo, _Higher order principal bundles_ ([pdf](http://www.math.uiuc.edu/K-theory/0681/cocycles6.pdf)).

* [[Rick Jardine]], _Cocycle categories_ ([pdf](http://arxiv.org/abs/math.AT/0605198)).

An earlier description in terms of simplicial objects is

* P. Glenn, _Realization of cohomology classes in arbitrary exact categories_, J. Pure Appl. Algebra 25, 1982, no. 1, 33--105.

In that article not the total space of the bundle $P \to X$ is axiomatized, but the $\infty$-[[action groupoid]] of the action of $G$ on it.

See the remarks at [[principal 2-bundle]].


See also

* {#Wendt10} [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_, J. Homotopy Relat. Struct. 6 (2011), no. 1, 1-38 ([arXiv:1009.2930](http://arxiv.org/abs/1009.2930))

on [[associated ∞-bundle]]s.

The fully general abstract formalization in [[(∞,1)-topos theory]] as discussed here was first indicated in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_

A more comprehensive conceptual account is in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- models and general theory]]_

The [[classifying spaces]] for a large class of principal $\infty$-bundles are discussed in

* [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundle in parameterized spaces_ ([arXiv:1203.2460](http://arxiv.org/abs/1203.2460))
 {#RobertsStevenson}

* [[Danny Stevenson]], _Classifying theory for simplicial parametrized groups_ ([arXiv:1203.2461](http://arxiv.org/abs/1203.2461))
 {#Stevenson}

A fairly comprehensive account of the literature is also in the introduction of [NSS 12, "Presentations"](#NSS12).

For $\mathbf{H}= \infty Grpd$ the statement that homotopy types over $B G$ are equivalently $G$-[[infinity-actions]] is maybe due to 

* E. Dror, [[William Dwyer]], and [[Daniel Kan]], _Equivariant maps which are self homotopy equivalences_, Proc. Amer. Math. Soc. 80 (1980), no. 4, 670&#8211;672 ([JSTOR](http://www.jstor.org/stable/2043448))

This is mentioned for instance as exercise 4.2in 

* {#Dwyer2008} [[William Dwyer]], _Homotopy theory of classifying spaces_, Lecture notes Copenhagen (June, 2008) [pdf](http://www.math.ku.dk/~jg/homotopical2008/Dwyer.CopenhagenNotes.pdf)

Closely related discussion of homotopy fiber sequences and homotopy action but in terms of [[Segal spaces]] is in section 5 of

* [[Matan Prezma]], _Homotopy normal maps_ ([arXiv](http://arxiv.org/pdf/1011.4708v7.pdf)) 

There, conditions are given for a morphism $A_\bullet \to B_\bullet$ to a [[reduced Segal space]] to have a fixed homotopy fiber, and hence encode an action of the loop group of $B$ on that fiber. 

Discussion in [[higher differential geometry]] of [[Kaluza-Klein compactification]] along [[principal ∞-bundles]], relating to [[double field theory]], [[T-folds]], [[non-abelian T-duality]], [[type II geometry]], [[exceptional geometry]]:

* [[Luigi Alfonsi]], _Global Double Field Theory is Higher Kaluza-Klein Theory_ ([arXiv:1912.07089](https://arxiv.org/abs/1912.07089))

* [[Luigi Alfonsi]], _The puzzle of global Double Field Theory: open problems and the case for a Higher Kaluza-Klein perspective_ ([arXiv:2007.04969](https://arxiv.org/abs/2007.04969))





[[!redirects principal infinity-bundles]]
[[!redirects principal ∞-bundle]]
[[!redirects principal ∞-bundles]]