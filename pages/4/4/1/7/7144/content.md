
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Definition

### Tradtional
 {#TraditionalDefinition}

Given an [[action]] $G\times X\to X$ of a [[group]] $G$ on a set $X$, for every element $x \in X$,  the __stabilizer subgroup__ of x (also called the __isotropy group__ of $x$) is the set of all elements in $G$ that leave $x$ fixed:

$$
  Stab_G(x) = \{g \in G \mid g\circ x = x\}
  \,.
$$

If all stabilizer groups are trivial, then the action is called a _free action_.


### Homotopy-theoretic formulation
 {#GeneralAbstract}

We reformulate the tradtitional definition [above](#TraditionalDefinition) from the [[nPOV]], in terms of [[homotopy theory]].

A [[group]] [[action]] $\rho\colon G \times X \to X$ is equivalently encoded in its [[action groupoid]] [[fiber sequence]] in [[Grpd]]

$$
  X \to X \sslash G \to \mathbf{B}G
  \,,
$$

where the $X \sslash G$ is the [[action groupoid]] itself, $\mathbf{B}G$ is the [[delooping]] [[groupoid]] of $G$ and $X$ is regarded as a [[0-truncated]] groupoid.

This fiber sequence may be thought of as being the $\rho$-[[associated bundle]] to the $G$-[[universal principal bundle]]. (Here discussed for $G$ a [[discrete group]] but this discussion goes through verbatim for $G$ a [cohesive group](/nlab/show/cohesive+%28infinity,1%29-topos+--+structures#InfinGroups)).

For

$$
  x\colon * \to X
$$

any [[global element]] of $X$, we have an induced element $x\colon * \to X \to X \sslash G$ of the action groupoid and may hence form the first [[homotopy group]] $\pi_1(X \sslash G, x)$. This is the stabilizer group. Equivalently this is the [[loop space object]] of $X \sslash G$ at $x$, given by the [[homotopy pullback]]

$$
  \array{
     Stab_G(x) &\to& * 
     \\
     \downarrow && \downarrow^{\mathrlap{x}}
     \\
     * &\stackrel{x}{\to}& X\sslash G
  }
  \,.
$$

This characterization immediately generalizes to stabilizer [[∞-groups]] of [∞-group actions](/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#GroupRepresentations). This we discuss [below](#ForInfinityGroupActions)


### For $\infty$-group actions
 {#ForInfinityGroupActions}

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and $G \in \infty Grp(G)$ be an [[∞-group]] object in $\mathbf{H}$. Write $\mathbf{B}G \in \mathbf{H}$ for its [[delooping]] object.


By the discussion at _[[∞-action]]_ we have the following.


+-- {: .num_prop #InfinityAction}
###### Proposition

For $X \in \mathbf{H}$ any object, an [[∞-action]] of $G$ on $X$ is equivalently an object $X \sslash G$ and a [[homotopy fiber sequence]] of the form

$$
  \array{
    X &\longrightarrow& X//G
    \\
    && \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

=--

Here $X//G$ is the [[homotopy quotient]] of the [[∞-action]]

+-- {: .num_remark}
###### Remark

The action as a morphism $X \times G \to X$ is recovered from prop. \ref{InfinityAction} by the [[(∞,1)-pullback]]

$$
  \array{
     X \times G &\to& X
     \\
     \downarrow && \downarrow
     \\
     X &\to& X \sslash G
  }
  \,.
$$

=--

+-- {: .num_defn #StabilizerInInfinityTopos}
###### Definition

Given an [[∞-action]] $\rho$ of $G$ on $X$ as in prop. \ref{InfinityAction},
and given a [[global element]]  of $X$

$$
  x \colon \ast \to X 
$$

then the **stabilizer $\infty$-group** $Stab_\rho(x)$ of the $G$-action at $x$ is the [[loop space object]]

$$
  Stab_\rho(x) \coloneqq \Omega_x (X // G)
 \,.
$$

=--

+-- {: .num_defn}
###### Remark

Equivalently, def. \ref{StabilizerInInfinityTopos}, gives the [[loop space object]] of the [[1-image]] $\mathbf{B}Stab_\rho(x)$ of the morphism

$$
  \ast \stackrel{x}{\to} X \to X//G
  \,.
$$

As such the [[delooping]] of the stabilizer $\infty$-group sits in a [[1-epimorphism]]/[[1-monomorphism]] factorization $\ast \to \mathbf{B}Stab_\rho(x) \hookrightarrow X//G$ which combines with the homotopy fiber sequence of prop. \ref{InfinityAction} to a diagram of the form

$$
  \array{
    \ast &\stackrel{x}{\longrightarrow}& X &\stackrel{}{\longrightarrow}& X//G
    \\
    \downarrow^{\mathrlap{epi}} && & \nearrow_{\mathrlap{mono}} & \downarrow
    \\
    \mathbf{B} Stab_\rho(x)
    &=&
    \mathbf{B} Stab_\rho(x)
    &\longrightarrow&
    \mathbf{B}G
  }
 \,.
$$

In particular there is hence a canonical homomorphism of $\infty$-groups

$$
  Stab_\rho(x) \longrightarrow G
  \,.
$$

However, in contrast to the classical situation, this morphism is not in general a monomorphism anymore, hence the stabilizer $Stab_\rho(x)$ is not a _sub_-group of $G$ in general.

=--




## Examples

### For an $\infty$-group acting on itself

For $G$ any [[∞-group]] in an [[(∞,1)-topos]] $\mathbf{H}$, its (right) [[action]] on itself is given by the [[looping and delooping|looping/delooping]] [[fiber sequence]]

$$
  G \to * \stackrel{\rho}{\to} \mathbf{B}G
  \,.
$$

Clearly, for every point $g \in G$ we have $Stab_{\rho}(g) \simeq * \times_* * \simeq *$ is trivial. Hence the action is free.


### Stabilizers of shapes -- Klein geometry
 {#KleinGeometry}

Let $X \to X\sslash G \stackrel{\rho}{\to} \mathbf{B}G$ be an [[∞-action]] of $G$ on $X$. 

Let $Y \in \mathbf{H}$ any other object, and regard it as equipped with the trivial $G$-action $Y \to Y \times \mathbf{B}G \to \mathbf{B}G$. There is then an induced [[∞-action]] $\rho_Y$ on the [[internal hom]] $[Y,X]$, the [[conjugation action]], given by internal hom in the [[slice (∞,1)-topos]] over $\mathbf{B}G$:

$$
  [Y,X] \to \underset{\mathbf{B}G}{\sum} [Y,X]_{/\mathbf{B}G} \to \mathbf{B}G
  \,.
$$

Now given any $f \colon Y \to X$, then the stabilizer group $Stab_{\rho_Y}(f)$ is the stabilizer of $Y$ "in" $X$ under this $G$-action. 

The morphism of $\infty$-groups

$$
  i_f\colon Stab_{\rho_Y}(f) \to G
$$

hence characterizes the [[higher Klein geometry]] induced by the $G$-action and by the shape $f\colon Y \to X$.


Notice that $\underset{\mathbf{B}G}{\sum} [Y,X]_{/\mathbf{B}G}$ is equivalently the [[(∞,1)-pullback]] 

$$
  \array{
    [Y,X] \sslash G &\to& [Y, X \sslash G]
    \\
    \downarrow^{\mathrlap{\rho_Y}} 
    && 
    \downarrow^{\mathrlap{[Y, \rho]}}
    \\
    \mathbf{B}G
    &\to&
    [Y, \mathbf{B}G]
  }
  \,,
$$

where the bottom morphism is the [[internal hom]] [[adjunct]] of the [[projection]] $Y \times \mathbf{B}G \to \mathbf{B}G$.

To see this, we check the Hom adjunction property: For any $p \colon A \to \mathbf{B}G$ we have

$$
  \array{
    && \mathbf{H}(A, [Y,X] \sslash G) &\to& \mathbf{H}(A,[Y, X \sslash G])
    \\
    \downarrow && \downarrow^{\mathrlap{\mathbf{H}(A,\rho_Y)}} 
    && 
    \downarrow^{\mathrlap{\mathbf{H}(A,[Y, \rho])}}
    \\
    \ast &\stackrel{\vdash p}{\longrightarrow}& \mathbf{H}(A,\mathbf{B}G)
    &\to&
    \mathbf{H}(A,[Y, \mathbf{B}G])
  }
  \,,
$$

$\simeq$

$$
  \array{
    && \mathbf{H}(A, [Y,X] \sslash G) &\to& \mathbf{H}(A \times Y, X \sslash G)
    \\
    \downarrow && \downarrow 
    && 
    \downarrow
    \\
    \ast &\stackrel{\vdash p}{\longrightarrow}& \mathbf{H}(A,\mathbf{B}G)
    &\to&
    \mathbf{H}(A \times Y,  \mathbf{B}G)
  }
  \,,
$$


## Related concepts

* [[normalizer subgroup]]

* [[centralizer subgroup]]

* [[stable point]]

* [[Klein geometry]], [[Cartan geometry]]

[[!redirects stabilizer group]]
[[!redirects stabilizer groups]]
[[!redirects stabiliser group]]
[[!redirects stabiliser groups]]


[[!redirects stabilizer]]
[[!redirects stabiliser]]
[[!redirects stabilizers]]
[[!redirects stabilisers]]

[[!redirects stabilizer ∞-group]]
[[!redirects stabilizer infinity-group]]
[[!redirects stabiliser ∞-group]]
[[!redirects stabiliser infinity-group]]
[[!redirects stabilizer ∞-groups]]
[[!redirects stabilizer infinity-groups]]
[[!redirects stabiliser ∞-groups]]
[[!redirects stabiliser infinity-groups]]


[[!redirects stabilizer subgroup]]
[[!redirects stabiliser subgroup]]
[[!redirects stabilizer subgroups]]
[[!redirects stabiliser subgroups]]

[[!redirects isotropy group]]
[[!redirects isotropy groups]]