
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

A **pseudofunctor** is a specific algebraic notion of _weak [[2-functor]]_ between [[bicategory|bicategories]] (including [[strict 2-category|strict 2-categories]]), i.e. a [[2-functor]] which preserves [[composition]] and [[identity morphism|identities]] of [[1-morphisms]] only up to [[coherent]] specified 2-[[isomorphism]]. (In contrast to _[[strict 2-functors]]_.)


In general, there is not much reason to say "pseudofunctor" instead of "functor," since by far the most important type of functor between arbitrary bicategories is weak.  However, if the domain and codomain are known to be [[strict 2-category|strict 2-categories]] (including ordinary $1$-[[1-category|categories]]), it can be helpful to say "pseudofunctor" or "weak functor" to emphasize that it is not a [[strict 2-functor]].  Note that if the codomain is a $1$-category, then there is no difference.

Pseudo or weak functors are also to be distinguished from [[lax functor]]s and [[lax functor|oplax functor]]s, which preserve identities and composition only up to a  transformation in one direction or the other, which may be non-invertible.

An older terminology, which should probably be avoided at all costs, uses "homomorphism of bicategories" for a weak functor and "morphism of bicategories" for a lax one.


## Definition

Given [[bicategories]] $C$ and $D$, a __pseudofunctor__ (or __weak $2$-functor__, or just __functor__) $P:C \to D$ consists of:

*  A function
\[
P:Ob_C\to Ob_D.
\]
*  For each [[hom-category]] $C(x,y)$ in $C$, a [[functor]] 
\[
P_{x,y}\colon C(x,y) \rightarrow D(P_x,P_y).
\]
*  For each object $x$ of $C$, an invertible [[2-morphism]] ($2$-cell)
\[
P_{\id_x}\colon \id_{P_x} \Rightarrow P_{x,x}(\id_x).
\]
*  For each triple $x,y,z$ of $C$-objects, an [[natural isomorphism|isomorphism]] (natural in $f\colon x \to y$ and $g\colon y \to z$) 
\[
P_{f,g}\colon P_{y,z}(g)\circ P_{x,y}(f) \Rightarrow P_{x,z}(g\circ f)
\]
*  For each hom-category $C(x,y)$,
<!-- https://q.uiver.app/#q=WzAsNCxbMCwwLCJQX3t4LCB5fShmKVxcY2lyYyBcXG9wZXJhdG9ybmFtZXtpZH1fe1BfeH0iXSxbMiwwLCJQX3t4LCB5fShmKSJdLFsyLDIsIlBfe3gseX0oZlxcY2lyYyBcXG9wZXJhdG9ybmFtZXtpZH1feCkiXSxbMCwyLCJQX3t4LHl9KGYpXFxjaXJjIFBfe3gseH0oXFxvcGVyYXRvcm5hbWV7aWR9X3gpIl0sWzAsMSwiXFxsYW1iZGFfe1Bfe3gseX0oZil9IiwwLHsibGV2ZWwiOjJ9XSxbMCwzLCJcXG9wZXJhdG9ybmFtZXtpZH1fe1Bfe3gseX0oZil9KlBfe1xcb3BlcmF0b3JuYW1le2lkfV94fSIsMix7ImxldmVsIjoyfV0sWzMsMiwiUF97eCx4LHl9KFxcb3BlcmF0b3JuYW1le2lkfV94LGYpIiwyLHsibGV2ZWwiOjJ9XSxbMiwxLCJQX3t4LHl9KFxcbGFtYmRhX2YpIiwyLHsibGV2ZWwiOjJ9XV0= -->
\begin{centre}
    \begin{tikzcd}
	{P_{x, y}(f)\circ \operatorname{id}_{P_x}} && {P_{x, y}(f)} \\
	\\
	{P_{x,y}(f)\circ P_{x,x}(\operatorname{id}_x)} && {P_{x,y}(f\circ \operatorname{id}_x)}
	\arrow["{\lambda_{P_{x,y}(f)}}", Rightarrow, from=1-1, to=1-3]
	\arrow["{\operatorname{id}_{P_{x,y}(f)}*P_{\operatorname{id}_x}}"', Rightarrow, from=1-1, to=3-1]
	\arrow["{P_{f, \operatorname{id}_x}(\operatorname{id}_x,f)}"', Rightarrow, from=3-1, to=3-3]
	\arrow["{P_{x,y}(\lambda_f)}"', Rightarrow, from=3-3, to=1-3]
\end{tikzcd}
\end{centre}
and
<!-- https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXG9wZXJhdG9ybmFtZXtpZH1fe1BfeX0gXFxjaXJjIFBfe3gseX0oZikiXSxbMCwyLCJQX3t5LHl9KFxcb3BlcmF0b3JuYW1le2lkfV95KVxcY2lyYyBQX3t4LHl9KGYpIl0sWzIsMiwiUF97eCx5fShcXG9wZXJhdG9ybmFtZXtpZH1feVxcY2lyYyBmKSJdLFsyLDAsIlBfe3gseX0oZikiXSxbMCwzLCJcXHJob197UF97eCx5fShmKX0iLDAseyJsZXZlbCI6Mn1dLFswLDEsIlBfe1xcb3BlcmF0b3JuYW1le2lkfV95fSAqIFxcb3BlcmF0b3JuYW1le2lkfV97UF97eCx5fShmKX0iLDIseyJsZXZlbCI6Mn1dLFsxLDIsIlBfe2YsIFxcb3BlcmF0b3JuYW1le2lkfV95fShcXG9wZXJhdG9ybmFtZXtpZH1feVxcY2lyYyBmKSIsMix7ImxldmVsIjoyfV0sWzIsMywiUF97eCx5fShcXHJob19mKSIsMix7ImxldmVsIjoyfV1d -->
\begin{centre}
    \begin{tikzcd}
	{\operatorname{id}_{P_y} \circ P_{x,y}(f)} && {P_{x,y}(f)} \\
	\\
	{P_{y,y}(\operatorname{id}_y)\circ P_{x,y}(f)} && {P_{x,y}(\operatorname{id}_y\circ f)}
	\arrow["{\rho_{P_{x,y}(f)}}", Rightarrow, from=1-1, to=1-3]
\arrow["{P_{\operatorname{id}_y} * \operatorname{id}_{P_{x,y}(f)}}"', Rightarrow, from=1-1, to=3-1]
	\arrow["{P_{f, \operatorname{id}_y}(\operatorname{id}_y\circ f)}"', Rightarrow, from=3-1, to=3-3]
	\arrow["{P_{x,y}(\rho_f)}"', Rightarrow, from=3-3, to=1-3]
    \end{tikzcd}
\end{centre}
   commute.

*  For each quadruple $w,x,y,z$ of $C$-objects,
<!-- https://q.uiver.app/#q=WzAsNixbMCwwLCJQX3t5LHp9KGgpXFxjaXJjIChQX3t4LHl9KGcpXFxjaXJjIFBfe3cseH0oZikpIl0sWzAsMiwiUF97eSx6fShoKVxcY2lyYyBQX3t3LHl9KGdcXGNpcmMgZikiXSxbMCw0LCJQX3t3LHp9KGhcXGNpcmMoZ1xcY2lyYyBmKSkiXSxbMiwwLCIoUF97eSx6fShoKVxcY2lyYyBQX3t4LHl9KGcpKVxcY2lyYyBQX3t3LHh9KGYpIl0sWzIsMiwiUF97eCx6fShoXFxjaXJjIGcpXFxjaXJjIFBfe3cseH0oZikiXSxbMiw0LCJQX3t3LHp9KChoXFxjaXJjIGcpXFxjaXJjIGYpIl0sWzAsMywiXFxhbHBoYV97UF97dyx6fShmKSxQX3t4LHl9KGcpLFBfe3ksen0oaCl9IiwwLHsibGV2ZWwiOjJ9XSxbMCwxLCJcXG9wZXJhdG9ybmFtZXtpZH1fe1Bfe3ksen0oaCl9ICogUF97ZixnfSIsMix7ImxldmVsIjoyfV0sWzEsMiwiUF97Z1xcY2lyYyBmLCBofSIsMix7ImxldmVsIjoyfV0sWzIsNSwiUF97dyx6fShcXGFscGhhX3tmLGcsaH0pIiwyLHsibGV2ZWwiOjJ9XSxbMyw0LCJQX3tnLGh9XFxjaXJjIFxcb3BlcmF0b3JuYW1le2lkfV97UF97dyx4fShmKX0iLDAseyJsZXZlbCI6Mn1dLFs0LDUsIlBfe2YsIGhcXGNpcmMgZ30iLDAseyJsZXZlbCI6Mn1dXQ== -->
\begin{centre}
\[\begin{tikzcd}
	{P_{y,z}(h)\circ (P_{x,y}(g)\circ P_{w,x}(f))} && {(P_{y,z}(h)\circ P_{x,y}(g))\circ P_{w,x}(f)} \\
	\\
	{P_{y,z}(h)\circ P_{w,y}(g\circ f)} && {P_{x,z}(h\circ g)\circ P_{w,x}(f)} \\
	\\
	{P_{w,z}(h\circ(g\circ f))} && {P_{w,z}((h\circ g)\circ f)}
	\arrow["{\alpha_{P_{w,x}(f),P_{x,y}(g),P_{y,z}(h)}}", Rightarrow, from=1-1, to=1-3]
	\arrow["{\operatorname{id}_{P_{y,z}(h)} * P_{f,g}}"', Rightarrow, from=1-1, to=3-1]
	\arrow["{P_{g,h}\circ \operatorname{id}_{P_{w,x}(f)}}", Rightarrow, from=1-3, to=3-3]
	\arrow["{P_{g\circ f, h}}"', Rightarrow, from=3-1, to=5-1]
	\arrow["{P_{f, h\circ g}}", Rightarrow, from=3-3, to=5-3]
	\arrow["{P_{w,z}(\alpha_{f,g,h})}"', Rightarrow, from=5-1, to=5-3]
\end{tikzcd}
\end{centre}
   commutes.

A pseudofunctor is **strict** if the structural isomorphisms for identities of 1-cells and composites are identity 2-cells.

### Composition of Pseudofunctors

The composite of two pseudofunctors $P:\mathfrak{C}\to\mathfrak{D}$, $Q:\mathfrak{B}\to\mathfrak{C}$ is defined as follows:

1. Action on objects is given by function composition, so
$$
P\circ Q(X)=P(Q(X))
$$
1. Hom functors are given by functor composition, so
$$
(P\circ Q)_{XY}=P_{XY}\circ Q_{XY}
$$
1. For each object $X\in\mathfrak{B}$,
$$
(P\circ Q)_{id_X}=P(Q_{id_X})\circ P_{id_{Q(X)}}
$$
1. For each pair of composable arrows $f:Y\to Z$, $g:X\to Y\in\mathfrak{B}$,
$$
(P\circ Q)_{f,g}=P(Q_{f,g})\circ P_{Q(f),Q(g)}
$$

Coherence diagrams commute as a consequence of the coherence diagrams for $P$ and $Q$ commuting.

## Pseudofunctors versus lax functors

If we remove the requirement that $P_{\id_x}$ and $P_{x,y,z}(f,g)$ be invertible, then we have the definition of __[[lax functor]]__.  Thus, a pseudofunctor may be defined as a lax functor whose comparison constraints are invertible.

If in the definition of lax functor we reverse the direction of the constraints, then we have an __[[oplax functor]]__.  Thus, if we consider the *inverses* of the constraints of a pseudofunctor, we obtain an oplax functor.  Because there is little difference between specifying an invertible morphism and specifying its invertible inverse, one could equally well define a pseudofunctor to be an oplax functor whose constraints are invertible (i.e. reverse the direction of the isomorphisms $P_{\id_x}$ and $P_{x,y,z}(f,g)$ above), and in the literature one sometimes finds this definition instead.

Of course, in particular applications, one direction or the other may be slightly more "natural".  For instance, when a [[Grothendieck fibration]] $E\to B$ gives rise to a pseudofunctor $B^{op} \to Cat$, the natural comparison maps (induced by the universal property of [[cartesian arrows]]) go in the "lax direction".  Dually, when a Grothendieck opfibration $E\to B$ gives rise to a pseudofunctor $B\to Cat$, the natural comparison maps go in the "oplax direction". 

## Strictification 

For $C$ a strict 2-category, there is a universal procedure for replacing pseudofunctors $F \colon C \to Cat$ with strict 2-functors $\hat{F} \colon C \to Cat$, where "universal" is in the following sense: 

+-- {: .num_prop}
###### Proposition 
For any pseudofunctor $F \colon C \to Cat$, there is a strict 2-functor $\hat{F}\colon C\to Cat$ and a pseudonatural equivalence $\eta_F\colon F\to \hat{F}$.  Moreover, for any strict 2-functor $G \colon C \to Cat$, composing with $\eta_F$ yields an isomorphism between the category of pseudonatural transformations $F \to G$ and modifications between them, and the category of strict natural transformations $\hat{F} \to G$ and modifications between them.
=-- 

+-- {: .proof} 
###### Proof (Sketch) 
For each object $c$ of $C$, define $\hat{F}(c)$ to be the category whose objects are pairs $(f, x)$ with $f \colon d \to c$ in $C$ and $x \in Ob(F(d))$, and whose morphisms $(f, x) \to (f', x')$ are morphisms $F(f)(x) \to F(f')(x')$ in $F(c)$.  For $g \colon c \to c'$ in $C$, the functor $\hat{F}(g) \colon \hat{F}(c) \to \hat{F}(c')$ takes $(f, x)$ to $(g f, x)$; notice $\hat{F}(-)$ preserves compositions $g' \circ g$ strictly since composition in $C$ is strictly associative. (Strictly speaking we have only defined the functor $\hat{F}(g)$ at the object level. However, the extension to morphisms $\theta \colon F(f)(x) \to F(f)(x')$ is the obvious one, where 

$$\hat{F}(g)(\theta) \coloneqq (F(g f)(x) \cong F(g)(F(f)(x)) \stackrel{F(g)(\theta)}{\to} F(g)(F(f)(x')) \cong F(g f)(x'))$$ 

preserves compositions $\theta' \circ \theta$ by naturality of the structural constraints $F(g)F(f) \cong F(g f)$.) Similarly, for 2-cells $\alpha: g \to g'$, the natural transformation $\hat{F}(\alpha) \colon \hat{F}(g) \to \hat{F}(g')$ is defined by taking its component at an object $(f, x)$ to be given by pasting in the first component: $F(\alpha \cdot f)(x) \colon F(g f)(x) \to F(g' f)(x)$. 

One easily checks that $\hat{F}$ is pseudonaturally equivalent to $F$...
=-- 

The construction of the strictification is a special case of a general strictification construction due to [Power](#Pow). Later Steve Lack [showed](#Lack) that the strictifications obtained from Power's coherence theorem always have a universal property analogous to that of the result above.

We also have the following result: 

+-- {: .num_prop}
###### Proposition 
Given bicategories $C$ and $D$, for any pseudofunctor $F \colon C \to D$, there is a pseudofunctor $\hat{F}\colon C\to D$ that strictly preserves identity 1-morphisms, and a pseudonatural equivalence $\eta_F\colon F\to \hat{F}$.  
=-- 

+-- {: .proof} 
###### Proof  
This is Proposition 5.2 of [Lack and Paoli](#LP).  Pseudofunctors that strictly preserve identity 1-morphisms are called
**normal**.  
=--


## History

Historically the term 'pseudofunctor' was conceived by [[Grothendieck]] who weakened, around 1957, the concept of a [[contravariant functor]] from a [[1-category]] to [[Cat]], by effectively replacing the $1$-category Cat by the [[2-category]] $Cat$ and allowing (contravariant) functoriality up to coherent $2$-cells. This was recorded in his [[Bourbaki]] seminar on [[descent]] via pseudofunctors. Later in [[SGA1]] Grothendieck (with the assistance of [[Pierre Gabriel]]) replaced pseudofunctors in the treatment of descent by more invariant [[fibered categories]]. [[Benabou]], in his 1967 [treatise](#Ben) introducing [[bicategories]], generalized the pseudofunctors of Grothendieck to pseudofunctors between arbitrary bicategories but under the name 'homomorphism of bicategories'. 

## Related concepts


* [[function]]

* [[functor]]

* [[2-functor]] / **pseudofunctor**

  * [[monoidal functor]]

* [[n-functor]]

* [[(∞,1)-functor]]

* [[(∞,n)-functor]]


## References 

The notion of pseudo-functors from a [[1-category]] to the [[2-category]] [[Cat]] originates with:

* [[Alexander Grothendieck]], §A.1 in: *Technique de descente et théorèmes d’existence en géométrie algébrique. I. Généralités. Descente par morphismes fidèlement plats*, Séminaire [[N. Bourbaki]] exp. no190 (1960) 299-327 &lbrack;[numdam:SB_1958-1960__5__299_0](http://www.numdam.org/item/?id=SB_1958-1960__5__299_0)&rbrack;

(where it is still called "[[fibered categories]]", a term that eventually came to refer to the [equivalent incarnation](Grothendieck+construction#EquivalenceBetweenFiberedCategoriesAndPsuedofunctors) of pseudofunctors as their [[Grothendieck constructions]]).

Review:

* [[Angelo Vistoli]], Def. 3.10 in: *Grothendieck topologies, fibered categories and descent theory*, in: *[[Fundamental algebraic geometry -- Grothendieck's FGA explained]]*, Mathematical Surveys and Monographs **123**, Amer. Math. Soc. (2005) 1-104 &lbrack;[ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [math.AG/0412512](http://arxiv.org/abs/math/0412512)&rbrack;


The general notion of pseudo-functors between [[bicategories]] is introduced as **homomorphisms of bicategories** in:

* {#Ben} [[Jean Bénabou]], *Introduction to Bicategories*, Lecture Notes in Mathematics **47** Springer (1967), pp.1-77 &lbrack;[doi:10.1007/BFb0074299](http://dx.doi.org/10.1007/BFb0074299)&rbrack;

In the above, [[strict pseudofunctors]] are called **strict homomorphisms of bicategories** and [[lax functors]] are called **morphisms of bicategories**.

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], *2-Dimensional Categories*, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))


See also:

* {#Lack} [[Stephen Lack]], _Codescent objects and coherence_, JPAA Vol. 175 (2002), 223-241. ([web](http://www.sciencedirect.com/science/journal/00224049/175/1))
 

* [[Stephen Lack]] and [[Simona Paoli]], 2-nerves for bicategories, $K$-Theory 38 (2008), 153-175.   ([arxiv](https://arxiv.org/abs/math/0607271)).
{#LP}

* A. J. Power, _A general coherence result_, JPAA Vol. 57 Iss. 2 (1989), 165-173. ([web](http://www.sciencedirect.com/science/article/pii/0022404989901138)) 
{#Pow}


[[!redirects pseudofunctors]]
[[!redirects pseudo functor]]
[[!redirects pseudo functors]]
[[!redirects pseudo-functor]]
[[!redirects pseudo-functors]]
[[!redirects strict pseudofunctor]]
[[!redirects strict pseudofunctors]]

[[!redirects weak 2-functor]]
[[!redirects weak 2-functors]]

[[!redirects homomorphism of bicategories]]
[[!redirects homomorphisms of bicategories]]