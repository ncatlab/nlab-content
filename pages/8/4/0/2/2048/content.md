A coherent sheaf is a geometric globalization of the notion of [[coherent module]].


Given a [[ringed space]] (or, more generally, [[ringed site]]) $(X,\mathcal{O})$, a sheaf $\mathcal{E}$ of $\mathcal{O}$-modules is __finitely generated__, or of _finite type_, if there is an exact sequence of $\mathcal{O}$-modules of the form $\mathcal{O}^n\to \mathcal{E}\to 0$ where $n$ is finite. A [[sheaf]] $\mathcal{E}$ of $\mathcal{O}$-modules is __coherent__ if it is finitely generated and for every open $U$ in the base space (resp. every object $U$ in the base site) there exist a finite $p$ and a morphism $\mathcal{O}^p|_U\to \mathcal{E}_U$ of $\mathcal{O}|_U$-modules with a finitely generated kernel. 

A sheaf $\mathcal{E}$ of $\mathcal{O}$-modules is __finitely presented__ if there is an exact sequence of the form $\mathcal{O}^p\to\mathcal{O}^n\to\mathcal{E}\to 0$ with $p$ and $n$ finite. Every finitely presented $\mathcal{O}$-module is finitely generated. For coherent sheaf $\mathcal{E}$ over a ringed space, for every point $y$ in the base space $X$ there is a neighborhood $V$ such that the $\mathcal{O}_X(V)$-module $\mathcal{E}(V)$ of sections of $\mathcal{E}$ over $V$ is finitely presented. 
On a [[noetherian scheme]] the notions of finitely presented and coherent sheaves of $\mathcal{O}$-modules agree, but this is not true on a general scheme or general analytic space; sometimes even the structure sheaf $\mathcal{O}$ itself is a counterexample (not coherent while finitely presented).

The notion of coherent sheaf behaves well on the category of noetherian schemes. On a general topological space, by a basic result of Serre, if two of the sheaves of $\mathcal{O}$-modules in a [[short exact sequence]]
$$
0\to \mathcal{E}\to\mathcal{E}'\to \mathcal{E}''\to 0
$$
are coherent then so is the third. All this holds even if $\mathcal{O}$ is a sheaf of noncommutative [[rings]]. For commutative $\mathcal{O}$, the inner hom $Hom_{\mathcal{O}}(\mathcal{E},\mathcal{F})$ in the category of sheaves of $\mathcal{O}$-modules is coherent if $\mathcal{E},\mathcal{F}$ are coherent. 

[[!redirects coherent sheaves]]