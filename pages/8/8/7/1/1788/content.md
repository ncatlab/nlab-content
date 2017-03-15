
+-- {: .num_prop}
###### Proposition

Let $f_\bullet \colon V_\bullet \longrightarrow W_\bullet$
be a [[chain map]] between [[chain complexes]].

For $n \in \mathbb{N}$, define the abelian group

$$
  (im_{n+1}(f))_n
    \coloneqq      
   \underset{v_{n-1} \in V_{n-1}}{\oplus}
    \left\{
      f_n(v_n) \vert \partial v_n = v_{n-1}
    \right\}
$$

and consider the following diagram of [[abelian groups]]:

$$
  \array{
    \vdots && \vdots && \vdots
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
     &&
    \downarrow^{\mathrlap{\partial_{W}}}    
     &&
    \downarrow^{\mathrlap{\partial_{W}}}    
    \\
    V_{n+2} 
      &\overset{f_{n+2}}{\longrightarrow}&
    W_{n+2}
      &\overset{=}{\longrightarrow}&
    W_{n+2}
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
     &&
    \downarrow^{\mathrlap{\partial_{W}}}    
     &&
    \downarrow^{\mathrlap{\partial_{W}}}    
    \\
    V_{n+1} 
      &\overset{f_{n+1}}{\longrightarrow}&
    W^{res}_{n+1}
      &\overset{}{\longrightarrow}&
    W_{n+1}
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
     &&
    \downarrow^{\mathrlap{\partial_W}}
     &\text{(pb)}&
    \downarrow^{\mathrlap{\partial_{W}}}    
    \\
    V_n 
      &\overset{f}{\longrightarrow}& 
    im_{n+1}(f)_n
     &\hookrightarrow&
    W_n
    \\
    \downarrow^{\mathrlap{\partial_V}}
    &&
    \downarrow
    &&
    \downarrow^{\mathrlap{\partial_W}}
    \\
    V_{n-1} 
      &\overset{=}{\longrightarrow}& 
    V_{n-1} 
      &\overset{f_{n-1}}{\longrightarrow}&
    W_{n-1}
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
    &&
    \downarrow^{\mathrlap{\partial_{V}}}
    &&
    \downarrow^{\mathrlap{\partial_W}}
    \\
    V_{n-2} 
      &\overset{=}{\longrightarrow}& 
    V_{n-2} 
      &\overset{f_{n-2}}{\longrightarrow}&
    W_{n-2}
    \\
    \\
    \downarrow^{\mathrlap{\partial_{V}}}
    &&
    \downarrow^{\mathrlap{\partial_{V}}}
    &&
    \downarrow^{\mathrlap{\partial_W}}
    \\
    \vdots && \vdots && \vdots
  }
$$

where $W_{n+1}^{res}$ is the [[pullback]] of $W_{n+1}$ along the canonical inclusion of $(im_{n+1}(f))_n$, as shown.

Here the middle vertical sequence is a chain complex $im_{n+1}(f)$, and hence the diagram gives a factorization of $f_\bullet$ into two chain maps

$$
  f_\bullet
   \;\colon\;
  V_\bullet \longrightarrow im_{n+1}(f)_\bullet \longrightarrow W_\bullet
  \,.
$$

This is a model for the [[n-image|(n+1)-image factorization]] of $f$ in that on [[homology groups]] the following holds:

1. $H_{\bullet \lt n}(V) \overset{\simeq}{\to} H_{\bullet \lt n}(im_{n+1}(f))$ are [[isomorphisms]];

1. $H_n(V) \to H_n(im_{n+1}(f)) \hookrightarrow H_n(W)$ is the [[image|image factorization]] of $H_n(f)$;

1. $H_{\bullet \gt n}(im_{n+1}(f)) \overset{\simeq}{\to} H_{\bullet \gt n}(W)$   are [[isomorphisms]]


=--

