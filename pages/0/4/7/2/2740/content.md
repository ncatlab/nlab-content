
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A Poisson Lie algebroid on a [[manifold]] $X$ is a [[Lie algebroid]]
on $X$ naturally defined from and defining the structure of a
[[Poisson manifold]] on $X$.

This is the degree-1 example of a tower of related concepts, described
at [[n-symplectic manifold]].


#Definition#

Let $\pi \in \Gamma(T X) \wedge \Gamma(T X)$ be a Poisson structure on
$X$, regarded as a bivector.

This is an element of degree 2 in the [[exterior algebra]]
 $\wedge^\bullet \Gamma(T X)$ of multivector fields on $X$. The Lie
 bracket on [[tangent bundle|tangent vector]]s in $\Gamma(T X)$
 extends to a bracket $[-,-]_{Sch$ on multivector field, the
 **Schouten bracket**. The defining property of the Poisson structure
 $\pi$ is that

$$
  [\pi,\pi]_{Sch} = 0
  \,.
$$

This makes 

$$
  d_{CE(X,\pi)} := [\pi, -] : CE(X,\pi) \to CE(X,\pi)
$$ 

into a differential of degree +1 that squares to 0. We write
$CE(X,\pi)$ for the exterior algebra equipped with this
differential. Then $CE(X,\pi)$ is the [[Chevalley-Eilenberg algebra]]
of some [[Lie algebroid]]. This is the **Poisson Lie algebroid** of
$(X,\pi)$.

In terms of the vector-bundle-with anchor definition of [[Lie
algebroid]] this is

$$
  \array{
      T^* X &&\stackrel{\pi(-)}{\to}&& T X
      \\
      & \searrow && \swarrow
      \\
      && X
  }
  \,.
$$

#Integration#

Under [[Lie integration]] a Poisson Lie alghebroid is supposed to
yield a [[symplectic groupoid]].

#References#

A review is for instance in appendix A of

* [[Dmitry Roytenberg]], _Courant algebroids, derived brackets and
  even symplectic supermanifolds_
  ([arXiv](http://arxiv.org/abs/math/9910078))
