
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Every [[(∞,1)-topos]] $E$ has a [[shape of an (∞,1)-topos|shape]] $Shape(E) \in Pro\infty Grpd$. When $E$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] then this is a genuine [[∞-groupoid]] $\Pi(E) \in $ [[∞Grpd]]. We may think of this as the [[fundamental ∞-groupoid]] of the $(\infty,1)$-topos regarded as a generalized [[space]].

But also every [[locally ∞-connected (∞,1)-topos]] has an _internal_ notion of [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] for objects of $E$, denoted $\Pi_E : E \to \infty Grpd$. Applied to its [[terminal object]] this does agree with the fundamental ∞-groupoid of the topos:

$$
  \Pi(E) \simeq \Pi_E(*)
  \,.
$$

Conversely, for an object $X\in E$, the fundamental ∞-groupoid $\Pi_E(X)$ internal to $E$ can be identified with the fundamental ∞-groupoid of the locally ∞-connected (∞,1)-topos $E/X$.


## Definition


+-- {: .un_def}
###### Definition

For $(\Pi_E \dashv \Gamma_E \dashv LConst_E) :  E \to \infty Grpd$ a [[locally ∞-connected (∞,1)-topos]] we say its **fundamental $\infty$-groupoid** is

$$
  \Pi(E) := \Pi_E(*)
  \,,
$$

where $*$ is the [[terminal object]] of $E$.  

In other words, it is the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|internal fundamental ∞-groupoid]] of the terminal object of $E$.

=--

## Properties


Let $\mathbf{H}$ be a locally $\infty$-connected $(\infty,1)$-topos and $X \in \mathbf{H}$ an [[object]]. Then also the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is locally $\infty$-connected (as discussed there). 

We have then two different definitions of the fundamental $\infty$-groupoid of $X$: once as $\Pi_{\mathbf{H}}(X)$ -- the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]  -- and once as $\Pi(\mathbf{H}/X)$.

+-- {: .un_prop}
###### Proposition

These agree:

$$
  \Pi_{\mathbf{H}}(X) \simeq \Pi(\mathbf{H}/X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since $X \stackrel{Id}{\to} X$ is the [[terminal object]] in $\mathbf{H}/X$ we have by definition

$$
  \Pi(\mathbf{H}/X) = \Pi_{\mathbf{H}/X}(Id_X)
  \,.
$$

Now observe that $\Pi_{\mathbf{H}/X} = \Pi_{\mathbf{H}} \circ X_!$ since the terminal [[global section]] geometric morphism of the over-topos is

$$
  \mathbf{H}/X 
    \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
  \mathbf{H}
  \stackrel{\overset{\Pi_{\mathbf{H}}}{\to}}{\stackrel{\overset{LConst_{\mathbf{H}}}{\leftarrow}}{\underset{\Gamma_{\mathbf{H}}}{\to}}}
  \infty Grpd
$$

and that $X_!$ in the [[etale geometric morphism]] is the projection map that sends $Y \stackrel{}{\to} X$ to $Y$.
=--


+-- {: .un_def}
###### Definition

Let $LC(\infty,1)Topos$ denote the full [[sub-(∞,1)-category]] of [[(∞,1)Topos]] determined by the locally ∞-connected objects.  

=--


+-- {: .un_prop}
###### Proposition

The $(\infty,1)$-category $\infty Gpd$ (as the category of local homeomorphisms over $\infty Gpd$) is [[reflective sub-(∞,1)-category|reflective]] in $LC(\infty,1)Topos$, 

$$
  \infty Grpd 
    \stackrel{\overset{\Pi}{\leftarrow}}{\hookrightarrow}
  LC(\infty,1)Topos
$$

with the reflector given by forming the fundamental $\infty$-groupoid.

=--


+-- {: .proof}
###### Proof

Any [[∞-groupoid]] $G$ gives rise to an [[(∞,1)-presheaf (∞,1)-topos]] $PSh(G) = [G^{op},\infty Gpd]$, which by the [[(∞,1)-Grothendieck construction]] is equivalent to the [[over-(∞,1)-topos]] $\infty Gpd / G$.  The $(\infty,1)$-toposes of this form are, by definition, those for which the unique [[(∞,1)-geometric morphism]] to $\infty Gpd$ is a [[local homeomorphism of toposes]].  This construction embeds $\infty Gpd$ as a full [[sub-(∞,1)-category]] of [[(∞,1)Topos]]:

$$
  PSh(-) : \infty Grpd \hookrightarrow LC(\infty,1)Topos
  \,.
$$

since in particular the $(\infty,1)$-toposes $PSh(G)$ are [[locally ∞-connected (∞,1)-topos|locally ∞-connected]].  


To show that $\Pi$ is a [[left adjoint|left]] [[adjoint (∞,1)-functor]] to $PSh(-)$ we demonstrate a natural hom-equivalence 

$$
  LC(\infty,1)Topos(E,(\infty,1)PSh(A)) \simeq \infty Grpd(\Pi_E(*), A)
$$ 

for $E\in LC(\infty,1)Topos$ and $A \in \infty Grpd$.

At [[shape of an (∞,1)-topos]] it is shown that we have a natural equivalence

$$
  (\infty,1)Topos(E, PSh(A)) \simeq \Gamma_E LConst_E G =: Shape(E)(A)
  \,.
$$

Now observe that furthermore we have a sequence of natural equivalences

$$
\begin{aligned}
Shape(E)(A) &= \Gamma(LConst(A))\\
&\simeq \infty Grpd(*, \Gamma(LConst(A)))\\
&\simeq E(LConst(*), LConst(A)) \\
&\simeq E(*, LConst(A)) \\
&\simeq \infty Grpd(\Pi_E(*),A).
\end{aligned}
  \,.
$$


=--

+-- {: .un_remark}
###### Remark

So equivalently, one may say that a locally ∞-connected (∞,1)-topos $E$ has a [[shape of an (∞,1)-topos|shape]] which is [[representable functor|representable]], and its [[fundamental ∞-groupoid]] $\Pi(\mathbf{H})$ is the representing object.

=--

## Examples

+-- {: .un_prop}
###### Proposition

For $X$ a [[locally contractible topological space]], we have an equivalence

$$
  \Pi ((\infty,1)Sh(X)) \simeq Sing X
$$

between the ordinary [[fundamental ∞-groupoid]] of $X$ defined by the [[singular simplicial complex]] and the topos-theoretic fundamental $\infty$-groupoid of the [[(∞,1)-sheaf (∞,1)-topos]] $(\infty,1)Sh(X)$ over $X$.

=--

+-- {: .proof}
###### Proof

Details are at [[geometric homotopy groups in an (∞,1)-topos]].

=--

More generally the [[shape of an (∞,1)-topos]] of $(\infty,1)Sh(X)$ reproduces the [[shape theory]] of $X$.

## Related concepts

* [[fundamental groupoid]], [[fundamental ∞-groupoid]], 

* [[homotopy group]], [[homotopy groups in an (∞,1)-topos]]

* **fundamental $\infty$-groupoid in a locally $\infty$-connected $(\infty,1)$-topos / [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|of a locally ∞-connected (∞,1)-topos]]




[[!redirects fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]]
[[!redirects fundamental ∞-groupoid of an (∞,1)-topos]]
