
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

The notion of _$\infty$-action_ is the notion of _[[action]]_ ([[module]]/[[representation]]) in [[homotopy theory]]/[[(∞,1)-category theory]], from [[algebra]] to [[higher algebra]]. 

Notably a [[monoid object in an (∞,1)-category]] $A$ may _act_ on another object $N$ by a [[morphism]] $A \otimes N \to N$ which satisfies an action property up to [[coherence law|coherent]] higher [[homotopy]].

If the $\infty$-action is suitably linear in some sense, this is also referred to as _[[∞-representation]]_.

## Definition

We discuss the actions of [[∞-groups]] in an [[(∞,1)-topos]], following [NSS](#NSS).
(For [[groupoid ∞-actions]] see there.)

Let $\mathbf{H}$ be an [[(∞,1)-topos]].

Let $G \in Grp(\mathbf{H})$ be an [[group object in an (∞,1)-category]] in $\mathbf{H}$, hence a homotopy-[[simplicial object]] on $\mathbf{H}$ of the form

$$
  \left(
  \cdots 
  \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}
  G \times G \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}} G \stackrel{\longrightarrow}{\longrightarrow} *
  \right)
$$

satisfying the groupoidal [[Segal conditions]].

hence an _[[∞-group]]_.


+-- {: .num_defn}
###### Definition

An **action** (or _$\infty$-action_, for emphasis) of $G$ on an object $V \in \mathbf{H}$ is a [[groupoid object in an (∞,1)-category]]  which is equivalent to one of the form

$$
  \left(
  \cdots 
  \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}
  V \times G \times G \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}} V \times G \stackrel{\overset{\rho}{\longrightarrow}}{\underset{p_1}{\longrightarrow}} V  
  \right)
$$

such that the projection maps

$$
  \array{
    \cdots 
    &\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}&
    V \times G \times G 
    &\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}& 
    V \times G 
    &\stackrel{\overset{\rho}{\longrightarrow}}{\underset{p_1}{\longrightarrow}}& 
    V  
    \\
    && \downarrow && \downarrow && \downarrow
    \\
    \cdots 
    &\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}&
    G \times G 
    &\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}& 
    G 
    &\stackrel{\overset{}{\longrightarrow}}{\underset{}{\longrightarrow}}& 
    *  
  }
$$

constitute a morphism of groupoid objects $V\sslash G \to *\sslash G$.

The [[(∞,1)-category]] of such actions is the slice of groupoid objects
over $*\sslash G$ on these objects.

=--

There is an equivalent formulation which does not invoke the notion of [[groupoid object in an (∞,1)-category]] explicitly. This is based on the fundamental fact, discussed at _[[∞-group]]_, that [[delooping]] constitutes an [[equivalence of (∞,1)-categories]]

$$
  \mathbf{B} : Grp(\mathbf{H}) \to \mathbf{H}^{*/}_{\geq 1}
  \,.
$$

form [[group objects in an (∞,1)-category]] to the [[(∞,1)-category]] of [[connected object in an (∞,1)-topos|connected]] [[pointed objects]] in $\mathbf{H}$.

+-- {: .num_prop }
###### Proposition

Every $\infty$-action $\rho : V \times G \to V$ has a classifying morphism $\mathbf{c}_\rho : V \sslash G \to \mathbf{B}G$ in that there is a [[fiber sequence]]


$$
  \array{
    V
    \\
    \downarrow
    \\
    V \sslash G &\stackrel{\overline{\rho}}{\to}& \mathbf{B}G
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

The [[(∞,1)-category]] of $G$-actions in $\mathbf{H}$ is the [[slice (∞,1)-topos]] of $\mathbf{H}$ over $\mathbf{B}G$:

$$
  Act_{\mathbf{H}}(G) \coloneqq \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

A $\rho \in Act_{\mathbf{H}}(G)$ corresponds to a morphism denoted
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

+-- {: .num_remark #DefinitionInTypeTheory}
###### Remark

In the form of def. \ref{GActionByFiberSequence} 
$\infty$-actions have a simple formulation in the [[internal language]] of [[homotopy type theory]]: a $G$-action on $V$ is simply a [[dependent type]] over $\mathbf{B}G$ with fiber $V$:

$$
  * : \mathbf{B}G \vdash V(*) : Type
 \,.
$$

=--

## Notions in higher representation theory
 {#NotionsInHigherRepresentationTheory}


We discuss some basic [[representation theory|representation theoretic]] notions of $\infty$-actions.

In summary, for $\mathbf{c} : \mathbf{B}G \vdash V(\mathbf{c}) : Type$ an action of $G$ on $V$, we have

* the [[dependent sum]]

  $$
    \vdash \sum_{\mathbf{c} : \mathbf{B}G} V(\mathbf{c}) : Type
  $$

  is the [[quotient]] $V\sslash G$ of $V$ by $G$;

* the [[dependent product]]

  $$
    \vdash \prod_{\mathbf{c} : \mathbf{B}G} V(\mathbf{c}) : Type
  $$

  is the collection of [[invariants]] ([[homotopy fixed points]]) of the action.


And for $V_1, V_2$ two actions we have

* the [[dependent product]] over the [[dependent type|dependent]] [[function type]]

  $$
    \vdash \prod_{\mathbf{c} : \mathbf{B}G}
    (V_1(\mathbf{c}) \to V_2(\mathbf{c})) : Type
  $$

  is the collection of $G$-[[homomorphisms]] ($G$-[[equivariance|equivariant]] maps);

* the [[dependent sum]] over the [[dependent type|dependent]] [[function type]]

  $$
    \vdash \sum_{\mathbf{c} : \mathbf{B}G}
    (V_1(\mathbf{c}) \to V_2(\mathbf{c})) : Type
  $$

  is the [[quotient]] of _all_ functions $V_1 \to V_2$ by the [[conjugation action]] of $G$.

### Invariants
 {#Invariants}

+-- {: .num_defn #TypeOfInvariants}
###### Definition

The [[invariants]] ([[homotopy fixed points]]) of a $G$-$\infty$-action $\rho$ are the [[sections]] of the morphism $V \sslash G \to \mathbf{B}G$,

$$
  Invariants(V) = \prod_{\mathbf{B}G \to *} (V \sslash G \to \mathbf{B}G)
  \,,
$$

where $\prod_{\mathbf{B}G \to *} : \mathbf{H}_{/\mathbf{B}G} \to \mathbf{H}$ is the [[direct image]] of the [[base change geometric morphism]].

In [[homotopy type theory]] [[syntax]] for

$$
  \mathbf{c} : \mathbf{B}G \vdash V(\mathbf{c}) : Type
$$

an action as in remark \ref{DefinitionInTypeTheory}, its type of [[invariants]] is the [[dependent product]]

$$
  \vdash \prod_{\mathbf{c} : \mathbf{B}G} V(\mathbf{c}) : Type
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is the [[internal limit]] in $\mathbf{H}$ of the [[internal diagram]]

$$
  \rho \colon \mathbf{B}G \to Type 
  \,.
$$

See at _[internal limit -- Examples -- Homotopy Invariants](internal+%28co-%29limit#BorelConstructionHomotopyQuotients)_.

=--

### Coinvariants / Quotients
 {#Quotients}

From def. \ref{GActionByFiberSequence} we read off:

+-- {: .num_defn }
###### Definition

The [[quotient]] of a $G$-action 

$$
  \mathbf{c} : \mathbf{B}G \vdash V(\mathbf{c}) : Type
$$

is the [[dependent sum]]

$$
  \vdash \sum_{\mathbf{c} : \mathbf{B}G} V(\mathbf{c}) : Type
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is the [[internal colimit]] in $\mathbf{H}$ of the [[internal diagram]]

$$
  \rho \colon \mathbf{B}G \to Type 
  \,.
$$

See at _[internal limit -- Examples -- Homotopy Coinvariants](internal+%28co-%29limit#BorelConstructionHomotopyQuotients)_.

=--


### Conjugation actions
 {#CartesianClosedMonoidalStructure}

+-- {: .num_remark}
###### Remark

By def. \ref{GActionByFiberSequence}, and basic facts disussed at _[[slice (∞,1)-topos]]_, the [[(∞,1)-category]] $Act_{\mathbf{H}}(G)$ is an [[(∞,1)-topos]] and in particular is  a [[cartesian closed (∞,1)-category]].

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
    V_i &\to& V_i \sslash G
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

is the [[inverse image]] of an [[etale geometric morphism]], hence is a [[cartesian closed functor]] (see the _[Examples](cartesian+closed+functor#Examples)_ there for details).
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

### Internal object of homomorphisms

+-- {: .num_remark}
###### Remark

The [[invariant]], def. \ref{TypeOfInvariants}
of the conjugation action, prop. \ref{InternalHomAction} are the action [[homomorphisms]]. (See also at [Examples - Conjugation actions](#ConjugationActions).)

=--

Therefore 

+-- {: .num_defn}
###### Definition

For $\bar \rho_i : V_i \sslash G \to \mathbf{B}G$ two $G$-actions, the **object of homomorphisms** is 

$$
  \prod_{\mathbf{B}G \to *}[\bar \rho_1, \bar \rho_2]
  \in \mathbf{H}
  \,.
$$

In the [[syntax]] of [[homotopy type theory]]

$$
  \vdash \prod_{\mathbf{c} : \mathbf{B}G}
  V_1(\mathbf{c}) \to V_2(\mathbf{c})
  : Type
  \,.
$$

=--

### Stabilizer groups

See at _[[stabilizer group]]_.


### Linearization
 {#Linearization}

We discuss _linearization_ of $\infty$-actions using the axioms of [[differential cohesion]].

Let $0 \colon \ast \to V$ be a [[pointed object]].

Let $G$ be an $\infty$-group acting on $V$

$$
  \array{
    V &\longrightarrow& V/G
    \\
    && \downarrow 
    \\
    && \mathbf{B}G
  }
$$

such that this action preserves the point of $V$, i.e. such that the point is an [[invariant]] of the action. This means equivalently that there is a lift as given by the diagonal morphism in

$$
  \array{
    \ast &\stackrel{0}{\longrightarrow}& V &\longrightarrow & V/G
    \\
    & \searrow& & \nearrow& \downarrow 
    \\
    && \ast &\longrightarrow& \mathbf{B}G
  }
$$

which in turn means that the action factors through an action of the [[stabilizer group]] $Stab_G(0)$

$$
  \array{
     \ast &\longrightarrow&  \mathbf{B}Stab_G(0)
     \\
     \downarrow &\nearrow& \downarrow & \searrow
     \\
     \mathbf{B}G &\longrightarrow& V/G &\longrightarrow& \mathbf{B}G
  }
$$

(using that the left morphism is a [[1-epimorphism]] and the right morphism a [[1-monomorphism]]).

It follows by the [[pasting law]] the top squares in the following diagram is a [[homotopy pullback]]

$$
  \array{
     \ast &\longrightarrow& \ast/G
     \\
     {}^{\mathllap{0}}\downarrow && \downarrow 
     \\
     V &\longrightarrow& V/G
     \\
     \downarrow && \downarrow
     \\
     \ast &\longrightarrow& \mathbf{B}G
  }
$$

exhibiting that the $G$-action on $V$ restricts to the trivial action on the point $0$ of $V$.

Now let $\int_{inf}$ denote the [[infinitesimal shape modality]]. Since it preserves the top homotopy pullback, it follows that applying the [[orthogonal factorization system]] ($\int_{inf}$-equivalences, [[formally etale morphisms]]) to the top vertical morphisms produces a pasting diagram of homotopy pullbacks of the form

$$
  \array{
     \ast &\longrightarrow& \ast/G
     \\
     \downarrow && \downarrow
     \\
     \mathbb{D}^V_0 &\longrightarrow& \mathbb{D}^V_0/G
     \\
     \downarrow && \downarrow
     \\
     \downarrow && \downarrow 
     \\
     V &\longrightarrow& V/G
     \\
     \downarrow && \downarrow
     \\
     \ast &\longrightarrow& \mathbf{B}G
  }
$$

where $\mathbb{D}^V_0$ is the [[infinitesimal disk]] around $0$ in $V$.

Here the cartesian subdiagram 

$$
  \array{
     \mathbb{D}^V_0 &\longrightarrow& \mathbb{D}^V_0/G
     \\
     \downarrow && \downarrow
     \\
     \ast &\longrightarrow& \mathbf{B}G
  }
$$

hence exhibits a $G$-action on $\mathbb{D}^V_0$.

Any $G$-action on an infinitesimal disk is a linear action, given by a homomorphism $G \to GL(V) \coloneqq \mathbf{Aut}(\mathbb{D}^V_0)$ to the [[automorphism infinity-group]] of the [[infinitesimal disk]], the [[general linear group]] of the [[tangent space]] of $V$ at 0.



## Examples

### Discrete group actions on sets 
 {#ExamplesPermutationRepresentations}

As the simplest special case, we discuss how the traditional concept of [[discrete groups]] acting on a [[sets]] ("[[permutation representations]]") is recoverd from the above general abstract concepts.

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

+-- {: .num_prop}
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
 



### $\infty$-group actions in an $\infty$-topos

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and let $G \in Grp(\mathbf{H})$ be an [[∞-group]] in $\mathbf{H}$. 

The following lists some fundamental classes of examples of $\infty$-actions of $G$, and of other canonical $\infty$-groups. By the discussion [above](#PropertiesOfGroupActionsInTopos) these actions may be given by the classifying morphisms.

#### Trivial action
 {#TrivialAction}

Consider the [[étale geometric morphism]]

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
  G \sslash G \simeq *
  \,.
$$

#### Adjoint action
 {#ExamplesAdjointAction}

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
  G \sslash_{Ad}G \simeq \mathcal{L}\mathbf{B}G
  \,.
$$

For more on this see at *[[free loop space of a classifying space]]*.


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
    V \sslash \mathbf{Aut}(V) &\to& \mathbf{B} \mathbf{Aut}(V)
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
  Act_{\mathbf{H}}(G)(V \times \Sigma, X)
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

#### Semidirect product groups
 {#SemidirectProductGroups}

Let $G, A \in Grp(\mathbf{H})$ be 0-truncated group objects and let $\rho$ be an action of $G$ on $A$ by group homomorphisms. This is equivalently an action of $G$ on $\mathbf{B}A$, hence a fiber sequence

$$
  \array{
    \mathbf{B}A &\to& \mathbf{B} (G \ltimes A)
    \\
    && \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

The corresponding [[action groupoid]] $(\mathbf{B}A)\sslash G \simeq \mathbf{B}( G \ltimes A)$ is the delooping of the corresponding [[semidirect product group]]. 


#### $G$-Modules
 {#GModules}

+-- {: .num_defn #InfinityModuleOverAnInfinityGroup}
###### Definition

For $G \in Grp(\mathbf{H})$ the $\infty$-category of **$G$-[[modules]]** is 

$$
  Stab( \mathbf{H}_{/\mathbf{B}G}) \simeq Stab(G Act)
  \,,
$$

the [[stabilization]] of the $\infty$-category of $G$-actions.

=--

+-- {: .num_example}
###### Example

For $G$ and $A$ 0-truncated groups, $A$ an [[abelian group]] with $G$-[[module]] structure, the semidirect product group $G \ltimes A$ from [above](#SemidirectProductGroups) exhibits $A$ as a $G$-module in the sense of def. \ref{InfinityModuleOverAnInfinityGroup}.

=--


#### Actions in a slice
 {#ExamplesActionsInASlice}

Consider an object $B \in \mathbf{H}$ and an object 

$$
  L \in \mathbf{H}_{/B}
$$

in the slice. By the discussion of [[conjugation actions]] [above](CartesianClosedMonoidalStructure), the [[automorphism ∞-group]] of $L$ as an object in $\mathbf{H}$ is the [[dependent product]] over the [[automorphism ∞-group]] $\mathbf{Aut}_{\mathbf{H}}(L)\in \mathbf{H}_{/B}$ in the slice.

$$
  \mathbf{Aut}_{\mathbf{H}}(L) 
    \coloneqq 
  \underset{B}{\prod} \mathbf{Aut}(L)
  \in 
  \mathrm{Grp}(\mathbf{H})
  \,.
$$

By [[adjunction]] there is a canonical morphism from the re-pullback of this to the slice automorphism group

$$
  \epsilon
  \colon
  B^\ast \mathbf{B}\mathbf{Aut}_{\mathbf{H}}(L)
  \longrightarrow
  \mathbf{B} \mathbf{Aut}(L)
  \,.
$$

Hence the canonical $\mathbf{Aut}(L)$-action on $L$ in the slice pulls back to give an action of $B^\ast \mathbf{Aut}_{\mathbf{H}}(L)$ on $L$:

$$
  \array{
     L
     &\longrightarrow&
     L//(B^\ast\mathbf{Aut}_{\mathbf{H}}(L))
     &\longrightarrow&
     L//\mathbf{Aut}(L)
     \\
     \downarrow && \downarrow && \downarrow
     \\
     \ast
     &\longrightarrow&
     \mathbf{B}B^\ast \mathbf{Aut}_{\mathbf{H}}(L)
     &\stackrel{\epsilon}{\longrightarrow}&
     \mathbf{B} \mathbf{Aut}(L)     
  }
$$



+-- {: .num_prop #AutomorphismActionInSliceInducingActionOnSum}
###### Proposition

Underlying the $B^\ast\mathbf{Aut}_{\mathbf{H}}(L)$-action on  $L$ is an $\mathbf{Aut}_{\mathbf{H}}(L)$-action on 

$$
  X  \coloneqq \underset{B}{\sum} L
$$

and 

$$
  \underset{B}{\sum} \left(L//B^\ast\mathbf{Aut}_{\mathbf{H}}(L)\right)
  \;\simeq\;
   X//\mathbf{Aut}_{\mathbf{H}}(L)
$$

=--

+-- {: .proof}
###### Proof

Applying $\underset{B}{\sum}$ to the Cartesian diagram that defines the $\infty$-action on $L$


$$
  \array{
     L
     &\longrightarrow&
     L//\mathbf{Aut}_{\mathbf{H}}(L) 
     \\
     \downarrow && \downarrow 
     \\
     \ast
     &\longrightarrow&
     \mathbf{B}B^\ast \mathbf{Aut}_{\mathbf{H}}(L)
  }
$$

yields

$$
  \array{
     X
     &\longrightarrow&
     \underset{X}{\sum} \left( L//\mathbf{Aut}_{\mathbf{H}}(L)  \right)
     \\
     \downarrow && \downarrow 
     \\
     B
     &\longrightarrow&
     \underset{B}{\sum} B^\ast \mathbf{B} \mathbf{Aut}_{\mathbf{H}}(L)
  }
$$

which is still Cartesian, by [this proposition](dependent+sum#AbsoluteDependentSumPreservesFiberProducts). Use that the bottom left object here is equivalently $B \simeq \underset{B}{\sum} B^\ast (\ast)$ and form the
[[pasting diagram|pasting]] with the [[naturality square]] of the $(\underset{B}{\sum}\dashv B^\ast)$-[[counit of an adjunction|counit]].

$$
  \array{ 
     X &\longrightarrow& \underset{B}{\sum} \left(L//\mathbf{Aut}_{\mathbf{H}}(L)\right)
     \\
     \downarrow && \downarrow
     \\
     \underset{B}{\sum}B^\ast \ast 
       &\longrightarrow& 
     \underset{B}{\sum}B^\ast \mathbf{B}\mathbf{Aut}_{\mathbf{H}}(L)     
     \\
     \downarrow && \downarrow
     \\
     \ast &\longrightarrow& \mathbf{B}\mathbf{Aut}_{\mathbf{H}}(L)
  }
  \,.
$$

By [this proposition](dependent+sum#NaturalitySquareOfCounitIsPullback) also this naturality square is Cartesian. Hence by the [[pasting law]] the total rectangle is Cartesian. This exhibits the $\mathbf{Aut}_{\mathbf{H}}(L)$-action on $X = \underset{B}{\sum} L$.


=--

+-- {: .num_remark}
###### Remark

Stated more intuitively, prop. \ref{AutomorphismActionInSliceInducingActionOnSum} says that sliced automorphisms of the form

$$
  \mathbf{Aut}_{\mathbf{H}}(L)
  =
  \left\{
    \array{
      X & & \stackrel{\simeq}{\longrightarrow} & & X
      \\
      & {}_{\mathllap{L}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{L}}
      \\
      && B 
    }
  \right\}
$$

act on $X$ by the evident restriction to the horizontal equivalences, 

$$
  \left\{
    \array{
      X & & \stackrel{\simeq}{\longrightarrow} & & X
    }
  \right\}
$$

and that forming the homotopy quotient of this action on $L$ makes $L$ [[descent]] to the homotopy quotient of $X$ by this action to yield

$$
  \array{
     X // \mathbf{Aut}_{\mathbf{H}}(L)
     \\
     \downarrow^{\mathrlap{L//\mathbf{Aut}_{\mathbf{H}}(L)}}
     \\
     B
  }
  \,.
$$

(For instance if here $B$ is a [[moduli stack]] for some [[prequantum n-bundles]], then this says that the [[quantomorphism n-group]] acting on this gives higher and pre-quantized "[[symplectic reduction]]" of these bundles to the quotient space.)

=--


#### Co-Discretization of Actions

Let $\mathbf{H}$ be a [[local (∞,1)-topos]] (for instance a [[cohesive (∞,1)-topos]]) and write $\sharp$ for its [[sharp modality]].
Write $\sharp_n$ for the [[n-image]] of itd [[unit of a monad|unit]].

+-- {: .num_prop #CoDiscretizationOfActions}
###### Proposition

Given an [[∞-group]] $G$ in $\mathbf{H}$ and a $G$-action, def. \ref{GActionByFiberSequence}, on some $X$, then $\sharp_n G$ is itself canonically an $\infty$-group equipped with a canonically induced action on $\sharp_n X$ such that the projection $X \to \sharp_n X$ carries the structure of a homomorphism of $G$-actions.

=--

We indicate two proofs, the first non-elementary (making use of the [[Giraud-Rezk-Lurie theorem]]), the second [[elementary (infinity,1)-topos|elementary]]. (Following [this](http://nforum.ncatlab.org/discussion/4576/nimage/?Focus=51743#Comment_51743) discussion.)

+-- {: .proof}
###### Proof

Observe that $\sharp_n$ preserves [[products]], since $\sharp$ does (being a [[right adjoint]]) and by [this proposition](n-image#nImagePreservesProducts). Now use that the [[homotopy quotient]] $V/G$ is the realization of the [[simplicial object in an (infinity,1)-category|simplicial object]] $(V/G)_\bullet = G^{\times_{\bullet}} \times V$. So applying $\sharp_n$ to this yields a simplicial object $((\sharp_n V)/(\sharp_n G))_\bullet = (\sharp_n G)^{\times_{\bullet}} \times (\sharp_n V)$ which exhibits the desired action.

=--

+-- {: .proof}
###### Proof

Generally, let $A:B\to Type$ be any [[dependent type]] family (speaking [[homotopy type theory]]).  We claim that there is an induced family $A^{\sharp_n} : \sharp_{n+1} B \to Type $ such that $A^{\sharp_n}(\eta_{n+1}(b)) = \sharp_n (A(b))$ for any $b:B$, where $\eta_{n+1} : B \to \sharp_{n+1} B$ is the inclusion.  Applying this when $A \to B$ is $V/G \to \mathbf{B}G$ and when $b$ is (necessarily) [[generalized the|the]] basepoint of $\mathbf{B}G$ gives the desired action on the desired type.

First of all, we have the composite $B \xrightarrow{A} Type \xrightarrow{\sharp} Type_{\sharp}$, where $Type_{\sharp} = \sum_{X:Type} is\sharp(X)$.  Since $Type_{\sharp}$ is itself $\sharp$ (since $\sharp$ is lex), this factors through $\sharp B$, giving a type family $A^\sharp : \sharp B \to Type_{\sharp}$ such that $A^{\sharp}(\eta(b)) = \sharp (A(b))$ for any $b:B$, where $\eta:B\to \sharp B$ is the unit of $\sharp$.

Now fix $y:\sharp B$ and $x:A^\sharp(y)$.  For any $b:B$ and $p:\eta(b)=y$, we can define the type ${\big\Vert \sum_{(a:A(b))} p_\ast (\eta(a)) = x\big\Vert}_n$.  This is an $n$-type, and since the [[type of types|type of]] [[truncated types]] $n\text{-}Type$ is an $(n+1)$-type, as a function of $(b,p) : \sum_{b:B} \eta(b)=y$, this construction factors through $\big\Vert \sum_{b:B} \eta(b)=y\big\Vert_{n+1}$.  Thus, for $y:\sharp B$ and $x:A^\sharp(y)$ and $\xi : {\big\Vert \sum_{(b:B)} \eta(b)=y\big\Vert}_{n+1}$ we have a type $P(y,x,\xi)$, such that
$$P\big(y,x,{|(b,p)|}_{n+1}\big) = {\left\Vert \sum_{(a:A(b))} p_\ast (\eta(a)) = x\right\Vert}_n.$$

Now by definition, $\sharp_{n+1} B \coloneqq \sum_{(y:\sharp B)} {\big\Vert \sum_{(b:B)} \eta(b)=y\big\Vert}_{n+1}$.  Thus, we can define $A^{\sharp_n} : \sharp_{n+1} B \to Type$ by $A^{\sharp_n}(y,\xi) = \sum_{x:A^\sharp(y)} P(y,x,\xi)$.  And since $\eta_{n+1}(b) = (\eta(b),{|(b,1)|}_{n+1})$, we have $A^{\sharp_n}(\eta_{n+1}(b)) = \sum_{x:\sharp(A(b))} {\big\Vert \sum_{(a:A(b))} \eta(a)) = x\big\Vert}_n$, which is $\sharp_{n}(A(b))$ by definition.


=--


### Infinitesimally: actions of $L_\infty$-algebroids

See _[[Lie infinity-algebroid representation]]_.

## Properties

### Model category presentation

In the context of [[geometrically discrete ∞-groupoids]]
a [[model category]] structure presenting the [[(∞,1)-category]]
of $\infty$-actions is the _[[Borel model structure]]_ ([DDK 80](#DDK80)).

## Related concepts

* [[action]], **$\infty$-action**

  * [[faithful ∞-action]]

  * [[stabilizer ∞-group]]

* [[module]], [[∞-module]]

* [[representation]], [[∞-representation]]

* [[associated bundle]], [[associated ∞-bundle]]

* [[induced representation]]

* [[equivariant homotopy theory]]

* [[equivariant cohomology]]

  * [[group cohomology]]

[[!include homotopy type representation theory -- table]]


## References

### General

Actions of [[A-∞ algebras]] in some [[symmetric monoidal (∞,1)-category]] are discussed in section 4.2 of

* [[Jacob Lurie]], _[[Higher Algebra]]_

Aspects of actions of [[∞-groups]] in an [[∞-topos]] in the contect of [[associated ∞-bundles]] are discussed in section I 4.1 of 

* {#NSS} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_, Journal of Homotopy and Related Structures, June 2014 ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248))
 
Discussion in [[homotopy type theory]] is in

* {#BuchholtzDoornRijke18} [[Ulrik Buchholtz]], [[Floris van Doorn]], [[Egbert Rijke]], _Higher Groups in Homotopy Type Theory_, LICS '18: Proceedings of the 33rd Annual ACM/IEEE Symposium on Logic in Computer Science  ([arXiv:1802.04315](https://arxiv.org/abs/1802.04315), [doi:10.1145/3209108.3209150](https://doi.org/10.1145/3209108.3209150))

### For discrete geometry
 {#ReferencesForDiscreteGeometry}

For $\mathbf{H}= \infty Grpd$ the statement that homotopy types over $B G$ are equivalently $G$-[[infinity-actions]] is (via the [[Borel model structure]]) is due to 

*  {#DDK80} E. Dror, [[William Dwyer]], [[Daniel Kan]], _Equivariant maps which are self homotopy equivalences_, Proc. Amer. Math. Soc. 80 (1980), no. 4, 670&#8211;672 ([jstor:2043448](http://www.jstor.org/stable/2043448))

This is mentioned for instance as exercise 4.2 in 

* {#Dwyer2008} [[William Dwyer]], _Homotopy theory of classifying spaces_, Lecture notes Copenhagen (June, 2008) [pdf](http://www.math.ku.dk/~jg/homotopical2008/Dwyer.CopenhagenNotes.pdf)

An alternative proof in terms of [[relative categories]] is in 

* {#Sharma15} Amit Sharma, _On the homotopy theory of $G$-spaces_, International Journal of Mathematics and Statistics Invention, Volume7 Issue 2, 2019 ([arXiv:1512.03698](http://arxiv.org/abs/1512.03698), [published pdf](https://www.ijmsi.org/Papers/Volume.7.Issue.2/H07025255.pdf))

Closely related discussion of homotopy fiber sequences and homotopy action but in terms of [[Segal spaces]] is in section 5 of

* [[Matan Prezma]], _Homotopy normal maps_, Algebr. Geom. Topol. Volume 12, Number 2 (2012), 1211-1238. ([arXiv:1011.4708](https://arxiv.org/abs/1011.4708v9), [euclid:agt/1513715387](https://projecteuclid.org/euclid.agt/1513715387)) 

There, conditions are given for a morphism $A_\bullet \to B_\bullet$ to a [[reduced Segal space]] to have a fixed homotopy fiber, and hence encode an action of the loop group of $B$ on that fiber. 


### For actions of topological groups
 {#ForActionsOfTopologicalGroups}

That $G$-actions for $G$ a [[topological group]] in the sense of [[G-spaces]] in [[equivariant homotopy theory]] (and hence with $G$ _not_ regarded as the geometrically discrete [[∞-group]] of its underying [[homotopy type]] ) are equivalently objects in the [[slice (∞,1)-topos]] over $\mathbf{B}G$ is [[Elmendorf's theorem]] together with the fact, highlighted in this context in 

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_, 2014

that 

$$
  G Space \simeq PSh_\infty(Orb_G) \simeq PSh_\infty(Orb_{/\mathbf{B}G})
  \simeq
  PSh_\infty(Orb)_{/\mathbf{B}G}
$$

is therefore the slice of the $\infty$-topos over the [[global orbit category]] by $\mathbf{B}G$.

[[!include equivariant homotopy theory -- table]]

See at _[[equivariant homotopy theory]]_ for more references along these lines.

[[!redirects ∞-action]]

[[!redirects infinity-actions]]
[[!redirects ∞-actions]]