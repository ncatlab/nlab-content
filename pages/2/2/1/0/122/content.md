#Idea#

Just as [[functor|functors]] go between [[category|categories]], natural transformations go between functors.

#Definition#

Given categories $C$ and $D$ and functors $F, G:C \to D,$ a _natural transformation_ $\alpha:F \to G$ assigns to every object $x$ in $C$ a morphism $\alpha_x:Fx \to Gx$ in $D$ such that for any morphism $f:x \to y$ in $C$, the following diagram commutes in $D$:

\[ \array{ Fx & \stackrel{Ff}{\to} & Fy \\ \alpha_x\downarrow && \downarrow \alpha_y \\ Gx \stackrel{Gf}{\to} } \] 