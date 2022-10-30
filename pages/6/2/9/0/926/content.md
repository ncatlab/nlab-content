
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _Postnikov system_ is the [[infinitary factorization system]] of [[(n-epi, n-mono) factorization system|(n-epi, n-mono)-factorizations]] through [[n-images]] in an [[(∞,1)-topos]].

The basic (and historically first) example is the factorization in [[∞Grpd]]/[[Top]] of morphisms to the point: here the Postnikov system assigns to a [[homotopy type]] $X$ a [[tower]]

$$
  X \to \cdots \to X_3 \to X_2 \to X_1 \to X_0  \simeq *
$$

where each $X_k$ is a [[homotopy n-type|homotopy (k-2)-type]]/[[n-truncated object in an (infinity,1)-category|(n-2)-truncated object]] and such that each morphism $X_{k+1} \to X_k$ induces an [[isomorphism]] on [[homotopy groups]] in degree $\leq k-2$.
This may be thought of as decomposing $X$ into its "layers" as seen by the degree of [[homotopy groups]]. The [[characteristic classes]] which give the [[∞-group extension]] in each layer are called the _[[Postnikov invariants]]_ or _[[k-invariants]]_ of $X$.

More generally, in any [[(∞,1)-topos]] and for any [[morphism]] $f \colon X \to Y$ the corresponding Postnikov system is a [[tower]]

$$
  f \colon X \simeq im_\infty(f) \to \cdots \to im_2(f) \to im_1(f) \to im_0(f) \simeq Y
$$

of [[n-images]] of $f$ which interpolates between $X$ and $Y$ along $f$: the object $im_n(f)$ is a [[homotopy type]] that looks like $X$ in low degrees (below $n-1$), looks like $Y$ in high degrees (above degree $n$) and looks like the ordinary (1-[[topos theory|topos theoretic]]) [[image]] of $f$ _on homotopy groups_ in degree $n-1$ itself.


## Definition

In full generality, the Postnikov system is the [[infinitary factorization system]] of [[(n-epi, n-mono) factorization system|(n-epi, n-mono)-factorizations]] through [[n-images]] in an [[(∞,1)-topos]]. 

The following spells this out explicitly for default [[homotopy theory]], hence in [[∞Grpd]] and in terms of the [[presentable (∞,1)-category|presentation]] by the [[model structure on topological spaces]] and the [[model structure on simplicial sets]]:

* _[For topological spaces](#DefinitionForTopologicalSpaces)_

* _[For simplicial sets](#DefinitionForSimplicialSets)_. 

With a little bit of care this induces corresponding presentations of Postnikov systems in general [[(∞,1)-topos]] by prolonging to suitable [[model structures on simplicial presheaves]]:

* _[For simplicial presheaves](#DefinitionForSimplicialPresheaves)_.

For more discussion of the general abstract situation see at

* _[[Postnikov tower in an (∞,1)-category]]_



### For topological spaces
 {#DefinitionForTopologicalSpaces}

Historically, Postnikov systems were first described on the model of [[homotopy types]] constituted by [[topological spaces]].

A __Postnikov system__ or __Postnikov [[tower]]__ or **Moore-Postnikov tower/system** of [[topological spaces]], or rather of their [[homotopy types]], is a sequence of [[path connected topological space|path connected]], [[pointed object|pointed]] [[topological spaces]] $X^{(n)}$, $n \geq 1$,
such that $\pi_r(X^{(n)})=0$ for $r \gt n$,
together with a sequence $\pi_n$ of [[module]]s of the [[fundamental group]] $\pi_1(X^{(1)})$ of $X^{(1)}$ and
[[fibration]]s $p_n : X^{(n+1)} \to X^{(n)}$ classified up to [[homotopy type]] by a specified cohomology class $k^{n+1} \in H^{n+1}(X^{(n)}, \pi_n)$. 

### For simplicial sets
 {#DefinitionForSimplicialSets}

We discuss the realization of Postnikov systems on [[simplicial sets]]/[[Kan complexes]], first in the 

* _[Absolute version](#DefinitionForSimplicialSetsAbsoluteVersion)_

and then more generally for the 

* _[Relative version](#ForSimplicialSetsRelativeVersion)_

#### Absolute version
 {#DefinitionForSimplicialSetsAbsoluteVersion}

+-- {: .num_defn #SimplicialPostnikovTower}
###### Definition

Let $X$ be a [[simplicial set]]. A **Postnikov tower** for $X$ is 

1. a sequence

   $$
     \cdots \to X_2 
       \stackrel{q_1}{\to}
     X_1
       \stackrel{q_0}{\to} 
     X_0
   $$

   with maps $i_n : X \to X_n$ such that all [[diagram]]s

   $$
     \array{
        && X
        \\
        & {}^{\mathllap{i_n}}\swarrow &&   
         \searrow^{\mathrlap{i_{n-1}}}
        \\
        X_n && \stackrel{q_{n-1}}{\to} && X_{n-1}
     }
   $$

   [[commuting diagram|commute]];

1. such that for all vertices $v \in X_0$ we have for the [[homotopy group]]s

   $$
     \pi_{\gt n}( X_n, v) = 0
   $$

   and

   $$
     (i_n)_* : \pi_i (X,v) \stackrel{\simeq}{\to} \pi_i X_n
   $$

   for $i \leq n$.


=--

This appears for instance as ([GoerssJardine, def VI 3.1](#GoerssJardine)).

#### Relative version
 {#ForSimplicialSetsRelativeVersion}


+-- {: .num_defn #SimplicialPostnikovTowerRelative}
###### Definition

Let $f : X \to Y$ be a homomorphism of [[simplicial sets]]. 
A (relative) **Postnikov tower** for $f$ is a [[tower]]

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    im_\infty(f)
    \\
    \downarrow
    \\
    \vdots
    \\
    \downarrow
    \\
    im_2(f)
    \\
    \downarrow
    \\
    im_1(f)
    \\
    \downarrow
    \\
    im_0(f)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    Y
  }
$$

that factors $f : X \to Y$ such that for all $n \in \mathbb{N}$

1. $X \to im_n(f)$ 

   1. induces an [[epimorphism]] on [[homotopy groups]] in degree $n-1$;

   1. induces an [[isomorphism]] on [[homotopy groups]] in degree $\lt n-1$

1. $im_n(f) \to Y$ 

   1. induces a [[monomorphism]] on [[homotopy groups]] in degree $n-1$;

   1. induces an [[isomorphism]] on [[homotopy groups]] in degree $\geq n$.


=--



This appears for instance as ([Goerss-Jardine, def. VI 2.9](#GoerssJardine)).


+-- {: .num_remark }
###### Remark

By the [[long exact sequence of homotopy groups]], the relative Postnikov tower is the tower of the [[(n-connected, n-truncated) factorization system]] of $f$ regarded as a morphism in the [[(∞,1)-category]] [[∞Grpd]]: is is the [[n-epimorphism]],[[n-monomorphism]] factorization through the  _[[n-image]]_ of a morphism.

=--

### For simplicial presheaves
 {#DefinitionForSimplicialPresheaves}

## Constructions

We discuss explicit constructions/presentations of Postnikov systems. 

* _[For simplicial sets](#ConStructionForSimplicialSets)_

* _[For strict &#969;-groupoids](#ForStrctOmegaGroupoids)_.

### For simplicial sets
 {#ConStructionForSimplicialSets}

There are three main functorial models for the Postnikov tower of a [[simplicial set]]:

* _[Coskeleton tower](#CoskeletonTower)_;

* _[Identification relative to skeleta](#IdentificationRelativeSkeleta)_;

* _[Homotopy classes relative to skeleta](#HomotopyClassesRelativeSkeleta)_

#### Coskeleton tower
 {#CoskeletonTower}

+-- {: .num_prop}
###### Proposition


If $X$ is regarded as an [[∞-groupoid]] modeled as a [[Kan complex]], then the [[coskeleton]] sequence

$$
  X = \lim_n cosk_n X \to \cdots \to cosk_{n+1} X \to cosk_{n} X \to \cdots \to *
$$

exhibits a Postnikov tower for $X$. 

=--

This is observed for instance in ([DwyerKan](#DwyerKan)). Also see [[coskeleton]] for more details.

#### Identification relative to skeleta
 {#IdentificationRelativeSkeleta}

The following construction quotients out the relations encoded by the cells that are thrown in in the above construction, such as to make the maps in the Postnikov tower into [[Kan fibrations]].

We first discuss the absolute tower  and then the relative version.

##### Absolute Postnikov tower

+-- {: .num_defn}
###### Definition

Let $X$ be a [[Kan complex]]. Define for each $n \in \mathbb{N}$  an [[equivalence relation]]  $\sim_n$ on the simplices of $X$ as follows: two $q$-simplices 

$$
  \alpha, \beta : \Delta^q \to X
$$

are equivalent if their restriction to the $n$-[[simplicial skeleton|skeleton]] coincides

$$
  sk_n(\alpha) = sk_n(\beta)
  : 
  sk_n(\Delta^q)
  \hookrightarrow
  \Delta^q
  \to X
  \,.
$$

Write 

$$
  X(n) := X/_{\sim_n}
$$

for the [[quotient]] [[simplicial set]].

=--

There are evident morphisms

$$
  X(n) \to X(n-1).
$$

+-- {: .num_prop #SimplPostnikovByCoskeletonQuotient}
###### Proposition

This is a Postnikov tower, def. \ref{SimplicialPostnikovTower}, and all morphisms are [[Kan fibrations]].

Moreover the canonical morphism

$$
  X \to \lim_{\leftarrow_n} X(n)
$$

is an [[isomorphism]], exhibiting $X$ as the [[limit]] ("[[inverse limit]]") over this tower diagram.

=--

This appears for instance as ([GoerssJardine, theorem Vi 3.5](#GoerssJardine)).

##### Relative Postnikov tower
 {#RelativePostnikovTowerConstruction}


We discuss a model for the relative Postnikov tower, def. \ref{SimplicialPostnikovTowerRelative}.

+-- {: .num_defn}
###### Definition

For $f : X \to Y$ a [[Kan fibration]] between [[Kan complexes]], 
define for each $n$ and each $k$ an [[equivalence relation]] $\sim_n$ on $k$-[[simplices]]

$$
  \alpha, \beta \colon \Delta^k \to X
$$

such that $\alpha \sim_n \beta$ if

1. the $n$-[[skeleta]] $sk_n \Delta^k \to \Delta^k \stackrel{\alpha, \beta}{\to} X$ are equal;

1. the [[images]] $f(\alpha), f(\beta)\in Y$ are equal.

Let 

$$
  im_{n+1}(f) \coloneqq X/\sim_n
$$

be the simplicial set of [[equivalence classes]] under this equivalence relation.

This canonically comes with morphisms $im_{n_1}(f) \to im_{n_2}(f)$ for $\infty \geq n_1 \gt n_2 \geq 0$.

=--

For instance ([Goerss-Jardine, def. VI 2.9](#GoerssJardine)).


+-- {: .num_prop}
###### Proposition

This construction gives indeed a relative Postnikov tower for $f$.

=--

For instance ([Goerss-Jardine, theorem VI 2.11](#GoerssJardine)).


#### Homotopy classes relative to skeleta
 {#HomotopyClassesRelativeSkeleta}

For $X$ a [[Kan complex]] and $n \in \mathbb{N}$,
let $\tau_{\lt n}X$ be the simplicial set defined as
the [[quotient]]

$$
  \tau_{\lt m}X : k \mapsto X_k / homotopy-rel-(n-1)-skeleton
  \,,
$$

where two $k$-cells are identified if there is a simplicial [[homotopy]] between them that fixes their $(n-1)$-skeleton.

This is due to [[John Duskin]]. See for instance ([Beke, pages 302-305](#Beke)).


### For strict $\omega$-groupoids
 {#ForStrictOmegaGroupoids}

+-- {: .num_prop}
###### Proposition

Consider a morphism in [[sSet]]/[[∞Grpd]] that is in the image of $Str\omega Grpd$, hence given by a morphism $f \colon X \to Y$ of [[strict ∞-groupoids]].

Then for $n \in \mathbb{N}$ the [[n-image]] factorization/$(n-1)$-Postnikov stage of $f$ is given by the [[strict ∞-groupoid]] $im_n(f)$ with

$$
  \left(im_n\left(f\right)\right)_k
  =
  \left\{
    \array{
      X_k & \forall  k \lt n-1
      \\
      im(X_{n-1}) \subset Y_{n-1} & \forall \; k = n-1
      \\
      Y_k & \forall  k \geq n
    }
  \right.
$$

equipped with the evident [[composition]] operations induced from those of $X$ and $Y$, and equipped with the canonical morphisms of strict $\omega$-groupoids

$$
  X \to im_n(f) \to Y
$$

(the left one being the identity in degree $k \lt n-1$, the quotent projection in degree $n-1$ and $f$ in degree $k \geq n$, and the right one being $f$ in degree $k \lt n-1$, the image inclusion in degree $n-1$ and the identity in degree $k \geq n$).
=--

For $Y = *$ this is discussed in ([BFGM](#BFGM)).

+-- {: .proof}
###### Proof

The [[homotopy groups]] of a strict $\omega$-groupoid in any degree $k$ are simply given by the groups of $k$-[[automorphisms]] of the identity $(k-1)$-morphism on a given baspoint modulo $(k+1)$-morphisms (hence the homology of the corresponding [[crossed complex]] in that degree). Therefore it is clear from the construction of $im_n(f)$ above that $X \to im_n(f)$ is surjective on $\pi_0$ and an isomorphism on $\pi_{k \lt n-1}$, and that $im_n(f)$ is a monomorphism on $\pi_{n-1}$ and an isomorphism on $\pi_{k \geq n}$.

=--

## Properties

### General

It is known that Postnikov systems classify all weak, pointed [[connected space|connected]] [[homotopy type]]s. In particular, if $X$ satisfies $\pi_r(X)=0 $ for $1 \lt r \lt n$ then the first non trivial Postnikov invariant is an  element $k^{n+1}$ of [[group cohomology]] (with twisted coefficients of course). Such elements are also determined by $n$-fold crossed extensions of $\pi_n$ by $\pi_1$,
which are exact [[crossed complex]]es of the form
$$ 0 \to \pi_n \to C_n \to C_{n-1} \to \cdots \to C_2 \to C_1 $$
together with an isomorphism $Coker(C_2 \to C_1) \cong \pi_1$. This
gives an algebraic model of such an $n$-[[homotopy n-type|type]]. Advantages of
algebraic models are that algebraic constructions can be made on
them, such as forming [[limits]] or colimits. The various [[higher
homotopy van Kampen theorem]]s are useful in the latter case. For
example, it may be difficult or well nigh impossible to write down a
determination of the Postnikov invariant of a pushout of crossed
modules, even if the pushout consists of finite groups.

A Postnikov system is easiest to understand in the 2-stage case,
i.e. two non vanishing homotopy groups, and focuses attention on the
cohomology of [[Eilenberg-Mac Lane space]]s, which also determine all
[[cohomology operation]]s. Basic work on this area was done by Eilenberg
and Mac Lane, and by H. Cartan, while the theory of cohomology
operations, including [[Steenrod operation]]s, is itself a large area.

The reference below shows the problems in the 3-stage systems. 

For homotopy 3-types, the algebraic model of [[crossed square]]s is more explicit than the corresponding Postnikov system, and more calculable. However, not much work has been done on, say, [[cohomology operation]]s using the algebraic model of $n$-fold groupoids, and it is not clear if that would help. 

### For simplicial sets

+-- {: .num_prop }
###### Proposition

Let $X$ be a [[Kan complex]] and $\{X(n)\}$ the model for its Postnikov tower from prop. \ref{SimplPostnikovByCoskeletonQuotient}. For any vertex $v \in X_0$ write $K(n)$ for the [[pullback]]

$$
  \array{
    K(n) &\to& *
    \\
    \downarrow && \downarrow^{\mathrlap{b}}
    \\
    X(n) &\to& X(n-1)
  }
  \,.
$$

Let $K(\pi_n (X,v), n)$ be the [[Eilenberg-MacLane object]] on the $n$-[[homotopy group]] of $X$. Then there is a [[weak homotopy equivalence]]

$$
  K(n) \stackrel{\simeq}{\to} K(\pi_n(X,v),n)
  \,.
$$

=--

This appears for instance as [GoerssJardine, corollary VI 3.7](#GoerssJardine).

+-- {: .proof}
###### Proof

Since $K(n) \to K(n-1)$ is a [[Kan fibration]] by prop.
\ref{SimplPostnikovByCoskeletonQuotient} the pullback $K(n)$ is the [[homotopy fiber]] of $X(n) \to X(n-1)$.

=--

## Generalizations

There are analogues in other setups, e.g. 

* [[Postnikov system in triangulated category|Postnikov systems in triangulated categories]] 

* [[motive|motivic]] homotopy theory (M. Levine, [The Postnikov tower in motivic stable homotopy theory](http://www.math.uiuc.edu/K-theory/0692)).

### Postnikov tower in an $(\infty,1)$-category

We may think of [[Top]] as being the archetypical [[(∞,1)-category]].

In every [[(∞,1)-category]] there is a notion of [[n-truncated object in an (∞,1)-category|n-truncated object]] and accordingly a notion of

* [[Postnikov tower in an (∞,1)-category]].

The traditional case of Postnikov towers in [[Top]] is a special case of this more general concept.

## Related concepts

* [[n-image]], [[n-epimorphism]], [[n-monomorphism]]

* [[Postnikov invariant]]/[[k-invariant]]

* [[k-ary factorization system]]

* [[chromatic tower]], [[Taylor tower]]

## References

A standard textbook reference is section 8 of 

* [[Peter May]], _Simplicial methods in algebraic topology_  ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu))

and section VI of 

* {#GoerssJardine} [[Paul Goerss]], [[Rick Jardine]], _[[Simplicial homotopy theory]]_
  


Orginal references include

* [[M. M. Postnikov]], _Determination of the homology groups of a space by means of the homotopy invariants_, Doklady Akad. Nauk SSSR (N.S.) 76: 359&#8211;362 (1951)

* [[George Whitehead]], _Elements of homotopy theory_, chapter 9

* Donald W. Kahn, _The spectral sequence of a Postnikov system_, Comm. Math. Helv. 40, n.1, 169--198, 1965 [doi](http://dx.doi.org/10.1007/BF02564370)

* P. I. Booth, _An explicit classification of three-stage Postnikov towers_, Homology, homotopy and applications 8 (2006), No. 2, 133--155
* [[G. J. Ellis]] and R. Mikhailov, _A colimit of classifying spaces_, [arXiv:0804.3581](http://www.arxiv.org/abs/0804.3581).

Probably the earliest treatment of Postnikov systems for [[simplicial sets]] is in

* [[John Moore|J. C. Moore]], _Semisimplicial complexes and Postnikov systems_, Symposium Internacional
de Topologia Algebraica, Mexico City, 1958, pp. 232-247,

and as a result, in that context, they are sometimes referred to as **Moore-Postnikov systems**


The coskeleton construction for the Postnikov tower of a Kan complex is already in 

* Artin, Mazur, _&#201;tale homotopy_, (Lecture Notes in Maths. 100). 

Another  classical article that amplifies the expression of Postnikov towers in terms of [[coskeleta]] is

* {#DwyerKan} [[William Dwyer]], [[Dan Kan]], _An obstruction theory for diagrams of simplicial sets_ ([pdf](http://www.nd.edu/~wgd/Dvi/ObstructionTheoryForDiagrams.pdf)), from 1984.
 

Analogous remarks are also in

*  [[John Duskin]] _Simplicial matrices and the nerves of weak $n$-categories I: Nerves of bicategories_ , TAC **9** no. 2, (2002). ([web](http://www.emis.de/journals/TAC/volumes/9/n10/9-10abs.html))

reviewed around page 302 in 

* {#Beke} [[Tibor Beke]], _Higher &#268;ech theory_, K-Theory, 32(4):293&#8211;322 (2004) ([web](http://www.math.uiuc.edu/K-theory/0646/))
 

Discussion in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], section 7.6 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_



Discussion for [[homotopy types]] modeled by [[crossed complexes]]/[[strict ∞-groupoids]] is in

* {#BFGM} M. Bullejos, E. Faro, and M. A. Garc&#237;a-Munoz, _Postnikov Invariants of Crossed Complexes_, Journal of Algebra Volume 285, Issue 1, 1 March 2005, Pages 238&#8211;291 ([arXiv:math/0409339](http://arxiv.org/abs/math/0409339)).
 

and for $n$-[[hypergroupoids]] in the thesis,

* M. A. Garc&#237;a-Munoz,  2003, _Un aceramiento algebraico a la theor&#237;a de 
Torres de Postnikov_, [thesis](http://0-hera.ugr.es.adrastea.ugr.es/tesisugr/16555065.pdf),  Universidad de Granada. 

This also contains a good discussion of the link with twisted cohomology and homotopy colimits.

A pedagogical introduction to Postnikov systems with an eye towards their generalization from [[homotopy types]] to [[n-categories]] is in

* [[John Baez]], [[Mike Shulman]], _[[Lectures on n-Categories and Cohomology]]_


[[!redirects Postnikov tower]]
[[!redirects Postnikov towers]]

[[!redirects Postnikov decomposition]]
[[!redirects Postnikov systems]]
