
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A **tangent bundle category** is a [[category]] equipped with a "[[tangent bundle]]" [[endofunctor]] satisfying some natural axioms.

Usually these are called simply **tangent categories**, but on the nLab the page [[tangent category]] is about "the tangent category of a given category" constructed by abelianization.  In other words, tangent bundle categories are about *abstraction* of the tangent bundle construction, while tangent categories are a *categorification* thereof (in some vague sense).

## Definition

Tangent bundle categories have three equivalent definitions: the first is due to Rosicky and was rediscovered/refined by [[Robin Cockett|Cockett]] and [[Geoff Cruttwell|Cruttwell]]. In his thesis, Poon Leung found an equivalent definition of tangent categories using a category structure that acts as an abstract Weil prolongation, and later [[Richard Garner]] gave a definition of a tangent category as a sort of enriched category.

### Classical Definition

Tangent bundle categories were originally introduced by Rosicky to model the behaviour of the tangent bundle on the category of smooth manifolds, and of [[microlinear spaces]] in a [[smooth topos]]. For smooth manifold $M$ and a point $m \in M$, on may consider a coordinate patch $U \subset \mathbb{R}^n$ around $m$. Looking at the tangent space of $U$, we see $T(U) \cong U \times \mathbb{R}^n$, and similarly
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
    0: \mathsf{id} \Rightarrow T, +: T \times_p T \Rightarrow T,
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
   T^2(M) \ar[r, "c"] \ar[d, "p_T"] & T^2(M) \ar[d, "{T(p)}"] 
   \\
   T(M) \ar[r, equals] & T(M)
 \end{tikzcd}

\end{center}

* The vertical lift $\ell$ gives an additive bundle morphism $(\ell, 0): p \Rightarrow T(p)$.
  


* We also require the following coherences between the vertical lift and the canonical flip: 

\begin{center}

\begin{tikzcd}
      T \ar[r, "\ell"] \ar[d, "\ell"'] & T^2 \ar[d, "{T(\ell)}"] 
      \\
      T^2 \ar[r, "\ell_T"] & T^3
\end{tikzcd}

\end{center}

\begin{center}

\begin{tikzcd}
      T^3 \ar[d, "c_T"] \ar[r, "{T(c)}"] & T^3 \ar[r, "c_T"] & T^3 
      \ar[d, "T(c)"] \\
      T^3 \ar[r, "{T(c)}"] & T^3 \ar[r, "c_T"] & T^3
\end{tikzcd}

\end{center}

\begin{center}

\begin{tikzcd}
      T^2 \ar[r, "\ell_T"] \ar[d, "c"'] 
      & T^3 \ar[r, "{T(c)}"] 
      & T^3 \ar[d, "c_T"]
     \\
      T^2 \ar[rr, "{T(\ell)}"] && T^3
\end{tikzcd}

\end{center}

\begin{center}

\begin{tikzcd} 
       T \ar[r, "\ell"] \ar[rd, "\ell"] 
       & T^2 \ar[d, "c"] 
       \\ & T^2   
\end{tikzcd}

\end{center}

In the monoidal category $[\mathbb{X}, \mathbb{X}]$, the first diagram corresponds to $\ell: T \Rightarrow T^2$ being a cosemigroup. The second diagram corresponds to $c: T^2 \Rightarrow T^2$ acting as a symmetry, and the third and fourth diagrams state that $\ell$ is a symmetric cosemigroup.

* Universality of the vertical lift: Define the map $\mu := T(+) \circ \langle \ell \circ \pi_0, 0_T \circ \pi_1 \rangle$, we require the following diagram be a pullback:

\begin{center}

\begin{tikzcd}
      T_2(M) \ar[r, "\mu"] \ar[d, "p \circ \pi_0 = p \circ \pi_1"] 
      & T^2(M) \ar[d, "{T(p)}"] \\
      M \ar[r, "0"] & T(M)
\end{tikzcd}

\end{center} 



### Tangent Structure as abstract Weil Prolongation


There is a vast literature on the notion of a "Weil functor". A particularly important theorem is that every product preserving endofunctor on the category of smooth manifolds is given by a prolongation operation with a Weil algebra. To simplify this section, we will only consider the case of tangent categories with negatives - see Leung's thesis to see the generalization to commutative rigs.

#### Weil Algebras

Consider a commutative ring $R$. For this section an $R$-algebra is a commutative, unital, associative $R$-algebra. A _Weil Algebra_ over $R$ is an augmented $R$-algebra $V$ so that:

1. The underlying $R$-module of $V$ is $R^n$.
1. The _kernel of augmentation_ of $\pi: V \to R$ is nilpotent: there exists
  a natural number $k$ so that for every $x \in \mathsf{ker}(\pi)$, $x^k = 0$. 

The category of Weil algebras is the full subcategory of $R-\mathsf{alg}/R$ whose objects are Weil algebras.

+-- {: .num_prop #cat_of_R_weil }
###### Proposition 

1. $R$-Weil algebras have products.
1. $R$-Weil algebras have coproducts.
1. $R$ is a zero object in the category of $R$-Weil algebras.

=--

It is often useful to consider a presentation of $R$-Weil algebras.

+-- {: .num_prop #presentation_of_R_weil }
###### Proposition 

* (1) Weil algebras may be presented as $R[X_i]/I$, where $I$ is an ideal of $R[X_i]$.

* (2) The product of Weil algebras $R[X_i]/I, R[Y_j]/J$ may be presented as  $R[X_i,Y_j]/(I \cup J \cup XY)$, where $XY = \{ X_i Y_j \}$, the coproduct as $R[X_i,Y_j]/(I \cup J)$. 

* (3) The following diagram is a [[pullback]]:

\begin{center}

\begin{tikzcd}
        R[X,Y]/(X^2,Y^2, XY) 
        \ar[r, "X \mapsto X Y", "Y \mapsto Y"'] 
        \ar[d, "X{,}Y \mapsto 0"]
        & R[X,Y]/(X^2,Y^2) \ar[d, "Y \mapsto 0{,} X \mapsto X"] \\
        R \ar[r, "0"] & R[X]/X^2
      \end{tikzcd}

\end{center}

* (4) For any Weil algebra $U$, the endofunctor $U \oplus (-)$ preserves products and the above pullback.

=--

We finally restrict our attention to the category $\mathsf{Weil}_1$. Let $W$ denote the $R$-Weil algebra $R[X]/X^2$, then we may consider the full subcategory whose objects are the closure of $\{ W^n | n \in \mathbb{N}\}$ under coproduct.


#### Abstract Weil Prolongation

Consider the category $\mathsf{Weil}_1$ over the the integers as a symmetric monoidal category with $(\mathsf{Weil}_1,\oplus, R)$. If a category $\mathbb{X}$ has a tangent structure, then it has an [[actegory]] structure

$$
  \propto: \mathbb{X} \times \mathsf{Weil}_1 \to \mathbb{X}
$$

so that for any object $M$ in $\mathbb{X}$, $\propto(M,-)$ preserves connected limits
of $\mathsf{Weil}_1$.

1. The tangent bundle functor is the action by $R[X]/X^2$.
  \[
   ( M \propto R[X]/X^2) \propto R[Y]/Y^2 = M \propto R[X,Y]/(X^2,Y^2)
  \]
1. The addition map is given by:
  \[
    M \propto (X,Y \mapsto X): M \propto R[X,Y]/X^2,Y^2,XY \to M \propto R[X]/X^2
  \]
  similarly $0$ is given by:
  \[
    M \propto 0: M \propto R \to M \propto R[X]/X^2
  \]
1. The canonical flip is given by:
  \[
    M \propto (X,Y \mapsto Y,X): M\propto R[X,Y](X^2,Y^2) \to M\propto R[X,Y](X^2,Y^2)
  \]
1. The vertical lift is given by:
  \[
    M \propto (X \mapsto XY): M \propto R[X]/X^2 \to M\propto R[X,Y](X^2,Y^2)
  \]


### Tangent Structure as a Weighted Limit


Using a theorem due to [[Richard Wood]], a
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

* Wolfgang Bertram and Arnaud Souvay. _A general construction of Weil functors._ arXiv preprint arXiv:1111.2463 (2011).([arXiv:1111.2463](https://arxiv.org/pdf/1111.2463.pdf))

[[!redirects tangent bundle categories]]
