
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

## Idea

Any $\infty$-groupoid $G$ gives rise to an $(\infty,1)$-topos $[G^{op},\infty Gpd]$, which is equivalent to $\infty Gpd / G$.  The $(\infty,1)$-toposes of this form are, by definition, those for which the unique [[(∞,1)-geometric morphism]] to $\infty Gpd$ is a [[local homeomorphism of toposes]].  This construction embeds $\infty Gpd$ as a full [[sub-(∞,1)-category]] of [[(∞,1)Topos]].

In particular, $(\infty,1)$-toposes of the above form are [[locally ∞-connected (∞,1)-topos|locally ∞-connected]].  Let $LC(\infty,1)Topos$ denote the full sub-(∞,1)-category of [[(∞,1)Topos]] determined by the locally ∞-connected objects.  Then $\infty Gpd$ (as the category of local homeomorphisms over $\infty Gpd$) is [[reflective sub-(∞,1)-category|reflective]] in $LC(\infty,1)Topos$, and the [[reflector]] constructs the **fundamental ∞-groupoid** of a locally ∞-connected (∞,1)-topos.

Equivalently, one may say that a locally ∞-connected (∞,1)-topos has a [[shape of an (∞,1)-topos|shape]] which is [[representable functor|representable]], and its fundamental ∞-groupoid is the representing object.

## Definition

Let $E$ be a locally ∞-connected (∞,1)-topos, with adjoint string $\Pi\dashv LConst \dashv \Gamma\colon E \to \infty Gpd$.  Then the **fundamental ∞-groupoid** of $E$ is $\Pi(*)$, where $*$ is the [[terminal object]] of $E$.  In other words, it is the [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy ∞-groupoid]] of the terminal object of $E$.

To see that this agrees with the above definition, we observe that the shape of $E$ is equivalently defined as $\Gamma \circ LConst$, whereas for any ∞-groupoid $A$ we have

$$
\begin{aligned}
Shape(E)(A) &= \Gamma(LConst(A))\\
&= Hom_{\infty Grpd}(*, \Gamma(LConst(A)))\\
&= Hom_{E}(LConst(*), LConst(A)) \\
&= Hom_{E}(*, LConst(A)) \\
&= Hom_{\infty Grpd}(\Pi(*),A).
\end{aligned}
$$

## Related concepts

* The [[fundamental ∞-groupoid]] of a [[topological space]] is close to a special case of this.  At least when $X$ is a locally contractible space, we can identify the fundamental ∞-groupoid of $X$ with that of the (∞,1)-topos $Sh(X)$.

* The [[shape of an (∞,1)-topos]] is a generalization of this to non-locally-∞-connected (∞,1)-toposes.

* [[geometric homotopy groups in an (∞,1)-topos]] are a generalization to objects of the topos other than the terminal object.

[[!redirects fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]]
[[!redirects fundamental ∞-groupoid of an (∞,1)-topos]]
