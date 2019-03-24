A **tangent bundle category** is a [[category]] equipped with a "[[tangent bundle]]" [[endofunctor]] satisfying some natural axioms.

Usually these are called simply **tangent categories**, but on the nLab the page [[tangent category]] is about "the tangent category of a given category" constructed by abelianization.  In other words, tangent bundle categories are about *abstraction* of the tangent bundle construction, while tangent categories are a *categorification* thereof (in some vague sense).

## Definition

Tangent bundle categories have three equivalent definitions: the first is due to Rosicky and was rediscovered/refined by Cockett and Cruttwell. In his thesis, Poon Leung found an equivalent definition of tangent categories using an category structure that acts as an abstract Weil prolongation, and later Richard Garner gave a definition of a tangent category as a sort of enriched category.

### Classical Definition

Tangent bundle categories were originally introduced by to model the behaviour of the tangent bundle on the category of smooth manifolds, and of [[microlinear spaces]] in a [[smooth topos]]. For smooth manifold $M$ and a point $m \in M$, on may consider a coordinate patch $U \subset \mathbb{R}^n$ around $m$. Looking at the tangent space of $U$, we see $T(U) \cong U \times \matbb{R}^n$, and similarly
$T^2(U) \cong (U \times \mathbb{R}^n) \times (\mathbf{R^n} \times \mathbb{R}^n)$. Besides the vector bundle structures on $p, p_T, T(p)$, there are two important morphisms:

* The vertical lift: $\ell(m,v) = (m,0,0,v)$.

* The canonical flip $c(m,u,v,w) = (m,v,u,w)$. 

These morphisms are important in the axiomatization of differential structure given in cartesian differential categories.

#### Additive bundles

Tangent categories were originally defined by Rosicky using abelian group bundles, however Cockett and Cruttwell's definition uses commutative monoid bundles in order to capture examples of tangent structure that arise in theoretical computer science.

An additive bundle $q: E \to B$ in a category $\mathbb{X}$ is a commutative monoid in $\mathbb{X}/B$. A bundle morphism $(f,g): q \to q'$ is _additive_ if it preserves the fibered commutative monoid structure.

#### Tangent structure

A tangent structure $\mathbb{T}$ on a category $\mathbb{X}$ is a tuple:

$$
  \left(
    T: \mathbb{X} \to \mathbb{X}, p: T \Rightarrow \mathsf{id},
    0: \mathsf{id} \Rightarrow \mathbb{X}, +: T {}_p\times_p T \Rightarrow R,
    \ell: T \Rightarrow T^2, c: T^2 \Rightarrow T^2
  \right)
$$

Denote pullback powers of $p$ as $T_n(M)$. 

* $T$ preserves all pullback powers of $p$.

* $(p, +,0)$ is a natural additive bundle. 

* The flip $c$ is a natural involution $cc = 1_{T^2M}$,
  and the following bundle morphism is additive:
  \begin{center}
    \begin{tikzcd}
      T^2(M) \ar[r, "c"] \ar[d, "p"] & T^2(M) \ar[d, "T(p)"] \\
      T(M) \ar[r, equals] & T(M)
    \end{tikzcd}
  \end{center}
* The vertical lift $\ell$ gives an additive bundle morphism $(\ell, 0): p \Rightarrow T(p)$.
  


* We also require the following coherences between the vertical lift and the canonical flip: 

\begin{center}
    \begin{tikzcd}
      T \ar[r, "\ell"] \ar[d, "\ell"'] & T^2 \ar[d, "T(\ell)"] \\
      T^2 \ar[r, "\ell_T"] & T^3
    \end{tikzcd}
\end{center}
\begin{center}
    \begin{tikzcd}
      T^3 \ar[d, "c_T"] \ar[r, "T(c)"] & T^3 \ar[r, "c_T"] & T^3 \ar[d, "T(c)"] \\
      T^3 \ar[r, "T(c)"] & T^3 \ar[r, "c_T"] & T^3
    \end{tikzcd}
\end{center}

\begin{center}
    \begin{tikzcd}
      T^2 \ar[r, "\ell_T"] \ar[d, "c"'] & T^3 \ar[r, "T(c)"] & T^3 \ar[d, "c_T"] \\
      T^2 \ar[rr, "T(\ell)"] && T^3
    \end{tikzcd}
\end{center}
\begin{center}
    \begin{tikzcd} T \ar[r, "\ell"] \ar[rd, "\ell"] & T^2 \ar[d, "c"] \\ & T \end{tikzcd}
\end{center}

In the monoidal category $[\mathbb{X}, \mathbb{X}]$, the first diagram corresponds to $\ell: T \Rightarrow TT$ being a cosemigroup. The second diagram corresponds to $c: TT \Rightarrow TT$ acting as a symmetry, and the third and fourth diagrams state that $\ell$ is a symmetric cosemigroup.

* Universality of the vertical lift:Define the map $\mu := T(+) \circ \langle \ell \circ \pi_0, 0 \circ \pi_1 \langle$, we require the following diagram be a pullback

\begin{center}
    \begin{tikzcd}
      T_2(M) \ar[r, "\mu"] & T^2(M) \ar[d, "T(p)"] \\
      M \ar[r, "0"] & T(M)
    \end{tikzcd}
 \end{center} 

### Tangent Structure as abstract Weil Prolongation

### Tangent Structure as a Weighted Limit

## References

The definition is due to

* [[Jiri Rosicky]], _Abstract tangent functors_, Diagrammes 12 (1984)

For developments of his ideas, see

* [[Robin Cockett]] and [[Geoff Cruttwell]], _Differential structure, tangent structure, and SDG_, ([pdf](https://www.mta.ca/uploadedFiles/Community/Bios/Geoff_Cruttwell/sman3.pdf))

* [[Robin Cockett]] and [[Geoff Cruttwell]], _Differential bundles and fibrations for tangent categories_, ([arXiv:1606.08379](https://arxiv.org/abs/1606.08379))

* [[Robin Cockett]] and [[Geoff Cruttwell]], _Connections in tangent categories_, ([arXiv:1610.08774](https://arxiv.org/abs/1610.08774))

* [[Geoff Cruttwell]], [[Rory Lucyshyn-Wright]], _A simplicial foundation for differential and sector forms in tangent categories_, ([arXiv:1606.09080](https://arxiv.org/abs/1606.09080))

* Poon Leung, _Classifying tangent structures using Weil algebras_, Theory and Applications of Categories, 32(9):286–337, 2017, ([tac](http://www.tac.mta.ca/tac/volumes/32/9/32-09abs.html))

Representation of this tangent structure as exponentiation by a tangent vector is given in

* [[Richard Garner]], _An embedding theorem for tangent categories_, ([arXiv:1704.08386](https://arxiv.org/abs/1704.08386))

The enriching category from the above paper was discussed earlier in

* [[Eduardo Dubuc]]. _Sur les modeles de la géométrie différentielle synthétique._ Cahiers de topologie et géométrie différentielle catégoriques 20, no. 3 (1979): 231-279. ([pdf](http://www.numdam.org/article/CTGDC_1979__20_3_231_0.pdf))

* Wolfgang Bertram _Weil spaces and Weil-Lie groups._ arXiv preprint arXiv:1402.2619 (2014),([arXiv:1402.2619](https://arxiv.org/abs/1402.2619))

Weil Prolongation is discussed in the following papers:

* [[Anders Kock]] (1986). _Convenient vector spaces embed into the Cahiers topos._ Cahiers de topologie et géométrie différentielle catégoriques, 27(1), 3-17 ([pdf](http://www.numdam.org/article/CTGDC_1986__27_1_3_0.pdf))

* Wolfgang Bertram, and Arnaud Souvay. "A general construction of Weil functors." arXiv preprint arXiv:1111.2463 (2011).

[[!redirects tangent bundle categories]]