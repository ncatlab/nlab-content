
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

A _relative_ monad $T \colon \mathbf J \to \mathbf C$ is much like a [[monad]] except that it is not an [[endofunctor]] on one [[category]], but more generally a functor between two different categories. To even formulate such a notion, (for instance the definition of the [[unit]]), the two categories have to be related somehow, typically via a specified comparison functor $J \colon \mathbf J \to \mathbf C$, in which case we say that $T$ is a monad *relative to* $J$. 

Ordinary monads are then the special case of $J$-relative monads where $J$ is the [[identity functor]].

In generalization of the [relation between adjunctions and monads](monad#RelationBetweenAdjunctionsAndMonads), relative monads are related to [[relative adjunctions]].


## Definitions
 {#Definition}

Let 

* $\mathbf J, \mathbf C$ be [[categories]] 

* $J \,\colon\, \mathbf J \to \mathbf C$ a [[functor]].


### As skew Kleisi triples
 {#AsSkewKleisliTriples}

The following definition is a variation of the [[Kleisli triple]]-formulation of ordinary [[monads]]:

\begin{definition}
\label{def}
A **relative monad $T$ on $J$** is 

* a [[functor]] $T \,\colon\, \mathbf J \to \mathbf C$ 

equipped with

1. a *$J$-relative [[unit of a monad|unit]]* 

   $\eta_X \,\colon\, J X \to T X$ 

   [[natural transformation|natural]] in $X \colon \mathbf J$,

1. a *$J$-relative [[Kleisli extension]]*

   $(-)^* \colon \mathbf{C}(J X, T Y) \to \mathbf{C}(T X, T Y)$ 

   natural in both $X, Y \colon \mathbf J$

such that for $X, Y, Z \colon \mathbf J$ and $k \colon J X \to T Y$ the following [[equations]] hold:

1. (*left [[unitality]]*) 

   $k = k^* \circ \eta_X \;,$

1. (*right [[unitality]]*) 

   $\eta_X^* = 1_{T X} \;,$

1. (*[[associativity]]*) 

   $(\ell^* \circ k)^* = \ell^* \circ k^*$ 

   for every $k \colon J X \to T Y$ and $\ell \colon J Y \to T Z$.

\end{definition}
&lbrack;[ACU14, Def. 2.1](#ACU14)&rbrack;

Notice that for any $f \colon X \to Y$ in $\mathbf J$, one has
\[
  T f 
  \;=\; 
  \big(
    \eta_{J Y} \circ J f
  \big)^*
  \,. 
\]


\begin{example}
**(ordinary [[monads]] as [[Kleisli triples]]/[[extension systems]])**
\linebreak
In the special case that $\mathbf{J} = \mathbf{C}$ and $J = id$ the [[identity functor]], Def. \ref{def} reduces to the definition of ordinary [[monads]], but in the guise known as "[[Kleisli triples]]" or "[[extension systems]]" which is nominally different from (though equivalent to) the way monads are traditionally presented in [[category theory]]/[[categorical algebra]] (namely as [[monoid objects]] [[internalization|internal to]] a [[functor category|category of]] [[endofunctors]]), but is exactly the form commonly used for [[monads in computer science]].
\end{example}


### As monoids in a skew-monoidal category

The notion of a *[[skew-monoidal category]]* is like that of a [[monoidal category]] except that the [[unitors]] and [[associators]] are not necessarily [[invertible morphism|invertible]]. [[monoid|Monoids]] may be defined in a [[skew-monoidal category]] analogously as to in a [[monoidal category]].

In the general case that $\mathbf{J}$ is distinct from $\mathbf{C}$,  the [[functor category]] $Func(\mathbf J, \mathbf C)$ lacks a natural [[monoidal category]] [[structure]] (as opposed to the case of [[endofunctors]] $Func(\mathbf{C}, \mathbf{C})$) so that the usual definition of [[monads]] as [[monoids]] cannot apply --- but a suitable "skew" variant works:


The (skew-)[[composition]] of [[functors]] $F,G \colon \mathbf J \to \mathbf C$ may be defined by first [[left Kan extension|extending]] $F$ along $J$ and then composing with $G$. The resulting composition product on $[\mathbf J, \mathbf C]$ is [[coherence|coherent]] but only [[lax natural transformation|laxly]] so, hence the need to appeal to skew-monoidal categories:

\begin{theorem}
**([ACU14, Thm. 3.4](#ACU14))**
\linebreak
Suppose $J \colon \mathbf J \to \mathbf C$ is such that $\mathrm{Lan}_J \colon [\mathbf J, \mathbf C] \to [\mathbf C, \mathbf C]$ exists (e.g. if $\mathbf J$ is small and $\mathbf C$ cocomplete).
Then $[\mathbf J, \mathbf C]$ is skew-monoidal, with unit $J$ and product $F \circ^J G = (\mathrm{Lan}_J F) \circ G$, and a relative monad is a monoid in $([\mathbf J, \mathbf C], J, \circ^J)$.
\end{theorem}

When $J:\mathbf J \to \mathbf C$ is a free completion of $\mathbf{J}$ under colimits from some set $\mathcal{F}$ of indexing types, then this skew-monoidal structure on $[\mathbf J, \mathbf C]$ is properly monoidal, since it is equivalent to the $\mathcal{F}$-colimit preserving functors $\mathbf C\to\mathbf C$, and the monoidal structure is just functor composition. 

### Relative to a Profunctor

The above definition makes sense even more generally when $J$ is a [[profunctor]] $\mathbf J^{op} \times \mathbf {C} \to Set$, i.e., we require

1.  a unit $\eta_X \colon J(X, T X)$, a [[natural transformation|natural]] in $X \colon \mathbf J$, that is an element of the [[end]], $\eta \in \int_{X: \mathbf J}J(X, T X)$

2.  a _[[extension system|Kleisli extension]]_ $(-)^* \colon J(X, T Y) \to \mathbf C(T X, T Y)$ natural in both $X,Y \colon \mathbf J$

with essentially the same equations. This generalizes the previous definition by defining the profunctor to be $\mathbf C(J-,=)$.

## Examples

### Generic examples

\begin{example}
\label{RelativeMonadsInducedFromActualMonads}
**(relative monads induced from actual monads)**
\linebreak
Given 

* a [[functor]] 
 
  $J \,\colon\, \mathbf{J} \to \mathbf{C}$,

* an actual$\;$ [[monad]] 

  $T \,\colon\, \mathbf{C} \to \mathbf{C}$ 

  with 

  * [[unit of a monad|unit]]$\;$  $\eta^T_{(-)}$

  * [[Kleisli extension]]$\;$ $bind^T$

the composite

* $T \circ J \,\colon\, \mathbf{J} \to \mathbf{C}$

becomes a $\mathbf{J}$-relative monad (Def. \ref{def}) with

* relative unit 

  $\eta^{T J}_X \,\coloneqq\, \eta^T_{J(X)}$

* relative Kleisli extension

  $
    bind^{T J}\big( J(X) \overset{k}{\to} T \circ J(Y) \big) 
      \;\coloneqq\;
    bind^T\big( J(X) \overset{k}{\to} T \circ J(Y) \big)
    \,.
  $

\end{example}
This example is stated in [ACU14, Prop. 2.3 (1)](#ACU14).
\begin{proof}
The required conditions on the relative Kleisli structure of $T \circ J$ immediately reduce to those of the actual Kleisli structure of $T$:

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
A relative monad on the embedding $J \colon \mathbf{FinSet} \to \mathbf {Set}$ is the same thing as an [[abstract clone]]. These are equivalent to [[finitary monads]] and single-sorted [[algebraic theories]]. 
\end{example}


\begin{example}
Fixing a category $\mathbb{V}$ with [[finite products]], to give a [[Freyd category]] is to give a strong relative monad on the [[Yoneda embedding]] $\mathbb{V}\to [\mathbb{V}^{\mathrm{op}},\mathbf{Set}]$. 
\end{example}

\begin{example}
The [[presheaf category]]-construction $(\mathbb{C}\mapsto [{\mathbb{C}}^{\mathrm{op}},\mathbf{Set}])$ may be regarded as a [[relative pseudomonad]] on the inclusion $\mathbf{Cat}\to \mathbf{CAT}$. (See also *[[Yoneda structures]]*.)
\end{example}

\begin{example}
A [[monad with arities|monad on $\mathbf C$ with arities in $\mathbf{J}\subseteq \mathbf C$]] is the same thing as a relative monad for the embedding $\mathbf{J}\to \mathbf C$. (Here $\mathbf{J}\subseteq \mathbf{C}$ is required to be a [[dense subcategory]], so that to give a functor $\mathbf{J}\subseteq \mathbf{C}$ is to give a functor $\mathbf{C}\to\mathbf{C}$ preserving $J$-absolute colimits.)
\end{example}

### Specific examples


\begin{example}\label{LinearSpan}
**([[linear span]])**
\linebreak
We spell out the simple but maybe instructive example of the construction which sends a [[set]] $B$ to the [[vector space]] which it [[linear span|spans]], i.e. to the $B$-[[indexed set|indexed]] [[direct sum]] of some [[ground field]] $\mathbb{K}$, regarded in $\mathbb{K}$-[[vector spaces]].

In detail,
for $\mathbb{K}$ any [[ground field]], consider:

1. $\mathbf{J} \coloneqq $ [[Set]];

1. $\mathbf{C} \coloneqq \int_{B \colon Set} Vect_B$ (or "[[VectBund]]", for short, see there for more) the [[category]] of [[indexed sets]] of [[vector spaces]] -- hence of [[vector bundles]] over [[sets]] (i.e. over [[discrete topological spaces]])

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

This specific example may be understood as a special case of the general situation of relative monads induced from an actual monad (Exmp. \ref{RelativeMonadsInducedFromActualMonads}): Here the actual monad in question is:

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

* [[polymonad]]

## References

The concept was introduced, in the context of [[monads in computer science]], in: 

* {#ACU14} [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;

Abstract discussion via [[virtual equipments]]:

* [[Nathanael Arkor]], [[Dylan McDermott]], _The formal theory of relative monads_, 2023. &lbrack;[arXiv:2302.14014](https://arxiv.org/abs/2302.14014)&rbrack;

* [[Nathanael Arkor]], [[Dylan McDermott]], _Relative monadicity_, 2023. &lbrack;[arXiv:2305.10405](https://arxiv.org/abs/2305.10405)&rbrack;

Exposition:

* [[Nathanael Arkor]], *Relative monads and their many guises*, talk at *[[Category Theory Octoberfest]]* [2022](https://richardblute.ca/octoberfest-2022/) &lbrack;slides:[pdf](https://richardblute.files.wordpress.com/2022/10/arkor-ofest.pdf), video:[mp4](https://richardblute.files.wordpress.com/2022/10/arkor-ofest-1.mp4)&rbrack;

On [[distributive laws]] for relative monads:

* [[Gabriele Lobbia]], *Distributive Laws for Relative Monads*, Applied Categorical Structures **31** 19 (2023)  &lbrack;[doi:10.1007/s10485-023-09716-1](https://doi.org/10.1007/s10485-023-09716-1), [arXiv:2007.12982](https://arxiv.org/abs/2007.12982)&rbrack;

[[!redirects relative monads]]

