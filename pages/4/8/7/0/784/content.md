
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Segal space_ is a [[precategory object in an (∞,1)-category|pre-category object]] in [[∞Grpd]].

A genuine [[category object in an (∞,1)-category|category object]] in [[∞Grpd]] is a _[[complete Segal space]]_.  This is a way of speaking of [[(∞,1)-categories]].

## Definition

A **Segal space** $X_\bullet$
  is a [[simplicial topological space]] or [[bisimplicial set]]
  $X_\bullet : \Delta^{op} \to Top$ which satisfies the [[Segal conditions]]: 

for all $m,n \in \mathbb{N}$ the square

$$
  \array{
    X_{m+n} &\stackrel{
      p^*_{0,\cdots, m}
    }{\to}& X_m
    \\
    {}^{\mathllap{p^*_{m, \cdots, m+n}}}\downarrow 
    && \downarrow^{\mathrlap{p^*_m}}
    \\
    X_n &\stackrel{p^*_0}{\to}& X_0
  }
$$

is a [[homotopy pullback]] square.

A Segal space for which $X_0$ is a [[discrete space]] is called a _[[Segal category]]_. See there for more dicussion.

## Examples
 {#Examples}

### In $Set$
 {#InSetByNervesOfCategories}

For $\mathcal{C}$ a ([[small category|small]]) [[category]] we may regard its ordinary [[nerve]] [[simplicial set]] $N(\mathcal{C}) \in Set^{\Delta^{op}}$ as a Segal space, under the canonical inclusion $Set \hookrightarrow \infty Grpd$,

$$
  N(\mathcal{C}) \in Set^{\Delta^{op}} \hookrightarrow \infty Grpd^{\Delta^{op}}
  \,.
$$

In fact, the classical "nerve theorem" about the [[Segal conditions]] says that a simplicial set is the nerve of a category precisely if it is a Segal space.

Notice that $Equiv(N(\mathcal{C})_1) \hookrightarrow N(\mathcal{C})_1$ is precisely the [[subset]] of [[isomorphisms]] in all [[morphisms]] of $\mathcal{C}$.

Therefore under this identification, $N(\mathcal{C})$ is a [[complete Segal space]] precisely if $\mathcal{C}$ is a [[gaunt category]], hence precisely if the only isomorphisms in $\mathcal{C}$ are the [[identities]]. 

In particular if $\mathcal{C}$ is a [[(0,1)-category]], hence a [[preordered set]], then $N(\mathcal{C})$ is complete Segal precisely if $\mathcal{C}$ is in fact an [[partially ordered set]].

### Construction in $1Grpd$ from a category
 {#ConstructionFromACategory}

Let $\mathcal{C}$ be an ordinary category. We discuss how Segal spaces are associated with this. 

Let $\mathcal{K}$ be a [[groupoid]] and $p \colon \mathcal{K} \to \mathcal{C}$ a [[functor]] which is [[essentially surjective functor|essentially surjective]].

Then let $X_1 \coloneqq (p/p)\in Grpd$ be the "lax fiber product" of $p$ with itself, or rather the [[comma object]] of $p$ with itself, hence the [[comma category]], sitting in the universal square

$$
  \array{
    X_1 &\stackrel{\partial_1}{\to}& \mathcal{K}
    \\
    {}^{\mathllap{\partial_0}}\downarrow &\swArrow& \downarrow^{\mathrlap{p}}
    \\
    \mathcal{K} &\underset{p}{\to}& \mathcal{C}
  }
  \,.
$$

Next let $X_2 = (p/p/p)$ be the "3-fold comma category", hence the comma category in 

$$
  \array{
    X_2 &\stackrel{\partial_{0}}{\to}& \mathcal{K}
    \\
    {}^{\mathllap{}}\downarrow &\swArrow& \downarrow^{\mathrlap{p}}
    \\
    X_1 &\underset{\partial_1}{\to}& \mathcal{C}  
  }
$$

and so forth: $X_n \coloneqq p^{/^{n+1}}$. 

This way an [[object]] of $X_n$ is an $(n+1)$-[[tuple]] of objects $(x_0,x_1, \cdots, x_n) \in \mathcal{K}$ together with a sequence of $n$ composable morphisms $p(x_0) \to p(x_1) \to \cdots \to p(x_n)$, and a [[morphism]] is an $(n+1)$-tuple of morphisms $(f_0,f_1, \cdots, f_n) \in \mathcal{K}$ and a [[pasting]] [[commuting diagram]]

$$
  \array{
    p(x_0) &\to& p(x_1) &\to&  \cdots &\to& p(x_1) 
    \\
    {}^{\mathllap{p(f_0)}}\downarrow && \downarrow^{\mathrlap{p(f_1)}} && \cdots   && \downarrow^{\mathrlap{p(f_1)}}
    \\
    p(x'_0) &\to& p(x_1) &\to& \cdots &\to& p(x'_1) 
  }
$$

in $\mathcal{C}$. 

By direct inspection, the maps $X_n \to X^{\partial \Delta^n}$ obtained this way are [[isofibrations]], hence [[fibrations]] in the [[canonical model structure]] on [[Grpd]] and so the [[homotopy pullbacks]] that enter the [[Segal conditions]] for $X_\bullet$ are given by ordinary [[fiber products]]. These clearly satisfy the Segal conditions, hence 

$$
  X_\bullet \in Grpd^{\Delta} \hookrightarrow \infty Grpd^{\Delta^{op}}
$$ 

constructed this way is a Segal space.

Two special case of the functor $p$ are important:

* if $\mathcal{K} \simeq core(\mathcal{C})$ is the [[core]] of $\mathcal{C}$ and $p$ is the canonical core inclusion, one finds that $Equiv(X_1) \hookrightarrow X_1$ by the above construction is $Equiv(X_1) = Core(\mathcal{C})^{\Delta^1}$, the [[arrow category]] of the [[core]] of $\mathcal{C}$. This is [[equivalence of categories|equivalent]] to $\mathcal{C}$ by, for instance, the source or  restriction map. Hence for $p$ the core inclusion, the above construction gives the [[complete Segal space]] corresponding to the category $\mathcal{C}$.

* if $p \colon \pi_0(\mathcal{C}) \to \mathcal{C}$ is a choice of basepoints in each [[isomorphism class]] of $\mathcal{C}$, then $X_\bullet$ is the [[Segal category]] incarnation of the category $\mathcal{C}$.


### In $1Grpd$
 {#ExamplesInIGrpd}

We consider the situation of _[From a category](#ConstructionFromACategory)_, but now conversely, starting with a Segal space in groupoids and then extracting a category from it.

Consider a Segal space that is degreewise just a [[1-groupoid]], hence a simplicial object in the inclusion

$$
  X_\bullet \in 1Grpd^{\Delta^{op}} \hookrightarrow \infty Grpd^{\Delta^{op}}
  \,.
$$

Choosing this to be [[Reedy model structure|Reedy]] [[fibrant object|fibrant]], the map $(\partial_0,\partial_1) \colon X_1 \to X_0 \times X_0$ is an [[isofibration]]. 

We may write an object $K \in X_1$ as a horizontal morphism

$$
  \partial_1(K) \stackrel{K}{\to} \partial_2(K)
$$

and a morphism $\lambda \colon L \to K$ in $X_1$ as a vertical [[double category]] arrow:

$$
  \array{
     \partial_1(L) & \stackrel{L}{\to} & \partial_0(L)
     \\
     {}^{\mathllap{\partial_1(\lambda)}}\downarrow &\Downarrow^{\mathrlap{\lambda}}& \downarrow^{\mathrlap{\partial_0(\lambda)}}
     \\
     \partial_1(K) &\stackrel{K}{\to}& \partial_0(K)
  }
  \,.
$$

Then the fact that $(\partial_1,\partial_0)$ is an [[isofibration]] means that for every "niche"

$$
  \array{
     y_0 & & y_1
     \\
     {}^{\mathllap{f_0}}\downarrow 
     && 
    \downarrow^{\mathrlap{f_1}}
     \\
     x_0 &\stackrel{K}{\to}& x_1
  }
  \,,
$$

namely for every pair of morphisms $f_0, f_1$ in $X_0$ and lift of its codomain to an object $K \in X_1$, there is a "niche filler" 

$$
  \array{
     y_0 & \stackrel{L}{\to} & Y_1
     \\
     {}^{\mathllap{f_0}}\downarrow 
     &\Downarrow^{\mathrlap{\lambda}}& 
    \downarrow^{\mathrlap{f_1}}
     \\
     x_0 &\stackrel{K}{\to}& x_1
  }
  \,,
$$

namely a lift of the whole pair $(f_0,f_1)$ to a morphism $\lambda$ in $X_1$, and this is necessarily universal in that any other such lift uniquely factors through this one (because $X_1$ is a groupoid). 

Comparison with the definition of a [[2-category equipped with proarrows]] in the incarnation _[as a double category](2-category+equipped+with+proarrows#DefinitionAsDoubleCategory)_ shows that this is the beginning of the construction of a [[pseudo double category]] whose vertical category is $X_0$ and whose weak horizontal composition is that induced by the Segal maps. 

Assume next that $X_3 \to X^{\partial \Delta^2}$ is a [[1-monomorphism]], as are all the higher $X^n \to X^{\partial \Delta^n }$, for $n \geq 3$, hence that $X_\bullet$ is [[coskeleton|2-coskeletal]] as a simplicial object. This means that the horizontal composition in this pseudo double category has unique composites, hence that the horizontal category is an ordinary category. If then furthermore the composite $Equiv(X_1) \to X_1 \stackrel{\partial_0}{\to} X_0$ is an equivalence, hence is the Segal space is a [[complete Segal space]] this means that $X_\bullet$ arises from this horizontal category by the construction [above](#ConstructionFromACategory).


## Related notions

* [[reduced Segal space]], [[Segal category]], 

* [[semi-Segal space]]

* [[complete Segal space]], [[model structure for complete Segal spaces]]

* [[higher Segal space]]

* [[Segal type]]

## References

See generally the references at _[[complete Segal space]]_.


The "[[Segal conditions]]" are first discussed in 

* [[Graeme Segal]], _Classifying spaces and spectral sequences_, Inst. Hautes &#201;tudes Sci. Publ. Math., vol. 34, pp. 105&#8211;112 (1968),

where it is attributed to [[Alexander Grothendieck]].

The term "Segal space" is due to 

* [[Charles Rezk]], ...


The _invertible_ case of Segal spaces, hence models for [[groupoid objects in an (infinity,1)-category]] are discussed in section 3 of 

* [[Julia Bergner]], _Adding inverses to diagrams II: Invertible homotopy theories are spaces_, Homology, Homotopy and Applications, Vol. 10 (2008), No. 2, pp.175-193. ([web](http://www.intlpress.com/hha/v10/n2/a9/), [arXiv:0710.2254](http://arxiv.org/abs/0710.2254))


[[!redirects Segal spaces]]
