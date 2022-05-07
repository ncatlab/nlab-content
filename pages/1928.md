
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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


The concept of _[[resolution]]_ in [[homotopy theory]] specialized to [[simplicial homotopy theory]] is "simplicial resolution".  Simplicial resolutions can be constructed in various ways, for instance by a comonad, or by a step-by-step method that resembles the construction of a Eilenberg-Mac Lane space from a presentation, followed by adding cells to 'kill' the higher homotopy groups.

> the following needs attention

##Remark

In any ambient [[category]] or $\infty$-[[infinity-category|category]] $C$ that admits a notion of 
[[colimit]] or [[weak limit|weak colimit]], a _simplicial resolution_
of an object $c \in C$ is a [[simplicial object]] 
$y_\bullet : \Delta^{op} \to C$ together with a realization of $c$ as a colimit

$$
  c \simeq colim_{[k]} y_k
  \,.
$$

The term is also used for a [[Reedy model structure|Reedy fibrant]] replacement of a constant simplicial object in a [[model category]]; see also [[resolution]].

[[Cocones]] under a simplicial diagram are exactly the [[augmented simplicial objects]], so a simplicial resolution of $c$ can alternately be described as an augmented simplicial object $y_\bullet : \Delta^{op}_+ \to C$ that is a colimiting cocone, and such that $y_{-1} = c$.

### Examples 

1. A basic example is the free simplicial resolution of a group.

There is the obvious adjoint pair of functors,

$$U:Groups\to Sets,  F:Sets\to Groups.$$


 Writing $\eta : Id \to UF$ and $\varepsilon :FU\to Id$ for the unit and counit of this adjunction, we have a comonad on $Groups$, the free  group comonad, $( FU, \varepsilon, F\eta U)$.  

We write $L = FU$, $\delta = F\eta U$, so that 

$$\varepsilon : L \to I$$ 

is the counit of the comonad whilst 

$$\delta: L \to L^2$$

is the comultiplication.

Now suppose $G$ is a  group and set $F(G)_i = L^{i+1}(G)$, so that $F(G)_0$ is the free  group on the underlying set of $G$ and so on.  

The counit (which is just the augmentation morphism from $FU(G)$ to $G$) gives, in each dimension, face morphisms

$$d_i = L^{n-i}\varepsilon L^{i}(G) : L^{n+1}(G) \to L^n(G),$$ 
for $i = 0, \ldots, n$,
whilst the comultiplication gives degeneracies,

$$s_i : L^n(G) \to L^{n+1}(G)$$

$$s_i = L^{n-1-i}\delta L^{i}, $$
for $i = 0, \ldots, n-1$,

satisfying the simplicial identities.  

The resulting object is an augmented [[simplicial group]] that is free in all non-negative dimensions and is acyclic. It has zeroth homotopy equal to $G$ and all homotopy groups are trivial.

Of course this construction did not depend on the fact that we were handling groups, so we could apply it to any [[comonad]] on any category (within reason!) This has the advantage of providing simplicial resolutions that are functorial. These are sometimes called _comonadic resolutions_.

This leads to the subject of [[monadic cohomology]]. 




1. In an [[(infinity,1)-topos]] [[Čech cover]] $C(U) \stackrel{\simeq}{\to} X$
  induced by a [[cover]] $(U = \coprod_i U_i) \to X$ is a simplicial resolution of $X$.

## Related concepts

* [[homological resolution]]

## References 

Classical soureces include Godement's book, 

** [[Roger Godement]], _Topologie Algébrique et Théorie des Faisceaux_. Actualités Sci. Ind. No. 1252. Publ. Math. Univ. Strasbourg. No. 13 Hermann, Paris 1958.


but the theory is explained in many sources including the monograph:
*  [[J. Duskin]], 1975, Simplicial methods and the interpretation of "triple" cohomology , number 163 in Mem. Amer. Math. Soc., 3, Amer. Math. Soc.

Simplicial resolutions in the context of 
[[presentable (infinity,1)-category|presentable (infinity,1)-categories]] are discussed in section 6.1.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

(below lemma 6.1.4.3)

[[!redirects simplicial resolutions]]

[[!redirects comonadic resolution]]
