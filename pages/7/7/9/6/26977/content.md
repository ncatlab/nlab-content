# Contents
* this block creates the table of contents, leave as is
{: toc}

## Idea

Diagrammatic sets are [[presheaf|presheaves]] over the [[atom category]]. There are kind of geometric [[polygraph|polygraphs]], and can serve as a model for [[higher category theory|higher categories]].


## Definition 

\begin{definition}
**(diagrammatic set)**\linebreak
A **diagrammatic set** $X$ is a presheaf over $\odot$, the [[atom category|category of atoms]] and cartesian maps. Diagrammatic sets and [[natural transformations]] form the category $\odot\mathbf{Set}$
\end{definition}


## Properties


Let $\mathbf{RDCpx}$ be the category of [[regular directed complex|regular directed complexes]] and cartesian maps. Since atoms are regular directed complexes, there is a [[full subcategory]] inclusion $i \colon \odot \hookrightarrow \mathbf{RDCpx}$. Moreover, any regular directed complex $P$ is canonically a colimit of its atoms, in the sense that there is a functor
$$
    P^* \colon P \to \mathbf{RDCpx} 
$$
sending $x \in P$ to the atom $\mathrm{cl}(x)$ and $x \le y$ to the inclusion $\mathrm{cl}(x) \hookrightarrow \mathrm{cl}(y)$, such that 
$$
    \colim P^* \cong P.
$$

Since $\odot\mathbf{Set}$ is the [[free cocompletion]] of $\odot$, one might wonder what happens when we compute the same colimit, but with the functor:
$$
    P^* \colon P \to \odot\mathbf{Set}.
$$
sending $x \in P$ to $y(\mathrm{cl}(x))$, where $y$ is the [[Yoneda embedding]]. Unsurprisingly, we obtain the same thing, in the following precise sense. The subcategory inclusion $i$ defines a [[restricted Yoneda embedding]]:
$$
    i^* \colon \mathbf{RDCpx} \to \odot\mathbf{Set}
$$
that sends a regular directed complex $P$ to the presheaf $\mathbf{RDCpx}(i^*(-), P)$. 

\begin{proposition}
    The functor $i^*$ is [[full and faithful functor|fully faithful]]. 
\end{proposition}
This means that $i$ is a [[dense functor]], so we see $\mathbf{RDCpx}$ as a full subcategory of $\odot\mathbf{Set}$, factoring the Yoneda embedding as
$$
    \odot\mathbf{Set} \hookrightarrow \mathbf{RDCpx} \hookrightarrow \odot\mathbf{Set}.
$$

Furthermore, the category $\odot$ is monoidal for the Gray product. By [[Day convolution]], the category $\odot\mathbf{Set}$ is also monoidal for (what we also call) the Gray product, with monoidal unit $y\mathbf{1}$, where $\mathbf{1}$ is the (Point). Let $P, Q$ be regular directed complexes, we have two ways of computing $P \otimes Q$:

*  via Day convolution when seeing $P, Q$ as presheaves over $\odot\mathbf{Set}$,
*  directly via the [[regular directed complex#operations|Gray product of regular directed complexes]]. 

Of course, those two ways give the same result, i.e. $i^*(P \otimes Q) = i^*(P) \otimes i^*(Q)$.

Another feature is the boundary. Similarly to the [[boundary of a simplex]], any atom $U$ has a boundary $\partial U$ which can be computed in two ways:

*  as the regular directed complex $U \backslash \{ \top_U \}$ with underlying poset $U$ without its top-element,
*  as the diagrammatic set generated from $yU$ minus its unique non-degenerate cell in dimension $\dim U$.

Again, those two ways coincide in the sense that $i^*(\partial U) = \partial yU$.



## Diagrammatic sets and higher category theory

The richeness of shapes in the category of atoms, as well as the quite rigid behavior of the category $\odot$ where they live make them a good candidate for modelling [[higher category theory|higher categories]]. In this perspective, in a diagrammatic set $X$, a natural transformation $x \colon U \to X$ whose domain is an $n$-dimensional atom, correspond to an **[[k-morphism|$n$-cell]]** in $X$. If $U$ is more generally an $n$-dimensional molecule, we call it an **$n$-diagram**, while when $U$ is furthermore round, we speak of a **round $n$-diagram**.

Before the more conjectural case of weak higher categories, we can deal with the case of higher groupoids.

### Higher groupoids
 
\begin{definition}
**(diagrammatic horn)**\linebreak
Let $U$ be an atom, let $V \sqsubseteq \partial^\alpha U$ be a [[regular directed complex#submolecule|rewritable submolecule]] of either the input or output boundary. The **diagrammatic horn** defined by $U, V$ is the regular directed complex
$$
    \Lambda^V_U \coloneqq U \backslash (V \backslash \partial V).
$$
We write
$$
    \lambda^V_U \colon \Lambda^V_U \hookrightarrow U   
$$
for the inclusion of a horn into its atom.
\end{definition}

\begin{example}
    Recall that the [[atom category|category]] $\odot$ contains as a full subcategory the oriented simplices, which is a category isomorphic to the [[simplex category]]. Then, any simplicial [[horn]] is also a diagrammatic horn.
\end{example}

\begin{definition}
**(Kan diagrammatic set)**\linebreak
A **Kan diagrammatic set** is a diagrammatic set $X$ in which all diagrammatic horns have a filler. That is, for all horn inclusions, and all solid arrows in
\begin{tikzcd}
    \Lambda^V_U \arrow[r, "\forall"] \arrow[d, "\lambda^V_U"', hook] & X \\
    U \arrow[ru, "\exists"', dotted]                                 &  
\end{tikzcd} 
there exists a diagonal dashed filler.
\end{definition}


The paper [ChanavatHadzihasanovic2024](#ChanavatHadzihasanovic2024) settles the Kan diagrammatic sets as model of [[infinity-groupoid|∞-groupoids]] in their following theorem:
\begin{theorem}\label{kan_model_structure}
There exists a [[cofibrantly generated model category|cofibrantely generated model structure]] on diagrammatic sets where

*  cofibrations are monomorphisms, and are generated by $\{ \partial U \hookrightarrow U \mid U\; \text{atom} \}$,
*  acyclic cofibrations are generated by the diagrammatic horn inclusions,
*  fibrant objects are Kan diagrammatic sets,

which is [[Quillen equivalence|Quillen equivalent]] to the [[classical model structure on simplicial sets]].
\end{theorem} 

\begin{remark}
Note that the existence of the model structure and the Quillen equivalence already follow from the fact that $\odot$ is a test category.
\end{remark}

We can realize the Quillen equivalence in two different ways. For the first one, recall that any atom is in particular a poset, of which we can take the [[nerve]], to get a simplicial set, which defines a functor from $\odot$ to $\mathbf{sSet}$. Then we define $\mathrm{Sd}_\odot \colon \odot\mathbf{Set} \to \mathbf{sSet}$ as the [[Yoneda extension]] of this functor, and we name its right adjoint $\mathrm{Ex}_\odot$. Then:

\begin{proposition}
    The adjunction $\mathrm{Sd}_\odot \dashv \mathrm{Ex}_\odot$ realizes the Quillen equivalence of Theorem \ref{kan_model_structure}.
\end{proposition}

But also, recall that, up to isomorphism, the [[simplex category]] is a full subcategory of $\odot$, thus of $\odot\mathbf{Set}$. The [[Yoneda extension]] of this full subcategory inclusion defines the functor $i_\Delta \colon \mathbf{sSet} \to \odot\mathbf{Set}$, together with its right adjoint $X \mapsto X_\Delta$. First we observe:

\begin{proposition}
The adjunctions $\mathrm{Sd}_\odot \dashv \mathrm{Ex}_\odot$ and $i_\Delta \dashv (-)_\Delta$
$$
\mathbf{sSet} \leftrightarrows \odot\mathbf{Set} \leftrightarrows \mathbf{sSet}
$$
factorize the adjunction $\mathrm{Sd} \dashv \mathrm{Ex}$ of simplicial sets (see [[subdivision]]). 
\end{proposition}

Hence,
\begin{proposition}
    The adjunction $i_\Delta \dashv (-)_\Delta$ also realizes the Quillen equivalence of Theorem \ref{kan_model_structure}.
\end{proposition}
\begin{proof}
    By [[two-out-of-three]] for Quillen equivalences.
\end{proof}


### Higher category

This part requires notion of internal invertibility in diagrammatic set that are not defined in this article, but whose treatment can be found in [Hadzihasanovic2020](#Hadzihasanovic2020).

\begin{definition}
**(merge)**\linebreak
Let $U$ be a round molecule. The **merge** of $U$ is the atom $\partial^- U \Rightarrow \partial^+ U$.
\end{definition}
The merge of a round molecule _composes_ all the top dimensional cells of $U$ inside one. For instance, the merge of
\begin{tikzcd}
    &                           & {}                                             &    &    \\
{} \arrow[rrdd] \arrow[rrrr, bend left=49] \arrow[rr] &                           & {} \arrow[u, Rightarrow] \arrow[dd] \arrow[rr] & {} & {} \\
    & {} \arrow[ru, Rightarrow] & {} \arrow[ru, Rightarrow]                      &    &    \\
    &                           & {} \arrow[rruu]                                &    &   
\end{tikzcd}
is 
\begin{tikzcd}
                                           &  & {}                        &  &    \\
{} \arrow[rrdd] \arrow[rrrr, bend left=49] &  &                           &  & {} \\
                                           &  & {} \arrow[uu, Rightarrow] &  &    \\
                                           &  & {} \arrow[rruu]           &  &   
\end{tikzcd}
Notice that $\langle U \rangle$ shares the same boundaries as $U$. In particular, since $U$ is round, $U \Rightarrow \langle U \rangle$ is well-defined.

\begin{definition}
**(weak composite)**\linebreak
Let $X$ be a diagrammatic set, let $x \colon U \to X$ be a round $n$-diagram. A weak composite of $x$ is a cell $\langle x \rangle \colon \langle U \rangle \to X$ such that $x \simeq \langle x \rangle$.
\end{definition}

Here, $x \simeq \langle x \rangle$ means a cell in $X$ of shape $U \Rightarrow \langle U \rangle$ which is invertible (in a sense we did not define here).

The contender for weak $\infty$-category is the notion of diagrammatic set with _weak composites_. 
\begin{definition}
**(diagrammatic set with weak composites)**\linebreak
A diagrammatic set has **weak composites** if all round diagrams have a weak composite. This means that for all round molecules $U$, and all solid arrows in
\begin{tikzcd}
    U \arrow[d, hook] \arrow[r, "\forall"]                    & X \\
    U \simeq \langle U \rangle \arrow[ru, "\exists"', dotted] &  
\end{tikzcd}
there exists a diagonal filler.
\end{definition}


## References

The origin of the name is in the following, where diagrammatic sets were presheaves over Johnson's [[pasting scheme|pasting schemes]]:

* Kapranov, M. M., and Voevodsky, V. A.. _$\infty $-groupoids and homotopy types._ Cahiers de Topologie et Géométrie Différentielle Catégoriques 32.1 (1991) ([link](http://eudml.org/doc/91469))

An older treatment of diagrammatic sets:

* {#Hadzihasanovic2020}[[Amar Hadzihasanovic]], _Diagrammatic sets and rewriting in weak higher categories_, ([arXiv:2007.14505](https://arxiv.org/abs/2007.14505))

For an updated version, together with results for higher groupoids:
 
* {#ChanavatHadzihasanovic2024} Clémence Chanavat, Amar Hadzihasanovic, _Diagrammatic sets as a model of homotopy types_, 2024 ([arXiv:2407.06285](https://arxiv.org/abs/2407.06285v1))



[[!redirects diagrammatic sets]]