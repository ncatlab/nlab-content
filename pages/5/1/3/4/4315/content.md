
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A (smooth) principal bibundle is a (smooth) [[principal bundle]] and notably a [[groupoid principal bundle]] with compatible [[actions]] on both the left and right.

They arise in two related situations: as the objects used to define [[nonabelian bundle gerbe]]s and as [[anafunctor]]-like morphisms between [[Lie groupoid]]s. The former is a special case of the latter. The general concept of [[bundle]] has no action and so there is nothing to do to make it a bibundle.  However, suppose that $G$ is a [[group]] and you are interested in [[G-bundle]]s.  Then a __$G$-bibundle__ is a bundle that is simultaneously a left $G$-bundle and a right $G$-bundle, such that the left and right actions of $G$ commute. This is a bibundle in the first sense. 

A __principal bibundle__ is a [[principal bundle|principal]] $G$-bundle with commuting left and right $G$-actions.

More generally, a __right principal bibundle__ between two groupoids $G$ and $H$ is a set $P$ with a $G$-$H$ [[biaction]] such that the map from $P$ to the objects of $G$ is a surjective submersion and such that the fibers are acted on by $H$ freely and transitively. See [discussion](http://sbseminar.wordpress.com/2007/07/23/a-bicategory-of-groupoids/).

This subsumes the notion of principal  bibundle defined above. A principal $G$-bibundle is the same as __right principal bibundle__ from the Lie groupoid $X$ (thought of as a [[discrete groupoid]] with only identity morphisms) to the underlying groupoid of the [[automorphism 2-group]] $(Aut(G), G)$. See Example 14 of Chris Schommer-Pries _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ [arXiv:0911.2483](http://arxiv.org/abs/0911.2483/).  

Similarly, let $(H, G)$&#8230; be a [[strict 2-group]]. Then an __$(H, G)$&#8230;-bibundle__ is a (right) principal $G$-bundle with an equivariant map $\phi: P \to H$. See [Murray's talk](http://www.mpim-bonn.mpg.de/digitalAssets/7050_Murray.pdf).

For a [[Lie groupoid]] $G$, a left (right) $G$-bundle $E$ over $X$ (equipped with  $\tau: X \to M$) is a left (right) $G$-action on $E$, and a $G$-invariant map
$\pi: E  \to M$. Then a __$G$-$H$-bibundle__ $E$ is a left $G$-bundle and a right $H$-bundle. See [Morton's talk](http://www.math.uwo.ca/~jmorton9/seminar/gpdrep.pdf).


The description of principal bibundles as maps to a [[2-group]] shows that there is an induced structure of a 2-group on the category of principal bibundles over a space. In fact this holds whenever the muliplication of the target $2$-group is given by a _bibundle_, and this allows the concept of a non-abelian [[bundle gerbe]] to be generalized past the classical setting of strict [[Lie 2-group]]s $(H,G)$. A general discussion occurs in Chris Schommer-Pries' [Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group](http://arxiv.org/abs/0911.2483/) in section 3.3,  see especially Example 61. 


Now let $G$ and $H$ be Lie groupoids. A [[manifold]] $M$ with a left $G$-action and a right $H$-action which commute, i.e., $(g \cdot m) \cdot h = g \cdot (m \cdot h)$, whenever defined, is called a __smooth $G$-$H$ bibundle__. See Definition 2.8 in _[Stacky Lie Groupoids](http://arxiv.org/abs/math/0702399)_.

## Properties

### Lie groupoid bibundles and Morita/stack morphisms

We discuss how Lie groupoid bibundles correspond to [[Morita morphism]] (morphisms of [[differentiable stacks]]/[[smooth stacks]]) between the Lie groupoids.

First we set up the relevant definitions and establish our notation in 

* [Lie groupoids and smooth stacks](#LieGroupoidsAndSmoothStacks)

Then we discuss smooth groupoid-principal bundles and how a Lie groupoid [[moduli stack]] for the bundles principal over it in 

* [Smooth groupoid-principal bundles](#SmoothGrooupoidPrincipalBundles).

Finally we consider the corresponding smooth bibundles and how they correspond to their modulating stack morphisms in

* [Smooth groupoid-principal bibundles](#SmoothGroupoidPrincipalBibundles)


#### Lie groupoids and smooth stacks
 {#LieGroupoidsAndSmoothStacks}


A _[[smooth stack]]_ or _[[smooth groupoid]]_ is a [[stack]] on the site [[SmoothMfd]] of [[smooth manifolds]] or equivalently (and often more conveniently) on its [[dense subsite]] [[CartSp]] of just [[Cartesian spaces]] $\mathbb{R}^n, n \in \mathbb{N}$ and [[smooth functions]] between them, equipped with the standard [[coverage]] of [[good open covers]].

We write 

$\;\;\; $[[SmoothGrpd]] $\coloneqq Sh_{(2,1)}(CartSp) \simeq L_{lhe} Func(CartSp^{op}, Grpd) $ 

for the [[(2,1)-category]] of [[stacks]] on this site, equivalently the result of taking [[groupoid]]-valued [[presheaves]] and then  [[simplicial localization|universally]] turning local (as seen by the [[coverage]]) [[equivalences of groupoids]] into global [[equivalence in an (infinity,1)-category]].

By generalizing here [[groupoids]] to general [[Kan complexes]] and [[equivalences of groupoids]] to [[homotopy equivalences]] of Kan complexes, one obtains _smooth [[∞-stacks]]_ or _[[smooth ∞-groupoids]]_, which we write 

$\;\;\;$ [[Smooth∞Grpd]] $\coloneqq Sh_{(\infty,1)}(CartSp) \simeq L_{lhe} Func(CartSp^{op}, KanCplx) $. 

We often write $\mathbf{H} \coloneqq$ [[Smooth∞Grpd]] for short.

By the [[(∞,1)-Yoneda lemma]] there is a sequence of [[full and faithful (∞,1)-functor|faithful inclusions]]

$\;\;\;$ [[SmoothMfd]] $\hookrightarrow$ [[SmoothGrpd]] $\hookrightarrow$ [[Smooth∞Grpd]].

This induces a corresponding inclusion of [[simplicial objects]] and hence of [[groupoid objects in an (∞,1)-category|groupoid objects]]

$$
  LieGrpd \hookrightarrow Grpd_\infty(SmoothMfd)  \hookrightarrow  Grpd_\infty(Smooth\infty Grpd)
  \,.
$$

For $\mathcal{G}_\bullet \in Grpd_\infty(\mathbf{H})$ a groupoid object we write 

$$
  \mathcal{G}_0 \to \mathcal{G} \coloneqq \underset{\longrightarrow}{\lim}_{n} \mathcal{G}_n
$$

for its [[(∞,1)-colimit|(∞,1)-colimiting]] [[cocone]], hence $\mathcal{G} \in \mathbf{H}$ (without subscript decoration) denotes the [[realization]] of $\mathcal{G}_\bullet$ as a single object in $\mathbf{H}$.

+-- {: .num_defn }
###### Definition

For $\mathcal{G}_\bullet \in Grpd_\infty(\mathbf{H})$ a [[groupoid object in an (infinity,1)-category|groupoid object]], we write $\mathcal{G} \coloneqq {\lim}_{n} \mathcal{G}_n \in \mathbf{H}$ for its **[[realization]]** and call the canonical [[1-epimorphism]]

$$
  \mathcal{G}_0 \to \mathcal{G}
$$

the canonical **[[atlas]]** of this realization.

=--

+-- {: .num_example }
###### Example

For $\mathcal{G}_\bullet \in Grpd(SmoothMfd) \hookrightarrow Grpd_\infty(Smooth\infty Grpd)$ a [[Lie groupoid]], we have that

1. $\mathcal{G}_0 \in SMoothMfd \hookrightarrow Smooth\infty Gprd$ is its [[smooth manifold]] of [[objects]] 

1. $\mathcal{G} \in $ [[SmoothGrpd]] $\hookrightarrow$ [[Smooth∞Grpd]] is the realization of the Lie groupoid as a [[differentiable stack]], hence as a [[smooth groupoid]]

1. $\mathcal{G}_0 \to \mathcal{G}$ is the canonically induced [[atlas]] in the traditional sense of [[geometric stack]]-theory.

=--

+-- {: .num_remark }
###### Remark

By the [[Giraud-Rezk-Lurie axioms]] of the [[(∞,1)-topos]] $\mathbf{H}$ this morphism $\mathcal{G}_0 \to \mathcal{G}$ is a [[1-epimorphism]] and its construction establishes is an [[equivalence of (∞,1)-categories]] $Grpd_\infty(\mathbf{H}) \simeq \mathbf{H}^{\Delta^1}_{1epi}$, hence morphisms $\mathcal{G}_\bullet \to \mathcal{K}_\bullet$ in $Grpd_\infty(\mathbf{H})$ are equivalently [[diagrams]] in $\mathbf{H}$ of the form

$$
  \array{
    \mathcal{G}_0 &\to& \mathcal{K}_0
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathcal{G} &\to& \mathcal{K}
  }
  \,.
$$

=--

This is evidently more constrained than just morphisms 

$$
  \mathcal{G} \to \mathcal{K}$ in $\mathbf{H}
$$

by themselves. The latter are the _generalized morphisms_ or _[[Morita morphisms]]_ between the groupoid objects $\mathcal{G}_\bullet$, $\mathcal{K}_\bullet$. 

+-- {: .num_defn #MoritaMorphism}
###### Definition

Given [[groupoid objects in an (∞,1)-category|groupoid objects]] $\mathcal{G}_\bullet, \mathcal{K}_\bullet \in Grpd_\infty(\mathbf{H})$, a **[[Morita morphism]]** between them is a morphism $\mathcal{G} \to \mathcal{K}$ in $\mathbf{H}$ between their [[realizations]]. A Morita morphism that is an [[equivalence in an (infinity,1)-category|equivalence]] in $\mathbf{H}$ is called a **[[Morita equivalence]]** of groupoid objects in $\mathbf{H}$.

=--


Here we want to express these Morita morphisms $\mathcal{G} \to \mathcal{K}$ in terms of bibundle objects $\mathcal{P} \in \mathbf{H}$ on which both $\mathcal{G}_\bullet$ and $\mathcal{K}_\bullet$ [[action|act]].


+-- {: .num_example}
###### Example

For $X \in \mathbf{H}$ any [[object]], its [[pair groupoid]] $Pair(X)_\bullet \in Grpd_\infty(\mathbf{H})$ is

$$
  Pair(X)_n \coloneqq X^{\times^{n+1}}
  \,.
$$

The [[realization]] of this is equivalent to the point

$$
  Pair(X) \coloneqq \underset{\longrightarrow}{\lim}_n Pair(X)_n
  \simeq *
  \,.
$$

Hence all [[Morita morphisms]], def. \ref{MoritaMorphism}, to the pair groupoid are equivalent. As a groupoid object $Pair(X)_\bullet$ is non-trivial, but it is [[Morita equivalence|Morita equivalent]] to the terminal groupoid object.

=--


#### Smooth groupoid-principal bundles
 {#SmoothGrooupoidPrincipalBundles}

+-- {: .num_defn #GroupoidAction}
###### Definition

For $\mathcal{G}_\bullet \in Grpd_\infty(\mathbf{H})$ a [[groupoid object in an (∞,1)-category|groupoid object]], $P \in \mathbf{H}$ any object equipped with a morphsim $a \colon P \to \mathcal{G}_0$ to the object of objects of $\mathcal{G}$, a **$\mathcal{G}_\bullet$-[[groupoid ∞-action]]** on $X$ with **anchor** $a$ is a [[groupoid object in an (∞,1)-category|groupoid]] $(X//\mathcal{G})_\bullet$ over $\mathcal{G}_\bullet$ of the form

$$
  \array{  
    \vdots && && \vdots
    \\
    \downarrow \downarrow \downarrow \downarrow
    && &&
    \downarrow \downarrow \downarrow \downarrow
    \\
    X \underset{\mathcal{G}_0}{\times} \mathcal{G}_2
    && \to && \mathcal{G}_2    
    \\
    \downarrow \downarrow \downarrow && &&   
    \downarrow \downarrow \downarrow
    \\
    X \underset{\mathcal{G}_0}{\times} \mathcal{G}_1
    && \to && \mathcal{G}_1
    \\
    \downarrow \downarrow && && \downarrow \downarrow
    \\
    X  && \stackrel{a}{\to} && \mathcal{G}_0
  }
  \,,
$$

where the [[homotopy fiber products]] on the left are those of the anchor $a$ with the leftmost 0-face map $\mathcal{G}_{(\{0\} \hookrightarrow \{0, \cdots, n\})}$ and  the horizontal morphisms are the corresponding [[projections]] on the second factor.

We call $(X//\mathcal{G})_\bullet$ also the **[[action groupoid]]** of the action of $\mathcal{G}_\bullet$ on $(X,a)$ and call its [[realization]] $X \to (X//\mathcal{G})$ the [[homotopy quotient]] of the action.

=--

+-- {: .num_example }
###### Example

For $\mathcal{G}_\bullet = (\mathbf{B}G)_\bullet$ the [[delooping]] of a [[group object in an (∞,1)-category|group object]], def. \ref{GroupoidAction} reduces to the definition of an [[∞-action]] of the [[∞-group]] $G$.

=--

Under this relation, the discussion of [[∞-groupoid-principal ∞-bundles]] proceeds in direct analogy with that of $G$-[[principal ∞-bundles]]:

+-- {: .num_prop }
###### Proposition

For $X \in $ [[Smooth∞Grpd]] any object, a morphism $f \colon X \to \mathcal{G}$ in $\mathbf{}H$ induces ("modulates") a $\mathcal{G}_\bullet$-[[groupoid action]], def. \ref{GroupoidAction}, on the [[homotopy pullback]] $f^\ast \mathcal{G}_0$ 

$$
  \array{
    f^* \mathcal{G}_0 &\to& \mathcal{G}_0
    \\
    \downarrow &pb_\infty& \downarrow
    \\
    X &\stackrel{f}{\to}& \mathcal{G}
    \,.
  }
$$

of the [[atlas]] of $\mathcal{G}$: the corresponding [[action groupoid]] is the [[Cech nerve]] of the [[projection]] $p \colon f^*\mathcal{G}_0 \to X$ (which as the [[(∞,1)-pullback]] of a [[1-epimorphism]] is itself a [[1-epimorphism]]):

$$
  \array{
     && \vdots && \vdots 
     \\
     && \downarrow \downarrow \downarrow &&
     \downarrow \downarrow \downarrow
     \\
    && (f^\ast \mathcal{G}_0) \underset{\mathcal{G}_0}{\times} \mathcal{G}_1
    &\to&
    \mathcal{G}_1
    \\
    && \downarrow \downarrow && \downarrow \downarrow
    \\
    && f^* \mathcal{G}_0 &\stackrel{a}{\to}& \mathcal{G}_0
    \\
    && \downarrow &pb_\infty& \downarrow
    \\
    (f^\ast \mathcal{G}_0)//\mathcal{G} &\simeq& X &\stackrel{f}{\to}& \mathcal{G} &\simeq& \underset{\longrightarrow}{\lim}_n \mathcal{G}_n
    \,.
  }
$$

=--

+-- {: .num_example #LieGroupoidPrincipalBundle}
###### Example

Let $f_\bullet \colon X_\bullet \to \mathcal{G}_\bullet$ be a morphism of 1-groupoid objects, say of [[Lie groupoids]]. Then as discussed at _[[homotopy pullback]]_ the [[(∞,1)-pullback]] of the [[atlas]] $\mathcal{G}_0 \to \mathcal{G}$ along the [[realization]] $f$ is computed as the 1-categorical [[pullback]]

$$
  \array{
   &\to& (\mathcal{G}_0 \underset{\mathcal{G}}{\times} \mathcal{G}^{\Delta^1})_\bullet
   \\
   \downarrow &pb& \downarrow
   \\
   \mathcal{X}_\bullet &\to& \mathcal{G}_\bullet
  }
$$

in $Sh(CartSp)^{\Delta^{op}}$. Schematically the groupoid on the right has morphisms $ \gamma_0 \to \gamma_1$ which are [[commuting diagrams]] in $\mathcal{G}$ of the form 
$$
  \array{
    && g
    \\
    & {}^{\mathllap{\gamma_0}}\swarrow && \searrow^{\mathrlap{\gamma_1}}
    \\
    g_0 && \to && g_1
  }
  \,.
$$

Therefore the pullback is the sheaf of groupoids which is schematically of the form

$$
  f^\ast \mathcal{G}_0
  \;\simeq\;
  \left\{
    \array{
      && g
      \\
      & {}^{\mathllap{\gamma_0}}\swarrow &&   \searrow^{\mathrlap{\gamma_1}} & && \in \mathcal{G}
      \\
      f(x_0) && \stackrel{f(\xi)}{\to} && f(x_1)
      \\
      x_0 && \stackrel{\xi}{\to}&& x_1 && \in \mathcal{X} 
    }
  \right\}
  \,.
$$

In this presentation now 

$$
  \mathcal{G}_1
  \;\simeq\;
  \left\{
    \array{
      && g_0
      \\
      && \downarrow^{\gamma}
      \\
      && g_1
      \\
      & {}^{\mathllap{\gamma_0}}\swarrow && \searrow^{\mathrlap{\gamma_1}}
      \\
      g_{1 0} && \to && g_{11}
    }
  \right\}
  \,.
$$

and the target map $\mathcal{G}_1 \to \mathcal{G}_0$ is given by forgetting the top vertical morphism in this diagram, while the source map is given by composing (!) the top vertical morphism with the two diagonal morphism.

Pullback of these two maps induces the left and right vertical map in

$$
  \array{
    f^\ast \mathcal{G}_0 \underset{\mathcal{G}_0}{\times}
    \mathcal{G}_1
    &\to& \mathcal{G}_1
    \\
    \downarrow\downarrow && \downarrow \downarrow
    \\
    f^\ast \mathcal{G}_0 &\stackrel{a}{\to}& \mathcal{G}_0
  }
  \,.
$$

from 

$$
  f^\ast \mathcal{G}_0 \underset{\mathcal{G}_0}{\times} \mathcal{G}_1
  \;\simeq\;
  \left\{
    \array{
      && g_0
      \\
      && \downarrow^{\gamma}
      \\
      && g_1 && && \in \mathcal{G}
      \\
      & {}^{\mathllap{\gamma_0}}\swarrow && \searrow^{\mathrlap{\gamma_1}} &
      \\
      f(x_0) && \stackrel{f(\xi)}{\to} && f(x_1)
      \\
      x_0 && \stackrel{\xi}{\to} && x_1 & & \in \mathcal{X}
    }
  \right\}
  \,.
$$

The left one just forgets the top vertical morphism, the right one composes it with the diagonal morphisms. This composion is the $\mathcal{G}_\bullet$-action on $f^\ast \mathcal{G}_0$.

=--


#### Smooth groupoid-principal bibundles
 {#SmoothGroupoidPrincipalBibundles}

Finally then for $\mathcal{X}_\bullet$ and $\mathcal{G}_\bullet$ two Lie groupoids and $f \;\colon\; \mathcal{X} \to \mathcal{G}$ a morphism in [[Smooth∞Grpd]] between the corresponding [[differentiable stacks]], we obtain first the $\mathcal{G}$-[[groupoid principal bundle]] $f^* \mathcal{G}_0 \stackrel{p}{\to} \mathcal{X}$ and then by further homotopy pullback also the left $\mathcal{X}$-[[groupoid principal bundle]] $p^* \mathcal{X}_0$:

+-- {: .num_defn }
###### Definition

For $\mathcal{X}_\bullet, \mathcal{G}_\bullet \in Grpd_\infty(\mathbf{H})$ two [[groupoid object in an (infinity,1)-category|groupoid objects]] and $f \colon \mathcal{X} \to \mathcal{G}$ a [[Morita morphism]] between them, def. \ref{MoritaMorphism}, we say that the corresponding **$\mathcal{X}_\bullet-\mathcal{G}_\bullet$-bibundle** $\mathcal{P}(f)$ is the $\mathcal{G}_\bullet$-[[groupoid-principal bundle]] $f^\ast \mathcal{G}_0$ pulled back to canonical [[atlas]] of $\mathcal{X}$ and equipped with the induced $\mathcal{X}_\bullet$-[[groupoid action]]:


$$
  \array{
    \mathcal{P}(f)& \coloneqq& p^* \mathcal{X}_0 &\to&
    f^* \mathcal{G}_0&\to& \mathcal{G}_0
    \\
    && \downarrow &\pb\infty& \downarrow^{\mathrlap{p}} &pb_\infty& \downarrow
    \\
    && \mathcal{X}_0
    &\to&
    \mathcal{X}
    &\stackrel{f}{\to}&
    \mathcal{G}
  }
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

Here $p^* \mathcal{X}_0$ still has a right $\mathcal{G}_\bullet$-action, albeit no longer a principal one.  Hence it is an $\mathcal{X}_\bullet$-$\mathcal{G}_\bullet$-groupoid bibundle, principal for the left action.

=--

+-- {: .num_remark }
###### Remark

If both [[atlases]] are [[0-truncated]] objects ([[smooth spaces]]) $\mathcal{X}_0, \mathcal{G}_0 \in Sh(CartSp) \simeq \tau_1 \mathbf{H} \hookrightarrow \mathbf{H}$, then by the [[pasting law]] for [[homotopy pullbacks]] we have that $\mathcal{P}(f)$ is [[n-truncated|(n-1)-truncated]] if $\mathcal{G}$ is [[n-truncated]].

In particular therefore the total space of a [[smooth groupoid|smooth 1-groupoid]] bibundle is 0-truncated hence is a [[smooth space]]. 

=--


+-- {: .num_example }
###### Example

In order to discuss Lie-groupoid bibundles we continue the discussion in  example \ref{LieGroupoidPrincipalBundle} of Lie-groupoid principal bundles. Proceeding for the second homotopy pullback diagram as discussed there for the first one, one finds that the total space $\mathcal{P}$ of the bibundle is presented by the sheaf of groupoids whose schematic depiction is

$$
  f^\ast \mathcal{G}_0
  \;\simeq\;
  \left\{
    \array{
      && g
      \\
      & {}^{\mathllap{\gamma_0}}\swarrow &&   \searrow^{\mathrlap{\gamma_1}} & && \in \mathcal{G}
      \\
      f(x_0) && \stackrel{f(\xi)}{\to} && f(x_1)
      \\
      x_0 && \stackrel{\xi}{\to}&& x_1 
      \\
      & \searrow && \swarrow &  && \in \mathcal{X}
      \\
      && x
    }
  \right\}
  \,.
$$

The right $\mathcal{G}_\bullet$-action is by precomposition of these diagram with morphisms in $\mathcal{G}$, while the left $\mathcal{X}$-action is by postcomposition with morphisms in $\mathcal{X}$.


=--

Conversely, given a $\mathcal{X}_\bullet$-$\mathcal{G}_\bullet$-Lie groupoid bibundle which is principal on the left

$$
  \array{
    \mathcal{P} &\to& \mathcal{B} &\to& \mathcal{G}_0
    \\
    \downarrow && && \downarrow
    \\
    \mathcal{X}_0 &\to& \mathcal{X} && \mathcal{G}
  }
$$

we recover the Morita morphism $f$ that it coresponds to by the [[Giraud-Rezk-Lurie axioms]]: first $p$ is the induced map between the [[homotopy colimits]] of the Cech nerves of the two left horizontal maps

$$
  \array{
    \mathcal{P} &\to& \mathcal{B} &\to& \mathcal{G}_0
    \\
    \downarrow && \downarrow^{\mathrlap{p}} && \downarrow
    \\
    \mathcal{X}_0 &\to& \mathcal{X} && \mathcal{G}
  }
$$

and then $f$ is similarly the map between the homotopy colimits of the Cech nerves of the two right vertical maps.


(...)

### Relation to groupoid convolution bimodules

The [[2-functor]] from [[Lie groupoids]] to [[C-star-algebras]] and [[Hilbert C-star-bimodules]] between them given by forming [[groupoid convolution algebras]] is naturally exhibited by Lie groupoid bibundles: the [[groupoid convolution algebra]] of the totoal space of hte bibindle becomes a [[bimodule]] over the two other groupoid convolution algebras.

(...)


## References

* [[Chris Schommer-Pries]] _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ [arXiv:0911.2483](http://arxiv.org/abs/0911.2483/) 

* [[Michael Murray]], _Bispaces and bibundles_ ([pdf slides](http://www.mpim-bonn.mpg.de/digitalAssets/7050_Murray.pdf))

* [[Michael Murray]], [[David Roberts]], [[Danny Stevenson]], _On the existence of bibundles_ LMS (2012)([arXiv:1102.4388](http://arxiv.org/abs/1102.4388))

[[!redirects bibundle]]
[[!redirects bibundles]]

[[!redirects groupoid bibundle]]
[[!redirects groupoid bibundles]]

[[!redirects ∞-groupoid bibundle]]
[[!redirects ∞-groupoid bibundles]]
[[!redirects infinity-groupoid bibundle]]
[[!redirects infinity-groupoid bibundles]]
