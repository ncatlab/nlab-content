
Write $TopSp$ for the [[convenient category of topological spaces|convenient category]] of [[compactly generated weak Hausdorff spaces]], and $TopSp_{Qu}$ for the [[classical model structure on topological spaces]] in its version for compactly generated spaces ([this Thm.](classical+model+structure+on+topological+spaces#ModelStructureOnTopcg)).

\begin{proposition}
  If $H \subset G \,\in\, Grp(TopSp)$ is a [[subgroup]]-inclusion of [[topological groups]] such that the corresponding [[coset space]] [[coprojection]] is a [[Serre fibration]]
$$
  G
  \xrightarrow{ \;\in Fib\; }
  G/H
  \;\;\;
  \in
  \;
  TopSp_{Qu}
$$
(for example in that it [[coset space coprojection admitting local sections|admits local sections]]).

Then the [[quotient]] of the [[universal principal bundle|universal principal space]] $E G$ by the subgroup $H$ is [[weak homotopy equivalence|weak homotopy equivalent]] to the [[classifying space]] $B H$ of $H$:
$$
  (E G)/H \;\simeq\; B H \;\;\; \in Ho(TopSp_{Qu})
  \,.
$$
\end{proposition}

$$
  H
  \xrightarrow{\;}
  \frac{E G \times G}{G}
  \xrightarrow{\;}
  \frac{
    E G \times (G/H)
  }{G}  
$$


\begin{prop}
Transported through the equivalence of Prop. \ref{HFixedLociOFMappingGroupoidFromEGToBGamma}, 
the canonical [[group action]] (see [this Prop.](fixed+point+space#PassageToFixedLociIsRightAdjoint)) of the [[Weyl group]] $W_G(H)$ on the $H$-[[fixed locus]] 
$
  Fnctr\big(\mathbf{E}G ,\, \mathbf{B}\Gamma\big)^H
$
becomes, on connected components
$
  \pi_0
  \big(
    CrsHom(H,\,\Gamma) \sslash_{\!\!ad} \Gamma
  \big)
  \;\;
  \simeq
  \;\;
  H^1_{Grp}(H,\,\Gamma)
$,
the $W_G(H)$-action on the non-abelian group 1-cohomology of $H$ from Prop. \ref{WeylGroupActsOnNonAbGroup1CohomOfSubgroup}.
\end{prop}
\begin{proof}
  We make explicit use of the functors $L, R$ constructed in the proof of Prop. \ref{HFixedLociOFMappingGroupoidFromEGToBGamma}. Noticing that $R$ is a section of $L$, we need to (1) send a crossed homomorphism up with $R$, (2) there act on it with $n$, (3) send the result back with $L$. The result is the desired induced action.

Explicitly, by the definition of $L$ in the proof of Prop. \ref{HFixedLociOFMappingGroupoidFromEGToBGamma}, this way a crossed homomorpism $\phi \,\colon\, H \to \Gamma$ is sent by $n \in N_G(H)$ to the assignment
\[
  \label{TransportingCanonicalActionOnFixedLocusToGroupCohomology}
  h \,\mapsto\,    
    \Big(L\big( n \cdot (R \phi) \big)\Big)(h)
    \;=\;
    \alpha(n)
    \Big(
      (R\phi)
      \big(
        n^{-1} ,\, n^{-1} \cdot h
      \big)
    \Big)
  \,.
\]

It just remains to evaluate the right hand side. 

Notice that the definition of $L$ is independent of the choice of $\sigma \,\colon\, G/H \xrightarrow{\;} G$ (eq:SectionOfTheCoprojectionToTheCosetSpace), and that $R$ (whose definition does depend on this choice ) is a section for each choice. Hence we may choose $\sigma$ in a way convenient way *for each $n$*.

Now if $n \in H \subset N_G(H)$ then its canonical action on the $H$-fixed locus is trivial, and also the claimed induced action is trivial, so that in this case there is nothing further to be proven. Therefore we assume now that $n$ is not in $H$, and then we choose $\sigma$ such as to pick $n^{-1}$ as the representative in its $H$-coset:
$$
  \sigma\big( \big[n^{-1}\big] \big) \;\coloneqq\; n^{-1}
  \,.
$$

With this choice, the right hand side of (eq:TransportingCanonicalActionOnFixedLocusToGroupCohomology) is evaluated as follows, where we repeatedly use that, by definition and choice of $\sigma$, $R\phi$ assigns the neutral element to the morphism $n^{-1} \to \mathrm{e}$ in the pair groupoid:

$$
  \begin{aligned}
    \Big(L\big( n \cdot (R \phi) \big)\Big)(h)
    & \;=\;
    \alpha(n)
    \Big(
      (R\phi)
      \big(
        n^{-1} ,\, n^{-1} \cdot h
      \big)
    \Big)
    \\
    & \;=\;
    \;=\;
    \alpha(n)
    \big(
      (R\phi)(\mathrm{e},\, n^{-1} \cdot h)
    \big)
    \\
    &
    \;=\;
    \alpha\big(n^{-1} \cdot h \cdot n \cdot n\big)
    \big(
      (R\phi)(n^{-1} \cdot h^{-1} \cdot n,\, n^{-1})
    \big)
    \\
    &
    \;=\;
    \alpha\big(n^{-1} \cdot h \cdot n  \cdot n\big)
    \big(
      (R\phi)(n^{-1} \cdot h^{-1} \cdot n,\, \mathrm{e})
    \big)
    \\
    &
    \;=\;
    \alpha(n)
    \big(
      (R\phi)(\mathrm{e},\, n^{-1} \cdot h \cdot n)
    \big)
    \\
    & \;=\;
    \alpha(n)
    \big(
      \phi(n^{-1} \cdot h \cdot n)
    \big)
    \mathrlap{\,.}
  \end{aligned}
$$

This is indeed the claimed formula (eq:ActionOfNormalizerOnCrossedHomomorphismsFromSubgroup).
\end{proof}


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