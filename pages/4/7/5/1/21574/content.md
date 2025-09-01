
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


\tableofcontents

\section{Idea}

Just as the category [[Cat]] of categories can be equipped with a [[canonical model structure]], namely the [[canonical model structure on categories]], so too can [[2Cat]], the category of strict 2-categories. This extends to weak 2-categories too, although in order to actually have a [[category]] on which to put the model structure, one has to work with [[strict 2-functor|strict 2-functors]]. 

The characterising feature of a canonical model structure on [[2Cat]] is that the weak equivalences should be [[equivalence of 2-categories|equivalences of 2-categories]], categorifying the fact that the equivalences in the [[canonical model structure on categories]] are [[equivalence of categories|equivalences of categories]]. What the fibrations and cofibrations should be, or more specifically how to categorify [[isofibration|isofibrations]] and [[iso-cofibration|iso-cofibrations]], is one of the main points to resolve to obtain the model structure.

What is usually referred to as the canonical model structure on 2-categories is a model structure first described by [[Stephen Lack|Lack]] in [Lack2002](#Lack2002) and [Lack2004](#Lack2004). In this model structure, the fibrations are [[Lack fibration|Lack fibrations]], and every object is [[fibrant object|fibrant]], but not every object is [[cofibrant object|cofibrant]], in contrast to the [[canonical model structure on categories]].

However, it is possible to put a different canonical model structure on [[2Cat]] in which every object is both fibrant and cofibrant, using the thesis [Williamson2011](#Williamson2011). The fibrations in this case are, roughly speaking, those [[2-functor|2-functors]] in which [[semi-strict equivalence|semi-strict equivalences]] can be lifted. 

\section{Lack model structure}

The following is Theorem 4 in [Lack2004](#Lack2004).

\begin{thm} There is a model structure on [[2Cat]] in which the equivalences are [[equivalence of 2-categories|equivalences of 2-categories]], and the fibrations are [[equiv-fibrations]]. \end{thm}

Note that by "equivalence of 2-categories" we mean the fully non-strict notion.  In particular, although the morphisms in $2Cat$ are [[strict 2-functors]], those that are equivalences may have inverses that are only [[pseudofunctors]] and hence not morphisms in $2Cat$.

Every object in this model category is fibrant, but not every object is cofibrant.  The cofibrant 2-categories are those whose underlying 1-category is the [[free category]] on a [[quiver]].  This property ensures that any [[pseudofunctor]] with cofibrant domain is equivalent to a strict 2-functor, so that the "homotopy theory" of the model category is bicategorically correct.

This is also a [[monoidal model category]] with respect to the [[Gray tensor product]].

\section{Canonical model structure in which every object is both fibrant and cofibrant}

Throughout this section, let $\mathcal{E}_{semi}$ denote the [[free-standing semi-strict equivalence]]. 

\begin{defn} A _semi-strict equiv-fibration_ is a [[2-functor]] $p: \mathcal{A} \rightarrow \mathcal{B}$ such that, for any (strictly) commutative diagram 

\begin{tikzcd}
\mathcal{X} \ar[r, "f"] \ar[d, swap, "id \times 0"] & \mathcal{A} \ar[d, "p"] \\
\mathcal{X} \times \mathcal{E}_{semi} \ar[r, swap, "g"] & \mathcal{B}  
\end{tikzcd}

in [[2Cat]], there is a functor $l: \mathcal{X} \times \mathcal{E}_{semi} \rightarrow \mathcal{A}$ such that the following diagram in [[2Cat]] (strictly) commutes.

\begin{tikzcd}
\mathcal{X} \ar[r, "f"] \ar[d, swap, "id \times 0"] & \mathcal{A} \ar[d, "p"] \\
\mathcal{X} \times \mathcal{E}_{semi} \ar[r, swap, "g"] \ar[ur, "l"] & \mathcal{B}  
\end{tikzcd}

\end{defn}

\begin{defn} A _semi-strict equiv-cofibration_ is a [[2-functor]] $j: \mathcal{A} \rightarrow \mathcal{B}$ such that, for any (strictly) commutative diagram 

\begin{tikzcd}
\mathcal{A} \ar[r, "id \times 0"] \ar[d, swap, "j"] & \mathcal{A} \times \mathcal{E}_{semi} \ar[d, "h"] \\
\mathcal{B} \ar[r, swap, "f"] & \mathcal{X}  
\end{tikzcd}

in [[2Cat]], there is a functor $k: \mathcal{B} \times \mathcal{E}_{semi} \rightarrow \mathcal{X}$ such that the following diagram in [[2Cat]] (strictly) commutes.

\begin{tikzcd}
\mathcal{A} \ar[r, "id \times 0"] \ar[d, swap, "j"] & \mathcal{A} \times \mathcal{E}_{semi} \ar[d, "j \times id"] \ar[ddr, bend left, "h"] & \\
\mathcal{B} \ar[r, swap, "id \times 0"] \ar[drr, swap, bend right, "f"] & \mathcal{B} \times \mathcal{E}_{semi} \ar[dr, "k"] & \\
& & \mathcal{X}  
\end{tikzcd}

\end{defn}

\begin{defn} A [[2-functor]] $f: \mathcal{A} \rightarrow \mathcal{B}$ is a _semi-strict equivalence of 2-categories_ if there is a 2-functor $g : \mathcal{B} \to \mathcal{A}$ and 2-functors $h: \mathcal{A} \times \mathcal{E}_{semi} \rightarrow \mathcal{A}$ and $k : \mathcal{B}\times \mathcal{E}_{semi} \to \mathcal{B}$ exhibiting "homotopies" from $f\circ g$ and $g\circ f$ to identities. \end{defn}

\begin{thm} The category [[2Cat]] can be equipped with a model structure in which the weak equivalences are semi-strict equivalences of 2-categories, the fibrations are semi-strict equiv-fibrations, and the cofibrations are semi-strict equiv-cofibrations. \end{thm} 

\begin{proof} By the section 'Structured interval' of the page [[walking equivalence]], $\mathcal{E}_{semi}$ can be equipped with the structure of an [[interval object]], and embellished with all the structures of [Williamson2011](#Williamson2011) which are required for Corollary XV.6 and/or Corollary XV.7 of this work, satisfying all the hypotheses of these corollaries. Applying these corollaries, we immediately obtain the theorem. \end{proof}

## Related concepts

* [[model structure on DblCat]]

\section{References}

Precursor discussion establishing a model structure on the category of ([[equivariant homotopy theory|equivariant]]) [[2-groupoids]]:

* {#MoerdijkSvensson93} [[Ieke Moerdijk]], Jan-Alve Svensson: *Algebraic classification of equivariant homotopy 2-types, I*, Journal of Pure and Applied Algebra **89** 1–2 (1993)  187-216 \[<a href="https://doi.org/10.1016/0022-4049(93)90094-A">doi:10.1016/0022-4049(93)90094-A</a>\]

The original result on the model structure on 2-categories:

* {#Lack2002} [[Stephen Lack]]: *A Quillen model structure for 2-categories*, K-Theory **26** 2 (2002) 171-205 &lbrack;[doi:10.1023/A:1020305604826](http://dx.doi.org/10.1023/A:1020305604826), [[Lack-ModelOn2Cat.pdf:file]], [zbmath](https://zbmath.org/?q=an%3A1017.18005)&rbrack;

* {#Lack2004} [[Stephen Lack]]: *A Quillen model structure for bicategories*, K-Theory **33 **3** (2004) 185-197 &lbrack;[doi:10.1007/s10977-004-6757-9](http://dx.doi.org/10.1007/s10977-004-6757-9), [[Lack-ModelOnBiCat.pdf:file]], [zbmath](https://zbmath.org/?q=an%3A1069.18008)&rbrack;

Further discussion:

* {#Williamson2011} [[Richard Williamson]]: *Cylindrical model structures*, PhD thesis, University of Oxford (2011) &lbrack;[author's webpage](http://rwilliamson-mathematics.info/cylindrical_model_structures/cylindrical_model_structures.html), [arXiv:1304.0867](https://arxiv.org/abs/1304.0867)&rbrack;

[[!redirects canonical model structures on 2-categories]]

[[!redirects canonical model structure on 2Cat]]
[[!redirects canonical model structures on 2Cat]]

[[!redirects Lack model structure]]
[[!redirects Lack model structures]]

