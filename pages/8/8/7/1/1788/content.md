
Let $\mathcal{C}$ be a [[small category]]. We write

\[
  \label{YonedaEmbedding}
  \mathcal{C}^{op} 
  \xhookrightarrow{\;\;\; y \;\;\;}
  Funct(\mathcal{C}, Sets)
\]

for the [[Yoneda embedding]] of its [[opposite category]], which we will often regard through its [[opposite functor]]

\[
  \label{OppositeYonedaEmbedding}
  \mathcal{C}
  \xhookrightarrow{\;\;\; y^{op} \;\;\;}
  Funct(\mathcal{C}, Sets)^{op} 
  \,.
\]

This is still a [[full subcategory]]-inclusion, now of $\mathcal{C}$ itself.

\begin{definition}\label{CategoryOfProObjects}
**(category of pro-objects)** \linebreak

The the *category of pro-objects in $\mathcal{C}$*, according to [Grothendieck 1960, Section 2](#Grothendieck1960), is the [[full subcategory]] of $Funct(\mathcal{C}, Sets)^{op}$ (eq:OppositeYonedaEmbedding)

\[
  \label{ProCAsFullSubcategoryOfOppositeOfCategoryOfPresheaves}
  Pro(\mathcal{C})
  \xhookrightarrow{\;\;}
  Funct(\mathcal{C}, Sets)^{op}   
\]

on those functors which are [[cofiltered limits]] of [[representable functors]] under the opposite Yoneda embedding (eq:OppositeYonedaEmbedding), hence of the form

\[
  \label{FilteredLimitOfRepresentablesInOppositeOfPresheafCategory}
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)
  \;\;
  \coloneqq
  \;\;
  \underset{\longleftarrow}{\lim}
  \big(
    \mathcal{I}
    \xrightarrow{\;X_\bullet\;}
    \mathcal{C}
    \xrightarrow{\;y^{op}\;}
    Funct(\mathcal{C}, Sets)^{op}
  \big)
  \,,
\]

for $\mathcal{I}$ a [[cofiltered category]]. These objects of $Pro(\mathcal{C})$ are also called the *pro-objects of $\mathcal{C}$*.
\end{definition}

\begin{remark}
Notice that $Funct(\mathcal{C}, Sets)^{op}$ (eq:OppositeYonedaEmbedding) is the [[free completion]] of $\mathcal{C}$, so $Pro(\mathcal{C})$ is the *free completion of $\mathal{C}$ under [[cofiltered limits]].* See also at [[pro-representable functor]].
\end{remark}

\begin{remark}\label{BetweenFilteredLimitsAndFilteredColimits}
Under the identification of the [[objects]] of a category with its [[opposite category]], the  objects (eq:FilteredLimitOfRepresentablesInOppositeOfPresheafCategory) are [[filtered colimits]] of [[presheaves]]:

$$
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  y(X^{op}_i)
  \;\;
  \coloneqq
  \;\;
  \underset{\longrightarrow}{\lim}
  \big(
    \mathcal{I}^{op}
    \xrightarrow{\;X^{op}_\bullet\;}
    \mathcal{C}^{op}
    \xrightarrow{\;y\;}
    Funct(\mathcal{C}, Sets)
  \big)
  \,.
$$
\end{remark}

\begin{lemma}\label{ProObjectsAsFunctors}
  The pro-objects regarded as functors (eq:FilteredLimitOfRepresentablesInOppositeOfPresheafCategory)
  are objectwise on $c \in \mathcal{C}$ given by 
  $$
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
    y^{op}(X_i)  
    \;\;
    \colon
    \;\;
    c 
    \;\mapsto\;
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
    \mathcal{C}(X_i, c)
    \,.
  $$
  because [[limit]] over an [[opposite functor]] is the [[colimit]] of the functor itself.
\end{lemma}
\begin{proof}
This is the composite of the following sequence of [[natural isomorphisms]]
$$
  \begin{aligned}
  \Big(
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)  
  \Big)
  (c) 
  &
  \;\simeq\;
  \Big(
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  y(X^{op}_i)  
  \Big)
  (c) 
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  \Big(
    \big(y(X^{op}_i)\big)
    (c)
  \Big)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \;
  Func(\mathcal{C},Sets)
  \big(
    y(c), \, y(X_i)
  \big)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \mathcal{C}^{op}(c, X_i)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \mathcal{C}(X_i, c)
  \mathrlap{\,,}
  \end{aligned}
$$
where

* the first step is Remark \ref{BetweenFilteredLimitsAndFilteredColimits};

* the second step uses that [[colimits of presheaves are computed objectwise]];

* the third step is the [[Yoneda lemma]];

* the fourth step is the [[Yoneda embedding]] (eq:YonedaEmbedding);

* the fifth step is the definition of the [[opposite category]].

\end{proof}

\begin{lemma}

The [[hom-sets]] in $Pro(\mathcal{C})$ (Def. \ref{CategoryOfProObjects})
are in [[natural bijection]] with [[limits]] of [[colimits]] of [[hom-sets]] in $\mathcal{C}$ as follows:

$$
  Pro(\mathcal{C})
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
$$

\end{lemma}

\begin{proof}
This is the composite of the following sequence of [[natural bijections]]:
$$
  \begin{aligned}
  Pro(\mathcal{C})
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
  &
  \;\simeq\;
  Func(\mathcal{C},Sets)^{op}
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
  \\
  & 
  \;\simeq\;
  Func(\mathcal{C},Sets)
  \Big(
    \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{lim}
    y(Y^{op}_j),    
    \,
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    y(X^{op}_i),
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \;
  Func(\mathcal{C},Sets)
  \Big(
    y(Y^{op}_j),    
    \,
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    y(X^{op}_i),
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \Big(
    \big(
      \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
      y(X^{op}_i)
    \big)
    \big(
      y(Y^{op}_j)
    \big)    
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    \mathcal{C}
    \big(
      X_i,
      \,
      Y_j
    \big)
  \Big)
  \end{aligned}
$$

Here

* the first step is the [[fully faithful functor|fully faithfulness]] of the defining [[full subcategory]]-inclusion (eq:ProCAsFullSubcategoryOfOppositeOfCategoryOfPresheaves);

* the second step is the definition of the [[opposite category]], using Remark \ref{BetweenFilteredLimitsAndFilteredColimits};

* the third step is the [[hom-functor preserves limits]] in the first argument, which means that in the first argument, $\mathcal{K}^{op} \times \mathcal{K} \xrightarrow{Hom} Sets$ takes *[[colimits]] in $\mathcal{K}$* to *limits in $\mathcal{K}$*, here for $\mathcal{K} = Func(\mathcal{C},Sets)$;

* the fourth step is the [[Yoneda lemma]];

* the fifth step is Lemma \ref{ProObjectsAsFunctors}.

\end{proof}

\linebreak

\linebreak

$$
\begin{aligned}
    \tau_0
    \,
    \mathbf{H}
    \big(
      X, \, B \mathcal{G}
    \big)
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    \big[
      X, \, B \mathcal{G}
    \big]
    \\
    &
    \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    \big[
      X,
      \,
      &#643;
      \, 
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    &#643;
    \,
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    Disc
    \,
    \mathrm{Sing}
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    \mathrm{Sing}
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \Big(
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    (\Delta^\bullet_{\mathrm{smth}})
    \Big)
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \Big(
    \mathbf{H}
    \big(
      X
      \times
      \Delta^\bullet_{\mathrm{smth}}
      \,
      \mathbf{B}\mathcal{G}
    \big)
    \Big)
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \big(
      {\mathcal{G}}PrinBund_{X \times \Delta^\bullet_{\mathrm{smth}}}
    \big)
    \\
    & \;\simeq\;
    \underset{\longrightarrow}{\mathrm{lim}}
    \,
    \tau_0
    \big(
    {\mathcal{G}}PrinBund_{X \times \Delta^\bullet_{\mathrm{smth}}}
    \big)
    \\
    & \;\simeq\;
    \Big(
      \tau_0
      \big(
        {\mathcal{G}}PrinBund_{ X }
      \big)
    \Big)
    \big/
    \Big(
      \tau_0
      \big(
      {\mathcal{G}}PrinBund_{X \times \Delta^1_{\mathrm{smth}}}
      \big)
    \Big)
    \\
    & \;\simeq\;
    \big(
      {\mathcal{G}}PrinBund_X
    \big)_{\sim_{\mathrm{conc}}}
  \end{aligned}
$$


$\leftrightarrows$

$\ldots$

$$
  \begin{aligned}
  & 
  2Loc_{QuillenEquivs}
  \big(
    CombinatorialModelCategories
  )
  \\
  &
  \;
  \overset{\color{purple}?}{\simeq}
  \;
  2Ho
  \big(
    Presentable \infty Categories
  \big)
  \end{aligned}
$$

\linebreak

***

\linebreak

For $\mathbf{H}$ an $\infty$-topos
and $G \in Groups(\mathbf{H})$,
one would expect that 

(1)
group objects 
$\Gamma /\!\!/ G \,\in\, \mathrm{Groups}\big( \mathbf{H}_{/\mathbf{B}G} \big)$
in the slice over the delooping of $G$

are equivalent to 

(2) group objects $\Gamma \,\in\, \mathrm{Groups}(\mathbf{H})$
equipped with an action of $G$ by group automorphisms.

A construction $(2)\Rightarrow (1)$ is in Prop. 2.102 on [p. 35](https://ncatlab.org/schreiber/files/orbi210607.pdf#page=35) of *[[schreiber:Proper Orbifold Cohomology|Proper Orbifold Cohomology]]*.

The following are some thoughts on how to go about $(1) \Rightarrow (2)$, but not conclusive yet.

The following pasting diagram shows something slightly weaker:

  \begin{tikzcd}
    &
    G 
    \ar[r]
    \ar[
      d,
      "{(e,\mathrm{id})}"{left}
    ]
    \ar[
      dr,
      phantom,
      "\mbox{\tiny\rm(d)}"
    ]
    &
    \ast
    \ar[d]
    \\
    G
    \ar[r]
    \ar[d]
    \ar[
      dr,
      phantom,
      "\mbox{\tiny\rm(d)}"
    ]
    &
    \Gamma \times G
    \ar[
      r,
      "\mathrm{pr}_1"{description}
    ]
    \ar[
      d,
      "\rho"{description}
    ]
    \ar[
      dr,
      phantom,
      "{\mbox{\tiny (c)}}"
    ]
    & 
    \Gamma
    \ar[d]
    \ar[rr]
    \ar[
      drr,
      phantom,
      "{\mbox{\tiny (b)}}"
    ]
    &&
    \ast
    \ar[d]
    \\
    \ast
    \ar[r]
    &
    \Gamma
    \ar[d]
    \ar[r]
    \ar[
      dr,
      phantom,
      "{\mbox{\tiny (b)}}"
    ]
    &
    \Gamma /\!\!/ G
    \ar[rr]
    \ar[d]
    \ar[
      drr,
      phantom,
      "\mbox{\tiny\rm(a)}"
    ]
    &&
    \mathbf{B}G
    \mathrlap{
      \;
      \simeq
      \Gamma /\!\!/ (\Gamma \rtimes G)
    }
    \ar[d]
    \\
    &
    \ast
    \ar[r]
    &
    \mathbf{B}G
    \ar[rr]
    &&
    \underset{\mathbf{B}G}{\sum} \mathbf{B} (\Gamma /\!\!/ G)
    \mathrlap{
      \;
      \simeq
      \mathbf{B}(\Gamma \rtimes G)
    }
    \ar[d]
    \\ 
    &&&&
    \mathbf{B}G
    &
    {\phantom{AAAAAAAAAA}}
  \end{tikzcd}

Here:

(a) is the homotopy pullback that exhibits $\Gamma /\!\!/ G$
as a group object in the slice over $\mathbf{B}G$;

(b) is the homotopy pullback that exhibits $\Gamma /\!\!/ G$
as the homotopy quotient of a $G$-action on $\Gamma$;

(c) is the homotopy fiber product which exhibits
the shear map equivalence of 
$\Gamma$ as a principal $G$-bundle over $\Gamma /\!\!/ G$;

(d) is a homotopy pullback implied from this by the pasting law.

While we can't seem to conclude group structure on $\Gamma$ directly, 
we see that $\Gamma \times G$ carries a group structure,
to be denoted $\Gamma \rtimes G$, whose delooping is 
the bottom right object.


Moreover, 
$G \xrightarrow{(e,\mathrm{id})} \Gamma \times G$ is
exhibited as a homomorphism of group objects.


Also, we see that 
$G \xrightarrow{(e,\mathrm{id})} \Gamma \times G \xrightarrow{\rho} \Gamma$
are $G$-equivariant maps for $G$ acting by right multiplication on itself.
This implies that $\rho$ is the given $G$-action, 

So we are beginning to see that $\Gamma \!\sslash\! G \in Groups\big( \Gamma \rtimes G\big)$ is equivalent to a  "semidirect product $\infty$-group"
$\Gamma \rtimes G$. 

But can we make explicit that the action of $G$ on $\Gamma$ is by group automorphisms? This would require constructing a homotopy fiber sequence of the form

$$
  \array{
    \mathbf{B}\Gamma
    &\longrightarrow&
    \mathbf{B}(\Gamma \rtimes G)
    \\
    && \big\downarrow
    \\
    && \mathbf{B}G
  }
$$

How to see this homotopy fiber from the above diagram (or from some other consideration)?


\linebreak
\linebreak







