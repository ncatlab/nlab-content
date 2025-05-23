
> This page is about the general concept of embeddings in [[category theory]]. For the special cases see embeddings  _[[embedding of topological spaces|of topological spaces]]_, _[[embedding of smooth manifolds|of smooth manifolds]]_, or _[[embedding of types|of types]]_. For the notion in [[model theory]] see instead at *[[elementary embedding]]*.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An embedding is, generally, a [[morphism]] which in some sense is an [[isomorphism]] onto its [[image]]

For this to make sense in a given [[category]] $C$, we not only need a good notion of image.  Note that it is not enough to have the image of $f\colon X \to Y$ as a [[subobject]] $\im f$ of $Y$; we also need to be able to interpret $f$ as a morphism from $X$ to $\im f$, because it is this morphism that we are asking to be an isomorphism.


* [[effective epimorphism]] $\Rightarrow$ [[regular epimorphism]] $\Leftrightarrow$ [[covering]]

* [[effective monomorphism]] $\Rightarrow$ [[regular monomorphism]] $\Leftrightarrow$ [[embedding]] .


## As regular or effective monomorphisms

### Definition

One general abstract way to define an _embedding_ morphism is to say that this is equivalently a [[regular monomorphism]].

If the ambient category has [[finite limits]] and [[finite colimits]], then this is equivalently an [[effective monomorphism]]. In terms of this we recover a formalization of the above idea, that an embedding is an iso onto its _image_ :

For a [[morphism]] $f : X \to Y$ in $C$ the definition of [image as an equalizer](http://ncatlab.org/nlab/show/image#AsEqualizer) says that the [[image]] of $f$ is

$$
  im f 
    \coloneqq 
  \lim_\leftarrow ( Y \stackrel{\to}{\to} Y \coprod_X Y) 
  \,.
$$ 

In particular we have a factorization of $f$ as

$$
  f \colon X \stackrel{\tilde f}{\to} im f \hookrightarrow Y
  \,,
$$

where the morphism on the right is a [[monomorphism]].

The morphism $f$ being an [[effective monomorphism]] means that $\tilde f$ is an [[isomorphism]], hence that $f$ is an "isomomorphism onto its image".

## Examples

### In $Top$

A morphism $U \to X$ of [[topological space]]s is a regular monomorphism precisely if this is an injection such that the topology on $U$ is the [[induced topology]]. This is an **[[embedding of topological spaces]]**.

### In $SmoothMfd$

* [[embedding of smooth manifolds]]

### In $Sch$

* [[Plücker embedding]]

## Related concepts

* [[embedding type]]

* [[embedding in type theory]]




[[!redirects embedding]]
[[!redirects embeddings]]
[[!redirects imbedding]]
[[!redirects imbeddings]]

[[!redirects closed embedding]]

[[!redirects open embedding]]
[[!redirects open embeddings]]

[[!redirects imbedding]]
[[!redirects imbeddings]]

