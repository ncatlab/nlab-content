
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $A$ a [[monoid]] equipped with an [[action]] on an [[object]] $V$ (often: a [[group]] with a [[group action]] on $V$), an **invariant** of the action is an [[generalized element|element]] of $V$ which is taken by the action to itself, hence which is a [[fixed point]] for all the operations of the monoid.

## Definitions

A robust definition of invariants that generalizes to [[homotopy theory]] is via the expression of actions as [[action groupoids]] regarded as sitting over [[delooping]] [[groupoids]], as discussed at _[[infinity-action]]_ and at _[[geometry of physics -- representations and associated bundles]]_.

We describe how the ordinary concept of invariants is recovered from this perspective and then consider its immediate generalizations to [[(infinity,1)-topos theory]] and its formalization in [[homotopy type theory]].

### Via sections of action groupoid projections
 {#ViaSectionsOfActionGroupoidProjections}

+-- {: .num_prop}
###### Proposition

For $G$ a [[discrete group]], $\rho$ a $G$-[[action]] on some set $S$, then the set of [[invariants]] of that action is equivalent to the groupoid of [[sections]] of the [[action groupoid]] projection of [this proposition](geometry+of+physics+--+representations+and+associated+bundles#MapFromActionGroupoidOnSetBackToBG), corresponding to the action via [this proposition](geometry+of+physics+--+representations+and+associated+bundles#EquivalenceOfPermutationRepresentationsWithActionGroupodsInSlice).

=--

+-- {: .proof}
###### Proof

The sections in question are diagrams in [[Grpd]] of the form

$$
  \array{
    \mathbf{B}G && \stackrel{\sigma}{\longrightarrow} && S//G
    \\
    & {}_{\mathllap{id}}\searrow 
    &\swArrow_{\mathrlap{\simeq}}& 
    \swarrow_{\mathrlap{p_\rho}}
    \\
    && \mathbf{B}G
  }
  \,,
$$

hence the groupoid which they form is equivalently the [[hom-groupoid]]

$$
  Grpd_{/\mathbf{B}G}(id_{\mathbf{B}G}, p_\rho)
  \in Grpd
$$

in the [[slice (infinity,1)-category|slice]] of [[Grpd]] over $\mathbf{B}G$. 
As in the proof of [this proposition](geometry+of+physics+--+representations+and+associated+bundles#IntertwinersOfPermutationActionAsSliceHoms), with the fibrant presentation $(p_\rho)_\bullet$ of [this proposition](geometry+of+physics+--+representations+and+associated+bundles#MapFromActionGroupoidOnSetBackToBG), this is equivalently given by strictly commuting diagrams of the form

$$
  \array{
    (\mathbf{B}G)_\bullet && \stackrel{\sigma_\bullet}{\longrightarrow} && (S//G)_\bullet
    \\
    & {}_{\mathllap{id_\bullet}}\searrow &=& \swarrow_{\mathrlap{(p_\rho)_\bullet}}
    \\
    && (\mathbf{B}G)_\bullet
  }
  \,.
$$

These $\sigma$ now are manifestly functors that are the identity on the group labels of the morphisms

$$
  \sigma_\bullet
  \;\colon\;
  \left(
  \array{
    \ast
    \\
    \downarrow^{\mathrlap{g}}
    \\
    \ast
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
    \sigma(\ast)
    \\
    \downarrow^{\mathrlap{g}}
    \\
    \sigma(\ast) & = \rho(\sigma(\ast)(g))
  }
  \right)
  \,.
$$

This shows that they pick precisely those elements $\sigma(\ast) \in S$ which are fixed by the $G$-action $\rho$.

Moreover, since these functors are identity on the group labels, there are no non-trivial [[natural isomorphisms]] between them, and hence the groupoid of sections is indeed a set, the set of invariant elements.

=--

More generally, we may consider sections of these groupoid projections after pulling them back along some cocycle:

+-- {: .num_prop}
###### Proposition

Given an [[associated bundle]] $P \times_G V\to X$ [[modulating morphism|modulated]], as in [this proposition](geometry+of+physics+--+representations+and+associated+bundles#Associated1BundleAsPullbackOfActionGroupoid), by a morphism of [[smooth groupoids]] of the form $g \colon X \longrightarrow \mathbf{B}G$, then its set of [[sections]] is equivalently the groupoid of diagrams

$$
  \array{
    X && \stackrel{\sigma}{\longrightarrow} && S//G
    \\
    & {}_{\mathllap{g}}\searrow 
    &\swArrow_{\mathrlap{\simeq}}& \swarrow_{\mathrlap{p_\rho}}
    \\
    && \mathbf{B}G
  }
  \,,
$$

hence the groupoid of sections is the slice [[hom-groupoid]]

$$
  \Gamma_X(P\times_G V)
  \simeq
  Grpd_{/\mathbf{B}G}(g, p_\rho)
  \,.
$$


=--

+-- {: .proof}
###### Proof

By the defining [[universal property]] of the [[homotopy pullback]] in [this proposition](geometry+of+physics+--+representations+and+associated+bundles#Associated1BundleAsPullbackOfActionGroupoid).

=--

+-- {: .num_remark}
###### Remark

Taken together this means that [[invariants]] of group actions are equivalently the sections of the corresponding [[universal principal bundle|universal]] [[associated bundle]].

=--


### Invariants of $\infty$-group actions
 {#ForInfinityGroupActions}

For $\mathbf{H}$ an [[(∞,1)-topos]],  $G \in Grp(\mathbf{H})$ an [[∞-group]] and 

$$
  * \colon \mathbf{B} G 
  \;\vdash\; 
  V(*) \colon Type
$$ 

an [[∞-action]] of $G$ on $V \in \mathbf{H}$, the type of invariants is the absolute [[dependent product]]

$$
  \vdash 
  \textstyle{\prod_{* \colon \mathbf{B}G}} 
  V(*) \colon Type
  \,.
$$

The [[connected components]] of this is equivalently the [[group cohomology]] of $G$ with [[coefficients]] in the [[infinity-module|$\infty$-module]] $V$.



## Properties

+-- {: .num_prop #TakingInvariantsForFiniteGroupCommutesWithTaingHomologyInCharZero}
###### Proposition
**(in [[characteristic zero]], [[invariants]] for [[finite group]] are compatible with [[chain homology]])

Let $(V_\bullet, \partial)$ be a [[chain complex]] over a [[ground field]] of [[characteristic zero]], equipped with an [[action]] by a [[finite group]] $G$. Then taking $G$-invariants commutes with passing to [[chain homology]]:

$$
  H_\bullet((V_\bullet,\partial)^G)
  \;\simeq\;
  H_\bullet((V_\bullet,\partial))^G
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since the [[ground field]] has [[characteristic zero]], [[group averaging]] exists and provides a [[linear map]]

$$
  \array{
    V_\bullet & \overset{p}{\longrightarrow} & V_\bullet^G
    \\
    x &\mapsto& \frac{1}{{\vert G \vert}} \underset{g \in G}{\sum} g(x)
  }
$$

onto the $G$-invariants. 

Now for a [[chain homology]]-class $[x] \in H_\bullet((V_\bullet,\partial))$ being $G$-invariant means that $g[x] \coloneqq [g(x)] = [x]$ for all $g \in G$, which implies that $[x] = [p(x)]$. This means that each invariant homology class has an invariant representative, hence that the map from invariant [[cycles]] to invariant [[chain homology]]-classes

$$
  Z((V_\bullet^G,\partial)) \longrightarrow H_\bullet((V_\bullet,\partial))
$$

is an [[epimorphism]].

Next consider the [[kernel]] of this map, which a priori is $Z((V_\bullet^G,\partial)) \cap B((V_\bullet,\partial))$. It is now sufficient to show that this coincides with the space of $G$-invariant [[boundaries]]:

$$
  Z((V_\bullet^G,\partial)) \cap B((V_\bullet,\partial))
  \;\simeq\;
  B((V_\bullet^G, \partial))
  \,.
$$

It is clear that there is an [[injective map|inclusion]]

$$
  B((V_\bullet^G, \partial)) 
    \hookrightarrow 
  Z((V_\bullet^G,\partial)) \cap B((V_\bullet,\partial))
$$

so it only remains to see that this is also a [[surjection]]. 

To that end, consider any

$$
  x \in Z((V_\bullet^G,\partial)) \cap B((V_\bullet,\partial))
  \,.
$$

Since in particular $x \in B((V_\bullet,\partial))$, there is $y \in V_\bullet$ with $x = \partial y$; and since moreover $x \in V_\bullet(G)$, the above implies that 

$$
  x = p(x) = p(\partial y) = \partial(p y)
$$

and hence that 

$$
  x \in B((V_\bullet^G,\partial)) 
  \,.
$$

=--

## Examples
 {#Examples}

### General

* [[invariant polynomial]]

* [[invariant differential form]]

* [[invariant metric]]

* [[invariant measure]]

* [[j-invariant]]

* [[knot invariant]], [[link invariant]]

  * [[Milnor mu-bar invariant]]

  * [[Vassiliev knot invariant]] ([[universal Vassiliev invariant|universal]])

* * [[topological invariant]], [[homeomorphism invariant]], [[homotopy invariant]]

  * [[k-invariant]]

  * [[Adams e-invariant]]

  * [[f-invariant]]

  * [[Hopf invariant]]

  * [[Kervaire invariant]]

  * [[Casson invariant]]

  * [[Chern-Simons invariant]]

  * [[Gromov-Witten invariant]]

  * [[Donaldson-Thomas invariant]]

  * [[eta invariant]]

* [[Dickson invariant]]


### Invariant cocycles on principal $\infty$-bundles
 {#ExamplesInvariantCocyclesOnPrincipalInfinityBundles}

Some illustration of the notion of invariants of [[infinity-action|$\infty$-actions]] from [above](#ForInfinityGroupActions).

Consider:

* $\mathbf{H}$ an [[(infinity,1)-topos|$\infty$-topos]],

* $G \in Grp(\mathbf{H})$ an [[infinity-group|$\infty$-group]] [[groupoid object in an (infinity,1)-category|object in]] $\mathbf{H}$,

* $G \curvearrowright P \in G Act(\mathbf{H})$ an [[infinity-action|$\infty$-action]],

* $X \coloneqq P \sslash G$ its [[homotopy quotient]].

Note that the quotient [[coprojection]] is a $G$-[[principal infinity-bundle|principal $\infty$-bundle]]:

\begin{tikzcd}
  G 
  \ar[r]
  &
  P
  \ar[d]
  \\
  {}
  &
  X
\end{tikzcd}

and every $G$-principal $\infty$-bundle is of this form (cf. [[schreiber:EPB]]v2 Prop. 1.2.1, [p. 15](/schreiber/files/EquivariantInfinityBundles_251013.pdf#page=15)).


Further consider:

* $\mathcal{A} \in \mathbf{H}$ any object,

  to be thought of as a [[moduli stack]] for some kind of structure, for instance for [[differential forms]] or [[differential cohomology]],

* $G \curvearrowright \mathcal{A} \coloneqq G \curvearrowright \ast \times \mathcal{A} \in G Act(\mathbf{H})$ its incarnation as a [[trivial action|trivial $G$-action]],

* $G \curvearrowright [P, \mathcal{A}] \coloneqq  \big[G \curvearrowright P,\, G \curvearrowright \mathcal{A} \big] \in G Act(\mathbf{H})$ the [[internal hom]] of $G$-actions, being the [[mapping space]] $[P,\mathcal{A}]$ equipped with the induced [[conjugation action]],

* $[P, \mathcal{G}]^G$ its $G$-[[fixed locus]]

(cf. [[schreiber:DCCT]]v1, Def. 3.6.232; [p. 339](https://arxiv.org/pdf/1310.7930v1#page=339);  [[schreiber:DCCT]]v2 Def. 5.1.278, [p. 443](/schreiber/files/dcct170811.pdf#page=443)).

\begin{proposition}
We have a [[natural equivalence]]:

$$
  [P, \mathcal{A}]^G
  \;\simeq\;
  [X, \mathcal{A}]
  \,.
$$
\end{proposition}

In words: "$G$-Invariant $\mathcal{A}$-cocycles on the total space $P$ of a $G$-principle bundle are equivalently plain $\mathcal{A}$-cocyles on the base space $X$."

\begin{proof}
Recall the equivalence ([[schreiber:EPB]]v2 Prop. 1.2.1, [p. 15](/schreiber/files/EquivariantInfinityBundles_251013.pdf#page=15)):

\begin{tikzcd}
  G \mathrm{Act}(\mathbf{H})
  \ar[r, "{ \sim }"]
  &
  \mathbf{H}_{/\mathbf{B}G}
  \\[-40pt]
  G \curvearrowright X
  \ar[r, |->, shorten=4pt]
  &
  \big(
    p_{X} \colon X /\!\!/ G \to \mathbf{B}G
  \big)
  \mathrlap{\,,}
\end{tikzcd}

under which forming [[fixed loci]] is right [[base change]] to the point: $(-)^G \leftrightarrow \prod_{\mathbf{B}G}$.

Hence in our case:
$$
  [P,\mathcal{A}]^G
  \;\;\leftrightarrow\;\;
  \big[P \sslash G, \mathcal{A}\sslash G\big]_{\mathbf{B}G}
  \,\coloneqq\,
  \prod_{\mathbf{B}G}
  \big[
    p_P, p_{\mathcal{A}}
  \big]
  \mathrlap{\,.}
$$

Now observe that have have a [[homotopy pullback]] square of this form ([[schreiber:EPB]]v2 Lem. 4.2.69 with Def. 4.2.66, [p. 121](/schreiber/files/EquivariantInfinityBundles_251013.pdf#page=121)):

\begin{tikzcd}
  \big[
    P /\!\!/ G
    ,\,
   \mathcal{A} \times \mathbf{B}G
  \big]_{ \mathbf{B}G }
  \ar[r]
  \ar[d]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  \big[
    P /\!\!/ G
    ,\,
    \mathcal{A}\times \mathbf{B}G
  \big]
  \ar[
    d,
    "{ (\mathrm{pr}_2)_\ast }"
  ]
  \\
  \ast
  \ar[
    r,
    "{ \vdash \, p_{{}_P} }"
  ]
  &
  \big[
    P /\!\!/ G
    ,\,
   \mathbf{B}G
  \big]
  \mathrlap{\,,}
\end{tikzcd}

where we used in the top row that the $G$-action on $\mathcal{A}$ being trivial (by assumption) means equivalently that its [[homotopy quotient]] is given by the product with the [[delooping]] $\mathbf{B}G$ of $G$:

\begin{tikzcd}
  \mathcal{A} /\!\!/ G
  \ar[rr, "{ \sim }"]
  \ar[dr, "{ p_{\mathcal{A}} }"{swap}]
  &[-40pt]&[-40pt]
  \mathcal{A} \times \mathbf{B}G
  \ar[dl, "{ \mathrm{pr}_2 }"]
  \\[-10pt]
  & 
  \mathbf{B}G
  \mathrlap{\,.}
\end{tikzcd}

But the [[internal hom]] $\big[P \sslash G,-\big]$ ([[adjoints preserve (co-)limits|being]] a [[right adjoints]]) [[preserved limit|preserves limits]], whence

$$
  \big[
    P \sslash G 
    ,\,
    \mathcal{A} \times \mathbf{B}G
  \big]
  \,\simeq\,
  \big[
    P \sslash G 
    ,\,
    \mathcal{A}
  \big]
    \times
  \big[
    P \sslash G 
    ,\,
    \mathbf{B}G
  \big]  
  \,,
$$

and since pullbacks commute with products, the above pullback square is seen to be equivalent to:

\begin{tikzcd}
  \big[
    P /\!\!/ G
    ,\,
   \mathcal{A}
  \big]
  \times
  \ast
  \ar[r]
  \ar[
    d,
    "{ p \,\times\, \mathrm{id} }"
  ]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  \big[
    P /\!\!/ G
    ,\,
   \mathcal{A}
  \big]
  \times
  \big[
    P /\!\!/ G
    ,\,
   \mathbf{B}G
  \big]
  \ar[
    d,
    "{ p \,\times\, \mathrm{id} }"
  ]
  \\
  \ast
  \times \ast
  \ar[
    r,
    "{ \mathrm{id} \,\times\, \vdash \, p_{{}_P} }"
  ]
  &
  \ast 
  \times
  \big[
    P /\!\!/ G
    ,\,
   \mathbf{B}G
  \big]
  \mathrlap{\,.}
\end{tikzcd}

Finally, since $P \sslash G \,\simeq\, X$, this proves the claim.
\end{proof}




## Related concepts

* [[invariant theory]], [[geometric invariant theory]]

* [[group averaging]], [[norm map]]

* [[coinvariant]]

* [[stabilizer subgroup]]

* [[gauge invariance]]




\linebreak

[[!include homotopy type representation theory -- table]]




[[!redirects invariants]]

[[!redirects invariance]]



