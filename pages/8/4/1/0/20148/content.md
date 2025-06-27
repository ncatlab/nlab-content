
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[Pin group]] in [[dimension]] [[2]].

## Properties

Let $\mathbb{H}$ be the [[quaternions]] generated from unit [[imaginary number|imaginaries]] $\mathbf{i}$, $\mathbf{j}$ with $\mathbf{k} \coloneqq \mathbf{i} \, \mathbf{j}$, with a copy of the [[complex numbers]] identified as

$$
  \begin{array}{ccc}
    \mathbb{C} &\xhookrightarrow{\phantom{---}}& \mathbb{H}
    \\
    x + \mathrm{i} y &\mapsto& x + \mathbf{i} y
    \mathrlap{\,.}
  \end{array}
$$ 

Identify the [[circle group]] with the [[unit circle]] in $\mathbb{C} \hookrightarrow \mathbb{H}$ this way

$$
  \begin{array}{ccccc}
    SO(2) 
    &\simeq&
    S\big( \mathbb{C}\big) 
      &\xhookrightarrow{\phantom{--}}& 
    \mathbb{H}
    \\
    && 
    x + \mathrm{i} y
    &\mapsto&
    x + \mathbf{i} y
  \end{array}
  \phantom{-------}
  \begin{array}{l}
    x,y \in \mathbb{R}   
    \\
    x^2 + y^2 = 1
    \mathrlap{\,,}
  \end{array}
$$

with group structure now thought of as given by multiplication of [[quaternions]]. Then the [[Pin group]] $Pin_-(2)$ is [[isomorphism|isomorphic]] to the [[subgroup]] of the [[group of units]] $\mathbb{H}^\times$ of the [[quaternions]] which consists of this copy of [[SO(2)]], together with the multiples of the imaginary quaternion $\mathbf{j}$ with this copy:

\[
  \label{PinMinus2AsUnionOfCircles}
  Pin_-(2)
  \;\simeq\;
  S\big( \mathbb{C}\big) 
   \;\cup\; 
  \mathbf{j} \cdot S\big( \mathbb{C}\big) 
  \;\subset\;
  \mathbb{H}^\times
  \,.
\]

This is in fact inside the [[unit sphere]] $S(\mathbb{H}) \simeq $ [[Spin(3)]], whence we have a canonical inclusion

\[
  \label{InclusionIntoSpin3}
  Pin_-(2)
  \xhookrightarrow{\phantom{--}}
  Spin(3)
  \,.
\] 


## Properties

### Relation to orthogonal and binary dihedral groups

By the classification of the [[finite subgroups of Spin(3)]] this means that the restriction of $Pin_-(2)$ to the inclusion of the [[dihedral group]] $D_{2n}$ into the [[orthogonal group]] $O(2)$ is the [[binary dihedral group]] $2 D_{2n}$:

\[
  \label{DiagramRestrictingToBinaryDihedralGroup}
  \array{
    2 D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Pin_-(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    \\
    D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    O(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
\]

{#ExplicitDoubleCovering} To make this fully explicit:

With the presentation (eq:PinMinus2AsUnionOfCircles) we are to identify the [[plane]] with the [[linear span]] of the generators $\mathbf{j}$ and $\mathbf{k}$

$$
  \mathbb{R}^2 
  \;\simeq\;
  \langle \mathbf{j}, \mathbf{k}\rangle
  \;\subset\;
  \mathbb{H}_{\mathrm{im}}
  \mathrlap{\,,}
$$

where we may think of 

* $\langle \mathbf{j} \rangle$ as the x-axis,

* $\langle \mathbf{k} \rangle$ as the y-axis.

The action of $Pin_-(2)$ on $\mathbb{R}^2$ is by [[conjugation]] in $\mathbb{H}$. Hence we have plane **[[rotation]]** operators

$$
  R_{\alpha}
  \;\coloneqq\; 
  Ad_{
    \cos(\alpha/2) 
    +
    \sin(\alpha/2)
    \mathbf{i} 
  }
  \;\in\;
  S(\mathbb{C}) \subset S(\mathbb{H})
$$

acting on $\mathbb{R}^2$ as

$$
  \begin{array}{rcl}
    R_\alpha(\mathbf{j})
    &\equiv&
    \big(
      \cos(\alpha/2) + \sin(\alpha/2)\mathbf{i}
    \big)
    \,
    \mathbf{j}
    \,
    \big(
      \cos(\alpha/2) - \sin(\alpha/2)\mathbf{i}
    \big)
    \\
    &=&
    \big(
      \cos(\alpha/2)^2 - \sin(\alpha/2)^2
    \big)
    \,
    \mathbf{j}
    +
    \big( 
      2 \sin(\alpha/2) \cos(\alpha/2)
    \big)
    \,
    \mathbf{k} 
    \\
    &=&
    \cos(\alpha) \, \mathbf{j}
    +
    \sin(\alpha) \, \mathbf{k}
  \end{array}
$$

(in the last line we used the [sum-of-angles](trigonometric+identity#eq:SumOfAnglesFormulas) [[trigonometric identities]]) 

and in addition the **[[reflection at a hyperplane|reflection]]** operator $I_y \coloneqq Ad_{\mathbf{j}}$ acting as

$$
  I_y \mathbf{j}
  \;=\;
  \mathbf{j} \, \mathbf{j} \, (- \mathbf{j})
  \;=\;
  \mathbf{j}
$$

$$
  I_y \mathbf{k}
  \;=\;
  \mathbf{j} \, \mathbf{k} \, (- \mathbf{j})
  \;=\;
  -
  \mathbf{k}
$$

(hence *inverting the y-axis*).

Together these clearly generate the group [[O(2)]]. Since the [[conjugation action]] assignment 

$$
  \begin{array}{ccc}
    Pin_-(2) &\longrightarrow& O(2)
    \\
    g &\mapsto& Ad_g
  \end{array}
$$

has [[kernel]] $\{\pm 1\} \in Pin_-(2)$, this exhibits $Pin_-(2)$ as the [[double cover]] of [[O(2)]].

To note here that under the inclusion $Pin_-(2) \hookrightarrow Spin(3)$ (eq:InclusionIntoSpin3), the above inversion of the $y$ axis in 2D corresponds to *rotation around the x-axis*, in 3D!


### Appearance in Seiberg-Witten theory and Floer homology

On a [[spin structure|spin]] [[4-manifold]], the $U(1)$-symmetry of the [[Seiberg-Witten equations]] enhances to a $Pin(2)$-symmetry ([Furuta 01](#Furuta01)). Because of this, $Pin(2)$-equivariance appears in [[Seiberg-Witten theory]] and [[Floer homology]]. See the references below.



## Related concepts

[[!include low dimensional rotation groups -- table]]


## References

$Pin(2)$-[[equivariant homotopy theory]]/[[equivariant cohomology theory]] 

application to [[Seiberg-Witten theory]] and [[Floer homology]]:

* {#Furuta01} Mikio Furuta, [_Monopole equation and the $11/8$-conjecture_](https://www.intlpress.com/site/pub/files/_fulltext/journals/mrl/2001/0008/0003/MRL-2001-0008-0003-a005.pdf) Mathematical Research Letters, Volume 8, Number 3, (2001).

* Ciprian Manolescu, _$Pin(2)$-equivariant Seiberg-Witten Floer homology and the Triangulation Conjecture_ ([arXiv:1303.2354](https://arxiv.org/abs/1303.2354))

* Matthew Stoffregen, _$Pin(2)$-equivariant Seiberg-Witten Floer homology of Seifert fibrations_ ([arXiv:1505.03234](https://arxiv.org/abs/1505.03234))

* Matthew Stoffregen, _A Remark on $Pin(2)$-Equivariant Floer Homology_,     Michigan Math. J. Volume 66, Issue 4 (2017), 867-884 ([euclid:1508810818](https://projecteuclid.org/euclid.mmj/1508810818))

$Pin(2)$-[[equivariant K-theory|equivariant]] [[KO-theory]]:

* Jianfeng Lin, _Pin(2)-equivariant KO-theory and intersection forms of spin four-manifolds_, Algebr. Geom. Topol. 15 (2015) 863-902 ([arXiv:1401.3264](https://arxiv.org/abs/1401.3264))


[[!redirects Pin(2)-group]]
[[!redirects Pin(2) group]]

[[!redirects pin(2)]]
[[!redirects pin(2)-group]]
[[!redirects pin(2) group]]

[[!redirects Pin2]]

 