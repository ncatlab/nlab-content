
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

An [[endofunctor]] on a [[category]] $\mathcal{A}$ is _pointed_ if it is equipped with a [[natural transformation]] from the [[identity functor]].



## Definition
 {#Definition}


\begin{definition}\label{PointedEndofunctor}
An [[endofunctor]] $S \colon \mathcal{A}\to \mathcal{A}$ is called **pointed** if it is equipped with a [[natural transformation]] $\sigma \colon Id_\mathcal{A} \to S$ from the [[identity functor]] on $\mathcal{A}$.  
\end{definition}

\begin{remark}\label{MeaningOfPointedness}
Def. \ref{PointedEndofunctor} is *not* the usual classical notion of a [[pointed object]] in the endo-[[functor category]], since the [[identity functor]] is not in general a [[terminal object]] there. It is however pointed in the sense of a [[pointed object in a monoidal category]], involving a morphism out of the monoidal unit, since the identity functor is the [[tensor unit]] for the canonical [[monoidal category]]-[[structure]] on the [[endofunctor category]] (given by [[horizontal composition]]). In this sense, a pointed endofunctor may be regarded as being equipped with a "monoidal point". A [[monad]] has a canonical such point (see Exp. \ref{Monads} below), usually called the *[[unit of a monad|unit]]*.
\end{remark}

\begin{remark}
The notion of a pointed endofunctors, Def \ref{PointedEndofunctor}, naturally extends to any [[2-category]], where we can define a **pointed endomorphism** to be an endo-[[1-morphism]] $s \colon a \to a$ equipped with a [[2-morphism]] $\sigma \colon id_a \Rightarrow s$ from the [[identity morphism]].
\end{remark}


\begin{definition}
A pointed endofunctor $(S, \sigma)$ (Def. \ref{PointedEndofunctor}) is called **[[well-pointed endofunctor|well-pointed]]** if $S\sigma = \sigma S$ as natural transformations $S \longrightarrow S \circ S$.
\end{definition}


## Properties

### Relation to free algebras

The pointed [[algebras over an endofunctor]] on a pointed endofunctor induce a theory of _[[transfinite construction of free algebras]]_ [[algebra over an endofunctor|over]] general endofunctors.

## Examples

\begin{example}\label{Monads}
A [[monad]] can be regarded as a pointed endofunctor where $\sigma$ is its [[unit of a monad|unit]].  
\end{example}


+-- {: .num_prop}
###### Proposition
The pointed endofunctor $(T,\eta)$ underlying a monad $(T : C \to C, \eta: 1\to T, \mu : T^2\to T)$ is well-pointed if and only if $T$ is [[idempotent monad|idempotent]], i.e. $\mu$ is an isomorphism.
=--
+-- {: .proof}
###### Proof
If $\mu$ is an isomorphism then $T\eta=\eta T$ since both are sections of $\mu$. 

Conversely, if $T\eta=\eta T$, then $T\eta$ is an inverse for $\mu$.
Indeed, 
$$
T\eta_A\circ\mu_A = \mu_{TA}\circ T^2\eta_A = \mu_{TA}\circ T\eta_{TA} = 1_{T^2A},
$$
and $\mu_A\circ T\eta_A = 1_{TA}$ by the right unit law.
=--

## For pointed object in the endofunctor category

Notice that the statement which one might expect, that a pointed endofunctor is a [[pointed object]] in the [[endofunctor category]] is not quite right in general.

The [[terminal object]] of the category of endofunctors on $\mathcal{A}$ is the functor $T$ which sends all objects to $\ast$ and all morphisms to the unique morphism $\ast \to \ast$, where $\ast$ is the terminal object of the category $\mathcal{A}$. So a pointed object in the endofunctor category should be an endofunctor $S:\mathcal{A} \to \mathcal{A}$ equipped with a natural transformation $\sigma:T \to S$.

Rather, a pointed endofunctor is equipped with a map from the [[unit object]] for the monoidal structure on the endofunctor category.


## Related concepts

* [[pointed object]]

* [[well-pointed endofunctor]]

## References

* [[Harvey Wolff]], p. 234 of: *Free monads and the orthogonal subcategory problem*, Journal of Pure and Applied Algebra **13** 3 (1978) 233-242 &lbrack;<a href="https://doi.org/10.1016/0022-4049(78)90010-5">doi:10.1016/0022-4049(78)90010-5</a>&rbrack;


* {#Kelly} [[Max Kelly]], _A unified treatment of transfinite constructions for free algebras, free monoids, colimits, associated sheaves, and so on._  Bull. Austral. Math. Soc. 22 (1980), 1--83. doi:[10.1017/S0004972700006353](http://dx.doi.org/10.1017/S0004972700006353)
 

[[!redirects pointed endofunctors]]
[[!redirects pointed endomorphism]]
[[!redirects pointed endomorphisms]]
