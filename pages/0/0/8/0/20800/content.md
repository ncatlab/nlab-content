
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A Turing category is a certain [[categorification]] of [[partial combinatory algebras]] (PCAs) based on [[restriction categories]].

+-- {: .num_defn #TuringCategory}
###### Definition
**(Turing category)**

A _Turing category_ is a cartesian restriction category $(\mathcal{C}, \bar{} )$ with a fixed object A and morphism $\bullet : A \times A \rightarrow A$ having the following universal property: for each $\mathcal{C}$-morphism $f : X \rightarrow Y$ there is a section $s: Y \rightarrow A$ and retract $r : A \rightarrow X$, along with a total map $h : \mathbf{1} \rightarrow A$ satisfying the diagram:

\begin{centre} 
    \begin{tikzcd}
    \arrow[r, "\bullet"] A \times A & A \arrow[r, "r"] & X \arrow[ddll, "f"] \\
    \arrow[u, "\mathsf{id_A} \times h"] A \times 1 \simeq A \arrow[ur, swap,  "sfr"] & & \\
    Y \arrow[u, "s"] & &
    \end{tikzcd}
\end{centre}

=--

While restriction structure captures the function partiality one finds in [[computability theory]], the universal property stated above captures the universal coding of $\mathcal{C}$-morphisms into operations on the _Turing object_ $A$, via the application $\bullet$. Indeed one recovers, as an example, the category $\mathbf{Rec}$, of natural numbers $n, m \in \mathbf{N}$ and partial recursive functions $ \mathbf{N}^n \rightarrow \mathbf{N}^m$. This has universal applicative structure:
    
\begin{centre}
     \begin{tikzcd}
    \arrow[d, swap, dashed, "\exists \hspace{0.1cm} \text{total} \hspace{0.1cm} h \hspace{0.1cm} : \hspace{0.1cm} 1 \times h"] \mathbf{N} \times 1 \simeq \mathbf{N} \arrow[rd, "f_i"] \\ \mathbf{N} \times \mathbf{N} \arrow[r, swap, "\langle -- \rangle"] & \mathbf{N}
    \end{tikzcd}
\end{centre}

and universal representation $\langle i, n \rangle = f_i(n)$ of the $i$th computable function. In this case the PCA is [[Kleene's first algebra]]. More generally, the computable map category of any PCA forms a Turing category, with Turing object the PCA and its Turing morphism being the applicative structure.

And conversely, a Turing object $A$ of $\mathcal{C}$ and its Turing morphism $\bullet : A \times A \rightarrow A$ form a (relative) PCA. This is effectively a PCA-object internal to an appropriate category:

+-- {: .num_defn #RelativePCA}
###### Definition
**(Relative PCA)**

A (relative) PCA $A$ is a combinatory complete partial applicative system in a cartesian [[restriction category]] $\mathcal{D}$, i.e. a morphism $\bullet : A \times A \rightarrow A$ in $\mathcal{D}$ such that finite powers $A^n$ and $A$-computable morphisms form a well-defined cartesian restriction subcategory of $\mathcal{D}$.

=--

Note, however, that not every relative PCA in a Turing category $\mathcal{C}$ is a Turing object for $\mathcal{C}$. 

### Basic properties

The arithmetical representation of a (partial) function $f : \mathbf{N} \rightarrow \mathbf{N}$ as a member of the recursive enumeration of relations $\varphi_i \subset \mathbf{N} \times \mathbf{N}$ is universal, and this representation satisfies the Kleene [[recursion theorems]]:

$\bullet$ (smn) Let $f: \mathbf{N} \rightarrow \mathbf{N}$ be a partial computable function. Then there is a partial computable function $s : \mathbf{N} \rightarrow \mathbf{N}$ such that $f(\langle i, n \rangle) = f_{s(i)} (n)$.

$\bullet$ (utm) There is a partial computable function $U : \mathbf{N} \rightarrow \mathbf{N}$ such that $U(\langle i, n \rangle ) = f_i (n)$.

As can be nearly read off the definition above, these properties hold with respect to any Turing object. This is part of the overall motivation for Turing categories, since they provide a more model-independent setting both for stating the main theorems of recursion theory, while also allowing the "intrinsic meaning" of different constructions in computability theory to stand out. For example, in [[Type II computability]] (or [[function realizability]]) it turns out that _function computability_ with respect to the PCA $\mathbf{N}^\mathbf{N}$ (either as [[Kleene's second algebra]] or the [[Baire space of sequences]]) has the topological meaning of _continuity_. Hence, despite the universal availability of Gödel-encodings of all "$A$-computations" for an appropriate data type $A$ into $\mathbf{N}$-computations (a form of the [[Church-Turing thesis]]), the theory of Turing categories and their applications to categorical realizability models, for example, are intended to give the intrinsic meaning of computational mathematics without resorting to such a universal representation, much like the success story of Type II computability.

## More Examples 

(...)


## Weak Limits and Exact Completions 

(...)


## Related concepts

* [[timed set]]


## References

Turing categories were isolated categorically and named in:

* [[Robin Cockett]], [[Pieter Hofstra]], _Introduction to Turing categories_, Annals of Pure and Applied Logic, 156, 2008 ([pdf](https://www.di.ens.fr/users/longo/files/Cockett-TuringCateg.pdf))


[[!redirects turing category]]
[[!redirects turing-categories]]
[[!redirects Turing category]]
[[!redirects turing categories]]
