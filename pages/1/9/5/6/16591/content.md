

#Contents#
* table of contents
{:toc}

## Definition

### Traditional

In the original sense, a _homothety_ is a [[function]] from a [[Euclidean space]] to itself, which is a dilation centered at a given point of the Euclidean space. Hence a homothety of a [[Cartesian space]] $\mathbb{R}^n$ is a function $\mathbb{R}^n \to \mathbb{R}^n$ given by multiplication with some $\kappa \in \mathbb{R}-\{0\}$.

Such dilations are [[linear functions]] $\kappa \in GL(\mathbb{R}^n)$ which commute, in particular, with all [[orthogonal group|orthogonal transformations]] on $\mathbb{R}^n$. In view of this, in the context of [[Cartan geometry]] one says more generally that given a [[vector space]] $V$ and a [[group]] [[homomorphism]] 
$\phi \colon G \longrightarrow  GL(V)$ to the [[general linear group]] of $V$, then a homothety of this data is an element $\kappa \in GL(V)$ such that for all $g \in G$ one has

$$
  \kappa \circ \phi(g) = \phi(g) \circ \kappa
  \,.
$$

Given then two [[G-structures]] on a [[smooth manifold]] modeled on $V$, then a homothety between these $G$-structures is a homothety of the local models which transforms the two $G$-structures into each other.

### General abstract

This has a succinct diagrammatic formulation in the formulation of $G$-structures on $V$-manifolds in [[differential cohesion]] (see at _[differential cohesion -- G-Structures](differential+cohesion#structures)_). Write

$$
  G \mathbf{Struc} \colon \mathbf{B}G\longrightarrow \mathbf{B}GL(V)
$$

for the [[delooping]] of the group homomorphism defining the kind of $G$-structure. Then a homothety is simply a [[homotopy]] from $G\mathbf{Struc}$ to itself

$$
  \array{
    & & \mathbf{B}G
    \\
    & \swarrow && \searrow^{\mathrlap{G\mathbf{Struc}}}
    \\
    & {}_{\mathllap{G\mathbf{Struc}}}\searrow &\swArrow_{\simeq}& \swarrow
    \\
    && \mathbf{B}GL(V)
  }
  \,.
$$

Accordingly, for $\mathbf{g}_1, \mathbf{g}_2 \colon \tau_X\longrightarrow G \mathbf{Struc}$ two $G$-structures on a $V$-manifold

$$
  \array{
     X && \longrightarrow && \mathbf{B}G
     \\
     & {}_{\mathllap{\tau_X}}\searrow &\swArrow_{\mathrlap{\mathbf{g}_i}}& \swarrow_{\mathrlap{G}\mathbf{Struc}}
     \\
     && \mathbf{B}GL(V)
  }
$$

then a homothety from $\mathbf{g}_1$ to $\mathbf{g}_2$ is a homotopy of homotopies of the form


$$
  \array{
     X && \longrightarrow && \mathbf{B}G
     \\
     & {}_{\mathllap{\tau_X}}
       \searrow 
     &\swArrow_{\mathrlap{\mathbf{g}_1}}& 
     \swarrow_{\mathrlap{G\mathbf{Struc}}} 
     &\swArrow_{\simeq}& 
      \searrow^{\mathrlap{G\mathbf{Struc}}}
     \\
     && \mathbf{B}GL(V) && =& \mathbf{B}GL(V)
  }
  \;\;\;\;\;\;
   \stackrel{\simeq}{\Rightarrow}
  \;\;\;\;\;\;
  \array{
     X && \longrightarrow && \mathbf{B}G
     \\
     & {}_{\mathllap{\tau_X}}\searrow &\swArrow_{\mathrlap{\mathbf{g}_2}}& \swarrow_{\mathrlap{G\mathbf{Struc}}} 
     \\
     && \mathbf{B}GL(V) 
  }
$$

## References

* Encyclopedia of Mathematics, _[Homothety](http://www.encyclopediaofmath.org/index.php/Homothety)_

[[!redirects homotheties]]