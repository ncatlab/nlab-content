
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of conntents
{:toc}

## Idea

$Spec(\mathbb{Z})$ denotes the [[spectrum of a commutative ring|spectrum]] of the [[commutative ring]] $\mathbb{Z}$ of [[integers]]. Its [[underlying]] [[topological space]] has the [[prime ideals]] of $\mathbb{Z}$ as points, carrying the [[Zariski topology]]. The [[closed points]] are the [[maximal ideals]] $(p)$, for each [[prime number]] $p$ in $\mathbb{Z}$; the non-maximal [[prime ideal]] $(0)$ is a [[generic point]] and has as [[topological closure|closure]] the whole of $Spec(\mathbb{Z})$. 
A [[subset]] of $Spec(\mathbb{Z})$ is [[closed subset|closed]] if and only if it is all of $Spec(\mathbb{Z})$ or consists of finitely many points of the form $(p)$ with $p$ prime.

As a [[ringed space]], $Spec(\mathbb{Z})$ carries a [[structure sheaf]] $\mathcal{O}$ which is a [[sheaf]] of [[commutative rings]] on the space $Spec(\mathbb{Z})$. Given a typical [[open set]]
$$ 
  U = Spec(\mathbb{Z})\setminus \{(p_1),\ldots,(p_n)\}
$$
we have
$$
  \mathcal{O}(U) = \left\{
\frac{a}{b}\in\mathbb{Q}\mid a,b\in\mathbb{Z}\ \text{and all primes dividing}\ b\ \text{are among}\ p_1,\ldots,p_n
\right\}.
$$
The restriction morphisms are the natural inclusions. 

The [[stalk]] at the point $(p)$ is the local ring $\mathbb{Z}_{(p)}=\left\{\frac{a}{b}\in\mathbb{Q}\mid a\in\mathbb{Z},\  b\in\mathbb{Z}\setminus (p)\right\}$ with [[residue field]] $\mathbb{F}_p$. The stalk at $(0)$ is $\mathbb{Q}$.

Since $\mathbb{Z}$ is the [[initial object]] in the [[category]] [[CRing]] of [[commutative rings]], $Spec(\mathbb{Z})$ is the [[terminal object]] in the [[category]] of [[affine schemes]], hence also among all [[schemes]]).

The [[functor of points]] corresponding to $Spec(\mathbb{Z})$ is the [[constant functor]] that assigns a [[singleton]] to every [[commutative ring]]. (see *[[functorial geometry]]*).

The [[gros topos|gros]] [[etale topos]] over $Spec(\mathbb{Z})$ is the context for [[arithmetic geometry]]. By the discussion at _[[Borger's absolute geometry]]_ it sits via an [[essential geometric morphism]] over the [[F1|$\mathbb{F}_1$]]-[[topos]]:

$$
  Et\big(Spec(\mathbb{Z})\big)\longrightarrow Et\big(Spec(\mathbb{F}_1)\big)
  \mathrlap{\,.}
$$

## Properties

There are some phenomena that may be interpreted as $Spec(\mathbb{Z})$ behaving like a [[3-manifold]] in some ways.

#### As a 3-sphere containing knots
 {#As3dSpaceContainingKnots}

Several properties of $Spec(\mathbb{Z})$ make it behave as if of [[dimension]] 3. For instance $Spec(\mathbb{Z}) \cup \{\infty\}$ has [[étale cohomology|étale]] [[cohomological dimension]] equal to 3, up to 2-torsion ([Mazur 73](#Mazur73)). Moreover the [[étale fundamental group]] $\hat \pi_1(Spec(\mathbb{Z}) \cup \{\infty\})$ is trivial, and hence Mazur suggested that $Spec(\mathbb{Z}) \cup \{\infty\}$ is in fact analogous to the [[3-sphere]].

Similarly, the spectra $Spec(\mathbb{F}_q)$ of [[finite fields]]  look like compact 1-dimensional spaces -- [[circles]] -- in that their [[étale cohomology]] with $\mathbb{Z}_l$-[[coefficients]] for $l$ coprime to $q$ is $\mathbb{Z}_l$ in degrees 0 and 1 and vanishes in all higher degrees.

From this it is [[folklore]] (going back to [Mazur](#Mazur) and Manin, review includes [Deninger 05, section 8](#Deninger05), [Kohno-Morishita 06](#KohnoMorishita06)) that the spectra of [[prime fields]] with their canonical embedding into $Spec(\mathbb{Z})$

$$
  Spec(\mathbb{F}_p) \hookrightarrow Spec(\mathbb{Z})
$$

(formally dual to the canonical mod-$p$ [[projection]] $\mathbb{Z}\to \mathbb{F}_p$) are analogous to [[knots]] inside this 3-dimensional space (a good exposition is in [LeBruyn](#LeBruyn10)). 

Observations like this give rise to the field of [[arithmetic topology]].

#### As a hyperbolic 3-manifold containing prime geodesics

However, in view of the [analogy between the Selberg zeta function and the Artin L-function](Selberg%20zeta%20function#AnalogyWithArtinLFunction) it might be more appropriate to think of $Spec(\mathbb{Z})$ as analogous to a  [[hyperbolic manifold]] of dimension 3 (see also [Fujiwara 07, slide 7](#Fujiwara07)) and then to think of finite field spectra as analogous to the [[prime geodesics]] in the manifold. This does not change the fact that every single $Spec(\mathbb{F}_p) \hookrightarrow Spec(\mathbb{Z})$ is like an embedded circle, hence like a knot, but it affects the perspective on which role these play. For instance there does not seem to be a differential geometric analog situation where one considers [[infinite products]] over all knots in a 3-space, but there are such situations where one considers infinite products over all [[prime geodesics]] in a space, namely the [[Selberg zeta function]] analogous to the [[Artin L-function]] with its product over [[prime ideals]].




### Function field analogy


[[!include function field analogy -- table]]

[[!redirects Et(Spec(Z))]]


## Related concepts

* [[Spec(S)]]

* [[field with one element]]

## References

* {#Mazur73} [[Barry Mazur]], _Notes on &#233;tale cohomology of number fields_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 6 no. 4 (1973), p. 521-552 ([NUMDAM](http://www.numdam.org/numdam-bin/fitem?id=ASENS_1973_4_6_4_521_0))

* {#Mazur} [[Barry Mazur]], _Remarks on the Alexander polynomial_, unpublished note

* {#Deninger05} [[Christopher Deninger]], _Arithmetic Geometry and Analysis on Foliated Spaces_ ([arXiv:math/0505354](http://arxiv.org/abs/math/0505354))

* {#KohnoMorishita06} [[Toshitake Kohno]], [[Masanori Morishita]] (eds.), _Primes and Knots_, Contemporary Mathematics, AMS 2006 ([web](http://www.ams.org/bookstore-getitem/item=CONM-416))

* {#LeBruyn10} [[Lieven LeBruyn]], talk 2010 ([pdf slides](http://win.ua.ac.be/~lebruyn/LeBruyn2010d.pdf) (35 mb), [MO comment](http://mathoverflow.net/a/50995/381) (with more details))

* {#Fujiwara07} K. Fujiwara, _$p$-adic gauge theory in number theory_, 2007 ([pdf slides](http://www.ms.u-tokyo.ac.jp/~t-saito/conf/rv/Leopoldt.pdf))

* [[Bertrand Toën]], [[Michel Vaquié]], *Au-dessous de $Spec \mathbb{Z}$*, Journal of K-Theory **3** 3 (2009) 437-500 &lbrack;[doi:10.1017/is008004027jkt048](https://doi.org/10.1017/is008004027jkt048)&rbrack;


[[!redirects Spec Z]]
