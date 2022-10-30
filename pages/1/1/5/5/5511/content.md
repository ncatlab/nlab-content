
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The generalization of the notion of [[effective epimorphism]] from [[category theory]] to [[(∞,1)-category theory]].

See also at _[[1-epimorphism]]_. 

## Definition

+-- {: .num_def}
###### Definition

A [[morphism]] $f : Y \to X$ in an [[(∞,1)-category]] is an **effective epimorphism** if it has a [[Cech nerve]], of which it is the [[(∞,1)-colimit]]; in other words the augmented simplicial diagram

$$
  \cdots
  Y \times_X Y \times_X Y 
  \stackrel{\tl}{\stackrel{\to}{\to}}
Y \times Y \times_X Y \stackrel{\to}{\to}  Y \stackrel{f}{\to} X
$$

is a colimiting diagram.

=--

This appears below [[Higher Topos Theory|HTT, cor. 6.2.3.5]] for $C$ a [[(∞,1)-semitopos]], but seems to be a good definition more generally.


## Properties

### Factorization

In an [[(∞,1)-topos]] the effective epis are the [[n-epimorphisms]] for $n = 1$ sitting in the [[(n-epi, n-mono) factorization system]] for $n = 1$ with the [[monomorphism in an (∞,1)-category]], factoring every morphism through its [[1-image]].

### Stability

+-- {: .num_prop}
###### Proposition

In an [[(∞,1)-semitopos]], effective epimorphisms are stable under [[(∞,1)-pullback]].

=--

This appears as ([Lurie, prop. 6.2.3.15](#Lurie)).



### Characterization
 {#Characterization}

+-- {: .num_prop}
###### Proposition

For $C$ an [[(∞,1)-semitopos]]  we have that $f : X \to Y$ is an effective epimorphism precisely if its (-1)-[[truncated|truncation]] is a [[terminal object in an (∞,1)-category|terminal object]] in the [[over-(∞,1)-category]] $C/Y$.

=--

This is [[Higher Topos Theory|HTT, cor. 6.2.3.5]].


More generally, 

+-- {: .num_prop }
###### Proposition

The effective epimorphisms in any [[(∞,1)-topos]] are precisely the [[n-connected object of an (infinity,1)-topos|(-1)-connected morphisms]], and form a [[orthogonal factorization system in an (∞,1)-category|factorization system]] together with the [[monomorphism in an (∞,1)-category|monomorphisms]] (the (-1)-truncated morphisms).

=--

See [[n-connected/n-truncated factorization system]] for more on this.

+-- {: .num_prop #CharacterizationByActionOnSubobjects}
###### Proposition

For $C$ an [[(∞,1)-topos]], a morphism $f : X \to Y$ in $C$ is effective epi precisely if the induced morphism on [[subobjects]] ([[monomorphism in an (∞,1)-category|(∞,1)-monos]], they form actually a [[small set]]) by [[(∞,1)-pullback]]

$$
  f^* : Sub(Y) \to Sub(X)
$$

is [[injective function|injective]].

=--

This appears as ([Rezk, lemma 7.9](#Rezk)). 

Useful is also the following characterization:

+-- {: .num_prop #CharacterizationAsEpiOnZeroTruncation}
###### Proposition

A morphism in an [[(∞,1)-topos]] is an effective epimorphism precisely if its [[0-truncated|0-truncation]] is an [[effective epimorphism]] in the underlying 1-[[topos]].

=--

This is ([Lurie, prop. 7.2.1.14](#Lurie)).

+-- {: .num_remark}
###### Remark

In words this means that a map is an effective epimorphism if it induces an epimorphism on connected components. 

=--

This is true generally in the [[internal logic]] of the $(\infty,1)$-topos (i.e. in [[homotopy type theory]], see at [[1-epimorphism]] for more on this), but in [[∞Grpd]] $\simeq L_{whe}$ [[sSet]] it is also true externally (prop. \ref{EffectiveEpisOfInfinityGroupoids} below):

+-- {: .num_example}
###### Example

A morphism of [[∞-groupoids]] $f \colon X \to Y$ is an effective epimorphism precisely if it is a [[surjection]] on connected components, hence if

$$
  \pi_0(f) \colon \pi_0(X) \to \pi_0(Y)
$$

is a surjection of sets.

=--


## Examples

As a corollary of prop. \ref{CharacterizationAsEpiOnZeroTruncation} we have

+-- {: .num_prop #EffectiveEpisOfInfinityGroupoids}
###### Proposition
**(effective epis of $\infty$-groupoids**)

In $C = $ [[∞Grpd]] a morphism $f : Y \to X$ is an effective epimorphism precisely if it induces an [[epimorphism]] $\pi_0 f : \pi_0 Y \to \pi_0 X$ in [[Set]] on connected components.
 
=--

This appears as [[Higher Topos Theory|HTT, cor. 7.2.1.15]].  



## Related concepts

* [[effective epimorphism]]

* **effective epimorphism in an $(\infty,1)$-category**

* [[regular epimorphism in an (∞,1)-category]]

* [[n-connected object of an (∞,1)-category]]

## References

Section 7.7 of 

* [[Charles Rezk]], _Toposes and homotopy toposes_ ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))
  {#Rezk}

Section 6.2.3 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
  {#Lurie}

[[!redirects effective epimorphism in an (∞,1)-category]]
[[!redirects effective epimorphisms in an (∞,1)-category]]
[[!redirects effective epimorphisms in an (infinity,1)-category]]
