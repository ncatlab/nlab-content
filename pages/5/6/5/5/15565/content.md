
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An analog of [[jet spaces]] in [[arithmetic geometry]].

## Definition
 {#Definition}

Notice that the [[p-adic integers]] $\mathbb{Z}_p$ are (by the discussion at [p-adic integer -- as formal power series](p-adic+integer#AsFormalNeighbourhoodOfPrime))  the analog in [[arithmetic geometry]] of a [[formal power series]] ring (around the point $p \in$ [[Spec(Z)]]), hence their [[formal spectrum]] $Spf(\mathbb{Z}_p)$ is an incarnation in [[arithmetic geometry]] of an abstract [[formal disk]]. 

Therefore in the sense of [[synthetic differential geometry]] the $p$-[[formal neighbourhood]] of any [[arithmetic scheme]] $X$ around a global point $x \colon Spec(\mathbb{Z}) \to X$ is the space of lifts

$$
  \array{
    Spf(\mathbb{Z}_p)  && \stackrel{\hat x}{\longrightarrow}&& X
    \\
    & \searrow &&  \swarrow
    \\
    && Spec(\mathbb{Z})
  }
  \,.
$$

Moreover the map that sends an commutative ring, hence an [[arithmetic variety]], to its $p$-formal power series in this sense is the construction of the [[ring of Witt vectors]] ($p$-typical Witt vectors if one fixes one prime, and "big Witt vectors" if one considers all at once) - see e.g. [Hartl 06, section 1.1](#Hartl06).

The following definition says essentially this, but further sends the resulting space to [[F1]]-geometry in the sense of [[Borger's absolute geometry]]:
 
For $X= Spec(R)$ an [[affine scheme]] over [[Spec(Z)]] (hence the formal dual of a [[ring]]), then the _arithmetic jet space_ of $X$ at [[prime]] $p$ is $(W_n)_\ast$ applied to the $p$-adic completion of $X$, where $(W_n)_\ast$ is the [[ring of Witt vectors]]-construction, the [[direct image]] of [[Borger's absolute geometry]] $Et(Spec(\mathbb{Z})) \to Et(Spec(\mathbb{F}_1))$.

The definition is originally due to ([Buium 96, section 2](#Buium96), [Buium 05, section 3.1](#Buium05)), reviewed in ([Buium 13, 1.2.3](#Buium13)). The above formulation is in ([Borger 10, (12.8.2)](#Borger10)).


## References

The original articles are

* {#Buium96} [[Alexandru Buium]], _Geometry of $p$-jets. Duke Math. J., 82(2):349&#8211;367, 1996. ([Euclid](http://projecteuclid.org/euclid.dmj/1077245037))

* {#Buium05} [[Alexandru Buium]], _Arithmetic differential equations_, volume 118 of Mathematical Surveys and Monographs. American Mathematical Society, Providence, RI, 2005. ([pdf](http://www.math.unm.edu/~buium/prebook.pdf))

Introduction and survey is in 

* {#Buium13} [[Alexandru Buium]], _Differential calculus with integers_ ([arXiv:1308.5194](http://arxiv.org/abs/1308.5194), [slightly differing pdf](http://www.math.unm.edu/~buium/statupdated.pdf))

* [[Alexandru Buium]], _Lectures on arithmetic differential equations_ ([pdf](http://www.lorentzcenter.nl/lc/web/2009/342/presentations/lectures%20A.%20Buium.pdf))

Discussion in the context of the [[function field analogy]] is in 

* {#Hartl06} [[Urs Hartl]], _A Dictionary between Fontaine-Theory and its Analogue in Equal Characteristic_ ([arXiv:math/0607182](http://arxiv.org/abs/math/0607182))

Discussion in the context of [[Borger's absolute geometry]] over [[F1]] is in 

* {#Borger10} [[James Borger]],  _The basic geometry of Witt vectors, II: Spaces_ ([arXiv:1006.0092](http://arxiv.org/abs/1006.0092))

See also

* [[Alexandru Buium]], Taylor Dupuy, _Arithmetic differential equations on $GL_n$, I: differential cocycles_ ([arXiv:1308.0748](http://arxiv.org/abs/1308.0748))
 


[[!redirects arithmetic jet spaces]]

[[!redirects arithmetic differential equation]]
[[!redirects arithmetic differential equations]]