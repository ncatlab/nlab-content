
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

# Pseudofunctors
* table of contents
{: toc}

## Idea

A **pseudofunctor** is a specific algebraic notion of _weak [[2-functor]]_ between [[bicategory|bicategories]] (including [[strict 2-category|strict 2-categories]]), i.e. a [[2-functor]] which preserves [[composition]] and [[identity morphism|identities]] of [[1-morphisms]] only up to [[coherent]] specified 2-[[isomorphism]]. (In contrast to _[[strict 2-functors]]_.)


In general, there is not much reason to say "pseudofunctor" instead of "functor," since by far the most important type of functor between arbitrary bicategories is weak.  However, if the domain and codomain are known to be [[strict 2-category|strict 2-categories]] (including ordinary $1$-[[1-category|categories]]), it can be helpful to say "pseudofunctor" or "weak functor" to emphasize that it is not a [[strict 2-functor]].  Note that if the codomain is a $1$-category, then there is no difference.

Pseudo or weak functors are also to be distinguished from [[lax functor]]s and [[lax functor|oplax functor]]s, which preserve identities and composition only up to a  transformation in one direction or the other, which may be non-invertible.

An older terminology, which should probably be avoided at all costs, uses "homomorphism of bicategories" for a weak functor and "morphism of bicategories" for a lax one.


## Definition

Given [[bicategories]] $C$ and $D$, a __pseudofunctor__ (or __weak $2$-functor__, or just __functor__) $P\colon C \to D$ consists of:

*  for each [[object]] $x$ of $C$, an object $P_x$ of $D$;
*  for each [[hom-category]] $C(x,y)$ in $C$, a [[functor]] $P_{x,y}\colon C(x,y) \rightarrow D(P_x,P_y)$;
*  for each object $x$ of $C$, an invertible [[2-morphism]] ($2$-cell) $P_{\id_x}\colon \id_{P_x} \Rightarrow P_{x,x}(\id_x)$;
*  for each triple $x,y,z$ of $C$-objects, an [[natural isomorphism|isomorphism]] (natural in $f\colon x \to y$ and $g\colon y \to z$) $P_{x,y,z}(f,g)\colon P_{x,y}(f) ; P_{y,z}(g) \Rightarrow P_{x,z}(f;g)$;
*  for each hom-category $C(x,y)$,
   $$ \array {
                                  &                                         & \id_{P_x} ; P_{x,y}(f) \\
                                  & {}^{P_{\id_x};\id_{P_{x,y}(f)}}\swArrow &                        & \seArrow^{\lambda_{P_{x,y}(f)}} \\
      P_{x,x}(\id_x) ; P_{x,y}(f) &                                         &                        &                                 & P_{x,y}(f) \\
                                  & {}_{P_{x,x,y}(\id_x,f)}\seArrow         &                        & \neArrow_{P_{x,y}(\lambda_f)} \\
                                  &                                         & P_{x,y}(\id_x;f) \\
   } $$
   and
   $$ \array {
                                  &                                         & P_{x,y}(f) ; \id_{P_y} \\
                                  & {}^{\id_{P_{x,y}(f)};P_{\id_y}}\swArrow &                        & \seArrow^{\rho_{P_{x,y}(f)}} \\
      P_{x,y}(f) ; P_{y,y}(\id_y) &                                         &                        &                              & P_{x,y}(f) \\
                                  & {}_{P_{x,y,y}(f,\id_y)}\seArrow         &                        & \neArrow_{P_{x,y}(\rho_f)} \\
                                  &                                         & P_{x,y}(f;\id_y) \\
   } $$
   commute; and
*  for each quadruple $w,x,y,z$ of $C$-objects,
   $$ \array {
      \big(P_{w,x}(f) ; P_{x,y}(g)\big) ; P_{y,z}(h)       & \overset{\alpha_{P_{w,x}(f),P_{x,y}(g),P_{y,z}(h)}}\Rightarrow & P_{w,x}(f) ; \big(P_{x,y}(g) ; P_{y,z}(h)\big) \\
      \mathllap{P_{w,x,y}(f,g);\id_{P_{y,z}(h)}}\Downarrow &                                                                & \Downarrow\mathrlap{\id_{P_{w,x}(f)};P_{x,y,z}(g,h)} \\
      P_{w,y}(f;g) ; P_{y,z}(h)                            &                                                                & P_{w,x}(f) ; P_{x,z}(g;h) \\
      \mathllap{P_{w,y,z}(f;g,h)}\Downarrow                &                                                                & \Downarrow\mathrlap{P_{w,x,z}(f,g;h)} \\
      P_{w,z}\big((f;g);h\big)                             & \underset{P_{w,z}(\alpha_{f,g,h})}\Rightarrow                  & P_{w,z}\big(f;(g;h)\big) \\
   } $$
   commutes.

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
This is Proposition 5.1 of [Lack and Paoli](#LP).  Pseudofunctors that strictly preserve identity 1-morphisms are called
**normal**.  
=---


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

* [[Jean Bénabou]], _Introduction to bicategories_, Springer LNM 47 (1967), 1-77. 
{#Ben} 

* [[Stephen Lack]], _Codescent objects and coherence_, JPAA Vol. 175 (2002), 223-241. ([web](http://www.sciencedirect.com/science/journal/00224049/175/1))
{#Lack} 

* [[Stephen Lack]] and [[Simona Paoli]], 2-nerves for bicategories, $K$-Theory 38 (2008), 153-175.   ([arxiv](https://arxiv.org/abs/math/0607271)).
{#LP}

* A. J. Power, _A general coherence result_, JPAA Vol. 57 Iss. 2 (1989), 165-173. ([web](http://www.sciencedirect.com/science/article/pii/0022404989901138)) 
{#Pow}






[[!redirects pseudofunctors]]
[[!redirects pseudo functor]]
[[!redirects pseudo functors]]
[[!redirects pseudo-functor]]
[[!redirects pseudo-functors]]

[[!redirects weak 2-functor]]
[[!redirects weak 2-functors]]

[[!redirects homomorphism of bicategories]]
[[!redirects homomorphisms of bicategories]]
