

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
* table of contents
{:toc}

## Idea
 {#Idea}

A _bibundle_ is a ([[groupoid-principal bundle|groupoid]]-)[[principal bundle]] which is equipped with a compatible second ([[groupoid action|groupoid]]-)[[action]] "from the other side".

In particular, Lie groupoid bibundles serve to exhibit "generalized morphisms"/[[Morita morphisms]] between [[Lie groupoids]]. This is in generalization of how the [[differentiable stack]]/[[smooth groupoid]] represented by a [[Lie groupoid]] is the [[moduli stack]] for [[groupoid-principal bundles]]. 

Therefore groupoid bibundles play a role in [[geometry]] analogous to the role played by [[bimodules]] in [[algebra]]. In this role they were originally introduced in ([Haefliger 84](#Haefliger), [Hilsum-Skandalis 87](#HilsumSkandalis), [Pradines 89](#Pradines89)) and accordingly they are also called _Hilsum-Skandalis maps_. Independently they were seen in [[topos theory]] ([Bunge 90](#Bunge), [Moerdijk 91](#Moerdijk91)).
Historically, a central motivation for their study has been that the [[groupoid convolution algebra]] construction sends smooth bibundles between [[Lie groupoids]] to ([[Hilbert bimodule|Hilbert-]])[[bimodules]] of the corresponding [[C-star-algebra|C-star]] [[convolution algebras]], such that [[Morita equivalence]] is respected ([Muhly-Renault-Williams 87](#MuhlyRenaultWilliams), [Landsman 00](#Landsman), [Mr&#269;un 05](#Mrcun)). This is of relevance notably for [[KK-theory]] of Lie groupoids ([Hilsum-Skandalis 87b](#HilsumSkandalis87b)).

Bibundles also appear as _transition bundles_ of [[nonabelian bundle gerbes]].


## Properties

### Lie groupoid bibundles and Morita/stack morphisms
 {#LieGroupoidBibundlesAndMoritaMorphisms}

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

Here the $\mathcal{G}_\bullet$-action on $\mathcal{P}(f)$ is principal over $\mathcal{X}_0$, in that the quotient map is

$$
  \mathcal{P}(f) \to \mathcal{P}(f)//\mathcal{G} \simeq \mathcal{X}_0
  \,,
$$

since $\mathcal{P}(f)$ is the pullback of a $\mathcal{G}_\bullet$-principal bundle (modualted by the bottom composite map in the above diagram). 

On the other hand the $\mathcal{X}_\bullet$-action on $\mathcal{P}(f)$ is not principal over $\mathcal{G}_0$ -- unless $f$ is an [[equivalence in an (infinity,1)-category]] (hence a ([[Morita equivalence|Morita]]) from $\mathcal{X}_\bullet$ to $\mathcal{G}_\bullet$.) It is instead always principal over $f^\ast \mathcal{G}_0$.

=--

Thus we arrive at an equivalent, however more basic definition of Lie groupoid bibundle:
+-- {: .num_defn }
###### Definition

Given Lie groupoids $G:=G_1\Rightarrow G_0$ and $H:=H_1\Rightarrow H_0$, a $G$-$H$-**bibundle** is a principal $H$-bundle $E \xrightarrow{\pi_G} G_0$ over $G_0$ with anchor $E\xrightarrow{\pi_H} H_0$ together with a left $G$-action (see [here](http://ncatlab.org/nlab/show/groupoid+principal+bundle#lie_groupoid_principal_bundles) ) with anchor $\pi_G$, such that the two actions commute. If the $G$-action also gives arise to a principal bundle over $H_0$, then $E$ induces a [[Morita equivalence]] between $G$ and $H$ and it is sometimes called a **Morita bibundle** in this case.
=--

+-- {: .num_example }
###### Example

Given a manifold $M$, and two open covers $\{U_i\}$ and $\{V_\alpha\}$, we may form two Cech groupoids (see [here](http://ncatlab.org/nlab/show/Lie+groupoid#examples_for_lie_groupoids) ) $\sqcup U_{ij} \Rightarrow \sqcup U_i$ and $\sqcup V_{\alpha \beta} \Rightarrow \sqcup V_\alpha$. Then $\sqcup_{i, \alpha} U_i \times_{M} V_\alpha 
$ (which is a common refinement of $\{U_i\}$ and $\{V_\alpha\}$) is a Morita bibundle. The actions are

$$(x_i, x_j)\cdot (x_j, x_\alpha)=(x_i, x_\alpha), \quad (x_i, x_\alpha)\cdot (x_\alpha, x_\beta)=(x_i, x_\beta). $$

Obviously these actions are free. Moreover, it is also not hard to see that $\sqcup U_i\times_M V_\alpha/\sqcup V_{\alpha \beta} = \sqcup U_i$ and $\sqcup U_i\times_M V_\alpha/\sqcup U_{ij} = \sqcup V_\alpha$. When a free action has representible quotient, it must automatically be proper.
 
=--

##### Composition

Given a bibundle functor $E: G\to H$ and a bibundle functor $F: H\to K$ between Lie groupoids, the composition $E\circ F: G\to K$ is the quotient manifold $E\times_{H_0} F/H_1$ equipped by remained $G$ and $K$ action. Here $H$ acts on $E\times_{H_0} F$ from right by $(x, y)\cdot h_1=(x\cdot h_1^{-1}, y \cdot h_1)$. It is free and proper because the right action of $H$  on $E$ is so. Then $G$ action and $K$ action descend to the quotient $E\times_{H_0} F/H_1$. Moreover, those who free and proper is (are), remains so. 

Thus bibundle functors compose to a bibundle functor, and Morita bibundles compose to a Morita bibundle.


Then we see that  there is a $(2,1)$-category $BUN$ with objects Lie groupoids, 1-morphisms bibundle functors, and 2-morphisms isomorphisms of bibundles. It is $(2,1)$-category because 2-morphisms are obviously invertible. This $(2,1)$-category is equivalent to the one obtained by generalised morphism or by anafunctors. 

##### Bundlisation #####

Given a strict morphism $G\xrightarrow{f} H$, then we may form a bibundle $E:= G_0\times_{f_0, H_0, t} H_1$ with right $H$ action induced by $H$-multiplication and with left $G$ action induced by $G$-action on $G_0$. Bundlisation preserves composition. 

Thus 


+-- {: .num_remark #TruncationOfBibundle}
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

Here the vertically-running morphisms are the [[objects]] and two such are related by a [[morphism]] if they fit into a commuting diagram complete by horizontal morphisms as indicated. Since $\mathcal{X}_\bullet$ and $\mathcal{G}_\bullet$ both are groupoids, these morphisms are unique if they exist, and hence, as predicted by remark \ref{TruncationOfBibundle}, $\mathcal{P}(f)$ is 0-truncated, hence is a [[smooth space]]. Moreover, since the [[isomorphism]] [[equivalence relation]] here is free, the [[quotient]] [[smooth space]] is actually a [[smooth manifold]] (since $\mathcal{X}_\bullet$ and $\mathcal{G}_\bullet$ are [[Lie groupoids]]). 

This then recovers the definition of bibundles for Lie groupoids as often found in the literature.


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
 {#RelationToGroupoidConvolutionBimodules}

There should be a [[2-functor]] from [[Lie groupoids]] to [[C-star-algebras]] and [[Hilbert C-star-bimodules]] between them given by forming [[groupoid convolution algebras]] and naturally exhibited by Lie groupoid bibundles: the [[groupoid convolution algebra]] of the total space of the bibindle becomes a [[bimodule]] over the two other groupoid convolution algebras.

Some aspects of this are in the literature, e.g. ([Mr&#269;un 99](#Mrcun99)) for [[étale Lie groupoids]] and ([Landsman 00](#Landsman00)) for general [[Lie groupoids]]. The follwing is taken from the latter article.

+-- {: .num_defn #BundleOfVertical}
###### Definition/Notation

For $p \colon E \to X$ a [[smooth function]] between smooth manifolds, we write $T^p E \hookrightarrow T E$ for the bundle of [[vertical vector fields]], the sub-bundle of the [[tangent bundle]] of $E$ on those vectors in the [[kernel]] of the [[differentiation]] maps $d p|_{e} \colon T_e E \to T_{\tau(e)} X$.

We write ${\vert \Lambda\vert^{1/2}}(T^\tau E)$ for the bundle of [[half-densities]] on vertical vector fields.

=--

+-- {: .num_remark #ActionOnVerticalVectors}
###### Remark

Let $\mathcal{G}_\bullet$ be a [[Lie groupoid]] and let ($E \stackrel{\tau}{\to} \mathcal{G}_0, \rho)$ be a $\mathbb{G}_\bullet$-[[groupoid-principal bundle]] $E \to E//\mathcal{G}$ (with anchor $\tau$ and action map $\rho$). 

Then the bundle of [[vertical vector fields]] $T^\tau E$ equipped with the anchor map $T^\tau E \stackrel{d \tau}{\to} T \mathcal{G}_0 \to \mathcal{G}_0$ inherits a canonical $\mathcal{G}_\bullet$-action itself.


The [[quotient]] map

$$
  {\vert \Lambda\vert^{1/2}}(T^\tau E)/\mathcal{G} \to E/\mathcal{G}
$$

exists and is naturall a vector bundle again.

=--

+-- {: .num_defn #TwoVersionsOfHalfDensities}
###### Definition

In the situation of remark \ref{ActionOnVerticalVectors}, write

* $C^\infty_{c/G}(E, {\vert\Lambda\vert}^{1/2}(T^\tau) E)^G$

  for the space of [[smooth function|smooth]] [[sections]] of the [[half-density]]-bundle of $T^\tau E$ which are $\mathcal{G}$-equivariant and which have [[compact support]] up to $\mathcal{G}$-action;

* $C^\infty_c(E/\mathcal{G}, {\vert \Lambda\vert}^{1/2}(T^\tau E))$

  for the space of smooth sections with compact support of the quotient bundle. 

=--

The following constructions work by repeatedly applying the following identification:

+-- {: .num_prop }
###### Proposition

In the situation of def. \ref{TwoVersionsOfHalfDensities}, there is a [[natural isomorphism]]

$$
  C^\infty_{c/G}(E, {\vert\Lambda\vert}^{1/2}(T^\tau) E)^G
  \simeq
  C^\infty_c(E/\mathcal{G}, {\vert \Lambda\vert}^{1/2}(T^\tau E)  )
  \,.
$$

=--

The central definition here is now:

+-- {: .num_defn #BisectionsOnFiberProductOfTwoGActionSpaces}
###### Definition

For $(E_1, \tau_1)$, $(E_2, \tau_2)$ two principal $\mathcal{G}_\bullet$ manifolds, set

$$
  (E_1, E_2)_{\mathcal{G}}
  \coloneqq
  C^\infty_c( E_1 \underset{\mathcal{G}_0}{\times}) E_2, {\vert\Lambda\vert^{1/2}(T^\tau E_1)} \otimes  {\vert\Lambda\vert^{1/2}(T^\tau E_2)}
$$

=--

And the central fact is:

+-- {: .num_prop #TheBimdoduleConvolutionProduct}
###### Proposition

Given 3 $\mathcal{G}_\bullet$-manifolds $(E_i, \tau_i)$, $i \in \{1,2,3\}$, there is a  [[smooth function]]

$$
  \star
  \;\colon\;
  (E_1, E_2)_{\mathcal{G}}
  \times
  (E_2, E_3)_{\mathcal{G}}
  \to
  (E_1, E_3)_{\mathcal{G}}
$$

given on sections $\sigma_1, \sigma_2$ and points $(e_1, e_3)$ by

$$
  \sigma_1 \star \sigma_2
  \colon
  (e_1, e_3)
  \mapsto
  \int_{\tau_2^{-1}(\tau_1 e_1)}
  \sigma_1(e_1, -)  \otimes \sigma_2(-,e_3)
  \,,
$$

where the [[integration]] is against the [[measure]] that appears by tensoring two (of the four) [[half-densities]] in the integrand.

This operation is an associative and invoutive partial composition operation and hence defines a [[star-category]] whose [[objects]] are $\mathcal{G}_\bullet$-principal manifolds and whose spaces of morphisms are as in def. \ref{BisectionsOnFiberProductOfTwoGActionSpaces}.

=--

In particular one has the following identifications.

+-- {: .num_example #GroupoidConvolutionAlgebraFromBibundleCase}
###### Example

For $\mathcal{G}_1 \to \mathcal{G}_0$ regarded as a $\mathcal{G}_\bullet$-principal action space, there is a [[natural isomorphism]]

$$
  (\mathcal{G}_1, \mathcal{G}_1)_{\mathcal{G}}
  \simeq
  C^\infty_c(\mathcal{G}_1, {\vert\Lambda\vert}^{1/2}(T^s \mathcal{G}_1) \otimes {\vert\Lambda\vert}^{1/2}(T^t \mathcal{G}_1))
$$

and the algebra structure on this by prop. \ref{TheBimdoduleConvolutionProduct} is isomorphic to the [[groupoid convolution algebra]] of smooth sections over $\mathcal{G}_\bullet$.

=--

More generally:

+-- {: .num_example }
###### Example

For $E \stackrel{\tau}{\to} \mathcal{G}_0$ any $\mathcal{G}$-principal manifold, we have a [[natural isomorphism]]

$$
  (\mathcal{G}_1, E)_{\mathcal{G}}
  \simeq
  C^\infty_c(E_1, {\vert\Lambda\vert}^{1/2}(T^G E) \otimes {\vert\Lambda\vert}^{1/2}(T\tau E))
  \,.
$$

=--

> We consider [[completion]] of all this to the [[C-star-algebra]] context (...)

Now we can put the pieces together and sends groupoid-bindunles to $C^\ast$-bimodules over the two [[groupoid convolution algebras]].

+-- {: .num_prop }
###### Proposition

Given two [[Lie groupoids]] $\mathcal{G}_\bullet$ and $\mathcal{K}_\bullet$ and given a [[Morita equivalence]] groupoid [[bibundle]] $E$ between them, we have

$$
  N \coloneqq (\mathcal{G}_1, E)_{\mathcal{G}} \simeq (E, \mathcal{K})_{\mathcal{K}}
$$

and this identification makes $N$ into a $C^\ast(\mathcal{G}_\bullet)-C^\ast(\mathcal{K}_\bullet)$-pre-[[Hilbert bimodule]] as follows:

1. The identification $N \simeq (E, \mathcal{K}_1)_{\mathcal{K}}$ defines the right $C^\ast(\mathcal{K}_\bullet)$-action by example \ref{GroupoidConvolutionAlgebraFromBibundleCase}; and similarly the identification $N \simeq (\mathcal{G}_1, E)_{\mathcal{G}}$ defines a left $C^\ast(\mathcal{G}_\bullet)$-action.

1. The $C^\ast(\mathcal{K})$-valued [[inner product]] on $N$ is that induced by the composite

   $$
     (E,\mathcal{K}_1)_{\mathcal{K}}^\ast
     \times
     (E,\mathcal{K}_1)_{\mathcal{K}}
     \stackrel{\simeq}{\to}
     (\mathcal{K}_1)_{\mathcal{K}, E}
     \times
     (E,\mathcal{K}_1)_{\mathcal{K}}
     \to
     (\mathcal{K}_1, \mathcal{K}_1)_{\mathcal{K}}
     \hookrightarrow
     C^\ast(\mathcal{K}_\bullet)
     \,.
   $$

=--


## References
 {#References}

### General

Groupoid bibundles were first considered for [[foliation groupoids]] in 

* [[Michel Hilsum]] and [[Georges Skandalis]], _Morphismes K-orientes d'espaces de feuilles et functorialite en theorie de Kasparov_. Ann. Scient. Ec. Norm. Sup. 20 (1987), 325&#8211;390. ([numdam](http://www.numdam.org/item?id=ASENS_1987_4_20_3_325_0))
 {#HilsumSkandalis}

The generalization to arbitrary [[topological groupoids]] was considered in

* [[André Haefliger]], _Groupo&#239;des d'holonomie et classifiants_, Ast&#233;risque 116 (1984), 70&#8211;97.
 {#Haefliger84}

* [[Jean Pradines]], _Morphisms between spaces of leaves viewed as fractions_. Cahiers Top. G&#233;om. Diff. Cat. XXX-3 (1989), 229&#8211;246
 {#Pradines89}

* M. Hilsum and [[Georges Skandalis]], _Morphismes K-orientes d'espaces de feuilles et functorialite en theorie de Kasparov_. Ann. Scient. Ec. Norm. Sup. 20 (1987), 325&#8211;390.
 {#HilsumSkandalis87b}

and independently in [[topos theory]] in

* [[Marta Bunge]], _An application of descent to a classification theorem. Math. Proc. Cambridge Phil. Soc. 107 (1990), 59&#8211;79.
 {#Bunge90}

* [[Ieke Moerdijk]], _Classifying toposes and foliations_. Ann. Inst. Fourier, Grenoble 41, 1 (1991), 189&#8211;209.
 {#Moerdijk91}

Groupoid bibundles are used in the context of [[groupoid convolution algebras]] as geometric analogs of [[bimodules]] in 

* [[Paul Muhly]], [[Jean Renault]], and D. Williams, _Equivalence and isomorphism for groupoid C&#8727;-algebras_, J. Operator Th. 17 (1987), 3&#8211;22.
 {#MuhlyRenaultWilliams}

* [[Klaas Landsman]], _The Muhly-Renault-Williams theorem for Lie groupoids and its classical counterpart_, Lett. Math. Phys. 54 (2000), no. 1, 43&#8211;59. ([arXiv:math-ph/0008005](http://arxiv.org/abs/math-ph/0008005))
 {#Landsman}
 {#Landsman00}

* [[Janez Mr?un]], _Stability and invariants of Hilsum-Skandalis maps_ ([arXiv:math/0506484](http://arxiv.org/abs/math/0506484))
 {#Mrcun05}

A review of [[Lie groupoid]]-bibundles and maps of [[differentiable stacks]] is in section 2 of 

* [[Christian Blohmann]], _Stacky Lie groups_, Int. Mat. Res. Not. (2008) Vol. 2008: article ID rnn082 ([arXiv:math/0702399](http://arxiv.org/abs/math/0702399))
 {#Blohmann}

Discussion of [[Lie group cohomology]] and the [[string 2-group]] [[infinity-group extension]] in terms of Lie groupoid bibundles is in

* [[Chris Schommer-Pries]] _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ [arXiv:0911.2483](http://arxiv.org/abs/0911.2483/) 
 {#Sp}

Talk notes on bibundles include

* [[Michael Murray]], _Bispaces and bibundles_ ([pdf slides](http://www.mpim-bonn.mpg.de/digitalAssets/7050_Murray.pdf))

* [[Jeffrey Morton]], ([pdf slides](http://www.math.uwo.ca/~jmorton9/seminar/gpdrep.pdf))

See also

* [[Michael Murray]], [[David Roberts]], [[Danny Stevenson]], _On the existence of bibundles_ LMS (2012)([arXiv:1102.4388](http://arxiv.org/abs/1102.4388))

### Convolution to $C^\ast$-bimodules

For groupoid bibundles between [[étale Lie groupoids]] the assignment of the [[groupoid convolution algebra]]-[[bimodule]] to them is shown to be [[functor|functorial]] in 

* [[Janez Mr?un]], _Functoriality of the bimodule associated to a Hilsum-Skandalis map_. K-Theory 18 (1999) 235&#8211;253.
 {#Mrcun99}

For more references along these lines see for the moment at [groupoid convolution algebra -- Extension to bibundles and bimodules](http://ncatlab.org/nlab/show/category+algebra#ExtensionToBibundlesAndBimodules)

[[!redirects bibundle]]
[[!redirects bibundles]]

[[!redirects groupoid bibundle]]
[[!redirects groupoid bibundles]]

[[!redirects Hilsum-Skandalis morphism]]
[[!redirects Hilsum-Skandalis morphisms]]

[[!redirects Hilsum-Skandalis map]]
[[!redirects Hilsum-Skandalis maps]]

[[!redirects ∞-groupoid bibundle]]
[[!redirects ∞-groupoid bibundles]]
[[!redirects infinity-groupoid bibundle]]
[[!redirects infinity-groupoid bibundles]]