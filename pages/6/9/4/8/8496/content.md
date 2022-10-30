
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

For $A$ a [[monoid]] equipped with an [[action]] on an object $V$, an **invariant** of the action is an [[generalized element|element]] of $V$ which is taken by the action to itself.

## Definitions

A robust definition of invariants that generalizes to [[homotopy theory]] is via the expression of actions as [[action groupoids]] regarded as sitting over [[delooping]] [[groupoids]], as discussed at _[[infinity-action]]_ and at _[[geometry of physics -- representations and associated bundles]]_.

We describe how the ordinary concept of invariants is recovered from this perspective and then consdider its immediate generalizations to [[(infinity,1)-topos theory]] and its formalization in [[homotopy type theory]].

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
    \swarrow_{\mathrlap{p_\phi}}
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
    & {}_{\mathllap{id_\bullet}}\searrow &=& \swarrow_{\mathrlap{(p_\phi)_\bullet}}
    \\
    && (\mathbf{B}G)_\bullet
  }
  \,.
$$

These $\sigma$ now are manifestly functors that are the identiy on the group labels of the morphisms

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
    &\swArrow_{\mathrlap{\simeq}}& \swarrow_{\mathrlap{p_\phi}}
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
  * : \mathbf{B} G \vdash : V(*) : Type
$$ 

an [[∞-action]] of $G$ on $V \in \mathbf{H}$, the type of invariants is the absolute [[dependent product]]

$$
  \vdash \prod_{* : \mathbf{B}G} V(*) : Type
  \,.
$$

The connected components of this is equivalently the [[group cohomology]] of $G$ with [[coefficients]] in the [[infinity-module]] $V$.


## Related concepts

* [[group averaging]]

* [[stabilizer subgroup]]

* [[invariant theory]], [[invariant polynomial]]

* [[gauge invariance]]

[[!include homotopy type representation theory -- table]]




[[!redirects invariants]]
