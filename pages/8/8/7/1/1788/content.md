
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

\begin{definition}
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

Here are some first observations

Throughout, let $\mathscr{C}$ be a category with [[colimits]], so that the [[Grothendieck construction]] 

\[
  \label{Loc}
  Loc_{\mathcal{C}}
  \;\;
  \coloneqq
  \;\;
  \underset{\mathcal{X} \in Grpd}{\textstyle{\int}}
  \mathcal{C}^{\mathcal{X}}
\]
is actually a [[bifibration]], induced from the [[CatAdj|$Cat_{adj}$]]-valued [[pseudofunctor]]
$$
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
$$
whose [[left adjoint]]-components $f_!$ are given by [[left Kan extension]].

We shall write
$$
  \array{
    Set \times \mathcal{C} 
     &\overset{(-)\cdot(-)}{\longrightarrow}&
    \mathcal{C}
    \\
    (S, \mathscr{V}) &\mapsto& \underset{s \in S}{\coprod} \mathscr{V}
  }
$$
for the canonically induced [[tensoring]] of $\mathcal{C}$ over [[Set]].

Finally, we assume now that $\mathcal{C}$ carries the [[structure]] of a [[symmetric monoidal category]]. This implies that $Loc_{\mathcal{C}}$ (eq:Loc) inherits the corresponding [[external tensor product]], which we denote

$$
  Loc_{\mathcal{C}}
  \times 
  Loc_{\mathcal{C}}
  \xrightarrow{ \boxtimes }
  Loc_{\mathcal{C}}
  \,.
$$ 

A good example to keep in mind is $\mathcal{C} \,\equiv\,$ [[Vect]] equipped with the usual [[tensor product of vector spaces]]. In this case the objects of $Loc_{\mathcal{C}}$ may be understood as [[flat vector bundles]] over [[homotopy 1-types]], also known as "[[local systems]]", whence our notation.

For $G$ a [[group]], we write

* $\mathbf{B}G \,\equiv\, (G \rightrightarrows pt)$ 

  for its [[delooping groupoid]] 

* $\mathbf{E}G \,\equiv\, (G \times G \rightrightarrows G)$ 
 
  for the [[action groupoid]] of $G$ [[action|acting]] on itself by right multiplication. 


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
      \overset{\mu(g,-)}{\longrightarrow}
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
      \mathbb{1}_g \,\boxtimes\, g_{pt}
    \big)
  }}
  &&
  \Big\downarrow\mathrlap{{}^{
    \mu(g,-)_{\mathbf{B}G}
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

