
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

A group is *residually finite* if it has a good supply of [[subgroups]] of [[finite number|finite]] [[index of a subgroup|index]].

## Definition

\begin{definition}
  A [[group]] $G$ is called *residually finite* if it satisfies the following equivalent conditions:

1. For each $g \in G$, $g \neq \mathrm{e}$, 

   1. there exists a [[normal subgroup]] $N \subset G$ of [[finite number|finite]] [[index of a subgroup|index]] $[G\colon N] \in \mathbb{N}$ such that $g \nin N$.

   1. there exists a [[finite group]] $K$ and a [[group homomorphism]] $\phi \,\colon\, G \to K$ such that $\phi(g) \neq \mathrm{e}$.

1. The [[intersection]] of all [[subgroups]] $H \subset G$ of [[finite number|finite]] [[index of a subgroup|index]] $[G\colon H] \in \mathbb{N}$ is [[trivial group|trivial]]. 

1. The [[intersection]] of all [[normal subgroups]] $N \subset G$ of [[finite number|finite]] [[index of a subgroup|index]] $[G\colon N] \in \mathbb{N}$ is [[trivial group|trivial]]. 

1. $G$ is a [[subgroup]] of a [[direct product group|direct product]] of [[finite groups]].

\end{definition}

## Examples

\begin{example}
Classes of examples of residually finite groups include

* [[finite groups]]

* [[free groups]]

* [[finitely generated group|finitely generated]]$\;$[[nilpotent groups]]

* [[finitely generated group|finitely generated]]$\;$[[linear group]]

\end{example}

\begin{example}
  The [[mapping class group]] of a [[closed manifold|closed]] [[orientation|oriented]] [[surface]] is residually finite.
\end{example}
([Grossman 1974](mapping+class+group#Grossman74))

## References

Review:

* [[Wilhelm Magnus]]: *Residually finite groups*,  Bull. Amer. Math. Soc. **75** 2 (1969) 305-316 &lbrack;[euclid:bams/1183530287](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society/volume-75/issue-2/Residually-finite-groups/bams/1183530287.full), [ams:1969-75-02/S0002-9904-1969-12149-X](https://www.ams.org/journals/bull/1969-75-02/S0002-9904-1969-12149-X)&rbrack;

* Tullio Ceccherini-Silberstein, Michel Coornaert: *Residually Finite Groups*, chapter 2 of: *Cellular Automata and Groups* &lbrack;[doi:10.1007/978-3-642-14034-1_2](https://doi.org/10.1007/978-3-642-14034-1_2), [pdf](https://link.springer.com/content/pdf/10.1007/978-3-642-14034-1_2)&rbrack;

See also: 

* Wikipedia, *[Residually finite group](https://en.wikipedia.org/wiki/Residually_finite_group)*

On residual finiteness of [[mapping class groups]]:

* {#Grossman74} Edna K. Grossman: *On the residual finiteness of certain mapping class groups*,  J. London Math. Soc. **s2-9** 1 (1974) 160–164 &lbrack;[doi;10.1112/jlms/s2-9.1.160](https://doi.org/10.1112/jlms/s2-9.1.160)&rbrack;


[[!redirects residually finite groups]]


[[!redirects residual finite group]]
[[!redirects residual finite groups]]



