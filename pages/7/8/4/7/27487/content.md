
> see also *[[Bousfield-Kan map]]*

# Bousfield–Kan formula

\tableofcontents

## Idea

Bousfield--Kan formula ([BK72](#BousfieldKan)) is a presentation
of [[colimits]] (or dually, limits) in [[(infinity,1)-categories]]
(i.e., [[homotopy colimits]]) in terms of coproducts and colimits
of simplicial objects.

In ordinary category theory, the colimit of a diagram $F:I\to C$
is computed as a coequalizer of the parallel pair
$$
\coprod_{c_{0}\to c_{1}}Fc_{0}\rightrightarrows\coprod_{c}Fc.
$$
When $C$ is an $(\infty,1)$-category, we need to take ``higher
data'' into account. So we take the geometric realization (i.e.,
$\Delta^{op}$-indexed colimit) of the simplicial object
$$
B_{\bullet}(\ast,I,F)=\left(\cdots\coprod_{c_{0}\to c_{1}\to c_{2}}Fc_{0}\Rrightarrow\coprod_{c_{0}\to c_{1}}Fc_{0}\rightrightarrows\coprod_{c\in C}Fc\right).
$$
This can be formalized as follows: There is an ``initial vertex''
functor $\mathrm{init}:(\Delta_{/I})^{op}\to I$ from the opposite
of the category of simplices of $I$, which is homotopy final. Thus,
$$
\mathrm{colim}_{I}F\simeq\mathrm{colim}_{(\Delta_{/I})^{op}}(F\circ\mathrm{init}).
$$
The simplicial object $B_{\bullet}(\ast,I,F)$ is just the left Kan
extension of $F\circ\mathrm{init}$ along the projection $(\Delta_{/I})^{op}\to\Delta^{op}$,
so we have
$$
\mathrm{colim}_{(\Delta_{/I})^{op}}(F\circ\mathrm{init})\simeq\mathrm{colim}_{\Delta^{op}}B_{\bullet}(\ast,I,F).
$$


## Particular Implementations in Model Categories

### Via Geometric Realizations

In a simplicial model category $C$, homotopy colimits indexed by
$\Delta^{op}$ is modeled by geometric realization. Therefore, the
Bousfield--Kan formula for homotopy colimit of a (pointwise cofibrant)
diagram $F:I\to C$ is computed by
$$
{\rm hocolim}_{I}F\simeq|B_{\bullet}(\ast,I,F)|.
$$
Textbook account includes [Rie14, Chapter 5](#Riehl14).

### Via Functor Tensor Product

Let $F:I\to C$ be a (pointwise cofibrant) diagram in a simplicial
model category. Some coend calculus shows [Rie14, 6.6.1](#Riehl14)
that 
$$
|B_{\bullet}(\ast,I,F)|\cong\int^{i\in I}N(I_{/i})\otimes F(i)=:N(I_{/-})\otimes_{I}F.
$$
The right hand side is also called the Bousfield--Kan formula. 

### In Model Categories with Framings

A cosimplicial framing on a model category is roughly a functorial
choice of cosimplicial resolutions [Chapter 16]({#Hir03}). With this
data, we can formally mimic the Bousfield--Kan formula, and this
is adopted as the definition of homotopy colimits in [Hir03, Chapter19]({#Hir03});
that this approach is equivalent to the ordinary notion of homotopy
colimits is established in [AO23]({#AO23}) (for combinatorial model
categories) and [Ara23, Section 1]({#Ara23}) (for general model categories).

## References

The Bousfield--Kan formula was introduced in:


* {#BK72} [[Aldridge K. Bousfield]] and [[Daniel M. Kan]], Chapter IX in: *[[Homotopy Limits, Completions and Localizations]]*, Lecture Notes in Mathematics 304 (1972; 1987), Springer ([doi:10.1007/978-3-540-38117-4](https://link.springer.com/book/10.1007/978-3-540-38117-4))

Discussions in simplicial model categories can be found in:


* {#Rie16} [[Emily Riehl]], Chapter 5 in: *[[Categorical Homotopy Theory]]*, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457), [pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf)&rbrack;

Further references:


* {#Hir03} [[Philip Hirschhorn]], _Model categories and their localizations_, (2003) &lbrack;[doi:10.1090/surv/099](https://doi.org/10.1090/surv/099)&rbrack;

* {#AO23} [[Sergey Arkhipov]], [[Sebastian Ørsted]]: _Homotopy (co)limits via homotopy (co)ends in general combinatorial model categories_, Appl. Categ. Structures **31** 6 (2023) &lbrack;[doi:10.1007/s10485-023-09747-8](https://doi.org/10.1007/s10485-023-09747-8)&rbrack;

* {#Ara23} [[Kensuke Arakawa]], Section 1 of _Homotopy Limits and Homotopy Colimits of Chain Complexes_, (2023) firstpage-lastpage &lbrack;[arXiv:2310.00201](https://arxiv.org/abs/2310.00201)&rbrack;

[[!redirects Bousfield--Kan formula]]