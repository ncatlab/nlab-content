
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


If one considers a [[hyperdoctrine]] of [[subobject lattices]], hence a collection of them parameterized over a [[category of contexts]] and equipped with [[pullback]]/[[substitution]]/[[context extension]], then a _universal closure operator_ or _[[modality]]_ is a [[closure operator]] acting on each of the slices and being compatible with the pullback operation. A hyperdoctrine equipped with such an operator is sometimes called a _[[modal hyperdoctrine]]_.

If there is moreover a [[subobject classifier]] $\Omega$ (hence if that hyperdoctrine is the collection of [[slice categories]] of a [[topos]]) then a universal closure operator is represented by a single [[monad]]/[[comonad]] on that subobject classifier, $\Diamond \colon \Omega \to \Omega$, see the discussion [below](DefinitionForReflectiveSubcategories).

Instead of [[subobjects]] one may consider more generally closures acting on the full [[slice categories]]. This promotes the corresponding _[[modal logic]]_ to _[[modal type theory]]_.  Unlike in the posetal case, such a monad will not automatically be [[idempotent monad|idempotent]], but often one requires this explicitly.


## Definition


### For reflective subcategories
 {#DefinitionForReflectiveSubcategories}

Let $Sh_j(\mathcal{C}) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow} \mathcal{E}$ be a [[reflective subcategory]] of a [[topos]] $\mathcal{E}$.

Here we discuss explicit translations between the structure given by the [[localization|reflector]] $L$ and the corresponding closure operator $j \colon \Omega \to \Omega$ (the [[Lawvere-Tierney topology|Lawvere-Tierney operator]]) in a way that makes the relation to [[modal type theory]] and [[monads (in computer science)]] most manifest.

+-- {: .num_defn #ClosureOperatorOfReflection}
###### Definition

Given a reflector $\sharp : \mathcal{E} \stackrel{L}{\to} Sh_j(\mathcal{E}) \hookrightarrow \mathcal{E}$, define for each object $X \in \mathcal{E}$ a **closure operator**,
being a [[functor]] on the [[poset of subobjects]] of $X$

$$
  c_L : Sub(X) \to Sub(X)
  \,,
$$

by sending any [[monomorphism]] $A \hookrightarrow X$ classified by a [[characteristic function]] $\chi_A : X \to \Omega$ to the [[pullback]] $c_L(A)$ in

$$
  \array{
    c_L(A) &\to& \sharp A
    \\
    \downarrow && \downarrow
    \\
    X &\to& \sharp X
  }
  \,,
$$

where $X \to \sharp X$ is the [[unit of an adjunction|adjunction unit]].

=--

+-- {: .num_prop }
###### Proposition

This is well defined. Moreover, $c_L$
commutes with [[pullback]] ([[change of base]]).

=--

This appears as ([Johnstone, lemma A4.3.2](#Johnstone)).

+-- {: .num_defn }
###### Definition

A family of functors $Sub(X) \to Sub(X)$ for all objects $X$ that commutes with [[change of base]] is called a **universal closure operation**.

=--

+-- {: .num_prop }
###### Proposition

Given a [[left exact functor|left exact]] reflector $\sharp$ as above with induced closure operation $c_L$, the corresponding Lawvere-Tierney operator $j : \Omega \to \Omega$ is given as the composite

$$
  j : \Omega \to \sharp \Omega \stackrel{\chi_{\sharp true}}{\to} \Omega  
  \,,
$$

where 

* $\Omega \to \sharp \Omega$ is the [[unit of an adjunction|adjunction unit]];

* $\chi_{\sharp true} : \sharp \Omega \to \Omega$ is the [[characteristic function]] of the result of applying $\sharp$ to the [[subobject classifier|universal subobject]]

  $$
    (* \stackrel{\sharp true}{\hookrightarrow} \sharp \Omega)
     :=
    \sharp (* \stackrel{true}{\hookrightarrow} \Omega)
  $$

  (which is again a [[monomorphism]] since $\sharp$ preserves [[pullbacks]]).

=--

+-- {: .proof}
###### Proof

For $A \hookrightarrow X$ any [[subobject]] with [[characteristic function]] $\chi_A : X \to \Omega$, we need to show that we have a [[pullback]] [[diagram]]

$$
  \array{
    c_L(A) &\to& &\to& &\to& *
    \\
    \downarrow && && && \downarrow
    \\
    X &\stackrel{\chi_A}{\to}& \Omega
    &\stackrel{}{\to}&
    \sharp \Omega
    &\stackrel{}{\to}&
    \Omega
  }
  \,.
$$

The pullback along the rightmost morphism is by definition $# * \to \sharp \Omega$

$$
  \array{
    c_L(A) &\to& &\to& # * = * &\to& *
    \\
    \downarrow && && \downarrow && \downarrow
    \\
    X &\stackrel{\chi_A}{\to}& \Omega
    &\stackrel{}{\to}&
    \sharp \Omega
    &\stackrel{}{\to}&
    \Omega
  }
  \,.
$$

Moreover, by the [[natural transformation|naturality]] of the [[unit of an adjunction|adjunction unit]] we have a [[commuting diagram]]


$$
  \array{
    X &\to& \sharp X
    \\
    {}^{\mathllap{\chi_A}}\downarrow && \downarrow^{\mathrlap{\sharp \chi_A}}
    \\
    \Omega &\to& \sharp \Omega
  }
  \,.
$$

Using this in the remaining bottom morphism of our would-be pullback square we find that equivalently

$$
  \array{
    c_L(A) &\to& &\to& # * = * &\to& *
    \\
    \downarrow && && \downarrow && \downarrow
    \\
    X &\stackrel{}{\to}& \sharp X
    &\stackrel{\sharp \chi_A}{\to}&
    \sharp \Omega
    &\stackrel{}{\to}&
    \Omega
  }
$$

needs to be a pullback diagram. Since $\sharp$ preserves pullbacks we have that also the middle square in 

$$
  \array{
    c_L(A) &\to& \sharp A &\to& # * = * &\to& *
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    X &\stackrel{}{\to}& \sharp X
    &\stackrel{\sharp \chi_A}{\to}&
    \sharp \Omega
    &\stackrel{}{\to}&
    \Omega
  }
$$

is a pullback. But then also the left square is a pullback, by def. \ref{ClosureOperatorOfReflection}. This finally means, by the [[pasting law]], that also the total rectangle is a pullback.

=--

+-- {: .num_remark }
###### Remark

Equivalently, by the [[pasting law]], we have that $j : \Omega \to \Omega$ is the [[characteristic function]] of the $L$-closure, def. \ref{ClosureOperatorOfReflection}, of the universal subobject $* \to \Omega$, because we have a [[pasting diagram]] of [[pullback]] squares

$$
  \array{
    c_L(*) &\to& \sharp * = * &\to & * 
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \Omega &\to& \sharp \Omega &\stackrel{\chi_{\sharp true}}{\to} & \Omega
  }
  \,.
$$

In this form the statement appears in the proof of ([Johnstone, Theorem A4.3.9](#Johnstone)).

=--


## Examples

* In a [[topos]] a universal closure operator as [above](#DefinitionForReflectiveSubcategories) is also called a  _[[Lawvere-Tierney topology]]_.

* For a [[local topos]] there are the closure operators _[[flat modality]] $\dashv$ [[sharp modality]]_.

## Related concepts

* [[modal type theory]]


## References

Section A4.4 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}



[[!redirects universal closure operator]]
[[!redirects universal closure operators]]
[[!redirects universal closure operation]]
[[!redirects universal closure operations]]

