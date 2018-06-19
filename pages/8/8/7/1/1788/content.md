

+-- {: .num_example #SliceCategory}
###### Example
**([[slice category]])**

Let $\mathcal{C}$ be a [[category]], and let $c \in \mathcal{C}$ be any [[object]]. Then 

1. The _[[slice category]]_ (or "[[overcategory]]") $\mathcal{C}_{/c}$ is the [[category]] whose [[objects]] are the [[morphisms]] $X \overset{f}{\to} c$ in $\mathcal{C}$, into $c$, and whose [[morphisms]] $(X_1,f_1) \to (X_2,f_2)$ are the [[morphisms]] $X_1 \overset{g}{\longrightarrow} X_2$ in $\mathcal{C}$ that make a commuting triangle (Def. \ref{CommutingDiagram}):

   $$
     f_2\circ g
     \;=\;
     f_1
     \phantom{AAAAAA}
     \array{
        X_1 
          && 
          \overset{\phantom{AA} g \phantom{AA}}{\longrightarrow} 
          &&
        X_2
        \\
        & {}_{\mathllap{f_1}}\searrow && \swarrow_{\mathrlap{f_2}}
        \\
        && c
     }
   $$

   Hence there is a canonical [[functor]] 

   $$
     \array{
       \mathcal{C}_{/c} 
       &\overset{}{\longrightarrow}& 
       \mathcal{C}
     }
   $$

   given by forgetting the morphisms to $c$.


1. The _[[coslice category]]_ (or "[[undercategory]]") $\mathcal{C}^{c/}$ is the [[category]] whose [[objects]] are the [[morphisms]] $c \overset{f}{\to} X$ in $\mathcal{C}$, out of $c$, and whose [[morphisms]] $(X_1,f_1) \to (X_2,f_2)$ are the [[morphisms]] $X_1 \overset{g}{\longrightarrow} X_2$ in $\mathcal{C}$ that make a commuting triangle (Def. \ref{CommutingDiagram}):

   $$
     f_2\circ g
     \;=\;
     f_1
     \phantom{AAAAAA}
     \array{
        && c
        \\
        & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
        \\
        X_1 
          && 
          \underset{\phantom{AA} g \phantom{AA}}{\longrightarrow} 
          &&
        X_2
     }
   $$

   Again, there is a canonical [[functor]] 

   $$
     \array{
       \mathcal{C}_{c/} 
       &\overset{}{\longrightarrow}& 
       \mathcal{C}
     }
   $$

   given by forgetting the morphisms to $c$.


=--

More generally:



+-- {: .num_example #SliceCategory}
###### Example
**([[slice category]])**

Let $\mathcal{C}$ be a [[category]], and let $c \in \mathcal{C}$ be any [[object]]. Then 

1. Then _[[slice category]]_ (or "[[overcategory]]") $\mathcal{C}_{/c}$ is the [[category]] whose [[objects]] are the [[morphisms]] $X \overset{f}{\to} c$ in $\mathcal{C}$, into $c$, and whose [[morphisms]] $(X_1,f_1) \to (X_2,f_2)$ are the [[morphisms]] $X_1 \overset{g}{\longrightarrow} X_2$ in $\mathcal{C}$ that make a commuting triangle (Def. \ref{CommutingDiagram}):

   $$
     f_2\circ g
     \;=\;
     f_1
     \phantom{AAAAAA}
     \array{
        X_1 
          && 
          \overset{\phantom{AA} g \phantom{AA}}{\longrightarrow} 
          &&
        X_2
        \\
        & {}_{\mathllap{f_1}}\searrow && \swarrow_{\mathrlap{f_2}}
        \\
        && c
     }
   $$

   There is a canonical [[functor]] 

   $$
     \array{
       \mathcal{C}_{/c} 
       &\overset{}{\longrightarrow}& 
       \mathcal{C}
     }
   $$

   given by forgetting the morphisms to $c$.


1. The _[[coslice category]]_ (or "[[undercategory]]") $\mathcal{C}^{c/}$ is the [[category]] whose [[objects]] are the [[morphisms]] $c \overset{f}{\to} X$ in $\mathcal{C}$, out of $c$, and whose [[morphisms]] $(X_1,f_1) \to (X_2,f_2)$ are the [[morphisms]] $X_1 \overset{g}{\longrightarrow} X_2$ in $\mathcal{C}$ that make a commuting triangle (Def. \ref{CommutingDiagram}):

   $$
     f_2\circ g
     \;=\;
     f_1
     \phantom{AAAAAA}
     \array{
        && c
        \\
        & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
        \\
        X_1 
          && 
          \underset{\phantom{AA} g \phantom{AA}}{\longrightarrow} 
          &&
        X_2
     }
   $$

   Again, there is a canonical [[functor]] 

   $$
     \array{
       \mathcal{C}^{c/} 
       &\overset{}{\longrightarrow}& 
       \mathcal{C}
     }
   $$

   given by forgetting the morphisms to $c$.


=--
