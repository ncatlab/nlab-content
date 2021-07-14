

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context####
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition ##

\begin{proposition}\label{SliceModelStructure}
**(slice model structure)** \linebreak
For $\mathcal{C}$ a [[model category]] and $X \in \mathcal{C}$ any [[object]], 
the [[slice category]] $\mathcal{C}_{/X}$ 
as well as the [[coslice category]] $\mathcal{C}^{X/}$ 
inherit themselves structures of [[model categories]], whose 
[[fibrations]], [[cofibrations]] and [[weak equivalences]] are precisely the morphism 
whose images under the [[forgetful functors]] $\mathcal{C}_{/X} \to \mathcal{C}$ or $\mathcal{C}^{X/} \to \mathcal{C}$
are fibrations, cofibrations or weak equivalences, respectively, in $\mathcal{C}$.
\end{proposition}

([Hirschhorn 2002, Thm. 7,6,5](#Hirschhorn02), [May & Ponto 2012, Th. 15.3.6](#MayPonto12))

## Properties ##

### Cofibrant generation, properness, combinatoriality

+-- {: .num_prop #ModelStructureInheritsGoodProperties}
###### Proposition

If $\mathcal{C}$ is

* a [[cofibrantly generated model category]]

* or a [[proper model category]]

* or a [[cellular model category]]

then so are $\mathcal{C}_{/X}$ and $\mathcal{C}^{X/}$.

More in detail, if $I,J \subset Mor(\mathcal{C})$ are the classes of [[generating cofibrations]] and of generating acylic cofibrations of $\mathcal{C}$, respectively, then 

* the generating (acyclic) cofibrations of $\mathcal{C}^{X/}$ are the image under $X \sqcup(-)$ of those of $\mathcal{C}$.

=--

([Hirschhorn 05](#Hirschhorn05), [May & Ponto 2012, Th. 15.3.6](#MayPonto12)).

+-- {: .num_prop #ModelStructureInheritsCombinatorial}
###### Proposition

If $\mathcal{C}$ is a [[combinatorial model category]], then so is $\mathcal{C}_{/X}$.

=--

+-- {: .proof}
###### Proof

By [basic properties](locally+presentable+category#Properties) of [[locally presentable categories]] they are stable under slicing. Hence with $\mathcal{C}$ locally presentable also $\mathcal{C}_{/X}$ is, 
and by prop. \ref{ModelStructureInheritsGoodProperties} with $\mathcal{C}$ cofibrantly generated also $\mathcal{C}_{/X}$ is. 

=--

+-- {: .num_prop #ModelStructureInheritsEnriched}
###### Proposition

If $\mathcal{C}$ is an [[cartesian enriched model category]], then so is $\mathcal{C}_{/X}$.

=--

+-- {: .proof}
###### Proof

By basic properties of [[cartesian enriched categories]] they are stable under slicing, where tensoring is computed in $\mathcal{C}$.
Hence with $\mathcal{C}$ enriched also $\mathcal{C}_{/X}$ is.
The [[pushout product axiom]] now follows from the fact
that in overcategories pushouts can be computed in the underlying category $\mathcal{C}$.
The [[unit axiom]] follows from the unit axiom of $\mathcal{C}$
using the fact that tensorings are computed in $\mathcal{C}$.

=--

### As presentations for over (∞,1)-categories

When restricted to [[fibrant objects]], the operation of forming the model structure on an overcategory presents the operation of forming the [[over (∞,1)-category]] of an [[(∞,1)-category]].

More explicitly, for any [[model category]] $\mathcal{C}$, let 

\[
  \label{LocalizationFunctor}
  \gamma \colon \mathcal{C} \longrightarrow L_W \mathcal{C}
\]

denote the localization of an (infinity,1)-category|localization]] (as an [[(∞,1)-category]]) inverting the [[weak equivalences]] (as e.g. given by [[simplicial localization]]; see also the [[model structure on relative categories]]). Then:

+-- {: .num_prop #PresentationOfSliceInfinityCatAlt}
###### Proposition

If $\mathcal{C}$ is a [[model category]] and $X \in \mathcal{C}$ is [[fibrant object|fibrant]], then $\gamma$ (eq:LocalizationFunctor) induces an  [[(∞,1)-functor]] $\mathcal{C}/X \to L_W(\mathcal{C})/\gamma(X)$, which in turn induces an [[equivalence of (∞,1)-categories]]

$$
  L_W(\mathcal{C}/X) 
    \overset{\simeq}{\longrightarrow}
  L_W(\mathcal{C})/\gamma(X)
  \,.
$$

=--

This main result is corollary 7.6.13 of [Cisinski 20](#Cisinski20). Model categories are (∞,1)-categories with weak equivalences and fibrations as defined in [Cisinski Def. 7.4.12](#Cisinski20).

We spell out a proof for the special case that $\mathcal{C}$ carries the [[extra structure]] of a [[simplicial model category]] (this proof was written [in 2011](https://ncatlab.org/nlab/revision/model+structure+on+an+over+category/7) when no comparable statement seemed to be available in the literature):

+-- {: .num_prop #PresentationOfSliceInfinityCat}
###### Proposition

If $\mathcal{C}$ is a [[simplicial model category]] and $X \in \mathcal{C}$ is [[fibrant object|fibrant]], then the [[overcategory]] $\mathcal{C}/X$ with the above slice model structure is a [[presentable (infinity,1)-category|presentation]] of the 
[[over-(∞,1)-category]] $L_W \mathcal{C} / \gamma(X)$: 
we have an [[equivalence of (∞,1)-categories]]

$$
  L_W(\mathcal{C}/X) \simeq  (L_W\mathcal{C}) / \gamma(X)
  \,.
$$

=--


+-- {: .proof}
###### Proof

We write equivalently $(-)^\circ \coloneqq L_W(-)$.

It is clear that we have an [[essentially surjective (∞,1)-functor]] $\mathcal{C}^\circ/X \to (\mathcal{C}/X)^\circ$. What has to be shown is that this is a [[full and faithful (∞,1)-functor]] in that it is an [[equivalence in an (∞,1)-category|equivalence]] on all [[hom-object|hom]]-[[∞-groupoid]]s $\mathcal{C}^\circ/X(a,b) \simeq (\mathcal{C}/X)^\circ(a,b)$.

To see this, notice that the hom-space in an [[over-(∞,1)-category]] $\mathcal{C}^\circ/X$ between objects $a \colon A \to X$ and $b \colon B \to X$ is given (as discussed there) by the  [[(∞,1)-pullback]]

$$
  \array{
    \mathcal{C}^\circ/X(A \stackrel{a}{\to} X, B \stackrel{b}{\to} X) 
     &\to& \mathcal{C}^\circ(A,B)
    \\
    \big\downarrow 
      && 
    \big\downarrow^{\mathrlap{b_*}}
    \\
    {*} &\stackrel{a}{\to}& \mathcal{C}^\circ(A,X)
  }
$$

in [[∞Grpd]].

Let $A \in C$ be a cofibrant representative and $b \colon B \to X$ be a 
fibration representative in $C$ (which always exists) of the objects of these names in $C^\circ$, respectively. In terms of these we have a cofibration

$$
  \array{
    \emptyset &&\hookrightarrow&& A
    \\
    & \searrow && \swarrow_{\mathrlap{a}}
    \\ 
    && X
  }
$$

in $\mathcal{C}/X$, exhibiting $a$ as a cofibrant object of $\mathcal{C}/X$;  and a fibration

$$
  \array{
    B &&\stackrel{b}{\to}&& X
    \\
    & {}_{\mathllap{b}}\searrow && \swarrow_{\mathrlap{Id}}
    \\ 
    && X
  }
$$

in $\mathcal{C}/X$, exhibiting $b$ as a fibrant object in $\mathcal{C}/X$.
 
Moreover, the diagram in [[sSet]] given by

$$
  \array{
    \mathcal{C}/X(a, b) &\longrightarrow& \mathcal{C}(A,B)
    \\
    \big\downarrow && \big\downarrow^{\mathrlap{b_*}}
    \\
    {*} &\stackrel{a}{\to}& \mathcal{C}(A,X)
  }
$$

is 

1. a [[pullback]] diagram in [[sSet]] (by the definition of morphism in an ordinary [[overcategory]]);

1. a [[homotopy pullback]] in the [[model structure on simplicial sets]], because  by the [[pullback power axiom]] on the [[sSet]]${}_{Quillen}$ [[enriched model category]] $C$ and the above (co)fibrancy assumptions, all objects are [[Kan complexes]] and the right vertical morphism is a [[Kan fibration]];

1. has in the top left the correct [[derived hom-space]] in $C/X$ (since $a$ is cofibrant and $b$ fibrant).

This means that this correct hom-space $\mathcal{C}/X(a,b) \simeq (\mathcal{C}/X)^\circ(a,b) \in sSet$ is indeed a model for $\mathcal{C}^\circ/X(a,b) \in \infty Grpd$.

=--


### Quillen adjunctions


\begin{proposition}\label{AdjunctionSliceCat}
**(slice Quillen adjunctions)** \linebreak

Consider a [[Quillen adjunction]]
$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\;\;\;\;\bot_{\mathrlap{Qu}}\;\;\;\;}
  \mathcal{C}
  \,,
$$

Then the following [sliced adjunctions](over+category#OnSlices) are [[Quillen adjunctions]] between the corresponding slice model categories (Prop. \ref{SliceModelStructure}):


1. For $d \in \mathcal{D}$ any object, the [sliced adjunction](over+category#OnSlices)

   \[
     \label{QuillenAdjunctionSlicedOverD}
     \mathcal{D}_{/d}
       \underoverset
         {\underset{R_{/d}}{\longrightarrow}}
         {\overset{L_{/d}}{\longleftarrow}}
         {\;\;\;\;\bot_{\mathrlap{Qu}}\;\;\;\;}
     \mathcal{C}_{/R(d)}
     \,,
     \;\;\;\;
     \text{with}
     \;\;
     L_{/d} 
       \;\colon\; 
     \mathcal{C}_{/R(d)} 
       \xrightarrow{\;L\;} 
     \mathcal{D}_{/L\circ R(d)} 
       \xrightarrow{\;(\eta_d)^\ast\;} 
     \mathcal{D}_{/d}
     \,,
   \]
   is a [[Quillen adjunction]].

   

1. If $X \in \mathcal{C}$, then
   $$
     L \colon \mathcal{C}_{/X} \leftrightarrows \mathcal{D}_{/L(X)} \colon R
   $$
   is an adjunction,
   where in the composition 
   $R \colon \mathcal{D}_{/L X} \to \mathcal{C}_{/R L X} \to A_{/X}$, 
   the second functor is the [[base change]] functor 
   along the [[adjunction unit]] $X \to R \circ L(X)$.


\end{proposition}

(e.g. [Li 2016, Prop. 2.5 (2)](#Li16))

\begin{proof}

From Prop. \ref{SliceModelStructure} it is immediate that:

* in the case (eq:QuillenAdjunctionSlicedOverD) the [[right adjoint]] $R_{/d}$ is a [[right Quillen functor]], since on [[underlying]] morphisms it is just $R$, which is a right Quillen functor by assumption

* in the case...

> am being interrupted...

\end{proof}

## Examples

* the [[classical model structure on pointed topological spaces]] is the model structure on the undercategory under the point of the [[classical model structure on topological spaces]].

## Related concepts


* [[over-category]] 

  * [[slice category]] 

  * [[under category]] 

  * [[over topos]]


* [[over (∞,1)-category]],

  * **model structure on an over-category**

  * [[over-(∞,1)-topos]]

* [[opposite model structure]]



## References 

* {#Hirschhorn02} [[Philip Hirschhorn]], Theorem 7.6.5 of: _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

* {#Hirschhorn05} [[Philip Hirschhorn]], _Overcategories and undercategories of model categories_, 2005 ([pdf](http://www-math.mit.edu/~psh/undercat.pdf), [arXiv:1507.01624](https://arxiv.org/abs/1507.01624))

* {#MayPonto12} [[Peter May]], [[Kate Ponto]], Thm. 15.3.6 in: _[[More concise algebraic topology]]_,   University of Chicago Press (2012) ([ISBN:9780226511795](https://press.uchicago.edu/ucp/books/book/chicago/M/bo12322308.html), [pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf))

* {#Li16} Zhi-Wei Li, *A note on the model (co-)slice categories*, Chinese Annals of Mathematics, Series B volume 37, pages 95–102 (2016) ([arXiv:1402.2033](https://arxiv.org/abs/1402.2033), [doi:10.1007/s11401-015-0955-z](https://doi.org/10.1007/s11401-015-0955-z))


* {#Cisinski20} [[Denis-Charles Cisinski]], _Higher category theory and homotopical algebra_, 2020 ([pdf](http://www.mathematik.uni-regensburg.de/cisinski/CatLR.pdf))

[[!redirects slice model structures]]

[[!redirects model structure on an over category]]
[[!redirects model structure on an overcategory]]
[[!redirects model structure on an under category]]
[[!redirects model structure on an undercategory]]

[[!redirects model structure on a slice category]]
[[!redirects model structure on a coslice category]]

[[!redirects model structures on a slice category]]
[[!redirects model structures on a coslice category]]

[[!redirects slice model category]]
[[!redirects slice model categories]]

[[!redirects coslice model category]]
[[!redirects coslice model categories]]

[[!redirects coslice model structure]]
[[!redirects coslice model structures]]

[[!redirects co-slice model category]]
[[!redirects co-slice model categories]]

[[!redirects co-slice model structure]]
[[!redirects co-slice model structures]]
