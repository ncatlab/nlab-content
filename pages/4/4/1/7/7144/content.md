
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

### Explicitly

Given an [[action]] $G\times X\to X$ of a [[group]] $G$ on a set $X$, for every element $x \in X$,  the __stabilizer subgroup__ of x (also called the __isotropy group__ of $x$) is the set of all elements in $G$ that leave $x$ fixed:

$$
  Stab_G(x) = \{g \in G \mid g\circ x = x\}
  \,.
$$

If all stabilizer groups are trivial, then the action is called a _free action_.


### General abstract characterization  {#GeneralAbstract}

We discuss stabilizer subgroups from the [[nPOV]].

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

Then for $X \in \mathbf{H}$ any other object, an [[action]] of $G$ on $X$ is an object $X \sslash G$ and a [[fiber sequence]] of the form

$$
  X \to X \sslash G \stackrel{\rho}{\to} \mathbf{B}G
  \,.
$$

The action as a morphism $X \times G \to X$ is recovered from this by the [[(∞,1)-pullback]]

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

Now for $x\colon * \to X$ any [[global element]], the **stabilizer $\infty$-group** of $\rho$ at $x$ is the [[loop space object]]

$$
  Stab_\rho(x) \coloneqq \Omega_x (X\sslash G)
 \,.
$$

This is equipped with a canonical morphism of [[∞-group]] objects

$$
  i_x\colon Stab_\rho(x) \to G
$$

given by the [[fiber sequence|looping]] of $\rho$

$$
  i_x \coloneqq \Omega_x(\rho)
  \,.
$$


## Examples

### For an $\infty$-group acting on itself

For $G$ any [[∞-group]] in an [[(∞,1)-topos]] $\mathbf{H}$, its (right) [[action]] on itself is given by the [[looping and delooping|looping/delooping]] [[fiber sequence]]

$$
  G \to * \stackrel{\rho}{\to} \mathbf{B}G
  \,.
$$

Clearly, for every point $g \in G$ we have $Stab_{\rho}(g) \simeq * \times_* * \simeq *$ is trivial. Hence the action is free.


### Stabilizers of shapes

For $X\sslash G \stackrel{\rho}{\to} \mathbf{B}G$ an [[action]], and $Y \in \mathbf{H}$ any other object, we get an induced action $\rho_Y$ on the [[internal hom]] $[Y,X]$ defined as the [[(∞,1)-pullback]] 

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

Then for $f\colon Y \to X$ a "shape" $Y$ in $X$, the stabilizer ∞-group of $Y$ under $\rho$ is $Stab_{\rho_Y}(f)$.

The morphism of $\infty$-groups

$$
  i_f\colon Stab_{\rho_Y}(f) \to G
$$

characterizes the [[higher Klein geometry]] induced by $f\colon Y \to X$.


## Related concepts

* [[normalizer subgroup]]

* [[centralizer subgroup]]

* [[stable point]]

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
