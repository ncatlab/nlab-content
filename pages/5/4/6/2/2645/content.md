
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Chern-Weil theory studies the refinement of [[characteristic class]]es of [[principal bundle]]s in ordinary [[cohomology]] to [[de Rham cohomology]] and further to [[ordinary differential cohomology]]. 

The central operation that models this refinement is the construction of the [[Chern-Weil homomorphism]] from $G$-[[principal bundle]]s to [[de Rham cohomology]] by choosing a [[connection on a bundle|connection]] $\nabla$ and evaluating its [[curvature]] form $F_\nabla$ in the [[invariant polynomial]]s $\langle -\rangle$ of the [[Lie algebra]] $\mathfrak{g}$ to produce the [[curvature characteristic form]] $\langle F_\nabla \rangle$. Its de Rham cohomology class refines a corresponding [[characteristic class]] in [[integral cohomology]]. 

Concretely, the [[Chern-Weil homomorphism]] is presented by the following construction:

For 

* $B G \in$ [[Top]] the [[classifying space]] of (the [[topological group]] underlying) a [[compact space|compact]] [[Lie group]] $G$ 

* and $[c] \in H^n(B G, \mathbb{Z})$ a class in its [[integral cohomology]] -- which we may call a _[[characteristic class]]_ for $G$-[[principal bundles]]

we get for each [[smooth manifold]] $X$  an assignment

$$
  [c] : G Bund(X)_\sim \to H^n(X,\mathbb{Z})
$$

on integral cohomology classes of base space to equivalence classes of $G$-[[principal bundle]]s by sending a bundle classified by a map $f : X \to B G$ to the class $[f^* c]$.

Let $[c]_\mathbb{R} \in H^n(B G, \mathbb{R})$ be the image of $[c]$ in [[real cohomology]], induced by the evident inclusion of [[coefficients]] $\mathbb{Z} \hookrightarrow \mathbb{R}$.

The **first main statement** of Chern-Weil theory is that there is an [[invariant polynomial]] 

$$
  \langle- \rangle :=  \phi^{-1} [c]_{\mathbb{R}}
$$ 

on the [[Lie algebra]] $\mathfrak{g}$ of $G$ associated to $[c]_{\mathbb{R}}$, given by an [[isomorphism]] (of real [[graded vector space]])s

$$
  \phi 
  \;\colon\;
   inv(\mathfrak{g}) 
   \overset{\simeq}{\longrightarrow}
   H^\bullet(B G, \mathbb{R})
  \,.
$$

The **second main statement** is that this invariant polynomial serves to provide a _differential_ ([[Lie integration]]) construction of $[c]_{\mathbb{R}}$:

for any choice of [[connection on a bundle|connection]] $\nabla$ on a $G$-principal bundle $P \to X$ we have the [[curvature]] 2-form $F_\nabla \in \Omega^2(P, \mathfrak{g})$ and fed into the invariant polynomial this yields an $n$-form

$$
 \langle F_\nabla \wedge \cdots \wedge F_\nabla \rangle
  \in
  \Omega^n(X)
  \,.
$$

The statement is that under the [[de Rham theorem]]-isomorphism $H^\bullet_{dR}(X) \simeq H^\bullet(X, \mathbb{R})$ this presents the class $[c]_{\mathbb{R}}$. 

The **third main statement**, says that this construction may be refined by combining [[integral cohomology]] and [[de Rham cohomology]] to [[ordinary differential cohomology]]: the $n$-form $\langle F_\nabla \wedge \cdots F_\nabla\rangle$ may be realized itself as the [[curvature]] $n$-form of a [[circle n-bundle with connection]] $\hat \mathbf{c}$. 

$$
  [\hat \mathbf{c}] : 
  G Bund_\nabla(X)_\sim
   \to
  U(1) n Bund_\nabla(X)_\sim
   \simeq H^n_{diff}(X)
  \,.
$$


In summary this yields the following picture:

$$
  \array{
    && [\hat \mathbf{c}]
    \\
    & \swarrow && \searrow
    \\
    [c] && && [\langle F_\nabla \wedge \cdots F_\nabla\rangle]
    \\
    & \searrow && \swarrow
    \\ 
    && [c]_{\mathbb{R}}
  }
  \;\;\;\;\;\;\;\;\;
   \in
  \;\;\;\;\;\;\;\;\;
  \array{
    && H_{diff}^n(X)
    \\
    & \swarrow && \searrow
    \\
    H^n(X,\mathbb{Z}) && && H_{dR}^n(X)
    \\
    & \searrow && \swarrow
    \\ 
    && H^n(X, \mathbb{R})
  }
  \,.
$$

A central **implication** of the last step is that with the refinement from [[curvatures]] in [[de Rham cohomology]] to [[circle n-bundles with connection]] in [[differential cohomology]] is that these come with a notion of [[higher parallel transport]] and higher [[holonomy]]:

* the local connection form of $\hat \mathbf{c}$ is the [[Chern-Simons form]] $cs(\nabla)$ of a [[Chern-Simons element]] $cs$ of the [[invariant polynomial]] $\langle- \rangle$ evaluated on the given $G$-[[connection on a bundle|connection]];

* the corresponding [[higher parallel transport]] as an assignment

  $$
    (\Sigma \stackrel{\phi}{\to} X) 
    \mapsto 
    \exp\Big(
      \textstyle{\int_\Sigma} 
      \nabla_{\hat \mathbf{c}}
    \Big)
    \in U(1)
  $$

  of $(n-1)$-[[dimensional]] manifolds in $X$ to the [[circle group]] is the [[action functional]] of the corresponding [[Chern-Simons theory]].

Specifically 

* for $\langle  -,-\rangle$ the [[Killing form]] invariant polynomial on a [[semisimple Lie algebra]], one calls $\hat \mathbf{c}$ the [[Chern-Simons circle 3-bundle]]; whose higher [[holonomy]] is the [[action functional]] of ordinary [[Chern-Simons theory]];

* for $\langle -,-,-,-\rangle$ the next higher invariant polynomial on a semisimple Lie algebra, $\hat \mathbf{c}$ is a [[Chern-Simons circle 7-bundle]], and so on.

So the refined Chern-Weil homomorphism provides a large family of [[gauge theory|gauge]] [[quantum field theories]] of Chern-Simons type in odd [[dimension]]s whose field configurations are always [[connection on a bundle|connections]] on [[principal bundle]]s and whose [[Lagrangians]] are [Chern-Simons element]]s on a [[Lie algebra]].

But the notion of [[invariant polynomial]]s and [[Chern-Simons element]]s naturally exists much more generally for [[L-∞ algebras]], and even more generally for [[L-∞ algebroid]]s. We claim here that in this fully general case there is still a natural analog of the Chern-Weil homomorphism -- which we call the _[[∞-Chern-Weil homomorphism]]_ . Accordingly this gives rise to a wide class of [[action functional]]s for [[gauge theory|gauge]] [[quantum field theories]], which may be called _[[schreiber:∞-Chern-Simons theories]]_.


## Generalizations

### To principal $\infty$-bundles

The notions of [[Lie group]], [[Lie algebra]], [[principal bundle]] and all the other ingredients of ordinary Chern-Weil theory generalize to notions in [[higher category theory]] such as  [[∞-Lie group]], [[∞-Lie algebra]], [[principal ∞-bundle]] etc. The generalization of Chern-Weil theory to this context is discussed at 

* [[∞-Chern-Weil theory]].

### In noncommutative geometry

There is a [[noncommutative geometry|noncommutative]] analogue discussed in ([AlekseevMeinrenken2000](#AlekseevMeinrenken)).


## Examples and applications

* [[de Rham theorem]]

* [[Gauss-Bonnet theorem]]

* [[differential string structure]]

* [[differential fivebrane structure]]


## History {#History}

> (following notes provided by [[Jim Stasheff]])

The beginnings of the [[rational homotopy theory]] of [[Lie group]]s $G$ and hence their [[dg-algebra]]-description in terms of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ originate in the first half of the 20th century.

In his survey of what was known in 1936 on the homology of compact Lie groups 

* [[Eli Cartan]], _La topologie des espaces repr&#233;sentatifs des groupes de Lie_ Act. Sci. Ind., No. 358, Hermann, Paris, (1936).

  reprinted in _Cartan's Complete Works_ vol $I_2$ pp. 1307-1330

E. Cartan conjectured that there should be a general result implying that the [[homology]] of the [[classical Lie group]]s is the same as the homology of a product of odd-dimensional [[sphere]]s. In particular, he lists the [[Poincare polynomial]]s for classical simple compact Lie groups.

In

* [[Heinz Hopf]],  _&#220;ber die Topologie der Gruppen-Mannigfaltigkeiten und ihre Verallgemeinerungen_  (German)  Ann. of Math. (2)  42,  (1941). 22--52.

Hopf showed that such a characterization in terms of homology groups as [[intersection pairing]] algebras holds for any [[compact space|compact]] [[dimension|finite dimensional]] [[connected]] [[orientable]] [[manifold]] with a map $m:M\times M\to M$ such that left and right translation have non-zero degrees.

Later in

* [[Shiing-shen Chern]], _Differential geometry of fiber bundles_ Proceedings of the International Congress of Mathematicians, Cambridge, Mass., 1950, vol. 2, pages 397-411,  Amer. Math. Soc., Providence, R. I. (1952)

with the development of [[cohomology]], especially [[de Rham cohomology]], this was stated as $H^\bullet(G)$ being [[isomorphic]] to  an [[exterior algebra]] on odd dimensional generators: the generating [[Lie algebra cohomology]] [[cocycle]]s $\mu \in CE(\mathfrak{g})$, $d_{CE(\mathfrak{g})} \mu = 0$.

Henri Cartan in

* [[Henri Cartan]], _Notions d'alg&#233;bre diff&#233;rentielle; applications aux groupes de Lie et aux vari&#233;t&#233;s o&#249; op&#232;re un groupe de Lie_ ,  Coll. Topologie Alg&#233;brique Bruxelles (1950)
15-28

  section 7, titled _Classes caracteristiques (reelles) d'un espace fibre principal_

at the end (1951) of an era of deRham cohomology dominence (prior to Serre's thesis) abstracted the [[differential geometry|differential geometric]] approach of Chern-Weil and the [[Weil algebra]] $W(\mathfrak{g})$ to the [[dg-algebra]] context with his notion of _$\mathfrak{g}$-algebras $A$_ . This involves what is known sometimes as the [[Cartan calculus]].  In addition to the differential $d$ of [[differential form]]s on a [[principal bundle]], Cartan abstracts the inner product aka contraction of differential forms with [[vector field]]s $X$ and the [[Lie derivative]] $\mathcal{L}_X$ with respect to vector fields.  that is, he posits 3 operators on a differential-graded-commutative alggebra (dgca):

$d$ of degree 1, $i_X$ of degree -1 and $L_X$ of degree 0 for X in $\mathfrak{g}$ subject to the relations:

* $[\iota_X,\iota_Y] = \iota_{[X,Y]}$

* $ [\mathcal{L}_X,\iota_Y]= \iota_{[X,Y]} $

and perhaps most useful

* $\mathcal{L}_X = d \iota_X + i\iota_X d$

This is what he terms a $\mathfrak{g}$-algebra.

For Cartan, an infinitesimal [[connection on a bundle|connection]] on a [[principal bundle]] $P \to X$ are  projectors (at each point $p$ of $P$) $\phi_p: T_p P\to T_p^{vert}$ equivariant with repect to the $G$-action. 
This can be abstracted to a morphism

$$
  \Omega^\bullet(P) \leftarrow \mathfrak{g}^* : A
$$

of [[graded vector space]]s of degree 1 -- equivalently a [[Lie-algebra valued 1-form]] $A \in \Omega^1(P,\mathfrak{g})$ -- such that the two [[Ehresmann connection|Ehresmann condition]]s hold: 

1. restricted to the fibers the 1-form $A$ is the [[Maurer-Cartan form]]

   $\iota_X A(h) = \iota_X h$

1. the form is equivariant in that 

   $\mathcal{L}_X A (h) = A(\mathcal{L}_X h)$

  for all $X\in \mathfrak{g}$ and $h\in \mathfrak{g}^*$.  This data Cartan calls an _algebraic connection_ .

He then extends such an $A$ to a [[homomorphism]] of [[graded algebra]]s 

$$
  \Omega^\bullet(P) \leftarrow CE(\mathfrak{g}) : A
$$

from the [[Chevalley-Eilenberg algebra]] $\wedge^\bullet \mathfrak{g}^*$.

In general, this will not respect the differentials, hence not be a morphism of [[dg-algebra]]s. In fact, the deviation gives the [[curvature]] of the connection: the curvature tensor is the map $h\mapsto d_{dR} A(h)-A(d_{CE} h)$.

> Jim: HAVE TO BREAK OFF NOW - WHAT WILL COME NEXT IS the [[Weil algebra]] $W(\mathfrak{g})$ as a Cartan $\mathfrak{g}$-algebra


* Weil, _Geometrie differentielle des espaces fibres_ (1949, unpublished)
  appears in Vol. 1, pp. 422-436, of his Collected Papers.

## Related concepts

* [[Sullivan model of classifying space]]

* [[Chern-Weil homomorphism]]


## References

[[!include Chern-Weil homomorphism -- references]]


More review:

* [[Fei Han]], _Chern-Weil theory and some results on classic genera_ ([pdf](http://math.berkeley.edu/~alanw/240papers03/han.pdf))


More monographs:

* [[Johan Louis Dupont]], _Fibre bundles and Chern-Weil theory_, Lecture Notes Series __69__, Dept. of Math., University of Aarhus, Aarhus, 2003, 115 pp. [pdf](http://www.johno.dk/mathematics/fiberbundlestryk.pdf)

* [[Johan Louis Dupont]], _Curvature and characteristic classes_, Lecture Notes in Math. __640__, Springer-Verlag, Berlin-Heidelberg-New York, 1978. 

* [[Mikhail Postnikov]], _&#1051;&#1077;&#1082;&#1094;&#1080;&#1080; &#1087;&#1086; &#1075;&#1077;&#1086;&#1084;&#1077;&#1090;&#1088;&#1080;&#1080;. &#1057;&#1077;&#1084;&#1077;&#1089;&#1090;&#1088; 4, &#1044;&#1080;&#1092;&#1092;&#1077;&#1088;&#1077;&#1085;&#1094;&#1080;&#1072;&#1083;&#1100;&#1085;&#1072;&#1103; &#1075;&#1077;&#1086;&#1084;&#1077;&#1090;&#1088;&#1080;&#1103;_ &#8212; &#1052;.: &#1053;&#1072;&#1091;&#1082;&#1072;, 1988	

* [[Raoul Bott]], [[Loring Tu]], _Differential forms in algebraic topology_, Graduate Texts in Mathematics __82__, Springer 1982. xiv+331 pp.

* [[Loring Tu]], _Differential Geometry -- Connections, Curvature, and Characteristic Classes_, Springer (2017) &lbrack;[ISBN:978-3-319-55082-4](https://www.springer.com/gp/book/9783319550824)&rbrack;

* [[Victor Guillemin]], [[Shlomo Sternberg]], _Supersymmetry and equivariant de Rham theory_, Springer, 1999.

Lecture notes with an eye on [[Morse theory]] in terms of [[supersymmetric quantum mechanics]]:

* [[Weiping Zhang]], _Lectures on Chern-Weil theory and Witten deformations_ , Nankai Tracts in Mathematics - Vol. 4  ([web](http://www.worldscibooks.com/mathematics/4756.html))

Chern-Weil theory in the context of [[noncommutative geometry]]

* {#AlekseevMeinrenken} [[Anton Alekseev]], [[Eckhard Meinrenken]], _The non-commutative Weil algebra_, Invent. Math. **139** 1 (2000) 135-172 &lbrack;[doi:10.1007/s002229900025](http://dx.doi.org/10.1007/s002229900025)&rbrack;
 
[[!redirects Chern-Weil theorem]]
[[!redirects Chern-Weil theorems]]

