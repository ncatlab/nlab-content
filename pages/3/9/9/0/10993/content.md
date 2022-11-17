
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

A _relative monad_ is what is to a _[[relative adjunction]]_ as a [[monad]] is to an [[adjunction]].

In [ACU14](#ACU14), the authors proved that a relative monad on a functor $J \colon \mathbf J \to \mathbf C$ are 'skew-monoids in the [[skew-monoidal category]] $[\mathbf J, \mathbf C]$' (see below).

The specialization of the following definition to plain monads, hence to the case $J = id$, yields at face value not the traditional definition of [[monads]] but the (equivalent) definition of *[[extension systems]]* (also "[[Kleisli triples]]", being the form of [[monads in computer science]]).


## Definitions

Let $\mathbf J, \mathbf C$ be [[categories]] and $J \colon \mathbf J \to \mathbf C$ be a [[functor]].

### As skew Kleisi triples


\begin{definition}
\label{def}
A **relative monad $T$ on $J$** is a functor $T \colon \mathbf J \to \mathbf C$ equipped with

1.  a _[[unit of a monad|unit]]_ $\eta_X \colon J X \to T X$ [[natural transformation|natural]] in $X \colon \mathbf J$,

1.  a _[[extension system|Kleisli extension]]_ $(-)^* \colon \mathbf C(J X, T Y) \to \mathbf C(T X, T Y)$ in both $X,Y \colon \mathbf J$

such that for every $X,Y,Z \colon \mathbf J$ and $k \colon J X \to T Y$ the following [[equations]] hold:

1. _(left [[unitality]])_ $k = k^* \circ \eta_X$,

1. _(right [[unitality]])_ $\eta_X^* = 1_{T X}$,

1. _([[associativity]])_ $(\ell^* \circ k)^* = \ell^* \circ k^*$ for every $\ell : J Y \to T Z$.

\end{definition}

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


### As skew-monoids

The notion of a *[[skew-monoidal category]]* is like that of a [[monoidal category]] except that the [[unitors]] and [[associators]] are not necessarily [[invertible morphism|invertible]]. A [[monoid]] in a [[skew-monoidal category]] is called a "*skew-monoid*".

In the general case that $\mathbf{J}$ is distinct from $\mathbf{C}$,  the [[functor category]] $Func(\mathbf J, \mathbf C)$ lacks a natural [[monoidal category]] [[structure]] (as opposed to the case of [[endofunctors]] $Func(\mathbf{C}, \mathbf{C})$) so that the usual definition of [[monads]] as [[monoids]] cannot apply --- but a suitable "skew" variant works:


The (skew-)[[composition]] of [[functors]] $F,G \colon \mathbf J \to \mathbf C$ may be defined by first [[left Kan extension|extending]] $F$ along $J$ and then composing with $G$. The resulting composition product on $[\mathbf J, \mathbf C]$ is [[coherence|coherent]] but only [[lax natural transformation|laxly]] so, hence the need to appeal to skew-monoidal categories:

\begin{theorem}
**([ACU14, Thm. 3.4](#ACU14))**
\linebreak
Suppose $J \colon \mathbf J \to \mathbf C$ is such that $\mathrm{Lan}_J \colon [\mathbf J, \mathbf C] \to [\mathbf C, \mathbf C]$ exists (e.g. if $\mathbf J$ is small and $\mathbf C$ cocomplete).
Then $[\mathbf J, \mathbf C]$ is skew-monoidal, with unit $J$ and product $F \circ^J G = (\mathrm{Lan}_J F) \circ G$, and a relative monad is a monoid in $([\mathbf J, \mathbf C], J, \circ^J)$.
\end{theorem}

When $J:\mathbf J \to \mathbf C$ is a free completion of $\mathbf{J}$ under colimits from some set $\mathcal{F}$ of indexing types, then this skew-monoidal structure on $[\mathbf J, \mathbf C]$ is properly monoidal, since it is equivalent to the $\mathcal{F}$-colimit preserving functors $\mathbf C\to\mathbf C$, and the monoidal structure is just functor composition. 

## Examples

* A relative monad on the embedding $J:\mathbf{FinSet} \to \mathbf {Set}$ is the same thing as an [[abstract clone]]. These are equivalent to [[finitary monads]] and single-sorted [[algebraic theories]]. 

* Any monad $T$ on $\mathbf{C}$ induces a relative monad $TJ$ on $J$, for any $J:\mathbf{J}\to \mathbf{C}$. 

* Fixing a category $\mathbb{V}$ with finite products, to give a [[Freyd category]] is to give a strong relative monad on the [[Yoneda embedding]] $\mathbb{V}\to [\mathbb{V}^{\mathrm{op}},\mathbf{Set}]$. 

* The presheaf construction $(\mathbb{C}\mapsto [{\mathbb{C}}^{\mathrm{op}},\mathbf{Set}])$ can be regarded as a [[relative pseudomonad]] on the inclusion $\mathbf{Cat}\to \mathbf{CAT}$. (See also [[Yoneda structures]].)

* A [[monad with arities|monad on $\mathbf C$ with arities in $\mathbf{J}\subseteq \mathbf C$]] is the same thing as a relative monad for the embedding $\mathbf{J}\to \mathbf C$. (Here $\mathbf{J}\subseteq \mathbf{C}$ is required to be a [[dense subcategory]], so that to give a functor $\mathbf{J}\subseteq \mathbf{C}$ is to give a functor $\mathbf{C}\to\mathbf{C}$ preserving $J$-absolute colimits.)

## Related pages

* [[relative comonad]]

* [[extension system]], [[Kleisli triple]], [[monad in computer science]]

## References

The concept was introduced, in the context of [[monads in computer science]], in: 

* {#ACU14} [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;


[[!redirects relative monads]]

