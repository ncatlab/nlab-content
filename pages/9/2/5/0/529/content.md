
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _group algebra_ of a [[group]] $G$ over a [[ring]] $R$ is the [[associative algebra]] whose elements are [[formal linear combinations]] over $R$ of the elements of $G$ and whose multiplication is given on these [[basis]] elements by the group operation in $G$.



## Definition



### For discrete groups
 {#ForDiscreteGroups}

Let $G$ be a [[discrete group]]. Let $R$ be a [[commutative ring]].

+-- {: .num_defn }
###### Definition

The **group $R$-algebra** $R[G]$ is the [[associative algebra]] over $R$

1. whose [[underlying]] $R$-[[module]] is the the [[free module]] over $R$ on the [[underlying set]] of $G$;

1. whose multiplication is given on [[basis]] elements by the group operation.

=--

+-- {: .num_remark }
###### Remark

By the discussion at [[free module]], an element $r$ in $R[G]$ is a [[formal linear combination]] of [[basis]] elements in $G$ with [[coefficients]] in $R$, hence a formal sum

$$
  r = \sum_{g \in G} r_g \cdot g
$$

with $\forall_{g \in G} (r_g \in R)$ and only finitely many of the coefficients different from $0 \in R$.

The addition of algebra elements is given by the componentwise addition of coefficients

$$
  r + \tilde r =
  \sum_{g \in G} (r_g + \tilde r_g) g
$$

and the multiplication is given by the [[convolution product]]

$$
  \begin{aligned}
    r \tilde r
    & =
    \sum_{g \in G}
      \sum_{\tilde g \in G}
      (r_g \tilde r_{\tilde g}) g \cdot \tilde g
    \\
    & =
    \sum_{q \in G}
    \left(
      \sum_{k \in G}  (r_{q\cdot k^{-1}} r_k)
    \right) q
    \,.
  \end{aligned}
$$

=--

+-- {: .num_remark }
###### Remark

The [[formal linear combinations]] over $R$ of element in $G$ may equivalently be thought of as [[functions]]

$$
  r_{(-)} \colon U(G) \to U(R)
$$

from the underlying set of $G$ to the underlying set of $R$ which have _finite support_. Accordingly,  often the underlying set of the group $R$-algebra is written as

$$
  U(R[G]) = Hom_{Set}^{fin\;supp}(U(G), U(R))
$$

and for the [[basis elements]] one writes

$$
  \chi_g \colon U(G) \to U(R)
  \,,
$$

the **characteristic function** of an element $g \in G$, defined by

$$
  \chi_g \colon \tilde g \mapsto
  \left\{
    \array{
      1 & | g = \tilde g
      \\
      0 & | otherwise
    }
  \right.
  \,.
$$

In terms of this the product in the group algebra is called the **[[convolution product]]** on functions.

=--

+-- {: .num_remark }
###### Remark

The notion of group algebra is a special case of that of a [[groupoid algebra]], hence of [[category algebra]].

=--


###For profinite groups

The completed group ring of a [[profinite group]] is a pseudocompact ring.
Let $\hat{\mathbb{Z}}$ be the [[profinite completion]] of the ring of integers, $\mathbb{Z}$, then $\hat{\mathbb{Z}}$  is itself a [[pseudocompact ring]] as it is the inverse limit of its _finite_ quotients.  Now let $G$ be a profinite group.


The _completed group algebra_, $\hat{\mathbb{Z}}[\![G]\!]$, of $G$ over $\hat{\mathbb{Z}}$ is the inverse limit of the ordinary group algebras, $\hat{\mathbb{Z}}[G/U] $, of the finite quotients, $G/U$ (for $U$ in the directed set, $\Omega(G)$, of open normal subgroups of $G$), over $\hat{\mathbb{Z}}$;

$$\hat{\mathbb{Z}}[\![G]\!] = lim_{U\in \Omega(G)} \hat{\mathbb{Z}}[G/U].$$

For $R$ a pseudocompact ring, it is then easy to construct the corresponding pseudo-compact group algebra of $G$ over $R$; see the paper by Brumer.

### For topological groups
 {#ForTopologicalGroups}

Discussion of group algebras in the generality of [[locally compact topological groups]]:

e.g. [Dixmier (1977) §13.2](#Dixmier77)



## Properties

### General

+-- {: .num_prop }
###### Proposition

A group algebra is in particular a [[Hopf algebra]] and a $G$-[[graded algebra]].

=--

The following states a [[universal property]] of the construction of the group algebra.

+-- {: .num_remark}
###### Remark

There is an [[adjunction]]

$$
  (R[-]\dashv (-)^\times)
  \;\colon\;
  Alg_R
    \underoverset
      {
        \underset{
          \;\;\;
          (-)^\times
          \;\;\;
        }{
          \longrightarrow
        }
      }
      {
        \overset{
          \;\;\;
          R[-]
          \;\;\;
        }{
          \leftarrow
        }
      }
      {}
  Grp
$$

between the [[category]] of [[Algebras]] ([[associative algebras]] over $R$) and that of [[Groups]], where $R[-]$ forms [[group rings]] and $(-)^\times$ assigns to an $R$-algebra its [[group of units]].

=--

+-- {: .num_remark}
###### Remark

Let $V$ be an [[abelian group]]. A [[homomorphism]] of rings $R[G] \to End(V)$ of the group ring to the [[endomorphism ring]] of $V$ is equivalently a $R[G]$-[[module]] structure on $V$.

Any [[homomorphism]] of groups $p \colon G \to Aut(V)$ to the [[automorphism group]] of $V$ extends to to a morphism of rings.

This observation is used extensively in the theory of [[group representation|group representations]]. See also at _[module -- Abelian groups with G-action as modules over a ring ](http://ncatlab.org/nlab/show/module#AbelianGroupsWithGAction)_.

=--

\begin{prop}\label{ComplexGroupAlgebraOfFiniteGroupAsDirectSumOfEndomorphismAlgebras}
  For $G$ a [[finite group]] with [[isomorphism classes]] of [[irreducible representations]] $[V] \in Irreps_{\mathbb{C}}(G)_{/\sim}$ over the [[complex numbers]], the complex [[group algebra]] of $G$ is [[isomorphism|isomorphic]] to the [[direct sum]] of the linear [[endomorphism algebras]] of the [[complex vector spaces]] underlying the [[irreps]]:
$$
  \mathbb{C}[G]
  \;\simeq\;
  \underset{
    [V] \in Irreps_{\mathbb{C}}(G)_{/\sim}
  }{ \oplus }
  End_{\mathbb{C}}(V)
$$
\end{prop}
(e.g. [Fulton-Harris 91, Prop. 3.29](#FultonHarris91))
\begin{proof}
  For every representation $V$, the defining [[group action]]
  $$
    G
      \overset{}{\longrightarrow}
    Aut_{\mathbb{C}}(V)
      \hookrightarrow
    End_{\mathbb{C}}(V)
  $$
  [[extension|extends]] uniquely to an [[algebra homomorphism]]
  $$
    \mathbb{C}[G]
      \overset{ \phi_V }{\longrightarrow}
    End_{\mathbb{C}}(V)
    \,.
  $$
  Observe that this is a [[surjection]], since if it were not then we could split off a  non-trivial [[cokernel]], contradicting the assumption that $V$ is irreducible.

  We claim that the resulting homomorphism to the [[direct sum]]
  $$
    \mathbb{C}[G]
      \overset{ (\phi_V)_{[V]} }{\longrightarrow}
    \underset{
      [V] \in Irreps_{\mathbb{C}}(G)_{/\sim}
    }{\oplus}
    End_{\mathbb{C}}(V)
  $$
  is an [[isomorphism]]: By the previous comment it is [[surjective]], hence it is sufficient to observe that the [[dimension of a vector space|dimension]] of the group algebra equals that of the right hand side, hence that
$$
  dim\big(
    \mathbb{C}[Sym(G)]
  \big)
  \;=\;
  \underset{[V]}{\sum} \big( dim(V)\big)^2
  \,.
$$
This is indeed the case, by [this property](regular+representation#RegularRepDecomposedIntoIrreps) of the [[regular representation]].
\end{proof}


+-- {: .num_theorem}
###### Theorem
([[Maschke's theorem]])

Let $G$ be a [[finite group]], let $R = k$ be a field.

Then $k[G]$ is a [[semi-simple algebra]] precisely if the [[order]] of $G$ is not divisible by the [[characteristic]] of $k$.

=--

The following is proven in [Gilmer 1992](#Gilmer92), p. 163:
 
\begin{theorem}
Let $A$ be an [[abelian group]] and $R$ a [[commutative ring]]. Then $R[A]$ is an [[integral domain]] iff $R$ is an integral domain and $A$ is [[torsion-free]].
\end{theorem}

### Of central extensions & Twisted group algebras
 {#OfCentralExtensionsAndTwistedGroupAlgebras}

A [[quotient algebra]] of the group algebra of a [[central extension]] $G^\omega$ of a group $G$ corresponding to a [[group cocycle|group 2-cocycle]] $\omega \,\colon\, G \times G \to k$ is the *$\omega$-twisted* group algebra of $G$ (eg. [Nachbin 1993, Ch 2, Thm. 4.1](#Nachbin93)).

\begin{example}
\label{ComplexGroupAlgebraOfCircleCentralExtension}
**(complex group algebra of $\mathrm{U}(1)$-central extension)**
\linebreak
For $\big(G, (-)\cdot(-), \mathrm{e}\big)$ a [[discrete group]], consider a [[central extension]]

$$
  1
    \to
  \mathbb{R}/\mathbb{Z}
    \hookrightarrow
  G^\omega
    \twoheadrightarrow
  G
    \to
  1
$$

classified by a [[circle group]]-valued [[group cocycle|group 2-cocycle]] with [[underlying]] [[function]]

$$
  \omega
    \,\colon\,
  G \times G \to \mathbb{R}/\mathbb{Z}
  \,,
$$

which we may and do assume to be normalized:

$$
  \omega(g,\mathrm{e}) \,=\, 0,\,
  \;\;\;
  \omega(\mathrm{e},g) \,=\, 0
  \,.
$$

In terms of this cocycle, the group operation on the [[underlying]] [[set]]

$$
  G^\omega
    \;\simeq\;
  G \,\times\, \mathbb{R}/\mathbb{Z}
$$

is given by

$$
  (g, r) \cdot (g',r')
  \;\equiv\;
  \big(
    g \cdot g'
    ,\,
    r + r' + \omega(r,r')
  \big)
 \,.
$$

> We regard $\mathbb{R}/\mathbb{Z}$ as a [[discrete group]]. Since the cocycle will typically (certainly if $G$ is [[finite group|finite]]) take values only in a [[finite group|finite]] [[cyclic group|cyclic]] [[subgroup]] $\mathbb{Z}/n \hookrightarrow \mathbb{R}/\mathbb{Z}$ one may want to take $G^\omega$ to be just the finite group given by the resulting $\mathbb{Z}/n$-[[central extension]]. The discussion here applies verbatim in either case.

If we denote the generators of the [[complex numbers|$\mathbb{C}$-valued]] [[group algebra]] of $G^\omega$ by

$$
  \array{
    G^\omega
      &\longrightarrow&
    \mathbb{C}\big(G^\omega\big)
    \\
    (g,r) &\mapsto& U(g,r)
  }
$$

then we have in $\mathbb{C}\big(G^\omega \big)$ the relations

$$
  U(g,r)
  \;=\;
  U(g,0) \cdot U(\mathrm{e},r)
  \;=\;
  U(\mathrm{e},r)
    \cdot
  U(g,0)
$$
(by normality of $\omega$) and hence
$$
  \begin{array}{rcl}
  U(g, 0) \cdot U(g', 0)
  &=&
  U\big(g g', \omega(g,g')\big)
  \\
  &=&
  U\big(\mathrm{e}, \omega(g,g')\big)
  \cdot
  U(g g', 0)
  \,.
  \end{array}
$$

This looks, up to the [[center|central]] correction factor $U\big(\mathrm{e}, \omega(g,g')\big)$, like the group algebra of $G$.

To bring out this relation, consider now the [[quotient algebra]] of $\mathbb{C}\big(G^\omega\big)$ by the canonical [[augmentation ideal]] of the group algebra of the extension group, ie. by the two-sided [[ideal]] in $\mathbb{C}\big(G^\omega\big)$ generated by the [[kernel]] of the $\mathbb{C}$- [[algebra homomorphism]]

$$
  \begin{array}{ccc}
    \mathbb{C}\big(\mathbb{R}/\mathbb{Z}\big)
    &\xrightarrow{\;\; \epsilon \;\;}&
    \mathbb{C}
    \\
    U\big(
     \mathrm{e},
     r
    \big)
    &\mapsto&
    e^{2 \pi \mathrm{i} r }
    \mathrlap{\,.}
  \end{array}
$$

In other words, in this quotient of $\mathbb{C}\big(G^\omega\big)$ we enforce the [[relations]]
$$
  \begin{array}{rcl}
    U(\mathrm{e}, r)
    &\sim&
    exp(2 \pi \mathrm{i} r )
    \,
    U(\mathrm{e}, 0)
    \\
    &=&
    exp(2 \pi \mathrm{i} r )
  \end{array}
$$
(using in the last step that $(\mathrm{e}, 0)$ is the [[neutral element]] of $G^\omega$, so that $U(\mathrm{e}, 0)$ is the [[unit element]] in its group algebra).

Therefore the [[quotient algebra]] $\mathbb{C}\big(G^\omega\big)\big/ ker(\epsilon)$ is that generated by $U(G) \,=\, U\big(G \times \{0\}\big)$ subject to the relations

$$
  U(g) \cdot U(g')
  \;=\;
  e^{ 2 \pi \mathrm{i} \omega(g,g') }
  \,
  U(g\cdot g')
  \,.
$$

This is the $\omega$-twisted group algebra $\mathbb{C}^\omega(G)$ of $G$:

$$
  \mathbb{C}\big(
    G^\omega
  \big)
  \big/
  \mathrm{ker}(\epsilon)
  \;\;
  \simeq
  \;\;
  \mathbb{C}^\omega(G)
  \,.
$$
\end{example}


With due care, this situation generalizes from [[discrete groups]] to suitable (eg. [[locally compact topological groups|locally compact]]) [[topological groups]] ([Edwards & Lewis 1969a](#EdwardsLewis69a), [1969b](#EdwardsLewis69b)).

\begin{example}
**([Binz, Honegger & Rieckers 2007](#BinzHoneggerRieckers07))** 
\linebreak
It is in this way that the group algebra of a ([[underlying]] [[discrete group|discrete]]) [[Heisenberg group]] (which is a [[central extension]] of an [[abelian group]]) is related to the corresponding [[Weyl group]] (whose [[Weyl relations]] are those of a twisted additive group algebra).
\end{example}


### Relation to universal enveloping algebras
 {#RelationToUniversalEnvelopingAlgebra}

Concerning group algebras of [[algebraic groups]]:

> The [[universal enveloping algebra]] of a [[Lie algebra]] is the analogue of the usual [[group algebra]] of a group. It has the analogous function of exhibiting the [[category]] of [[Lie algebra modules]] as a category of [[modules]] for an [[associative algebra]]. This becomes more than an analogy when the universal enveloping algebra is viewed with its full [[Hopf algebra]] structure. By dualization, one obtains a commutative Hopf algebra which, in the case where the Lie algebra is that of an irreducible [[algebraic group]] over a [[field]] of [[characteristic 0]], contains the algebra of polynomial functions of that group as a sub Hopf algebra in a natural fashion.

(quoted from [Hochschild 1981, p. 221](universal+enveloping+algebra#Hochschild81), see Thm. 3.1 on p. 230 there)



## Related concepts

* [[Cohn localization]]

* [[groupoid algebra]], [[category algebra]]

* [[augmentation ideal]]

* [[pseudocompact ring]]

* [[Day convolution]]

* [[∞-group ∞-ring]]

## References

### General

Original discussion:

* [[Hermann Weyl]], §III.13 in: *Gruppentheorie und Quantenmechanik*, S. Hirzel, Leipzig (1931), translated by H. P. Robertson: *The Theory of Groups and Quantum Mechanics*, Dover (1950) &lbrack;[ISBN:0486602699](https://store.doverpublications.com/0486602699.html), [ark:/13960/t1kh1w36w](https://archive.org/details/ost-chemistry-quantumtheoryofa029235mbp/page/n15/mode/2up)&rbrack;

Exposition:

* D. S. Passman: *What is a Group Ring?*, The American Mathematical Monthly **83** 3 (1976)  &lbrack;[doi:10.1080/00029890.1976.11994069](https://doi.org/10.1080/00029890.1976.11994069)&rbrack;


Monographs:

for the case of [[locally compact topological groups]]:

* {#Dixmier77} [[Jacques Dixmier]], §13.2 in: *$C^\ast$-algebras*, North Holland (1977)


* {#Landsman17} [[Klaas Landsman]], §C.18 in: *Foundations of quantum theory -- From classical concepts to Operator algebras*, Springer Open (2017) &lbrack;[doi:10.1007/978-3-319-51777-3](https://link.springer.com/book/10.1007/978-3-319-51777-3), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf)&rbrack;


for the case of [[finite groups]]:

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]], Section 3.4 of: *Representation Theory: a First Course*, Springer (1991) &lbrack;[doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9)&rbrack;

* [[A. P. Balachandran]], S. G. Jo, [[Giuseppe Marmo]], p 51, 197 of: *Group Theory and Hopf Algebras -- Lectures for Physicists*, World Scientific (2010) &lbrack;[doi:10.1142/7872](https://doi.org/10.1142/7872)&rbrack;


Lecture notes:

* [[Kiyoshi Igusa]], _Algebra II, part D: representations of groups_, ([pdf](http://people.brandeis.edu/~igusa/Math101bS07/Math101b_notesD1a.pdf))

* Andrei Yafaev, _Group algebras_ ([pdf](http://www.ucl.ac.uk/~ucahaya/GroupAlgebras.pdf))

On twisted group algebras and their relation to plain group algebras of [[group extensions]]:


* C. M. Edwards, *$C^\ast$-algebras of central group extensions I*, Annales de l'institut Henri Poincaré. Section A, Physique Théorique **10** 3 (1969) 229-246 &lbrack;[numdam:AIHPA_1969__10_3_229_0](http://www.numdam.org/item/?id=AIHPA_1969__10_3_229_0)&rbrack;

* {#EdwardsLewis69a} C. M. Edwards, [[John T. Lewis]], *Twisted group algebras I*, Communications in Mathematical Physics **13** (1969) 119–130 &lbrack;[doi:10.1007/BF01649871](https://doi.org/10.1007/BF01649871), [euclid:cmp/1103841535](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-13/issue-2/Twisted-group-algebras-I/cmp/1103841535.full)&rbrack;

* {#EdwardsLewis69b} C. M. Edwards, [[John T. Lewis]], *Twisted group algebras II*, Communications in Mathematical Physics **13** (1969) 131–141 &lbrack;[doi:10.1007/BF01649872](https://doi.org/10.1007/BF01649872)&rbrack;

* {#Nachbin93} Leopoldo Nachbin (ed.), *Twisted Group Algebras*, Chapter 2 in: *Group Representations Volume 2*, North-Holland Mathematics Studies **177** (1993) 65-103 &lbrack;<a href="https://doi.org/10.1016/S0304-0208(09)70147-1">doi:10.1016/S0304-0208(09)70147-1</a>&rbrack;

The [[universal localization]] of group rings (see also at _[[Snaith's theorem]]_) is discussed in

* [[M. Farber]], [[Pierre Vogel]], _The Cohn localization of the free group ring_, Math. Proc.  Camb. Phil. Soc. (1992) 111, 433  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/fv.pdf))

* Davidson, Nicholas, _Modules Over Localized Group Rings for Groups Mapping Onto Free Groups_ (2011). Boise State University Theses and Dissertations. Paper 170. ([web](http://scholarworks.boisestate.edu/td/170/))

On the case of profinite groups:

* A. Brumer, _Pseudocompact algebras, profinite groups and class formations_,  J. Algebra __4__ (1966) 442-470, [MR202790](http://www.ams.org/mathscinet-getitem?mr=202790), <a href="http://dx.doi.org/10.1016/0021-8693(66)90034-2">doi</a> [pdf](http://deepblue.lib.umich.edu/bitstream/handle/2027.42/33410/0000811.pdf?sequence=1)

### In physics

On group algebras as [[strict deformation quantization|strict]] [[deformation quantizations]] of [[Lie-Poisson manifolds]]:

* [[Marc A. Rieffel]], *Lie Group Convolution Algebras as Deformation Quantizations of Linear Poisson Structures*, American Journal of Mathematics **112** 4 (1990) 657-685 &lbrack;[doi:10.2307/2374874](https://doi.org/10.2307/2374874), [jstor:2374874](https://www.jstor.org/stable/2374874)&rbrack;

* {#Rieffel90} [[Marc Rieffel]], Ex. 7, Ex. 8 in: _Deformation quantization and operator algebras_, in: Operator theory: operator algebras and applications, Part 1 (Durham, NH, 1988), 411-423, Proc. Sympos. Pure Math. __51__, Part 1, Amer. Math. Soc. (1990) &lbrack;[pdf](http://math.berkeley.edu/~rieffel/papers/deformation.pdf), [[Rieffel-DefQuantization.pdf:file]] [MR91h:46120](http://www.ams.org/mathscinet-getitem?mr=1077400)&rbrack;

Strengthening of the original result, including generalization to [[groupoid algebras]] of [[Lie groupoids]] [[Lie integration|integrating]] given [[Lie algebroids]]:

* [[Nicolaas P. Landsman]], §3.4 in: *Classical and quantum representation theory* &lbrack;[arXiv:hep-th/9411172](https://arxiv.org/abs/hep-th/9411172)&rbrack;


* [[Nicolaas P. Landsman]], Ex. 2 in: *Lie Groupoid $C^\ast$-Algebras and Weyl Quantization*, Communications in Mathematical Physics **206** (1999) 367–381 &lbrack;[doi:10.1007/s002200050709](https://doi.org/10.1007/s002200050709)&rbrack;

* [[Nicolaas P. Landsman]], B. Ramazan, Ex. 11.1 in: *Quantization of Poisson algebras associated to Lie algebroids*, in: *Groupoids in Analysis, Geometry, and Physics*, Contemporary Mathematics **282** (2001) &lbrack;[arXiv:math-ph/0001005](https://arxiv.org/abs/math-ph/0001005), [ams:conm/282](http://www.ams.org/books/conm/282)&rbrack;


See also:

* [[Klaas Landsman]], *Strict deformation quantization of a particle in external gravitational and Yang-Mills fields*, Journal of Geometry and Physics __12__ 2 (1993) 93-132 &lbrack;<a href="https://doi.org/10.1016/0393-0440(93)90010-C">doi:10.1016/0393-0440(93)90010-C</a>&rbrack;

* [[Nicolaas P. Landsman]], p. 27 in: *Classical and quantum representation theory* &lbrack;[arXiv:hep-th/9411172](https://arxiv.org/abs/hep-th/9411172)&rbrack;


On [[group algebras]] of ([[underlying]] [[discrete group|discrete]]) [[Heisenberg groups]] as [[strict deformation quantizations]] of [[presymplectic manifold|pre-]][[symplectic vector spaces|symplectic]] [[topological vector spaces]] by [[continuous field of C-star algebras|continuous fields of]] [[Weyl algebras]]:

* {#BinzHoneggerRieckers07} [[Ernst Binz]], [[Reinhard Honegger]], [[Alfred Rieckers]], *Infinite dimensional Heisenberg group algebra and field-theoretic strict deformation quantization*, International Journal of Pure and Applied Mathematics **38** 1 (2007) &lbrack;[ijpam:2007-38-1/6](https://ijpam.eu/contents/2007-38-1/6/index.html), [pdf](https://www.ijpam.eu/contents/2007-38-1/6/6.pdf)&rbrack;

* [[Reinhard Honegger]], [[Alfred Rieckers]], *Heisenberg Group Algebra and Strict Weyl Quantization*, Chapter 23 in: *Photons in Fock Space and Beyond, Volume I: From Classical to Quantized Radiation Systems*, World Scientific (2015) &lbrack;chapter:[doi;10.1142/9789814696586_0023](https://doi.org/10.1142/9789814696586_0023), book:[doi:10.1142/9251-vol1](https://doi.org/10.1142/9251-vol1)&rbrack;

On the [[supersymmetry|supersymmetric]] [[WZW model]] using group algebra:

* [[Matthias Blau]], [[George Thompson]], *Equivariant Kähler Geometry and Localization in the $G/G$ Model*, Nucl. Phys. B **439** (1995) 367-394 &lbrack;<a href="https://doi.org/10.1016/0550-3213(95)00058-Z">doi:10.1016/0550-3213(95)00058-Z</a>, [arXiv:hep-th/9407042](https://arxiv.org/abs/hep-th/9407042)&rbrack;

Group algebras play a role in the relation between [[ordered abelian groups]] and divisibility in [[integral domains]]:

* {#Gilmer92}[[Robert Gilmer]]: *Multiplicative Ideal Theory*, Queen's Papers in Pure and Applied Mathematics (1992)

[[!redirects group algebras]]

[[!redirects group ring]]
[[!redirects group rings]]

[[!redirects twisted group algebra]]
[[!redirects twisted group algebras]]


[[!redirects group convolution algebra]]
[[!redirects group convolution algebras]]

