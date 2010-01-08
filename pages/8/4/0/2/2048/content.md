
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _coherent sheaf_ is a geometric globalization of the notion of [[coherent module]].


## Definition

Let $(X,\mathcal{O})$ be a [[ringed space]] or, more generally, a [[ringed site]]. 

A [[sheaf]] $\mathcal{E}$ on $X$ of $\mathcal{O}$-[[module]]s is

*  __finitely generated__, or of __finite type__ , if every point $x \in X$ has an open neighbourhood such that there is a surjective morphism 

   $$\mathcal{O}^n|_U \to \mathcal{E}|_U$$ 

   from a [[free module]] to $E|_{U}$,  where $n$ is finite. 

* __coherent__ if it is 

  1. finitely generated 

  1. for every open $U$ in the base space (resp. every object $U$ in the base site) there exist a finite $p \in \mathbb{N}$ and a morphism 

     $$\mathcal{O}^p|_U\to \mathcal{E}_U$$ 

     of $\mathcal{O}|_U$-modules with a finitely generated [[kernel]]. 

* __finitely presented__ if there is an exact sequence of the form 

  $$\mathcal{O}^p\to\mathcal{O}^n\to\mathcal{E}\to 0$$ 

  with $p$ and $n$ finite. 

Every finitely presented $\mathcal{O}$-module is finitely generated. 

* __[[quasicoherent sheaf|quasi coherent]]__ if it is _locally_   -- on a cover $\{U_i\}$ -- _presentable_ in that ther are [[exact sequence]]s

  $$
    \mathcal{O}^{I_i}|_{U_i} \to \mathcal{O}^{J_i}|_{U_i}
    \to \mathcal{E}|_{U_i}
    \to 0
  $$

  where $I_i$ and $J_i$ may be infinite, i.e. of $\mathcal{E}$ is locally the [[cokernel]] of [[free module]]s. For more see [[quasicoherent sheaf]].

## Properties

For a coherent sheaf $\mathcal{E}$ over a [[ringed space]], for every  point $y$ in the base space $X$ there is a neighborhood $V$ such that the $\mathcal{O}_X(V)$-module $\mathcal{E}(V)$ of sections of $\mathcal{E}$ over $V$ is finitely presented. 
On a [[noetherian scheme]] the notions of finitely presented and coherent sheaves of $\mathcal{O}$-modules agree, but this is not true on a general scheme or general analytic space; sometimes even the structure sheaf $\mathcal{O}$ itself is a counterexample (not coherent while finitely presented).

The notion of coherent sheaf behaves well on the category of noetherian schemes. On a general topological space, by a basic result of Serre, if two of the sheaves of $\mathcal{O}$-modules in a [[short exact sequence]]
$$
0\to \mathcal{E}\to\mathcal{E}'\to \mathcal{E}''\to 0
$$
are coherent then so is the third. All this holds even if $\mathcal{O}$ is a sheaf of noncommutative [[rings]]. For commutative $\mathcal{O}$, the inner hom $Hom_{\mathcal{O}}(\mathcal{E},\mathcal{F})$ in the category of sheaves of $\mathcal{O}$-modules is coherent if $\mathcal{E},\mathcal{F}$ are coherent. 

[[!redirects coherent sheaves]]