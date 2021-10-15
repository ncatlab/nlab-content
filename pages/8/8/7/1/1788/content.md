

\begin{proof}
Suppose given functors $L \,\colon\, C \to D$, $R: D \to C$ and the structure of a pair of [[adjoint functors]] in the form of a natural isomorphism of [[hom-sets]] ([here](adjoint+functor#InTermsOfHomIsomorphism))

$$
  \Psi_{c, d}
  \;\colon\; 
  \hom_D(L(c), d) \cong \hom_C(c, R(d))
$$ 

Now the idea is that, in the spirit of the (proof of the) [[Yoneda lemma]], we would like $\Psi$ to be determined by what it does to [[identity morphisms]]. With that in mind, define the [[adjunction unit]] $\eta \colon 1_C \to R L$ by the formula $\eta_c = \Psi_{c, L(c)}(1_{L(c)})$. Dually, define the counit $\varepsilon \,\colon\, L R \to 1_D$ by the formula
$$
  \varepsilon_d 
  \,\coloneqq\, \Psi^{-1}_{R(d), d}(1_{R(d)})
  \,.
$$

Then given $g \,\colon\, L(c) \to d$, the claim is that 

$$
  \Psi_{c, d}(g) 
    \,=\, 
  (c \stackrel{\eta_c}{\to} R(L(c)) \stackrel{R(g)}{\to} R(d))
  \,.
$$ 

This may be left as an exercise in the yoga of the Yoneda lemma, applied to $\hom_D(L(c), -) \to \hom_C(c, R(-))$. By [[formal duality]], given $f \,\colon\, c \to R(d)$, 

$$
  \Psi^{-1}_{c, d}(f) = (L(c) \stackrel{L(f)}{\to} L(R(d)) \stackrel{\varepsilon_d}{\to} d)
  \,.
$$ 

(We spell out the Yoneda-lemma proof of this dual form [below](#YonedaLemmaArgument).)

Finally, these operations should obviously be mutually inverse, but that can again be entirely encapsulated Yoneda-wise in terms of the effect on identity maps. Thus, if $\eta_c \coloneqq \Psi_{c, L(c)}(1_{L(c)})$, via the recipe just given for $\Psi^{-1}$ we recover 

$$1_{L(c)} = (L(c) \stackrel{L(\eta_c)}{\to} L R L(c) \stackrel{\varepsilon_{L(c)}}{\to} L(c))$$ 

and this is one of the famous [[triangle identities]]: $1_L = (L \stackrel{L \eta}{\to} L R L \stackrel{\varepsilon L}{\to} L)$.  Here, juxtaposition of functors and natural transformations denotes neither functor application, nor vertical composition, nor horizontal composition, but [[whiskering]]. By duality, we have the other [[triangle identity]] $1_R = (R \stackrel{\eta R}{\to} R L R \stackrel{R \varepsilon}{\to} R)$. These two triangular equations are enough to guarantee that the recipes for $\Psi$ and $\Psi^{-1}$ indeed yield mutual inverses. 

In conclusion it is perfectly sufficient to define an adjoint pair of functors in $Cat$ as given by unit and counit transformations $\eta: 1_C \to R L$, $\varepsilon: L R \to 1_D$, satisfying the triangle identities above. 
\end{proof}


[link]( https://en.wikipedia.org/wiki/Draft:Funding_Sources_for_American_Mathematicians)

\begin{example}\label{GActionsAndGOrbits}
**([[G-sets]] and [[orbits]])**
\linebreak
  Let $G \,\in\, Grp(Set)$ be a [[discrete group]]. Write

* [[G-set|$G Set$]] for its category of [[group actions]] on [[sets]], 

* $G Orbt \xhookrightarrow{\;} G Set$ for its [[orbit category]], the [[full subcategory]] on the [[transitive actions]], hence the [[coset space|sets of cosets]] $G/H$, for [[subgroups]] $H \subset G$.

Since every [[G-set]] $X$ decomposes as a [[disjoint union]] of [[transitive actions]], namely of [[orbits]] of [[elements]] of $X$, this inclusion exhibits $G Set$ as the [[free coproduct completion]] of [[orbit category|G Orbt]].
\end{example}

$$
  B H \to B G
$$

$\simeq$

$$
  H \backslash\!\!\backslash G \sslash G
$$


$$
\{
\boxed{
\boxed{\underset{x}{}\swarrow
\,\,\,\,\,\,\,}
\!\!\!\!\!\!\!\!
\,\,\,\,\,\,\,\,
\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,
}\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
\!\!\!\!\!\!\!\!
\boxed{
 \boxed{
\overset{\boxed{U}}{}
\searrow
\underset{X}{} \swarrow
\overset{\boxed{V}}{}
}\!\!\!\!\!\!\!
{\,\,\,\,\,\,\searrow\underset{y}{} }
}
\}
$$


\begin{tikzcd}[column sep=20pt]
     \mathrm{PSh}(\mathcal{C})_{/y_{\mathcal{C}}(X)}
     \big(
       (y_{\mathcal{C}})_{/X}(U \xrightarrow{\phi} X)
       ,\,
       (E \xrightarrow{p} y_{\mathcal{C}}(X) )
     \big)
     \ar[
       rr
     ]
     \ar[d]
     &&
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        E
     \big)
     \ar[d]
     \\
     \big\{
        y_{\mathcal{C}}(\phi)
     \big\}
     \ar[rr]
     &&
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        y_{\mathcal{C}}(X)
     \big)              
\end{tikzcd}



\begin{prop}
  Given a pair of [[adjoint functors]], $L \dashv R$, if there is any [[natural isomorphism]] $L \circ R \underoverset{\sim}{\phi}{\longrightarrow} id$ then the [[adjunction counit]] is an isomorphism: $L \circ R \underoverset{\epsilon}{\sim}{\longrightarrow} id$.
\end{prop}


$$
  id
  \underoverset
    {\sim}
    {\phi^{-1}}
    {\longrightarrow}
  L \circ R
  \underoverset
    {}
    {L \circ \eta \circ R}
    {\longrightarrow}
  L \circ R \circ L \circ R
  \underoverset
    {\sim}
    {\phi \phi}
    {\longrightarrow}
  id \circ id
    \simeq
  id
$$



# Separation axioms as lifting properties

It is easy to see that the definitions of separation axioms $T_0-T_4$ are represented by the following lifting diagrams
involving finite topological spaces. In the pictures above,
boxes are put around open subsets, and 
 an arrow $\bullet_u\to \bullet_c$  means that $\bullet_c$ is in the closure of $\bullet_u$; the indices of $\bullet$ indicate 
 where points are sent by the morphisms. These diagrams for $T_2-T_4$ omit the conditions $T_1$ that points are closed. 



\begin{tikzcd}
[
  column sep={between origins, 40pt},
  row sep={between origins, 40pt}
]
  \mathrm{CoDsc}
  \big(
    \boxed{\{\bullet_0\leftrightarrow \bullet_1\}}
  \big)
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[dd,"{ (T_0) }"]
  \\
  \\
  \bullet_{0=1}
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \bullet
\end{tikzcd}
\begin{tikzcd}
[
  column sep={between origins, 40pt},
  row sep={between origins, 40pt}
]
  \mathrm{Sierp}
  \big(
    \{\boxed{ {\bullet_0} }\rightarrow{\bullet_1} \}
  \big)
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[dd,"{ (T_1) }"]
  \\
  \\
  \bullet_{0=1}
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \bullet
\end{tikzcd}

\begin{tikzcd}
[
  column sep={between origins, 80pt},
  row sep={between origins, 40pt}
]
  \boxed{\{\boxed{\bullet_x}, \boxed{\bullet_y}\}}
  \ar[
    rr,
    "{ }"
  ]
  \ar[dd, hook, "{ \forall  }"{left}, ,"{ (T_2) }"{right} ]
  &&
  \boxed{
    \overset{
      \boxed{
        \boxed{\bullet_x}
        \;\;
        \,
        \;\;
        \boxed{\bullet_y}}
      }{
        \underset{
           \bullet_X
        }
        {
          \searrow \;\, \swarrow
        }
      }
  }
  \ar[dd]
  \\
  \\
  X
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
   \{\bullet_{x=X=y}\}
\end{tikzcd}
\begin{tikzcd}
[
  column sep={between origins, 60pt},
  row sep={between origins, 40pt}
]
  \{\bullet_x\}
  \ar[dd,"{ \forall }"{left}, "{ (T_3) }"{right}]
  \ar[rr]
  &&
\{
\boxed{
 \boxed{
\overset{\boxed{\bullet_x}}{}
\searrow
\underset{\bullet_X}{} \swarrow
\overset{\boxed{\bullet_U}}{}
}\!\!\!\!\!\!\!
{\,\,\,\,\,\,\searrow\underset{\bullet_F}{} }
}
\}
  \ar[dd]
  \\
  \\
  X
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
      \{\overset{\boxed{\bullet_{x=X=U}}}{}\searrow\underset{\bullet_F}{}\}
\end{tikzcd}
\begin{tikzcd}
[
  column sep={between origins, 60pt},
  row sep={between origins, 40pt}
]
  \varnothing
  \ar[dd, "{ (T_4) }"{right}]
  \ar[rr]
  &&
\boxed{
\boxed{\underset{\bullet_x}{}\swarrow
\,\,\,\,\,\,\,}
\!\!\!\!\!\!\!\!
\,\,\,\,\,\,\,\,
\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,
\,\,\,\,
\,\,\,\,\,}
\!\!\!\!\!\!\!
\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
\!\!\!\!\!\!\!\!
\!\!\!\!\!\!\!\!
\!\!\!\!
\boxed{
\boxed{
\overset{\boxed{\bullet_u}}{}
\searrow
\underset{\bullet_X}{} \swarrow
\boxed{
\overset{\boxed{\bullet_v}}{}
\!\!\!\!\!\!\!
{\,\,\,\,\,\,\searrow\underset{\bullet_y}{} }
}\!\!\!\!\!\!\!%%%%%%%%
\!\!\!\!\!}
%\,\,\,\,\,\,\,\,\,
\,\,\,\,\,\,\,\,\,}
  \ar[dd]
  \\
  \\
  X
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \{
\boxed{
\underset{\bullet_x}{}{\swarrow}             
\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,
%\,\,
%\,\,\,\,\,\,\,
}
\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
%\!\!%\!\!\!\!\!\!\!
\boxed{\overset{\boxed{\bullet_{U=X=V}}}{}
{\searrow}
\underset{\bullet_y}{}
}
\}
\end{tikzcd}
