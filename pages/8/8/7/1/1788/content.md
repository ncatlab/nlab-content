
Given $\alpha \,G\, \xrightarrow{\;} Aut_{Grp}(\Gamma)$
as above, consider a [[subgroup]] $H \subset G$.

\begin{proposition}
The set of crossed homomorphisms $H \to \Gamma$, with respect to the restricted action of $H$ on $\Gamma$, carries a [[group action]] of the [[normalizer subgroup]] $N_G(H) \,\subset\, G$,
given by
$$
  \array{
    N_G(H) \times CrsHom(H,\,G)
    &\xrightarrow{\;\;}&
    CrsHom(H,\,G)
    \\
    (n, \phi)
    &\mapsto&
    \phi_{n}
    \mathrlap{
    \;\coloneqq\;
    \alpha(n)
    \Big(
      \phi
      \big(
        n^{-1} \cdot (-) \cdot n
      \big)
    \Big) 
    }
  }
$$
Moreover, on crossed-conjugation classes of crossed homomorphisms, hence on first non-abelian group cohomology, this action descends to an action of the [[Weyl group]] $W_G(H) \coloneqq N_G(H)/H$:
$$
  H^1_{Grp}(H,\,\Gamma)
  \;\;\;
  \in
  \;
  W_G(H) Act(Sets)
  \,.
$$
\end{proposition}
\begin{proof}
For the first statement:
It is clear that this is a group action if only $\phi_n$ is indeed a crossed homomorphism. This follows by a direct computation: 
$$
  \begin{array}{lll}
    \phi_n( h_1 \cdot h_2 )
    & 
    \;=\;
    \alpha(n)
    \Big(
      \phi
      \big( 
        n^{-1} \cdot h_1 \cdot h_2 \cdot n 
      \big)
    \Big)
    &
    \text{definition of}\; \phi_n
    \\
    &
    \;=\;
    \alpha(n)
    \Big(
      \phi
      \big( 
        n^{-1} \cdot h_1 \cdot n \cdot n^{-1} \cdot h_2 \cdot n 
      \big)
    \Big)
    & 
    \text{group property of}\; N_G(H) \subset G
    \\
    & \;=\;
    \alpha(n)
    \Big(
      \phi
      \big( 
        n^{-1} \cdot h_1 \cdot n
      \big)
      \cdot
      \alpha(n^{-1} \cdot h_1 \cdot n)
      \big(
        \phi( n^{-1} \cdot h_2 \cdot n )
      \big)
    \Big)
    & 
    \text{crossed homomorphism property of} \; \phi
    \\
    & \;=\;
    \alpha(n)
    \Big(    
      \phi
      \big( 
        n^{-1} \cdot h_1 \cdot n  
      \big)
    \Big)
      \cdot
    \alpha(h_1 \cdot n)
    \Big(
      \phi\big( n^{-1} \cdot h_2 \cdot n \big)
    \Big)    
    &
    \text{action property of} \; \alpha
    \\
    & \;=\;
    \alpha(n)
    \Big(    
      \phi
      \big( 
        n^{-1} \cdot h_1 \cdot n  
      \big)
    \Big)
      \cdot
    \alpha(h_1)
    \bigg(
      \alpha(n)
      \Big(
        \phi\big( n^{-1} \cdot h_2 \cdot n \big)
      \Big)    
    \bigg)
    &
    \text{action property of} \; \alpha
    \\
    & \;=\;
    \phi_n(h_1)
    \cdot
    \alpha(h_1)
    \big(
      \phi_n(h_2)
    \big)
    &
    \text{definition of}\; \phi_n
    \mathrlap{\,.}
  \end{array}
$$

To see that this action descends to group cohomology, we need to show for 

$$
  \phi'(-)
  \;=\;
  \gamma^{-1} \cdot \phi(-) \cdot \alpha(-)(\gamma)
$$

a crossed conjugation, that there exists a crossed conjugation between $\phi'_n$ and $\phi_n$. The following direct computation shows that this is given by crossed conjugation with $\alpha(n)(\gamma)$:

$$
  \begin{array}{lll}
    \phi'_n(h)
    & 
    \;=\;
    \alpha(n)
    \Big(
      \gamma^{-1} 
        \cdot 
      \phi\big( n^{-1} \cdot h \cdot n \big) 
      \cdot 
      \alpha
        \big( n^{-1} \cdot h \cdot n \big)
        (\gamma)
    \Big)
    &
    \text{assumption with definition of} \; \phi_n
    \\
    & 
    \;=\;     
    \alpha(n)
    \big(
      \gamma^{-1} 
    \big)
      \cdot 
    \alpha(n)
    \Big(
      \phi\big( 
        n^{-1} \cdot h \cdot n 
      \big) 
    \Big)
    \cdot 
    \alpha(h)
    \Big(
      \alpha(n)(\gamma)
    \Big)
    &
    \text{action property of} \; \alpha
    \\
    & \;=\;
    \big(
      \alpha(n)(\gamma)
    \big)^{-1}
      \cdot
    \phi_n(h)
      \cdot
    \alpha(h)
    \big(
      \phi(n)(\gamma)
    \big)
    &
    \text{definition of} \; \phi_n
    \,.
  \end{array}
$$ 

To conclude, we need to show that 
for $n \in H \subset N(H)$ there is a crossed conjugation between $\phi_n$ and $\phi$. The following direct computation shows that this is given by crossed conjugation with $\phi(n)$ (which is indeed defined, by the assumption that $n \in H$):
$$
  \begin{array}{lll}
    \phi_n(h)
    &
    \;=\;
    \alpha(n)
    \Big(
      \phi
      \big(
        n^{-1} \cdot h \cdot n
      \big)
    \Big)
    & 
    \text{definition of} \; \phi_n
    \\
    & 
    \;=\;
    \alpha(n)
    \bigg(
      \phi(n^{-1})
      \cdot
      \alpha(n^{-1})
      \Big(
         \phi(h)
         \cdot
         \alpha(h)
         \big(
           \phi(n)
         \big)
      \Big)
    \bigg)
    &
    \text{crossed homomorphism property of} \; \phi
    \\
    & \;=\;
    \alpha(n)
    \big(
      \phi(n^{-1}) 
    \big)
    \cdot
    \phi(h)
    \cdot
    \alpha(h)
    \big(
      \phi(n)
    \big)
    &
    \text{action property of} \; \alpha
    \\
    & \;=\;
    \big(
      \phi(n)
    \big)^{-1}
    \cdot
    \phi(h)
    \cdot
    \alpha(h)
    \big(
      \phi(n)
    \big)
    &
    \text{crossed homomorphism property of} \; \phi
    \mathrlap{\,.}
  \end{array}
$$
\end{proof}

\linebreak

Let $\phi \;\colon\; G \xrightarrow{\;} \Gamma$ be a [[crossed homomorphism]], hence equivalently a plain group homomorphism
$(\phi(-),\,(-)) \,\colon\, G \xrightarrow{\;} \Gamma \rtimes G$.
Say that another crossed homomorphism $\phi'$ is nearby if it is so as a plain homomorphism $(\phi'(-),(-))$. 

Then the above theorem says that there is an element $(\gamma,\,h) \,\in\, \Gamma \rtimes G$ such that

$$
  \big(
    \phi'(g),\,g
  \big)
  \;\;
  =
  \;\;
  \big(
    \gamma, \, h
  \big)^{-1}
  \cdot
  \big(
    \phi'(g),\,g
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)
  \,.
$$

In order for such a conjugation to be a crossed conjugation of the original morphism, we need $h = \mathrm{e}$. 

Notice that we know already that $h \in C(G)$ is in the [[center of a group|center]] of $G$, since the projection of both sides of the equation to $G$ must be the identity, by construction of crossed homomorphisms.

Hence the further conjugation of the above equation by $\big(\mathrm{e},\,h^{-1}\big)$ yields:

$$
  \Big(
    \alpha(h^{-1})
    \big(
      \phi'(g),\, g
    \big)
  \Big)
  \;\;
  =
  \;\;
  \big(
    \mathrm{e},\, h 
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)^{-1}
  \cdot
  \big(
    \phi'(g),\,g
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)
  \cdot
  \big(
    \mathrm{e},\, h^{-1} 
  \big)
  \,.
$$

Therefore, if the action of $G$ on $\Gamma$ restricts along the inclusion $C(G) \xhookrightarrow{\;} G$ to the [[trivial action]], then

$$
  \big(
    \gamma, \, h
  \big)
  \cdot
  \big(
    \mathrm{e},\, h^{-1} 
  \big)
  \;\;
  =
  \;\;
  \big(
    \gamma, \, \mathrm{e}
  \big)  
$$

corresponds to a crossed conjugation

$$
  \phi'(-) \;=\;  \gamma^{-1} \cdot \phi(-) \cdot \alpha(-)(\gamma)
  \,.
$$

[[CrossedHomomorphismsAsSlicedFunctors210831.jpg:file]]

\begin{tikzcd}
      &&
      \mathbf{B}(\Gamma \rtimes G)
      \ar[
        d,
        "\mathbf{B}\mathrm{pr}_2"
      ]
      \\
      \mathbf{B}G
      \mathrlap{\,.}
      \ar[
        rr,-,
        shift right=1pt
      ]
      \ar[
        rr,-,
        shift left=1pt
      ]
      \ar[
        urr,
        dashed,
        bend left=30,
        "\ "{right, name=s}
      ]
      \ar[
        urr,
        dashed,
        bend right=10,
        "\ "{left, name=t}
      ]
      &&
      \mathbf{B}G
      %
      \ar[
        from=s,
        to=t,
        dashed,
        Rightarrow
      ]
\end{tikzcd}



\begin{proposition}
  [[internalization|Internal to]] some 
  ambient [[category]] $\mathcal{C}$
  with [[finite limits]], let 

  * $G \,\in\, Grp(\mathcal{C})$ be a [[group object]], 
  * $P \,\in\, G Act(\mathcal{C})$ an [[action object]],
  * $(P \to X) \,\in\, G PsTor(\mathcal{C}_{/X})$ a [[formally principal bundle]].

Then the following are equivalent:

1. $P \to X$ is the $G$-[[quotient]] [[coprojection]];

1. $P \to X$ is an [[effective epimorphism]].

***

\linebreak

- $G$-fixed-wise contractibility of $Maps(\mathbf{E}G,\mathbf{E}\Gamma)$ follows from $G$-equivariant contraction of $\mathbf{E}\Gamma$

- the universal equivariant principal $\infty$-bundle is $\ast \longrightarrow Maps(\mathbf{E}G, \mathbf{B}\Gamma)$ and the point is that the base space is pointed, but no longer pointed connected -- but the universal bundle is still that point inclusion (meaning that all other fibers are empty, as admissible for a formally principal bundle)


\linebreak

***

\end{proposition}
\begin{proof}
  The first condition is equivalent to 
  $$
    P \times_X P \rightrightarrows P \to X
  $$
  being a [[coequalizer]], the second to
  $$
    P \times G \rightrightarrows P \to X
  $$
  being a coequalizer. But the pseudo-principality condition 
  says that we have an [[isomorphism]] (the [[shear map]])
  $$
    P \times_X P \simeq P \times G
  $$
  which identifies these two [[diagrams]].
\end{proof}


\begin{tikzcd}
  \mathrm{Grpd}
  \ar[
    rr,
    shift left=26pt,
    "{
      \pi_0
    }"{description}
  ]
  \ar[
    rr,
    "{
      (-)_0
    }"{description}
  ]
  &&
  \mathrm{Set}
  \ar[
    ll,
    shift right=13pt,
    "{
      \mathrm{Disc}
    }"{description}
  ]
  \ar[
    ll,
    shift left=13pt,
    "{
      \mathrm{Codisc}
    }"{description}
  ]
\end{tikzcd}


$$
  Maps
  \big(
    \mathcal{X}
    ,\,
    \mathbf{E}G
  \big)
  \;=\;
  \Big(
  Fnctr
  \big(
    \mathcal{X}
    ,\,
    \mathbf{E}G
  \big)
  \times
  Fnctn
  \big(
    X_0
    ,\,
    G
  \big)
  \rightrightarrows
  Fnctr
  \big(
    \mathcal{X}
    ,\,
    \mathbf{E}G
  \big)
  \Big)
$$

$$
  Fnctr
  \big(
    \mathcal{X}
    ,\,
    \mathbf{E}G
  \big)
  \;\;
  \simeq
  \;\;  
  Fnctr
  \big(
    \mathcal{X}
    ,\,
    \mathbf{B}G
  \big)
  \times
  G^{\pi_0(\mathcal{X})}
$$


