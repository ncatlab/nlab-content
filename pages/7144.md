
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

Given an [[action]] of a [[group]] on some [[space]], and given a point or (or more generally some subspace), then the _stabilizer group_ of that point (that subspace) is the [[subgroup]] whose action leaves the point (the subspace) fixed, [[invariant]].

The importance of stabilizer subgroups for the general development of [[geometry]] was famously highlighted in ([Klein 1872](#Klein1872)) in the context of what has come to be known the _[[Erlangen program]]_. For more on this aspect see at _[[Klein geometry]]_ and _[[Cartan geometry]]_. 

Sometimes (such as in the context of [[Wigner classification]]) stabilizer groups are called _little groups_.

## Definition

### Traditional
 {#TraditionalDefinition}

Given an [[action]] $G\times X\to X$ of a [[group]] $G$ on a set $X$, for every element $x \in X$,  the __stabilizer subgroup__ of $x$ (also called the __isotropy group__ of $x$) is the set of all elements in $G$ that leave $x$ fixed:

$$
  Stab_G(x) = \{g \in G \mid g\circ x = x\}
  \,.
$$

If all stabilizer groups are trivial, then the action is called a _free action_.


### Homotopy-theoretic formulation
 {#GeneralAbstract}

We reformulate the traditional definition [above](#TraditionalDefinition) from the [[nPOV]], in terms of [[homotopy theory]].

A [[group]] [[action]] $\rho\colon G \times X \to X$ is equivalently encoded in its [[action groupoid]] [[fiber sequence]] in [[Grpd]]

$$
  X \to X//G \to \mathbf{B}G
  \,,
$$

where the $X//G$ is the [[action groupoid]] itself, $\mathbf{B}G$ is the [[delooping]] [[groupoid]] of $G$ and $X$ is regarded as a [[0-truncated]] groupoid.

This fiber sequence may be thought of as being the $\rho$-[[associated bundle]] to the $G$-[[universal principal bundle]]. (Here discussed for $G$ a [[discrete group]] but this discussion goes through verbatim for $G$ a [cohesive group](/nlab/show/cohesive+%28infinity,1%29-topos+--+structures#InfinGroups).)

For

$$
  x\colon * \to X
$$

any [[global element]] of $X$, we have an induced element $x\colon * \to X \to X//G$ of the action groupoid and may hence form the first [[homotopy group]] $\pi_1(X//G, x)$. This is the stabilizer group. Equivalently this is the [[loop space object]] of $X//G$ at $x$, given by the [[homotopy pullback]]

$$
  \array{
     Stab_G(x) &\to& * 
     \\
     \downarrow && \downarrow^{\mathrlap{x}}
     \\
     * &\stackrel{x}{\to}& X//G
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

For $X \in \mathbf{H}$ any object, an [[∞-action]] of $G$ on $X$ is equivalently an object $X/G$ and a [[homotopy fiber sequence]] of the form

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

Here $X/G$ is the [[homotopy quotient]] of the [[∞-action]]

+-- {: .num_remark}
###### Remark

The action as a morphism $X \times G \to X$ is recovered from prop. \ref{InfinityAction} by the [[(∞,1)-pullback]]

$$
  \array{
     X \times G &\to& X
     \\
     \downarrow && \downarrow
     \\
     X &\to& X//G
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
  Stab_\rho(x) \coloneqq \Omega_x (X//G)
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

### For a group acting on itself

For $G$ any [[∞-group]] in an [[(∞,1)-topos]] $\mathbf{H}$, its (right) [[action]] on itself is given by the [[looping and delooping|looping/delooping]] [[fiber sequence]]

$$
  G \to * \stackrel{\rho}{\to} \mathbf{B}G
  \,.
$$

Clearly, for every point $g \in G$ we have $Stab_{\rho}(g) \simeq * \times_* * \simeq *$ is trivial. Hence the action is free.


### Stabilizers of shapes -- Klein geometry
 {#KleinGeometry}

Let $X \to X//G \stackrel{\rho}{\to} \mathbf{B}G$ be an [[∞-action]] of $G$ on $X$. 

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

hence characterizes the ([[higher Klein geometry|higher]]) [[Klein geometry]] induced by the $G$-action and by the shape $f\colon Y \to X$. (See at [Klein geometry -- History](Klein+geometry#History).)


For completeness we notice that:

+-- {: .num_prop #ReformulationOfRightSidedConjugationAction}
###### Proposition


Here  $(\underset{\mathbf{B}G}{\sum} [Y,X]_{/\mathbf{B}G} \to \mathbf{B}G )$ is equivalently the [[(∞,1)-pullback]]  $\rho_Y$ in

$$
  \array{
    \underset{\mathbf{B}G}{\sum} [Y,X]_{/\mathbf{B}G} &\to& [Y, X//G]
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

=--

+-- {: .proof}
###### Proof

We check the Hom adjunction property, that for any $(A//G \stackrel{\alpha}{\to} \mathbf{B}G) \in \mathbf{B}G$ we have

$$
  \mathbf{H}_{/\mathbf{B}G}(A,[Y,X]_{\mathbf{B}G})
  \simeq
  \mathbf{H}_{/\mathbf{B}G}(A\times_{\mathbf{B}G} Y, X)
$$

with $[Y,X]_{/\mathbf{B}G}$ replaced by the above pullback. 

Notice that by the $G$-action on $Y$ being trivial, we have $A \times_{\mathbf{B}G} Y \simeq (A//G \times Y  \stackrel{p_1}{\to} A//G \stackrel{\alpha}{\to} \mathbf{B}G) \in \mathbf{H}_{/\mathbf{B}G}$.


Then use the characterization of [Hom-spaces in a slice](over-%28infinity%2C1%29-category#HamSpacesInASlice) to find $\mathbf{H}_{/\mathbf{B}G}(A,[Y,X]_{\mathbf{B}G})$ as the [[homotopy pullback]] on the left of


$$
  \array{
    \mathbf{H}_{/\mathbf{B}G}(A,[Y,X]_{\mathbf{B}G}) 
      &\longrightarrow& 
    \mathbf{H}(A//G, [Y,X]//G) &\to& \mathbf{H}(A//G,[Y, X//G])
    \\
    \downarrow && \downarrow^{\mathrlap{\mathbf{H}(A//G,\rho_Y)}} 
    && 
    \downarrow^{\mathrlap{\mathbf{H}(A//G,[Y, \rho])}}
    \\
    \ast 
      &\stackrel{\vdash \alpha}{\longrightarrow}& 
    \mathbf{H}(A//G,\mathbf{B}G)
      &\to&
    \mathbf{H}(A//G,[Y, \mathbf{B}G])
  }
  \,,
$$

Now using the Hom-adjunction in $\mathbf{H}$ itself, the fact that $\mathbf{H}(A//G,-)$ preserves [[homotopy pullbacks]] and the [[pasting law]] this is equivalent to

$$
  \array{
    \mathbf{H}_{/\mathbf{B}G}(A\times_{\mathbf{B}G} Y, X) 
      &\longrightarrow&  
      &\longrightarrow& 
    \mathbf{H}(A//G \times Y, X //G)
    \\
    \downarrow && \downarrow 
    && 
    \downarrow
    \\
    \ast 
      &\stackrel{\vdash \alpha}{\longrightarrow}& 
    \mathbf{H}(A//G,\mathbf{B}G)
      &\to&
    \mathbf{H}(A//G \times Y,  \mathbf{B}G)
  }
  \,,
$$

Here the bottom map is indeed the name of $\alpha \circ p_1$ and so again by the pullback characterization of [Hom-spaces in a slice](over-%28infinity%2C1%29-category#HamSpacesInASlice) this pasting diagram does exhibit $\mathbf{H}_{/\mathbf{B}G}(A\times_{\mathbf{B}G} Y, X)$ as indicated.

=--

### For the canonical action on a coset space
 {#ForCanonicalActionOnCosetSpace}

Conversely, for any [[homomorphism]] $H \to G$ of [[∞-groups]] given, then the canonical $G$-$\infty$-action for which $H$ is the stabilizer $\infty$-group of a point is the canonical action on (the "[[coset]]") $G/H$.

This follows from def. \ref{StabilizerInInfinityTopos} by observing that the homotopy fiber sequence of prop. \ref{InfinityAction} for the $G$-action on $G/H$ is just 

$$
  \array{
    G/H &\stackrel{}{\longrightarrow}& \mathbf{B}H
    \\
    && \downarrow
    \\
    && \mathbf{B}G
  }
$$

so that for any point $x \colon \ast \to G/H$ we have

$$
  Stab(x) \simeq \Omega_{x}(\mathbf{B}H) \simeq \Omega_\ast \mathbf{B}H \simeq H
  \,.
$$

### Stabilizers of coshapes
 {#StabilizersOfCoShapes}

Dually to "stabilizers of shapes", as [above](#KleinGeometry) one may consider stabilizers of "co-shapes".

I.e. given a $G$-action on $X$, and given a map $f \colon X \to A$, then one may ask for the stabilizer of $f$ in the canonical $G$-action on $[X,A]$.

For instance if $A$ here is $\mathbf{B}^{n}U(1)_{conn}$, and $f \colon X \to \mathbf{B}^n U(1)_{conn}$ is regarded as a [[prequantum n-bundle]] ,and $[X,A]$ is replaced by its [[differential concretification]], then these stabilizers are the [[quantomorphism n-groups]].

> to be expanded on


## Related concepts

* [[normalizer subgroup]]

* [[centralizer subgroup]]

* [[stable point]]

* [[Klein geometry]], [[Cartan geometry]]

## References

An early occurence of the concept of stabilizer subgroups:

* {#Klein1872} [[Felix Klein]], p. 4 of: _Vergleichende Betrachtungen &#252;ber neuere geometrische Forschungen_ (1872)

  translation by M. W. Haskell, _A comparative review of recent researches in geometry_ , trans. M. W. Haskell, Bull. New York Math. Soc. 2, (1892-1893), 215-249. ([retyped pdf](http://math.ucr.edu/home/baez/erlangen/erlangen_tex.pdf), [[KleinRetyped.pdf:file]], [scan of original](http://math.ucr.edu/home/baez/erlangen/erlangen.pdf))

  (the "[[Erlangen program]]").



* {#Bredon72} [[Glen Bredon]], Section I.2 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))


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

[[!redirects homotopy stabilizer group]]
[[!redirects homotopy stabilizer groups]]


[[!redirects stabilizer subgroup]]
[[!redirects stabiliser subgroup]]
[[!redirects stabilizer subgroups]]
[[!redirects stabiliser subgroups]]

[[!redirects isotropy group]]
[[!redirects isotropy groups]]
[[!redirects isotropy subgroup]]
[[!redirects isotropy subgroups]]

[[!redirects stabilizer 2-group]]
[[!redirects stabilizer 2-groups]]

[[!redirects little group]]
[[!redirects little groups]]
