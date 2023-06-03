
#Contents#
* table of contents
{:toc}


## Idea

Noticing hat 

1. every [[set]] is the [[coproduct]] over its [[singleton]] elements, 

1. every [[skeletal groupoid]] is the [[coproduct]] over its [[connected component]] [[delooping groupoids]], hence is a "set of points with [[automorphism groups]]"

1. a [[coproduct]] is a [[colimit]] over a [[diagram]] of the shape of a [[discrete category]] (a [[set]]) [[Set]] $\hookrightarrow$ [[Cat]]

it makes sense, in [[homotopy theory|homotopy theoretic]] generalization of coproducts, to consider *quasi-coproducts* &lbrack;[Hu & Tholen (1996)](#HuTholen96)&rbrack; to be colimits over diagrams of the shape of [[skeletal groupoids]] $Grpd_{skl} \hookrightarrow Cat$ which are degreewise [[free actions]], in a suitable sense, such that these colimits tend to behave like [[homotopy colimits]].


## Definition

\begin{definition}\label{QuasiCoproduct}
  A *quasi-coproduct* in a [[category]] $\mathcal{C}$ is a [[colimit]] over a [[diagram]] 
$$
  \mathscr{V}_{(-)}
    \,\colon\, 
  \mathcal{G} \longrightarrow \mathcal{C}
$$
of the shape of a [[skeletal groupoid]] $\mathcal{G} \,\in\, Grpd_{skl} \hookrightarrow$ such that the following condition is satisfied

* for all [[connected components]] $\mathbf{B}G_i \hookrightarrow \mathcal{G}$ and all non-[[initial objects]] $\mathscr{W} \,\in\, \mathcal{C}$ the [[group action]] in [[Set]] given by the composite with the [[hom-functor]] $\mathcal{C}(\mathscr{W},-)$
$$
 \mathbf{B}G_i
 \hookrightarrow
 \mathcal{G}
  \overset{
    \mathscr{V}_{(-)}
  }{\longrightarrow}
 \mathcal{C}
  \overset{\mathcal{C}(\mathscr{W},-)}{\longrightarrow}
 Set
$$
is a [[free action]].

\end{definition}
&lbrack;[Hu & Tholen (1996), §1.3](#HuTholen96)&rbrack;


## Properties

### Free quasi-coproduct-completion

In generalization of how 

* the [[free coproduct completion]] of a category $\mathcal{C}$ is the [[Grothendieck construction]] $\int_{X \in Set} \mathcal{C}^X$ over the [[pseudofunctor]] 

  $$
    Set^{op} 
     \hookrightarrow 
    Cat^{op} 
    \overset{
     Func(-,\mathcal{C})
    }{\longrightarrow}
    Cat
  $$

it ought to be the case that 

* the free quasi-coproduct completion of $\mathcal{C}$ is the [[Grothendieck construction]] $\int_{\mathcal{X} \in Grpd} \mathcal{C}^{\mathcal{X}}$ over the [[pseudofunctor]] 

  $$
    Grpd^{op} 
     \hookrightarrow 
    Cat^{op} 
    \overset{
     Func(-,\mathcal{C})
    }{\longrightarrow}
    Cat
  $$

Or something close.

\begin{definition}
\label{DeloopingGroupoids}
For $(G, \mu, \mathrm{e})$ a [[group]], we write

* $\mathbf{B}G \,\equiv\, (G \rightrightarrows pt)$ 

  for its [[delooping groupoid]]

* $\mathbf{E}G \,\equiv\, (G \times G \rightrightarrows G)$ 
 
  for the [[action groupoid]] of $G$ [[action|acting]] on itself by left multiplication. 

The remaining right multiplication of $G$ on $\mathbf{E}G$ defines a [[group action]]
$$
  \array{
    \mathbf{B}G 
    &\longrightarrow&
    Grpd
    \\
    pt &\mapsto& \mathbf{E}G
    \\
    \Big\downarrow\mathrlap{{}^{ g }}
      && 
    \Big\downarrow\mathrlap{{}^{ \mu(-,g) }}
    \\
    pt &\mapsto& \mathbf{E}G
  }
$$
whose [[quotient object]] is
$$
  \mathbf{B}G
  \;\simeq\;
  \big(\mathbf{E}G\big)/G
  \,.
$$
(See also at *[[universal principal bundle]]* and at [[simplicial classifying space]].)
\end{definition}

\begin{definition}
\label{CategoryWithHomotopicalQuasiCoproducts}
A category with *homotopical quasi-coproducts* is

* equipped with a [[tensoring]] over the [[1-category]] [[Grpd]]

  \[
    \label{GrpdTensoring}
    Grpd \times \mathcal{C} 
      \xrightarrow{(-)\cdot(-)} 
    \mathcal{C}
  \]

* has all quasi-coproducts (Def. \ref{QuasiCoproduct}) of the form

  \[
    \label{HomotopicalQuasiCoproducts}
    \array{
      \mathcal{G} &\longrightarrow& \mathcal{C}
      \\
      \mathllap{{}^{=}}\Big\uparrow
        &&
      \Big\uparrow\mathrlap{
        (-)\cdot(-) 
      }
      \\
      \underset{i}{\coprod}
      \mathbf{B}G_i
      &\underset{
        \big(
          \mathbf{E}G_i  ,\, \mathscr{V}_{(-)}
        \big)_{i\in I}
      }{\longrightarrow}&
      Grpd \times \mathcal{C}
    }
  \]

\end{definition}


\begin{definition}
**(free homotopical quasi-coproduct completion)**
\linebreak
  For $\mathcal{C}$ a category, its *free homotopical quasi-coproduct completion* is 

* a category $QC(\mathcal{C})$ with homotopical quasi-products (Def. \ref{CategoryWithHomotopicalQuasiCoproducts}) 

equipped with 

* a [[full subcategory]] inclusion $\mathcal{C} \hookrightarrow QC(\mathcal{C})$,

such that 

* [[functors]] $QC(\mathcal{C}) \longrightarrow \mathcal{D}$ to another category $\mathcal{D}$ with homotopical quasi-coproducts which [[preserved colimit|preserve]] 

  1. the $Grpd$-tensoring (eq:GrpdTensoring) 

  1. the quasi-coproducts (eq:HomotopicalQuasiCoproducts) 

  are fixed by the restriction of the [[underlying]] functor along $\mathcal{C} \hookrightarrow QC(\mathcal{C})$.

\end{definition}

Here are some first observations.

The following Def. \ref{CategoryOfLocalSystems} of "categories of local systems" may be understood as the 1-step [[homotopy theory|homotopy-theoretic]] generalization of the category $\int_{X \in Set} \mathcal{C}^X$ of [[indexed sets]] of objects in $\mathcal{C}$

\begin{definition}
\label{CategoryOfLocalSystems}
 For $\mathcal{C}$ a [[category]], we write
\[
  \label{Loc}
  Loc_{\mathcal{C}}
  \;\;
  \coloneqq
  \;\;
  \underset{\mathcal{X} \in Grpd}{\textstyle{\int}}
  \mathcal{C}^{\mathcal{X}}
\]
for the [[Grothendieck construction]] on the [[pseudofunctor]] which sends [[groupoids]] $\mathcal{X} \in $ [[Grpd]] to the [[functor category]] $\mathcal{C}^{\mathcal{X}} \,\coloneqq\,Func(\mathcal{X}, \mathcal{C})$ and [[functors]] $f \,\colon\,\mathcal{X} \to \mathcal{X}'$ to the [[precomposition]] operation $f^\ast \,\coloneqq\, (-) \circ f$: 
\[
  \label{PseudofunctorOfFunctorCategories}
  \array{
    Grpd &\longrightarrow& Cat
    \\
    \mathcal{X} &\mapsto& \mathcal{C}^{\mathcal{X}}
    \\
    \Big\downarrow\mathrlap{{}^{f}}
    &&
    \Big\uparrow\mathrlap{{}^{f^\ast}}
    \\
    \mathcal{X}' &\mapsto& \mathcal{C}^{\mathcal{X}'}
  }
\]
\end{definition}

\begin{example}
For $\mathbb{K}$ a [[field]] and $\mathcal{C} \,\equiv\, $ [[Mod|$Mod_{\mathbb{K}}$]] $\equiv$ [[Vect|$Vect_{\mathbb{K}}$]] its category of [[vector spaces]], a functor $\mathcal{X} \longrightarrow Mod_{\mathbb{C}}$ -- for $\mathcal{X}$ thought of as the [[fundamental groupoid]] of some [[topological space]] $X$ --, is (equivalently a [[flat vector bundle]] on $X$ but) also known as a *[[local system]]* $X$. Therefore in this case the category (eq:CategoryOfLocalSystems)
$$
  Loc_{\mathbb{K}}
  \;\coloneqq\;
  Loc_{Mod_{\mathbb{K}}}
$$
may be thought of as the category of "local systems over varying base spaces", whence the notation in Def. \ref{CategoryOfLocalSystems}.
\end{example}

\begin{remark}
If $\mathscr{C}$ has all [[small diagram|small]] [[colimits]],  then the [[Grothendieck construction]] of Def. \ref{CategoryOfLocalSystems}
$$
  \array{
    Loc_{\mathcal{C}}
    \\
    \Big\downarrow
    \\
    Grpd
  }
$$
is actually a [[bifibration]], induced from the [[CatAdj|$Cat_{adj}$]]-valued [[pseudofunctor]]
\[
  \label{CatAdjValuedPseudofunctorOfFunctorCategories}
  \array{
    Grpd_{skl} &\longrightarrow& Cat_{adj}
    \\
    \mathcal{X} &\mapsto& \mathcal{C}^{\mathcal{X}}
    \\
    \Big\downarrow\mathrlap{{}^{f}}
    &&
    \mathllap{{}^{f_!}}\Big\downarrow
    {}^{\dashv}
    \Big\uparrow\mathrlap{{}^{f^\ast}}
    \\
    \mathcal{X}' &\mapsto& \mathcal{C}^{\mathcal{X}'}
  }
\]
whose [[left adjoint]]-components $f_!$ are given by [[left Kan extension]].

In this case, all [[colimits]] over [[diagrams]] $\mathscr{V}_{\mathcal{X}} \,\colon\, \mathcal{I} \longrightarrow Loc_{\mathcal{C}}$ in the [[Grothendieck construction]] $Loc_{\mathcal{C}}$ (eq:Loc) exist and (by the discussion [there](Grothendieck+construction#CoLimitsInAGrothendieckConstruction)) are given on [[underlying]] groupoids as the corresponding underlying colimit $\underset{\longrightarrow}{lim} \mathcal{X}$ in [[Grpd]] and on components in $\mathcal{C}$ the colimit in $\mathcal{C}^{ \underset{\longrightarrow}{lim} \mathcal{X}}$ of the diagram of pushforwards $q_!$ (eq:CatAdjValuedPseudofunctorOfFunctorCategories) of morphisms along the underlying [[coprojections]] $\mathcal{X}_i \xrightarrow{q_i} \underset{\longrightarrow}{lim} \mathcal{X}$:
$$
  \underset{\longrightarrow}{\lim}
  \mathscr{V}_{\mathcal{X}}
  \;\;
  \simeq
  \;\;
  \big(
    \underset{\longrightarrow}{lim}
    q_!\mathscr{V}
  \big)_{ \underset{\longrightarrow}{lim} \mathcal{X} }
  \,.
$$
\end{remark}

\begin{remark}
If $\mathcal{C}$ carries the [[structure]] of a [[symmetric monoidal category]] such that the pullback functors $f^\ast$ (eq:PseudofunctorOfFunctorCategories) are [[strong monoidal functors]], then $Loc_{\mathcal{C}}$ (eq:Loc) inherits the corresponding [[external tensor product]], which we denote

$$
  Loc_{\mathcal{C}}
  \times 
  Loc_{\mathcal{C}}
  \xrightarrow{ \boxtimes }
  Loc_{\mathcal{C}}
  \,.
$$ 

Notice that for any $\mathcal{X} \,\in\, Grpd$ the external tensor product with $\mathbb{1}_{\mathcal{X}} \,\coloneqq\, (p_{\mathcal{X}})^\ast \mathbb{1}_{pt}$ (i.e. with the [[tensor unit]] over $\mathcal{X}$, which is the [[constant functor]] $\mathcal{X} \to \ast \xrightarrow{\mathbb{1}} \mathcal{C}$) is equivalently the [[base change]] operation along the [[projection]] out of the [[product groupoid]] $pr_{\mathcal{Y}} \,\colon\, \mathcal{X} \times \mathcal{Y} \longrightarrow \mathcal{Y}$

$$
  \mathbb{1}_{\mathcal{X}}
  \,\boxtimes\,
  \mathscr{V}_{\mathcal{Y}}
  \;\;\;
    \simeq
  \;\;\;
  \big(
    (pr_{\mathcal{Y}})^\ast \mathscr{V}
  \big)_{\mathcal{X} \times \mathcal{Y}}
  \,.
$$
Since here the expression on the right hand side does not actually invoke the [[monoidal category|monoidal structure]] of $\mathcal{C}$ it is expedient to allow ourselves to use the notation on the left even when $\mathcal{C}$ is not equipped with monoidal structure.

This is the canonical [[tensoring]] of $Loc_{\mathcal{C}}$ over [[Grpd]]:
\[
  \label{CanonicalTensoringOfLocOverGrpd}
  \array{
    Grpd \times Loc_{\mathcal{C}}
    &\overset{(-)\cdot(-)}{\longrightarrow}&
    Loc_{\mathcal{C}}
    \\
    \big(
      \mathcal{X}
      ,\,
      \mathscr{V}_{\mathcal{Y}}
    \big)
    &\mapsto&
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{V}
    \big)_{
      \mathcal{X} \times \mathcal{Y}
    }
  }
\]

\end{remark}

\begin{lemma}
  Given an object $\mathscr{V}_{\mathcal{X}} \,\in\, Loc_{\mathbb{C}}$ (eq:Loc) it is [[isomorphism|isomorphic]] to a [[coproduct]] of [[tensorings]] with [[codiscrete groupoids]] of objects over [[delooping groupoids]]
$$
  \mathscr{V}_{\mathcal{X}}
  \;\;
  \simeq
  \;\;
  \underset{i \in \pi_0(\mathcal{C})}{\coprod}
    \Big(
      CoDisc\big(
        Obj(\mathcal{X}_i)
      \big)
      \cdot
      \big(
       \iota_{\mathbf{B}G_i}^\ast
       \mathscr{V}
    \big)_{\mathbf{B}G_i}
  \Big)
  \,.
$$
and hence to the [[domain]] of a morphism obtained as a [[coproduct]] of [[tensorings]] (eq:CanonicalTensoringOfLocOverGrpd) of local system over a [[skeletal groupoids]] with the terminal maps out of [[codiscrete groupoids]]:
$$
  \mathscr{V}_{\mathcal{X}}
  \,\in\,
  Loc_{\mathcal{C}}
  \;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;
  \mathscr{V}_{\mathcal{X}}
  \simeq
  \bigg(
    \underset{i \in \mathcal{X}_i}{\amalg}
    \Big(
      CoDisc\big(\mathrm{Obj}(\mathcal{X}_i)\big)
      \cdot
      \big(
        \iota_{\mathbf{B}G_i}^\ast
        \mathscr{V}
      \big)_{ \mathbf{B}G_i }
    \Big)
  \Bigg)
  \overset{
    \underset{i \in I}{\amalg}
    \Big(
      p_i \cdot 
      \big(
        \iota_{\mathbf{B}G_i}^\ast
        \mathscr{V}
      \big)_{ \mathbf{B}G_i }
    \Big)
  }{\longrightarrow}
  \Big(
    \underset{i \in \mathcal{X}_i}{\amalg}
    \big(
      \iota_{\mathbf{B}G_i}^\ast
      \mathscr{V}
    \big)_{ \mathbf{B}G_i }
  \Big)  
$$
\end{lemma}
\begin{proof}
  On [[underlying]] groupoids the isomorphism is induced by a choice of [[adjoint equivalence|adjoint]] [[deformation retraction]] onto a [[skeletal groupoid]] (spelled out [here](Introduction+to+Topology+--+2#EveryGroupoidIsomorphicToQuasiSkeletalGroupoid)).

It remains to observe that every local system on $CoDisc\big(Obj(\mathcal{X}_i)\big) \times \mathbf{B}G_i$ is isomorphic to one pulled back from $\mathbf{B}G_i$, i.e. to one which constant along $CoDisc\big(Obj(\mathcal{X}_i)\big)$. For this choose any $x_i \in Obj(\mathcal{X}_i)$ and consider the evident [[natural isomorphism]]

$$
  \array{
    CoDisc\big(Obj(\mathcal{X}_i)\big)
    &\overset{}{\longrightarrow}&
    \mathcal{C}
    \\
    x
    &\mapsto&
    \mathscr{V}_x
    &\overset{\mathscr{V}_{(x,x_i)}}{\longrightarrow}&
    \mathscr{V}_{x_i}
    \\
    \Big\downarrow
    &&
    \Big\downarrow\mathrlap{{}^{ \mathscr{V}_{(x,x')} }}
    &&
    \Big\downarrow\mathrlap{{}^{id}}
    \\
    x'
    &\mapsto&
    \mathscr{V}_{x'}
    &\underset{\mathscr{V}_{(x',x_i)}}{\longrightarrow}&
    \mathscr{V}_{x_i}
    \mathrlap{\,.}
  }
$$
\end{proof}



\begin{lemma}
For $G \in Grp$, any $G$-[[group representation|representation]] $\mathscr{V}_{\mathbf{B}G} \,\colon\, \mathbf{B}G \overset{\rho}{\longrightarrow} \mathcal{C}$ is the colimit in $Loc_{\mathcal{C}}$ (eq:Loc) over the diagram
$$
  \array{
    \mathbf{B}G
    &\overset{\;}{\longrightarrow}&
    Loc_{\mathcal{C}}
    \\
    pt 
      &\mapsto& 
    \mathbb{1}_{\mathbf{E}G} 
      \boxtimes 
    \mathscr{V}_{pt}
    \\
    \Big\downarrow\mathrlap{{}^g}
      && 
    \Big\downarrow\mathrlap{{}^{  
      \mathbb{1}_{\mu(g,-)}   
      \,\boxtimes\,
      {\rho(g)}_{pt}
    }}
    \\
    pt
    &\mapsto&
    \mathbb{1}_{\mathbf{E}G} 
      \boxtimes 
    \mathscr{V}_{pt}
  }
$$
\end{lemma}
\begin{proof}
Consider the cocone
$$
  \array{
    \mathbb{1}_{\mathbf{E}G}
    \boxtimes
    \mathscr{V}_{pt}
    &&\overset{
      \mathbb{1}_{\mu(g,-)} \,\boxtimes\, \rho(g)_{pt}
    }{\longrightarrow}&&
    \mathbb{1}_{\mathbf{E}G}
    \boxtimes
    \mathscr{V}_{pt}
    \\
    & 
    \mathllap{{}_{\mathscr{q}_q}}\searrow 
      && 
    \swarrow\mathrlap{{\mathfrak{q}}_{q}}
    \\
    && 
    \mathscr{V}_{\mathbf{B}G}
  }
$$

By the general formula for colimits in Grothendieck constructions ([here](Grothendieck+construction#CoLimitsInAGrothendieckConstruction)), the colimit in question has as [[underlying]] object in [[Grpd]] the colimiting cocone of the underlying diagram in [[Grpd]]:
$$
  \array{
    \mathbf{E}G 
    && 
      \overset{\mu(-,g)}{\longrightarrow}
    &&
    \mathbf{E}G
    \\
    & 
    \mathllap{{}_q}\searrow 
      && 
    \swarrow\mathrlap{{}_q}
    \\
    && \mathbf{B}G
  }
$$
and the $\mathcal{C}$-component over that is the colimit in $\mathcal{C}$ of the diagram of images of morphism under pushforward $q_!$ along the underlying [[coprojection]] $q$.

Now observe that
$$
  \array{
  q_! 
  \big(
    \mathbb{1}_{\mathbf{E}G}
    \,\boxtimes\,
    \mathscr{V}_{pt}
  \big)
  &
  \simeq
  &
  (G\cdot\mathbb{1})_{\mathbf{B}G} \boxtimes \mathscr{V}_{pt}
  \\  
  \Big\downarrow\mathrlap{{}^{
    q_!\big(
      \mathbb{1}_{\mu(-,g)} \,\boxtimes\, \rho(g)_{pt}
    \big)
  }}
  &&
  \Big\downarrow\mathrlap{{}^{
    \mu(-,g)_{\mathbf{B}G}
    \,\boxtimes\,
    {\rho(g)}_{pt}
  }}
  \\
  q_! 
  \big(
    \mathbb{1}_{\mathbf{E}G}
    \,\boxtimes\,
    \mathscr{V}_{pt}
  \big)   
  &
  \simeq
  &
  (G\cdot\mathbb{1})_{\mathbf{B}G} \boxtimes \mathscr{V}_{pt}
  }
$$


\end{proof}




## References

* {#HuTholen96} [[Hongde Hu]], [[Walter Tholen]], *Quasi-coproducts and accessible categories with wide pullbacks*, Appl Categor Struct **4** (1996) 387–402 &lbrack;[doi:10.1007/BF00122686](https://doi.org/10.1007/BF00122686)&rbrack;

