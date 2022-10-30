

> This entry contains one chapter of _[[geometry of physics]]_. See there for background and context.

> previous chapters: _[[geometry of physics -- groups|groups]]_, _[[geometry of physics|principal bundles]]_

> next chapter: _[[geometry of physics -- modules|modules]]_

***

#Contents#
* table of contents
{:toc}

## Representations and associated bundles

The mathematical term _group_ is short for _group of [[symmetries]]_, namely of symmetries of some object. That a group $G$ is the group of symmetries of some $V$ is technically expressed by there being an [[action]] of $G$ on $X$. Generally, or at least if $V$ and this representation are suitably linear, this is also called a [[representation]] of $G$ (namely a representation of the abstract group as an actual group of symmetries).

The chapter _[[geometry of physics -- groups]]_ discusses in detail how in geometric [[homotopy theory]] groups $G$ are equivalent to [[groupoids]] $\mathbf{B}G$ which have a single object and $G$ as the [[automorphisms]] of that object, if only $\mathbf{B}G$ is regarded as a [[pointed object]] via the canonical base point inclusion $\ast \to \mathbf{B}G$.

This perspective turns out to be exceedingly useful for the discussion of the representations of $G$: these turn out to be equivalent simply to $\mathbf{B}G$-[[dependent types]], hence to any [[bundles]] $E \to \mathbf{B}G$ over $G$. Given such, then the object that $V$ that this encodes an action on is the [[homotopy fiber]] of this map

$$
  \array{
     V &\longrightarrow& E
     \\
     && \downarrow
     \\
     && \mathbf{B}G
  }
  \,.
$$ 

In traditional literature this is familiar in special cases, where the perspective is usually the opposite: given an [[action]] of $G$ on $V$, then there is the [[associated bundle]] $E = \mathbf{E}G \times_G V$ which is associated to the $G$-[[universal principal bundle]] via the action.

Indeed, in the generality of geometric homotopy theory, this association is an equivalence, so that actions and universal associated bundles are essentially the same concept.


### Model Layer

##### 1-Representations of 1-Groups
 {#1RepresentationsOf1Groups}
 
We discuss here ordinary [[groups]] (i.e. [[infinity-groups]] which are just 1-groups), and their ordinary [[actions]] and ordinary [[associated bundles]]. Even that ordinary case profits from its formulation via [[action groupoids]], but its key advantage is that this formulation seamlessly generalizes. 

###### Actions
 {#ActionsOf1Groups}

We discuss here traditional concept of [[discrete groups]] [[action|acting]] on a [[sets]] ("[[permutation representations]]") but phrased in terms of [[action groupoids]] [[slice (infinity,1)-category|sliced]] over [[delooping]] groupoids. The discussion immediately, and essentially verbatim, generalizes to pre-smooth groupoids and to [[smooth groupoids]] proper.


Write [[Grpd]] for the [[(2,1)-category]] of [[groupoids]], the [[full sub-(infinity,1)-category]] of [[∞Grpd]] on the [[1-truncated objects]].

We write 

$$
  X_\bullet = (X_1 \stackrel{\longrightarrow}{\longrightarrow} X_0)
$$

for a [[groupoid object]] given by an explicit choice of set of objects and of morphisms and then write $X \in Grpd$ for the object that this presents in the $(2,1)$-category. Given any such $X$, we recover a presentation by choosing any [[essentially surjective functor]] $S \to X$  (an [[atlas]]) out of a set $S$ (regarded as a groupoid) and setting

$$
  X_\bullet = (S \underset{X}{\times} S \stackrel{\longrightarrow}{\longrightarrow} S)
$$

hence taking $S$ as the set of objects and the [[homotopy fiber product]] of $S$ with itself over $X$ as the set of morphism.


For $G$ a [[discrete group]], then $\mathbf{B}G$ denotes the [[groupoid]] presented by $(\mathbf{B}G)_\bullet = (G \stackrel{\longrightarrow}{\longrightarrow}\ast)$ with [[composition]] operation given by the product in the group. Of the two possible ways of making this identification, we agree to use

$$
  \array{
    && \ast
    \\
    & {}^{\mathllap{g_1}}\nearrow && \searrow^{\mathrlap{g_2}}
    \\
    \ast && \underset{g_1 \cdot g_2}{\longrightarrow} && \ast
  }
  \,.
$$

+-- {: .num_defn #Action1Groupoid}
###### Definition

Given a [[discrete group]] $G$ and an [[action]] $\rho$ of $G$ on a [[set]] $S$

$$
  \rho \colon S \times G \longrightarrow S
$$

then the corresponding _[[action groupoid]]_ is 

$$
  (S//G)_\bullet
  \coloneqq
  \left(
    S\times G
    \stackrel{\overset{p_1}{\longrightarrow}}{\underset{\rho}{\longrightarrow}}
    S
  \right)
$$

with [[composition]] given by the product in $G$. Hence the [[objects]] of $S$ are the elements of $S$, and the morphisms $s \stackrel{}{\longrightarrow } t$ are labeled by elements $g\in G$ and are such that $t = \rho(s)(g)$. 

=--

Schematically:

$$
  (S//G)_\bullet =
  \left\{
    \array{
      && \rho(s)(g)
      \\
      & {}^{\mathllap{g_1}}\nearrow && \searrow^{\mathrlap{g_2}}
      \\
      s && \underset{g_1 g_2}{\longrightarrow} && \rho(s)(g_1 g_2)
    }
  \right\}
  \,.
$$

+-- {: .num_example}
###### Example

For the unique and trivial $G$-action on the singleton set $\ast$, we have

$$
  \ast//G \simeq \mathbf{B}G
  \,.
$$

=--

This makes it clear that:

+-- {: .num_prop #MapFromActionGroupoidOnSetBackToBG}
###### Proposition

In the situation of def. \ref{Action1Groupoid}, 
there is a canonical morphism of groupoids

$$
  (p_\rho)_\bullet \;\colon\; (S//G)_\bullet \longrightarrow (\mathbf{B}G)_\bullet
$$

which, in the above presentation, forgets the labels of the objects and is the identity on the labels of the morphisms.

This morphism is an [[isofibration]].

=--

+-- {: .num_prop #IntertwinersOfPermutationActionAsSliceHoms}
###### Proposition

For $G$ a [[discrete group]], given two $G$-[[actions]] $\rho_1$ and $\rho_2$ on sets $S_1$ and $S_2$, respectively, then there is a [[natural equivalence]] between the set of action [[homomorphisms]] ("[[intertwiners]]") $\rho_1 \to \rho_2$, regarded as a groupoid with only identity morphisms, and the [[hom groupoid]] of the [[slice (infinity,1)-category|slice]] $Grpd_{/\mathbf{B}G}$ between their [[action groupoids]] regarded in the slice via the maps from prop. \ref{MapFromActionGroupoidOnSetBackToBG}

$$
  G Act(\rho_1,\rho_2)
  \simeq
  Grpd_{/\mathbf{B}G}(p_{\rho_1}, p_{\rho_2})
  \,.
$$

=--

+-- {: .proof}
###### Proof

One quick way to see this is to use, via the discussion at _[[slice (infinity,1)-category]]_, that the [[hom-groupoid]] in the slice is given by the [[homotopy pullback]] of unsliced hom-groupoids

$$
  \array{
    Grpd_{/\mathbf{B}G}(p_{\rho_1}, p_{\rho_2})
    &\longrightarrow&
    Grpd(S_1//G, S_2//G)
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{Grpd(S_1//G,p_{\rho_2})}}
    \\
    \ast &\stackrel{}{\longrightarrow}& Grpd(S_1//G, \mathbf{B}G)
  }
  \,.
$$

Now since $(p_{\rho_2})_\bullet$ is an [[isofibration]], so is $Grpd((S_1//G)_\bullet, (p_{\rho_2})_\bullet)$, and hence this is computed as an ordinary pullback (in the above presentation). That in turn gives the [[hom-set]] in the 1-categorical slice. This consists of functors

$$
  \phi_\bullet \colon (S_1//G)_\bullet \longrightarrow (S_1//G)_\bullet
$$

which strictly preserves the $G$-labels on the morphisms. These are manifestly the intertwiners.

$$
  \phi_\bullet
  \;\colon\;
  \left(
  \array{
    s
    \\
    \downarrow^{\mathrlap{g}}
    \\
    \rho(s)(g)
  }
  \right)
  \mapsto
  \left(
  \array{
    \phi(s)
    \\
    \downarrow^{\mathrlap{g}}
    \\
    \phi(\rho(s)(g)) & = \rho(\phi(s))(g)
  }
  \right)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The [[homotopy fiber]] of the morphism in prop. \ref{MapFromActionGroupoidOnSetBackToBG} is [[equivalence of groupoids|equivalent]] to the set $S$, regarded as a groupoid with only identity morphisms, hence we have a [[homotopy fiber sequence]] of the form

$$
  \array{
    S &\longrightarrow& S//G
    \\
    && \downarrow^{\mathrlap{p_\rho}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

In the presentation $(S//G)_\bullet$ of def. \ref{Action1Groupoid}, $p_\rho$ is an [[isofibration]], prop. \ref{MapFromActionGroupoidOnSetBackToBG}. Hence the [[homotopy fibers]] of $p_\rho$ are equivalent to the ordinary fibers of $(p_\rho)_\bullet$ computed in the 1-category of 1-groupoids. Since $(p_\rho)_\bullet$ is the identity on the labels of the morphisms in this presentation, this ordinary fiber is precisely the sub-groupoid of $(S//G)_\bullet$ consisting of only the identity morphismss, hence is the set $S$ regarded as a groupoid.

=--

Conversely, the following construction extract a group action from a homotopy fiber sequence of groupoids of this form.

+-- {: .num_defn #ActionMapFromFiberSequenceSetToGroupoidToBG}
###### Definition

Given a [[homotopy fiber sequence]] of [[groupoids]] of the form

$$
  \array{
    S &\stackrel{i}{\longrightarrow}& E
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    && \mathbf{B}G
  }
$$

such that $S$ is [[equivalence of groupoids|equivalent]] to a [[set]] $S$, define a $G$-[[action]] on this set as follows.

Consider the [[homotopy fiber product]] 

$$
  S \underset{E}{\times} S
  \stackrel{\overset{}{\longrightarrow}}{\underset{}{\longrightarrow}}
  S
$$ 

of $i$ with itself. By the [[pasting law]] applied to the total homotopy pullback diagram

$$
  \array{
    S \underset{E}{\times} S &\longrightarrow& S  
    \\
    \downarrow && \downarrow^{\mathrlap{i}} 
    \\
    S &\stackrel{i}{\longrightarrow}& E 
    \\
    \downarrow && \downarrow^{\mathrlap{p}} 
    \\
    \ast &\longrightarrow& \mathbf{B}G 
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
    S\times G &\stackrel{p_1}{\longrightarrow}& S  
    \\
    \downarrow && \downarrow 
    \\
    G &\stackrel{}{\longrightarrow}& \ast
    \\
    \downarrow && \downarrow
    \\
    \ast &\longrightarrow& \mathbf{B}G 
  }
$$

there is a canonical [[equivalence of groupoids]]

$$
  S \underset{E}{\times} S \simeq S \times G
$$

such that one of the two canonical maps from the fiber product to $S$ is projection on the first factor. The _other_ map under this equivalence we denote by $\rho$:

$$
  S \times G
  \stackrel{\overset{p_1}{\longrightarrow}}{\underset{\rho}{\longrightarrow}}
  S
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The functor $i \colon S \to E$ is clerly [[essentially surjective functor|essentially surjective]] (every connected component of $E$ has a homotopy fiber under its map to $\mathbf{B}G$). This implies that $E$ is presented by 

$$
  E_\bullet \coloneqq (S \underset{E}{\times}S \stackrel{\overset{p_1}{\longrightarrow}}{\underset{p_2}{\longrightarrow}} S)
$$ 

and hence, via the construction in def. \ref{ActionMapFromFiberSequenceSetToGroupoidToBG}, by

$$
  E_\bullet \simeq (S \times G \stackrel{\overset{p_1}{\longrightarrow}}{\underset{\rho}{\longrightarrow}} S)
  \,.
$$ 

=--

But this already exhibits $E$ as an [[action groupoid]], in particular it mans that $\rho$ is really an [[action]]:


+-- {: .num_prop #ActionGroupoidFromFiberSequence}
###### Proposition

The morphism $\rho$ constructed in def. \ref{ActionMapFromFiberSequenceSetToGroupoidToBG} is a $G$-[[action]] in that it satisfies the action propery, which says that the [[diagram]] (of [[sets]])

$$
  \array{
    S\times G \times G &\stackrel{(id,(-)\cdot(-))}{\longrightarrow}& S \times G
    \\
    \downarrow^{\mathrlap{(\rho,id)}} && \downarrow^{\mathrlap{\rho}}
    \\
    S \times G &\stackrel{\rho}{\longrightarrow}& S
  }
$$

[[commuting diagram|commutes]].

=--

+-- {: .num_prop #EquivalenceOfPermutationRepresentationsWithActionGroupodsInSlice}
###### Proposition

For $G$ a [[discrete group]], there is an [[equivalence of categories]]

$$
  G Act(Set)
  \stackrel{\simeq}{\longrightarrow}
  (Grpd_{/\mathbf{BG}})_{\leq 0}
$$

between the category of [[permutation representations]] of $G$ and the full subcategory of the [[slice (infinity,1)-category|slice (2,1)-category]] of [[Grpd]] over $\mathbf{B}G$ on the [[0-truncated objects]].

This equivalence takes an action to its [[action groupoid]].

=--

+-- {: .proof}
###### Proof

By remark \ref{ActionGroupoidFromFiberSequence} the construction of action groupoids is [[essentially surjective functor|essentially surjective]]. 
By prop. \ref{IntertwinersOfPermutationActionAsSliceHoms} it is [[fully faithful functor|fully faithful]].

=--

####### Examples of actions

One remarkable consequence of prop. \ref{EquivalenceOfPermutationRepresentationsWithActionGroupodsInSlice} is that it says that categories of actions are [[slice (infinity,1)-category|slices]] of [[(2,1)-toposes]], hence are [[slice (infinity,1)-topos|slice (2,1)-toposes]] hence in particular are themselves [[(2,1)-topos]]. In particular there is an [[internal hom]] of actions. This is the [[conjugation action]] construction.

+-- {: .num_defn #ConjugationActionForDiscrete1Groups}
###### Definition

Given a [[discrete group]] $G$ and two $G$-actions $\rho_1$ and $\rho_2$ on [[sets]] $S_1$ and $S_2$, respectively, then the [[function set]] $[S_1, S_2]$ is naturally equipped with the [[conjugation action]]

$$
  Ad \;\colon \;  [S_1, S_2] \times G \longrightarrow [S_1,S_2]
$$

which takes $((S_1 \stackrel{f}{\to} S_2), g)$ to 

$$
  \rho_2(-)(g)\circ f \circ  \rho_1(-)(g^{-1})
  \;\colon\;
  S_1 \stackrel{\rho_1(-)(g^{-1})}{\longrightarrow} S_1 \stackrel{f}{\longrightarrow} S_2\stackrel{\rho_2(-)(g)}{\longrightarrow} S_2
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The [[conjugation action]] construction of def. \ref{ConjugationActionForDiscrete1Groups} is the [[internal hom]] in the [[category]] of actions.

=--

+-- {: .proof}
###### Proof

We need to show that for any three [[permutation representations]],  [[functions]]

$$
  \phi \;\colon\; S_3 \longrightarrow [S_1,S_2]
$$

which [[intertwiner|intertwine]] the $G$-action on $S_3$ with the conjugation action on $[S_1,S_2]$ are in [[natural bijection]] with functions

$$
  \tilde \phi \;\colon\; S_3 \times S_1 \longrightarrow S_2
$$

which intertwine the diagonal action on the [[Cartesian product]] $S_3 \times S_1$ with the action on $S_2$.

The condition on $\phi$ means that for all $g\in G$ and $s_3 \in S_3$ it sends

$$
  \phi
   \;\colon\;
  \rho_3(s_3)(g)
  \mapsto
  \left(
    s_1 \mapsto
    \rho_2\left(
     \phi\left(s_3\right)\left( \rho_1\left(s_1\right)\left(g^{-1}\right) \right)\right)\left(g\right) 
  \right)
 \,.
$$

This is equivalently a function $\tilde \phi$ of two variables which sends

$$
  \tilde \phi
  \;\colon\;
  (\rho_3(s_3)(g), s_1)
  \mapsto
  \rho_2
  (
     \phi(s_3)( 
       \rho_1(s_1)(g^{-1})
     )
  )(g)
 \,.
$$

Since this has to hold for all values of the variables, it has to hold when substituing $s_1$ with $\rho_1(s_1)(g)$. After this substitution the above becomes

$$
  \tilde \phi
  \;\colon\;
  (\rho_3(s_3)(g),
  \rho_1(s_1)(g))
  \mapsto
   \rho_2(\phi(s_3)(s_1 ))(g) 
  \,.
$$

This is the intertwining condition on $\tilde \phi$. Conversely, given $\tilde \phi$ satisfying this for all values of the variables, then running the argument backwards shows that its hom-[[adjunct]] $\phi$ satisfies its required intertwining condition.

=--

The following is immediate but conceptually important:

+-- {: .num_prop }
###### Proposition

The [[invariants]] of the conjugation action on $[S_1,S_2]$ is the set of action [[homomorphisms]]/[[intertwiners]]. 

=--

Hence the inclusion of invariants into the conjugation action gives the inclusion of the external [[hom set]] of the category of $G$-actions into the set underlying the [[internal hom]]

$$ 
  G Act(\rho_1,\rho_2)\hookrightarrow [\rho_1,\rho_2]
  \,.
$$




+-- {: .num_example}
###### Example

Given any $X$ with its canonical action of its [[automorphism group]] $Aut(X)$, regard any $Y$ as equipped with the trivial $Aut(Y)$-action.

Then the [[conjugation action]], def. \ref{ConjugationActionForDiscrete1Groups}, on $[X,Y]$ is the action by precomposition with automorphisms of $X$.

=--
 
###### Associated bundles

At _[[geometry of physics -- principal bundles]]_ in the section _[Smooth principal bundles via smooth groupoids](geometry%20of%20physics%20--%20principal%20bundles#PrincipalBundlesViaSmoothGroupoids)_ is discussed how smooth [[principal bundles]] for a [[Lie group]] $G$ over a [[smooth manifold]] $X$ are equivalently the [[homotopy fibers]] of morphisms of [[smooth groupoids]] ([[smooth stacks]]) of the form

$$
  X \stackrel{}{\longrightarrow} \mathbf{B}G
  \,.
$$

Now given an [[action]] $\rho$ of $G$ on some [[smooth manifold]] $V$, and regardiing this action via its [[action groupoid]] projection $p_\rho \colon V//G \to \mathbf{B}G$ as discussed [above](#ActionsOf1Groups), then we may consider these two morphisms into $\mathbf{B}G$ jointly

$$
  \array{
    && V//G
    \\
    && \downarrow^{\mathrlap{p_\rho}}
    \\
    X &\stackrel{g}{\longrightarrow}& \mathbf{B}G
  }
$$

and so it is natural to construct their [[homotopy fiber product]]. 

We now discuss that this is equivalently the [[associated bundle]] which is associated to the principal bundle $P \to X$ via the action $\rho$.

+-- {: .num_prop #Associated1BundleAsPullbackOfActionGroupoid}
###### Proposition

For $G$ a [[smooth group]] (e.g. a [[Lie group]]), $X$ a [[smooth manifold]], $P \to X$ a smooth $G$-[[principal bundle]] over $X$ and $\rho$ a smooth [[action]] of $G$ on some [[smooth manifold]] $V$, then the [[associated bundle|associated]] $V$-[[fiber bundle]] $P \times_G V\to X$ is equivalently (regarded as a [[smooth groupoid]]) the [[homotopy pullback]] of the [[action groupoid]]-projection $p_\rho \colon V//G \to \mathbf{B}G$ along a morphism $g \colon X\to\mathgbf{B}G$ which [[modulating morphism|modulates]] $P$

$$
  \array{
    P\times_G V &\longrightarrow& V//G
    \\
    \downarrow && \downarrow^{\mathrlap{p_\rho}}
    \\
    X &\stackrel{g}{\longrightarrow}& \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion at _[[geometry of physics -- principal bundles]]_ in the section _[Smooth principal bundles via smooth groupoids](geometry%20of%20physics%20--%20principal%20bundles#PrincipalBundlesViaSmoothGroupoids)_, the morphism $g$ of smooth groupoids is presented by a morphism of pre-smooth groupoids after choosing an [[open cover]] $\{U_i \to X\}$ over wich $P$ trivialize and choosing a trivialization, by the [[zig-zag]]

$$
  \array{
    C(\{U_i\})_\bullet &\stackrel{g_\bullet}{\longrightarrow}& (\mathbf{B}G)_\bullet
    \\
    \downarrow^{\mathrlap{\simeq_{lwe}}}
    \\
    X
  }
$$

where the top morphism is the [[Cech cohomology|Cech cocycle]] of the given local trivialization regarded as a morphism out of the [[Cech groupoid]] of the given cover.

Moreover, by prop. \ref{MapFromActionGroupoidOnSetBackToBG} the morphism $(p_\rho)_\bullet$ is a global fibration of pre-smooth groupoids, hence, by the discussion at _[[geometry of physics -- smooth homotopy types]]_, the homotopy pullback in question is equivalently computed as the ordinary pullback of pre-smooth groupoids of $(p_\rho)_\bullet$ along this $g_\bullet$

$$
  \array{
    C(\{U_i\})_\bullet \underset{(\mathbf{B}G)_\bullet}{\times} (V//G)_\bullet &\longrightarrow& (V//G)_\bullet
    \\
    \downarrow && \downarrow^{\mathrlap{(p_\rho)_\bullet}}
    \\
    C(\{U_i\})_\bullet &\stackrel{g_\bullet}{\longrightarrow}&
    (\mathbf{B}G)_\bullet
    \\
    \downarrow^{\mathrlap{\simeq_{lwe}}}
    \\
    X
  }
  \,.
$$

This pullback is computed componentwise. Hence it is the pre-smooth groupoid whose morphisms are pairs consisting of a morphism $(x,i)\to (x,j)$ in the Cech groupoid as well as a morphism $s \stackrel{g}{\to} \rho(s)(g)$ in the action groupoid, such that the group label $g$ of the latter equals the cocycle $g_{i j}(x)$ of the cocycle on the former. Schematically:

$$
  C(\{U_i\})_\bullet \underset{(\mathbf{B}G)_\bullet}{\times} (V//G)_\bullet
  =
  \left\{
     ((x,i),s) \stackrel{g_{i j}(x)}{\longrightarrow} ((x,j),\rho(s)(g))
  \right\}
  \,.
$$

This means that the pullback groupoid has at most one morphism between every ordered pair of objects. Accordingly this groupoid is [[equivalence of groupoids]] equivalent to the [[quotient]] of its space of objects by the [[equivalence relation]] induced by its morphisms:

$$
  \cdots \simeq
  \left(
    \underset{i}{\coprod} U_i \times V
  \right)/_\sim
  \,.
$$

This is a traditional description of the [[associated bundle]] in question.

=--

###### Invariants and sections

One advantage of the perspective on representations via action groupoids is that it gives a good formulation of the [[invariants]] and the [[coinvariants]] of actions. The invariants are the _[[sections]]_ of the action groupoid projection, while the coivariants in fact are the action groupoid itself.

+-- {: .num_prop}
###### Proposition


For $G$ a [[discrete group]], $\rho$ a $G$-[[action]] on some set $S$, then the set of [[invariants]] of that action is equivalent to the groupoid of [[sections]] of the [[action groupoid]] projection of prop. \ref{MapFromActionGroupoidOnSetBackToBG}, corresponding to the action via prop. \ref{EquivalenceOfPermutationRepresentationsWithActionGroupodsInSlice}.

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
As in the proof of prop. \ref{IntertwinersOfPermutationActionAsSliceHoms}, with the fibrant presentation $(p_\rho)_\bullet$ of prop. \ref{MapFromActionGroupoidOnSetBackToBG}, this is equivalently given by strictly commuting diagrams of the form

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

Given an [[associated bundle]] $P \times_G V\to X$ [[modulating morphism|modulated]], as in prop. \ref{Associated1BundleAsPullbackOfActionGroupoid}, by a morphism of [[smooth groupoids]] of the form $g \colon X \longrightarrow \mathbf{B}G$, then its set of [[sections]] is equivalently the groupoid of diagrams

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

hence the groupoid of sections is equivalently the slice [[hom-groupoid]]

$$
  \Gamma_X(P\times_G V)
  \simeq
  Grpd_{/\mathbf{B}G}(g, p_\rho)
  \,.
$$


=--

+-- {: .proof}
###### Proof

By the defining [[universal property]] of the [[homotopy pullback]] in prop. \ref{Associated1BundleAsPullbackOfActionGroupoid}.

=--

+-- {: .num_remark}
###### Remark

Taken together this means that [[invariants]] of group actions are equivalently the sections of the corresponding [[universal principal bundle|universal]] [[associated bundle]].

=--


#### $\infty$-Representations of 1-groups

The [above](#1RepresentationsOf1Groups) perspective on ordinary representations of ordinary groups on sets via their [[action groupoid]] projection has the advantage that it immediately generalizes to a definition where 1-groups act on more general [[homotopy types]] up to [[coherence|coherent]] [[homotopy]], hence to _[[infinity-representations]]_ or _[[infinity-actions]]_.

+-- {: .num_defn }
###### Definition

Given a [[discrete group]] $G$ and a [[Kan complex]] $V_\bullet$, then an _[[infinity-representation]]_ or _[[infinity-action]]_ of $G$ on $V$ is another [[Kan complex]], to be denoted $(V//G)_\bullet$, equipped with a simplicial map $(p_\rho) \colon (V//G)_\bullet \longrightarrow N(\mathbf{B}G)_\bullet$ to the [[nerve]] of $(\mathbf{B}G_\bullet)$, such that the [[homotopy fiber]] of that map is [[weak homotopy equivalence|weakly homotopy equivalent]] to $V_\bullet$.

=--


###### Examples of $\infty$-Representations

Given an [[abelian group]] $A$ and $n \in \mathbb{N}$, 
write $(\mathbf{B}^n A)_\bullet$ for the [[Kan complex]] which is the image under the [[Dold-Kan correspondence]] of the [[chain complex]] that is concentrated on $A$ in degree $n$.

Then for $G$ a [[discrete group]], the [[mapping complex]] 

$$
  [\mathbf{B}G,\mathbf{B}^n A] \in KanCplx
$$

is the [[infinity-groupoid]] whose [[objects]] are the degree-$n$ [[group cohomology|group cocycles]] on $G$ with [[coefficients]] in $A$ (regarded as a $G$-[[module]] with trivial [[action]]), whose [[morphisms]] are the [[coboundaries]] between these cocycles, and whose higher morphisms are higher order coboundaries-of-coboundaries.

Being a [[mapping space]], this naturally carries a precomposition action by the [[automorphism infinity-group]] of $\mathbf{B}G$, which is also known as the [[automorphism 2-group]] of $G$. Restricting this to _pointed_ automorphisms is is the 1-group $Aut_{Grp}(G)$ of invertible group homomorphisms of $G$.
 



### Semantic Layer


#### $\infty$-Actions

[[∞-action]]

  $$
    \array{
      V &\to& V\sslash G
      \\
      && \downarrow
      \\
      && \mathbf{B}G
    }
  $$

#### Associated $\infty$-bundles

* [[associated infinity-bundle]]

$$
  \array{
    E &\to& V\sslash G
    \\
    \downarrow &pb& \downarrow
    \\
    \tilde X &\to& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

* [[section]]

$$
  \array{
    X &&\stackrel{\sigma}{\to}&& V \sslash G
    \\
    & \searrow &\swArrow_{\simeq}& \swarrow
    \\
    && \mathbf{B}G
  }
$$


### Syntactic Layer


#### The context of a pointed connected type: representation theory

(...)

#### Dependent product over a pointed connected type: invariants

(...)

#### Dependent sum over a pointed connected type: quotients 

(...)