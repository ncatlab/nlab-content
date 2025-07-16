+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

### Idea

**Ultracategories** are [[categories]] endowed with [[extra structure]] meant to abstract the possibility of forming [[ultraproducts]]. They were introduced by [Makkai](#Makkai87) in order to prove [[conceptual completeness | strong conceptual completeness]] for [[coherent logic]], thus allowing to reconstruct a coherent theory from its category of [[models]]. 

\begin{theorem}[Makkai]\label{thm:makkai}
Let $P$ be a small [[pretopos]] and let $\operatorname{Mod}(P) = \mathbf{Pretop}(P, Set)$ be its category of models. Then, the evaluation functor
\[ ev : P \to \mathbf{Ult} ( \operatorname{Mod}(P) , Set ) \]
is an [[equivalence of categories]], where $\mathbf{Ult}$ is the [[2-category ]] of ultracategories, ultrafunctors, and transformations thereof.
\end{theorem}

To provide intuition on ultracategories, let's start by recalling that a [[compact Hausdorff space]] $K$ can be seen as a [[relational beta-module | relational $\beta$-module ]] where each [[ultrafilter]] $\mu$ on $K$ [[convergence | converges]] to a unique _limit_, namely the unique point $x \in K$ such that every open neighborhood of $x$ in $K$ lies in $\mu$, so as to determine a function $\beta K \to K$. More generally, we can say that a function $f \colon I \to K$ for some set $I$ _converges_ with respect to some ultrafilter $\mu$ on $I$ to the limit of the ultrafilter $f_*(\mu) = \{ S \subseteq K | f^{-1}(K) \in \mu\}$, i.e. the unique point $x \in K$ such that every open neighborhood of $x$ in $K$ contains a $\mu$-large subset of values of $f$. This way, the convergence relation on $K$ can be seen as a family of functions 
\[ K^I \times \beta I \to K\]
for each set $I$: in the same spirit, an _ultrastructure_ (called _pre-ultracategory_ in [Makkai](#Makkai)) on a category $\mathcal{M}$ is given at its core by a family of [[functors]]
\[ \mathcal{M}^I \times \beta I \to \mathcal{M} \]
satisfying some axioms. Different, inequivalent, choices are possible for the precise axiomatization: most notably, [Lurie](#Lurie)'s definition of ultracategories (together with the introduction of new morphisms between them) allowed to extend Makkai's result to a reconstruction theorem for [[coherent toposes]], and it formalizes the idea that ultracategories categorify compact Hausdorff spaces (see [Lurie, Thm 3.1.5](#Lurie)).

\begin{theorem}[Lurie]\label{thm:lurie}
Let $P$ be a small pretopos and let $\mathcal{E} = Sh(P)$ be its coherent topos of sheaves. Then, the evaluation functor $ev : P \to \mathbf{Ult}^L (\operatorname{Mod}(P) , Set )$ induces an equivalence 
\[ \mathcal{E} \simeq \mathbf{Ult}^L ( \operatorname{Mod}(P) , Set ) \]
where $\mathbf{Ult}^L$ is the $2$-category of ultracategories, left ultrafunctors, and transformations thereof. In particular, $ev$ is an equivalence $P \simeq \mathbf{Ult} (\operatorname{Mod}(P) , Set )$, where $\mathbf{Ult}$ is the [[locally full sub-2-category]] of $\mathbf{Ult}^L$ determined by ultrafunctors.
\end{theorem}

Lurie's axiomatization was proved by [Hamad](#Hamad) to coincide with that of [[colax algebra | normal colax algebras]] for a [[pseudomonad]] on the 2-category of locally small categories. [Tarantino and Wrigley](#TarWrig) weakened Lurie's definition to obtain an axiomatization of ultracategories sharing the same properties, but emerging universally from the [[ultrafilter monad]] by means of a kind of [[ Kan extension ]]. Instead, [Saadia](#Saadia) and [Hamad](#HamadGen) independently introduced _virtual ultracategories_ as a [[generalized multicategory | multicategorical]] generalization of ultracategories which allows to extend Lurie's result to [[point of a topos | toposes with enough points]]; the former, in particular, introduces yet another axiomatization of ultracategories, satisfying the same reconstruction theorem above, as a particular case of virtual ultracategories. If ultracategories categorify compact Hausdorff spaces, _virtual_ ultracategories categorify all topological spaces, allowing for maps into an abstract ultraproduct which may not exist in the underlying category.


### Related concepts

* In ([Clementino-Tholen 03](#ClemTholen)), a different concept of ultracategory is introduced as an instance of a [[generalized multicategory]]. 

* [[conceptual completeness]]

### References

* {#Makkai87} [[Mihaly Makkai]], _Stone duality for first-order logic_, Adv. Math. __65__ (1987) no. 2, 97--170, [doi](http://dx.doi.org/10.1016/0001-8708%2887%2990020-X),  [MR89h:03067](http://www.ams.org/mathscinet-getitem?mr=900266)

* Marek W. Zawadowski, _Descent and duality_, Annals of Pure and Applied Logic __71__, n.2 (1995), 131&#8211;188

* {#Lurie} [[Jacob Lurie]], _Ultracategories_ ([pdf](http://www.math.harvard.edu/~lurie/papers/Conceptual.pdf))

For a different notion of ultracategory see

* {#ClemTholen} [[Maria Manuel Clementino]], [[Walter Tholen]], _Metric, topology and multicategory--a common approach_, J. Pure Appl. Algebra 179 (2003) 13-47, ([doi:10.1016/S0022-4049(02)00246-3](https://doi.org/10.1016/S0022-4049%2802%2900246-3)).


On a [[2-monad|2-monadic]] treatment of ultracategories:

* [[Francisco Marmolejo]], _Ultraproducts and continuous families of models_, PhD thesis (1995) &lbrack;[hdl:10222/55092](https://dalspace.library.dal.ca/handle/10222/55092); [pdf](http://peterlefanulumsdaine.com/files/marmolejo-1995-phd-thesis.pdf)&rbrack;

As [[colax algebra for a 2-monad|colax algebras]] for a [[pseudomonad]]:

* {#Hamad} Ali Hamad, *Ultracategories as colax algebras for a pseudo-monad on CAT* &lbrack;[arXiv:2502.20597](https://arxiv.org/abs/2502.20597)&rbrack;

In terms of [[Kan extensions]] of [[relative monads]]:

* {#TarWrig} [[Umberto Tarantino]], Joshua Wrigley, *Ultracategories via Kan extensions of relative monads* &lbrack;[arXiv:2506.09788](https://arxiv.org/abs/2506.09788)&rbrack;

For a generalization to *virtual* ultracategories, a [[categorification]] of [[relational beta-modules]], designed to allow reconstruction of any [[topos with enough points]], see

* {#Saadia} Gabriel Saadia, _Extending conceptual completeness via virtual ultracategories_ &lbrack;[arXiv:2506.23935](https://arxiv.org/abs/2506.23935)&rbrack;
* {#HamadGen} Ali Hamad, *Generalised ultracategories and conceptual completeness of geometric logic* &lbrack;[arXiv:2507.07922](https://arxiv.org/abs/2507.07922)&rbrack;


[[!redirects ultracategories]]


