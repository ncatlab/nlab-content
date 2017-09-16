#Idea#

Just as [[functor|functors]] go between [[category|categories]], natural transformations go between functors.

#Definition#

Given categories $C$ and $D$ and functors $F, G:C \to D,$ a _natural transformation_ $\alpha:F \Rightarrow G$ 

$$
  \array{
    \\
    & \nearrow \searrow^F
    \\
    C
    &\Downarrow^{\alpha}&
    D
    \\
    & \searrow \nearrow_G
  }
$$
assigns to every object $x$ in $C$ a morphism 
$\alpha_x:F(x) \to G(x)$ in $D$ such that for any morphism $f:x \to y$ in $C$, the following diagram commutes in $D$:

\[ 
  \array{ 
    F(x) 
    & 
    \stackrel{F(f)}{\to} 
    & 
    F(y) 
    \\ 
    \alpha_x\downarrow 
    && 
    \downarrow \alpha_y 
    \\ G(x) 
    & 
    \stackrel{G(f)}{\to} & G(y) 
  }
  \,. 
\] 

Natural transformations between functors $C \to D$ compose in the obvious way
and functors $F : C \to D$ with natural transformations between them form the [[functor category]] 
$$
  [C,D]
$$ 
(the notation alludes to the fact that this makes [[Cat]] a [[closed monoidal category]]).

There is also a horizontal composition of natural transformations, which makes [[Cat]] a [[2-category]].