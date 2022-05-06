
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

For $\mathcal{T}$ a [[sheaf topos]], $G \in Grp(\mathcal{T})$ a [[group object]] and $V \in \mathcal{T}$ any object, and for $\rho \colon V \times G \to V$ an [[action]] of $G$ on $V$  , the **quotient stack** $V//G$ is the [[quotient]] of this action but formed not in $\mathcal{T}$ but under the inclusion

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




## Properties

### Relation to principal and associated bundles

For $V = *$ the [[terminal object]], one writes $\mathbf{B}G \coloneqq *//G$.  This is the [[moduli stack]] for $G$-[[principal bundles]]. It is also the trivial _$G$-[[gerbe]]_.

There is a canonical projection $\overline{\rho} \;\colon\; V//G \to \mathbf{B}G$. This is the [[universal associated infinity-bundle|universal rho-associated bundle]].


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

[[!redirects quotient stacks]]

[[!redirects orbifold quotient]]
[[!redirects orbifold quotients]]

[[!redirects quotient orbifold]]
[[!redirects quotient orbifolds]]

[[!redirects stacky quotient]]
