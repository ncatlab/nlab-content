
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### For topological spaces

A __Postnikov system__ or __Postnikov [[tower]]__ of [[topological spaces]] ([[M M Postnikov]], 1951) is a sequence of [[path connected topological space|path connected]], [[pointed object|pointed]] [[topological spaces]] $X^{(n)}$, $n \geq 1$,
such that $\pi_r(X^{(n)})=0$ for $r \gt n$,
together with a sequence $\pi_n$ of [[module]]s of the [[fundamental group]] $\pi_1(X^{(1)})$ of $X^{(1)}$ and
[[fibration]]s $p_n : X^{(n+1)} \to X^{(n)}$ classified up to [[homotopy type]] by a specified cohomology class $k^{n+1} \in H^{n+1}(X^{(n)}, \pi_n)$. 

### For simplicial sets

#### Absolute version

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

   1. induces an [[epimorphism]] on connected components;

   1. induces an [[isomorphism]] on [[homotopy groups]] in degree $\leq n-1$

1. $im_n(f) \to Y$ 

   1. induces a [[monomorphism]] on [[homotopy groups]] in degree $n-1$;

   1. induces an [[isomorphism]] on [[homotopy groups]] in degree $\geq n$.


=--



This appears for instance as ([Goerss-Jardine, def. VI 2.9](#GoerssJardine)).


+-- {: .num_remark }
###### Remark

By the [[long exact sequence of homotopy groups]], the relative Postnikov tower is the tower of the [[(n-connected, n-truncated) factorization system]] of $f$ regarded as a morphism in the [[(∞,1)-category]] [[∞Grpd]]. For more on this see at _[[∞-image]]_.

=--


## Constructions

### For simplicial sets
 {#ConStructionForSimplicialSets}

There are three main functorial models for the Postnikov tower of a simplicial set.

* [Coskeleton tower](#CoskeletonTower);

* [Identification relative to skeleta](#IdentificationRelativeSkeleta);

* [Homotopy classes relative to skeleta](#HomotopyClassesRelativeSkeleta)

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

The following construction qotients out the relations encoded by the cells that are thrown in in the above construction, such as to make the maps in the Postnikov tower into [[Kan fibrations]].

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

1. the $n$-[[skeleta]] $sk_n \Delta^k \to \Delta^k \stackrel{f,g}{\to} X$ are equal;

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

## References

Orginal references include

* M.M. Postnikov, _Determination of the homology groups of a space by means of the homotopy invariants_, Doklady Akad. Nauk SSSR (N.S.) 76: 359&#8211;362 (1951)
* George Whitehead, _Elements of homotopy theory_, chapter 9
* Donald W. Kahn, _The spectral sequence of a Postnikov system_, Comm. Math. Helv. 40, n.1, 169--198, 1965 [doi](http://dx.doi.org/10.1007/BF02564370)
* P. I. Booth, _An explicit classification of three-stage Postnikov towers_, Homology, homotopy and applications 8 (2006), No. 2, 133--155
* [[G. J. Ellis]] and R. Mikhailov, _A colimit of classifying spaces_, [arXiv:0804.3581](http://www.arxiv.org/abs/0804.3581).


Probably the earliest treatment of Postnikov systems for simplicial sets is in

* [[John Moore|J. C. Moore]], _Semisimplicial complexes and Postnikov systems_, Symposium Internacional
de Topologia Algebraica, Mexico City, 1958, pp. 232-247,

and as a result, in that context, they are sometimes referred to as **Moore-Postnikov systems**


The coskeleton construction for the Postnikov tower of a Kan complex is already in Artin and Mazur, _&#201;tale homotopy_, (Lecture Notes in Maths. 100). Another 
classical article that amplifies the expression of Postnikov towers in terms of [[coskeleta]] is

* [[William Dwyer]], [[Dan Kan]], _An obstruction theory for diagrams of simplicial sets_ ([pdf](http://www.nd.edu/~wgd/Dvi/ObstructionTheoryForDiagrams.pdf)), from 1984.
 {#DwyerKan}


A standard textbook reference is section 8 of 

* [[Peter May]], _Simplicial methods in algebraic topology_  ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu))

and section VI of 

* [[Paul Goerss]], [[Rick Jardine]], _[[Simplicial homotopy theory]]_
  {#GoerssJardine}


Analogous remarks are also in

*  [[John Duskin]] _Simplicial matrices and the nerves of weak $n$-categories I: Nerves of bicategories_ , TAC **9** no. 2, (2002). ([web](http://www.emis.de/journals/TAC/volumes/9/n10/9-10abs.html))

reviewed around page 302 in 

* [[Tibor Beke]], _Higher &#268;ech theory_, K-Theory, 32(4):293&#8211;322 (2004) ([web](http://www.math.uiuc.edu/K-theory/0646/))
 {#Beke}


A pedagogical introduction to Postnikov systems with an eye towards their $\infty$-[[infinity-groupoid|groupoid]] incarnation under the correspondence given by the [[homotopy hypothesis]] is in

* [[John Baez]], [[Mike Shulman]], _[[Lectures on n-Categories and Cohomology]]_


[[!redirects Postnikov tower]]
[[!redirects Postnikov towers]]

[[!redirects Postnikov decomposition]]
[[!redirects Postnikov systems]]
