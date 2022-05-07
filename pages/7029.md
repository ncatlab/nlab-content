

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### In sets
 {#InSets}

\begin{definition}
\label{FreeGroupActionInComponents}
A [[group action]]

$$
  (-)\cdot(-) \;\colon\; G \times X \to X
$$

of a [[group]] $G$ on a [[set]] $X$ is called _free_ if for every $x \in X$,  the [[equation]] $g \cdot x = x$ [[implication|implies]] $g = \mathrm{e}$ (the [[neutral element]]), hence if only the action of the [[neutral element]] has [[fixed points]]

\[
  \label{FreenessConditionInComponents}
  \underset{x \in X}{\exists}
  \;\;
  g \cdot x \,=\, x  
  \;\;\;\;\;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;\;\;\;\;
  g \,=\, \mathrm{e} 
  \,.
\]

Equivalently, an action is free if and only if for any [[pair]] of elements $x,y \in X$, there is _at most one_ group element $g \in G$ such that $g \cdot x = y$. 

\end{definition}

\begin{remark}
Beware the similarity to and difference of free actions with [[effective group action|effective action]]: a free action is effective, but an effective action need not be free.
\end{remark}

\begin{remark}
A free action that is also [[transitive action|transitive]] is called _[[regular action|regular]]_ (at least after passing to its [[linear representation|linear]] [[permutation representation]]).
\end{remark}

\begin{proposition}
\label{FreeGroupActionViaMonomorphicShearMap}
A group action is free according to Def. \ref{FreeGroupActionInComponents} iff its [[shear map]] is a [[monomorphism]]:

\[
  \label{FreeActionWitnessedByMonomorphicShearMap}
  G \curvearrowright X 
  \;
  \text{is free} 
  \;\;\;\;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    G \times X
    &
    \xhookrightarrow{\;(pr_2, \cdot)\;}
    &
    X \times X
    \\
    (g, x) 
    &
    \mapsto
    & 
    \big( x, g \cdot x \big)
    \,.
  }
\]
\end{proposition}
\begin{proof}
  In one direction, assume that the 
action is free in the sense of Def. \ref{FreeGroupActionInComponents}.
Then given $(x,g\cdot x) = (x', g' \cdot x')$
it follows that $x = x'$ and thus that $g \cdot x = g' \cdot x$, which by (eq:FreenessConditionInComponents) implies that $g = g'$. This implication means that the shear map is injective.

In the other direction, assume that the shear map is injective. Then given $g \cdot x = x$, hence equivalently $(x, g \cdot x) = (x, \mathrm{e} \cdot x)$ it follows that ($x = x$ and) $g = \mathrm{e}$. This is the required implication (eq:FreenessConditionInComponents).
\end{proof}


### In categories with finite products

In the form (eq:FreeActionWitnessedByMonomorphicShearMap) the definition of free action makes sense more generally for [[action objects]] [[internalization|internal]] to any ambient [[category]] (with [[finite products]]):

\begin{definition}
\label{FreeInternalActions}
  Let $\mathcal{C}$ be a [[category]] with [[finite products]], let $G \,\in\, Grp(\mathcal{C})$ be an [[internal group]] and $G \curvearrowright X \,\in\, G Act(\mathcal{C}) $ an [[internal action]]:

$$
  G \times X \xrightarrow{\;\; rho \;\;} X
  \,.
$$

Then this is a *free action* if its [[shear map]] is a [[monomorphism]]  in $\mathcal{C}$: 
\[
  \label{FreeInternalAction}
  \rho \; \text{is free}
  \;\;\;\;
  \Leftrightarrow
  \;\;\;\;
  G \times X \xhookrightarrow{\; (\rho, pr_2)\;} X \times X
  \,.
\] 
\end{definition}


### In an $\infty$-topos
 {#DefinitionInAnInfinityTopos}

Def. \ref{FreeInternalActions} also makes sense in the generality of [[(infinity,1)-category theory|$(\infty,1)$-category theory]], with [[monomorphisms]] understood to be [[n-truncated object in an (infinity,1)-category|(-1)-truncated morphisms]].

\begin{definition}
\label{FreeInfinityAction}
**(free $\infty$-action in an $\infty$-topos)**
\linebreak
Let

* $\mathbf{H}$ be an [[(infinity,1)-topos|$\infty$-topos]];

* $G \,\in\, Grp(\mathbf{H})$ a [[group object in an (infinity,1)-category|group object]] (a [[geometric homotopy theory|geometric]] [[infinity-group|$\infty$-group]]);

* $G \curvearrowright X \,\in\, G Act(\mathbf{H})$ an [[infinity-action|$\infty$-action]] of $G$ on $X$.

we say that the $\infty$-action is *free*, if its [[shear map]] $shear_1$ is [[(-1)-truncated]]:

\begin{tikzcd}
      X \times G
      \ar[rr, "\rho"]
      \ar[dd, "\mathrm{pr}_1"{left}]
      \ar[dr, hook, dashed, "\mathrm{shear}_1"{sloped}]
      &&
      X
      \ar[dr, -, shift left=1pt]
      \ar[dr, -, shift right=1pt]
      \ar[dd, ->>]
      \\
      &
      X \times X
      \ar[rr, crossing over, "\mathrm{pr}_1"{pos=.17}]
      \ar[ddrr, phantom, "{\mbox{\tiny (pb)}}"{pos=.1}]
      &&
      X
      \ar[dd]
      \\
      X
      \ar[dr, -, shift left=1pt]
      \ar[dr, -, shift right=1pt]
      \ar[rr, ->>]
      &&
      X /\!\!/ G
      \ar[dr]
      \\
      &
      X \ar[rr]
      \ar[from=uu, crossing over, "\mathrm{pr}_2"{left, pos=.25}]
      &&
      \ast
\end{tikzcd}

\end{definition}

\begin{lemma}
\label{HigherShearMapsOfFreeInfinityActionsAreMinusOneTruncated}
**(higher shear maps of free $\infty$-actions are $(-1)$-truncated)**
\linebreak
  If an $\infty$-action is free according to Def. \ref{FreeInfinityAction}, then also all its higher shear maps $shear_n$ are [[(-1)-truncated]]:

\begin{tikzcd}
      {}
      \ar[d, -, shift left=15pt, dotted]
      \ar[from=d, -, shift left=10pt, dotted]
      \ar[d, -, shift left=5pt, dotted]
      \ar[from=d, -, dotted]
      \ar[d, -, shift right=5pt, dotted]
      \ar[from=d, -, shift right=10pt, dotted]
      \ar[d, -, shift right=15pt, dotted]
      &
      {}
      \ar[d, -, shift left=15pt, dotted]
      \ar[from=d, -, shift left=10pt, dotted]
      \ar[d, -, shift left=5pt, dotted]
      \ar[from=d, -, dotted]
      \ar[d, -, shift right=5pt, dotted]
      \ar[from=d, -, shift right=10pt, dotted]
      \ar[d, -, shift right=15pt, dotted]
      \\
      X
        \times 
      {G} \times {G}
      \ar[d, shift left=10pt, hook]
      \ar[from=d, shift left=5pt]
      \ar[d]
      \ar[from=d, shift right=5pt]
      \ar[d, shift right=10pt]
      \ar[r, hook, "\mathrm{shear}_2"]
      &
      X \times X \times X
      \ar[d, shift left=10pt]
      \ar[from=d, shift left=5pt]
      \ar[d]
      \ar[from=d, shift right=5pt]
      \ar[d, shift right=10pt]
      \\
      X
        \times 
      {G}
      \ar[d, shift left=5pt, hook]
      \ar[from=d]
      \ar[d, shift right=5pt]
      \ar[r, hook, "\mathrm{shear}_1"]
      &
      X \times X
      \ar[d, shift left=5pt]
      \ar[from=d]
      \ar[d, shift right=5pt]
      \\
      X
      \ar[r, -, shift right=1pt]
      \ar[r, -, shift left=1pt, "\mathrm{shear}_0"{above}]
      \ar[d, ->>]
      &
      X
      \ar[d, ->>]
      \\
      X /\!\!/ G
      \ar[r]
      &
      \ast
\end{tikzcd}

\end{lemma}
\begin{proof}
  Notice that for $X \twoheadrightarrow \mathcal{X}$ any [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] in the $\infty$-topos $\mathbf{H}$, we have for $n \in \mathbb{N}_+$ the following [[homotopy pullback]] [[pasting diagram]]:

\begin{tikzcd}[column sep=30pt] 
    &&
    X^{\times^{n+2}_{\mathcal{X}}}
    \ar[dl]
    \ar[dd, phantom, "\mbox{\tiny (pb)}"]
    \ar[dr]
    \\
    & 
    X^{\times^{n+1}_{\mathcal{X}}}
    \ar[dl]
    \ar[dr]
    \ar[dd, phantom, "\mbox{\tiny (pb)}"]
    &&
    X^{\times^2_{\mathcal{X}}}
    \ar[dl]
    \ar[dr]
    \ar[dd, phantom, "\mbox{\tiny (pb)}"]
    \\
    X^{\times^n_{\mathcal{X}}}
    \ar[dr]
    &&
    X
    \ar[dl]
    \ar[dr]
    &&
    X
    \ar[dl]
    \\
    &
    \mathcal{X}
    &&
    \mathcal{X}
\end{tikzcd}
Here the two bottom squares are homotopy Cartesian by definition of [[Cech nerves]], and the top square is homotopy Cartesian since the Cech nerve is a [[groupoid object in an (infinity,1)-category|groupoid object]] (see also at *[[groupoid objects in an (∞,1)-topos are effective]]*) which satisfies the groupoidal [[Segal conditions]] (by [this Def.](groupoid+object+in+an+infinity1-category#GroupoidObjectsViaGroupoidalSegalCondition)).

But this implies, for all $n \geq 1$, that the $n+1$st shear map is the [[homotopy fiber product]] in the [[arrow category]] $\mathbf{H}^{\Delta[1]}$ of the 1st with the $n$th shear map over the [[identity morphism]] on $X$:

\begin{tikzcd}
    X \times G^{\times^{n+1}}
    \ar[rr]
    \ar[dr, hook, dashed, "\mathrm{shear}_{n+1}"{sloped, below}]
    \ar[dd]
    &&
    X \times G
    \ar[dr, hook, "\mathrm{shear}_1"{sloped}]
    \ar[dd, "\mathrm{pr}_1"{left, pos=.3}]
    \\
    &
    X^{\times^{n+2}}
    \ar[rr, crossing over]
    \ar[ddrr, phantom, "\mbox{\tiny (pb)}"{pos=.15}]
    &&
    X \times X
    \ar[dd, "\mathrm{pr}_1"{left, pos=.3}]
    \\
    X \times G^{\times^n}
    \ar[rr]
    \ar[dr, hook, "\mathrm{shear}_n"{sloped}]
    &&
    X
    \ar[dr, -, shift left=1pt]
    \ar[dr, -, shift right=1pt]
    \\
    &
    X^{\times^{n+1}}
    \ar[rr]
    \ar[from=uu, crossing over]
    &&
    X
\end{tikzcd}

Now the claim follows by [[induction]] from the fact that [[(-1)-truncated]] morphisms are the right class in an [[orthogonal factorization system in an (infinity,1)-category|orthogonal factorization system]] (namely the 
[[(n-connected, n-truncated) factorization system]] for $n = -1$) and such classes of morphisms are closed under all [[(infinity,1)-limits|$\infty$-limits]], in particular under [[homotopy pullbacks]], in the [[arrow category]] (by [this Prop.](orthogonal+factorization+system+in+an+infinity1-category#RightClassStableUnderLimitsInArrowCategory)).
\end{proof}


## Examples

* Any [[group]] $G$ acts freely on itself by multiplication $\cdot \colon G \times G \to G$, which is called the (left) [[regular representation]] of $G$.

* An action of $\mathbb{Z}/2\mathbb{Z}$ on a set $X$ corresponds to an arbitrary [[involution]] $i : X \to X$, but the action is free just in case $i$ is a _[[fixed point]]-free_ involution.

* For any set $X$ equipped with a [[transitive action]] $* : G \times X \to X$, the group $Aut_G(X)$ of $G$-equivariant automorphisms of $X$ (i.e., [[bijections]] $\phi : X \to X$ commuting with the action of $G$) acts freely on $X$.  In particular, suppose $\phi \in Aut_G(X)$ is such that $\phi(x) = x$ for some $x\in X$, and let $y\in X$ be arbitrary.  By the assumption that $G$ acts transitively, there is a $g \in G$ such that $y = g*x$. But then $G$-equivariance implies that $\phi(y) = \phi(g*x) = g*\phi(x) = g*x = y$. Since this holds for all $y\in Y$, $\phi$ must be equal to the identity $\phi = id_X$, and therefore $Aut_G(X)$ acts freely on $X$.

* A [[combinatorial species]] $F : \mathbb{P} \to Set$ is said to be _flat_ if all of the actions $S_n \times F(n) \to F(n)$ are free (see [[Combinatorial species and tree-like structures]]). For example, the species of [[linear orders]] is flat.

## Properties

### Homotopy colimits of free actions
 {#HomotopyColimitsOfFreeActions}


\begin{proposition}
\label{HomotopyQuotientsOfFreeActionsAreQuotientsOfZeroTruncatedAction}
**([[homotopy quotients]] of [[free actions|free]] [[infinity-action|$\infty$-action]] are plain [[quotients]] of [[0-truncated]] [[group actions]])**
\linebreak
Let 

* $\mathbf{H}$ be an [[(infinity,1)-topos|$\infty$-topos]];

* $G \,\in\, Grp(\mathbf{H})$ a [[group object in an (infinity,1)-category|group object]] (a [[geometric homotopy theory|geometric]] [[infinity-group|$\infty$-group]]);

* $G \curvearrowright X \,\in\, A Act(\mathbf{H})$ an [[infinity-action|$\infty$-action]] of $G$ on $X$.

If this is a free $\infty$-action (Def. \ref{FreeInfinityAction}) then the [[homotopy quotient]] 

\[
  \label{HomotopyQuotientAsInfinityColimit}
  X 
    \!\sslash\! G 
   \,=\, 
   \underset{\underset{[n] \in \Delta^{op}}{\longrightarrow}}{\lim} 
  X \times G^{\times_n}
  \;\;\;
  \in
  \;
  \mathbf{H}
\]

is [[equivalence in an (infinity,1)-category|equivalent]] to the plain [[quotient]], namely to the [[coequalizer]]

\[
  \label{QuotientAsCoequalizer}
  \tau_0(X) 
    /
  \tau_0(G) 
   \,\coloneqq\, 
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
\]

of [[0-truncated]] objects 

\[
  \label{ZeroTruncationReflectionInProofOfFreeHomotopyQuotients}
\]
\begin{tikzcd}
  \mathbf{H}_0
  \ar[r, hook, shift right=7pt, "i_0"{below}]
  &
  \mathbf{H}
  \,,
  \ar[
    l, 
    shift right=7pt, 
    "{\mathclap{\times}}"{description, pos=0}, 
    "{\tau_0}"{above}
  ]
  \ar[l, phantom, "{\scalebox{.7}{$\bot$}}"]
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

In particular, if both $X$ and $G$ are already [[0-truncated]], then the action of $G$ on $X$ is free iff it is free in the [[1-category]] theoretic sense (eq:FreeInternalAction), and then the homotopy quotient coincides with their ordinary quotient.
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

Incidentally, the left morphism above is an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] as shown, hence is [[(-1)-connected]]. Threfore, *if* the right vertical morphism $X \!\sslash\! G \xrightarrow{\;\;} \ast$ were [[(-1)-truncated]] (hence if $X \!\sslash\! G$ were [[subterminal object|subterminal]]), then the [[(n-connected, n-truncated) factorization system]] would imply the required [[lift]]. While this would-be argument fails, as $X \!\sslash\! G$ is in general far from being subterminal, the following argument observes that with a suitable choice of [[atlases]] for all four [[infinity-stack|$\infty$-stacks]], their [[groupoid object in an (infinity,1)-category|groupoid objects]] do form a [[lifting problem]] to which the [[(n-connected, n-truncated) factorization system]] does apply:

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
    \ar[dd, shift right=12pt, start anchor={[yshift=-6pt]}]
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
{#ObservingTheConnectedTruncatedLiftingPropblems}
Observe that all the upper horizontal squares in this diagram have, as indicated: 

1. a [[(-1)-connected]] morphisms $\twoheadrightarrow$ on the left, since the [[underlying]] [[infinity-groupoid|$\infty$-groupoid]] $K \in Grpd_\infty$ of every [[discrete infinity-groupoid|discrete $\infty$-group]] is [[inhabited object|inhabited]] and since $LConst$, being an [[inverse image]]-functor, is a [[lex functor|lex]] [[left adjoint]] and hence [[preserved limit|preserves]] [[Cech nerves]] and [[(infinity,1)-colimits|$\infty$-colimits]] and hence [[effective epimorphism in an (infinity,1)-category|effective epimorphisms]].

1. a [[(-1)-truncated]] morphism $\hookrightarrow$ on the right, by Lemma \ref{HigherShearMapsOfFreeInfinityActionsAreMinusOneTruncated}.

Since [[n-connected object in an (infinity,1)-topos|$n$-connected]]/[[n-truncated object in an (infinity,1)-category|$n$-truncated]] morphisms in  [[(infinity,1)-categories of (infinity,1)-presheaves|$\infty$-categories of $\infty$-presheaves]] (here: of [[simplicial objects]] in $\mathbf{H}$) are detected objectwise (since they are characterized by [[categorical homotopy groups in an (infinity,1)-topos|categorical homotopy groups]]),  this means that the entire square diagram of [[simplicial objects]] (i.e. disregarding the bottom square) has a [[(-1)-connected]] morphism on the left and a [[(-1)-truncated]] morphism in the right.  Therefore, the [[(n-connected, n-truncated) factorization system]] implies that there exist compatible dashed [[lifts]] filling all the upper squares, as shown. 

But then taking the [[(infinity,1)-colimits|$\infty$-colimit]] over [[simplicial objects]] and using that [[groupoid objects in an (infinity,1)-topos are effective|groupoid objects in an $\infty$-topos are effective]], recovers the bottom square, but now also equipped with a dashed [[lift]]. This is the claimed factorization which shows that $X \!\sslash\! G$ is [[0-truncated]];

\[
  \label{ZeroTruncationOfHomotopyQuotientOfFreeAction}
  i_0
  \circ
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
    i_0
    \circ
    \tau_0
    \big( 
      X \!\sslash\! G
    \big)
    & 
    \text{ (eq:ZeroTruncationOfHomotopyQuotientOfFreeAction) }
    \\
    & 
    \;\simeq\;
    i_0
    \circ
    \tau_0
    \Big( 
      \underset{\underset{ [n] \in \Delta^{op} }{\longrightarrow}}{\lim}
      \,
      X \times G^{\times_n}
    \Big)    
    &
    \text{ (eq:HomotopyQuotientAsInfinityColimit) }
    \\
    & \;\simeq\;
    i_0
    \Big(
    \underset{\underset{ [n] \in \Delta^{op} }{\longrightarrow}}{\lim}
    \,
    \tau_0(X) \times \big(\tau_0(G)\big)^{\times_n}
    \Big)
    &
    \text{ (eq:ZeroTruncationReflectionInProofOfFreeHomotopyQuotients) }
    \\
    & \;\simeq\;
    i_0
    \Big(
      coeq
      \big(
        \tau_0(X) \times \tau_0(G)
        \overset{\phantom{---}}{\rightrightarrows}
        \tau_0(X)
      \big)
    \Big)
    &
    \text{ (eq:InclusionOfParallelPairIntoOppositeSimplexCategoryIsFinal) }
    \\
    & \;=\;
    i_0
    \big(
      \tau_0(X)
      /
      \tau_0(G)
    \big)
    &
    \text{ (eq:QuotientAsCoequalizer). }
  \end{array}  
$$

In the second but last line we used (from [this Example](final+functor#FirstPairOfFaceMapsFinalInOppositeSimplexCategory)) that the inclusion of the [[diagram]] consisting of a [[pair]] of [[parallel morphisms]] into the [[opposite category|opposite]] of the [[simplex category]] is [[final functor]]
\[
  \label{InclusionOfParallelPairIntoOppositeSimplexCategoryIsFinal}
    \left(
      [1]
      \underoverset
        {d_0}
        {d_1}
        {\rightrightarrows}          
      [0]
    \right)
    \;\xhookrightarrow{\phantom{---}}\;
    \Delta^{op}
    \;\;\;\;\;\;
    \text{is final}
    \,,
\]
meaning that the [[colimit]] over a [[simplicial object]] in a [[1-category]] is equivalently the [[coequalizer]] of the first two [[face maps]].
\end{proof}





## Related concepts

* [[fixed point]]

* [[homogeneous space]]

* [[torsor]]

* [[universal principal bundle]]

* [[transitive action]], [[effective action]], [[free action]], [[semi-free action]], [[regular action]],

* [[proper action]], [[properly discontinuous action]]


[[!redirects free actions]]