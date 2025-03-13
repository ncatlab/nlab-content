# Contents
* this block creates the table of contents, leave as is
{: toc}

## Idea

Atoms are [[regular directed complex|regular directed complexes]] with a maximal cell. With the correct notion of maps, they are a contender for [[geometric shape for higher structures|geometric shape for higher categories]].

## Definition 

\begin{definition}
**(atom)**\linebreak
An **atom** is a [[regular directed complex]] whose underlying poset has a maximal element.
\end{definition}

In [[regular directed complex]], we defined a **morphism** $f \colon P \to Q$ between regular directed complex as a function of the underlying posets that respects both input and output faces, that is, $f$ induces a bijection between $\Delta^\alpha x$ and $\Delta^\alpha f(x)$. 

This notion is, albeit well-suited for defining regular directed complexes, quite restrictive. For instance, the point $\mathbf{1}$ is not a terminal object in this category. In fact, if there is a morphism $f \colon P \to Q$, then $\dim P \le \dim Q$, which prevent using morphisms for modelling degeneracies.

Instead, we define a less restrictive notion of map, that strictly generalizes the morphisms.

\begin{remark}
    In the following definition, we will impose two conditions (finality, and fibration) 
\end{remark}

\begin{definition}
**(cartesian map of regular directed complex)**\linebreak
A **cartesian map** $f \colon P \to Q$ between regular directed complexes is a function of the underlying set such that

*  $f$ is a [[Grothendieck fibration]] (in particular, $f$ is order-preserving);
*  for all $x \in P$, $\alpha \in \{ -, + \}$, $n \geq 0$,
$$
    f(\partial^\alpha_n x) = \partial^\alpha_n f(x);
$$
*  for all $x \in P$, the restriction and corestriction of $f \colon \partial^\alpha_n x \to \partial^\alpha_n f(x)$ is [[final functor|final]];  

\end{definition}

\begin{remark}
In the previous definition, the [[Grothendieck fibration|fibration]] and [[final functor|finality]] condition implicitely see the underlying posets as categories.
\end{remark}

This new definition of cartesian map generalizes the notion of morphism in the following sense:
\begin{lemma}
    Any morphism of regular directed complex is a cartesian map, and a cartesian map is a morphism if and only if it is dimension-preserving.
\end{lemma}

\begin{definition}
**(atom category)**\linebreak
We define the **atom category**, that we write **$\odot$**, to be a [[skeleton]] of the category of atoms and cartesian maps.  
\end{definition}

## Properties

\begin{theorem}
The category $\odot$ is a strict [[generalized Reedy category|Cisinski generalized Reedy category]] (Def 2.4), where

*  the degree map $d \colon \odot \to \mathbb{N}$ is given by the dimension $U \mapsto \dim U$;
*  the wide subcategory $\odot^+$ is the cartesian maps that are injective;
*  the wide subcategory $\odot^-$ is the cartesian maps that are surjective;

\end{theorem}

\begin{remark}
    We use the prefix "strict" in the previous definition to mean that the factorisation system $(\odot^-, \odot^+)$ is [[strict factorization system|strict]] rather than merely [[orthogonal factorization system|orthogonal]] 
\end{remark}

In particular, any cartesian map of atom factors uniquely as a surjection, which we also call a **collapse**, followed by an inclusion, which we also call an **inclusion**, and any cartesian map between atoms of the same dimension has to be the identity.

The inclusions are very-well behaved, we have
\begin{proposition}
Let $U$ be an atom, there is a one-to-one correspondance between elements of $U$ and inclusions $V \hookrightarrow U$ given by 
$$
    x \in U \mapsto (\iota_x \colon \mathrm{cl}(x) \hookrightarrow U)
$$
\end{proposition}
\begin{proof}
    If $\iota \colon V \hookrightarrow U$ is an inclusion, there is an isomorphisms $V \cong \iota(V) \subseteq U$, since $V$ is an atom, so is $\iota(V)$, whose maximal element defines an element $x \in U$ which uniquely characterize $\iota$ (since the category is skeletal).   
\end{proof}

However, the precise behavior of collapses is not as explicit as in the case of [[simplex]] or [[category of cubes|cube]] categories. Nevertheless, we have 
\begin{lemma}
The point $\mathbf{1}$ is the terminal object of $\odot$. 
\end{lemma}
as well as the Cisinski-Eilenberg-Zilber axiom which state that

*  every degeneracy has a section;
*  if two degeneracies have the same set of section, they are equal.


### Stability of operations

\begin{proposition}
The [[regular directed complex#operations|Gray product, the join, and the suspension]] are again atoms. Therefore:      
\end{proposition}

\begin{proposition}
$(\odot, \otimes, \mathbf{1})$ is a [[monoidal category]].
\end{proposition}

Notice that the only reason why the join $\star$ does not make a monoidal category is because its unit $\emptyset$ is only a regular directed complex, but not an atom.

\begin{definition}
**(oriented simplex)**\linebreak
The **$n$-th oriented simplex** $\vec{\Delta}_n$ is defined inductively by

*  $\vec{\Delta}_0 \coloneqq \mathbf{1}$;
*  inductively, $\vec{\Delta}_n \coloneqq \vec{\Delta}_{n - 1} \star \mathbf{1}$;

We call $\vec{\Delta}$ the [[full subcategory]] of $\odot$ on oriented simplices.
\end{definition}

\begin{theorem}
The category $\vec{\Delta}$ is isomorphic to the [[simplex category]]. More in details, the coface map $d_i \colon \vec{\Delta}_{n - 1} \to \vec{\Delta}_{n}$ can be reconstructed as
$$
    \mathrm{id} \star ! \star \mathrm{id} \colon \vec{\Delta}_{i - 1} \star \emptyset \star \vec{\Delta}_{n - i - 1} \hookrightarrow \vec{\Delta}_{i - 1} \star \mathbf{1} \star \vec{\Delta}_{n - i - 1}
$$
and the codegeneracy $s_i \colon \vec{\Delta}_{n + 1} \to \vec{\Delta}_{n}$ can be reconstructed as
$$
\mathrm{id} \star ! \star \mathrm{id} \colon \vec{\Delta}_{i - 1} \star \vec{\Delta}_1 \star \vec{\Delta}_{n - i - 1} \hookrightarrow \vec{\Delta}_{i - 1} \star \mathbf{1} \star \vec{\Delta}_{n - i - 1}.
$$
\end{theorem}


### Test category

\begin{theorem}
The category $\odot$ is a [[test category]]. 
\end{theorem}
\begin{proof}
    As $\mathbf{1}$ is the terminal object, $\odot$ is aspherical. Therefore, it suffices to prove that $\odot$ is a local test category. This follows from [Cisinski06, Corollaire 8.2.16](#Cisinski06), using the [[cylinder object]] $U \mapsto \vec{I} \otimes U$, extend via [[Day convolution]] on presheaves. Since atoms are stable under Gray products, the map $I \otimes U \twoheadrightarrow U$ is representable, so is a weak equivalence (in the sense of [[test category|here]]).
\end{proof}

In fact, $\odot$ is even a strict test category.

## Related concepts

*  A presheaf over $\odot$ is a [[diagrammatic set]]
*  [[simplex category]]
*  [[regular directed complex]]
*  [[geometric shape for higher structures|geometric shape for higher categories]]


## References

For the basic properties of atoms, and their relations to cube, simplices, and other shapes:

* {#Hadzihasanovic2024} [[Amar Hadzihasanovic]], _Combinatorics of higher-categorical diagrams_, 2024 ([link](https://arxiv.org/abs/2404.07273))

Statements about Eilenberg-Zilber category and test category are proved here:

* {#ChanavatHadzihasanovic2024} Clémence Chanavat, Amar Hadzihasanovic, _Diagrammatic sets as a model of homotopy types_, 2024 ([arXiv:2407.06285](https://arxiv.org/abs/2407.06285v1))

In part 8, we find a lot of results to prove that Eilenberg-Zilber related categories are test categories:

* {#Cisinski06} [[Denis-Charles Cisinski]], _Les préfaisceaux comme modèles des types d'homotopie_, Astérisque 308, 2006 ([doi:10.24033/ast.715](https://smf.emath.fr/publications/les-prefaisceaux-comme-modeles-des-types-dhomotopie), [NUMDAM](http://www.numdam.org/item/AST_2006__308__R1_0/))
