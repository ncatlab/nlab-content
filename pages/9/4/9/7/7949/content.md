
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

The generalization of the notion of _[[image]]_ from [[category theory]] to [[(∞,1)-category theory]].

## Definition

### By epi/mono factorization in an $(\infty,1)$-topos
 {#ViaEpiMonoFactorization}

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Then by the discussion at _[[(n-connected, n-truncated) factorization system]]_ there is a [[orthogonal factorization system in an (∞,1)-category|orthogonal factorization system]] 

$$
  (Epi(\mathbf{H}), Mono(\mathbf{H})) \subset Mor(\mathbf{H}) \times Mor(\mathbf{H})
$$

whose left class consists of the [[n-connected object in an (∞,1)-topos|(-1)-connected]] morphisms , the [[effective epimorphism in an (∞,1)-category|(∞,1)-effective epimorphisms]], while the right class consists of the [[n-truncated object in an (∞,1)-category|(-1)-truncated morphisms]] morphisms, hence the [[monomorphism in an (∞,1)-category|(∞,1)-monomorphisms]].

So given a morphism $f : X \to Y$ in $\mathbf{H}$ with epi-mono factorization

$$
  f : X \to im_1(f) \hookrightarrow Y
  \,,
$$

we may call $im_1(f) \hookrightarrow Y$ the **image** of $f$.

### As the ∞-colimit of the kernel ∞-groupoid
 {#ViaColimitOfCechNerve}

In a sufficiently well-behaved 1-[[category]], the [[coimage|(co)image]] of a morphism $f \colon X \to Y$ may be defined as the [[coequalizer]] of its [[kernel pair]], hence by the fact that 

$$
  X \times_Y X \stackrel{\to}{\to} X \stackrel{}{\to} im(f)
$$

is a [[colimit|colimiting]] [[cocone]] under the [[parallel morphism]] [[diagram]].

In an [[(∞,1)-topos]] the $\infty$-image is the [[(∞,1)-colimit]] not just of these two morphisms, but of the full "$\infty$-kernel", namely of the full [[Cech nerve]] [[simplicial object]]

$$
  \cdots
   \stackrel{\to}{\stackrel{\to}{\stackrel{\to}{\to}}}
  X \times_Y X \times_Y X
   \stackrel{\to}{\stackrel{\to}{\to}} 
  X \times_Y X \stackrel{\to}{\to} X \stackrel{}{\to} im(f)
  \,.
$$

(Here all degeneracy maps are notionally suppressed.)

To see that this gives the same notion of image as given by the epi-mono factorization as discussed [above](#ViaEpiMonoFactorization), let $f \colon X \stackrel{f}{\to} im(f) \hookrightarrow Y$ be such a factorization. Then using (by the discussion at _[truncated morphism -- Recursive characterization](n-truncated+object+of+an+%28infinity%2C1%29-category#RecursiveDefinition)_) that the [[(∞,1)-pullback]] of a [[monomorphism in an (∞,1)-category|monomorphism]] is its domain, we find a [[pasting diagram]] of [[(∞,1)-pullback]] squares of the form

$$
  \array{ 
    X \times_{im(f)} X &\to & X &\stackrel{\simeq}{\to} & X
    \\
    \downarrow && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{f}}
    \\
    X &\stackrel{f}{\to}& im(f) &\stackrel{\simeq}{\to}& im(f)
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}} && \downarrow
    \\
    X &\stackrel{f}{\to}& im(f) &\hookrightarrow& Y
  }
  \,,
$$

which shows, by the [[pasting law]], that $X \times_{Y} X \simeq X \times_{im(f)} X$ and hence that the [[Cech nerve]] of $X \stackrel{f}{\to} Y$ is equivalently that of the effective epimorphism $X \stackrel{f}{\to} im(f)$. Now, by one of the [[Giraud-Rezk-Lurie axioms]] satisfied by [[(∞,1)-toposes]], the [[(∞,1)-colimit]] over the [[Cech nerve]] of an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] is that morphism itself. Therefore the $\infty$-image defined this way coincides with the one defined by the epi/mono factorization.

### Tower of $n$-images

More generally for $f \colon X \to Y$ a morphism we have a [[tower]] of $n$-images

$$
  X \simeq im_\infty(f) \to \cdots \to im_2(f) \to im_1(f) \to im_0(f) \simeq Y
$$

factoring $f$, such that for each $n \in \mathbb{N}$ the factorization $X \to im_{n+2}(f) \to Y$ is the [[(n-connected, n-truncated) factorization]] of $f$.

This is the relative [[Postnikov system]] of $f$.

## Properties

### Syntax in homotopy type theory
 {#SyntaxInHomotopyTypeTheory}

Let the ambient [[(∞,1)-category]] be an [[(∞,1)-topos]] $\mathbf{H}$. Then its [[internal language]] is [[homotopy type theory]].
We discuss the [[syntax]] of $\infty$-images in this theory.

+-- {: .num_prop #SyntaxOfInfinityImage}
###### Proposition
If 
$$ a\colon A \;\vdash \; f(a) \colon B $$
is a [[term]] whose [[categorical semantics]] is a [[morphism]] $A \xrightarrow{f} B$ in $\mathbf{H}$, then the $\infty$-image of that morphism, when regarded as an object of $\mathbf{H}/B$, is the categorical semantics of the [[dependent type]]
$$
  (b:B) \; \vdash \; 
  \Big(\Big[
    \sum_{a \colon A} (b = f(a))
  \Big]
  : Type\Big).
$$
=--

Here $=$ denotes the [[identity type]] or "path type", $\sum$ denotes the [[dependent sum type]], and $[-]$ denotes the [[bracket type]] (which is constructible in homotopy type theory either as a [[higher inductive type]] or using the [[univalence axiom]] and a resizing rule to obtain a [[subobject classifier]]).


+-- {: .proof}
###### Proof

Let $\mathbf{M}$ be a suitable [[model category]] [[presentable (∞,1)-category|presenting]] $\mathbf{H}$.  Then by the rules for [[categorical semantics]] of [[identity types]] and [[substitution]], the interpretation of
$$ (b:B),\, (a:A) \;\vdash\; ((b = f(a)) : Type)$$
in $\mathbf{M}$ a is the following [[pullback]] $\tilde A$ (see _[[homotopy pullback]]_ for more details):

$$
  \array{
    \tilde A &\to& B^{I}
    \\
    \downarrow && \downarrow
    \\
    A \times B &\stackrel{(f,id_B)}{\to}& B \times B
  }.
$$

Here all objects now denote [[fibrant object]] representatives of the given objects in $\mathbf{H}$, and the right-hand morphism is the [[fibration]] out of a [[path space object]] for $B$. By the [[factorization lemma]] the composite $\tilde A \to A \times B \to B$ here is a [[fibration]] [[resolution]] of the original $A \stackrel{f}{\to} B$ and $\tilde A \to A \times B$ is a fibration resolution of $A \stackrel{(id_A,f)}{\to} A \times B$. Regarded in the [[slice category]] $\mathbf{M}/(A \times B)$, this now interprets the syntax $(b = f(a))$ as an $(A \times B)$-[[dependent type]].

Now the interpretation of the sum $\sum_{a:A}$ is simply that we forget the map to $A$ (or equivalently compose with the projection $A\times B\to B$), regarding $\tilde A$ as an object of $\mathbf{M}/B$.  Of course, this is just a fibration resolution of $f$ itself.

Finally, the interpretation of the [[bracket type]] of this is precisely the [[n-truncated object in an (infinity,1)-category|(-1)-truncation]] of this morphism, which by the discussion there is its $\infty$-image $im_\infty(\tilde A \to B)$, regarded as a dependent type over $B$.  Thus, it is precisely the the $\infty$-image of $f$.
=--

By additionally forgetting the remaining map to $B$, we obtain:

+-- {: .num_cor #NonDependentSyntax}
###### Corollary
In the above situation, the $\infty$-image of $f$, regarded as an object of $\mathbf{H}$ itself, is the semantics of the non-dependent type
$$
  \vdash \; 
  \Big(\Big(
    \sum_{b:B}\Big[\sum_{a:A} (b = f(a))\Big]
  \Big)
  : Type\Big).
$$
=--


+-- {: .num_remark }
###### Remark
The bracket type of a [[dependent sum]] is the [[propositions as some types]] version of the [[existential quantifier]], so we can write the dependent type in Prop. \ref{SyntaxOfInfinityImage} as

$$
  (b:B) \; \vdash \; 
  \left(\exists a:A . (b = f(a))
  \;:\; hProp\right).
$$

The dependent sum *of* an [[h-proposition]] is then the propositions-as-some-types version of the [[comprehension rule]], $\{b \in B | \phi(b)\}$, so the non-dependent type in Cor. \ref{NonDependentSyntax} may be written as

$$
  \left\{
    b \in B \,|\, \exists a \in A . (b = f(a))
  \right\}
$$

which is manifestly the naive definition of [[image]].
=--


## Examples

### Automorphisms

Let $V \in \mathbf{H}$ be a $\kappa$-[[compact object in an (∞,1)-category|small object]], and let

$$
  * \stackrel{\vdash V}{\to} Obj_\kappa
$$

the corresponding morphism to the [[object classifier]]. Then the $\infty$-image of this is $\mathbf{B}\mathbf{Aut}(V)$, the [[delooping]] of the internal [[automorphism ∞-group]] of $V$.

## Related concepts

* [[homotopy image]]

[[!redirects ∞-image]]
[[!redirects ∞-images]]
[[!redirects infinity-images]]


[[!redirects n-image]]
[[!redirects n-images]]
