


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--








#Contents#
* table of contents
{:toc}

## Idea

The analog in the context of [[(∞,1)-topos]] theory of a [[local geometric morphism]] in [[topos theory]].


## Definition

A **local geometric morphism** $f : E \to S$ between [[(∞,1)-topos]]es $\mathbf{H},\mathbf{S}$ is 

* a [[geometric morphism]]

  $$
    (f^* \dashv f_*) 
     : 
      \mathbf{H} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}
    {\to}}  \mathbf{S}
  $$

* such that a further [[right adjoint]] $f^! : \mathbf{S} \to \mathbf{H}$ exists:

  $$
    (f^* \dashv f_* \dashv f^!) : 
    \mathbf{H}
     \stackrel{\overset{f^*}{\leftarrow}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    \mathbf{S}
  $$

* and such that some additional condition is satisfied.  See [[local geometric morphism]] for a list of equivalent conditions in the 1-categorical case; one or more of them should appear here.  (However, one may expect them to be redundant when $S=\infty Gpd$, just as they are redundant in the 1-categorical case when $S=Set$.)

If $f : \mathbf{H} \to \mathbf{S}$ is the [[global section]] geometric morphism in the category of $(\infty,1)$toposes over $\mathbf{S}$, then we say that $\mathbf{H}$ is a **local $(\infty,1)$-topos**.


## Properties

* [[concrete (∞,1)-sheaf]]










## Related concpepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / **local (∞,1)-topos**.

* [[cohesive topos]] / **cohesive (∞,1)-topos**

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]


## References

The 1-categorical notion is discussed in

* [[Peter Johnstone]], [[Ieke Moerdijk]], _Local maps of toposes_  Proc. London Math. Soc.  (1989)   s3-58  (2):  281-305.  ([pdf](http://plms.oxfordjournals.org/content/s3-58/2/281.full.pdf+html))




[[!redirects local (∞,1)-geometric morphisms]]
[[!redirects local (∞,1)-topos]]
[[!redirects local (∞,1)-toposes]]
[[!redirects local (∞,1)-topoi]]


[[!redirects local (infinity,1)-topos]]