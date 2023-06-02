
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

* the free quasi-coproduct completion of $\mathcal{C}$ is the 
[[Grothendieck construction]] $\int_{\mathcal{X} \in Grpd} \mathcal{C}^{\mathcal{X}}$ over the [[pseudofunctor]] 

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

$$
  Loc_{\mathcal{C}}
  \;\;
  \coloneqq
  \;\;
  \underset{\mathcal{X} \in Grpd}{\int}
  \mathcal{C}^{\mathcal{X}}
$$

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


\begin{lemma}
For $G \in Grp$, any $G$-[[group representation|representation]] $\mathscr{V}_{\mathbf{B}G} \,\colon\, \mathbf{B}G \longrightarrow \mathcal{C}$ is the colimit in $Loc_{\mathcal{C}}^{skl}$ over the diagram
$$
  \array{
    \mathbf{B}G
    &\overset{\;}{\longrightarrow}&
    Loc^{skl}_{\mathbb{K}}
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
      \mathbb{1}_{g}   
      \,\boxtimes\,
      g_{pt}
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
      \mathbb{1}_g \,\boxtimes\, g_{pt}
    }{\longrightarrow}&&
    \mathbb{1}_{\mathbf{E}G}
    \boxtimes
    \mathscr{V}_{pt}
    \\
    & 
    \mathllap{{}_{\mathscr{q}_q}}\searrow 
      && 
    \swarrow\mathrlap{{}_{q}}
    \\
    && 
    \mathscr{V}_{\mathbf{B}G}
  }
$$

The colimiting cocone of the underlying diagram in [[Grpd]] is 
$$
  \array{
    \mathbf{E}G 
    && 
      \overset{g}{\longrightarrow}
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
We have
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
    (g)_{\mathbf{B}G}
    \,\boxtimes\,
    g_{pt}
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

