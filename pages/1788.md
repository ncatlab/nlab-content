

\begin{tikzcd}[row sep=-6pt, column sep=14pt]
  123
  \ar[rrrr,-]
  \ar[ddddd,-]
  \ar[ddrrr,-]
  &&
  &&
  132
  \ar[ddddd,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  &&&
  \scalebox{.8}{$321$}
  \ar[dddr,-]
  \\
  &
  \scalebox{1.2}{231}
  \ar[ddl,-]
  \ar[uuurrr,-, crossing over]
  \ar[urr,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  213
  \ar[rrrr,-]
  &&&&
  312
\end{tikzcd}




$$
  \array{
    &
    123
    \\
    &
    \swarrow \downarrow \searrow
    \\
    213 & 132 & 321 
    \\
    & 
    \searrow \downarrow \swarrow
    \\   
    & 
    312
  }
$$

$\,$

$\,$

$$
  \array{
    & \vdots
    \\
    213 & 132 & 321 
    \\
    & 
    \searrow \downarrow \swarrow
    \\   
    & 
    231
  }
$$


This main result is corollary 7.6.13 of [Cisinski 20](#Cisinski20). Model categories are (∞,1)-categories with weak equivalences and fibrations as defined in [Cisinski Def. 7.4.12](#Cisinski20).

We spell out a proof for the special case that $\mathcal{C}$ carries the [[extra structure]] of a [[simplicial model category]]:

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


=--


