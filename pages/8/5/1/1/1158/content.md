#Idea#

Smooth Deligne cohomology in degree $n$, 
denoted $\bar H^n(X,\mathbb{Z}) = H(X, \mathbb{Z}(n)^\infty,D)$,
of a smooth manifold $X$
is a realization of the 
[[differential cohomology|differential refinement]] $\bar H^n(X,\mathbb{Z})$ of the 
[[integral cohomology]] $H^n(X, \mathbb{Z})$ of $X$ in terms of
[[abelian sheaf cohomology]].

[[differential cohomology|Recall]] 
that analgous to how $H^n(X,\mathbb{Z})$ classifies line $(n-1)$-bundles 
and equivalently line $(n-2)$-gerbes on $X$, $\bar H^n(X, \mathbb{Z})$
classifies line $(n-2)$-gerbes with connection.

Accordingly, the _Deligne complex_ of sheaves $\mathbb{Z}(n)^\infty_D$
is a complex of sheaves of differential forms.

#Definition#

For $k \in \mathbb{N}$
write $\Omega^k(X)$ for the [[sheaf] of smooth differential $k$-forms on $X$
and $C^\infty(X,U(1))$ for the sheaf of smooth $U(1)$-valued functions on 
$X$. Let $C^\infty(X,U(1)) \stackrel{d log}{\to} \Omega^1(X)$ be the 
morphism of sheaves induced by regarding a $U(1) \simeq \mathbb{R}/\mathbb{Z}$-valued function locally
as a $\mathbb{R}$-valued function and applying the deRham differential $d$ to that.

This yields for each $n \in \mathbb{N}$ a complex of sheaves

$$
  \cdots \to 0 \to C^\infty(X,U(1)) \stackrel{d log}{\to}
    \Omega^1(X) \stackrel{d}{\to} \cdots \stackrel{d}{\to}
    \Omega^n(X)
$$

with $\Omega^n(X)$ in degree 0 and $C^\infty(X,U(1))$ in degree $n$.

This is ([[quasi-isomorphism|quasi-isomorphic]]) to the 
**Deligned complex** of sheaves, denoted $\mathbb{Z}(n+1)^\infty_D$.

**Deligne cohomology** in degree $n+1$ of $X$ is the 
[[abelian sheaf cohomology]] of this complex.

#Interpretation in terms of parallel transport#

There is a natural way to understand the Deligne complex of sheaves as a sheaf which assigns to each patch the Lie $n$-groupoid of smooth parallel transport $n$-functors. This perspective is helpful for understanding how Deligen cohomology relates to the bigger picture of [[differential cohomology]].

We start by discussing this in low degree.

There is a [[Lie groupoid]] called $P_1(X)$ whose smooth 
space of objects is $X$ and whose smooth space of morphisms is
a space of classes of smooth paths in $X$. 
Every smooth 1-form $A \in \Omega^1(X)$ induces 
a smooth [[functor]] $tra_A : P_1(X) \to \mathbf{B}U(1)$
from $P_1(X)$ to to the smooth [[groupoid]] $\mathbf{B} U(1)$
with one object and $U(1)$ as its smooth space of morphisms
by sending each path $\gamma : [0,1] \to X$
to $\exp (2 \pi i\int_0^1 \gamma^* A)$. This map 
from 1-forms to smooth functors turns out to be bijective:
every smooth functor of this form uniquely arises this way.
Similarly, one finds that smooth [[natural transformation]]
$\eta_f : tra_A \to tra_{A'}$ between two such functors
is in components precisely a 
smooth function $f : X \to U(1)$ such that $A' = A + d log f$.

Since the analogous statements are true for every open subset 
$U \subset X$ this defines a [[sheaf]] of [[Lie groupoid]]s 
$$
  Funct^\infty(P_1(-), \mathbf{B}U(1)) : Op(X)^{op} \to LieGrpd
  \,.
$$
By the [[Dold-Kan correspondence]] this sheaf of groupoids
corresponds to a sheaf of complexes of groups. This complex
of sheaves is nothing but the degree 2 Deligne complex

$$
  Funct^\infty(\Pi_1(-), \mathbf{B}U(1)) \simeq \mathbb{Z}(2)^\infty_D
  \,.
$$
 
This way Deligne cohomology is realized as computing the
[[(infinity,1)-sheafification|stackification]] of the pre-stack
$Funct^\infty(P_1(-), \mathbf{B}(1))$ of smooth $U(1)$-valued 
parallel transport functors.

The identification generalizes: for all $n$ there is a smooth 
[[n-category|n-groupoid]] $P_n(X)$ whose $k$-morphisms are 
$k$-dimensional smooth paths in $X$. Smooth $n$-functors
$tra_C : _n(X) \to \mathbf{B}^n U(1)$ are canonically identified
with smooth $n$-forms $C \in \Omega^n(X)$ and 
under the [[Dold-Kan correspondence]] the Deligne-complex in degree
$n+1$ is identified with the sheaf of $n$-groupoids of such smooth 
$n$-functors
$$
  n Funct^\infty(P_n(-), \mathbf{B}^n)
  \simeq
  \mathbb{Z}(n+1)^\infty_D
  \,.
$$

See

* John Baez, Urs Schreiber, _Higher Gauge Theory_ ([arXiv](http://arxiv.org/abs/math/0511710))

The full proof for $n=1$ this is in

* Urs Schreiber, Konrad Waldorf, _Parallel transport and functors_ ([arXiv](http://arxiv.org/abs/0705.0452));

for $n=2$ in 

* Urs Schreiber, Konrad Waldorf, _Smmoth functors versus differential forms_ ([arXiv](http://arxiv.org/abs/0802.0663))

For more on this see [[schreiber:differential nonabelian cohomology|differential nonabelian cohomology]].

For higher $n$ there is as yet no detailed proof in the literature, but the
low dimensional proofs have obvious generalizations.

---
## Deligne cohomology

Deligne cohomology and homology form a twisted Poincare duality theory in the sense of Bloch and Ogus. See [Jannsen](http://www.math.uni-muenster.de/u/peter.schneider/publ/beilinson-volume/Jannsen.pdf).

category: Properties
---
## Deligne cohomology

Bigraded theory. For $q=0$ we recover singular cohomology.

###Memo notes from reading de Rham: Differentiable manifolds

(NOTE: The "homology" described below is most probably de Rham homology, so perhaps this whole section of notes should be moved)
 
Chapter III: Currents.

Let $V$ be a mfd of dim $n$. A current on $V$ is a linear functional on the vector space of all $C^{\infty}$ forms ("smooth forms") with compact support in $V$. The functional is required to be continuous in a certain sense.

A current $T$ is said to be homogeneous of dimension $p$ and of odd (even) type, if it is zero for each homogeneous form which is not of degree $p$ and even (odd). In this case, the number $n-p$ is called the degree of $T$.

Examples: A chain defines a current. A locally integrable form defines a current.

Def: Support of a current. Note that a current with compact support is defined on the space of all smooth forms. Def: the exterior product of a current and a smooth form.

In the domain of a coordinate system, each current may be represented by a differential form with coeffs which are currents of degree zero.

Def: The integral of a current $T$ is $T[1]$.

Some notation: Write $E^p$ for the space of all $C^p$ forms in $V$ with real coefficients. Write $E$ for $E^{\infty}$. Write $D^p$ and $D$ for the subspaces of forms with compact support. (All these are curly letters in the book.)

Can define the notion of a bounded set in each of these spaces. This is equivalent to defining a topology on the space ("a set $U$ is a nbhd of zero iff each bounded set is contained in a homothety of $U$ "). All the above spaces are complete. For some strange reason, the norm on these spaces is not made explicit. The space $D$ is dense in each of the above four spaces.

Let $H$ be one of the above four spaces. A continuous linear functional on $H$ is a linear functional sending bounded sets to bounded sets of real numbers. The set of all continuous functionals is denoted by $H'$. We have defined a current as an element of $D'$. We can identify $E'$ with the space of currents with compact support. Def: Current continuous to order $p$, relation to the othes spaces above. Various inclusions between all these spaces. Each of the four spaces is reflexive. More details, omitted.

Can define the boundary of a current by $bT[\phi] = T[d \phi]$. Both $d$ and $b$ are continuous linear mappings (of $D$ and $E$, and of $D'$ and $E'$, respectively). We also define the differential of a current (almost the same thing as the boundary). We have $b^2 = 0$ and $d^2 = 0$. For a form with compact support $T$, the integral of $dT$ is zero.

Def: Partial derivative of a current wrt some coordinate. Product rule for differentiation. Can write

$$  d = \sum_i dx^i \wedge \frac{\partial}{\partial x^i}
$$

also for currents.

Def: Image of current by a smooth map of manifolds.

Chapter IV: Homologies

A current $T$ is called closed if $bT =0$. It is called homologous to zero if there exists a current $S$ with $bS = T$ (also say $T$ bounds $S$), and compactly homologous to zero if $S$ can be taken with compact support (this implies that it is closed and has compact support). Get homology groups; the compact support group is the group of closed currents with compact support modulo currents compactly homologous to zero.

Homology classes (compact or not) which contain a homogeneous current are said to be homogeneous, and homology groups decompose into direct sums of subgroups which consist of homogeneous classes of a given parity and a given degree/dimension.

Thm: In a manifold $V$, each (compactly supported) current is (compactly) homologous to a $C^{\infty}$ form. If a $C^r$ form bounds a current (with compact support), it bounds a $C^r$ form (with compact support).

Cor: On a connected mfd, each even closed current of degree zero is equal to a constant function.

Homology groups (compact or not) carry a product structure. 

Compact homology is functorial wrt oriented smooth maps $\mu$, but functorial only as groups, not as rings. Homology is functorial wrt oriented smooth maps which are proper. Both functors preserve dimension and parity.

Homology classes are operators on compact homology groups.

The "transposed image" $\mu^*$ on forms induce a contravariant functorial behaviour for homology, respecting degree and multiplicative structure. If $\mu$ is proper, the same is true for compact homology.

Def and properties of degree.

Homologies in $\mathbb{R}^n$.

The Kronecker index (looks like a generalization of intersection number).

Duality in a mfd endowed with a polyhedral subdivision, later extended to any differentiable mfd.

Thm 17: Describes how to use Kronecker index to check whether a current is homologous to zero or not.

Thm 18: Each closed current $T$ is homologous to a chain (compactly homologous if the support of $T$ is compact).

Thm 19: The homology group of a compact mfd possesses a finite base.

Prop: If a chain is (compactly) homologous to zero, it bounds a (finite) chain.

Chapter V: Harmonic forms

Everything seems to happen on a Riemannian space.

The star operator, and various other cool operators.

Scalar product.

Harmonic currents, and loads of other material...

Cor (p. 134): On a compact Riemannian space, each current can be uniquely decomposed into a sum of a current homologous to zero, a current cohomologous to zero, and a harmonic form. 

Cor: On a compact space, each closed current is homologous to one and only one harmonic form.

Consequences: A new proof of finite-dimensionality, and other things...

The Hodge Thm: On a compact Riemannian space, there always exists a harmonic form having arbitrarily assigned periods relative to given cycles no linear combination of which is homologous to zero.

Decomposition for noncompact spaces.

Explicit formula for Kronecker index.

Analyticity of harmonic forms.

category: [Private] Notes
---
## Deligne cohomology

Goncharov in K-theory handbook (page 304) discusses the real Deligne cohomology of a regular projective scheme over a number field. It is a real vector space.

He also discusses the regulator map for any regular complex projective variety, constructed by Beilinson: Higher regulators and values of L-functions.

category: Domain Category [private]
---
## Deligne cohomology

[MathSciNet](http://www.ams.org/mathscinet/search/publications.html?pg4=AUCN&s4=&co4=AND&pg5=TI&s5=&co5=AND&pg6=PC&s6=&co6=AND&pg7=ALLF&s7=%22Deligne+cohomology%22&co7=AND&Submit=Search&dr=all&yrop=eq&arg3=&yearRangeFirst=&yearRangeSecond=&pg8=ET&s8=All)

[Google Scholar](http://scholar.google.co.uk/scholar?q=%22Deligne+cohomology%22&hl=en&lr=&btnG=Search)

[Google](http://www.google.com/search?hl=en&q=%22Deligne+cohomology%22&btnG=Search)

[arXiv: Experimental full text search](http://search.arxiv.org:8081/?query=%22Deligne+cohomology%22&in=)

[arXiv: Abstract search](http://front.math.ucdavis.edu/search?a=&t=&q=%22Deligne+cohomology%22&c=&n=25&s=Abstracts)

category: Search results
---
## Deligne cohomology

AG (Algebraic geometry)

category: World [private]
---
## Deligne cohomology

Mixed, Arithmetic

category: Labels [private]
---
## Deligne cohomology

Possibly the article of [Dubois and Jarraud](http://www.ams.org/mathscinet-getitem?mr=0376678) could be interesting. Contains results (\"locally free of finite type and compatible with base change\") about higher direct images of sheaves of differential forms, and also the structure sheaf, assuming certain properties of the morphism.

Deligne cohomology is mentioned at the [nLab](http://ncatlab.org/nlab/show/differential+cohomology) entry on differential cohomology

category: Other Information
---
## Deligne cohomology

Maybe not directly related to representability, but Voevodsky: Homology of schemes II, p 25, states that Deligne cohom is a homotopy invariant [[Pretheory]]

category: Representability [private]
---
## Deligne cohomology

See also: [[Deligne-Beilinson cohomology]], [[Absolute Hodge cohomology]], [[Deligne homology]], [[Bloch-Ogus cohomology]], [[Pretheory]]

category: General Introduction
---
## Deligne cohomology

Deninger: Higher order operations in Deligne cohomology

Map from Lawson homology to Deligne cohomology, preprint by Wenchuan Hu

Voevodsky: Homology of schemes I. Discusses the moral of the notion of transfers in the introduction. One of the points seem to be that CTs are functorial wrt correspondences iff they are ordinary, i.e. come from coeffs in a complex of abelian sheaves. Another point is that the "motive" of a CW complex should be its stable homotopy type, if we by motive mean universal wrt all CTs, but if we work with ordinary theories, it should be its singular simplicial complex, as an object in the derived cat of abelian groups. More details provided.

category: Extra Structure [private]
---
## Deligne cohomology

See the chapter by [Esnault and Viehweg](http://www.math.uni-muenster.de/u/peter.schneider/publ/beilinson-volume/EsnaultViehweg.pdf) in the Beilinson volume (on Peter Schneider's web page). See also the excellent article of Scheider himself in the same volume, for more detiailed intro to some of the same things as Deninger-Scholl.

Deninger-Scholl: The Beilinson conjectures. Excellent summary of lots of properties of Deligne cohomology.

&lt;http://ncatlab.org/nlab/show/Deligne+cohomology>

category: Online References
---
## Deligne cohomology

Philosophically, absolute Hodge cohomology might be better in some cases. See Schneider bottom of p 8. This may or may not be related to connectivity properties of the representing spectra. Last paragraph of Schneider says that the interpretation of Deligne cohomology as an Ext group is valid for p &lt; 2q, the Ext group being Ext1 from R to $H^{i-1} (X(C), R(j) )$.

###Notes from discussion with Scholl, Nov 2007:
Consider the complex os sheaves

$$ A(n)_D = A(n) \to \mathcal{O}_X \to \Omega^1 \to \ldots \to \Omega^{n-1}
$$

on $X^{an}$. (X is probably a complex variety). Here $A$ is some ring, and $A(n)$ is $(2 \pi i)^n A$, I think.

We define $H^i_D(X, A(n)) = H^i(X^{an}, A(n)_D )$. (hypercohomology, I think)

See more details in notes from the discussion.

category: Definition
---
## Deligne cohomology

&lt;http://mathoverflow.net/questions/60951/galois-action-on-betti-cohomology>

category: Computations and Examples
---
## Deligne cohomology

[Ayoub and Barbieri-Viale](http://front.math.ucdavis.edu/0607.5738) on an algebraic avatar of Deligne cohomology.

There are articles by Lima-Filho on a construction of integral Deligne cohomology, see for example the abstract under [[Bredon cohomology]]

MR1273841 (95g:19002)
Karoubi, Max(F-PARIS7-M)
Classes caract&#233;ristiques de fibr&#233;s feuillet&#233;s, holomorphes ou alg&#233;briques. (French. English, French summary) [Characteristic classes of foliated, holomorphic or algebraic bundles]
Proceedings of Conference on Algebraic Geometry and Ring Theory in honor of Michael Artin, Part II (Antwerp, 1992).
$K$-Theory 8 (1994), no. 2, 153--211.

MR1758580 (2001g:14033)
Gajer, Pawe\l(1-JHOP)
Geometry of higher connections.

MR2123228 (2005m:14008)
Chen, Xi(3-AB); Lewis, James D.(3-AB)
The Hodge-$\scr D$-conjecture for $K3$ and abelian surfaces.

category: Some Research Articles
---
## Deligne cohomology

Regulator map!

Note the following version which might be related to a regulator map from etale motivic cohomology: Paulo Lima-Filho, TAMU Integral Deligne cohomology for real projective varieties

We develop an 'integral Deligne cohomology theory' for real varieties which bears to Bredon cohomology the same relation that ordinary Deligne cohomology for complex varieties bears to singular cohomology. The theory has a wide range of connections ranging from equivariant topology (via Bredon equivariant cohomology), through complex differential geometry (via holomorphic line bundles with quadratic forms and holomorphic connections) to number theory (via Milnor K-theory of number fields and regulator maps). We will present --time permitting-- many examples. In a forthcoming work we show that the cycle map from motivic cohomology to Bredon cohomology factors through our Deligne cohomology groups.

In Esnault-Vieweg's survey on Deligne they outline a theory for real varieties, as well. Such a variant would be related to Lichtenbaum's etale motivic cohomology and the Borel version of equivariant cohomology. The difference between their version and ours stems from the difference between the etale and Nisnevich topologies.

category: Connections to Number Theory
---
## Deligne cohomology

Burgos-Gil: The regulators of Beilinson and Borel

Levine, in K-theory handbook page 510, mentions real Deligne cohomology and integral Deligne cohomology, and cycle class maps to these cohomologies.

C*-algebras: See many things in the folder Noncomm geom and Cstar-alg. Same for Noncomm geom in the sense of Connes, Cyclic homology

Loday: Cyclic homology. In Noncomm geom folder. Covers many aspects of Cyclic and Hochschild homology. Among many other topics: Secondary char classes (section 11.5), Homology of small categories (App C), periodic and negative cyclic homology, Andre-Quillen homology, Deligne cohomology. For the latter, the main point is that there a cyclic homology complex of Connes which computes integral coeffs reduced Deligne cohomology but which has strictly commutative products!! This is stated for smooth algebras over C, not sure if it can be generalized to more general schemes. Also I am not sure if this has any relevance for non-reduced Deligne cohomology.

LNM 1594: Algebraic cycles and Hodge theory. Contains the following lectures, many of them touching Deligne cohomology in some way: 

- Green: Infinitesimal methods in Hodge theory
- Murre: Algebraic cycles and algebraic aspects of cohomology and K-theory
- Voisin: Transcendental methods in the study of algebraic cycles
- Pirola
- Van Geemen: An introduction to the Hodge conjecture for abelian varieties
- Muller-Stach: A remark on height pairings

category: Paper References

nLab page on [[nlab:Deligne cohomology]]
