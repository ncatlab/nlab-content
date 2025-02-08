
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A _relative_ monad $T \colon A \to E$ is much like a [[monad]] except that its underlying functor is not required to be an [[endofunctor]]: rather, it can be an arbitrary functor between categories. To even formulate such a notion, (for instance the definition of the [[unit]]), the two categories have to be related somehow, typically via a specified comparison functor $J \colon A \to E$, in which case we say that $T$ is a monad *relative to* $J$. 

Ordinary monads are the special case of $J$-relative monads where $J$ is the [[identity functor]].

In generalisation of the [relation between adjunctions and monads](monad#RelationBetweenAdjunctionsAndMonads), relative monads are related to [[relative adjunctions]]. Dually, [[relative comonads]] are related to [[relative coadjunctions]].


## Definitions
 {#Definition}

Let $J \colon A \to E$ be a functor between categories, the **root**.

## In extension form

The following definition is a variation of the formulation of a [[monad in extension form]]:

\begin{definition}
\label{def}
A **$J$-relative monad $T$** &lbrack;[ACU15, Def. 2.1](#ACU15)&rbrack; comprises:

- a function $T \colon |A| \to |E|$, the **underlying functor**;

- for each object $X \in |A|$, a morphism $\eta_X \colon J X \to T X$ in $E$, the **unit**;

- for each morphism $f \colon J X \to T Y$ in $E$, a morphism $f^\dagger \colon T X \to T Y$ in $E$, the **extension operator**,

such that, for each $X, Y, Z \in |A|$, the following equations hold:

- $f = f^\dagger \circ \eta_X$ for each $f \colon J X \to T Y$ (**left unitality**);

- $(\eta_X)^\dagger = 1_{T X}$ (**right unitality**);

- $(g^\dagger \circ f)^\dagger = \g^\dagger \circ f^\dagger$ for each $f \colon J X \to T Y$ and $g \colon J Y \to T Z$.

\end{definition}

It follows that $T$ is canonically equipped with the structure of a [[functor]]. For each $f \colon X \to Y$ in $A$:
\[
  T f 
  \;:=\; 
  \big(
    \eta_{Y} \circ J f
  \big)^\dagger
  \,. 
\]
and that the unit $\eta$ and the extension operator $({-})^\dagger$ are then [[natural transformations]].

In particular, in the special case that $J$ is the [[identity functor]], Def. \ref{def} reduces to the definition of [[monad in extension form]].

### As monoids in a skew-monoidal category, skew-multicategory, or multicategory

Monads are, by definition, [[monoids]] in [[monoidal categories]] of [[endofunctors]]. It is similarly possible to present relative monads as monoids in categories of [[functors]]. However, generally speaking, arbitrary functor categories are not monoidal. However, given a fixed functor $J \colon A \to E$, the functor category $[A, E]$ may frequently be equipped with [[skew-monoidal category|skew-monoidal]] structure. The notion of a *[[skew-monoidal category]]* is like that of a [[monoidal category]] except that the [[unitors]] and [[associators]] are not necessarily [[invertible morphism|invertible]]. [[monoid|Monoids]] may be defined in a [[skew-monoidal category]] analogously as to in a [[monoidal category]], and a monoid in $[A, E]$ (equipped with the skew-monoidal structure induced by $J$) is precisely a $J$-relative monad.

\begin{theorem}
**([ACU15, Thm. 3.4](#ACU15))**
\linebreak
Let $J \colon A \to E$ be a functor for which $\mathrm{Lan}_J \colon [A, E] \to [E, E]$ exists (e.g. if $A$ is small and $E$ cocomplete).
Then $[A, E]$ admtis a skew-monoidal structure, with unit $J$ and tensor $F \circ^J G = (\mathrm{Lan}_J F) \circ G$, and a relative monad is precisely a monoid in $([A, E], J, \circ^J)$.
\end{theorem}

When $J \colon A \to E$ is a free completion of $A$ under a class $\mathcal{F}$ of small colimits, then this skew-monoidal structure on $[A, E]$ is properly monoidal, since it is equivalent to the $\mathcal{F}$-colimit preserving functors $E \to E$, and the monoidal structure is just functor composition.

More generally, if $\mathrm{Lan}_J$ does not exist, we may still define a [[skew-multicategory]] structure on $[A, E]$. Thus, relative monads are always monoids.

\begin{theorem}
**([AM, Thm. 4.16](#AM24))**
\linebreak
Let $J \colon A \to E$ be a functor.
Then $[A, E]$ admits a unital skew-multicategory structure, and a relative monad is precisely a monoid therein.
\end{theorem}

This skew-multicategory structure is [[representable multicategory|representable]] just when $\mathrm{Lan}_J$ exists, recovering the result of [ACU15](#ACU15). When $J$ is a [[dense functor]], the above theorem simplifies.

\begin{theorem}
**([AM, Cor. 4.17](#AM24))**
\linebreak
Let $J \colon A \to E$ be a [[dense functor]].
Then $[A, E]$ admits a unital multicategory structure, and a relative monad is precisely a monoid therein.
\end{theorem}

### As monads in the bicategory of distributors

An alternative useful perspective on relative monads is the following.

\begin{theorem}
**([AM, Thm. 4.22](#AM24))**
\linebreak
Let $J \colon A \to E$ be a [[dense functor]].
A $J$-relative monad is precisely a [[monad]] in the [[bicategory]] of [[distributors]] whose underlying 1-cell is of the form $E(J, T)$ for some functor $T \colon A \to E$.
\end{theorem}

### Relative to a distributor

The above definition makes sense even more generally when $J$ is a [[distributor]] $E &#8696; A$, i.e. a functor $\mathbf A^{op} \times E \to Set$. Explicitly, we ask for:

- a functor $T \colon A \to E$;

- a unit $\eta_X \in J(X, T X)$ for each $X \in |A|$, [[natural transformation|natural]] in $X \in |A|$ (equivalently, an element of the [[end]], $\eta \in \int_{X \in |A|}J(X, T X)$);

- an extension operator $(-)^\dagger \colon J(X, T Y) \to \mathbf C(T X, T Y)$ natural in $X,Y \in |A|$

with essentially the same equations. We recover the previous definition by taking the corepresentable distributor $E(J-,=)$. See Remark 4.24 of [AM24](#AM24).

## Examples

### Generic examples

\begin{example}
\label{RelativeMonadsInducedByPrecomposition}
**(relative monads induced from actual monads)**
\linebreak
Given 

* a [[functor]] 
 
  $J \,\colon\, A \to E$,

* a $\;$ [[monad]] 

  $T \,\colon\, E \to E$ 

  with 

  * unit $\;$  $\eta^T_{(-)}$

  * extension operator $\;$ $bind^T$

the composite

* $T \circ J \,\colon\, A \to E$

defines a $A$-relative monad (Def. \ref{def}) with

* unit 

  $\eta^{T J}_X \,\coloneqq\, \eta^T_{J(X)}$

* extension operator

  $
    bind^{T J}\big( J(X) \overset{k}{\to} T \circ J(Y) \big) 
      \;\coloneqq\;
    bind^T\big( J(X) \overset{k}{\to} T \circ J(Y) \big)
    \,.
  $

\end{example}

This example is stated in [ACU15, Prop. 2.3 (1)](#ACU15). More generally, we can precompose any relative monad with a functor to obtain a new relative monad: see Proposition 5.36 of [AM24](#AM24).

\begin{proof}
The required conditions on the relative monad structure $T \circ J$ immediately reduce to those of the monad structure of $T$:

Given

$$
  k \,\colon\, J(X) \to T \circ J(X')
  ,\;\;\;
  \ell \,\colon\, J(X') \to T \circ J(X'')
$$

we have

left unitality:

$$
  \begin{array}{l}
    bind^{T J}(k) \circ \eta^{T J}_{X}
    \\
    \;\equiv\;
    bind^T(k) \circ \eta^T_{J(X)}
    \\
    \;=\;
    k
  \end{array}
$$

right unitality:

$$
  \begin{array}{l}
    bind^{T J}\big(
      \eta^{T J}_{X}
    \big)
    \\
    \;\equiv\;
    bind^T\big(
      \eta^T_{J (X)}
    \big)
    \\
    \;=\;
    id_{T \circ J(X)}
  \end{array}
$$

associativity:

$$
  \begin{array}{l}
    bind^{T J}\big(
      bind^{T J}(\ell)
      \circ 
      k
    \big)
    \\
    \;\equiv\;
    bind^{T}\big(
      bind^{T}(\ell)
      \circ 
      k
    \big)
    \\
    \;=\;
    bind^T(\ell) \circ bind^T(k)
    \\
    \;\equiv\;
    bind^{T J}(\ell) \circ bind^{T J}(k)    
  \end{array}
$$

\end{proof}

A concrete instance of Exp. \ref{RelativeMonadsFromActualMonads} is spelled out in Exp. \ref{LinearSpan} below.

\begin{example}
A relative monad on the embedding $J \colon \mathbf{FinSet} \to \mathbf {Set}$ is equivalent to an [[abstract clone]]. These are equivalent to [[finitary monads]] and single-sorted [[algebraic theories]]. 
\end{example}

\begin{example}
Fixing a category $\mathbb{V}$ with [[finite products]], to give a [[Freyd category]] is to give a strong relative monad on the [[Yoneda embedding]] $\mathbb{V}\to [\mathbb{V}^{\mathrm{op}},\mathbf{Set}]$. 
\end{example}

\begin{example}
The [[presheaf category]]-construction $(\mathbb{C}\mapsto [{\mathbb{C}}^{\mathrm{op}},\mathbf{Set}])$ may be regarded as a [[relative pseudomonad]] on the inclusion $\mathbf{Cat}\to \mathbf{CAT}$. (See also *[[Yoneda structures]]*.)
\end{example}

\begin{example}
A [[monad with arities|monad on $\mathbf C$ with arities in $A\subseteq \mathbf C$]] is the same thing as a relative monad for the embedding $A\to \mathbf C$. (Here $A\subseteq E$ is required to be a [[dense subcategory]], so that to give a functor $A\subseteq E$ is to give a functor $E\toE$ preserving $J$-absolute colimits.)
\end{example}

### Specific examples

\begin{example}\label{LinearSpan}
**([[linear span]])**
\linebreak
We spell out the simple but maybe instructive example of the construction which sends a [[set]] $B$ to the [[vector space]] which it [[linear span|spans]], i.e. to the $B$-[[indexed set|indexed]] [[direct sum]] of some [[ground field]] $\mathbb{K}$, regarded in $\mathbb{K}$-[[vector spaces]].

In detail,
for $\mathbb{K}$ any [[ground field]], consider:

1. $A \coloneqq $ [[Set]];

1. $E \coloneqq \int_{B \colon Set} Vect_B$ (or "[[VectBund]]", for short, see there for more) the [[category]] of [[indexed sets]] of [[vector spaces]] -- hence of [[vector bundles]] over [[sets]] (i.e. over [[discrete topological spaces]])

   $$
     \array{
       \mathscr{H}
       \\
       \big\downarrow
       \\
       B
     }
   $$


   with possibly base-changing vector bundle [[maps]] between them: 


   $$
     \array{
       \mathscr{H}
       &\longrightarrow&
       \mathscr{H}'
       \\
       \big\downarrow
       &&
       \big\downarrow
       \\
       B
       &\underset{f}{\longrightarrow}&
       B'
     }
   $$

1. the relativization functor given by sending a set to the [[trivial bundle|trivial]] [[tensor unit]]-bundle over it:

   \[
     \label{FormingTrivialTensorUnitBundle}
     \array{
       J 
       &\colon&
       Set
       &\longrightarrow&
       \int_{B \colon Set} Vect_B
       \\
       &&
       B
       &\mapsto&
       B \times \mathbb{K}
     }
   \]

Notice that for each [[map]] $f \;\colon\; B \to B'$ of base sets, there is a [[base change]] [[adjoint triple]] of functors 

\[
  \label{BaseChangeForIndexedSetsOfVectorBundles}
  f_! \dashv f^\ast \dashv f_\ast
  \;\;\colon\;\;
  Vect_{B}
  \leftrightarrow
  Vect_{B'}
  \,.
\]

In particular, for $S' = \ast$ the [[terminal object|terminal]] [[singleton set]], the left base change along the unique $p_X \colon S \to \ast$ is the operation which forms the [[direct sum]] of the ([[fiber]]-)vector spaces in the bundle, and regards the resulting [[vector space]] as a bundle over the point:

$$
  (p_B)_! 
  \;\colon\;
  Vect_B 
    \longrightarrow 
  Vect_\ast \,=\, Vect
  \,.
$$

In view of this, we claim that the functor   

$$
  \array{
    Q
    &\colon&
    Set
    &\longrightarrow&
    \int_{B \colon Set} Vect_{B}
    \\
    &&
    S
    &\mapsto&
    (p_B)_!\big( B \times \mathbb{K} \big)
    \mathrlap{
      \;\simeq\;
      \underset{b \colon B}{\bigoplus} \mathbb{K}
    }
  }
$$

which may be understood as sending a [[set]] to its $\mathbb{K}$-[[linear span]],

carries the structure of a monad relative to the functor $J$ from (eq:FormingTrivialTensorUnitBundle) with

1. [[unit of a monad|unit]] given by

   $$
     \array{
       \eta_{B}
       &\colon&
       B \times \mathbb{K}
       &\longrightarrow&
       \underset{b \colon B}{\bigoplus} \mathbb{K}
       \\
       &&
       (b,k) &\mapsto& (k)_b
     }
   $$

1. [[extension system|Kleisli extension]] given by

   $$
     \Big(
       B \times \mathbb{K} 
         \xrightarrow{f}
       \underset{
         \mathclap{b' \colon B'}
       }{\oplus} \mathbb{K}
     \Big)
     \;\;\;\;\mapsto\;\;\;\;
     \Big(
       \underset{b \colon B}{\oplus} \mathbb{K}     
       \xrightarrow{
         \big( 
           f(b,-) 
         \big)_{b \colon B}
       }
       \underset{b' \colon B}{\oplus} \mathbb{K}     
     \Big)
   $$

This specific example may be understood as a special case of the general situation of relative monads induced from an actual monad (Exmp. \ref{RelativeMonadsInducedByPrecomposition}): Here the actual monad in question is:

$$
  \array{
    \triangle
    &\colon&
    \int_{B \colon Set} Vect_B
    &\longrightarrow&
    \int_{B \colon Set} Vect_B
    \\
    &&
    \left[ 
      \array{
        \mathscr{V} 
        \\ 
        \big\downarrow\mathrlap{{}^p} 
        \\ 
        B
      } 
      \;\;\;
    \right] 
    &\mapsto& 
    p_! \mathscr{V} 
  }
$$

This monad is in fact the [[reflective localization]] of the [[reflective subcategory]]-embedding of plain [[VectorSpaces]] into bundled/parameterized vector spaces:

$$
  Vect
  \;\simeq\;
  Vect_\ast
  \xhookrightarrow{\phantom{--}}
  \int_{B \colon Set} Vect_B
  \,.
$$

\end{example}

## Related pages

* [[relative adjunction]]

* [[relative comonad]]

* [[extension system]], [[Kleisli triple]], [[monad in computer science]]

* [[relative pseudomonad]]

* [[polymonad]]

## References

The concept was introduced, in the context of [[monads in computer science]], in: 

* {#ACU15} [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;

A comprehension development in the context of [[formal category theory]] may be found in:

* {#AM24} [[Nathanael Arkor]], [[Dylan McDermott]], _The formal theory of relative monads_, Journal of Pure and Applied Algebra 107676. (2024) &lbrack;[arXiv:2302.14014](https://arxiv.org/abs/2302.14014),  doi:[10.1016/j.jpaa.2024.107676](https://doi.org/10.1016/j.jpaa.2024.107676)&rbrack;

* [[Nathanael Arkor]], [[Dylan McDermott]], _Relative monadicity_, 2023. &lbrack;[arXiv:2305.10405](https://arxiv.org/abs/2305.10405)&rbrack;

* [[Nathanael Arkor]], [[Dylan McDermott]], _The pullback theorem for relative monads_ (2024) &lbrack;[arXiv:2404.01281](https://arxiv.org/abs/2404.01281)&rbrack;

Exposition:

* [[Nathanael Arkor]], *Relative monads and their many guises*, talk at *[[Category Theory Octoberfest]]* [2022](https://richardblute.ca/octoberfest-2022/) &lbrack;slides:[pdf](https://richardblute.files.wordpress.com/2022/10/arkor-ofest.pdf), video:[mp4](https://richardblute.files.wordpress.com/2022/10/arkor-ofest-1.mp4)&rbrack;

On [[distributive laws]] for relative monads:

* [[Gabriele Lobbia]], *Distributive Laws for Relative Monads*, Applied Categorical Structures **31** 19 (2023)  &lbrack;[doi:10.1007/s10485-023-09716-1](https://doi.org/10.1007/s10485-023-09716-1), [arXiv:2007.12982](https://arxiv.org/abs/2007.12982)&rbrack;

[[!redirects relative monads]]

