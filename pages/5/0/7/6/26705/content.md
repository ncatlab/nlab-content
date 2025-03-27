[[!redirects Algebraic pattern]]

#Contents#
* table of contents
{:toc}


## Idea

An [[algebraic pattern]] is a blueprint for a notion of functors on a fixed category satisfying a [[Segal condition]], suitable for formalizing homotopy-coherent algebra in the Cartesian setting.

## Definitions

\begin{definition}\label{Algebraic pattern definition}

An **[[algebraic pattern]]** is an [[(∞,1)-category]] $\mathcal{O}$ together with the following data:

* a pair of [[wide subcategories]] $\mathcal{O}^{\mathrm{int}},\mathcal{O}^{\mathrm{act}} \subset \mathcal{O}$, whose morphisms are called _inert_ and _active_ morphisms, and

* a [[full subcategory]] $\mathcal{O}^{\mathrm{el}} \subset \mathcal{O}^{\mathrm{int}}$, whose objects are called _elementary objects_,

subject to the condition that for all $f:X \rightarrow X'$ in $\mathcal{O}$, the space of factorizations of $f$ of the form $X \xrightarrow{i} Y \xrightarrow{a} X'$ with $i \in \mathcal{O}^{\mathrm{int}}$ and $r \in \mathcal{O}^{\mathrm{act}}$ is contractible.
\end{definition}

The pair $(\mathcal{O}^{\mathrm{int}},\mathcal{O}^{\mathrm{act}})$ is a [[factorization system]], with no assumptions made about orthogonality.

It is customary to abusively refer to the quadruple $(\mathcal{O},\mathcal{O}^{\mathrm{int}},\mathcal{O}^{\mathrm{act}},
\mathcal{O}^{\mathrm{el}})$ simply as $\mathcal{O}$, and to decorate inert morphisms as $\mapsto$ and active morphisms as $\rightsquigarrow$.
These are so defined in order to define _Segal objects_.


\begin{definition}\label{Segal object definition}
Let $\mathcal{O}$ be an algebraic pattern and $\mathcal{C}$ a complete [[(∞,1)-category]]. A **Segal $\mathcal{O}$-object in $\mathcal{C}$** is a functor
$$
  F:\mathcal{O} \rightarrow \mathcal{C}
$$
subject to the condition that, for all $Z \in \mathcal{O}$, the canonical morphism
$$
  F(Z) \rightarrow \lim_{\stackrel{Z \mapsto E}{E \in \mathcal{O}^{\mathrm{el}}}}F(E)
$$
is an equivalence.
\end{definition}

By Lemma 2.9 of [Chu-Hangseng](#Chu19), these are equivalently given as functors $F:\mathcal{O} \rightarrow \mathcal{C}$ whose restriction to $\mathcal{O}^{\mathrm{int}}$ are right [[(∞,1)-Kan extension|Kan extended]] from $\mathcal{O}^{\mathrm{el}}$.

One example of this is the pattern $\mathbb{F}_*^{\flat}$, whose underlying category is the category $\mathbb{F}_*$ of finite pointed sets with 

* inert morphisms given by those $\phi:\langle n \rangle \rightarrow \langle m \rangle$ with $|\varphi^{-1}(j)| = 1$ for all $j \neq *$, 

* active morphisms given by those $\phi$ with $\phi^{-1}(*) = \{*\}$, and

* elementary objects spanned by $\langle 1 \rangle$.

The resulting [[(∞,1)-category]] of Segal $\mathbb{F}_*^{\flat}$-objects in $\mathcal{C}$ consists of the [[Γ-space|Γ-objects]] in $\mathcal{C}$; hence they are equivalent to [[E-∞ algebra|E∞ algebras]] in $\mathcal{C}$ with the [[cartesian monoidal (∞,1)-category|cartesian symmetric monoidal structure]]. 

In particular, applying this to the category $\mathrm{Cat}_\infty$ of small [[(∞,1)-categories]] and applying [[(∞,1)-Grothendieck construction|unstraightening]]  yields a distinguished subcategory of [[cocartesian fibrations]] over $\mathcal{O}$ satisfying [[Segal conditions]].
These are sometimes called _Segal fibrations_.

Relaxing the condition that Segal fibrations have underlying [[cocartesian fibrations]] then yields the following notion, [originally](#chu19) called _weak Segal fibrations_.


\begin{definition}
  Let $\mathcal{O}$ be an algebraic pattern. 
  A functor $\pi:\mathcal{P} \rightarrow \mathcal{O}$ is called a _fibrous pattern_ if it satisfies the following conditions:
  
  * $\mathcal{P}$ has $\pi$-cocartesian lifts for inert morphisms in $\mathcal{O}$.

  * For all $Z \in \mathcal{O}$, the canonical map 
    $$\mathcal{P} \times_{\mathcal{O}}     \mathcal{O}^{\mathrm{act}}_{/Z}   \rightarrow   \mathcal{O}^{\mathrm{act}}_{/Z}     \times_{     \lim_{E \mapsto Z}     \mathcal{O}^{\mathrm{act}}_{/E}}   \left(\lim_{E \mapsto Z} \mathcal{P}      \times_{\mathcal{O}}       \mathcal{O}^{\mathrm{act}}_{/E},\right)$$ 
    is an equivalence, where the limits run across all inert maps $E \mapsto Z$ with elementary domain.

\end{definition}

One of the main reasons to use algebraic patterns over the categorical patterns of [Higher Algbera](https://people.math.harvard.edu/~lurie/papers/HA.pdf) is the relative ease of constructing functoriality in families of examples.
The central concept driving this is that of a Segal morphism.


\begin{definition}
  A functor of algebraic patterns $F:\mathcal{O} \rightarrow \mathcal{P}$ is called a

* _Segal morphism_ if the pullback functor 
$F^*:\mathrm{Fun}(\mathcal{P}, \mathcal{C}) \rightarrow \mathrm{Fun}(\mathcal{O}, \mathcal{C})$
 preserves Segal objects for all $\mathcal{C}$, and a

* _strong Segal morphism_ if for all $Z \in \mathcal{O}$, the associated functor  $\mathcal{O}^{\mathrm{el}}_{/Z} \rightarrow \mathcal{O}^{\mathrm{el}}_{/F(Z)}$ is [[final (infinity,1)-functor|initial]].

\end{definition}


By Lemma 4.5 of [Chu-Haugseng](#Chu19), for a functor of algebraic patterns to be a Segal morphism, it suffices to check that $F^*$ preserves Segal spaces. As developed in [Barkan-Haugseng-Steinebrunner](#Barkan22), (strong) Segal morphisms induce functors on fibrous patterns in the presence of mild categorical "soundness" or "extendability" conditions on the patterns involved.




## Examples

* By Proposition 4.1.7 of [Barkan-Haugseng-Steinebrunner](#Barkan22), $\mathbb{F}_*^{\flat}$-fibrous patterns are precisely the [[(∞,1)-operads]];
  defining the pattern structure $\mathbb{F}_*^{\natural}$ on $\mathbb{F}_*$ with the usual inert and active morphisms together with $\emptyset, \langle 1 \rangle$ as elementary objects, the $\mathbb{F}_*^{\natural}$-fibrous patterns are the [[generalized (∞,1)-operads]].

* More generally, when G is a finite group, the [[G-category]] of finite pointed [[G-sets]] admits a similar pattern structure $\underline{\mathbb{F}}_{G,*}^{\flat}$, whose Segal objects are the [[G-commutative monoids]] and whose fibrous patterns are precisely the [[G-∞-operads]].

Both of these examples are more easily presented via span patterns.
The theorem relating these is Proposition 5.2.14 of [Barkan-Haugseng-Steinebrunner](#Barkan22).
They define a pattern $\mathrm{Span}(\mathbb{F}_G)$ whose inert maps are backwards, active maps are forwards, and elementary objects are transitive [[orbit category|G-sets]].

\begin{theorem}
  The forgetful functor $\mathbb{F}_{G,*} \rightarrow \mathrm{Span}(\mathbb{F}_G)$ lifts to a Segal morphism of patterns, which induces an equivalence on the categories of Segal objects and fibrous patterns.
\end{theorem}

* The category $\Delta^{\op}$ has two pattern structures $\Delta^{\op,\natural}, \Delta^{\op, \flat}$, which parameterize [[Segal spaces]] (i.e. [[∞-categories]]) and [[E-n algebra|E1 algebras]], respectively.

* The $n$-fold product $\Delta^{\op, n, \natural}$ parameterizes $n$-fold Segal spaces, i.e. [[n-fold category|n-fold ∞-categories]]; the $n$-fold product $\Delta^{\op, n, \flat}$ models $\mathbb{E}_n$-spaces.

* The $n$-fold [[categorical wreath product|wreath product]] $\Theta_n := \Delta \wr \cdots \wr \Delta$ has on its opposite two interesting pattern structures;
  the pattern $\Theta_n^{\op,\natural}$ models [[(∞,n)-categories]], and the pattern $\Theta_n^{\op,\flat}$ models $\mathbb{E}_n$-spaces.

* Let $\mathcal{S}_m$ denote the $\infty$-category of [[m-finite spaces]]. Then, the pattern $\mathrm{Span}(\mathcal{S}_{m})$ models [[m-commutative monoids]].

* The opposite $\Omega^{\op}$ of the dendroidal category of [Moerdijk-Weiss](https://arxiv.org/abs/math/0701293) has a pattern structure $\Omega^{\op,\natural}$ whose segal objects are the Dendroidal Segal spaces of [Cisinski-Moerdijk](https://arxiv.org/abs/1010.4956), hence they are [[operads]].

## Related concepts

* [[Segal condition]]

* [[(∞,n)-categories]], 

* [[operad]]

* [[lawvere theory]]

* [[Parametrized Higher Category Theory and Higher Algebra]]

## References

Original references:

* {#Chu19} Hongyi Chu, [[Rune Haugseng]], _Homotopy-coherent algebra via Segal conditions_, (2019) ([arXiv:1907.03977](https://arxiv.org/abs/1907.03977))

* {#Barkan22} [[Shaul Barkan]], [[Rune Haugseng]], [[Jan Steinebrunner]], _Envelopes for Algebraic Patterns_, (2022) ([arXiv:2208.07183](https://arxiv.org/abs/2208.07183))

* Hongyi Chu, [[Rune Haugseng]], _Enriched homotopy-coherent structures_, (2023) ([arxiv:2308.11502](https://arxiv.org/abs/2308.11502)) 

Slice patterns and morita equivalences appear in:

* [[Shaul Barkan]], _Arity Approximation of ∞-Operads_, (2022) ([arXiv:2207.07200](https://arxiv.org/abs/2207.07200))

[[!redirects segal object]]