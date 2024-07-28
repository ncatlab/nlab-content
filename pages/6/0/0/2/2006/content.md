
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
      \overset{\mu_P}{\longrightarrow}
    T (P)
    \,;
  \]

* the [[identity morphisms]] on $M$ is the Kleisli morphism which is the [[unit of a monad|$T$-unit]] $M \xrightarrow{ \eta_M } T M$.

\end{definition}


\begin{proposition}\label{KleisliEquivalence}
**([[Kleisli equivalence]])**
\linebreak
The construction which sends a Kleisli morphism $X \xrightarrow{f} T Y$ (eq:KleisliMorphism) to

$$
  T(X) 
    \overset{T(f)}{\longrightarrow} 
  T^2(Y) 
    \overset{\mu_Y}{\longrightarrow} 
  T(Y)
$$ 

constitutes a [[fully faithful functor]] 

$$
  \mathcal{C}_{T} \xhookrightarrow{\phantom{--}} \mathcal{C}^{T}
$$

from the $T$-Kleisli category (Def. \ref{KleisliCategory}) to the category of [[algebra over a monad|$T$-algebras]], hence constitutes an [[equivalence of categories]] onto its  [[essential image]] (the free $T$-algebras).

\begin{tikzcd}[sep=0pt]
    \mathcal{C}_{T}
    \ar[
      rr,
      hook
    ]
    &&
    \mathcal{C}^{T}
    \\
    X 
    &\mapsto&
    \big(
      T(X)
      ,\,
      \mu_X
    \big)
    \\[+5pt]
    \mathcal{C}_{T}
    (X,\, Y)
    \ar[
      rr,
      <->,
      "{ \sim }"
    ]
    &&
    \mathcal{C}^{T}
    \Big(
      \big(T(X),\mu_X\big)
      ,\,
      \big(T(Y),\mu_{Y}\big)
    \Big)
    \\
    \Big(
      X
      \xrightarrow{
        \hspace{22pt}
        f
        \hspace{22pt}
      }
      \mathcal{E}(Y)
    \Big)
    &\mapsto&
    \Big(
      \mathcal{E}(X) 
      \xrightarrow{ \mathcal{E}(f)}
      \mathcal{E}\big(\mathcal{E}(Y)\big)
      \xrightarrow{ \mu_{Y} }
      \mathcal{E}(Y)
    \Big)
    \\
    \Big(
    X
    \xrightarrow{
      \eta^{\mathcal{E}}_{X} 
    }
    \mathcal{E}(X)
    \xrightarrow{ \phi }
    \mathcal{E}(Y)
    \Big)    
    \ar[rr, phantom, "{\mapsto}"{rotate=180}]
    &&
    \Big(
    \mathcal{E}(X)
    \xrightarrow{ 
      \hspace{39pt} 
      \phi 
      \hspace{39pt} 
    }
    \mathcal{E}(Y)
    \Big)
\end{tikzcd}

\end{proposition}

(eg. [Borceux (1994), Prop. 4.1.6](#Borceux94))

\begin{proof}
\label{ProofOfKleisliEquivalence}
To see that the functor is [[full functor|full]], hence that $f \mapsto \mu_Y \circ T(f)$ is [[surjective]], oberve that any homomorphism $g \colon T(X) \to T(Y)$ of [[algebra over a monad|algebras]] is the [[image]] of $X \stackrel{\eta_X}{\to} T(X) \stackrel{g}{\to} T(Y)$, as shown by the following [[commuting diagram]]:

\begin{tikzcd}
  T(X)
  \ar[r, "{ T(\eta_X) }"]
  \ar[dr, equals]
  &
  T T(X)
  \ar[r, "{ T(g) }"]
  \ar[d, "{ \mu_X }"]
  &
  T T(Y)
  \ar[d, "{ \mu_Y }"]
  \\
  &
  T(X) 
  \ar[r, "{ g }"]
  &
  T(Y)
  \mathrlap{\,.}
\end{tikzcd}

Here the triangle on the left is the [[unit law]] of the monad, while the commutativity of the square is the fact that $G$ is a [[homomorphism]] of [[algebra over a monad|algebras]].

To see that the functor is [[faithful functor|faithful]], hence that $f \mapsto \mu_Y \circ T(f)$ is [[injectivity|injective]], notice that

$$
  \big( \mu_Y \circ T(f) \big) \circ \eta_X
  \;=\;
  f
  \,,
$$

by [[naturality square|naturality]] of the [[unit of a monad|unit]] $\eta_X$ combined with its [[unit law]]:

\begin{tikzcd}
  X 
    \ar[r, "{ f }"] 
    \ar[d, "{ \eta_X }"]
  &  
  T(Y)
    \ar[d, "{ \eta_Y }"]
  \ar[dr, equals]
  \\
  T(X)
  \ar[r, "{ T(f) }"{swap}]
  & 
  T T(Y)
  \ar[r, "{ \mu_Y }"{swap}]
  &
  T(Y)
  \mathrlap{\,,}
\end{tikzcd}

whence

$$
  \mu_Y \circ T(f)
  \,=\,
  \mu_Y \circ T(g)
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  \mu_Y \circ T(f) \circ \eta_X
  \,=\,
  \mu_Y \circ T(g) \circ \eta_X
  \;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;
  f \,=\, g
  \,.
$$
\end{proof}

+-- {: .num_remark}
###### Remark

This Kleisli composition plays an important role in [[computer science]]; for this, see the article at [[monad (in computer science)]].

=--




### Two-sided Kleisli category
 {#TwoSidedKleisliCategory}


\begin{proposition}
\label{ExistenceOfTwoSidedKleisliCategory}
If in addition to the given monad $\mathcal{E}$ there is a [[comonad]] $\mathcal{C}$ on the same category $\mathbf{C}$, equipped with a [[distributivity law]] (see [there](distributive+law#ComonadDistributingOverMonad))

$$
  distr^{\mathcal{C}, \mathcal{E}}
  \;\;\colon\;\;
  \mathcal{C}
  \big(
    \mathcal{E}(D)
  \big)
  \longrightarrow
  \mathcal{E}
  \big(
    \mathcal{C}(D)
  \big)
$$

then there is a two-sided ("double") [[Kleisli category]] whose [[objects]] are those of $\mathbf{C}$, and whose morphisms $D_1 \to D_2$ are morphisms in $\mathbf{C}$ of the form
$$
  prog_{12}
  \;\colon\;
  \mathcal{C}(D_1) 
    \longrightarrow 
  \mathcal{E}(D_2)
$$

with two-sided Kelisli composition

$$
  prog_{12} \text{>=>} prog_{23}
  \;\;
  \colon
  \;\;
  \mathcal{C}(D_1)
  \longrightarrow
  \mathcal{E}(D_3)
$$

given by the (co-)[[Kleisli extension|bind-operation]] on the factors connected by the distributivity transformation:

\begin{imagefromfile}
    "file_name": "CoMonKleisliComposition-230930b.pdf",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

\end{proposition}
([Brookes & Van Stone 1993 Thm. 2](#BrookesVanStone93))

\begin{proposition}
\label{MonadTransformationsOnTwoSidedKleisli}
In the situation of Prop. \ref{ExistenceOfTwoSidedKleisliCategory}, given in addition:

1. $\mathcal{E}'$ another monad on $\mathbf{C}$ 

   * also equipped with distributivity $distr^{\mathcal{C}, \mathcal{E}'} \,\colon\, \mathcal{C}\circ \mathcal{E}' \to \mathcal{E}' \circ \mathcal{C}$ over the given comonad $\mathcal{C}$,

1. a [[monad transformer|monad transformation]] $trans^{\mathcal{E} \to \mathcal{E}'} \,\colon\, \mathcal{E} \to \mathcal{E}'$ 

   * which is compatible with the distributive laws in that that 

\begin{tikzcd}
    \mathcal{C}\big(
      \mathcal{E}(-)
    \big)
    \ar[
      dd,
      "{
        \mathrm{distr}
          ^{ \mathcal{C}, \mathcal{E} }
          _{ (-) }
      }"{description}
    ]
    \ar[
      rr,
      "{
        \mathcal{C}\big(
          \mathrm{trans}
            ^{ \mathcal{E} \to \mathcal{E}' }
            _{ (-) }
        \big)
      }"
    ]
    &&
    \mathcal{C}\big(
      \mathcal{E}'(-)
    \big)
    \ar[
      dd,
      "{
        \mathrm{distr}
          ^{ \mathcal{C}, \mathcal{E}' }
          _{ (-) }
      }"{description}
    ]
    \\
    \\
    \mathcal{E}\big(
      \mathcal{C}(-)
    \big)
    \ar[
      rr,
      "{
        \mathrm{trans}
          ^{ \mathcal{E} \to \mathcal{E}' }
          _{ \mathcal{C}(-) }
      }"{swap}
    ]
    &&
    \mathcal{E}'\big(
      \mathcal{C}(-)
    \big)
\end{tikzcd}

then the usual compatibility of the one-sided-Kleisli category under monad transformations (see [here](monad+transformer#eq:RespectForBindOperation)) passes to the two-sided Kleisli category, in that 

\[
  \label{TransformationActingOnTwoSidedKleisliComposition}
  \big(
    trans^{ \mathcal{E} \to \mathcal{E}' }_{D_2}
    \circ 
    prog_{12}
  \big)
  \;\;
  \text{>=>}
  \;\;
  \big(
    trans^{ \mathcal{E} \to \mathcal{E}' }_{D_3}
    \circ 
    prog_{23}
  \big)
  \;\;\;
  =
  \;\;\;
  trans^{ \mathcal{E} \to \mathcal{E}' }_{D_3}
  \circ
  \big(
    prog_{12}
    \;\text{>=>}\;
    prog_{23}
  \big)
  \,.
\]
\end{proposition}
\begin{proof}
Consider the following diagram:

\begin{imagefromfile}
    "file_name": "MonadTransfOnTwoSidedKleisli-290801.jpg",
    "width": 750,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

Here all squares commute by assumption on the monad transformation and hence the entire [[commuting diagram|diagram commutes]]. Now the total top and right composite is the right hand side of (eq:TransformationActingOnTwoSidedKleisliComposition), while the total left and bottom composite is the left hand side of (eq:TransformationActingOnTwoSidedKleisliComposition), thus proving their equality.
\end{proof}

## Properties


### Adjunction

Each Kleisli category comes with an adjunction 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=small,%
]
\mathcal{C} \ar[bend left]{rr}{L} & \perp &  \mathcal{C}_T \ar[bend left]{ll}{R}
\end{tikzcd}

In terms of [[Kleisli morphisms]]:

* The functor $L:\mathcal{C}\to\mathcal{C}_T$ is the identity on objects, and on morphisms it maps $f:X\to Y$ to the Kleisli morphism defined by $\eta_Y\circ f:X\to T Y$, where $\eta$ is the unit of the monad.
* The functor $R:\mathcal{C}_T\to\mathcal{C}$ maps an object $X$ to the object $T X$, and a Kleisli morphism defined by $k:X\to T Y$ to its [[Kleisli extension]] $\mu_Y\circ T k:T X\to T Y$, where $\mu$ is the multiplication of the monad.

In terms of [[algebra over a monad#FreeAlgebras|free algebras]]:

* The functor $L:\mathcal{C}\to\mathcal{C}_T$ maps an object $X$ to the free algebra $(T X,\mu_X)$, where $\mu$ is the multiplication of the monad, and a morphism $f:X\to Y$ to the morphism of algebras $T f: T X\to T Y$.
* The functor $R:\mathcal{C}_T\to\mathcal{C}$ is the forgetful functor mapping free algebras and morphisms of algebras to the underlying objects and morphisms of $\mathcal{C}$.


### Universal properties
 {#UniversalProperties}

In more general 2-categories the [[universal properties]] of [[Kleisli objects]] are dual to the universal properties of [[Eilenberg-Moore category#Definition|Eilenberg-Moore objects]].

In particular, $C_{\mathbf{T}}$ is [[initial object|initial]] in the [[adjoint functor#RelationToMonads|category of adjunctions]] for $\mathbf{T}$ (whereas $C^{\mathbf{T}}$ is [[terminal objects|terminal]]). For a proof, see _[[Category Theory in Context]]_ Proposition 5.2.12.


### Limits and colimits

* By the fact that the functor $L:\mathcal{C}\to\mathcal{C}_T$ is [[left adjoint]], [[left adjoints preserve colimits|it preserves all the colimits]] which exist in $\mathcal{C}$. 

* While $L$, in general, doesn't preserve all [[limits]], one can say the following:

\begin{proposition}\label{Tlim}
 A limit in $\mathcal{C}$ is preserved by $L:\mathcal{C}\to\mathcal{C}_T$ if and only if it is preserved by the monad $T:\mathcal{C}\to\mathcal{C}$.
\end{proposition}

\begin{proof}
Let $D$ be a diagram in $\mathcal{C}$, and suppose its limit exists.

First, suppose that the limit of $D$ is preserved by $L$. Then since $R:\mathcal{C}_T\to\mathcal{C}$ is [[right adjoint]], [[right adjoints preserve limits|it preserves limits]], and so the limit of $D$ is also preserved by $T=R\circ L$.

Conversely, denote by $U:\mathcal{C}^T\to\mathcal{C}$ the [[forgetful functor]] from the [[Eilenberg-Moore category]] of $T$, and denote by $J:\mathcal{C}_T\to\mathcal{C}^T$ the [[comparison functor]]. We have that $R:\mathcal{C}_T\to\mathcal{C}$ factors as $U\circ J$, and so $T=U\circ J\circ L$. 
Now suppose that the limit of $D$ is preserved by $T=U\circ J\circ L$. Since $U$ is [[monadic functor|monadic]] and [[created limit#examples|monadic functors create limits]], the limit is also preserved by the functor $J\circ L:\mathcal{C}\to\mathcal{C}^T$. 
Now since $J$ is a full inclusion, and [[reflected limit#Examples|full inclusions reflect limits]], the limit is also preserved by the functor $L:\mathcal{C}\to\mathcal{C}_T$ alone.
\end{proof}


## Examples

### General

\begin{example}\label{CallByValueProgramming}
In [[type theory|typed]] [[functional programming]], the Kleisli category is used to model [[call-by-value]] functions with [[side effects]] and [[computation]]. 
Dually, the [[co-Kleisli category]] of a [[comonad]] may be used to model [[call-by-name]] programming , see [there](Kleisli+category+of+a+comonad#CallByNameProgramming).

Generally, see at _[[monad (in computer science)]]_ for more on this.
\end{example}

### Specific

\begin{example}
**([[matrix multiplication]] as (co-)Kleisli composition)**
\linebreak
See [here](Kleisli+category+of+a+comonad#MatrixmultiplicationAsCoKleisliComposition).
\end{example}

## Related concepts

* [[Kleisli triple]]

* [[co-Kleisli category]]

* [[Kleisli object]]

* [[extension system]] 

* [[monad in computer science]]

* [[Kleisli 2-category]]

* [[thunk-force category]]



## References

The original articles:

* {#Kleisli65} [[Heinrich Kleisli]], *Every standard construction is induced by a pair of adjoint functors*, Proc. Amer. Math. Soc. **16**, AMS (1965) 544-546 &lbrack;[ISSN0002-9939](http://www.ams.org/journals/proc/1965-016-03/S0002-9939-1965-0177024-4/), [jstor:2034693](https://www.jstor.org/stable/2034693)&rbrack;

* {#Maranda66} [[Jean-Marie Maranda]], *On Fundamental Constructions and Adjoint Functors*, Canadian Mathematical Bulletin **9** 5  (1966) 581-591 &lbrack;[doi:10.4153/CMB-1966-072-9](https://doi.org/10.4153/CMB-1966-072-9)&rbrack;

Early accounts (together with the [[Eilenberg-Moore category]]):

* [[Fred Linton]], §7 in: *An outline of functorial semantics*, in *[[Seminar on Triples and Categorical Homology Theory]]*, Lecture Notes in Mathematics **80**, Springer (1969) 7-52 &lbrack;[doi:10.1007/BFb0083080](https://doi.org/10.1007/BFb0083080)&rbrack;

* {#MacLane71} [[Saunders MacLane]], §VI.5 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5**  Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* [[Michael Barr]], [[Charles Wells]], §3.2 of: *[[Toposes, Triples, and Theories]]*, Grundlehren der math. Wissenschaften **278**, Springer (1983) &lbrack;[TAC:12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)&rbrack;

* Jen&#246; Szigeti, _On limits and colimits in the Kleisli category_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques **24** 4 (1983) 381-391 &lbrack;[numdam:CTGDC_1983__24_4_381_0](http://www.numdam.org/item?id=CTGDC_1983__24_4_381_0)&rbrack;


The [[equivalence of categories]] between the [[Kleisli category]] over a given [[monad]] with the [[co-Kleisli category]] of an [[adjoint functor|adjoint]] [[comonad]] (if it exists):

* [[Mark Kleiner]],  *Adjoint monads and an isomorphism of the Kleisli categories*, Journal of Algebra **133** 1 (1990) 79-82 &lbrack;<a href="https://doi.org/10.1016/0021-8693(90)90069-Z">doi:10.1016/0021-8693(90)90069-Z</a>&rbrack;

The terminology "[[Kleisli triple]]" for a [[monad]] presented as an "[[extension system]]" and relation to [[computation]] with effects (see at *[[monads in computer science]]*):

* {#Moggi91} [[Eugenio Moggi]], *Notions of computation and monads*, Information and Computation, **93** 1 (1991) &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90052-4">doi:10.1016/0890-5401(91)90052-4</a>, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf)&rbrack;

Textbook account making explicit the [[Kleisli equivalence]]:

* {#Borceux94} [[Francis Borceux]], pp. 191 in: *[[Handbook of Categorical Algebra]]*, Vol 2 *Categories and Structures*, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865)&rbrack;


Lecture notes:

* [[Thomas Streicher]], pp. 54 in: *Introduction to Category Theory and Categorical Logic* (2003) &lbrack;[pdf](https://www2.mathematik.tu-darmstadt.de/~streicher/CTCL.pdf), [[Streicher-CategoryTheory.pdf:file]]&rbrack;


Discussion of cases where the inclusion of the Kleisli category into the [[Eilenberg-Moore category]] is a [[reflective subcategory]]:

* [[Marcelo Fiore]], [[Matias Menni]], _Reflective Kleisli subcategories of the category of Eilenberg-Moore algebras for factorization monads_, Theory and Applications of Categories, Vol. 15, CT2004, No. 2, pp 40-65. ([TAC](http://www.tac.mta.ca/tac/volumes/15/2/15-02abs.html))

{#TwoSidedReferences} Discussion of combined "double" or "two-sided" Kleisli categories, combining the Kleisli category of a [[monad]] with the [[co-Kleisli category]] of a [[comonad]] that [[distributive law|distributes]] over it:

* {#BrookesVanStone93} [[Stephen Brookes]],  [[Kathryn Van Stone]], *Monads and Comonads in Intensional Semantics* (1993) &lbrack;[dtic:ADA266522](https://apps.dtic.mil/sti/citations/ADA266522), [pdf](https://www.cs.cmu.edu/~brookes/papers/MonadsComonads.pdf), [[BrookesVanStone-CoMonads.pdf:file]]&rbrack;

and generalization to [[2-monads]]:

* {#Garner08} [[Richard Garner]], pp. 11 of: *Polycategories via pseudo-distributive laws*, Advances in Mathematics **218** 3 (2008) 781-827 &lbrack;[arXiv:0606735](https://arxiv.org/abs/math/0606735), [doi:10.1016/j.aim.2008.02.001](https://doi.org/10.1016/j.aim.2008.02.001)&rbrack;


Discussion in [[internal category]] theory:

* Tomasz Brzezi&#324;ski, Adrian Vazquez-Marquez, _Internal Kleisli categories_, Journal of Pure and Applied Algebra **215** 9 (2011) 213-147 &lbrack;[arXiv:0911.4048](http://arxiv.org/abs/0911.4048)&rbrack;

Discussion in a context of [[categorical systems theory]]:


* {#MyersBook} [[David Jaz Myers]], §2.3 of: *Categorical systems theory*, book project &lbrack;[github](https://github.com/DavidJaz/DynamicalSystemsBook/tree/master/book), [pdf](http://davidjaz.com/Papers/DynamicalBook.pdf)&rbrack;


Discussion of Kleisli categories in [[type theory]] is in 

* [[Alex Simpson]], _Recursive types in Kleisli Categories_ ([pdf](https://www.research.ed.ac.uk/en/publications/recursive-types-in-kleisli-categories))

[[!redirects Kleisli category]]
[[!redirects Kleisli categories]]

[[!redirects Kleisli morphism]]
[[!redirects Kleisli function]]
[[!redirects Kleisli map]]

[[!redirects Kleisli morphisms]]
[[!redirects Kleisli functions]]
[[!redirects Kleisli maps]]

[[!redirects Kleisli composition]]
[[!redirects Kleisli compositions]]

[[!redirects Kleisli composite]]
[[!redirects Kleisli composites]]

[[!redirects Kleisli construction]]
[[!redirects Kleisli constructions]]


[[!redirects Kleisli equivalence]]

