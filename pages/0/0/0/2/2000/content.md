
#Contents#
* table of contents
{:toc}


This entry is about smooth morphisms of schemes. There are many notions of smoothness in algebra and algebraic geometry, many under the name of (such and such) regularity (nonsingularity); even in [[EGA]] there are something like 11 notions, one of which is called the smooth morphism of schemes. In the literature there are sometimes even small variations of the latter (e.g. weather we allow globally varying dimension of the smooth morphism or not). In $n$Lab a prominent role is played by the [[formally smooth morphism|formal smoothness]], which is weaker than smoothness.

## Idea

Smooth morphism is a relativization of the notion of a [[smooth scheme]].

## Definition


A [[morphism]] $f:X\to Y$ of [[schemes]] is **smooth** if 

* it is [[flat morphism|flat]] 

* and finitely presented (cf. [[relativization in algebraic geometry]]) 

* and if all the [[fiber]]s $f^{-1}(y)$ where $y\in Y$ are [[smooth schemes]] over the corresponding [[residue field]]s $k_y$. 


## Properties

Smoothness of a morphism is a higher dimensional analogue of the notion of a morphism being [[etale morphism|étale]] (which is a smooth morphism of relative dimension $0$), but stronger than the notion of [[formally smooth morphism|formal smoothness]]. 

#### Smoothness versus formal smoothness 

For a morphism $f:X\to Y$ of schemes, and $x$ a point of $X$, the following are equivalent

(i) $f$ is a smooth morphism at $x$

(ii) $f$ is locally of finite presentation at $x$ and there is an open neighborhood $U\subset X$ of $x$ such that $f|_U: U\to Y$ is formally smooth

(iii) $f$ is flat at $x$, locally of finite presentation at $x$ and the sheaf of [[Kähler differential]]s $\Omega_{X/Y}$ is locally free in a neighborhood of $x$

The relative dimension of $f$ at $x$ will equal the rank of the module of K&#228;hler differentials. 

This is ([[EGAIV]]${}_4$ 17.5.2 and 17.15.15)

## Related concepts

A smooth morphism of [[relative dimension]] 0 is an [[étale morphism]].

See also [[formally smooth morphism]].

* The [[lisse-étale site]] of a [[scheme]] $X$ consists of smooth morphisms $U \to X$.


## References

* Arthur Ogus, _Smooth morphisms_ ([pdf](http://math.berkeley.edu/~ogus/Math%20_256A--08/smooth.pdf))

* Peter Bruin, _Smooth morphisms_ ([ps](http://www.google.com/url?sa=t&source=web&cd=8&ved=0CEkQFjAH&url=http%3A%2F%2Fwww.math.leidenuniv.nl%2F~pbruin%2Fsmooth.ps&rct=j&q=%22relative%20dimension%22%20smooth&ei=1zn9TOesBIrrOZbr1NQK&usg=AFQjCNFRuNB5BNwI3hXEA9jsLajt0tZldQ&cad=rja))

[[!redirects smooth morphisms of schemes]]