
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


# Effective epimorphisms
* automatic table of contents goes here
{:toc}

## Idea

* [[effective epimorphism]] $\Rightarrow$ [[regular epimorphism]] $\Leftrightarrow$ [[covering]]

* [[effective monomorphism]] $\Rightarrow$ [[regular monomorphism]] $\Leftrightarrow$ [[embedding]] .


## Definition 


An **effective epimorphism** in a [[category]] $C$ is a [[morphism]] $f : c \to d$ (in a given [[category]]) that has a [[kernel pair]] $c \times_d c$ and is the [[quotient object]] of this kernel pair in that 

$$
  c \times_d c \stackrel{\to}{\to} c \stackrel{f}{\to} d
$$

is a [[colimit]] diagram (a [[coequalizer]]).  This is equivalent to saying that $f$ is a [[regular epimorphism]] which has a kernel pair, since any morphism which is a coequalizer and has a kernel pair must be the coequalizer of its kernel pair.  (This is a special case of the theory of [[generalized kernels]].)

The reader should be aware, however, that some writers use "effective epimorphism" to mean what is here called a [[strict epimorphism]].

In other words this says that $f : c \to d$ is effective if $d$ is the [[coimage]] of $f$.

Sometimes we say that such morphism $f$ is an [[effective quotient]].



## Remarks 

The [[duality|dual]] concept is that of [[effective monomorphism]].

An effective epimorphism is necessarily a [[regular epimorphism]].  Conversely, any regular epimorphism that has a kernel pair is an effective epimorphism.

In [[Set|the category of sets]], every [[epimorphism]] is effective. Thus, it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.  In particular, one may define a [[projective object]] (and hence the [[axiom of choice]]) using effective epimorphisms.



## Related concepts

* **effective epimorphism**

* [[effective epimorphism in an (infinity,1)-category]]

[[!redirects effective epi]]
[[!redirects effective epimorphism]]
[[!redirects effective epimorphisms]]


