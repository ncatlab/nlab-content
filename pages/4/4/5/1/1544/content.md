
A connection on a [[bundle]] can be introduced in several very different but equivalent formalisms: as a __parallel transport__ functor, as a rule for __[[covariant derivative]]__, as a __distribution (field) of horizontal subspaces__ (see [[Ehresmann connection]]) and via a __connection $1$-form__ which annihilates the distribution of horizontal subspaces. The connection in that sense induces a smooth version of [[Hurewicz connection]]. The usual textbook convention is to say just connection for the distribution of horizontal subspaces, and the objects of the other three approaches one calls more specifically covariant derivative, connection $1$-form and parallel transport.

The following article mostly deals with parallel transport.

#Contents#
* automatic table of contents goes here
{:toc}


#Idea#

Given a smooth [[bundle]] $P \to X$, for instance a $G$-[[principal bundle]] or a [[vector bundle]], a _connection_ on $P$ is a prescription to associate with each path

$$
  \gamma : x \to y
$$

in $X$  (which is a [[morphism]] in the [[path groupoid]] $P_1(X)$) a morphism $tra(\gamma)$ between the fibers of $P$ over these points

$$
  \array{
     P_x &\stackrel{tra(\gamma)}{\to}& P_y
     \\
     x &\stackrel{\gamma}{\to}& y
  }
$$

such that

* this assignment respects the structure on the fibers $P_x$ (for instance is $G$-equivariant in the case that $P$ is a $G$-bundle or that is linear in the case that $P$ is a vector bundle);

* this assignment is smooth in a suitable sense;

* this assignment is [[functor]]ial in that for all pairs $x \stackrel{\gamma}{\to} y$, $y \stackrel{\gamma'}{\to} z$ of composable paths in $X$ we have
  $$
    \array{
       P_x &\stackrel{tra(\gamma)}{\to}& P_y &\stackrel{tra(\gamma')}{\to}& P_z
       \\
       x &\stackrel{\gamma}{\to}& y &\stackrel{\gamma'}{\to}& z
    }
    \;\;\;
    =
    \;\;\;
    \array{
       P_x &\stackrel{tra(\gamma' \circ \gamma)}{\to}& P_z
       \\
       x &\stackrel{\gamma'\circ \gamma}{\to}& z
    }
  $$


In other words, a connection on $P$ is a [[functor]] 

$$
  tra : P_1(X) \to At''(P)
$$

from the [[path groupoid]] of $X$ to the [[Atiyah Lie groupoid]] of $P$ that is smooth in a suitable sense and _splits the Atiyah sequence_ in that $P_1(X) \stackrel{tra}{\to} At''(X) \to P_1(X)$ (see the notation at [[Atiyah Lie groupoid]]).

## Terminology ##

The functor $tra$ is called the **parallel transport** of the connection. This terminology comes from looking at the orbits of all points in $P$ under $tra$ (i.e. from looking at the [[category of elements]] of $tra$): these trace out paths in $P$ sitting over paths in $X$ and one thinks of the image of a point $p \in P_x$ under $tra(\gamma)$ as the result of propagating $p$ parallel to these curves in $P$. 

## flat connections ##

It may happen that the assignment $tra : \gamma \mapsto tra(\gamma)$ only depends on the [[homotopy]] class of the path $\gamma$ relative to its endpoints $x, y$. In other words: that $tra$ factors through the functor $P_1(X) \to \Pi_1(X)$ from the [[path groupoid]] to the [[fundamental groupoid]] of $X$. In that case the connection is called a **flat connection**.

## more concrete picture ##

By [[Lie theory|Lie differentiation]] the functor $tra$, i.e. by looking at what it does to very short pieces of paths, one obtains from it a splitting of the [[Atiyah Lie groupoid|Atiyah Lie algebroid sequence]], which is a morphism

$$
  \nabla : T X \to at(P)
$$ 

of vector bundles. Locally on $X$ -- meaning: when everything is pulled back to a [[cover]] $Y \to X$ of $X$ -- this is a $Lie(G)$-valued 1-form $A \in \Omega^1(Y, Lie(G))$ with certain special properties.

In particular, since every $G$-[[principal bundle]] canonically trivializes when pulled back to its own total space $P$, a connection in this case gives rise to a 1-form $A \in \Omega^1(P)$ satisfying two conditions. This data is called an **[[Ehresmann connection]]**.

If instead $P = E$ is a vector bundle, then the two conditions satisfies by $A$ imply that it defines a linear map

$$
  \nabla : \Gamma(E) \to \Omega^1(X) \otimes \Gamma(E)
$$

from the space $\Gamma(E)$ of section of $E$ that satisfies the properties of a **covariant derivative**.

If again the connection is flat, then this is manifestly the datum of a [[Lie infinity-algebroid representation]] of the [[Lie algebroid|tangent Lie algebroid]] $T X$ of $X$ on $E$: it defines the action [[Lie algebroid]] which is the [[Lie theory|Lie version]] of the [[Lie groupoid]] classified by the parallel transport functor.

...

## more abstract picture ##

Recall from the discussion at $G$-[[principal bundle]] that the $G$-bundle $P \to X$ is encoded in a a suitable morphism

$$
  X \to \mathbf{B}G
$$

(namely a morphism in the right [[(infinity,1)-category]] which may be represented by an [[anafunctor]]).

It turns out that similarly suitable morphisms

$$
  P_1(X) \to \mathbf{B}G
$$

encode in one step the $G$-bundle together with its parallel transport functor.

This is described in great detail in the reference by Schreiber--Waldorf below.

(...am running out of time... for more see [[schreiber:Differential Nonabelian Cohomology|here]])
...

#Definition# 

...


# Special cases #

## connections on the tangent bundle ##

Connections on [[tangent bundle]]s play an important role for instance on  [[Riemannian manifold]]s and [[pseudo-Riemannian metric|pseudo-Riemannian manifold]]s. From the end of the 19th century and the beginning of the 20th centure originates a language to talk about these in terms of [[Christoffel symbol]]s. 


# Generalizations#

## superconnections ##

Generalizing the parallel transport definition from ordinary manifolds to [[supermanifold]]s yields the notion of [[superconnection]].

#References#

The description of connections as smooth functors on the [[path groupoid]] has a long history in its restriction to _based loops_ . This is recalled at

* [[Urs Schreiber]], [History of Understanding Bundles with Connection using Parallel Transport around Loops](http://golem.ph.utexas.edu/category/2007/03/history_of_understanding_bundl.html).

The idea to generalize this from loops to paths is due to [[John Baez]] and appears in 

* [[John Baez]], [[Urs Schreiber]], _Higher Gauge Theory_ ([arXiv](http://math.ucr.edu/home/baez/higher.pdf))

Full details, including detailed discussion of the equivalence to other familiar definitions, are in 

* [[Urs Schreiber]], [[Konrad Waldorf]], _Parallel transport and functors_ ([arXiv](http://arxiv.org/abs/0705.0452))

A proposal for the full proper generalization of the functorial notion of connection to the context of smooth [[infinity-stack]]s along the lines described at [[motivation for sheaves, cohomology and higher stacks]] is in [section 2.1.6](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf#page=15) of 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential String- and Fivebrane structures_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf))

For more links, more history and further pointers see

* [[schreiber:Differential Nonabelian Cohomology|Differential Nonabelian Cohomology]] .


[[!redirects parallel transport]]