
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

### In $1Grpd$
 {#ExamplesInIGrpd}

Consider a Segal space that is degreewise just a [[1-groupoid]], hence a simplcial object in the inclusion

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



## Related notions

* [[reduced Segal space]], [[Segal category]], 

* [[semi-Segal space]]

* [[complete Segal space]], [[model structure for complete Segal spaces]]


## References

See generally the references at _[[complete Segal space]]_.


The "[[Segal conditions]]" are first discussed in 

* [[Graeme Segal]], _Classifying spaces and spectral sequences_, Inst.
Hautes &#201;tudes Sci. Publ. Math., vol. 34, pp. 105&#8211;112 (1968),

where it is attributed to [[Alexander Grothendieck]].

The term "Segal space" is due to 

* [[Charles Rezk]], ...


The _invertible_ case of Segal spaces, hence models for [[groupoid objects in an (infinity,1)-category]] are discussed in section 3 of 

* [[Julia Bergner]], _Adding inverses to diagrams II: Invertible homotopy theories are spaces_, Homology, Homotopy and Applications, Vol. 10 (2008), No. 2, pp.175-193. ([web](http://www.intlpress.com/hha/v10/n2/a9/), [arXiv:0710.2254](http://arxiv.org/abs/0710.2254))


[[!redirects Segal spaces]]
