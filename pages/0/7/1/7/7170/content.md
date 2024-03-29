
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Wu classes_ are a type of [[universal characteristic class]] in $\mathbb{Z}_2$-[[cohomology]] that refine the [[Stiefel-Whitney classes]].

## Definition

For $X$ a [[topological space]] equipped with a class $E : X  \to B SO(n)$ (a real [[vector bundle]] of some [[rank]] $n$), write

$$
  w_k \in H^k(X, \mathbb{Z}_2)
$$ 

for the [[Stiefel-Whitney classes]] of $X$. Moreover, write

$$
  \cup : H^k(X, \mathbb{Z}_2) \times H^l(X, \mathbb{Z}_2)
  \to 
  H^{k+l}(X, \mathbb{Z}_2)
$$

for the [[cup product]] on $\mathbb{Z}_2$-[[cohomology groups]] and write 

$$
  Sq^k(-) : H^l(X, \mathbb{Z}_2) \to H^{k+l}(X, \mathbb{Z}_2)
$$

for the [[Steenrod square]] operations.

+-- {: .num_defn #WuClassesBySteenrodSquares}
###### Definition

The **Wu class** 

$$
  \nu_k
  \in 
  H^k(X,\mathbb{Z}_2)
$$ 

is defined to be the class that "represents" $Sq^k(-)$ under the cup product, in the sense that for all $x \in H^{n-k}(X, \mathbb{Z}_2)$ where $n$ is the dimension of $X$, we have

$$
  Sq^k(x) = \nu_k \cup x
  \,.
$$

=--

(e.g. [Milnor-Stasheff 74, p. 131-133](#MilnorStasheff74))


+-- {: .num_remark }
###### Remark

In other words this says that the lifts of Wu classes to [[integral cohomology]] ([[integral Wu structures]]) are _[[characteristic element of a bilinear form|characteristic elements]]_ of the [[intersection product]] on integral cohomology, inducing [[quadratic refinements]].

=--

## Properties

### Relation to Stiefel-Whitney classes

The total [[Stiefel-Whitney class]] $w$ is the total [[Steenrod square]] of the total Wu class $\nu$.

$$
  w = Sq(\nu)
  \,.
$$

Solving this for the components of $\nu$ in terms of the components of $w$, one finds the first few Wu classes as [[polynomials]] in the Stiefel-Whitney classes as follows

* $\nu_1 = w_1$;

* $\nu_2 = w_2 + w_1^2$

* $\nu_3 = w_1 w_2$

* $\nu_4 = w_4 + w_3 w_1 + w_2^2 + w_1^4$

* $\nu_5 = w_4 w_1 + w_3 w_1^2 + w_2^2 w_1 + w_2 w_1^3$ 

...

### Relation to Pontryagin classes
 {#RelationToPontryaginClasses}

+-- {: .num_prop #InTermsOfPontryagin}
###### Proposition

Let $X$ be an [[orientation|oriented]] [[manifold]] $T X : X \to  B SO(n)$ with [[spin structure]] $\hat T X : X \to B Spin(n)$. Then the following classes in [[integral cohomology]] of $X$, built from [[Pontryagin classes]], coincide with Wu-classes under mod-2-reduction $\mathbb{Z} \to \mathbb{Z}_2$:

* $\nu_4 = \frac{1}{2} p_1$

* $\nu_8 = \frac{1}{8}(11 p_1^2  - 20 p_2)$

* $\nu_{12} = \frac{1}{16}(37 p_1^3 - 100 p_1 p_2 + 80 p_3)$.

(all products are [[cup product|cup products]]).

=--

This is discussed in ([Hopkins-Singer, page 101](#HopkinsSinger)).

+-- {: .num_cor #DivisibilityOfCupSquare}
###### Corollary

Suppose $X$ is 8 dimensional. Then, for $G \in H^4(X, \mathbb{Z})$ any integral 4-class, the expression

$$
  G \cup G - G \cup \frac{1}{2}p_1 \in H^4(X, \mathbb{Z})
$$

is always even (divisible by 2).

=--

+-- {: .proof}
###### Proof

By the basic properties of Steenrod squares, we have for the 4-class $G$ that 

$$
  G \cup G = Sq^4(G)
  \,.
$$

By the definition \ref{WuClassesBySteenrodSquares} of Wu classes, the image of this integral class in $\mathbb{Z}_2$-coefficients equals the cup product with the Wu class

$$
  G \cup G - G \cup \frac{1}{2}p_1
  = 
  Sq^4(G) - G \cup \nu_4
  = 
  0 \; mod \; 2.
  \,,
$$

where the first step is by prop. \ref{InTermsOfPontryagin}.

=--

## Applications

### To higher dimensional Chern-Simons theory

+-- {: .num_remark}
###### Remark

The relation \ref{DivisibilityOfCupSquare} plays a central role in the definition of the [[higher dimensional Chern-Simons theory|7-dimensional Chern-Simons theory]] which is [[holographic principle|dual]] to the [[self-dual higher gauge theory]] on the [[M5-brane]]. In this context it was first pointed out in ([Witten 1996](#Witten)) and later elaborated on in ([Hopkins-Singer](#HopkinsSinger)).

Specifically, in this context $G$ is the 4-class of the [[circle n-bundle with connection|circle 3-bundle]] underlying the [[supergravity C-field]], subject to the quantization condition

$$
  G_4 = \frac{1}{2}(\frac{1}{2}p_1) + a
  \,,
$$

for some $a \in H^4(X, \mathbb{Z})$, which makes direct sense as an equation in $H^4(X, \mathbb{Z})$ if the [[spin structure]] on $X$ happens to be such $\frac{1}{2}p_1$ is further divisible by 2, and can be made sense of more generally in terms of [[twisted cohomology]] (which was suggested in ([Witten 1996](#Witten)) and made precise sense of in ([Hopkins-Singer](#HopkinsSinger)) ). 

For simplicity, assume that $\frac{1}{2}p_1$ of $X$ is further divisible by 2 in the following. We then may consider direct refinements of the above ingredients to [[ordinary differential cohomology]] and so we consider [[circle n-bundle with connection|differential cocycles]] $\hat a, \hat G \in \hat H^4(X)$ with

\[
  \hat G = \frac{1}{2}(\frac{1}{2}\hat \mathbf{p}_1) + \hat a
  \in \hat H^4(X)
  \,,
  \label{DifferentialQuantizationCondition}
\]

where the differential refinement $\frac{1}{2}\hat \mathbf{p}_1$ is discussed in detail at _[[differential string structure]]_.

Now, after [[Kaluza-Klein mechanism|dimensional reduction]] on a 4-[[sphere]], the [[action functional]] of [[11-dimensional supergravity]] on the remaining 7-dimensional $X$ contains a [[higher dimensional Chern-Simons theory|higher Chern-Simons term]] which up to prefactors is of the form

$$
  \hat G \mapsto 
  \exp i 
  \int_X 
    (
      \hat G \cup \hat G - 
      (\frac{1}{4}\hat \mathbf{p}_1)^2
    )
  \,,
$$

where 

* the cup product now is the differential [[Beilinson-Deligne cup product]] refinement of the integral cup product;

* the symbol $\exp(i \int_X (-))$ denotes [[fiber integration in ordinary differential cohomology]].

Using (eq:DifferentialQuantizationCondition) this is 

$$
  \cdots
   = 
  \exp i 
  \int_X 
  \left(
    \hat a \cup \hat a + \hat a \cup \frac{1}{2}\hat \mathbf{p}_1
  \right)
  \,.
$$

But by corollary \ref{DivisibilityOfCupSquare} this is further divisible by 2.
Hence the generator of the group of higher Chern-Simons action functionals is one half of this

$$
  \hat G 
   \mapsto 
  \exp i 
  \int_X 
   \frac{1}{2}
    (
      \hat G \cup \hat G - 
      (\frac{1}{4}\hat \mathbf{p}_1)^2
    )
  \,.
$$

In ([Witten 1996](#Witten)) it is discussed that the space of [[states]] of this "fractional" functional over a 6-dimensional $\Sigma$ is the space of [[conformal blocks]] of the [[self-dual higher gauge theory]] on the [[M5-brane]].

=--

## Related concepts

* [[integral Wu structure]], [[twisted Wu structure]]

* [[shifted C-field flux quantization]]

* [[Pontryagin class]], [[Stiefel-Whitney class]], [[one-loop anomaly polynomial I8]]

* [[Euler class]]

## References

The original reference is 

* [[Wen-Tsun Wu]], _On Pontrjagin classes: II_ Sientia Sinica 4 (1955) 455-490

See also around p. 228 of

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton University Press (1974)

and section 2 of 

* Yanghyun Byun, _On vanishing of characteristic numbers in Poincar&#233; complexes_, Transactions of the AMS, vol 348, number 8 (1996) ([pdf](http://www.ams.org/journals/tran/1996-348-08/S0002-9947-96-01495-X/S0002-9947-96-01495-X.pdf))

and

* [[Robert Stong]], Toshio Yoshida, _Wu classes_ Proceedings of the American Mathematical Society  Vol. 100, No. 2, (1987)  ([JSTOR](http://www.jstor.org/pss/2045970))

Details are reviewed in appendix E of

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_
 {#HopkinsSinger}

This is based on or motivated from observations in 

* [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 {#Witten}

More discussion of Wu classes in this physical context is in 

* [[Hisham Sati]], _Twisted topological structures related to M-branes II: Twisted $Wu$ and $Wu^c$ structures_ ([arXiv:1109.4461](http://arxiv.org/abs/1109.4461))

which also summarizes many standard properties of Wu classes.

[[!redirects Wu classes]]