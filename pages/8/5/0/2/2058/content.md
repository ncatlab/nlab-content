
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


\tableofcontents

## Definition

Let $C$ be a [[category]] with [[pullbacks]] and [[colimits]] of some [[small category|shape]] $D$.  

\begin{definition}\label{BasicDefinition}
We say that colimits of shape $D$ are __stable by [[base change]]__, or __stable under pullback__, or that these colimits are __universal__, if for every [[functor]] $G \colon D \to C$ and for all [[pullback]] [[diagrams]] of the form

$$
  \array{
    \big(\underset{\longrightarrow}{\lim}_D G\big) 
      \times_Z  
    Y 
      &\longrightarrow& 
    \underset{\longrightarrow}{\lim}_D G
    \\
    \big\downarrow && \big\downarrow
    \\
    Y 
      &\underset{f}{\longrightarrow} &
    Z
  }
$$

the canonical morphism

$$
  \label{IsoForPullbackStabilityOfColimis}
  \underset{\underset{d \in D}{\longrightarrow}}{\lim}
  \big(
    G(d) \times_Z Y
  \big)
    \overset{\sim}{\longrightarrow}
  \big(
    \underset{\underset{d \in D}{\longrightarrow}}{\lim}
    G(d)
  \big) \times_Z Y
$$

is an [[isomorphism]].  

\end{definition}



This says equivalently that every [[pullback]] [[functor]] $f^* \colon C/Z \longrightarrow C/Y$ [[preserved limit|preserves]] $D$-colimits.

Similar definitions apply for [[higher categories]].

\begin{proposition}
The condition in Def. \ref{BasicDefinition} is equivalent to the following:

For every functor $G \colon D \to C$ and every morphism $f : Y \to \underset{\longrightarrow}{\lim}_D G$, if we define $Y(d)$ as the pullback of $f$ along the coprojection $\iota_d : G(d) \to \underset{\longrightarrow}{\lim}_D G$, then the induced morphism $\underset{\underset{d \in D}{\longrightarrow}}{\lim} Y(d) \to Y$ is an isomorphism. 
\end{proposition}
\begin{proof}
The implication $\implies$ follows by applying Def. \ref{BasicDefinition} to $Z = \underset{\longrightarrow}{\lim}_D G$ and the identity morphism, 
The converse implication $\impliedby$ follows by applying the assumption to the morphism (eq:IsoForPullbackStabilityOfColimis) and the cancelling rule for pullbacks.
\end{proof}

\begin{proposition}
The condition in Def. \ref{BasicDefinition} is equivalent to the universality condition given at [[van Kampen colimit#universality_and_descent|van Kampen colimit]].
\end{proposition}
\begin{proof}
Observe that, given a [[natural transformation]] $\alpha' : F' \Rightarrow G'$, the diagram

$$
  \array{
    F'(*) 
      &\overset{\alpha'_*}{\longrightarrow}& 
    \underset{\longrightarrow}{\lim}_D G
    \\
    \mathllap{^\id}\big\downarrow 
      && 
    \big\downarrow\mathrlap{^\id}
    \\
    F'(*) 
      &\underset{\alpha'_*}{\longrightarrow} & 
    \underset{\longrightarrow}{\lim}_D G
  }
$$

is a degenerate [[pullback]] square, hence there is a canonical isomorphism

$$
  \underset{\underset{d \in D}{\longrightarrow}}{\lim}
  \big(
    G(d) \times_{\underset{\longrightarrow}{\lim}_D G} F'(*)
  \big) 
    \simeq 
  F'(*)
  \mathrlap{\,.}
$$

But if $\alpha'$ is [[equifibered natural transformation|equifibered]], we have $G(d) \times_{\underset{\longrightarrow}{\lim}_D G} F'(*) \simeq F(d)$, hence we get the desired isomorphism $F'(*) \simeq \underset{\longrightarrow}{\lim}_D F$.

Conversely, given a pullback diagram as above, let $F' = f^* \circ G'$ (viewing $G'$ as a functor $D \to C/Z$ and remembering that colimits in $C/Z$ are [[over category#ColimitInSliceAreReflectedByColimitsInPlainCategory|computed]] as colimits in $C$) and $\alpha' \colon F' \Rightarrow G'$ the natural transformation induced by the pullback projections, which is [[equifibered natural transformation|equifibered]] as a consequence of the [[pasting law for pullbacks]]. Then $f^* \circ G'$ is a colimiting cocone, which is to say that $f^*$ preserves $colim_D G$.
\end{proof}


## Examples

### Toposes

\begin{example}\label{InTopoi}
The stability of all colimits is one of [[Giraud's axioms]] that characterize [[Grothendieck toposes]] in the [[category theory|1-categorical context]] and Grothendieck-Rezk-Lurie [[(∞,1)-toposes]] in the [[higher category theory|higher categorical context]].  

The fact that colimits are stable in toposes can be seen from the characterization of toposes as left-exact reflective subcategories of presheaf categories as follows:

* First observe that colimits are stable in $C =$ [[Set]].

* Now colimits are stable for $C =$ a [[presheaf]] category $[S^{op},Set]$, since colimits in such $C$ are computed objectwise in $Set$.  (See [[limits and colimits by example]].)

* Finally, stability of colimits is preserved in left exact reflective subcategories, since the reflector preserves both colimits and pullbacks.

For [[(∞,1)-toposes]], this is [[Higher Topos Theory|HTT, theorem 6.1.0.6 (3) ii)]].


\end{example}.

### Non-toposes

Generalizing Ex. \ref{InTopoi}:
\begin{example}
Colimits are stable in any [[locally cartesian closed category]]: In that case the pullback functors $f^*$ all have [[right adjoints]].  

Conversely, if $C$ is cocomplete with all stable colimits, and the [[adjoint functor theorem]] applies to all its slice categories, then it is locally cartesian closed.
\end{example}

\begin{example}
Colimits are also stable in any [[exact category|exact]] infinitary [[extensive category]], since all colimits can be constructed out of coproducts, images, and [[quotients]] by [[equivalence relations]], which are all pullback-stable in an exact and infinitary-extensive category.
\end{example}

\begin{example}
A [[counterexample]]:

* Colimits are not stable $C = $ [[Ab]].

\end{example}


## Properties

### Relation to commutativity and distributivity

Although stability of colimits appears as a sort of "commutativity" between colimits and pullbacks, it is not literally an instance of [[commutativity of limits and colimits]].  It is an *example* of the latter if the [[colimit]] over $D$ of the diagram constant on a single object (such as $Y$) is that single object.  For ordinary colimits in [[category theory]] this is a mild condition,  requiring $D$ to be a [[connected category]]; but in [[higher category theory]] this becomes an ever stronger condition; for [[colimits in an (infinity,1)-category]] it means that the [[infinity-groupoid]] generated by $D$ is [[contractible homotopy type]] (see [this corollary](infinity-limit#EveryInfinityGroupoidIsHomotopyColimitOfConstantFunctorOverItself)).

It *is* generally true that (eq:IsoForPullbackStabilityOfColimis) is an example of _[[distributivity of limits over colimits]]_; see [there](distributivity+of+limits+over+colimits#PullbackStableColimits).


## Related concepts

* [[van Kampen colimit]]
* [[pullback-stability]]

## References 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ (Section 6.1.1) 

[[!redirects universal colimit]]
[[!redirects universal colimits]]
[[!redirects stable colimit]]
[[!redirects stable colimits]]
[[!redirects pullback-stable colimit]]
[[!redirects pullback-stable colimits]]
