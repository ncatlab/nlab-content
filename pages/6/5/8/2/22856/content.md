
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A *divided power algebra* is a [[commutative ring]] $A$ together with an [[ideal]] $I$ and a collection of operations $\{\gamma_{n}\colon I\to A\}_{n\in\mathbb{N}}$ which behave like operations of taking divided powers $x\mapsto x^{n}/n!$ in [[power series]].


## Definition

A __divided power algebra__ is a triple $(A,I,\gamma)$ with

- $A$ a [[commutative ring]] (with identity);

- $I$ an [[ideal]] of $A$;

- $\gamma=\{\gamma_{n}\colon I\to I\}_{n\geq 1}$ an [[indexed set]] of [[functions]] (of [[underlying]] [[sets]]);

where we additionally adopt the convention $\gamma_0(x) = 1$ (which is usually not in $I$), and this data is required to satisfy the following conditions:

1. For each $x\in I$, we have $\gamma_{1}(x)=x$.

1. For each $x,y\in I$ and $n\geq 0$, we have
$$
\gamma_{n}(x+y)=\sum_{k=0}^{n}\gamma_{n-k}(x)\gamma_{k}(y),
$$

1. For each $\lambda\in A$, each $x\in I$ and $n\geq 0$, we have
$$
\gamma_{n}(\lambda x)=\lambda^{n}\gamma_{n}(x).
$$

1. For each $x\in I$ and each $m,n\geq 0$, we have
$$
\gamma_{n}(x)\gamma_{m}(x)=\frac{(n+m)!}{n!m!}\gamma_{n+m}(x).
$$

1. For each $x\in I$ and each $m\geq 0$, $n\geq 1$, we have
$$
\gamma_{m}(\gamma_{n}(x))=\frac{(n m)!}{(n!)^{m}m!}\gamma_{n m}(x).
$$

For a given $(A,I)$, a __divided power structure__ on $(A,I)$ is a $\gamma$ making $(A, I, \gamma)$ a divided power algebra.

If $A$ is an $R$-algebra for a ring $R$, we call it a __divided power $R$-algebra__ or __PD-$R$-algebra__.


+-- {: .un_remark}
###### Remark

Some sources include $\gamma_0$ in the data rather than as convention. Some sources give the data as $\gamma_n : I \to A$ typing while including $\gamma_n(x) \in I$ for $n \geq 1$ as an axiom.

=--

## Properties

Genuine powers can be constructed in the expected way from the divided powers, and when $A$ is torsion free, the reverse is true:

+-- {: .num_prop} 
###### Proposition

If $(A,I,\gamma)$ is a divided power algebra, then $n! \gamma_n(x) = x^n$ for every $x \in I$ and $n \geq 0$ (taking $x^0:=1$).
=--

+-- {: .proof} 
###### Proof 

It is true for $n=0$ and $n=1$ by definition. 
For $n \geq 2$, this follows by [[induction]], since $n! \gamma_n(x) = (n-1)! \gamma_{n-1}(x) \cdot 1! \gamma_1(x) = x^{n-1} \cdot x$.

=--
+-- {: .num_prop} 
###### Proposition

If $A$ is a commutative, torsion free ring with an ideal $I$ such that $x^n$ is an $(n!)$-th multiple for every $x \in I$ and $n \geq 0$, then $(A,I)$ has a unique divided power structure, and it is given by $\gamma_n(x) = x^n / n!$.
=--

+-- {: .proof} 
###### Proof 

The hypotheses imply the quotients $x^n / n!$ are unique and well-defined, and any divided power structure on $(A,I)$ must be given by that formula. It's straightforward to check the definition does give a divided power algebra.

=--

So in the torsion free case, the divided power algebras are precisely of the motivating form. In positive characteristic, though, examples can be somewhat more exotic.

## Categorically

We can define the concept of divided power in any symmetric monoidal category.

Let $\mathcal{C}$ be a symmetric monoidal category.

The $n^{th}$ divided power of an object $A$ is then defined as the equalizer of the following diagram:

\begin{tikzcd}
A^{\otimes n} \arrow[rr, "\sigma", shift left=2] \arrow[rr, "...", shift right=2] &  & A^{\otimes n}
\end{tikzcd}

where there is one arrow for every $\sigma \in \mathfrak{S}_{n}$. We write $\sigma$ for the natural transformation associated to $\sigma$, which is defined in the entry [[symmetric monoidal category]].

The $n-th$ divided power $\Gamma_{n}(A)$ is thus described by the following equalizer diagram:

\begin{tikzcd}
\Gamma_{n}A \arrow[rr, "s_{n}"] &  & A^{\otimes n} \arrow[rr, "\sigma", shift left=2] \arrow[rr, "...", shift right=2] &  & A^{\otimes n}
\end{tikzcd}

In the category of modules over some commutative ring, the $n-th$ divided power of a module $A$ is equivalently descibed as the space $(A^{\otimes n})^{\mathfrak{S}_{n}}$ of [[invariants]] under the action of $\mathfrak{S}_{n}$ on $A^{\otimes n}$ by permutation of the factors. Note that the $n-th$ symmetric power $S_{n}(A)$ of an object $A$ in a symmetric monoidal category is described as the coequalizer of the $n!$ permutations $A^{\otimes n} \rightarrow A^{\otimes n}$. In a category of modules, it is equivalently described as the space $(A^{\otimes n})_{\mathfrak{S}_{n}}$ of [[coinvariants]] by the action of $\mathfrak{S}_{n}$. We then have the relation $(S_{n}(A^{*}))^{*} = \Gamma_{n}(A)$ which probably means that these powers can be interpreted as [[graded modalities|graded exponential modalities]] in a kind of graded [[differential linear logic]]. In [[characteristic 0]], we have $\Gamma_{n}(A) \cong S_{n}(A)$. Nondegenerated models of such a logic in a category of vector spaces would thus be only in the case where the field is of [[positive characteristic]].

## Related concepts

* [[crystalline cohomology]]

## References

Divided power algebras were originally introduced in 

* [[Henri Cartan]], _Puissances divisées_, Séminaire Henri Cartan, Tome 7 (1954–1955) no. 1, Exposé no. 7, 11 p. [Numdam:SHC_1954–1955__7_1_A7_0](http://www.numdam.org/item/SHC_1954-1955__7_1_A7_0/).

Their theory was further developed in [[Pierre Berthelot]]'s PhD thesis (in the context of [[crystalline cohomology]]), which was later published as:

* [[Pierre Berthelot]], _Cohomologie cristalline des sch&#233;mas de caract&#233;ristique $p \gt 0$_, Lecture Notes in Mathematics, Vol. 407, Springer-Verlag, Berlin, 1974. ([doi:10.1007/BFb0068636](https://doi.org/10.1007/BFb0068636),  MR 0384804)

Review:

* [[Pierre Berthelot]], [[Arthur Ogus]], _Notes on crystalline cohomology_, Princeton Univ. Press 1978. vi+243, ([ISBN:0-691-08218-9](https://press.princeton.edu/books/hardcover/9780691648323/notes-on-crystalline-cohomology-mn-21))

* [[Aise Johan de Jong]] et al., [[The Stacks Project]], [Chapter 09PD](https://stacks.math.columbia.edu/tag/09PD).

Recent works on divided power algebras include:

* [[Sacha Ikonicoff]], _Divided power algebras over an operad_, Glasgow Math. J. **62** (2020) 477-517, [doi:10.1017/S0017089519000223](https://doi.org/10.1017/S0017089519000223), [pdf](https://arxiv.org/pdf/1712.03694.pdf)

* [[Sacha Ikonicoff]], _Divided power algebras and distributive laws_, 2021, [doi:10.48550/arXiv.2104.11736]( https://doi.org/10.48550/arXiv.2104.11736), [pdf](https://arxiv.org/pdf/2104.11736.pdf)

It is related to [[differential categories]] in:

* [[Sacha Ikonicoff]], [[Jean-Simon Pacaud Lemay]], _Cartesian Differential Comonads and New Models of Cartesian Differential Categories_, 2021, [doi:10.48550/arXiv.2108.04304](https://doi.org/10.48550/arXiv.2108.04304), [pdf](https://arxiv.org/pdf/2108.04304.pdf)

On divided powers:

* Luis Narváez Macarro: _Hasse-Schmidt derivations, divided powers and differential smoothness_, 2009, [doi:10.5802/aif.2513](https://doi.org/10.5802/aif.2513), [pdf](https://aif.centre-mersenne.org/item/10.5802/aif.2513.pdf)

See also:

* Wikipedia, *[Divided power structure](https://en.wikipedia.org/wiki/Divided_power_structure)*

In relation to the [[sphere spectrum]]

* [[Sanath Devalapurkar]], _Divided powers and the sphere spectrum_, [blog post](https://sanathdevalapurkar.github.io/blog/algebraic-topology/2019/02/20/divided-powers.html)

[[!redirects PD-algebra]]
[[!redirects PD-algebras]]

[[!redirects divided power structure]]
[[!redirects divided power structures]]
[[!redirects divided power algebras]]

[[!redirects divided power]]
[[!redirects divided powers]]
