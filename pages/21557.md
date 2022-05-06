[[!redirects Geometric nerve of a tricategory]]
[[!redirects Street nerve]]
[[!redirects Street nerves]]
[[!redirects tricategory nerve]]
[[!redirects nerve of tricategories]]
[[!redirects nerve of a tricategory]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _geometric nerve_ is a natural  [[nerve]] operation on [[tricategories]], associating to every [[tricategory]] $\mathcal{C}$ a [[simplicial set]] $\mathrm{N}^{\mathsf{S}}_{\bullet}(\mathcal{C})$.

Also called the _Street nerve_ of $\mathcal{C}$, this notion, like the [[Duskin nerve]] of a [[bicategory]], is implicit in  ([ [[Ross Street]]'s work on [[oriental]]s](#Street1987)). While this construction was announced in ([Duskin, 2002](#Duskin2002)) as to appear in a (then) forthcoming paper, the latter never appeared. Instead, the notion was developed by Cegarra–Heredia in ([Cegarra–Heredia, 2012](#CegarraHeredia2012)).

Roughly, the [[Street]] nerve of $\mathcal{C}$ may be thought of as the [[simplicial set]] $\mathrm{N}^{\mathsf{S}}_{\bullet}(\mathcal{C})$ whose $n$-simplices are [[lax functors]] from the locally discrete [[tricategory]] associated to $[n]$ to $\mathcal{C}$ satisfying a variety of unitality conditions. In detail, however, the definition is more involved, as one faces problems with the definition of [[lax functor]]s between [[tricategories]] found in ([Gordon–Powers–Street](#GPS1995)); see ([Definition 5.1.1 of Cegarra–Heredia](#CegarraHeredia2012)).

There are other nerve constructions for tricategories besides the Street nerve. One of them is the **Grothendieck nerve**, which to every [[tricategory]] $\mathcal{C}$ associates a "[[pseudosimplicial bicategory]]" $\mathrm{N}^\mathsf{G}_\bullet(\mathcal{C})\colon\Delta^\op\longrightarrow\mathsf{Bicats}$; meaning a pseudofunctor from the locally discrete tricategory associated to $\Delta^\op$ to the tricategory $\mathsf{Bicats}$. Its bicategory of $n$-simplices has as objects $n$-tuples of composable morphisms of $\mathcal{C}$.

One also has the **Segal nerve** $\mathrm{N}^\mathsf{Segal}_\bullet(\mathcal{C})\colon\Delta^\op\longrightarrow\mathsf{Bicats}$ of $\mathcal{C}$, which is a simplicial bicategory, and a kind of "rectification" of $\mathrm{N}^\mathsf{G}_\bullet(\mathcal{C})$. When $\mathcal{C}$ is the locally discrete tricategory associated to a bicategory $\mathcal{B}$, the Segal nerve of $\mathcal{C}$ agrees with the $2$-nerve of $\mathcal{B}$ introduced in ([Lack–Paoli, 2006](#LackPaoli2006)).

All of these nerve constructions are equivalent in the sense that their classifying spaces are homotopy equivalent to each other. For more details, see ([Cegarra–Heredia, 2012](#CegarraHeredia2012)).
 
## Properties

* The Street nerve identifies precisely nerves of [[trigroupoid]]s with $3$-[[hypergroupoid]]s: those [[Kan complexes]] for which the horn fillers in dimension $\geq 4$ are _unique_; see ([Carrasco, 2014](#Carrasco2014)).

## Picturing the Street nerve

Let ($\mathcal{C}$,$\mathsf{Hom}_{\mathcal{C}}(-,-)$,$\otimes$,$1^\mathcal{C}$,$\alpha$,$\alpha^{\bullet}$,$\phi$,$\phi^{\bullet}$,$\lambda$,$\lambda^{\bullet}$,$\eta$,$\eta^{\bullet}$,$\rho$,$\rho^{\bullet}$,$\epsilon$,$\epsilon^{\bullet}$,$\mathbf{\pi}$,$\mathbf{\lambda}$,$\mathbf{\mu}$,$\mathbf{\rho}$) be a tricategory, where
   
* ($\alpha$,$\alpha^{\bullet}$,$\phi$,$\phi^{\bullet}$) is the associator adjoint equivalence of $\mathcal{C}$, 
* ($\lambda$,$\lambda^{\bullet}$,$\eta$,$\eta^{\bullet}$) is the left unitor adjoint equivalence of $\mathcal{C}$,
* ($\rho$,$\rho^{\bullet}$,$\epsilon$,$\epsilon^{\bullet}$) is the right unitor adjoint equivalence of $\mathcal{C}$, and
* $\mathbf{\pi}$,$\mathbf{\lambda}$,$\mathbf{\mu}$,$\mathbf{\rho}$ are the pentagonator, left, middle, and right $2$-unitors of $\mathcal{C}$.

(Below we also write these with "$^\mathcal{C}$" superscripts, and write $\mathbf{\pi}$,$\mathbf{\lambda}$,$\mathbf{\mu}$,$\mathbf{\rho}$ in blackboard bold font.)

The **Street nerve** of the tricategory $\mathcal{C}$ is then the simplicial set $\mathrm{N}^\mathsf{S}_{\bullet}(\mathcal{C})$ where

1. The $0$-simplices of $\mathrm{N}^\mathsf{S}_{\bullet}(\mathcal{C})$ are the objects of $\mathcal{C}$;

2. The $1$-simplices of $\mathrm{N}^\mathsf{S}_{\bullet}(\mathcal{C})$ are the $1$-morphisms of $\mathcal{C}$;

3. The $2$-simplices of $\mathrm{N}^\mathsf{S}_{\bullet}(\mathcal{C})$ are quadruples $(i,j,k,\theta)$ as in the diagram

   [[2-simplex-of-NC.svg:pic]]
   where $A,B,C\in\mathrm{Obj}(\mathcal{C})$, $i,j,k\in\mathrm{Mor}_1(\mathcal{C})$ and $\theta\colon j\circ i\Rightarrow k$ is a $2$-morphism of $\mathcal{C}$;

4. The $3$-simplices of $\mathrm{N}^\mathsf{S}_{\bullet}(\mathcal{C})$ are $15$-tuples
   $$(A_{0},A_{1},A_{2},A_{3},f_{01},f_{02},f_{03},f_{12},f_{13},f_{23},\theta_{012},\theta_{013},\theta_{023},\theta_{123},\Gamma_{0123})$$

   as in the diagram
   [[3-simplex-of-the-street-nerve.svg:pic]]

5. The $4$-simplices of $\mathrm{N}^\mathsf{S}_{\bullet}(\mathcal{C})$ are $28$-tuples

   * ($A_{0}$,$A_{1}$,$A_{2}$,$A_{3}$,$f_{01}$,$f_{02}$,$f_{03}$,$f_{04}$,$f_{12}$,$f_{13}$,$f_{14}$,$f_{23}$,$f_{24}$,$f_{34}$,$\theta_{012}$,$\theta_{013}$,$\theta_{014}$,$\theta_{023}$, $\theta_{024}$,$\theta_{123}$,$\theta_{124}$,$\theta_{134}$,$\theta_{234}$,$\Gamma_{0123}$,$\Gamma_{0124}$,$\Gamma_{0134}$,$\Gamma_{0234}$,$\Gamma_{1234}$)

   with objects, $1$-morphisms, and $2$-morphisms as in the diagram
   [[4-simplex-duskin.svg:pic]]
   and $3$-morphisms as in the diagrams
   \begin{imagefromfile}
       "file_name": "4-simplex-street.svg",
       "width":     "800"
   \end{imagefromfile}
   such that the diagram
   \begin{imagefromfile}
       "file_name": "street-4th-oriental.svg",
       "width":     "800"
   \end{imagefromfile}
   corresponding to [[Street]]'s fourth [[oriental]], commutes. (See [ [here] ](https://ncatlab.org/nlab/files/street-nerve-fourth-oriental.pdf) for a zoomable PDF).

6. The $n$-simplices of $\mathrm{N}^\mathsf{S}_{\bullet}(\mathcal{C})$, similarly to the $4$-simplices of $\mathrm{N}^\mathsf{S}_{\bullet}(\mathcal{C})$, consist of

   * A collection $\{A_{i}\}_{0\leq i\leq n}$ of objects of $\mathcal{C}$,
   * A collection $\{f_{ij}\colon A_{i}\longrightarrow A_{j}\}_{0\leq i\lt j\leq n}$ of $1$-morphisms of $\mathcal{C}$,
   * A collection $\{\theta_{ijk}\colon f_{jk}\circ f_{ij}\Rightarrow f_{ik}\}_{0\leq i\lt j\lt k\leq n}$ of $2$-morphisms of $\mathcal{C}$, and
   * A collection $\{\Gamma_{ijkl}\}_{0\leq i\lt j\lt k\lt l\leq n}$ of $3$-morphisms of $\mathcal{C}$

   such that, for each $i,j,k,l\in\N$ with $0\leq i\lt j\lt k\lt l\leq n$, the diagram corresponding to [[Street]]'s fourth [[oriental]] above commutes.
7. The degeneracy map
   $$\mathrm{s}^{0}_{0}\colon \mathrm{N}^{\mathsf{S}}_{0}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{1}(\mathcal{C})$$
   of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$ in degree $0$ is the map sending a $0$-simplex $A$ of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$ (i.e. an object $A$ of $\mathcal{C}$) to the $1$-simplex $\mathrm{id}_{A}\colon A\to A$.

8. The degeneracy maps
   $$
   \mathrm{s}^{1}_{0} \colon \mathrm{N}^{\mathsf{S}}_{1}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C}),
   $$
   $$
   \mathrm{s}^{1}_{1} \colon \mathrm{N}^{\mathsf{S}}_{1}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C}),
   $$
   of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$ in degree $1$ are the maps described as follows: given a $1$-simplex $\sigma=(A\xrightarrow{f}B)$ of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$, we have
   [[deg-1-degeneracies-of--duskin-nerve.svg:pic]]

9. The degeneracy maps in degree $2$
   $$
   \mathrm{s}^{2}_{0} \colon \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{3}(\mathcal{C}),
   $$
   $$
   \mathrm{s}^{2}_{1} \colon \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{3}(\mathcal{C}),
   $$
   $$
   \mathrm{s}^{2}_{2} \colon \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{3}(\mathcal{C}),
   $$
   of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$  in degree $2$ are the maps described as follows: given a $2$-simplex
   [[2-simplex-duskin-sigma.svg:pic]]
   of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$, we have (page author's note: please take the following $3$-morphisms with a grain of salt; I'm quite unsure about whether they are correct or not. In any case, note that we _must_ use the left, middle, and right $2$-unitors of $\mathcal{C}$ here---this is where they appear in the Street nerve!)
   \begin{imagefromfile}
       "file_name": "deg-2-degeneracies-street-1-new.svg",
       "width":     "800"
   \end{imagefromfile}
   \begin{imagefromfile}
       "file_name": "deg-2-degeneracies-street-2.svg",
       "width":     "800"
   \end{imagefromfile}
   \begin{imagefromfile}
       "file_name": "deg-2-degeneracies-street-3-new.svg",
       "width":     "800"
   \end{imagefromfile}
   For the details regarding these pastings, see [ [this PDF] ](https://ncatlab.org/nlab/files/pastings-in-street-nerve.pdf).

10. The face maps
   $$
   \mathrm{d}^{1}_{0} \colon \mathrm{N}^{\mathsf{S}}_{1}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{0}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{1}_{1} \colon \mathrm{N}^{\mathsf{S}}_{1}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{0}(\mathcal{C}),
   $$
   of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$ in degree $1$ are given by
   $$\mathrm{d}^{1}_{0}(A\xrightarrow{f}B)=B$$
   $$\mathrm{d}^{1}_{1}(A\xrightarrow{f}B)=A$$

11. The face maps
   $$
   \mathrm{d}^{2}_{0} \colon \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{1}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{2}_{1} \colon \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{1}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{2}_{1} \colon \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{1}(\mathcal{C}),
   $$
   of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$ in degree $2$ are described as follows: given a $2$-simplex
   [[2-simplex-duskin-sigma.svg:pic]]
   of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$, we have
   [[face-maps-deg-2-duskin.svg:pic]]

12. The face maps
   $$
   \mathrm{d}^{3}_{0} \colon \mathrm{N}^{\mathsf{S}}_{3}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{3}_{1} \colon \mathrm{N}^{\mathsf{S}}_{3}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{3}_{2} \colon \mathrm{N}^{\mathsf{S}}_{3}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C}),
   $$
   $$
   \mathrm{d}^{3}_{3} \colon \mathrm{N}^{\mathsf{S}}_{3}(\mathcal{C})\longrightarrow \mathrm{N}^{\mathsf{S}}_{2}(\mathcal{C}),
   $$
   of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$ in degree $3$ are described as follows: given a $3$-simplex $\sigma$ of $\mathrm{N}^\mathsf{S}_\bullet(\mathcal{C})$ as in the diagram
   [[3-simplex-of-the-street-nerve.svg:pic]]
   we have
   [[face-maps-deg-3-duskin.svg:pic]]


## Related concepts

* [[nerve]]

* [[geometric nerve of a bicategory]]

* **geometric nerve of a tricategory**

* [[∞-nerve]]

* [[homotopy coherent nerve]]


## References

* {#CegarraHeredia2012} Antonio M. Cegarra and Benjamín A. Heredia, _Geometric Realizations of Tricategories_. Algebraic & Geometric Topology 14, no. 4 (2014): 1997-2064. [ [arXiv:1203.3664] ](https://arxiv.org/abs/1203.3664) 

* {#Carrasco2014} Pilar Carrasco, _Nerves of Trigroupoids as Duskin-Glenn’s $3$-Hypergroupoids_, Applied Categorical Structures 23.5 (2015): 673–707.

* {#LackPaoli2006} Stephen Lack and Simona Paoli, _2-nerves for bicategories_, Journal of $K$-Theory 38.2 (2008): 153–175. [ [arXiv:0607271] ](https://arxiv.org/abs/math/0607271).

* {#Street1987} [[Ross Street]], _The algebra of oriented simplexes_, Journal of Pure and Applied Algebra, Volume 49, Issue 3, December 1987, Pages 283&#8211;335.

* {#GPS1995} [[Robert Gordon]], [[John Power]], [[Ross Street]], _Coherence for tricategories_, Mem. Amer. Math Soc. 117 (1995) no 558.

* {#Duskin2002} [[John Duskin]], _Simplicial matrices and the nerves of weak n-categories I: nerves of bicategories_ ([tac](http://www.tac.mta.ca/tac/volumes/9/n10/9-10abs.html)), Theory and Applications of Categories, Vol. 9, No. 10, 2002, pp. 198&#8211;308.
{#Duskin}