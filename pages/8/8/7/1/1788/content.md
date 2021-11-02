
\begin{proposition}
\label{HomotopyQuotientsOfFreeActionsAreQuotientsOfZeroTruncatedAction}
**([[homotopy quotients]] of [[free actions|free]] [[infinity-action|$\infty$-action]] are plain [[quotients]] of [[0-truncated]] [[group actions]])**
\linebreak
Let 

* $\mathbf{H}$ be an [[(infinity,1)-topos|$\infty$-topos]];

* $G \,\in\, Groups(\mathbf{H})$ a [[group object in an (infinity,1)-category|group object]] ([[infinity-group|$\infty$-group]]);

* $G \curvearrowright X \,\in\, A Act(\mathbf{H})$ an [[infinity-action|$\infty$-action]] of $G$ on $X$.

If this is an $\infty$-[[free action]] in that all its higher [[shear maps]] are [[n-truncated object in an (infinity,1)-category|(-1)-truncated]]

\[
  \label{HigherShearMapsOfInfinityFreeAction}
  X \times G^n
  \xhookrightarrow{ \phantom{---}  }
  X^{\times_{n+1}}
\]

then the [[homotopy quotient]] 

\[
  \label{HomotopyQuotientAsInfinityColimit}
  X 
    \!\sslash\! G 
   \,=\, \underset{\underset{[n] \in \Delta^{op}}{\longrightarrow}}{\lim} X \times G^{\times_n}
  \;\;\;
  \in
  \;
  \mathbf{H}
\]

is equivalent to the plain [[quotient]], namely the [[coequalizer]]

$$
  \tau_0(X) 
    /
  \tau_0(G) 
   \,=\, 
  coeq
  \big(
    \tau_0(X) \times \tau_0(G)
    \overset{\phantom{---}}{\rightrightarrows}
    \tau_0(X)
  \big)
  \;\;\;
  \in
  \;
  \mathbf{H}_0
$$


of [[0-truncated]] objects 

\[
  \label{ZeroTruncationReflectionInProofOfFreeHomotopyQuotients}
\]
\begin{tikzcd}
  \mathbf{H}_0
  \ar[rr, hook, shift right=7pt, "i_0"{below}]
  &&
  \mathbf{H}
  \ar[
    ll, 
    shift right=7pt, 
    "\mathclap{\times}"{pos=0}, 
    "{\tau_0}{above}"
  ]
\end{tikzcd}

in that

\[
  \label{EquivalenceOfHomotopyQuotientOfFreeActionToPlainQuotient}
  X \!\sslash\! G
  \;\;
  \simeq
  \;\;
  i_0\big( \tau_0(X)/\tau_0(G) \big)
  \;\;\;
  \in
  \;
  \mathbf{H}_0
  \xhookrightarrow{i_0}
  \mathbf{H}
  \,.
\]

In particular, if both $X$ and $G$ are already [[0-truncated]], then the action of $G$ on $X$ is $\infty$-free iff it is free in the ordinary sense, and then the homotopy quotient coincides with their ordinary quotient.
\end{proposition}

\begin{proof}
First we show that $X \!\sslash\! G$ is [[0-truncated]], in that for every $U \,\in\, \mathbf{H}$ and every [[infinity-group|
$\infty$-group]] $K$ in the [[inverse image]] $Grpd_\infty \xrightarrow{ LConst } \mathbf{H}$ of the [[terminal geometric morphism]],
every morphism into it out of $U \times \mathbf{B}K$  factors through the [[projection]] onto $U$:

\begin{tikzcd}
  U \times \mathbf{B}K
  \ar[rr, "\forall"]
  \ar[d, ->>, "\mathrm{pr}_1"{left}]
  &&
  X /\!\!/ G
  \ar[d]
  \\
  U
  \ar[urr, dashed, "\exists"]
  \ar[rr, -, shift left=1pt]
  \ar[rr, -, shift right=1pt]
  &&
  \ast
\end{tikzcd}

Here $\ast$ denotes the [[terminal object]], which we adjoin, without changing the situation, to bring out the form of the [[lifting problem]].

The left morphism above is an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] as shown, hence is [[(-1)-connected]], since the [[underlying]] [[infinity-groupoid|$\infty$-groupoid]] $K \in Grpd_\infty$ of every $\infty$-group is [[inhabited object|inhabited]] and since $LConst$, being an [[inverse image]]-functor, is a [[lex functor|lex]] [[left adjoint]] and hence [[preserved limit|preserves]] [[Cech nerves]] and [[(infinity,1)-colimits|$\infty$-colimits]] and hence [[effective epimorphism in an (infinity,1)-category|effective epimorphisms]].

Notice, therefore, that *if* the right vertical morphism $X \!\sslash\! G \xrightarrow{\;\;} \ast$ were [[(-1)-truncated]] (hence if $X \!\sslash\! G$ were [[subterminal object|subterminal]]), then the [[(n-connected, n-truncated) factorization system]] would imply the required [[lift]]. While this would-be argument fails, as, $X \!\sslash\! G$ is in general far from being subterminal, the following argument observes that with a suitable choice of [[atlases]] for all four [[infinity-stack|$\infty$-stacks]], their [[groupoid object in an (infinity,1)-category|groupoid objects]] do form a [[lifting problem]] to which the [[(n-connected, n-truncated) factorization system]] does apply:

So consider extending the above square diagram to a square of [[augmented simplicial object|augmented]] [[simplicial objects]] by considering  [[atlas|atlases]] and their [[Cech nerves]], as shown by the following solid arrows:
\begin{tikzcd}[row sep=30pt]
    U \times K \times K
    \ar[dd, shift left=12pt, start anchor={[yshift=-4pt]}]
    \ar[from=dd, shift left=6pt]
    \ar[dd]
    \ar[from=dd, shift right=6pt]
    \ar[dd, shift right=12pt]
    \ar[rr]
    \ar[dr, ->>]
    &&
    X \times G \times G
    \ar[dd, shift left=12pt]
    \ar[from=dd, shift left=6pt]
    \ar[dd]
    \ar[from=dd, shift right=6pt]
    \ar[dd, shift right=12pt]
    \ar[dr, hook]
    \\
    & 
    U
    \ar[rr, crossing over]
    \ar[ur, dashed]
    &&
    X \times X \times X
    \ar[dd, shift left=12pt]
    \ar[from=dd, shift left=6pt]
    \ar[dd]
    \ar[from=dd, shift right=6pt]
    \ar[dd, shift right=12pt]
    \\
    U \times K
    \ar[rr]
    \ar[dr, ->>]
    \ar[dd, shift left=6pt]
    \ar[from=dd]
    \ar[dd, shift right=6pt]
    &&
    X \times G
    \ar[dr, hook]
    \ar[dd, shift left=6pt]
    \ar[from=dd]
    \ar[dd, shift right=6pt]
    \\
    & 
    U
    \ar[rr, crossing over]
    \ar[from=uu, shift left=12pt, crossing over, end anchor={[yshift=7pt]}]
    \ar[uu, shift left=6pt, crossing over, start anchor={[yshift=3pt]}]
    \ar[from=uu, crossing over]
    \ar[uu, shift right=6pt, crossing over, start anchor={[yshift=3pt]}]
    \ar[from=uu, shift right=12pt, crossing over, end anchor={[yshift=7pt]}]
    \ar[ur, dashed]
    &&
    X \times X
    \ar[dd, shift left=6pt]
    \ar[from=dd]
    \ar[dd, shift right=6pt]
    \\
    U
    \ar[rr]
    \ar[dd, ->>]
    \ar[dr, -, shift left=1pt]
    \ar[dr, -, shift right=1pt]
    &&
    X
    \ar[dd, ->>]
    \ar[dr, -, shift left=1pt]
    \ar[dr, -, shift right=1pt]
    \\
    &
    U
    \ar[rr, crossing over]
    \ar[from=uu, shift left=6pt, crossing over]
    \ar[uu, crossing over]
    \ar[from=uu, shift right=6pt, crossing over]
    \ar[ur, dashed]
    &&
    X
    \ar[dd, ->>]
    \\
    U \times \mathbf{B}K
    \ar[rr]
    \ar[dr]
       &&
    X /\!\!/ G
    \ar[dr]
    \\
    & 
    U
    \ar[rr]
    \ar[from=uu, ->>, crossing over]
    \ar[ur, dashed]
    &&
    \ast
\end{tikzcd}
By the [[inhabited object|inhabitation]] of $K$ and the assumption (eq:HigherShearMapsOfInfinityFreeAction) on $G \curvearrowright X$ all the upper horizontal squares have a [[(-1)-connected]] morphism $\twoheadrightarrow$ on the left and a [[(-1)-truncated]] morphism $\hookrightarrow$ on the right. Since $n$-connected/$n$-truncated morphisms for [[(infinity,1)-categories of (infinity,1)-presheaves|$\infty$-categories of $\infty$-presheaves]] (here: of [[simplicial objects]] in $\mathbf{H}$) are detected objectwise,  this means that the entire square diagram of [[simplicial objects]] (i.e. disregarding the bottom square) has a [[(-1)-connected]] morphism on the left and a [[(-1)-truncated]] morphism in the right.  Therefore, the [[(n-connected, n-truncated) factorization system]] implies that there exist compatible dashed [[lifts]] filling all the upper squares, as shoown. 

But then taking the [[(infinity,1)-colimits|$\infty$-colimit]] over [[simplicial objects]] and using that [[groupoid objects in an (infinity,1)-topos are effective|groupoid objects in an $\infty$-topos are effective]], recovers the bottom square, but now also equipped with a dashed [[lift]]. This is the claimed factorization which shows that $X \!\sslash\! G$ is [[0-truncated]];

\[
  \label{ZeroTruncationOfHomotopyQuotientOfFreeAction}
  \tau_0
  \big(
    X \!\sslash\! G
  \big)
  \;\;
  \simeq
  \;\;
  X \!\sslash\! G 
  \,.
\]

To conclude the proof of (eq:EquivalenceOfHomotopyQuotientOfFreeActionToPlainQuotient), use that $\tau_0$ is a [[left adjoint]] (eq:ZeroTruncationReflectionInProofOfFreeHomotopyQuotients), [[left adjoints preserve colimits|hence preserves $\infty$-colimits]], and also [[preserved limit|preserves]] [[products]], i.e. [[homotopy products]] (by [this Prop.](n-truncated+object+of+an+infinity1-category#nTruncationInToposPreservesFiniteProducts)). Here this implies that:

$$
  \begin{array}{lll}
    X \!\sslash\! G
    & 
    \;\simeq\;
    \tau_0
    \big( 
      X \!\sslash\! G
    \big)
    & 
    \text{ (eq:ZeroTruncationOfHomotopyQuotientOfFreeAction) }
    \\
    & 
    \;\simeq\;
    \tau_0
    \big( 
      \underset{\underset{ [n] \in \Delta^{op} }{\longrightarrow}}{\lim}
      \,
      X \times G^{\times_n}
    \big)    
    &
    \text{ (eq:HomotopyQuotientAsInfinityColimit) }
    \\
    & \;\simeq\;
    \underset{\underset{ [n] \in \Delta^{op} }{\longrightarrow}}{\lim}
    \,
    \tau_0(X) \times \big(\tau_0(G)\big)^{\times_n}
    &
    \text{ (eq:ZeroTruncationReflectionInProofOfFreeHomotopyQuotients) }
    \\
    & \;\simeq\;
    coeq
    \big(
      \tau_0(X) \times \tau_0(G)
      \overset{\phantom{---}}{\rightrightarrows}
      X
    \big)
    &
    \text{ (eq:InclusionOfParallelPairIntoOppositeSimplexCategoryIsFinal) }
  \end{array}  
$$

In in the last line we used (from [this Example](final+functor#FirstPairOfFaceMapsFinalInOppositeSimplexCategory)) that the inclusion of the [[diagram]] consisting of a [[pair]] of [[parallel morphisms]] into the [[opposite category|opposite]] of the [[simplex category]] is [[final functor]]
\[
  \label{InclusionOfParallelPairIntoOppositeSimplexCategoryIsFinal}
    \big(
      [1]
      \underoverset
        {d_0}
        {d_1}
        {\rightrightarrows}          
      [0]
    \big)
    \;\xhookrightarrow{\phantom{---}}\;
    \Delta^{op}
    \;\;\;\;\;\;\;\;\;
    \text{is final}
    \,,
\]
meaning that the [[colimit]] over a [[simplicial object]] is equivalently the [[coequalizer]] of the first two [[face maps]].
\end{proof}


