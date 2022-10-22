
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Kleisli category
* table of contents
{: toc}

## Idea

Given a [[monad]] $T$ on some [[category]] $\mathcal{C}$, then its _Kleisli category_ is the [[full subcategory]] of the [[Eilenberg-Moore category]] of $T$, hence the category of [[algebras over a monad|T-algebras]], on those that are *[free](algebra+over+a+monad#FreeAlgebras)* [[algebra for a monad|T-algebras]] (free $T$-[[modules]]).

Explicitly one may describe (Prop. \ref{KleisliEquivalence} below) the _Kleisli category_ of $T$ (Def. \ref{KleisliCategory}) to have as [[objects]] the objects of $\mathcal{C}$, and a morphism $X \to Y$ in the Kleisli category is a morphism in $\mathcal{C}$ of the form $X \to T(Y)$ in $\mathcal{C}$. The monad structure induces a natural [[composition]] of such "$T$-shifted" morphisms.


The Kleisli category is also characterized by the following [[universal property]]:

Since every [[adjunction]] gives rise to a [[monad]] on the [[domain]] of its [[left adjoint]], we might ask if every monad may be construed as arising from an adjunction. This is in fact true, and the [[initial object|initial]] such adjunction in the [[adjoint functor#RelationToMonads|category of adjunctions]] for the given monad has the Kleisli category as the codomain of its left adjoint.


## Definition

Let $\mathbf{T} = (T,\mu,\eta)$ be a [[monad]] in [[Cat]], where $T \colon \mathcal{C} \longrightarrow \mathcal{C}$ is an [[endofunctor]] with 

* multiplication $\mu \colon T T \to T$,

* [[unit of a monad|unit]] $\eta \colon Id_C \to T$.


### In terms of free algebras

\begin{definition}\label{FreeTAlgebras}

A __free $\mathbf{T}$-[[algebra|algebra over a monad]]__ (or free $\mathbf{T}$-module) is a $\mathbf{T}$-algebra (module) of the form $(T(M),\mu_M)$, where the [[action]] is the component of multiplication transformation $\mu_M : T(T(M))\to T(M)$. 

\end{definition}


\begin{definition}\label{KleisliCategory}

The __Kleisli category__ $C_{\mathbf{T}}$ of the monad $\mathbf{T}$ is the [[full subcategory]] of the [[Eilenberg-Moore category]] $C^{\mathbf{T}}$ on the free $\mathbf{T}$-algebras (Def. \ref{FreeTAlgebras}).

\end{definition}

+-- {: .num_remark}
###### Remark

If $U:C^{\mathbf{T}}\to C$ is the [[forgetful functor]] and $F: C\to C^{\mathbf{T}}$ is the [[free functor|free algebra functor]] $F: M\mapsto (T M,\mu_M)$, then the Kleisli category is simply the [[full subcategory]] of $C^{\mathbf{T}}$ containing those objects in the image of $F$.

=--


### In terms of Kleisli morphisms
 {#InTermsOfKleisliMorphisms}

As another way of looking at this, we can keep the same objects as in $C$ but redefine the morphisms. This was the original Kleisli construction: 


\begin{definition}\label{KleisliCategory}

The **Kleisli category** $C_{\mathbf{T}}$ of a [[monad]] $T$ on a [[category]] $\mathcal{C}$ has: 

1. as [[objects]] the objects of $\mathcal{C}$, 

1. as [[morphisms]] $M \to N$ the [[morphisms]] of the form 

   \[
     \label{KleisliMorphism}
     M \longrightarrow{\;\;} T(N)
   \] 

   in $\mathcal{C}$, called **Kleisli morphisms**;

and

* [[composition]] of $M \xrightarrow{f} T N$ with $N \xrightarrow{ g } T P$ is given by the **Kleisli composition** rule 

  \[
    \label{KleisliComposition}
    g \circ_{Kleisli} f 
    \;\coloneqq\; 
    \mu_P \circ T(g) \circ f
    \;\colon\;
    M 
      \overset{f}{\longrightarrow} 
    T (N) 
      \overset{T (g)}{\longrightarrow}
    T \big(T (P)\big) 
      \overset{\mu_z}{\longrightarrow}
    T (P)
    \,;
  \]

* the [[identity morphisms]] on $M$ is the Kleisli morphism which is the [[unit of a monad|$T$-unit]] $M \xrightarrow{ \eta_M } T M$.

\end{definition}


\begin{proposition}\label{KleisliEquivalence}

The construction which sends a Kleisli morphism $X \xrightarrow{f} T Y$ (eq:KleisliMorphism) to

$$
  T(X) 
    \overset{T(f)}{\longrightarrow} 
  T^2(Y) 
    \overset{\mu_Y}{\longrightarrow} 
  T(Y)
$$ 

constitutes a [[full and faithful functor]] 

$$
  \mathcal{C}_{T} \longrightarrow \mathcal{C}^{T}
$$

from the $T$-Kleisli category (Def. \ref{KleisliCategory}) to the category of [[algebra over a monad|$T$-algebras]], hence constitutes an [[equivalence of categories]] onto its  [[essential image]] which is that of free $T$-algebras/

\end{proposition}

+-- {: .proof}
###### Proof 

[[full functor|Fullness]] holds because any morphism $g \colon T(X) \to T(Y)$ of algebras has 
as antecedent the composite $X \stackrel{\eta_X}{\to} T(X) \stackrel{g}{\to} T(Y)$.
Indeed, the latter is mapped by the functor into
$\mu_Y \circ T(g) \circ T(\eta_X)$, which because $g$ is a morphism of algebras
is equal to 
$g \circ \mu_X \circ T(\eta_X)$, i.e., $g$.

[[faithful functor|Faithfulness]] holds as follows: if $\mu_Y \circ T(f) = \mu_Y \circ T(g)$,
then precomposing by $\eta_X$ yields $\mu_Y \circ T(f) \circ \eta_X =
\mu_Y \circ \eta_{T(Y)} \circ f = f$ and similarly for $g$, hence $f = g$.
=--

+-- {: .num_remark}
###### Remark

This Kleisli composition plays an important role in [[computer science]]; for this, see the article at [[monad (in computer science)]].

=--


## Properties

### Universal properties
 {#UniversalProperties}



In more general 2-categories the [[universal properties]] of [[Kleisli objects]] are dual to the universal properties of [[Eilenberg-Moore category#Definition|Eilenberg-Moore objects]].

In particular, $C_{\mathbf{T}}$ is [[initial object|initial]] in the [[adjoint functor#RelationToMonads|category of adjunctions]] for $\mathbf{T}$ (whereas $C^{\mathbf{T}}$ is [[terminal objects|terminal]]). For a proof, see _[[Category Theory in Context]]_ Proposition 5.2.12.

### In functional programming

In [[type theory|typed]] [[functional programming]], the Kleisli category is used to model [[call-by-value]] functions with side-effects and [[computation]]. See at _[[monad (in computer science)]]_ for more on this.

## Related concepts

* [[Kleisli object]]

* [[Kleisli 2-category]]

* [[monad (in computer science)]]

* [[co-Kleisli category]]

## References

The original source is

* H. Kleisli, _Every standard construction is induced by a pair of adjoint functors_ , Proc. Amer. Math. Soc. **16** (1965) pp.544&#8211;546. ([AMS](http://www.ams.org/journals/proc/1965-016-03/S0002-9939-1965-0177024-4/))

* Jen&#246; Szigeti, _On limits and colimits in the Kleisli category_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 24 no. 4 (1983), p. 381-391 ([NUMDAM](http://www.numdam.org/item?id=CTGDC_1983__24_4_381_0))

Discussion of cases where the inclusion of the Kleisli category into the [[Eilenberg-Moore category]] is a [[reflective subcategory]] is in

* [[Marcelo Fiore]], [[Matias Menni]], _Reflective Kleisli subcategories of the category of Eilenberg-Moore algebras for factorization monads_, Theory and Applications of Categories, Vol. 15, CT2004, No. 2, pp 40-65. ([TAC](http://www.tac.mta.ca/tac/volumes/15/2/15-02abs.html))

Discussion in [[internal category]] theory is in 

* Tomasz Brzezi&#324;ski, Adrian Vazquez-Marquez, _Internal Kleisli categories_, Journal of Pure and Applied Algebra Volume 215, Issue 9, September 2011, Pages 2135&#8211;2147 ([arXiv:0911.4048](http://arxiv.org/abs/0911.4048))

Discussion of Kleisli categories in [[type theory]] is in 

* [[Alex Simpson]], _Recursive types in Kleisli Categories_ ([pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.47.9679&rep=rep1&type=pdf))

[[!redirects Kleisli category]]
[[!redirects Kleisli categories]]

[[!redirects Kleisli morphism]]
[[!redirects Kleisli function]]
[[!redirects Kleisli morphisms]]
[[!redirects Kleisli functions]]

[[!redirects Kleisli composition]]


[[!redirects Kleisli construction]]
[[!redirects Kleisli constructions]]

