
> This entry is about base change of [[slice categories]]. For base change in [[enriched category theory]] see at [[change of enriching category]].

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Topos theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

For $f : X \to Y$ a [[morphism]] in a [[category]] $C$ with [[pullbacks]], there is an induced [[functor]]

$$
  f^* : C/Y \to C/X
$$

of [[over-categories]]. This is the _base change_ morphism. If $C$ is a [[topos]], then this refines to an [[essential geometric morphism]]

$$
  (f_! \dashv f^* \dashv f_*) : C/X \to C/Y
  \,.
$$

More generally, such a triple adjunction holds whenever $C$ is [[locally cartesian closed category|locally cartesian closed]], and indeed this [[locally cartesian closed category#DependentProductImpliesLocalCartesinClosure|characterises]] locally cartesian closed categories. The [[duality|dual]] concept is [[cobase change]].


## Definition

### Pullback

For $f : X \to Y$ a [[morphism]] in a [[category]] $C$ with [[pullback]]s, there is an induced [[functor]]

$$
  f^* : C/Y \to C/X
$$

of [[over-categories]].  It is on objects given by [[pullback]]/[[fiber product]] along $f$

$$
  (p : K \to Y)
  \mapsto
  \left(
  \array{
    X \times_Y K &\to & K
    \\
    {}^{\mathllap{p^*}}\downarrow && \downarrow
    \\
    X &\stackrel{f}{\to}& Y 
  }
  \right)
  \,.
$$

On morphisms, it follows from the universal property of pullback

$$
  \left\lbrace
    \array{
       K &&\stackrel{g}{\to}&& K'
       \\
       & {}_p \searrow && \swarrow_{p'}
       \\   
       && Y
    }
  \right\rbrace
  \mapsto
  \left\lbrace
    \array{
       X \times_Y K &&\stackrel{g^*}{\to}&& X \times_Y K'
       \\
       & {}_{p^*} \searrow && \swarrow_{p'^*}
       \\   
       && X
    }
  \right\rbrace
$$

by observing that this square commutes

$$
  \array{
     &&&& X \times_Y K
     \\& 
    &&
      {}^{p^*}\swarrow
      && \searrow^{g \circ p_K}
    \\
     && X &&&& K'
      \\
      &
      && {}_f\searrow
       &
       & \swarrow_{p'}
      &&
     \\
     &&&&
     Y
     &&&&
  }
  \,.
$$


### In a fibered category

The concept of base change generalises from this case to other [[fibered category|fibred categories]].


### Base change geometric morphisms 
  {#GeometricMorphism}

+-- {: .num_prop #BaseChangeIsEssentialGeometricMorphism}
###### Proposition


For $\mathbf{H}$ a [[topos]] (or [[(∞,1)-topos]], etc.) $f : X \to Y$ a [[morphism]] in $\mathbf{H}$, then base change induces an [[essential geometric morphism]] between over-toposes/[[over-(∞,1)-topos]]es

$$
  (\sum_f \dashv f^* \dashv \prod_f) : \mathbf{H}/X 
   \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
 \mathbf{H}/Y
$$ 

where $f_!$ is given by postcomposition with $f$ and $f^*$ by [[pullback]] along $f$.

=--

+-- {: .proof}
###### Proof

That we have [[adjoint functor]]s/[[adjoint (∞,1)-functor]]s $(f_! \dashv f^*)$ follows directly from the universal property of the pullback. The fact that $f^*$ has a further [[right adjoint]] is due to the fact that it preserves all small [[colimit]]s/[[(∞,1)-colimit]]s by the fact that in a topos we have [[universal colimits]] and then by the [[adjoint functor theorem]]/[[adjoint (∞,1)-functor theorem]].

=--

+-- {: .num_remark}
###### Remark

The ([[comonad|co-]])[[monads]] induced by the [[adjoint triple]] in prop. \ref{BaseChangeIsEssentialGeometricMorphism} have special names in some contexts:

* $f_\ast f^\ast$ is also called the [[function monad]] (or "[[reader monad]]", see at _[[monad (in computer science)]]_).

* $f_! f^\ast$ is also called the "[[writer comonad]]" (in computer science)

* in [[modal type theory]] $f^\ast f_\ast$ is _[[necessity]]_ while $f^\ast f_!$ is _[[possibility]]_.

=--

+-- {: .num_prop}
###### Proposition

Here $f^\ast$ is a [[cartesian closed functor]], hence base change of toposes constitutes a cartesian [[Wirthmüller context]].

=--

See at _[[cartesian closed functor]]_ for the proof.

+-- {: .num_prop}
###### Proposition

$f^*$ is a [[logical functor]]. Hence $(f^* \dashv f_*)$ is also an [[atomic geometric morphism]].

=--

This appears for instance as ([MacLaneMoerdijk, theorem IV.7.2](#MacLaneMoerdijk)).

+-- {: .proof}
###### Proof

By prop. \ref{BaseChangeIsEssentialGeometricMorphism} $f^*$ is a [[right adjoint]] and hence preserves all [[limit]]s, in particular [[finite limit]]s.

Notice that the [[subobject classifier]] of an [[over topos]] $\mathbf{H}/X$ is $(p_2 : \Omega_{\mathbf{H}} \times X \to X)$. This [[product]] is preserved by the [[pullback]] by which $f^*$ acts, hence $f^*$ preserves the subobject classifier.

To show that $f^*$ is logical it therefore remains to show that it also preserves [[exponential object]]s.  (...)

=--

+-- {: .num_defn}
###### Definition

A (necessarily essential and atomic) geometric morphism of the form $(f^* \dashv \prod_f)$ is called the **base change geometric morphism** along $f$.

The [[right adjoint]] $f_* = \prod_f$ is also called the [[dependent product]] relative to $f$.

The [[left adjoint]] $f_! = \sum_f$ is also called the [[dependent sum]] relative to $f$.

In the case $Y = *$ is the  [[terminal object]], the base change geometric morphism is also called an **[[etale geometric morphism]]**. See there for more details

=--

## Properties

+-- {: .num_prop}
###### Proposition

If $\mathcal{C}$ is a [[locally cartesian closed category]] then for every morphism $f \colon X \to Y$ in $f$ the [[inverse image]] $f^* \colon \mathcal{C}_{/Y} \to \mathcal{C}_{/X}$ of the base change is a [[cartesian closed functor]].

=--

See at _[cartesian closed functor -- Examples](cartesian%20closed%20functor#Examples)_ for a proof.


## Examples 


### Along $\mathbf{B}H \to \mathbf{B}G$
 {#AlongDeloopingsOfGroupHomomorphisms}


For $\mathbf{H}$ an [[(∞,1)-topos]] and $G$ an group object in $\mathbf{H}$ (an [[∞-group]]), then the [[slice (∞,1)-topos]] over its [[delooping]] may be identified with the [[(∞,1)-category]] of $G$-[[∞-actions]] (see there for more):


$$
  Act_G(\mathbf{H}) \simeq \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

Under this identification, then left and right base change long a morphism of the form $\mathbf{B}H \to \mathbf{B}G$ (corresponding to an [[∞-group]] homomorphism $H \to G$) corresponds to forming [[induced representations]] and [[coinduced representations]], respectively.

### Along $\ast \to \mathbf{B}G$
 {#AlongPointInclusionIntoBG}

As the special case of the [above](#AlongDeloopingsOfGroupHomomorphisms) for $H = 1$ the trivial group we obtain the following:

+-- {: .num_prop #CyclicLoopSpace}
###### Proposition

Let $\mathbf{H}$ be any  [[(∞,1)-topos]] and let $G$ be a group object in $\mathbf{H}$ (an [[∞-group]]). Then the base change along the canonical point inclusion 

$$
  i \;\colon\; \ast \to \mathbf{B}G
$$ 

into the [[delooping]] of $G$ takes the following form: 

There is a pair of [[adjoint ∞-functors]] of the form

$$
  \mathbf{H}
    \underoverset
      { \underset{i_\ast \simeq [G,-]/G}{\longrightarrow}}
      { \overset{i^\ast \simeq hofib}{\longleftarrow}}
      {\bot}
  \mathbf{H}_{/\mathbf{B}G}
  \,,
$$


where

* $hofib$ denotes the operation of taking the [[homotopy fiber]] of a map to $\mathbf{B}G$ over the canonical basepoint;

* $[G,-]$ denotes the [[internal hom]] in $\mathbf{H}$;

* $[G,-]/G$ denotes the [[homotopy quotient]] by the [[conjugation action|conjugation]] [[∞-action]] for $G$ equipped with its canonical [[∞-action]] by left multiplication and the argument
regarded as equipped with its trivial $G$-$\infty$-action 

  (for $G = S^1$ then this is the [[cyclic loop space]] construction).

Hence for

* $\hat X \to X$ a $G$-[[principal ∞-bundle]]

* $A$ a [[coefficient]] object, such as for some [[differential cohomology|differential]] [[generalized cohomology theory]]

then there is a [[natural equivalence]]


$$
  \underset{
    \text{original} \atop \text{fluxes}
  }{
  \underbrace{
    \mathbf{H}(\hat X\;,\; A)
  }
  }
    \;\;
    \underoverset
      {\underset{oxidation}{\longleftarrow}}
      {\overset{reduction}{\longrightarrow}}
      {\simeq}
    \;\;
  \underset{
     \text{doubly} \atop { \text{dimensionally reduced} \atop \text{fluxes} }
  }{
  \underbrace{
    \mathbf{H}(X \;,\; [G,A]/G)
  }
  }
$$

given by

$$
  \left(
     \hat X \longrightarrow A
  \right)
  \;\;\;
    \leftrightarrow
  \;\;\;
  \left(
    \array{
       X && \longrightarrow && [G,A]/G
       \\
       & \searrow && \swarrow
       \\
       && \mathbf{B}G
    }
  \right)
$$

=--

+-- {: .proof #DimensionalReductionAbstractly}
###### Proof

The statement that $i^\ast \simeq hofib$ follows immediately by the definitions. What we need to see is that the [[dependent product]] along $i$ is given as claimed.

To that end, first observe that the [[conjugation action]] on $[G,X]$ is the [[internal hom]] in
the [[(∞,1)-category]] of $G$-[[∞-actions]] $Act_G(\mathbf{H})$.
Under the [[equivalence of (∞,1)-categories]]

$$
  Act_G(\mathbf{H}) \simeq \mathbf{H}_{/\mathbf{B}G}
$$

(from [NSS 12](https://ncatlab.org/schreiber/show/Principal+%E2%88%9E-bundles+--+theory%2C+presentations+and+applications)) then $G$ with its canonical [[∞-action]] is $(\ast \to \mathbf{B}G)$
and $X$ with the trivial action is $(X \times \mathbf{B}G \to \mathbf{B}G)$.

Hence

$$
  [G,X]/G
    \simeq
  [\ast, X \times \mathbf{B}G]_{\mathbf{B}G}
  \;\;\;\;\;
  \in
   \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

So far this is the very definition of what $[G,X]/G \in \mathbf{H}_{/\mathbf{B}G}$ is to mean in the first place.

But now since the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ is itself [[cartesian closed (infinity,1)-category|cartesian closed]], via

$$
  E \times_{\mathbf{B}G}(-)
  \;\;\;
   \dashv
  \;\;\;
  [E,-]_{\mathbf{B}G}
$$

it is immediate that
there is the following sequence of [[natural equivalences]]

$$
  \begin{aligned}
   \mathbf{H}_{/\mathbf{B}G}(Y, [G,X]/G)
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(Y, [\ast, X \times \mathbf{B}G]_{\mathbf{B}G})
   \\
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(
     Y \times_{\mathbf{B}G} \ast,
     \underset{p^\ast X}{\underbrace{X \times \mathbf{B}G }}
  )
  \\
  & \simeq
  \mathbf{H}(
     \underset{hofib(Y)}{\underbrace{p_!(Y \times_{\mathbf{B}G} \ast)}},
     X
  )
  \\
  & \simeq
  \mathbf{H}(hofib(Y),X)
  \end{aligned}
$$

Here $p \colon \mathbf{B}G \to \ast$ denotes the terminal morphism and $p_! \dashv p^\ast$ denotes the [[base change]] along it.


=--

See also at _[[double dimensional reduction]]_ for more on this.

### Along $V/G \to \mathbf{B}G$

More generally:

+-- {: .num_prop #RightBaseChangeAlongUniversalFiberBundleProjection}
###### Proposition

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and $G \in Grp(\mathbf{H})$ an [[∞-group]].

Let moreover $V \in \mathbf{H}$ be an object equipped with a $G$-[[∞-action]] $\rho$, equivalently (by the discussion there) a [[homotopy fiber sequence]] of the form

$$
  \array{
    V
    \\
    \downarrow
    \\
    V/G & \overset{p_\rho}{\longrightarrow}& \mathbf{B}G
  }
$$

Then 

1. pullback along $p_\rho$ is the operation that assigns to a morphism $c \colon X \to \mathbf{B}G$ the $V$-[[fiber ∞-bundle]] which is [[associated ∞-bundle|associated]] via $\rho$ to the $G$-[[principal ∞-bundle]] $P_c$ classified by $c$:

   $$
     (p_\rho)^\ast \;\colon\; c \mapsto P_c \times_G V
   $$

1. the right base change along $p_\rho$ is given on objects of the form $X \times (V/G)$ by

   $$
     (p_\rho)_\ast \;\colon\; X \times (V/G) \;\mapsto\;  [V,X]/G 
   $$


=--

+-- {: .proof}
###### Proof


The first statement is [NSS 12, prop. 4.6](https://ncatlab.org/schreiber/show/Principal+%E2%88%9E-bundles+--+theory%2C+presentations+and+applications).


The second statement follows as in the proof of prop. \ref{CyclicLoopSpace}: Let 

$$
  \left(
    \array{
      Y
      \\
      \downarrow^{\mathrlap{c}}
      \\
      \mathbf{B}G
    }
  \right)
  \;\in\;
  \mathbf{H}_{/\mathbf{B}G}
$$

be any object, then there is the following sequence of [[natural equivalences]]

$$
  \begin{aligned}
   \mathbf{H}_{/\mathbf{B}G}(Y, [V,X]/G)
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(Y, [V/G, X \times \mathbf{B}G]_{\mathbf{B}G})
   \\
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(
     Y \times_{\mathbf{B}G} (V/G),
     \underset{p^\ast X}{\underbrace{X \times \mathbf{B}G }}
  )
  \\
  & \simeq
  \mathbf{H}_{/\mathbf{B}G}
  (
    (p_\rho)_!( P_c \times_G (V/G) ),
    p^\ast X
  )
  \\
  & \simeq
     \mathbf{H}_{/(V/G)}
     (
       P_c \times_G V, (p_\rho)^\ast p^\ast X
     )
  \\
  & 
  \simeq
    \mathbf{H}_{/(V/G)}(P_c \times_G V, X \times (V/G))
  \end{aligned}
$$

where again

$$
  p \colon \mathbf{B}G \to \ast
  \,.
$$

=--

+-- {: .num_example #SymmetricPowers}
###### Example
**(symmetric powers)**

Let 

$$
  G = \Sigma(n) \in Grp(Set) \hookrightarrow Grp(\infty Grpd) \overset{LConst}{\longrightarrow} \mathbf{H}
$$ 

be the [[symmetric group]] on $n$ elements, and 

$$
  V = \{1, \cdots, n\} \in Set \hookrightarrow \infty Grpd \overset{LConst}{\longrightarrow} \mathbf{H}
$$

the $n$-element [[set]] ([[h-set]]) equipped with the canonical $\Sigma(n)$-[[action]]. Then prop. \ref{RightBaseChangeAlongUniversalFiberBundleProjection} says that right base change of any $p_\rho^\ast p^\ast X$ along

$$
  \{1, \cdots, n\}/\Sigma(n)
    \longrightarrow
  \mathbf{B}\Sigma(n)
$$

is equivalently the $n$th [[symmetric power]] of $X$

$$
 [\{1,\cdots, n\},X]/\Sigma(n)
  \simeq 
  (X^n)/\Sigma(n)
  \,.
$$

=--


## Related concepts

* **base change**

  * [[dependent sum]], [[dependent product]]

  * [[dependent sum type]], [[dependent product type]]

  * [[necessity]], [[possibility]], [[reader monad]], [[writer comonad]]

* [[proper base change theorem]]

* Base change geometric morphisms may be interpreted in terms of [[fiber integration]]. See [[integral transforms on sheaves]] for more on this.

* [[change of enriching category]]

[[!include notions of pullback -- contents]]


## References

A general discussion that applies (also) to [[enriched categories]] and [[internal categories]] is in 

* [[Dominic Verity]], _Enriched categories, internal categories and change of base_ Ph.D. thesis, Cambridge University (1992), reprinted as Reprints in Theory and Applications of Categories, No. 20 (2011) pp 1-266 ([TAC](http://www.tac.mta.ca/tac/reprints/articles/20/tr20abs.html))

Discussion in the context of [[topos theory]] is around example A.4.1.2 of

* {#Johnstone} [[Peter Johnstone]],  _[[Sketches of an Elephant]]_ 
 

and around theorem IV.7.2 in 

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
  

Discussion in the context of [[(infinity,1)-topos theory]] is in section 6.3.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

See also 

* A. Carboni, G. Kelly, R. Wood, _A 2-categorical approach to change of base and geometric morphisms I_ ([numdam](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1991__32_1/CTGDC_1991__32_1_47_0/CTGDC_1991__32_1_47_0.pdf))

[[!redirects change of base]]
[[!redirects changes of base]]
[[!redirects base changes]]

[[!redirects base change geometric morphism]]
[[!redirects base change geometric morphisms]]