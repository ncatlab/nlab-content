
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--


> under construction


 
#Contents#
* table of contents
{:toc}

## Idea

[[cobordism theory]] for unoriented manifolds with stably [[framed manifold|framed]] [[manifold with boundary|boundaries]], thus unifying [[MO]] with [[MFr]].

## Definition

Consider the [[cofiber sequence]] of the unit morphism of the [[ring spectrum]] [[MO]]

\[
  \label{AsUnitCofiber}
  \array{
    \mathbb{S}
    &
      \overset{
        1^{M\mathrm{O}}
      }{
        \longrightarrow
      }
    &
    M \mathrm{O}
    \\
    \big\downarrow
    &
    {}^{{}_{(po)}}
    &
    \big\downarrow
    \\
    \ast 
    &\longrightarrow&
    M \mathrm{O}/ \mathbb{S}
  }
\]

The [[homotopy cofiber]]

$$
  M(\mathrm{O},fr)
  \;\coloneqq\;
  M \mathrm{O} / \mathbb{S}
  \,,
$$

has [[stable homotopy groups]] the [[cobordism ring]] of unoriented bordisms with [[stable tangent bundle|stably]] [[framed manifold|framed]] [[manifold with boundary|boundaries]]


\[
  \label{OFrCobordismRing}
  \Omega^{\mathrm{O},fr}_{\bullet}
  \;\coloneqq\;
  \pi_{\bullet}
  \big(
    M\mathrm{O}/\mathbb{S}
  \big)
\]

## Properties

### Boundary morphism to $MFr$
  {#BoundaryMorphism}

The realization (eq:AsUnitCofiber) makes it manifest  that there is a [[cohomology operation]] to [[MFr]] of the form

\[
  \label{BoundaryCohomologyOperation}
  \array{
    M(\mathrm{O},fr)
    \;=
    &
    M \mathrm{O}/\mathbb{S}
    &
    \overset{
      \;\;\;
      \partial
      \;\;\;
    }{\longrightarrow}
    &
    \Sigma 
    \mathbb{S}
    & =\;
    \Sigma Mfr
    \\
    \pi_{2d+2}\big( M(\mathrm{O},fr) \big)
    &&
    \longrightarrow
    &&
    \pi_{2d+1}\big( Mfr \big)
  }
  \,.
\]

Namely, $\partial$ is the second next step in the long [[homotopy cofiber]]-sequence starting with $1^{M \mathrm{O}}$. In terms of the [[pasting law]]:

\[
  \label{BoundaryOperationViaPastingLaw}
  \array{
    \mathbb{S}
    &
      \overset{
        1^{M\mathrm{O}}
      }{
        \longrightarrow
      }
    &
    M \mathrm{O}
    &
    \longrightarrow
    &
    \ast
    \\
    \big\downarrow
    &
    {}^{{}_{(po)}}
    &
    \big\downarrow
    &
    {}^{{}_{(po)}}
    &
    \big\downarrow
    \\
    \ast 
    &
    \longrightarrow
    &
    M \mathrm{O}/ \mathbb{S}
    &
      \underset{
        \partial
      }{
        \longrightarrow
      }
    &    
    \Sigma \mathbb{S}
  }
\]


### Relation to $M \mathrm{O}$ and $M Fr$


+-- {: .num_prop #PositiveDegreeFramedBordismTrivialInUnorientedBordism} 
###### Proposition

The unit morphism of [[MO]] is trivial on [[stable homotopy groups]] in [[positive number|positive]] degree:

$$
  \array{
    \pi_{n+1}
    \big(
      \mathbb{S}
    \big)
    &
    \overset{ 1^{M \mathrm{O}} }{\longrightarrow}
    &
    \pi_{n + 1}
    \big(
      M \mathrm{O} 
    \big)
    \\
    \big\downarrow{}^{\mathrlap{=}}
    &&
    \big\downarrow{}^{\mathrlap{=}}
    \\
    \Omega^{fr}_{n + 1}
    &\underset{i}{\longrightarrow}&
    \Omega^{\mathrm{O}}_{n + 1}
  }
  \phantom{AAAAAAA}
  n \in \mathbb{N}
$$

=--

([Stong 68, p. 102-103](#Stong68))


+-- {: .num_prop #AShortExactSequenceOfOFrBordismRings} 
###### Proposition

In [[positive number|positive]] degree, the underling [[abelian groups]] of the [[bordism rings]] for [[MO]], [[MFr]] and $MOFr$ (eq:OFrCobordismRing) sit in [[short exact sequences]] of this form:

\[
  \label{ShortExactSequenceOfUFrBordismRings}
  0 
  \to
  \Omega^{\mathrm{O}}_{n+2}
  \overset{i}{\longrightarrow}
  \Omega^{\mathrm{O},fr}_{n+2}
  \overset{\partial}{
    \longrightarrow
  }
  \Omega^{fr}_{n+1}
  \to
  0
  \,,
  \phantom{AAAA}
  n \in \mathbb{N}
  \,,
\]

where $i$ is the evident inclusion, while $\partial$ is the [[boundary]] homomorphism from [above](#BoundaryMorphism). 

=--

([Stong 68, p. 102-103](#Stong68))

+-- {: .proof}
###### Proof

We have the [[long exact sequence of homotopy groups]] obtained from the [[cofiber sequence]] $\mathbb{S} \overset{1^{M\mathrm{O}}}{\longrightarrow} M \mathrm{O} \to M \mathrm{O}/\mathbb{S} \overset{\partial}{\to} \Sigma \mathbb{S}$ (eq:BoundaryOperationViaPastingLaw), the relevant part of which looks as follows:

\[
  \label{SToMULongExactSequenceOfHomotopyGroups}
  \array{
    \pi_{d+2}
    \big(
      \mathbb{S}
    \big)
    &
    \overset{
      1^{M\mathrm{O}}
    }{
      \longrightarrow
    }
    &
    \pi_{d+2}
    \big( 
      M\mathrm{O}
    \big)
    &
    \overset{
    }{\longrightarrow}
    &
    \pi_{d+2}
    \big(
      M\mathrm{O}/\mathbb{S}
    \big)
    &
    \overset{
      \partial
    }{\longrightarrow}
    &
    \pi_{d+1}\big(\mathbb{S}\big)
    &\longrightarrow&
    \pi_{d+1}\big(M\mathrm{O}\big)  
    \\
    \big\downarrow{}^{\mathrlap{=}}
    &&
    \big\downarrow{}^{\mathrlap{=}}
    &&
    \big\downarrow{}^{\mathrlap{=}}
    &&
    \big\downarrow{}^{\mathrlap{=}}
    &&
    \big\downarrow{}^{\mathrlap{=}}
    \\
    \Omega^{fr}_{d+2}
    &
    \underset{
      \color{green}
      0
    }{
      \longrightarrow
    }
    &
    \Omega^{\mathrm{O}}_{d+2}
    &
    \underset{
      i
    }{\longrightarrow}
    &
    \Omega^{(\mathrm{O},fr)}_{d+2}
    &
    \underset{
      \partial
    }{\longrightarrow}
    &   
    \Omega^{fr}_{d + 1}
    &
    \underset{
      \color{green}
      0
    }{\longrightarrow}
    &   
    \Omega^{\mathrm{O}}_{d+1}
  }
\]

Here the two outermost morphisms shown are [[zero morphisms]], by Prop. \ref{PositiveDegreeFramedBordismTrivialInUnorientedBordism}, and hence the claim follows.

=--


## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

* {#Stong68} [[Robert Stong]], p. 102-106 of: _Notes on Cobordism theory_, Princeton University Press, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/stongcob.pdf))

Analogous discussion for [[MO]]-bordism with [[MSO]]-boundaries:

* G. E. Mitchell, _Bordism of Manifolds with Oriented Boundaries_, Proceedings of the American Mathematical Society Vol. 47, No. 1 (Jan., 1975), pp. 208-214 ([doi:10.2307/2040234](https://doi.org/10.2307/2040234))

