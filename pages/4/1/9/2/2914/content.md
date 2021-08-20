

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

([Hirschhorn 2002, Thm. 7.6.5](#Hirschhorn02), [May & Ponto 2012, Th. 15.3.6](#MayPonto12))

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
 {#PropertiesQuillenAdjunctions}

#### Base change Quillen adjunction
 {#BaseChangeQuillenAdjunction}

\begin{proposition}\label{LeftBaseChangeQuillenAdjunction}
**(left base change Quillen adjunction)** \linebreak
  For $\mathcal{C}$ a [[model category]] and $c_1 \xrightarrow{f} c_2$ any [[morphism]] in $\mathcal{C}$, the left [[base change]] adjunction $(f_1 \dashv f^\ast)$ along $f$ (where $f_!$ is [[postcomposition]] with and $f^\ast$ is [[pullback]] along $f$) is a [[Quillen adjunction]]:
  $$
    \mathcal{C}_{/c_1}
      \underoverset
        {\underset{f^\ast}{\longleftarrow}}
        {\overset{f_!}{\longrightarrow}}
        {\;\;\;\;\bot_{\mathrlap{Qu}}\;\;\;\;}    
    \mathcal{C}_{/c_2}
    \,.
  $$
\end{proposition}
\begin{proof}
  Since the [[left adjoint]] $f_1$ is the [[postcomposition]] operation, it manifestly preserves the classes of [[underlying]] morphisms, hence in particular preserves the classes of (acyclic) cofibrations in the slice model structure (by Prop. \ref{SliceModelStructure}), hence is a [[left Quillen functor]].
\end{proof}

If this adjunction is a [[Quillen equivalence]], then $f$ must be a [[weak equivalence]].  In general, the converse can be proven only if $c_1$ and $c_2$ are [[fibrant objects|fibrant]].

\begin{proposition}\label{RightPropernessAndLeftQuillenBaseChange}
The following are equivalent:

1. $\mathcal{C}$ is a [[right proper model category]].

1. If $f \colon c_1 \to c_2$ is any [[weak equivalence]] in $\mathcal{C}$, then the left base change Quillen adjunction $(f_! \dashv f^\ast)$ (from Prop. \ref{LeftBaseChangeQuillenAdjunction}) is a [[Quillen equivalence]].

\end{proposition}

This is due to [Rezk 02, Prop. 2.5](#Rezk02).



#### Sliced Quillen adjunctions

\begin{proposition}\label{SlicedQuillenAdjunction}
**(slice Quillen adjunctions)** \linebreak
Given a [[Quillen adjunction]]
$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\;\;\;\;\bot_{\mathrlap{Qu}}\;\;\;\;}
  \mathcal{C}
  \,,
$$

then:

1. for any [[object]] $b \in \mathcal{C}$ the [sliced adjunction](over+category#OnSlices) over $b$ is a  [[Quillen adjunction]] between the corresponding slice model categories (Prop. \ref{SliceModelStructure}):

   \[
     \label{SlicedQuillenAdjointFunctorsOverLb}
     \mathcal{D}_{/L(c)}
     \underoverset
       {\underset{\;\;\;\;R_{/b}\;\;\;\;}{\longrightarrow}}
       {\overset{\;\;\;\;L_{/b}\;\;\;\;}{\longleftarrow}}
       {\bot_{\mathrlap{Qu}}}
     \mathcal{C}_{/b}
     \mathrlap{\,,}
   \]

1. for any [[object]] $b \in \mathcal{D}$ the [sliced adjunction](over+category#OnSlices) over $b$ is a  [[Quillen adjunction]] between the corresponding slice model categories (Prop. \ref{SliceModelStructure}):

   \[
     \label{SlicedQuillenAdjointFunctorsOverRb}
     \mathcal{D}_{/c}
     \underoverset
       {\underset{\;\;\;\;R_{/b}\;\;\;\;}{\longrightarrow}}
       {\overset{\;\;\;\;L_{/b}\;\;\;\;}{\longleftarrow}}
       {\bot_{\mathrlap{Qu}}}
     \mathcal{C}_{/R(b)}
     \mathrlap{\,,}
   \]

\end{proposition}

(e.g. [Li 2016, Prop. 2.5 (2)](#Li16))

\begin{proof}
Consider the first case:
By the nature of the [sliced adjunction](over+category#OnSlices), 
its [[left adjoint]] $L_{/b}$ acts as $L$ on [[underlying]] [[morphisms]]. 
But since $L$ is assumed to be a [[left Quillen functor]]
and since the (acyclic) cofibrations of the slice model structure are those of [[underlying]] morphisms (Prop. \ref{SliceModelStructure}), 
$L_{/b}$ preserves them and is hence itself a [[left Quillen functor]].

The second case is directly analogous: Here it is evident that $R_{/b}$ is a [[right Quillen functor]], since it acts via $R$ on [[underlying]] morphisms, and $R$ is right Quillen by assumption.
\end{proof}

\begin{proposition}\label{SlicedQuillenQuivalences}
**(sliced Quillen equivalences)** \linebreak
Consider a [[Quillen equivalence]]
$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\;\;\;\;\simeq_{\mathrlap{Qu}}\;\;\;\;}
  \mathcal{C}
  \,.
$$

Then:

1. for a [[cofibrant object]] $b \in \mathcal{C}$ such that $L(b)$ is a [[fibrant object]], the sliced Quillen adjunction (eq:SlicedQuillenAdjointFunctorsOverLb) from Prop. \ref{SlicedQuillenAdjunction} is itself a [[Quillen equivalence]]:

$$
  \mathcal{D}_{/L(b)}
  \underoverset
    {\underset{\;\;\;\;R_{/b}\;\;\;\;}{\longrightarrow}}
    {\overset{\;\;\;\;L_{/b}\;\;\;\;}{\longleftarrow}}
    {\simeq_{\mathrlap{Qu}}}
  \mathcal{C}_{/b}
$$

1. for a [[fibrant object]] $b \in \mathcal{D}$, the sliced Quillen adjunction (eq:SlicedQuillenAdjointFunctorsOverRb) from Prop. \ref{SlicedQuillenAdjunction} is itself a [[Quillen equivalence]]:

$$
  \mathcal{D}_{/b}
  \underoverset
    {\underset{\;\;\;\;R_{/b}\;\;\;\;}{\longrightarrow}}
    {\overset{\;\;\;\;L_{/b}\;\;\;\;}{\longleftarrow}}
    {\simeq_{\mathrlap{Qu}}}
  \mathcal{C}_{/R(b)}
$$

\end{proposition}
(e.g. [Li 16, Prop. 3.1](#Li16))
\begin{proof}
  It is sufficient to check that the [[derived adjunction unit]] and [[derived adjunction counit]] are [[weak equivalences]] (...)
\end{proof}

## Examples

\begin{example}
The [[classical model structure on pointed topological spaces]] is the model structure on the [[undercategory]] under the point (the [[category of pointed objects]]) of the [[classical model structure on topological spaces]].
\end{example}


\begin{prop}\label{InducedQuilleAdjunctionsOnModelCategoriesOfPointedObjects}
**(induced [[Quillen adjunction]] on [[model categories of pointed objects]])** \linebreak
Given a [[Quillen adjunction]] between [[model categories]]
$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}
  \,,
$$
there is induced a [[Quillen adjunction]] between the corresponding [[model categories of pointed objects]]
$$
  \mathcal{D}^{\ast\!/}
    \underoverset
      {\underset{R^{\ast\!/}}{\longrightarrow}}
      {\overset{L^{\ast\!/}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{\ast\!/}
  \,,
$$
where 

* the [[right adjoint]] acts directly as $R$ on the triangular [[commuting diagrams]] in $\mathcal{C}$ that define the morphisms in $\mathcal{C}^{\ast\!/}$;

* the [[left adjoint]] is the [[composition|composite]] of the corresponding direct application of $L$ followed by [[pushout]] along the [[adjunction counit]] $L(\ast) \simeq L \circ R(\ast) \xrightarrow{ \;\epsilon_\ast \; } \ast$ (using that $R(\ast) \simeq \ast$ since [[right adjoints preserve limits]] and hence [[terminal objects]]):

  $$
    L^{\ast\!/}
    \;\colon\;
    \mathcal{C}^{\ast\!/}
    \xrightarrow{ \;\; L  \;\; }
    \mathcal{D}^{L(\ast)\!/}
    \;\simeq\;
    \mathcal{D}^{L\circ R(\ast)\!/}
    \xrightarrow{ \;\; (-) \sqcup \epsilon_\ast \;\; }
    \mathcal{D}^{\ast\!/}
    \,.
  $$

\end{prop}
\begin{proof}
  It is fairly straightforward to check this directly (e.g. [Hovey 1999, Prop. 1.3.5](model+structure+on+pointed+objects#Hovey99)), but it is also a special case of Prop. \ref{SlicedQuillenAdjunction} --- to make this explicit, notice that passing to [[opposite categories]] with their [[opposite model structures]] turns the original Quillen adjunction into the [[opposite Quillen adjunction]]:

$$
  \mathcal{C}^{op}
    \underoverset
      {\underset{L^{op}}{\longrightarrow}}
      {\overset{R^{op}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{D}^{op}
  \,.
$$

Now the passage to [[pointed objects]] corresponds to [[slice category|slicing]] (instead of [[coslice category|co-slicing]]), since

\[
  \label{PointedObjectsIsOppositeOfCopointedObjectsInOpposite}
  \mathcal{C}^{\ast\!/}
  \;\;
  \simeq
  \big(
    \mathcal{C}^{op}_{/\ast}
  \big)^{op}
  \,,
  \;\;\;\;\;\;\;
  \text{similarly}
  \;\;\;
  \mathcal{D}^{\ast\!/}
  \;\;
  \simeq
  \big(
    \mathcal{D}^{op}_{/R(\ast)}
  \big)^{op}
  \,,
\]

whence item (1) in Prop. \ref{SlicedQuillenAdjunction} says that there is a Quillen adjunction of the form

$$
  \mathcal{C}^{op}_{/R(\ast)}
    \underoverset
      {\underset{L^{op}_{/\ast}}{\longrightarrow}}
      {\overset{R^{op}_{/\ast}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{D}^{op}_{/\ast}
  \,,
$$

hence with [[opposite Quillen adjunction]] of the required form

$$
  \mathcal{D}^{\ast\!/}  
  \simeq
  \big(\mathcal{D}^{op}_{/R(\ast)}\big)^{op}
    \underoverset
      {\underset{ 
        R^{\ast\!/} \,\coloneqq\, \big( R^{op}_{/\ast} \big)^{op}
      }{\longrightarrow}}
      {\overset{
        L^{\ast\!/} \,\coloneqq\, \big( L^{op}_{/\ast} \big)^{op}
      }{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \big(\mathcal{C}^{op}_{/\ast}\big)^{op}
  \simeq
  \mathcal{C}^{\ast\!/}
  \,,
$$


with $R^{op}$ acting directly as $R$ on underlying diagrams, and with $L^{op}$ acting as the composite of $L$ following by [[pullback]] -- in $\mathcal{C}^{op}$ -- along the [[adjunction unit]] of $(R^{op} \dashv L^{op})$. Since the component morphism of the [[adjunction unit|unit]] of the [[opposite adjunction]] $(R^{op} \dashv L^{op})$ is that of the adjunction unit of $(L \dashv R)$, and since [[pullback]] in an [[opposite category]] is [[pushout]] in the original category, this implies the claim. 
\end{proof}


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

See also:

* {#Rezk02} [[Charles Rezk]], _Every homotopy theory of simplicial algebras admits a proper model_, Topology and its Applications, Volume 119, Issue 1, 2002, Pages 65-94, (<a href="https://doi.org/10.1016/S0166-8641(01)00057-8">doi:10.1016/S0166-8641(01)00057-8</a>, [arXiv:math/0003065](http://arxiv.org/abs/math/0003065))


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


[[!redirects base change Quillen adjunction]]
[[!redirects base change Quillen adjunctions]]

[[!redirects left base change Quillen adjunction]]
[[!redirects left base change Quillen adjunctions]]

[[!redirects right base change Quillen adjunction]]
[[!redirects right base change Quillen adjunctions]]


[[!redirects base change Quillen equivalence]]
[[!redirects base change Quillen equivalences]]

[[!redirects left base change Quillen equivalence]]
[[!redirects left base change Quillen equivalences]]

[[!redirects right base change Quillen equivalence]]
[[!redirects right base change Quillen equivalences]]


