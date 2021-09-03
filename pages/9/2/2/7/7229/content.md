
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

Hilbert's fifth problem, from his famous [[Hilbert's problems|list of problems]] in his address to the International Congress of Mathematicians in 1900, is conventionally understood as broadly asking 

> Which [[topological group|topological groups]] admit [[Lie group]] structures? 

A Lie group here is understood as a [[group object]] in the category of finite-dimensional smooth manifolds locally modeled on $\mathbb{R}^n$. Evidently not all topological groups $G$ admit Lie group structures (consider for example the compact group of $p$-adic integers under addition); a necessary condition is that the underlying space of $G$ be a topological manifold (or equivalently, using the group structure, that there is a neighborhood of the identity that is homeomorphic to a Euclidean space $\mathbb{R}^n$). 

## Results

+-- {: .num_theorem}
###### Theorem 1 (Gleason; Montgomery-Zippin) 
A topological group $G$ underlies a (unique) Lie group structure if and only if the underlying space of $G$ is a topological manifold. 
=-- 

A deeper structural theorem from which theorem 1 can be deduced is 

+-- {: .num_theorem} 
###### Theorem 2 (Gleason-Yamabe) 
Let $G$ be a locally compact group, and let $U$ be an open neighborhood of the identity in $G$. Then there exists an open subgroup $V$ of $G$, and a compact normal subgroup $H$ of $V$ contained in $U$, such that $V/H$ is isomorphic to a Lie group. 
=-- 

An exposition of this incredible theorem was given in a series of blog posts by Terry Tao; see the reference below for a suitable entry point. 

Here are some sample theorems which follow from the Gleason-Yamabe theorem. 

+-- {: .num_theorem} 
###### Theorem 
Suppose $G$ is a locally compact group. A necessary and sufficient condition for $G$ is that it satisfies the "no small subgroups" property (NSS for short) that there exist a neighborhood the identity $U$ so small that it contains no nontrivial subgroups. 
=-- 

+-- {: .proof}
###### Proof 
First let us prove that Lie groups $G$ are NSS. Certainly $\mathbb{R}$ is NSS, and so is $\mathbb{R}^n$. This means we can find a starlike neighborhood $W$ of the origin in $Lie(G)$, small enough so that the exponential map $\exp: Lie(G) \to G$ maps diffeomorphically onto its image $U = \exp(W)$, and so that $W$ contains no line through the origin. Then $U$ contains the image of no 1-parameter subgroup $\phi \colon \mathbb{R} \to G$, otherwise we get a line $L$: 

$$L = (\mathbb{R} \stackrel{\phi}{\to} U \stackrel{\exp^{-1}}{\to} Lie(G))$$ 

whose image is contained in $W$, and this is a contradiction. Since $U$ contains no 1-parameter subgroups, it follows easily that $U$ contains no non-trivial subgroups. 

In the other direction, suppose given such a $U$. It follows from the Gleason-Yamabe theorem that there is an open subgroup $V$ of $G$ that is a Lie group. (To be completed.) 
=--

## Related concepts

* [[nearby homomorphisms from compact Lie groups are conjugate]]

 
## References 

* [[Terence Tao]], Hilbert's fifth problem and Gleason metrics. _What's new_ (weblog), June 17, 2011 ([link](http://terrytao.wordpress.com/2011/06/17/hilberts-fifth-problem-and-gleason-metrics/)). 

