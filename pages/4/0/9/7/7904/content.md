
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $\mathbf{H}$ be an ambient [[(∞,1)-topos]]. Let $V, X$ be two [[objects]] of $\mathbf{H}$. Then a _$V$-[[fiber bundle]]_ over $X$ in $\mathbf{H}$ is a morphism $E \to X$ such that there is an [[effective epimorphism]] $U \to X$ and an [[(∞,1)-pullback]] square of the form

$$
  \array{
    U \times V &\to& E
    \\
    \downarrow && \downarrow
    \\
    U &\to& X
  }
  \,.
$$

Externally this is a _$V$-fiber $\infty$-bundle_.

See at _[[associated ∞-bundle]]_ for more.

## Example

A fiber $\infty$-bundle whose typical fiber $V$ is a pointed [[connected object in an (∞,1)-topos|connected object]], hence a [[delooping]] $\mathbf{B}G$ of an [[∞-group]] $G$

$$
  V \simeq \mathbf{B}G
$$

is a _$G$-[[∞-gerbe]]_.

## Properties

Every $V$-fiber $\infty$-bundle is the [[associated ∞-bundle]] to an [[automorphism ∞-group]]-[[principal ∞-bundle]].

For let $Type$ be the [[object classifier]]. Then any bundle $E \to X$ is classified by a morphism

$$
  X \longrightarrow Type
$$

On the other hand, since the pullback to the bundle on some $U$ is trivializable, that bundle over $U$ is classsified by a map that factors through the point which is the name of the fiber $V$

$$
  U \longrightarrow \ast \stackrel{\vdash V}{\longrightarrow} Type
  \,.
$$

The [[1-image]]-of this point inclusion is the [[delooping]] of the [[automorphism ∞-group]] of $V$ :

$$
  U \longrightarrow \ast \longrightarrow \mathbf{B}\mathbf{Aut}(V) \hookrightarrow Type
  \,.
$$

Therefore the fact that $E$ is trivialized over $U$ means that there the classifying maps fit into a [[commuting diagram]] of the form

$$
  \array{
     U  &\longrightarrow& \mathbf{B}\mathbf{Aut}(V)
     \\
     \downarrow && \downarrow
     \\
     X &\longrightarrow& Type
  }
$$

By assumption the left morphism is a [[1-epimorphism]] and by the above construction the right morphism is a [[1-monomorphism]]. Therefore by the [[(n-connected, n-truncated) factorization system]] this diagram has an essentially unique lift

$$
  \array{
     U  &\longrightarrow& \mathbf{B}\mathbf{Aut}(V)
     \\
     \downarrow &\nearrow& \downarrow
     \\
     X &\longrightarrow& Type
  }
$$

This diagonal lift classifies an $\mathbf{Aut}(V)$-[[principal ∞-bundle]] and the commutativity of the bottom right triangle exhibits the original bundle $E \to X$ as the [[associated ∞-bundle]] to that.

## Related concepts

* [[associated ∞-bundle]], [[principal ∞-bundle]]

* [[∞-gerbe]]

* [[local coefficient ∞-bundle]]

## References

See the references at _[[associated ∞-bundle]]_. 

The explicit general definition appears as def. 4.1 in part I of

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal infinity-bundles]]_

[[!redirects fiber ∞-bundle]]
[[!redirects fiber ∞-bundles]]
