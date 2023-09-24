## Idea

Proto-exact category is a nonadditive generalization of a [[Quillen exact category]]. The definition is self-dual as the notion of Quillen exact category is.

## Definition 

A proto-exact category is a pointed category $A$, with zero object $0$, together with two
classes of morphisms, $I$ and $D$, called inflations and deflations such that

(i) each morphism $0\to U$ is an inflation and each morphism $U\to 0$ is a deflation

(ii) classes $I$ and $D$ are closed under composition and contain all isomorphisms

(iii) each square of the form

 $$\array{
U &\rightarrow &V\\
\downarrow && \downarrow\\
W &\rightarrow & Z
}$$
where the horizontal arrows are inflations and the vertical arrows are deflations is a pushout iff it is a pullback

(iv) Every diagram of the form $W\rightarrow Z\leftarrow V$ where $W\rightarrow Z$ is a deflation and $Z\leftarrow V$ a inflation may be completed to a biCartesian square of the form in (iii)

(v) Every diagram of the form $W\leftarrow U\rightarrow V$ where $W\leftarrow U$ is an inflation and $U\rightarrow V$ a deflation may be completed to a biCartesian square of the form in (iii)


## Literature

The concept originates in 

* Tobias Dyckerhoff, [[Mikhail Kapranov]], _Higher Segal spaces I_, [arxiv:1212.3563](https://arxiv.org/abs/1212.3563); now part of the book T. Dyckerhoff, M. Kapranov, _Higher Segal spaces_, Springer LNM 2244 (2019) [doi](https://doi.org/10.1007/978-3-030-27124-4)
 {#DyckerhoffKapranov12}

* Jaiung Jun, [[Matt Szczesny]], Jeffrey Tolliver, _Proto-exact categories of matroids, Hall algebras, and K-theory_ Math. Z. __296__ (2020) 147--167 [doi](https://doi.org/10.1007/s00209-019-02429-z)
* Jaiung Jun, [[Matt Szczesny]], Jeffrey Tolliver, _Proto-exact categories of modules over semirings and hyperrings_, [arXiv:2202.01573](https://arxiv.org/abs/2202.01573)

> _Proto-exact categories_, introduced by Dyckerhoff and Kapranov, are a generalization of Quillen exact categories which provide a framework for defining algebraic K-theory and Hall algebras in a \emph{non-additive} setting. This formalism is well-suited to the study of categories whose objects have strong combinatorial flavor.
In this paper, we show that the categories of modules over semirings and hyperrings - algebraic structures which have gained prominence in tropical geometry - carry proto-exact structures.
In the first part, we prove that the category of modules over a semiring is equipped with a proto-exact structure; modules over an idempotent semiring have a strong connection to matroids. We also prove that the category of algebraic lattices $\mathcal{L}$ has a proto-exact structure, and furthermore that the subcategory of $\mathcal{L}$ consisting of finite lattices is equivalent to the category of finite $\mathcal{B}$-modules as proto-exact categories, where $\mathcal{B}$ is the _Boolean semifield_. We also discuss some relations between $\mathcal{L}$ and geometric lattices (simple matroids) from this perspective.
In the second part, we prove that the category of modules over a hyperring has a proto-exact structure. In the case of finite modules over the _Krasner hyperfield_ $\mathbf{K}$, a well-known relation between finite $\mathbf{K}$-modules and finite incidence geometries yields a combinatorial interpretation of exact sequences. 

* Matthew B Young, _Degenerate versions of Green’s theorem for Hall modules_, J. Pure & Applied Algebra __225__ (2021) 106557 [doi](https://doi.org/10.1016/j.jpaa.2020.106557)

* J. Hekking, _Segal objects in homotopical categories &
K-theory of proto-exact categories_, master thesis 2017 [pdf](https://www.universiteitleiden.nl/binaries/content/assets/science/mi/scripties/master/hekking_master.pdf)

[[!redirects proto-exact categories]]