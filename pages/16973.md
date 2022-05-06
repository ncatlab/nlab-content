
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea


The _real Hopf fibration_ is the [[fibration]]


$$
  \array{
     S^0 &\hookrightarrow& S^1
     \\
     && \downarrow^{\mathrlap{p_{\mathbb{R}}}}
     \\
     && S^1
  }
$$

of the [[1-sphere]] over itself with [[fiber]] the [[0-sphere]], which is induced via the [[Hopf construction]] from the product operation 

$$
  \mathbb{R} \times \mathbb{R} \stackrel{(-)\cdot (-)^{-1}}{\longrightarrow}
  \mathbb{R}
$$

on the [[real numbers]]. 

This may also be understood as the [[Spin(2)]]-[[double cover]] of [[SO(2)]].

## Realizations

Here are different but equivalent ways of realizing this explicitly:

### Via projective space

If the domain $S^1$ is regarded as the [[unit sphere]] $\{(x,y)  | {\vert x\vert}^2 + {\vert y\vert}^2 = 1\}$ in $\mathbb{R}\times \mathbb{R}$ and the codomain $S^1$ is regarded as the real [[projective space]], then $p$ is given simply by

$$
  p \colon (x,y) \mapsto [x;y] = [x/y; 1]
  \,,
$$
One can view the real Hopf fibration as the boundary of a [[Möbius strip]], which is the non-trivial double cover of the circle.

As an element in the first ([[stable homotopy group|stable]]) [[homotopy group]] [[homotopy groups of spheres|of spheres]] $\pi_1(S^1) \simeq \mathbb{Z}$, the real Hopf fibration represents $p_{\mathbb{R}} = 2$.


### Via join construction
  {#ViaJoinConstruction}

We spell out the real Hopf fibration realized as the [[Hopf construction]] 

$$
  \array{
     X \ast X 
       &\overset{H_{\mathbb{R}}}{\longrightarrow}&
     \Sigma X
     \\
     =
     &&
     =
     \\
     (X \times [0,1] \times X)_{/\sim}
     &&
     (X \times [0,1])_{/\sim}
     \\
     (x,t,y) &\mapsto& \big( f(x,y), t\big) 
  }
$$

(as defined [there](Hopf+construction#Definition)) on 

$$
  X 
    \coloneqq 
  \mathbb{Z}/2
$$

regarded with its [[cyclic group]]-[[structure]]

$$
  \array{
    (\mathbb{Z}/2) \times (\mathbb{Z}/2)
      &\overset{f}{\longrightarrow}&
    (\mathbb{Z}/2)
    \\
    (x,y) &\mapsto& x + y 
  }
$$

Here the [[equivalence relation]] for the [[suspension]] $\Sigma X = (X \times [0,1])_{/\sim}$ on the right is

$$
  (x_1,0) \sim (x_2,0) \;\,,\;\;  (x_1, 1) \sim (x_2, 1) \;\;\; \forall x_1,x_2 \in X
$$

while the [[equivalence relation]] for the [[join of topological spaces|join]] $X\ast X = (X \times [0,1] \times X)_{/\sim}$ on the left is

$$
  (x, 0, y_1) \simeq (x,0,y_2) \;\;,\;\; (x_1,1,y) \sim (x_2, 1, y)
  \,.
$$


So on the left we have a [[circle]] $S^1$ realized by gluing four copies of the [[interval]] $[0,1]$ labeled in $\mathbb{Z}/2 \times \mathbb{Z}/2$ by identifying them pairwise at $0 \in [0,1]$ and pairwise _the other way_ at $1 \in [0,1]$. while on the right we have a [[circle]] $S^1$ realized by  two copies, labeled by $\mathbb{Z}/2$. 

$$
  S^1 \longrightarrow S^1
  \,.
$$

A full path around the circle on the left is given, in terms of the above [[coordinates]] in $[0,1] \times (\mathbb{Z}_2 \times \mathbb{Z}_2)$, by

$$
  \array{
   (0,(0,0)) 
    &\rightsquigarrow&
   (1,(0,0))  
   \\
   &&
    \sim 
   \\
   &&
   (1,(1,0)) 
    &\rightsquigarrow&
   (0,(1,0)) 
   \\
   &&&&
     \sim 
   \\
    &&&&
    (0,(1,1)) 
    &\rightsquigarrow&
    (1,(1,1)) 
    \\
    &&&&&&
      \sim 
    \\
    &&&&&&
     (1,(0,1))
    & \rightsquigarrow&
     (0,(0,1)) 
    \\
    &&&&&&&&
       \sim 
    \\
    &&&&&&&&
     (0,(0,0)) 
  }
$$

As we map this path over to the other $S^1$ by adding up the two coordinate labels in $\mathbb{Z}/2$, we trace out the following path on the right, with coordinates in $[0,1] \times \mathbb{Z}/2$:

$$
  \array{
   (0,(0+0 = 0)) 
    &\rightsquigarrow&
   (1,(0 + 0 = 0)) 
   \\
   &&
    \sim 
   \\
   &&
   (1,(1 + 0 = 1)) 
    &\rightsquigarrow&
   (0,(1 + 0 = 1)) 
   \\
   && &&
     \sim 
   \\
    && &&
    (0,(1+1 = 0)) 
    &\rightsquigarrow&
    (1,(1+1 = 0)) 
    \\
    && && &&
      \sim 
    \\
    && && &&
     (1,(0 + 1 = 1))
      &\rightsquigarrow&
     (0,(0 + 1 = 1)) 
    \\
    && && && &&
       \sim 
    \\
    && && && && 
     (0,(0 + 0 = 0)) 
  }
$$

That's twice around the circle on the right, for once on the left, manifestly showing that the real Hopf fibration is the non-trivial [[double cover]] of the [[circle]] by itself:

$$
  S^1 \overset{\cdot 2}{\longrightarrow} S^1
  \,.
$$




## Related concepts

* [[complex Hopf fibration]]

* [[quaternionic Hopf fibration]]

* [[octonionic Hopf fibration]]

