## Idea

Cotorsion pairs in [[abelian categories]] are a notion generalizing both [[projective object|projective]] and [[injective objects]].

## Definition

Let $\mathcal{A}$ be an [[abelian category]].

+-- {: .num_defn}
###### Definition
A **cotorsion pair** in $\mathcal{A}$ is a pair $(\mathcal{D},\mathcal{E})$ of classes
of objects of $\mathcal{A}$ such that

* $D \in \mathcal{D}$ if and only if $Ext^1(D, E) = 0$ for all $E \in \mathcal{E}$
* $E \in \mathcal{E}$ if and only if $Ext^1(D, E) = 0$ for all $D \in \mathcal{D}$.
=--

+-- {: .num_example}
###### Example
Let $\mathcal{I}$ denote the class of [[injective objects]] of $\mathcal{A}$.  Then $(\mathcal{A}, \mathcal{I})$ is a cotorsion pair, where we write $\mathcal{A}$ for the class of all objects of $\mathcal{A}$.

Dually, there is a cotorsion pair $(\mathcal{P}, \mathcal{A})$ where $\mathcal{P}$ is the class of [[projective objects]] of $\mathcal{A}$.
=--

+-- {: .num_example #FlatCotorsionPair}
###### Example
The **flat cotorsion pair** on the category of $R$-[[modules]] (for some [[ring]] $R$) is defined by letting $\mathcal{D}$ be the class of [[flat module|flat]] $R$-modules and $\mathcal{E}$ the class of [[cotorsion modules]], i.e. $R$-modules $E$ such that $Ext^1_R(D,E)=0$ for all flat $D$.
=--

+-- {: .num_defn}
###### Definition
We say that a cotorsion pair $(\mathcal{D},\mathcal{E})$ **has enough injectives** if for every [[object]] $X$ of $\mathcal{A}$, there exist objects $D \in \mathcal{D}$ and $E \in \mathcal{E}$ such that there is an exact sequence
\[ 0 \to X \to E \to D \to 0. \]
We say that it **has enough projectives** if for every [[object]] $X$ of $\mathcal{A}$, there exist objects $D \in \mathcal{D}$ and $E \in \mathcal{E}$ such that there is an exact sequence
\[ 0 \to E \to D \to X \to 0. \]
=--

Note that the category $\mathcal{A}$ has enough injectives if and only if the cotorsion pair $(\mathcal{A}, \mathcal{I})$ has enough injectives, and $\mathcal{A}$ has enough projectives if and only if $(\mathcal{P}, \mathcal{A})$ has enough projectives.

+-- {: .num_defn}
###### Definition
A cotorsion pair $(\mathcal{D},\mathcal{E})$ is called **complete** if it has enough injectives and enough projectives.
=--

## References

* [[Mark Hovey]], _Cotorsion pairs and model categories_, Contemp. Math. __436__ (2007) 277-296 [pdf](http://homepages.math.uic.edu/~bshipley/hovey.pdf) [gBooks](https://books.google.hr/books?id=UZ8bCAAAQBAJ) [doi](https://doi.org/10.1090/conm/436/08413)

On the generalization of $n$-cotorsion pairs:

* Huimin Chang, Panyue Zhou. *Mutation of n-cotorsion pairs in triangulated categories* (2024). ([arXiv:2404.18336](https://arxiv.org/abs/2404.18336)).

[[!redirects cotorsion pairs]]