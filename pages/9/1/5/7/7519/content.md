[[!redirects HNN-extension]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[combinatorial group theory]], by the *HNN construction* --- named after [Higman, Neumann and Neumann (1949)](#HigmanNeumannNeumann49) --- one means a [[universal construction]] which from a [[group]] and two *abstractly* [[isomorphism|isomorphic]] [[subgroups]] produces a group extension in which these two become [[conjugate subgroups]].

If the group is a fundamental group of a [[topological space]], this comes from the following situation.
If $X$ is a topological spaces, $A$ and $B$ to isomorphic subspaces of $X$, and one is given a fundamental group of $X$, what is the fundamental group of $X$ with attached handle from $A$ to $B$ ?


## Definition

\begin{definition}\label{HNNConstruction}
Given a [[group]], $G$, and a [[subgroup]], $H \subset G$, equipped with a(nother) [[monomorphism]] $\theta \colon  H \hookrightarrow G$, then the **HNN-extension** $G \ast_H$ is obtained by adjoining an [[element]] $t$ to $G$ subject to the condition:

$$
  \underset{h \in H}{\forall} 
  \;\;\;\;
  t^{-1} \cdot h \cdot t \;=\; \theta(h)
  \,.
$$

\end{definition}

Notice that there is a canonical [[subgroup]]-inclusion

$$
  G \hookrightarrow G \ast_H
$$

under which the two copies of $H$ in $G$ (given by $H$ itself and by the [[image]] $\theta(H)$) become [[conjugate subgroups]] in $G \ast_H$.

## Properties

### Link with graphs of groups

Examine the [[fundamental group of a graph of groups|fundamental group]] of the [[graph of groups]], $\mathcal{G}$, with [[underlying]] [[graph]] the graph with one [[vertex]], $v$ and one [[edge]], $e$ and nothing else. 

Take 

* the vertex group, $G_v$, to be $G$, 

* the edge group, $G_e$, to be $H$, 

* the two morphisms from $G_e$ to $G_v$ to be the canonical inclusion of $H$ into $G$ and the given monomorphism, $\theta$, 

then $\Pi_1(\mathcal{G})(v) \cong G \ast_H$.

### As a 2-colimit
 {#AsATwoColimit}

Consider groups $G$ seen in terms of their [[delooping groupoid]] $\mathbf{B}G$ as objects of the [[(2,1)-category]] [[Grpd]] of [[groupoids]]. 

> Beware that this construction $\mathbf{B}(-) \;\colon\; Grps \to Grpds$ is not a [[fully faithful (infinity,1)-functor|fully faithful]] [[(2,1)-functor]]: The fully-faithful embedding is obtained only by regarding the delooping groupoids as *[[pointed objects]]* in [[Grpd]], see at *[[looping and delooping]]*. The [[2-morphisms]] between ([[1-morphisms]] between) delooping groupoids which do not respect the base point are precisely those [[natural transformations]] referred to in the following.

Explicitly, this means that for a [[parallel pair]] of [[group homomorphisms]] $(\varphi,\theta) \colon H \rightrightarrows G$, a [[2-morphism]] $\mathbf{B}\varphi \Rightarrow \mathbf{B}\theta$ between their [[deloopings]] is equivalently (a [[natural isomorphism]] whose unique component is) an element $g \in G$ such that $g\varphi g^{-1}=\theta$.

Now within this [[(2,1)-category]], the ([[delooping]] of the) HNN-extension $G\ast_H$ (Def. \ref{HNNConstruction}) is a [[2-colimit]]: 

Namely, if $\iota \colon H \hookrightarrow G$ denotes the given [[subgroup]] inclusion and $\theta \colon H \hookrightarrow G$ the (other) monomorphism, then $\mathbf{B}(G\ast_H)$ is the *[[coinserter]]* of $(\mathbf{B}\theta,\mathbf{B}\iota) \colon \mathbf{B}H \rightrightarrows \mathbf{B}G$.


## References

The original article:

* {#HigmanNeumannNeumann49} Graham Higman, B. H. Neumann, Hanna Neuman, *Embedding Theorems for Groups*, J. of the London Mathematical Society **s1-24** 4 (1949)  247-254 &lbrack;[doi:10.1112/jlms/s1-24.4.247](https://doi.org/10.1112/jlms/s1-24.4.247)&rbrack;


See also:

* Wikipedia, *[HNN extension](https://en.wikipedia.org/wiki/HNN_extension)*

* [[Jean-Pierre Serre]], _Arbres, amalgames, $SL_2$_, volume 46 of _Ast&#233;risque , Soci&#233;t&#233; math&#233;matique 
de France (1977)

* [[Jean-Pierre Serre]], , _Trees_ , Springer Monographs in Mathematics, Springer-Verlag Berlin.  
150, 157, 161 (2003)

A standard reference is

* Lyndon, Schupp, _Combinatorial group theory_

Recent survey

* arXiv:[2512.10800](https://arxiv.org/pdf/2512.10800)

[[!redirects HNN-extension]]
[[!redirects Higman-Neumann-Neumann extension]]