
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

See also at _[[1-epimorphism]]_. However, beware of the [[red herring principle]]: effective epimorphisms in an $(\infty, 1)$-category need _not_ be [[epimorphism in an (infinity,1)-category|epimorphisms]].

## Definition

+-- {: .num_defn}
###### Definition

A [[morphism]] $f : Y \to X$ in an [[(∞,1)-category]] is an **effective epimorphism** if it has a [[Cech nerve]], of which it is the [[(∞,1)-colimit]]; in other words the [[augmented simplicial set|augmented simplicial]] [[diagram]]

$$
  \cdots
  Y \times_X Y \times_X Y 
  \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
 Y \times_X Y \stackrel{\longrightarrow}{\longrightarrow}  Y \stackrel{f}{\longrightarrow} X
$$

is an [[(∞,1)-colimit|colimiting]] diagram.

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

This appears as ([Rezk, lemma 7.9](#Rezk)) and ([Lurie, prop. 6.2.3.10](#Lurie)). 

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

This is true generally in the [[internal logic]] of the $(\infty,1)$-topos (i.e. in [[homotopy type theory]], see at [[1-epimorphism]] for more on this), but in [[∞Grpd]] $\simeq L_{whe}$ [[sSet]] it is also true externally (prop. \ref{EffectiveEpisOfInfinityGroupoids} below).




### In a sheaf $\infty$-topos

In the [[infinity-topos]] of [[infinity-sheaves]] on an $\infty$-site (i.e. in a [[topological localization]]), one has the following characterization of morphisms which become effective epimorphisms after applying the [[associated sheaf functor]].

+-- {: .num_prop #EffectiveEpiInSheafTopos}
###### Proposition
Let $(C,t)$ be an $\infty$-site and $f : F \to G$ a morphism of [[presheaves]] in $P(C)$.
The morphism $a_t(f)$ is an effective epimorphism in $Shv_t(C)$ if and only if $f$ is a [[local epimorphism]], i.e.
  $$ \colim \check{C}(f) \longrightarrow G $$
is $t$-covering, or in other words
  $$ \colim \check{C}(f) \times_G h(X) \longrightarrow h(X) $$
is a $t$-[[covering sieve]] for all morphisms $h(X) \to G$, where $h$ is the [[Yoneda embedding]].
(Here $a_t$ denotes the [[associated sheaf functor]].)
=--

This is clear.  See [MO/177325/2503](http://mathoverflow.net/a/177325/2503) by [[David Carchedi]] for the argument.

## Examples

### In $\infty Grpd$

As a corollary of prop. \ref{CharacterizationAsEpiOnZeroTruncation} we have:

+-- {: .num_prop #EffectiveEpisOfInfinityGroupoids}
###### Proposition
**(effective epis of $\infty$-groupoids**)

In $C = $ [[∞Grpd]] a morphism $f : Y \to X$ is an effective epimorphism precisely if it induces an [[epimorphism]] $\pi_0 f : \pi_0 Y \to \pi_0 X$ in [[Set]] on [[connected components]].
 
=--

This appears as [[Higher Topos Theory|HTT, cor. 7.2.1.15]].  

+-- {: .num_example #AnEffectiveEpiNotBeingEpiInInfinityGroupoids}
###### Example


If $S^1 = \ast \underset{\ast \coprod \ast}{\coprod} \ast$ denotes the [[homotopy type]] of the [[circle]], then the unique morphism $S^1 \to \Delta^0$ is an effective epimorphism, by prop. \ref{EffectiveEpisOfInfinityGroupoids}, but it not an [[epimorphism in an (infinity,1)-category|epimorphism]], because the [[suspension]] of $S^1$ is the [[sphere]] $S^2$, which is not [[contractible]].

=--



## Related concepts

* [[effective epimorphism]]

* **effective epimorphism in an $(\infty,1)$-category**

* [[regular epimorphism in an (∞,1)-category]]

* [[n-connected object of an (∞,1)-category]]

* [[n-types cover]]

## References

Section 7.7 of 

* {#Rezk} [[Charles Rezk]], _Toposes and homotopy toposes_ ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))

Section 6.2.3 of

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects effective epimorphism in an (∞,1)-category]]
[[!redirects effective epimorphisms in an (∞,1)-category]]
[[!redirects effective epimorphisms in an (infinity,1)-category]]