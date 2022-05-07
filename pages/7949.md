[[!redirects infinity-image]]

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

whose left class consists of the [[n-connected object in an (∞,1)-topos|(-1)-connected]] morphisms, the [[effective epimorphism in an (∞,1)-category|(∞,1)-effective epimorphisms]], while the right class consists of the [[n-truncated object in an (∞,1)-category|(-1)-truncated morphisms]] morphisms, hence the [[monomorphism in an (∞,1)-category|(∞,1)-monomorphisms]].

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
  X \times_Y X \stackrel{\longrightarrow}{\longrightarrow} X \stackrel{}{\longrightarrow} im(f)
$$

is a [[colimit|colimiting]] [[cocone]] under the [[parallel morphism]] [[diagram]].

In an [[(∞,1)-topos]] the 1-image is the [[(∞,1)-colimit]] not just of these two morphisms, but of the full "$\infty$-kernel", namely of the full [[Cech nerve]] [[simplicial object]]

$$
  \cdots
   \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}
  X \times_Y X \times_Y X
   \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}} 
  X \times_Y X \stackrel{\longrightarrow}{\longrightarrow} X \stackrel{}{\longrightarrow} im(f)
  \,.
$$

(Here all degeneracy maps are notionally suppressed.)

To see that this gives the same notion of image as given by the epi-mono factorization as discussed [above](#ViaEpiMonoFactorization), let $f \colon X \stackrel{f}{\longrightarrow} im(f) \hookrightarrow Y$ be such a factorization. Then using (by the discussion at _[truncated morphism -- Recursive characterization](n-truncated+object+of+an+%28infinity%2C1%29-category#RecursiveDefinition)_) that the [[(∞,1)-pullback]] of a [[monomorphism in an (∞,1)-category|monomorphism]] is its domain, we find a [[pasting diagram]] of [[(∞,1)-pullback]] squares of the form

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

which shows, by the [[pasting law]], that $X \times_{Y} X \simeq X \times_{im(f)} X$ and hence that the [[Cech nerve]] of $X \stackrel{f}{\to} Y$ is equivalently that of the effective epimorphism $X \stackrel{f}{\to} im(f)$. Now, by one of the [[Giraud-Rezk-Lurie axioms]] satisfied by [[(∞,1)-toposes]], the [[(∞,1)-colimit]] over the [[Cech nerve]] of an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] is that morphism itself. Therefore the 1-image defined this way coincides with the one defined by the epi/mono factorization.

### Tower of $n$-images

More generally for $f \colon X \to Y$ a morphism we have a [[tower]] of $n$-images

$$
  X \simeq im_\infty(f) \to \cdots \to im_2(f) \to im_1(f) \to im_0(f) \simeq Y
$$

factoring $f$, such that for each $n \in \mathbb{N}$ the factorization $X \to im_{n+2}(f) \to Y$ is the [[(n-connected, n-truncated) factorization system]] of $f$.

This is the relative [[Postnikov system]] of $f$.

## Properties




### Syntax in homotopy type theory
 {#SyntaxInHomotopyTypeTheory}

Let the ambient [[(∞,1)-category]] be an [[(∞,1)-topos]] $\mathbf{H}$. Then its [[internal language]] is [[homotopy type theory]].
We discuss the [[syntax]] of 1-images in this theory.

+-- {: .num_prop #SyntaxOfInfinityImage}
###### Proposition
If 
$$ a\colon A \;\vdash \; f(a) \colon B $$
is a [[term]] whose [[categorical semantics]] is a [[morphism]] $A \xrightarrow{f} B$ in $\mathbf{H}$, then the 1-image of that morphism, when regarded as an object of $\mathbf{H}/B$, is the categorical semantics of the [[dependent type]]
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

Finally, the interpretation of the [[bracket type]] of this is precisely the [[n-truncated object in an (infinity,1)-category|(-1)-truncation]] of this morphism, which by the discussion there is its 1-image $im_1(\tilde A \to B)$, regarded as a dependent type over $B$.  Thus, it is precisely the the 1-image of $f$.
=--

By additionally forgetting the remaining map to $B$, we obtain:

+-- {: .num_cor #NonDependentSyntax}
###### Corollary
In the above situation, the 1-image of $f$, regarded as an object of $\mathbf{H}$ itself, is the semantics of the non-dependent type
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


### Compatibility with limits


+-- {: .num_prop #nImagePreservesProducts}
###### Proposition

In an [[(∞,1)-topos]] $\mathbf{H}$, the $n$-image of a product is the product of $n$-images:

$$
  im_n\left(X_1 \times X_2 \stackrel{(f,g)}{\longrightarrow}) X_2 \times Y_2\right)
  \simeq
  \left(
     im_n(f) \times im_n(g)
     \longrightarrow
     X_2 \times Y_2
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The morphism  $(f,g)$ is the product of $(f,id)$ with $(g,id)$ in the [[slice (∞,1)-topos]] over $X_2 \times Y_2$, namely there is a [[homotopy fiber product]] in $\mathbf{H}$ of the form

$$
  \array{
     && X_1 \times Y_1
     \\
     & {}^{\mathllap{(id,g)}}\swarrow && \searrow^{\mathrlap{(f,id)}}
     \\
     X_1 \times Y_2 && \swArrow_{\simeq} && X_2 \times Y_1
     \\
     & {}_{\mathllap{(f,id)}}\searrow && \swarrow_{\mathrlap{(id,g)}}
     \\
     && X_2 \times Y_2
  }
$$

But by [this proposition](n-truncated+object+of+an+infinity-category#nTruncationInToposPreservesFiniteProducts), $n$-truncation in the slice $\infty$-topos preserves products, so that

$$
  \begin{aligned}
     im_n(f,g)
     & = 
     \tau_n (f,g)
     \\
     & \simeq \tau_n ((f,id)\times_{X_2 \times Y_1} (id,g))
     \\
     &\simeq (\tau_n(f,id)) \times_{X_2 \times Y_2} (\tau_n(id,g))
     \\
     & \simeq (im_n f, id)\times_{X_2 \times Y_2} (id, im_n g)
     \\
     & \simeq (im_n f, im_n g)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The $n$-image of the [[looping]] of a morphism $f \colon X \to Y$ of [[pointed objects]] is the looping of its $(n+1)$-image

$$
  im_n (\Omega(f))
  \simeq
  \Omega(im_{n+1}(f))
  \,.
$$

i.e. we have the following diagram, where the columns are [[homotopy fiber sequences]]

$$
  \array{  
    \Omega f \colon 
     & \Omega X &\longrightarrow& im_n(\Omega f) 
     &\longrightarrow& \Omega Y
    \\
    & \downarrow && \downarrow && \downarrow
    \\
    id_\ast \colon & \ast &\longrightarrow & im_{n+1}(id_\ast) \simeq \ast &\longrightarrow& \ast
    \\
    & \downarrow && \downarrow && \downarrow
    \\
    f\colon & X &\stackrel{}{\longrightarrow}& im_{n+1}(f) &\stackrel{}{\longrightarrow}& Y
  }
$$

=--

## Examples

### Automorphisms

Let $V \in \mathbf{H}$ be a $\kappa$-[[compact object in an (∞,1)-category|small object]], and let

$$
  * \stackrel{\vdash V}{\to} Obj_\kappa
$$

the corresponding morphism to the [[object classifier]]. Then the 1-image of this is $\mathbf{B}\mathbf{Aut}(V)$, the [[delooping]] of the internal [[automorphism ∞-group]] of $V$.

### Of functors between groupoids
 {#NImagesOf1FunctorsBetweenGroupoids}

The simplest nontivial case of higher images after the ordinary case of images of functions of sets is images of [[functors]] between [[groupoids]] hence betwee [[1-truncated]] objects $X, Y \in Grpd \hookrightarrow$ [[∞Grpd]].

+-- {: .num_prop #FactorizationOf1FunctorsBetween1Groupoids}
###### Proposition

For $f \colon X \to Y$ a [[functor]] between [[groupoids]], its image factorization is

$$
  f \colon X \to im_2(f) \to im_1(f) \to Y 
  \,,
$$

where (up to [[equivalence of groupoids]])

* $im_1(f) \to Y$ is the [[full subcategory|full subgroupoid]] of $Y$ on those objects $y$ such that there is an object $x \in X$ with $f(x) \simeq y$;

* $im_2(f)$ is the groupoid whose objecs are those of $X$ and whose morphisms are equivalence classes of morphisms in $X$ where $\alpha,\beta \in Mor(X)$ are equivalent if they have the same domain and codomain in $X$ and if $f(\alpha) = f(\beta)$

  * $im_2(f)\to im_1(f)$ is the identity on objects and the canonical inclusion on sets of morphisms;

  * $X \to im_2(f)$ is the identity on objects and the defining [[quotient]] map on sets of morphisms.

=--

+-- {: .proof}
###### Proof

Evidently $im_1(f) \to Y$ is a [[fibration]] ([[isofibration]]) and so the [[homotopy fiber]] over every point is given by the 1-categorical [[pullback]]

$$
  \array{
    F_y &\to& im_1(y)
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{y}{\to}& Y
  }
  \,.
$$

If there is no $x \in X$ such that $f(x) \simeq y$ then fiber $F_y$ is [[empty set]]. If there is such $x$ then the fiber is the groupoid with that one object and all morphisms in $X$ on that object which are mapped to the identity morphism, which by construction is only the identity morphism itself, hence the fiber is the point. Hence indeed the homotopy fibers of $im_1(f) \to Y$ are [[(-1)-truncated]] objects and the map from homotopy fiber of $f$ to those of $im_1(f)$ is their (-1)-truncation.

Next, the [[homotopy fibers]] of $im_2(f) \to Y$ over a point $y \in Y$ are the groupoids whose objects are pairs $(x, (f(x) \to y))$ and whose morphisms are pairs

$$
  \left(
    \array{
      x_1 &\stackrel{[\alpha]}{\to}& x_2
      \\
      f(x_1) &\stackrel{f(\alpha)}{\to}& f(x_2)
      \\
      \downarrow && \downarrow 
      \\
      y &=& y
    }
  \right)
  \,.
$$

Notice first that the above is [[0-truncated]]: an automorphism of $(x,(f(x) \to y))$ is of the form $x \stackrel{[\alpha]}{to} x$ such that $f(\alpha) = id_{f(x)}$ and so there is precisely one such, namely the equivalence class of $id_x$. 

Notice second that the homotopy fibers of $f$ itself have the same form, only that $\alpha \colon x_1 \to x_2$ appears itself, not as its equivalence class. Also if two objects in the homotopy fiber of $f$ are connected by a morphism, then by construction so they are in the homotopy fiber of $im_2(f) \to Y$ and hence the latter is indeed the [[0-truncation]] of the former.

=--

+-- {: .num_remark }
###### Remark

The factroization $f \colon X \to im_2(f) \to im_1(f) \to Y$ of prop. \ref{FactorizationOf1FunctorsBetween1Groupoids} exhibits a _[[ternary factorization system]]_ in [[Grpd]].

=--

+-- {: .num_remark }
###### Remark

This situation can also be considered from the perspective of the formalization of [[stuff, structure, property]]. See there at _[A factorization system](stuff%2C+structure%2C+property#AFactorizationSystem)_.

=--


## Related concepts

* [[image]], [[coimage]]

* [[homotopy image]]

* [[Postnikov system]]

* [[k-ary factorization system]]

## References

Discussion of $n$-image factorization in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], section 7.6 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

A construction of $n$-image factorizations in [[homotopy type theory]] using only [[homotopy pushouts]] and specifically [[join of topological spaces|joins]] (instead of more general [[higher inductive types]]) is described in 

* {#Rijke17} [[Egbert Rijke]], _The join construction_ ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))


[[!redirects ∞-image]]
[[!redirects ∞-images]]
[[!redirects infinity-images]]


[[!redirects n-image]]
[[!redirects n-images]]

[[!redirects n-image]]
[[!redirects n-images]]


[[!redirects 0-image]]
[[!redirects 0-images]]
[[!redirects 1-image]]
[[!redirects 1-images]]
[[!redirects 2-image]]
[[!redirects 2-images]]
[[!redirects 3-image]]
[[!redirects 3-images]]