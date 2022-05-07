
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

One analog in [[(∞,1)-category theory]] of _[[epimorphism]]_ in [[category theory]]. Beware that there are other notions such as _[[effective epimorphism in an (infinity,1)-category|effective epimorphism in an $(\infty,1)$-category]]_ and, more generally, the concept of _[[n-epimorphism]]_.

## Definition

\begin{definition}
 \label{EpimorphismInAnInfinityCategory}
For $\mathcal{C}$ an [[(∞,1)-category]], a [[1-morphism]] $f \colon X \to Y$ in $\mathcal{C}$ is an **epimorphism** if for all [[objects]] $A \in \mathcal{C}$ the induced morphism on [[hom infinity-groupoids|hom $\infty$-groupoids]]

$$
  \mathcal{C}(f,A) 
  \,\colon\, 
  \mathcal{C}(Y,A) 
    \xhookrightarrow{\;\;}
  \mathcal{C}(X,A)
$$

is a [[monomorphism in an (∞,1)-category|monomorphism in]] [[∞Grpd]].
\end{definition}



## Examples
 {#Examples}

\begin{example}\label{TerminalEpimorphismsInInfinityGroupoids}
**(terminal epimorphisms of $\infty$-groupoids)**
\linebreak
  For $\mathcal{X} \,\in\,$ [[Infinity-Grpd|$Grpd_\infty$]], if the [[terminal object in an (infinity,1)-category|terminal map]] $\mathcal{X} \to \ast$ is an epimorphism in the sense of Def. \ref{EpimorphismInAnInfinityCategory} then

1. $\mathcal{X}$ is [[connected homotopy type|connected]];

1. [[fundamental group|$\pi_1(\mathcal{X})$]] is [[perfect group|perfect]].

([Hoyois 2019, Lem. 3](#Hoyois19))

In particular, this means that in order for the [[delooping groupoid]] $\mathbf{B}G$ of a [[discrete group]] $G$ (i.e. the [[Eilenberg-MacLane space]] $K(G,1)$) to be such that $\mathbf{B}G \to \ast$ is epi, the group $G$ must be [[perfect group|perfect]].
\end{example}

\begin{remark}
**(terminal epimorphisms of 1-groupoids)**
  In contrast to Ex. \ref{TerminalEpimorphismsInInfinityGroupoids},
  in the [[(2,1)-category]] [[Grpd|$Grpd_1$]] of [[1-groupoid|1-]][[groupoids]] the maps

$$
  \mathcal{X} 
  \xrightarrow{Map(B G \to \ast, \mathcal{X})}
  Map(B G, \mathcal{X})
$$

are always [[fully faithful functor|fully faithful]], for all $\mathcal{X} \in Grpd_1$, without further conditions on $G$, notably so for non-trivial [[abelian groups]] $G$. Explicitly, for the case $\mathcal{X} \simeq B K$ (to which the general situation reduces by [[extensive category|extensivity]]), we have the coproduct decomposition

$$
  Map(B G, \, B K)
  \;\simeq\;
  \underset{
    c \in H^1_{Grp}(G,K)
  }{\coprod}
  B Stab_K(c)
  \;\;\;\simeq\;\;\;
  B K
  \,
  \sqcup
  \,
  \underset{
    {
      c \in H^1_{Grp}(G,K)
    }
    \atop
    {
      c \neq 1
    }
  }{\coprod}
  B Stab_K(c)  
$$

which plays a central role in discussion such as of [[inertia orbifolds]], [[equivariant principal bundles]], [[equivariant K-theory]] and other aspects of [[equivariant cohomology]].

The point is that a [[natural transformation]] out of $B G$ into a [[1-groupoid]] has only a single component, corresponding to the point $\ast \to B G$, but a [[pseudonatural transformation]] out of $B G$ into a [[2-groupoid]] (and higher) has in addition a component for each element of $G$, which are not reflected on $\ast \to B G$. 
\end{remark}


In generalization of Ex. \ref{TerminalEpimorphismsInInfinityGroupoids}:
\begin{example}
A morphism $X\to Y$ between [[connected spaces]] is an epimorphism iff $Y$ is formed via a [[Quillen plus construction]] from a [[perfect group|perfect]] [[normal subgroup]] of the [[fundamental group]] $\pi_1(X)$.  

More generally, a map of spaces is an epi iff all its fibers are acyclic spaces in the sense that their [[suspensions]] are [[contractible]].  
\end{example}
This is discussed in [Raptis 2017](#Raptis17).

A generalization of this to epimorphisms and acyclic spaces in [[(infinity,1)-toposes|$(\infty,1)$-toposes]] is discussed in [Hoyois 19](#Hoyois19).

\begin{example}
A morphism $A \to B$ of [[E-infinity rings|$E_\infty$-rings]] is an epimorphism iff $B$ is [[smashing localization|smashing]] over $A$, i.e., if $ B \wedge_A B \approx B$.
\end{example}


## Related concepts

* [[Quillen plus construction]]

## References

* {#Raptis17} [[George Raptis]], *Some characterizations of acyclic maps*, Journal of Homotopy and Related Structures volume 14, pages 773–785 (2019) 2017 ([arxiv:1711.08898](https://arxiv.org/abs/1711.08898), [doi:10.1007/s40062-019-00231-6](https://doi.org/10.1007/s40062-019-00231-6))

* {#Hoyois19} [[Marc Hoyois]], *On Quillen's plus construction*, 2019 ([pdf](http://www.mathematik.ur.de/hoyois/papers/acyclic.pdf), [[Hoyois_PlusConstruction.pdf:file]])


[[!redirects epimorphisms in an (infinity,1)-category]]

[[!redirects epimorphism in an (∞,1)-category]]
[[!redirects epimorphisms in an (∞,1)-category]]

[[!redirects epimorphism in an infinity1-category]]
