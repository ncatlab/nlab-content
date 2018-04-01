
[[HiggsPotentials.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsPotentials.png" width="600">


[[HiggsVacuumStability.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStability.png" width="600">

[[HiggsVacuumStabilityII.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStabilityII.png" width="400">


Consider the map

$$
  \array{
    \Sigma^\infty_{S^3}( S^4/\!/S^1 )
    &
      \overset{
         \Sigma^\infty_{S^3}(\eta)
      }{\longrightarrow}&
    \Sigma^\infty_{S^3}( Cyc(S^4) )  
  }
$$

{#AClaim}**Claim**

The map $\Sigma^\infty_{S^3}(\eta)^\ast$ does not have the elements
$\omega_{\bullet \geq 8}$ in its image.

**Proof**

Suppose on the contrary that $\omega_8$ were in the image. Its pre-image would have to be of the form

$$
  \{\omega_8\}
  \overset{
    \Sigma^\infty_{S^3}(\eta)^\ast
  }{\longleftarrow}
  \left\{
    \begin{aligned}
      & \phantom{+} a_1 \; \omega_6 \wedge \omega_2
      \\
      & + 
      a_2 \; \omega_4 \wedge \omega_2 \wedge \omega_2
      \\
      & +
      a_4 \; \omega_2 \wedge \omega \wedge \omega_2 \wedge \omega_2
    \end{aligned}
  \right\}
$$

for some $a_1, a_2, a_4 \in \mathbb{R}$.

(Here $\omega_4 \wedge \omega_4$ does not appear because in the minimal dg-module for the Vigu&eacute;-model this is identified with $2 \omega_6 \wedge \omega_4$. But even without this identification we could include $\omega_4 \wedge \omega_4$ and the remainder of the argument would still go through in the same way. )

But then the respect for the differentials implies the top arrow in the following diagram

$$
  \array{
  \{h_3 \wedge \omega_6\}
  &
  \overset{ \Sigma^\infty_{S^3}(\eta)^\ast }{\longleftarrow}
  &
  \left\{
    \begin{aligned}
      & \phantom{+} a_1 \; h_3 \wedge \omega_4 \wedge \omega_2
      \\
      & + 
      a_2 \; h_3 \wedge \omega_2 \wedge \omega_2 \wedge \omega_2
    \end{aligned}
  \right\}
    \\
    {}^{\mathllap{d}}\uparrow
    &&
    \uparrow^{d}
    \\
    \{\omega_8\}
    &
    \overset{
      \Sigma^\infty_{S^3}(\eta)^\ast
    }{\longleftarrow}
    &
    \left\{
      \begin{aligned}
        & \phantom{+} a_1 \; \omega_6 \wedge \omega_2
        \\
        & + 
        a_2 \; \omega_4 \wedge \omega_2 \wedge \omega_2
        \\
        & +
        a_4 \; \omega_2 \wedge \omega \wedge \omega_2 \wedge \omega_2
      \end{aligned}
    \right\}
  }
$$

and by the respect for the $Sym(h_3)$-module structure this would imply that

$$
  \{\omega_6\}
  \overset{
    \Sigma^\infty_{S^3}(\eta)^\ast
  }{\longleftarrow}
  \left\{
    \begin{aligned}
      & \phantom{+} a_1 \; \omega_4 \wedge \omega_2
      \\
      & + 
      a_2 \; \omega_2 \wedge \omega_2 \wedge \omega_2
    \end{aligned}
  \right\}
$$

Applying this same kind of argument again, it would follow that

$$
  \{\omega_4\}
  \overset{
    \Sigma^\infty_{S^3}(\eta)^\ast
  }{\longleftarrow}
  \left\{
    \begin{aligned}
      & \phantom{+} a_1 \; \omega_2 \wedge \omega_2
    \end{aligned}
  \right\}
$$

But this is impossible, because the differential on $\omega_2 \wedge \omega_2$ vanishes, while that on $\omega_4$ does not. 


$$
  \array{
    \{h_3 \wedge \omega_2\}
    &&
    \{0\}
    \\
    {}^{\mathllap{d}}\uparrow
     &&
    \uparrow^{\mathrlap{d}}
    \\
    \{\omega_4\}
    &
    \overset{
      \Sigma^\infty_{S^3}(\eta)^\ast
    }{\longleftarrow}
    &
    \left\{
      \begin{aligned}
        & \phantom{+} a_1 \; \omega_2 \wedge \omega_2
      \end{aligned}
    \right\}
  }
$$


Hence we have a proof by contradiction showing that $\omega_8$ is not in fact in the image.

The argument for all the $\omega_{\bullet \geq 10}$ is analogous: The point is that the would-be pre-image in each case would necessarily consist of sums of wedge products of elements of degree $\leq 6$; and by iteratively using the dg-module homomorphism property these eventually "decay" into a wedge product of $\omega_2$-s. On the latter the differential vanishes, while on the corresponding would-be image element it does not.



**Claim**

The map $\Sigma^\infty_{S^3}(\eta)$
pulls back the generators $\omega_2, \omega_4, \omega_6$ of the Vigu&eacute; model to the generators of the same name in the Roig model, possibly up to addition of a multiple of $\omega_2 \wedge \omega_2 \wedge \omega_2$

$$
  \left\{
    \omega_2, \omega_4, \omega_6
  \right\}
   \overset{\Sigma^\infty_{S^3}(\eta)^\ast}{\longleftarrow}
  \left\{
    \omega_2, \omega_4, \omega_6 + a\; \omega_2 \wedge \omega_2 \wedge \omega_2
  \right\}
$$

for $a \in \mathbb{R}$.



**Sketch of proof**.

Recall the right base change adjunction (details are [here](https://ncatlab.org/schreiber/show/Super+Lie+n-algebra+of+Super+p-branes#GeneralReduction))

$$
  \mathbf{H}
  \underoverset
    {\underset{Cyc(-) = \mathcal{L}(-)/\!/ S^1}{\longrightarrow}}
    {\overset{Ext(-) = hofib}{\longleftarrow}}
    {\bot}
  \mathbf{H}_{/B S^1}
$$

The unit

$$
  X \overset{\eta}{\longrightarrow} Cyc(Ext(X))
$$

sends a point in $X$ to the loop which winds at constant speed around the fiber over this point.

What is the counit? To see this, observe that

$$
  Ext(Cyc(X)) = \mathcal{L}(X)
$$

is the free loop space.

Hence the counit ought to be the base point evaluation

$$
  Ext(Cyc(X)) = \mathcal{L}(X) \overset{ev_{pt}}{\longrightarrow} X
$$

This implies with the zig-zag-identity that $Ext(\eta)$ is the identity on basepoints:

$$
  \array{
    Ext(X) &\overset{Ext(\eta)}{\longrightarrow}& \mathcal{L}(Ext(X))
    \\
    & {}_{\mathllap{id}}\searrow & \downarrow^{\mathrlap{ ev_{pt} }}
    \\
    && Ext(X)
  }
$$

Applied to the case that $X = S^4$ with

$$
  Ext(\eta)
  \;\colon\;
  S^4 \longrightarrow \mathcal{L}(S^4)
$$

this should say that 

$$
  \Sigma^\infty_{S^3}(\eta)^\ast
$$

is the identity on the generator $\omega_4$ of $H^4(S^4)$:

$$
  \{\omega_4\}
  \overset{
    \Sigma^\infty_{S^3}(\eta)^\ast
  }{\leftarrow}
  \{\omega_4\}
$$

But then the respect for the differential

$$
  \array{
    \{h_3 \wedge \omega_2\}
    &&
    \{h_3 \wedge \omega_2\}    
    \\
    {}^{\mathllap{d}}\uparrow && \uparrow^{\mathrlap{d}}
    \\
    \{\omega_4\}
    &
      \overset{ \Sigma^\infty_{S^3}(\eta)^\ast }{\leftarrow}&
    \{\omega_4\}
  }
$$

together with the $Sym(h_3)$-dg-module property
implies that 

$$
  \{\omega_2\}
  \overset{
     \Sigma^\infty_{S^3}(\eta)^\ast
  }{\leftarrow}
  \{\omega_2\}
$$

Similarly the respect for the differential


$$
  \array{
    \{h_3 \wedge \omega_4\}
    &
      \overset{
        \Sigma^\infty_{S^3}(\eta)^\ast
      }{
        \leftarrow
      }
    &
    \{h_3 \wedge \omega_4\}    
    \\
    {}^{\mathllap{d}}\uparrow && \uparrow^{\mathrlap{d}}
    \\
    \{\omega_6\}
    &&
    \{\omega_6\}
  }
$$

implies that 

$$
  \{\omega_6 + closed\}
    \overset{
      \Sigma^\infty_{S^3}(\eta)^\ast
    }{\leftarrow}
  \{\omega_6\}
$$

The only closed element of degree 6 in the model for $S^4/\!/S^1$ is $\omega_2 \wedge \omega_2 \wedge \omega$, up to a scale.


**end of sketchy sketch**

#<span style="display: block; text-align: center;">Title</span>#


