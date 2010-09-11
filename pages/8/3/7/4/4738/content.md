
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

An _$\infty$-anafunctor_ is a model for a [[morphism]] in an [[(∞,1)-category]] $\mathbf{H}$ of structured [[(n,r)-categories]] notably of [[∞-stack]]s with values in [[(n,r)-categories]] in terms of [[span]]s of ordinary morphisms (of [[presheaves]], notably). It generalizes the notion of 1-[[anafunctor]].

The [[category with weak equivalences]] that models the $(n,r)$-categories in questions should be refined to the structure of a [[category of fibrant objects]] for $\infty$-anafunctors to be a good model

In such a model $[C^{op},(n,r)Cat]$ for $\mathbf{H}$, a [[morphism]] in $\mathbf{H}$ between $X$ to $Y$ is presented by a [[span]]

$$
  \array{
    \hat X &\to& X
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

of presheaves. This is an **$\infty$-anafunctor**, generalizing the notion of [[anafunctor]].

The point is that this is a special simple form of the more general and more complicated constructions in [[simplicial localization]], which require zig-zags of morphisms of greater length than a single span.

## Definition

An _$\infty$-anafunctor_ $g : C \to D$ is a span

$$
  \array{
     \hat C &\stackrel{g}{\to}& D
     \\
     \downarrow
     \\
     C
  }
$$

of whose left leg is an _acyclic fibration_ with 


Given two $\infty$-anafunctors $C \stackrel{g}{\to} D$ and $D \stackrel{h}{\to} E$ their _composite_ $\infty$-anafunctor is given by the span

$$
  \array{
     g^* \hat D &\to& D &\stackrel{h}{\to}& E
     \\
     \downarrow && \downarrow 
     \\
     \hat C &\stackrel{g}{\to}& D
     \\
     \downarrow
     \\
     C
  }
  \,,
$$

where the top left square is a pullback square. Notice that acyclic fibrations are preserved under pullback and closed under composition, so that the total vertical $\omega$-functor on the left is indeed again an acyclic fibration and hence the total span here indeed again an $\infty$-anafunctor.

While this definition of composition is in itself well defined, it is not quite associative: the two ways of composing three spans representing $\infty$-anafunctors tis way in general produces two spans out of different -- albeit isomorphic -- [[hypercover]]s.

Of course the precise choice of hypercover $\hat C$ of $C$ is not an essential datum: two $\infty$-anafuntors should be regarded as equivalent if they become equal after pulled back to a joint hypercover. This is formalized in the following definition:

(...)


## Examples

### Ambient contexts

Any of the algebraic models for higher categories provide categories of fibrant objects, such as the [[folk model structure]]s. 

But also thopse [[simplicial sheaves]] that are [[stalk]]wise [[Kan complex]]es works, and notably  the [[full subcategories]] on fibrant objects in one of the [[model structure on simplicial presheaves]] and more generally of [[model structures on homotopical presheaves]] model arbitrary $\infty$-stacks with values in [[(n,r)-categories]].

### Cocycles for principal $\infty$-bundles

For $G \in [C^{op}, sSet]$ a model in [[simplicial presheaves]] for an [[∞-group]] in $\mathbf{H}$ and $\mathbf{B}G \in [C^{op}, sSet]$ its fibrant [[delooping]] object, an $\infty$-anafunctor

$$
  \array{
    \hat X &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow
    \\
    X
  }
$$

is a [[cocycle]] for a $G$-[[principal ∞-bundle]]. Here $\hat X \to X$ is essentially the [[hypercover]] on which the cocycle is defined.

More precisely, in order for this to be a useful cocycle presentation we either use the structure of a [[category of fibrant objects]] given by [[stalk]]-wise fibrant [[simplicial presheaves]] as in ([Brown](#Brown)), or if we use the full subcategory on fibrant objects of a [[local model structure on simplicial presheaves]] then we should take the site $C$ to contain only "elementary test objects" so that $\mathbf{B}G$ has a chance of being fibrant. This issue of big versus small sites and how this shifts the amount of fibrant and cofibrant objects around is discussed in some detail at [[∞-Lie groupoid]] in the context of sites of smooth test spaces.

An introductory exposition to how such spans are [[Cech cohomology]] cocycles see for instance [[∞-Chern-Weil-theory introduction]].

The [[principal ∞-bundle]] classified by such an $\infty$-anafuntor is the (ordinary!) [[pullback]]

$$
  \array{
    P &\to& \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    \hat X &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow
    \\
    X
  }
  \,,
$$


where $\mathbf{E}G$ is the [[universal principal ∞-bundle]], itself defined by the pullback

$$
  \array{
    \mathbf{E}G &\to& * 
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G^I &\to& \mathbf{B}G
    \\
    \downarrow
    \\
    \mathbf{B}G
  }
  \,.
$$

## Properties

### Relation to $\infty$-groupoid bibundles

Ordinary [[anafunctor]]s of [[Lie groupoid]]s can equivalently be modeled by [[groupoid principal bundle]]s that are [[bibundles]].

The generalization of this statement to $\infty$-anafunctors is given in ([BlohmannZhu](BlohmannZhu)).

## References

For $(\infty,0)$-anafunctors modeling morphisms in a [[hypercomplete]] [[(∞,1)-topos]] this is in 

* [[Kenneth Brown]], _[[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]_ .
{#Brown}

A result relating $(\infty,0)$-anafunctors to [[∞-groupoid]]-[[bibundle]]s has been announced by

* [[Christian Blohmann]], [[Chenchang Zhu]], ([blog](http://golem.ph.utexas.edu/category/2010/08/minicourse_on_nonabelian_diffe.html#c034648))
{#BlohmannZhu}

[[!redirects ∞-anafunctor]]