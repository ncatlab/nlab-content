
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $\mathcal{T}$ a [[sheaf topos]], $G \in Grp(\mathcal{T})$ a [[group object]] and $V \in \mathcal{T}$ any object, and for $\rho \colon V \times G \to V$ an [[action]] of $G$ on $V$  , the **quotient stack** $V// G$ is the [[quotient]] of this action but formed not in $\mathcal{T}$ but under the inclusion

$$
  \mathcal{T} \hookrightarrow \mathbf{H}
$$

into the [[(2,1)-topos]] over the given [[site]] of definition: it is the quotient after regarding the action as an [[infinity-action]] in $\mathbf{H}$.

This is the geometric version of the notion of _[[action groupoid]]_. A wider notion of the quotient stack may be defined using more general internal groupoids. Indeed,
the [[small fibration]] obtained by the [[externalization]] of an internal groupoid in a site with pullbacks will be a [[fibered category]] which is a candidate for a quotient stack in this context. For many interesting sites, sometimes under additional conditions on the internal groupoid, the resulting small fibration is indeed a stack.

If the [[stabilizer subgroups]] of the [[action]] are [[finite groups]], then the quotient stack is an [[orbifold]]/[[Deligne-Mumford stack]] --the "quotient orbifold".

## Motivation for definition of quotient stack. 

Let $G$ be a Lie group action on a manifold $X$ (left action). 

We define the quotient stack $[X/G]$ as 
$$
[X/G](Y):=\{P\xrightarrow{p} Y, P\xrightarrow{f}X | P\rightarrow Y \text{ is a G-bundle,} f  \text{ is } G\text{-equivariant}\}.
$$ 

Morphisms of objects are $G$-equivariant isomorphisms. This definition is taken from Heinloth's [Some notes on Differentiable stacks](https://www.uni-due.de/~hm0002/stacks.pdf).

Given a Lie group action of $G$ on $X$, if we want to associate a stack, we  start with simpler cases which allows us to guess how to define $[X/G]$ in general.

1. Suppose $X$ is trivial and $G$ acts trivially on $X=\{*\}$ then $[X/G]$ should only depend on $G$. We know what stack to associate for a Lie group $G$ i.e., $BG$. Thus, $[X/G]$ should just be $BG$.

2. Suppose $G$ is trivial and $G$ acts on $X$, $[X/G]$ should only depend on $X$. We know what stack to associate for a manifold $X$ i.e., $\underline{X}$. Thus, $[X/G]$ should just be $\underline{X}$.

3. Suppose $G$ is non trivial and $X$ is non trivial and that the action of $G$ on $X$ is free (and proper) so that $X/G$ is a manifold. We know what stack to associate for a manifold $X/G$ i.e., $\underline{X/G}$. Thus, $[X/G]$ should just be $\underline{X/G}$. 

 
For general case of $G$ acting on $X$, we get a Lie groupoid, called the Translation groupoid (or action groupoid) usually denoted by $G\ltimes X$. 

* Given a manifold $M$, we have a stack associated to it, namely $\underline{M}$. Given a Lie group $G$, we have a stack associated to it, namely $BG$. Given a Lie groupoid $\mathcal{G}$, we have a stack associated to it, namely $B\mathcal{G}$ i.e., the stack of principal groupoid $\mathcal{G}$ bundles.

For action groupoid $\mathcal{G}=G\ltimes X$, let $B\mathcal{G}$ be the corresponding stack of principal $\mathcal{G}$ bundles. It turns out that $B\mathcal{G}$ is same $[X/G]$ defined above. More details to be found in [this page](https://mathoverflow.net/questions/319038/motivation-for-definition-of-quotient-stack).


 * If action of the Lie group $G$ on the manifold $X$ is free and proper, what we get is   **a manifold** $X/G$. Stack associated to this manifold is $\underline{X/G}$ which we call to be the quotient stack, denote by $[X/G]$.


 * If the action of the Lie group $G$ on the manifold $X$ is not necessarily free and proper, what we get is   **a Lie groupoid** denoted (among other symbols) by $X//G$. Stack associated to this Lie groupoid $X//G$ is $B(X//G)$ which we call to be the quotient stack, denote by $[X/G]$.

## Universal property (??) for Quotient stack

Let $G$ be a Lie group and $X$ be a manifold with a $G$ action on it. 

Suppose $G$ acts freely, properly on $X$ then, we have mentioned that the quotient stack $[X/G]$ has to be the stack $\underline{X/G}$. The proper, free action of $G$ on $X$ gives a principal $G$ bundle $X\rightarrow X/G$. This $X\rightarrow X/G$ gives a map of stacks $\underline{X}\rightarrow \underline{X/G}$. We call the map of stacks $\underline{X}\rightarrow \underline{X/G}$ to be a principal $G$ bundle. 

A map of stacks $\underline{M}\rightarrow \mathcal{D}$ is said to be representable morphism if given a manifold $N$ and a map of stacks $\underline{N}\rightarrow \mathcal{D}$, the fiber product $\underline{M}\times_{\mathcal{D}}\underline{N}$ is a manifold. 

A map of stacks $\underline{M}\rightarrow \mathcal{D}$ is said to be a principal $G$ bundle if it is a representable morphism and the map of manifolds $\underline{M}\times_{\mathcal{D}}\underline{N}\rightarrow N$ is a principal $G$ bundle. 

It is easy to see that the map of stacks $\underline{X}\rightarrow \underline{X/G}$ is a principal $G$ bundle as the map of manifolds
$X\rightarrow X/G$ is a principal $G$ bundle. 

We see the property "$\underline{X}\rightarrow \underline{X/G}$ is a principal $G$ bundle" as main  ingredient to define the quotient stack $[X/G]$.  Irrespective of $G$ acting freely and properly on $X$, we want to define quotient stack as a stack $\mathcal{D}$ such that $\underline{X}\rightarrow \mathcal{D}$ is a principal $G$ bundle in minimal terms. 

More precisely, by quotient stack of the action of $G$ on $X$, we mean a stack $\mathcal{D}$ that **comes with a map of stacks $\underline{X}\rightarrow \mathcal{D}$** that is a principal $G$ bundle (in the sense defined above) any map of stacks $\underline{X}\rightarrow \mathcal{C}$ that is a principal $G$ bundle factors through this map $\underline{X}\rightarrow \mathcal{D}$. 

If $G$ acts freely and properly, then obvious choice for $\mathcal{D}$ is the stack $\underline{X/G}$. 

Using the universal property, it turns out that $\mathcal{D}$ has to be the stack in the definition of quotient stack 
$$
\mathcal{D}(Y):=\{P\xrightarrow{p} Y, P\xrightarrow{f}X | P\rightarrow Y \text{ is a G-bundle,} f  \text{ is } G\text{-equivariant}\}.
$$ 

Morphisms of objects are $G$-equivariant isomorphisms. We fix the notation $[X/G]$ for $\mathcal{D}$ and call it the quotient stack. 



## Properties

### Relation to principal and associated bundles

For $V = *$ the [[terminal object]], one writes $\mathbf{B}G \coloneqq *// G$.  This is the [[moduli stack]] for $G$-[[principal bundles]]. It is also the trivial _$G$-[[gerbe]]_.

There is a canonical projection $\overline{\rho} \;\colon\; V// G \to \mathbf{B}G$. This is the [[universal associated infinity-bundle|universal rho-associated bundle]].


## Related concepts

* [[quotient]], [[quotient space]], [[quotient type]]

* [[action groupoid]]

* [[local quotient stack]]

* [[Borel construction]]

* [[(infinity,1)-colimit]], [[infinity-action]]

* [[mapping stack]]

* [[orbifold]], [[Deligne-Mumford stack]]

* [[geometric invariant theory]]


## References

(...)

* [[Jack Morava]], _Theories of anything_ ([arXiv:1202.0684](http://arxiv.org/abs/1202.0684))

* [[J. Heinloth]], _Some notes on Differentiable stacks_([stacks] (https://www.uni-due.de/~hm0002/stacks.pdf))

[[!redirects quotient stacks]]

[[!redirects orbifold quotient]]
[[!redirects orbifold quotients]]

[[!redirects quotient orbifold]]
[[!redirects quotient orbifolds]]

[[!redirects stacky quotient]]
