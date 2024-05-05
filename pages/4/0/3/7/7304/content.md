
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _Boardman-Vogt tensor product_ is a natural [[tensor product]] on [[symmetric operads]]. It makes the category [[Operad]] of colored [[symmetric operads]] over [[Set]] into a [[closed monoidal category]].

## Definition

### In the 1-category of symmetric operads

All [[operads]] in the following are colored [[symmetric operads]] enriched over [[Set]], equivalently [[symmetric multicategories]].

Let $\mathcal{P}$ be an operad over a set of colors $C$, and $\mathcal{Q}$ be an operad over a set of colors $D$.

Their **Boardman-Vogt tensor product** $\mathcal{P} \otimes_{BV} \mathcal{Q}$ is the operad whose set of colors is $C \times D$, and whose operations are given by generators and relations as follows:

There is one generating operation for every pair $(p,d)$ with $p \in \mathcal{P}(c_1, \cdots, c_n; c)$ and with $d \in D$, denoted

$$
  p \otimes d 
  \in 
  \mathcal{P} \otimes_{BV} \mathcal{Q}(
    (c_1,d), \cdots, (c_n,d); (c,d)
  )
$$

and for each pair $(c,q)$ with $c \in C$ and $q \in \mathcal{Q}(d_1, \cdots, d_n; d)$, denoted

$$
  c \otimes q
  \in
  \mathcal{P}\otimes_{BV} \mathcal{Q}(
   (c, d_1), \cdots, (c, d_n);
   (c,d)
  )
$$

for all $n \in \mathbb{N}$. These are subject to the following relations

1. The tensor product $c \otimes (-)$ with $c \in C$ respects the composition in $\mathcal{Q}$, and the tensor product $(-) \otimes d$ with $d \in D$ respects the composition in $\mathcal{P}$ and both respect the action of the [[symmetric group]] on the operations.
   
   Equivalently this means that for all $c \in C$ tensoring with $c$ extends to a morphism of operads

   $$
     \mathcal{Q} \to \{c\} \otimes_{BV}\mathcal{Q}
   $$

   and for all $d \in D$ a morphism of operads

   $$
     \mathcal{P} \to \mathcal{P} \otimes_{BV} \{d\}
     \,.
   $$

1. The operations  in $\mathcal{P}$ and $\mathcal{Q}$ [[distributive law|distribute]] over each other in $\mathcal{P} \otimes_{BV} \mathcal{Q}$ in the evident sense (...).

### In the $\infty$-category of $\infty$-operads

Let $\mathrm{Cat}_{\infty,/\mathbb{F}_*}^{\mathrm{Int}-\mathrm{cocart}} \subset \mathrm{Cat}_{\infty,/\mathbb{F}_*}$ denote the (non-full) subcategory of functors to finite pointed sets which posses cocartesian lifts over inert morphisms. 

The full subcategory $\mathrm{Op}_\infty \subset \mathrm{Cat}_{\infty,/\mathbb{F}_*}^{\mathrm{Int}-\mathrm{cocart}}$ spanned by the $\infty$-operads of Lurie is localizing; write $L_{\mathrm{Op}}: \mathrm{Cat}_{\infty,/\mathbb{F}_*}^{\mathrm{Int}-\mathrm{cocart}} \rightarrow \mathrm{Op}_\infty$ for its localization functor.

Then, given $\mathcal{O}^{\otimes},\mathcal{P}^{\otimes} \in \mathrm{Op}_\infty$, their **Boardman-Vogt tensor product** is the localization
$$
    \mathcal{O}^{\otimes} \otimes_{\mathrm{BV}} \mathcal{P}^{\otimes} := L_{\mathrm{Op}} \left( \mathcal{O}^{\otimes} \times \mathcal{P}^{\otimes} \rightarrow \mathbb{F}_* \times \mathbb{F}_* \xrightarrow{\wedge} \mathbb{F}_* \right).
$$



## Properties

### Closed monoidal structure
 {#ClosedMonoidalStructure}

+-- {: .num_prop}
###### Proposition

Equipped with the Boardman-Vogt tensor product, [[Operad]] is a [[closed monoidal category|closed]] [[symmetric monoidal category]].

=--

See for instance the proof provided in ([Weiss, theorem 2.22](#Weiss)).

This implies directly several useful statements about the BV-tensor product

+-- {: .num_cor}
###### Corollary

* The BV tensor products preserves [[colimits]] of operads in each variable separately.

=--

We write in the following

$$
  [-,-] : Operad^{op} \times Operad \to Operad
$$

for the corresponding [[internal hom]] (leaving a subscrip "${}_{BV}$" implicit.)

+-- {: .num_prop #InternalHomOperadAsAlgebraOperad}
###### Proposition

For $P, Q \in $ [[Operad]], the internal hom operad $[P, Q]$ has

* as colors the [[algebra over an operad|P-algebras]] in $Q$;

* as unary operations the $P$-algebra homomorphisms in $Q$. 

=--

See ([Weiss, lemma 2.23](#Weiss)).

We may therefore speak of $[P,Q]$ as being the **operad of $P$-algebras in $Q$.



+-- {: .num_example}
###### Example

Write $Set$ for the operad induced by the [[cartesian monoidal category|cartesian]] [[symmetric monoidal category]] structure on [[Set]]. Then for $P$ any operad, the vertices and unary operations of the internal hom operad $[P,Set]$ form the ordinary [[algebra over an operad|category of algebras over]] $P$ in $Set$.

=--



+-- {: .num_corollary}
###### Corollary

For $P_1, P_2, E \in Operad$, the category of $P_1$-algebras in $P_2$-algebras in $E$ is equivalent to the category of $P_2$-algebras in $P_1$-algebras in $E$. 

=--

In view of prop. \ref{InternalHomOperadAsAlgebraOperad} this is the statement of the [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]] structure $(Operad, \otimes_{BC})$:

$$
  [P_1, [P_2, E]] \simeq [P_1 \otimes_{BV} P_2, E]
  \simeq 
  [P_2 \otimes_{BV} P_1, E]
  \simeq
  [P_2, [P_1, E]]
  \,.
$$


### The $\infty$-categorical universal property of the BV-tensor product {#Bifunctorprop}
  An arrow $\mathcal{O}^{\otimes} \times \mathcal{P}^{\otimes} \rightarrow \mathcal{Q}^{\otimes}$ is a **bifunctor of $\infty$-operads** if it extends to a commutative diagram 

\begin{centre}
    \begin{xymatrix}
        \mathcal{O}^{\otimes} \times \mathcal{P}^{\otimes} \ar[r] \ar[d] 
        & \mathcal{Q}^{\otimes} \ar[d]\\
         \mathbb{F}_* \times \mathbb{F}_* \ar[r] & \mathbb{F}_*
    \end{xymatrix}
\end{centre}

sending pairs of (cocartesian lifts of) inert morphisms in $\mathcal{O}^{\otimes} \times \mathcal{P}^{\otimes}$ to (cocartesian lifts of) inert morphisms in $\mathcal{Q}$.

Let $\mathrm{BiFun}(\mathcal{O}^{\otimes},\mathcal{P}^{\otimes}; \mathcal{Q}^{\otimes}) \subset \mathrm{Fun}_{/\mathbb{F}_*}(\mathcal{O}^{\otimes} \times \mathcal{P}^{\otimes}, \mathcal{Q}^{\otimes})$ be the full subcategory spanned by functors satisfying the above inert morphism condition.

\begin{proposition}
There is an equivalence of $\infty$-categories
$$
  \mathrm{Alg}_{\mathcal{O}^{\otimes} \otimes_{\mathrm{BV}} \mathcal{P}^{\otimes}}(\mathcal{Q}^{\otimes}) \simeq \mathrm{BiFun}(\mathcal{O}^{\otimes},\mathcal{P}^{\otimes}; \mathcal{Q}^{\otimes}) .
$$
\end{proposition}

### The symmetric monoidal $\infty$-categorical universal property
The following is Theorem E of [Barkan-Steinebrunner 23](#Barkan23)
\begin{theorem}
  The [canonical tensor product of symmetric monoidal $\infty$-categories](https://ncatlab.org/nlab/show/tensor+product+of+commutative+monoids#in_category_theory) uniquely restricts to a tensor product on $\mathrm{Op}_\infty$ such that the [[symmetric monoidal envelope]] is a symmetric monoidal functor.
\end{theorem}

This is not the symmetric monoidal structure constructed in Higher algebra; however, both it and that of Higher algebra have tensor functors satisfying the above [universal property](#Bifunctorprop), so their tensor functors agree.

Lurie's tensor product comes from an ad-hoc construction involving a left-derived functor from a seldom-used [[monoidal model category]], which doesn't obviously satisfy many nice properties; thus it is likely that the above theorem constructs the "correct" coherences on $\otimes_{\BV}$, and those in [[Higher Algebra]] may be "incorrect."

### Connectivity and the Eckmann-Hilton argument

Let $\mathcal{A}_2^{\otimes}$ be the free unital [[(∞,1)-operad]] with a binary operation (so that it's Stasheff's 2nd operad, i.e. $\mathcal{A}_2$-algebras are [[unital magmas]]). 
The [[Eckmann-Hilton argument]] states that the canonical map of [[(∞,1)-operads]] $\mathcal{A}_2^{\otimes} \otimes_{\mathrm{BV}} \mathcal{A}_2^{\otimes} \rightarrow \mathrm{Comm}^{\otimes}$ induces an equivalence
$$
  \mathrm{Alg}_{\mathcal{A}_2} \mathrm{Alg}_{\mathcal{A}_2}^{\otimes}(\mathcal{C}) \simeq \mathrm{Alg}_{\mathcal{A}_2 \otimes_{\mathrm{BV}} \mathcal{A}_2}(\mathcal{C}) \rightarrow \mathrm{CAlg}(\mathcal{C})
$$
whenever $\mathcal{C}$ is a symmetric monoidal 1-category.

We say that a reduced [[(∞,1)-operad]] $\mathcal{O}^{\otimes}$ is $n$-connected if the canonical map $\mathcal{O}^{\otimes} \rightarrow \mathrm{Comm}^{\otimes}$ induces equivalences on the respective categories of algebras in symmetric monoidal $n$-categories.

The following result is proved in [Schlank-Yanovski 19](#Schlank19), where it is called the $\infty$-categorical [[Eckmann-Hilton argument]].

\begin{theorem}{#EH}
  If $\mathcal{O}^{\otimes}$ is $d_{\mathcal{O}}$-connected and $\mathcal{P}^{\otimes}$ is $d_{\mathcal{P}}$-connected, then the Boardman-Vogt tensor product $\mathcal{O}^{\otimes} \otimes_{\mathrm{BV}} \mathcal{P}^{\otimes}$ is $(d_{\mathcal{O}} + d_{\mathcal{P}} + 2)$-connected.
\end{theorem}

## Examples

### Infinite tensor products of reduced $\infty$-operads are $\mathrm{Comm}$.

Let $\mathcal{O}^{\otimes}$ be a reduced $\infty$-operad other than $\mathbb{E}_0$, so that there is a canonical map of operads $\mathrm{triv}^{\otimes} \rightarrow \mathcal{O}^{\otimes}$, inducing a teloscope
$$
  \mathcal{O}^{\otimes \infty} \coloneqq \colim \left( \mathcal{O}^{\otimes} \rightarrow \mathcal{O}^{\otimes 2} \rightarrow \mathcal{O}^{\otimes 3} \rightarrow \cdots \right)
$$

The above [connectivity bound](#EH) implies the following corollary, which may be viewed as an _operadic Eilenberg swindle_.

\begin{corollary}
  The canonical map $\mathcal{O}^{\otimes \infty} \rightarrow \mathrm{Comm}^{\otimes}$ is an equivalence.
\end{corollary}

### Dunn's additivity theorem

Let $C_n$ be the topological [[little n-cubes operad]].
Then, the canonical maps $C_n,C_m \rightarrow C_{n+m}$ together yield a map $\mu:C_n \otimes C_m \rightarrow C_{n+m}$.
In the case $n = 1$, [Dunn 88](#Dunn88) constructs a diagram

\begin{centre}
    \begin{xymatrix}
        C_n \otimes C_m \ar[rr]^\mu \ar[d]^{\mu'}
        && C_{n+m}\\ 
        C_n | C_m 
        & D_{n} | D_{m} \ar@{=}[r] \ar@{^{(}->}[l]^\simeq
        & D_{n+m} \ar@{^{(}->}[u]^\simeq
    \end{xymatrix}
\end{centre}

where $D_{n+m}$ us the operad of decomposable little $(n+m)$-cubes and $C_{n} | C_{m}$ is the image of $\mu$. The difficult statement in [Dunn 88](#Dunn88) is the statement that $\mu'$ is a local $\Sigma$-equivalence.
This implies the following.
\begin{theorem}
  The topological operads $C_n \otimes C_m \simeq C_{n+m}$ are related by a zigzag of local $\Sigma$-equivalences.
\end{theorem}
This theorem is slightly unusual, as the operad $C_n$ is _not_ cofibrant, and the tensor product in the statement is _underived_.
Simpler proofs of this statement involve the thesis [Brinkmeier 00](#Brinkmeier00) and the recent paper [Barata-Moerdijk 22](#Barata22).

The corresponding statement for the _derived_ tensor product is proved as Theorem 5.1.2.2 in [[Higher Algebra]].

\begin{theorem}
  The canonical map of $\infty$-operads $\mathbb{E}_{n}^{\otimes} \otimes \mathbb{E}_{m}^{\otimes} \rightarrow \mathbb{E}_{n + m}^{\otimes}$ is an equivalence;
  hence for any symmetric monoidal $\infty$-category $\mathcal{C}$, the pullback functor
  $$
    \mathrm{Alg}^{\otimes}_{\mathbb{E}_{n+m}}(\mathcal{C}) \rightarrow \mathrm{Alg}_{\mathbb{E}_n}^{\otimes} \mathrm{Alg}_{\mathbb{E}_m}^{\otimes}(\mathcal{C}) 
  $$
  is an equivalence.
\end{theorem}


## Related concepts

* The Boardman-Vogt tensor product extends from operads to a tensor product on [[dendroidal sets]]. See there for more details.

* [[tensor product of monads]]

## References

The original reference is

* [[Michael Boardman]], [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological spaces_, Lecture Notes in Mathematics, Vol. 347, Springer-Verlag, (1973).

A review is in

* {#Weiss} [[Ittay Weiss]], _From Operads to Dendroidal Sets_, in _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ AMS (2011) ([arXiv:1012.4315](http://arxiv.org/abs/1012.4315))

see around def. 2.21 there.

Underived proofs of Dunn's additivity theorem include

* {#Dunn88} Gerald Dunn, _Tensor product of operads and iterated loop spaces._ (1988) ([pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/Dunn.pdf))

* {#Brinkmeier00} Michael Brinkmeier, _On Operads_. PhD thesis, Universitat Osnabrüeck, 2000.

* {#Barata22} [[Miguel Barata]], [[Ieke Moerdijk]], _On the additivity of the little cubes operads_ (2022) ([arXiv:2205.12875](https://arxiv.org/abs/2205.12875))

The $\infty$-categorical universal property is Definition 2.2.5.3 in the following textbook;
an $\infty$-operadic version of Dunn's additivity theorem is Theorem 5.1.2.2.

* [[Higher Algebra]].

It is reviewed in the form used above in the lecture notes

* {#Haugseng23} [[Rune Haugseng]], _An allegedly somewhat friendly introduction to $\infty$-operads_ ([pdf](https://folk.ntnu.no/runegha/iopd.pdf)) 

It was realized to be compatible with the [[symmetric monoidal envelope]] in

* {#Barkan23} [[Shaul Barkan]], [[Jan Steinebrunner]], _Segalification and the Boardman-Vogt tensor product_, [arXiv:2301.08650](https://arxiv.org/abs/2301.08650).

The ∞-categorical [[Eckmann-Hilton argument]] is due to

* {#Schlank19} [[Tomer Schlank]], [[Lior Yanovski]], *The ∞-Categorical Eckmann-Hilton Argument*, Algebr. Geom. Topol. 19 (2019) 3119-3170 ([arXiv:1808.06006](https://arxiv.org/abs/1808.06006), [doi:10.2140/agt.2019.19.3119](https://doi.org/10.2140/agt.2019.19.3119))
