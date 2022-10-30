
#Contents#
* table of contents
{:toc}

## Definition

### Explicitly

Given an [[action]] $G\times X\to X$ of a [[group]] $G$ on a set $X$, for every element $x \in X$,  the __stabilizer subgroup__ of x (also called the __isotropy group__ of $x$) is the set of all elements in $G$ that leave $x$ fixed:

$$
  Stab_G(x) = \{g \in G \mid g\circ x = x\}
  \,.
$$


### General abstract characterization  {#GeneralAbstract}

We discuss stabilizer subgroups from the [[nPOV]].

A [[group]] [[action]] $\rho : G \times X \to X$ is equivalently encoded in its [[action groupoid]] [[fiber sequence]] in [[Grpd]]

$$
  X \to X\sslash G \to \mathbf{B}G
  \,,
$$

where the $X\sslash G$ is the [[action groupoid]] itself, $\mathbf{B}G$ is the [[delooping]] [[groupoid]] of $G$ and $X$ is regarded as a [[0-truncated]] groupoid.

This fiber sequence may be thought of as being the $\rho$-[[associated bundle]] to the $G$-[[universal principal bundle]]. (Here discussed for $G$ a [[discrete group]] but this discussion goes through verbatim for $G$ a [cohesive group](/nlab/show/cohesive+%28infinity,1%29-topos+--+structures#InfinGroups)).

For

$$
  x : * \to X
$$

any [[global element]] of $X$, we have an induced element $x : * \to X \to X\sslash G$ of the action groupoid and may hence form the first [[homotopy group]] $\pi_1(X\sslash G, x)$. This is the stabilizer group. Equivalently this is the [[loop space object]] of $X\sslash G$ at $x$, given by the [[homotopy pullback]]

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

This characterization immediately generalizes to stabilizer [[∞-groups]] of [∞-group actions](/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#GroupRepresentations).



[[!redirects stabilizer]]
[[!redirects stabiliser]]
[[!redirects stabilizers]]
[[!redirects stabilisers]]

[[!redirects stabiliser subgroup]]

[[!redirects stabilizer subgroups]]
[[!redirects stabiliser subgroups]]

[[!redirects isotropy group]]
[[!redirects isotropy groups]]
