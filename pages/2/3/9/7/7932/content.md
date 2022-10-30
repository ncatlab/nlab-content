
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The generalization of the notion of _[[action]]_ from [[algebra]] to [[higher algebra]]. 

If the action is suitably linear in some sense, this is also referred to as _[[∞-representation]]_.

## Properties

### For $\infty$-groups in an $\infty$-topos 
 {#PropertiesOfGroupActionsInTopos}

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and let $G \in Grp(\mathbf{H})$ be an [[∞-group]] in $\mathbf{H}$.

+-- {: .num_prop}
###### Proposition

Every $\infty$-action $\rho : V \times G \to V$ has a classifying morphism $\mathbf{c}_\rho : V//G \to \mathbf{B}G$ in that there is a [[fiber sequence]]

$$
  \array{
    V
    \\
    \downarrow
    \\
    V//G &\stackrel{\overline{\rho}}{\to}& \mathbf{B}G
  }
$$

such that $\rho$ is the $G$-action on $V$ regarded as the corresponding $G$-[[principal ∞-bundle]] modulated by $\overline{\rho}$.

=--

This allows to characterize $\infty$-actions in the following convenient way.
See ([NSS](#NSS)) for a detailed discussion.


+-- {: .num_defn #GActionByFiberSequence}
###### Definition

For $V \in \mathbf{H}$ an object, a $G$-$\infty$-action $\rho$ on $V$ is a 
[[fiber sequence]] in $\mathbf{H}$ of the form

$$
  \array{
    V &\to& V \sslash G
    \\
    && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

The [[(∞,1)-category]] of $G$-actions in $\mathbf{H}$ is

$$
  Act_{\mathbf{H}}(G) \coloneqq \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

An $\rho \in Act_{\mathbf{H}}(G)$ corresponds to a morphism denoted
$\overline{\rho} : V\sslash G \to \mathbf{B}G$ in $\mathbf{H}$ hence to an object $\overline{\rho} \in \mathbf{H}_{/\mathbf{B}G}$.

A morphism $\phi : \rho_1 \to \rho_2  $ in $Act_{\mathbf{H}}(G)$
corresponds to a diagram

$$
  \array{
     V_1 \sslash G &&\stackrel{}{\to}&& V_2 \sslash G
     \\
     & {}_{\mathllap{\overline{\rho_1}}}\searrow && \swarrow_{\mathrlap{\overline{\rho_2}}}
     \\
     && \mathbf{B}G
  }
$$

in $\mathbf{H}$.

=--

+-- {: .num_remark}
###### Remark

The bundle $\overline{\rho}$ in def. \ref{GActionByFiberSequence} is the
universal $\rho$-[[associated infinity-bundle|associated]] $V$-[[fiber ∞-bundle]].

=--

### Invariants
 {#Invariants}

The [[invariants]] of a $G$-$\infty$-action are the [[sections]] of the morphism $V \sslash G \to \mathbf{B}G$:

$$
  Invariants(V) = \prod_{\mathbf{B}G} (V \sslash G \to \mathbf{B}G)
  \,.
$$

In [[homotopy type theory]] [[syntax]]: for

$$
  \mathbf{c} : \mathbf{B}G \vdash V(\mathbf{c}) : Type
$$

an action, its type of invariants is

$$
  \vdash \prod_{\mathbf{c} : \mathbf{B}G} V(\mathbf{c})
  \,.
$$

### Cartesian closed monoidal structure on $\infty$-actions
 {#CartesianClosedMonoidalStructure}

+-- {: .num_remark}
###### Remark

By def. \ref{GActionByFiberSequence}, and basic facts disussed at _[[slice (∞,1)-topos]]_,
the [[(∞,1)-category]] $Act_{\mathbf{H}}(G)$
is an [[(∞,1)-topos]] and in particular is 
a [[cartesian closed (∞,1)-category]].

=--

We describe here aspects of the [[cartesian product]] and [[internal hom]] of $\infty$-actions given this way. The following statements are essentially immediate consequences of basic [[homotopy type theory]].


+-- {: .num_prop}
###### Proposition

For $(V_1, \rho_1), (V_2, \rho_2) \in Act(G)$ their [[cartesian product]]
is a $G$-action on the product of $V_1$ with $V_2$ in $\mathbf{H}$.

=--

+-- {: .proof}
###### Proof

Let 

$$
  \array{
    V_i &\to& V\sslash G
    \\
    && \downarrow^{\bar \rho_i}
    \\
    && \mathbf{B}G
  }
$$

be the [[principal ∞-bundles]] exhibiting the two actions.

Along the lines of the discussion at [[locally cartesian closed category]] we find that $(V_1, \rho_1) \times (V_2, \rho_2) \in Act(G)$ is given in $\mathbf{H}$ by the [[(∞,1)-pullback]] 

$$
  \sum_{\mathbf{B}G}
    \bar \rho_1 \times 
    \bar \rho_2
  \simeq
   V_1\sslash G \times_{\mathbf{B}G} V_2 \sslash G
$$

in $\mathbf{H}$,
with the product action being exhibited by the [[principal ∞-bundle]]

$$
  \array{
    V_1 \times V_2 &\to& V_1\sslash G \times_{\mathbf{B}G} V_2 \sslash G
    \\
    && \downarrow^{\mathrlap{\overline{ \rho_1 \times \rho_2 }}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

Here the [[homotopy fiber]] on the left is identified as $V_1 \times V_2$ by using that [[(∞,1)-limits]] commute over each other.

=--

+-- {: .num_prop #InternalHomAction}
###### Proposition

For $\rho_1, \rho_2 \in Act(G)$ their [[internal hom]] $[\rho_1, \rho_2] \in Act_{\mathbf{H}}(G)$ is a $G$-action on the [[internal hom]] $[V_1, V_2] \in \mathbf{H}$. 

=--

+-- {: .proof }
###### Proof

Taking fibers 

$$
  pt_{\mathbf{B}G}^* : \mathbf{H}_{/\mathbf{B}G} \to \mathbf{H}
$$

is the [[inverse image]] of a [[etale geometric morphism]], hence is a [[cartesian closed functor]] (see the _[Examples](cartesian+closed+functor#Examples)_ there for details).
Therefore it preserves [[exponential objects]]:

$$
  \begin{aligned}
    pt_{\mathbf{B}G}^* [\bar \rho_1, \bar \rho_2]
    &
    \simeq
    [pt_{\mathbf{B}G}^* \bar \rho_1, pt_{\mathbf{B}G}^* \bar \rho_2]
    \\
    & \simeq [V_1, V_2]
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The above internal-hom action 

$$
  \array{
    [V_1,V_2] &\to& V_1 \sslash G \times_{\mathbf{B}G} V_2 \sslash G
    \\
    && \downarrow^{\mathrlap{\overline{[\rho_1,\rho_2]}}}
    \\
    && \mathbf{B}G
  }
$$

encodes the [[conjugation action]] of $G$ on $[V_1, V_2]$ by pre- and post-composition of [[functions]] $V_1 \to V_2$ with the $G$-action on $V_1$ and on $V_2$, respectively.

See also at _[Conjugation actions](#ConjugationActions)_ below.

=--



## Examples

### Of $\infty$-group actions in an $\infty$-topos

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and let $G \in Grp(\mathbf{H})$ be an [[∞-group]] in $\mathbf{H}$. 

The following lists some fundamental classes of examples of $\infty$-actions of $G$, and of other canonical $\infty$-groups. By the discussion [above](#PropertiesOfGroupActionsInTopos) these actions may be given by the classifying morphisms.

#### Trivial action
 {#TrivialAction}

Consider the [[etale geometric morphism]]

$$
  Act_{\mathbf{H}}(G) \coloneqq
  \mathbf{H}_{/\mathbf{B}G}
  \stackrel{\overset{p^* \coloneqq (-) \times \mathbf{B}G}{\leftarrow}}{\underset{}{\to}}
  \mathbf{H}
  \,.
$$

+-- {: .num_defn #TrivialAction}
###### Definition

For $V \in \mathbf{H}$ any object, the **trivial action** of $G$ on
$V$ is $p^* V \in Act_{\mathbf{H}}(G)$, exhibited by the split fiber sequence

$$
  \array{
    V &\to& V \times \mathbf{B}G
    \\
    && \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

=--

#### Fundamental action

The _right $\infty$-action_ of $G$ on itself is given by the fiber sequence

$$
  \array{
    G 
    \\
    \downarrow
    \\
    * &\to& \mathbf{B}G
  }
$$

which exhibits $\mathbf{B}G$ as the [[delooping]] of $G$.

$$
  G//G \simeq *
  \,.
$$

#### Adjoint action

The fiber sequence

$$
  \array{
    G
    \\
    \downarrow
    \\
    \mathcal{L} \mathbf{B}G &\stackrel{ev_*}{\to}& \mathbf{B}G
  }
$$

given by the [[free loop space object]] $\mathcal{L}\mathbf{B}G$ exhibits the higher [[adjoint action]] of $G$ on itself:

$$
  G//_{Ad}G \simeq \mathcal{L}\mathbf{B}G
  \,.
$$

#### Automorphism action
 {#AutomorphismAction}

+-- {: .num_defn #AutomorphAction}
###### Definition


For $V \in \mathbf{H}$ any object, there is a canonical action of the 
internal [[automorphism infinity-group]] $\mathbf{Aut}(V)$:

$$
  \array{
    V
    \\
    \downarrow
    \\
    V//\mathbf{Aut}(V) &\to& \mathbf{B} \mathbf{Aut}(V)
  }
$$

=--

#### Conjugation actions
 {#ConjugationActions}

We discuss the simple case of the [[cartesian closed category]] of $G$-sets (G-[[permutation representations]]) for $G$ an ordinary [[discrete group]]
as a simple illustration of the internal hom of $\infty$-actions, prop. \ref{InternalHomAction}.

This example spells out everything completely in components:

+-- {: .num_example}
###### Example

Let $\mathbf{H} = $ [[∞Grpd]], let $G \in Grp(\infty Grpd)$ be an ordinary [[discrete group]] and let $V, \Sigma, X$ be [[sets]] equipped with $G$-[[action]] ([[permutation representations]]).

In this case $[\Sigma,X]$ is simply the set of [[functions]] $f : \Sigma \to X$ of sets. Its $G$-action as the internal hom of $G$-actions given, for every $g \in G$  and $\sigma \in \Sigma$, by

$$
  g(f)(\sigma) = g(f(g^{-1}(\sigma)))
  \,,
$$

(where we write generically $g(-)$ for the given action on the set specified implicitly by the type of the argument).

Hence a morphism of $G$-actions

$$
  \phi : V \to [\Sigma,X]
$$

is a function $\phi$ of the underlying sets such that for all $V \in V$, $g \in G$ and all $\sigma \in \Sigma$ we have

\[
  \label{Equation1}
  \phi(g(v))(\sigma) = g(\phi(v)(g^{-1}(\sigma))
  \,.
\]

On the other hand, a morphism of actions

$$
  \psi : V \times \Sigma \to X
$$

is a function of the underlying sets, such that for all these terms we have

$$
  \psi(g(v), g(\sigma)) = g(\psi(v,\sigma))
$$

which is equivalent to

\[
  \label{Equation2}
  \psi(g(v), \sigma) = g(\psi(v,g^{-1}(\sigma)))
  \,.
\]

Comparison of (eq:Equation1) and (eq:Equation2) shows that the identification

$$
  \psi(v,\sigma) \coloneqq \phi(v)(\sigma)
$$

establishes a [[natural equivalence]] (a [[natural bijection]] of sets in this case)

$$
  Act_{\mathbf{H}}(G)(V, [\Sigma,X])
  \simeq
  Act_{\mathbf{H}}(G)(V \times \Sigma, X])
  \,,
$$

showing how $[\Sigma,X]$ is indeed the [[internal hom]] of $G$-actions.

=--

+-- {: .num_remark}
###### Remark

Generally, for $G$ a [[discrete ∞-group]] we have an [[equivalence of (∞,1)-categories]]

$$
  \infty Grpd_{/\mathbf{B}G}
  \simeq
  \infty Func(\mathbf{B}G, \infty Grpd)
$$

(by the [[(∞,1)-Grothendieck construction]]), and hence

$$
  Act_{\infty Grpd}(G) 
   \simeq 
  \infty Func(\mathbf{B}G, \infty Grpd)
$$

is the [[(∞,1)-category]] of [[∞-permutation representations]].

=--



#### General covariance
 {#GeneralCovariance}

Let $X \in \mathbf{H}$ be a [[moduli infinity-stack]] for 
field in a [[gauge theory]] or [[sigma-model]]. Let $\Sigma \in \mathbf{H}$ be the corresponding [[spacetime]] or [[worldvolume]], respectively. 

We have the automorphism action, def. \ref{AutomorphAction}

$$
  \array{
     \Sigma &\to& \Sigma \sslash \mathbf{Aut}(\Sigma)
      \\
      && \downarrow
      \\
      && \mathbf{B} \mathbf{Aut}(\Sigma)
  }
  \,.
$$

The slice $\mathbf{H}_{/\mathbf{Aut}(\Sigma)} = Act_{\mathbf{H}}(\mathbf{Aut}(\Sigma))$ is the context of types which are _[[general covariance|generally covariant]]_ over $\Sigma$.

On $X$ consider the trivial $\mathbf{Aut}(\Sigma)$-action, def. \ref{TrivialAction}. Then the internal-hom action of prop. \ref{InternalHomAction}

$$
  [\Sigma, X]\sslash \mathbf{Aut}(\Sigma)
  \simeq
  [\Sigma \sslash \mathbf{Aut}(\Sigma), X \times \mathbf{B}\mathbf{Aut}(\Sigma)]_{\mathbf{B}\mathbf{Aut}(\Sigma)}
$$

is the configuration space of fields on $\Sigma$ modulo automorphisms (diffeomorphisms, in [[smooth infinity-groupoid|smooth cohesion]]) of $\Sigma$. This is the configuration space of "[[general covariance|generally covariant]]" field theory on $\Sigma$.

## Related concepts

* [[action]], **$\infty$-action**

* [[representation]], [[∞-representation]]

* [[associated bundle]], [[associated ∞-bundle]]


## References

Actions of [[A-∞ algebras]] in some [[symmetric monoidal (∞,1)-category]] are discussed in section 4.2 of

* [[Jacob Lurie]], _[[Higher Algebra]]_

Aspects of actions of [[∞-groups]] in an [[∞-topos]] in the contect of [[associated ∞-bundles]] are discussed in section I 4.1 of 

* _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_
 {#NSS}

[[!redirects ∞-action]]

[[!redirects infinity-actions]]
[[!redirects ∞-actions]]

