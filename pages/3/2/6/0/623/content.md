+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea

The _Moore complex_ of a [[simplicial group]] -- also known in its normalized version as the **complex of normalized chains** -- is a [[chain complex]] whose [[differential]] is built from the face maps of the simplicial group.

The operation of forming the Moore complex of chains of a [[simplicial group]] is one part of the [[Dold-Kan correspondence]] that relates [[simplicial object|simplicial]] (abelian) [[groups]] with [[chain complexes]].

Recall that a [[simplicial group]] $G$, being in particular a [[Kan complex]], may be thought of, in the sense of the [[homotopy hypothesis]], as a combinatorial space equipped with a group structure. The Moore complex of $G$ is a [[chain complex]] 

* whose $n$-cells are the "$n$-disks with basepoint on their boundary" in this space, with the basepoint sitting on the identity element of the space;

* the boundary map on which acts literally like a boundary map should: it sends an $n$-disk to its boundary, read as an $(n-1)$-disk whose entire boundary is concentrated at the identity point.

This is entirely analogous to how a [[crossed complex]] is obtained from a [[strict ∞-groupoid]]. In fact it is a special case of that, as discussed at [[Dold-Kan correspondence]] in the section on the nonabelian version.

## Definition

### For general simplicial groups
 {#ForGeneralSimplicialGroups}

+-- {: .num_defn #NormalizedChainComplexOnGeneralGroup}
###### Definition

Given a [[simplicial group]] $G$, its _[[normalized chain complex]]_ or _Moore complex_ is the $\mathbb{N}$-graded [[chain complex]] $((N G)_\bullet,\partial )$ of (possibly [[nonabelian group|nonabelian]]) groups which



* is in degree $n$ the joint [[kernel]] 

  $$
    (N G)_n=\bigcap_{i=1}^{n}ker\,d_i^n 
  $$

  of all face maps except the 0-face;

* with differential given by the remaining 0-face map

  $$
   \partial_n \coloneqq d_0^n|_{(N G)_n} : (N G)_n \rightarrow (N G)_{n-1}
   \,.
  $$ 

=--



+-- {: .num_remark}
###### Remark

In def. \ref{NormalizedChainComplexOnGeneralGroup} one may equivalently take the  joint [[kernel]] of all but the $n$-face map and take that remaining face map,  $d_n^n$, to be the differential.

=--

+-- {: .num_remark}
###### Remark

We may think of the elements of the complex $N G$, def. \ref{NormalizedChainComplexOnGeneralGroup}, in degree $k$
as being $k$-dimensional [[disks]] in $G$ all of whose [[boundary]] is captured by a single face:

* an element $g \in N G_1$ in degree 1 is a 1-disk

  $$
    1 \stackrel{g}{\to} \partial g
    \,,
  $$

* an element $h \in N G_2$ is a 2-disk

  $$
    \array{
       && 1 
       \\
       & {}^1\nearrow &\Downarrow^h& \searrow^{\partial h}
       \\
       1
       &&\stackrel{1}{\to}&&
       1
    }
    \,,
  $$

* a degree 2 element in the kernel of the boundary map is such a 2-disk that is closed to a 2-[[sphere]]

  $$
    \array{
       && 1 
       \\
       & {}^1\nearrow &\Downarrow^h& \searrow^{\partial h = 1}
       \\
       1
       &&\stackrel{1}{\to}&&
       1
    }
    \,,
  $$

etc.

=--


+-- {: .num_prop}
###### Proposition

For every [[simplicial group]] $G$ the normalized chain complex $(N G)_\bullet$ in def. \ref{NormalizedChainComplexOnGeneralGroup} is a [[normal complex of groups]], 

=--

+-- {: .num_remark}
###### Remark

This means that is easy to take the homology of the complex, even though the groups involved may be non-abelian. 

=--





### For simplicial abelian groups
 {#ForSimplicialAbelianGroups}

Let now $A$ be a [[simplicial abelian group]]. Then its [[normalized chain complex]] $(N A)_\bullet \in Ch_\bullet^+$ of def. \ref{NormalizedChainComplexOnGeneralGroup} is an ordinary [[connective chain complex|connective]] [[chain complex]] in the [[abelian category]] [[Ab]].

In this abelian cases are two other chain complexes naturally associated with $A$:

+-- {: .num_defn #AlternatingFaceMapComplex}
###### Definition

For $A$ a [[simplicial abelian group]] its **alternating face map complex** $(C A)_\bullet$ of $A$ is the [[chain complex]] which 

* in degree $n$ is given by the group $A_n$ itself

  $$
    (C A)_n \coloneqq A_n
  $$


* with [[differential]] given by the alternating sum of face maps (using the abelian group structure on $A$)

  $$
    \partial_n \coloneqq \sum_{i = 0}^n (-1)^i d_i  \;\colon\; (C A)_n \to (C A)_{n-1}
    \,.
  $$

  (see lemma \ref{AlternatingSumOfFacesInNilpotent}).

=--

+-- {: .num_lemma #AlternatingSumOfFacesInNilpotent}
###### Lemma

The differential in def. \ref{AlternatingFaceMapComplex} is well-defined in that it indeed squares to 0.

=--

+-- {: .proof}
###### Proof

Using the [[simplicial identities|simplicial identity]] $d_i \circ d_j = d_{j-1} \circ d_i$ for $i \lt j$ one finds:

$$
  \begin{aligned}
    \partial_n \partial_{n+1}
    & =
    \sum_{i, j} 
      (-1)^{i+j}
      d_i \circ d_{j}
    \\
    &=
    \sum_{i  \geq j} (-1)^{i+j} d_i \circ d_j 
    + 
    \sum_{i \lt j} (-1)^{i+j}
      d_i \circ d_j 
    \\
    &=
    \sum_{i  \geq j} (-1)^{i+j} d_i \circ d_j 
    + 
    \sum_{i \lt j} (-1)^{i+j}
      d_{j-1} \circ d_i 
    \\
    &=
    \sum_{i  \geq j} (-1)^{i+j} d_i \circ d_j 
    -
    \sum_{i \leq k} (-1)^{i+k}
      d_{k} \circ d_i 
    \\
    &=
    0
  \end{aligned}
  \,.
$$


=--

+-- {: .num_defn #DegenerateElement}
###### Definition

Given a [[simplicial group]] $A$ (or in fact any [[simplicial set]]), then an element $a \in A_{n+1}$ is called _degenerate_  if it is in the [[image]] of one of the simplicial degeneracy maps $s_i \colon A_n \to A_{n+1}$. All elements of $A_0$ are regarded a non-degenerate.
Write

$$
  D (A_{n+1}) \coloneqq \langle \cup_i s_i(A_{n}) \rangle \hookrightarrow A_{n+1}
$$ 

for the [[subgroup]] of $A_{n+1}$ which is generated by the degenerate elements (i.e. the smallest subgroup containing all the degenerate elements). Elements of $D(A)_{n}$ are often called _[[thin element|thin]]_ $n$-simplices.

=--


+-- {: .num_defn #ComplexModuloDegeneracies}
###### Definition


For $A$ a [[simplicial abelian group]] its **alternating face maps chain complex modulo degeneracies**, $(C A)/(D A)$ is the [[chain complex]] 

* which in degree 0 equals is just $((C A)/D(A))_0 \coloneqq A_0$;

* which in degree $n+1$ is the [[quotient]] group obtained by dividing out the group
  the degenerate elements, def. \ref{DegenerateElement}:

  $$
    ((C A)/D(A))_{n+1} \coloneqq A_{n+1} / D(A_{n+1})
  $$

* whose [[differential]] is the induced action of the alternating sum of faces on the quotient (which is well-defined by lemma \ref{LeftCosetsDisjoint}).

=--



+-- {: .num_lemma #LeftCosetsDisjoint}
###### Lemma

Def. \ref{ComplexModuloDegeneracies} is indeed well defined 
in that the  alternating face map differential 
respects the degenerate subcomplex.

=--
+-- {: .proof}
###### Proof

Using the mixed [[simplicial identities]] we find that for $s_j(a) \in A_n$ a degenerate element, its boundary is

$$
  \begin{aligned}
     \sum_i (-1)^i d_i s_j(a)
     &=
     \sum_{i \lt j} (-1)^i  s_{j-1} d_i(a)
     +
     \sum_{i = j, j+1} (-1)^i  a
     +
     \sum_{i \gt j+1} (-1)^i s_j d_{i-1}(a)
     \\
     &=
     \sum_{i \lt j} (-1)^i  s_{j-1} d_i(a)
     +
     \sum_{i \gt j+1} (-1)^i s_j d_{i-1}(a)
  \end{aligned}
$$

which is again a combination of elements in the image of the degeneracy maps.

=--


 

## Properties

### Normalization


+-- {: .num_prop #NormalizedIntoModuloDegeneraciesIsIsomorpism}
###### Proposition

Given a [[simplicial abelian group]] $A$, the evident composite of natural morphisms

$$
  N A \stackrel{i}{\hookrightarrow} CA
  \stackrel{p}{\to}
  (C A)/(D A)
$$

from the normalized chain complex, def. \ref{NormalizedChainComplexOnGeneralGroup}, into the alternating face map complex modulo degeneracies, def. \ref{ComplexModuloDegeneracies}, (inclusion followed by projection to the quotient) is a [[natural isomorphism]] of chain complexes.

=--

([Goerss-Jardine, theorem III 2.1](#GoerssJardine), see also [Schwede-Shipley 03, Section 2.1](#SchwedeShipley03)).


+-- {: .num_cor #SplittingOffDegenerateCells}
###### Corollary

For $A$ a [[simplicial abelian group]], there is a splitting

$$
  C_\bullet(A) \simeq N_\bullet(A) \oplus D_\bullet(A)
$$

of the alternating face map complex, def. \ref{AlternatingFaceMapComplex} as a [[direct sum]],
where the first direct summand is [[natural isomorphism|naturally isomorphic]] to the [[normalized chain complex]] of def. \ref{NormalizedChainComplexOnGeneralGroup} and the second is the degenerate cells from def. \ref{ComplexModuloDegeneracies}.

=--

+-- {: .proof}
###### Proof

By prop. \ref{NormalizedIntoModuloDegeneraciesIsIsomorpism} there is an [[inverse]] to the diagonal composite in

$$
  \array{
    C A &\stackrel{p}{\longrightarrow}& (C A)/(D A)
    \\
    {}^{\mathllap{i}}\uparrow & \nearrow
    \\
    N A 
  }
  \,.
$$

This hence exhibits a [[split exact sequence|splitting]] of the [[short exact sequence]] given by the quotient by $D A$.

$$
  \array{
    0 &\to& D A &\hookrightarrow & C A &\stackrel{p}{\longrightarrow}& (C A)/(D A) &\to & 0 
    \\
    && && {}^{\mathllap{i}}\uparrow & \swarrow_{\mathrlap{\simeq}_{iso}}
    \\
    && && N A 
  }
  \,.
$$



=--


+-- {: .num_theorem #EMTheorem}
###### Theorem (Eilenberg-MacLane)

Given a [[simplicial abelian group]] $A$, then the inclusion 

$$
  i \colon N A \hookrightarrow C A
$$

of the normalized chain complex, def. \ref{NormalizedChainComplexOnGeneralGroup} into the full alternating face map complex, def. \ref{AlternatingFaceMapComplex},
is a [[natural transformation|natural]] [[quasi-isomorphism]] and in fact a natural chain [[homotopy equivalence]], i.e. the complex $D_\bullet(X)$ is [[null homotopy|null-homotopic]] (a [[contractible chain complex]]).

=--

([Goerss-Jardine, theorem III 2.4](#GoerssJardine))

+-- {: .proof}
###### Proof

Following the proof of ([Goerss-Jardine, theorem III 2.1](#GoerssJardine)) we look for each $n \in \mathbb{N}$ and each $j \lt n$ at the  groups

$$
  N_n(A)_j \coloneqq  \cap_{i=0}^j ker (d_i) \subset A_n
$$

and similarly at

$$
  D_n(A)_j = \{s_{i}\}_{i \leq j}(A_{n-1}) \subset A_n
  \,,
$$ 

the subgroup generated by the first $j$ degeneracies.

For $j= n-1$ these coincide with $N_n(A)$ and with $D_n(A)$, respectively.  We show by induction on $j$ that the composite

$$
  N_n(A)_j \hookrightarrow A_n \stackrel{}{\to} A_n/D_n(A)_j
$$

is an isomorphism of all $j \lt n$. For $j = n-1$ this is then the desired result.

(...)

=--

+-- {: .num_cor}
###### Corollary

Given a [[simplicial abelian group]] $A$, then the projection [[chain map]]

$$
  (C A) \longrightarrow (C A)/(D A)
$$

from its alternating face maps complex, def. \ref{AlternatingFaceMapComplex}, to the alternating face map complex modulo degeneracies, def. \ref{ComplexModuloDegeneracies}, is a [[quasi-isomorphism]].

=--

+-- {: .proof}
###### Proof

Consider the pre-composition of the map with the inclusion of the 
normalized chain complex, def. \ref{NormalizedChainComplexOnGeneralGroup}.

$$
  \array{
    C A &\stackrel{p}{\longrightarrow}& (C A)/(D A)
    \\
    {}^{\mathllap{i}}\uparrow & \nearrow
    \\
    N A 
  }
$$

By theorem \ref{EMTheorem} the vertical map is a [[quasi-isomorphism]] and by prop. \ref{NormalizedIntoModuloDegeneraciesIsIsomorpism} the composite diagonal map is an [[isomorphism]], hence in particular also a [[quasi-isomorphism]]. Since quasi-isomorphisms satisfy the [[two-out-of-three]] property, it follows that also the map in question is a quasi-isomorphism.

=--



### Equivalence of categories

+-- {: .num_prop }
###### Proposition

The [[normalized chain complex]] [[functor]] of def. \ref{NormalizedChainComplexOnGeneralGroup} restricts on [[simplicial abelian groups]] to an [[equivalence of categories]]

$$
  N \colon 
  sAb \stackrel{\simeq}{\longrightarrow} Ch_\bullet^+(A)
$$

between [[sAb]] and the [[category of chain complexes]] in non-negative degree.

=--

This is the statement of the _[[Dold-Kan correspondence]]_. See there for details.


### Homology and homotopy groups

Notice that the [[simplicial set]] underlying any [[simplicial group]] $G$ (as described there) is a [[Kan complex]]. Write

$$
  \pi_n(G) \;\;\; n \in \mathbb{N}
$$

for the $n$-th [[simplicial homotopy group]] of $G$. Notice that due to the group structure of $G$ in this case also $\pi_0(G)$ is indeed canonically a group, not just a set.

+-- {: .num_prop }
###### Proposition

For $A$ a simplicial abelian group there are [[natural isomorphism]]s

$$
  \pi_n(A,0) \simeq H_n(N A) \simeq H_n(A)
$$

between the [[simplicial homotopy group]]s and the [[chain homology]] groups of the unnormalized and of the normalized chain complexes.

=--

+-- {: .proof}
###### Proof

The first isomorphism follows with the [[Eckmann-Hilton argument]]. The second directly from the [Eilenberg-MacLane theorem](#EMTheorem) above.

=--

+-- {: .num_remark }
###### Remark

Both $sAb$ as well as $Ch_\bullet^+$ are naturally [[categories with weak equivalences]] given by those morphisms that induce [[isomorphism]]s on all [[simplicial homotopy group]] and on all [[chain homology]] groups, respectively. So the above statement says that the Moore complex functor $N$ respects these weak equivalences.

In fact, it induces an equivalence of categories also on the corresponding [[homotopy categories]]. And even better, it induces a [[Quillen equivalence]] with respect to the standard [[model category]] structures that refine the structures of categories of weak equivalences. All this is discussed at [[Dold-Kan correspondence]]. 

=--

### Hypercrossed complex structure {#HypercrossedComplex}

+-- {: .num_prop }
###### Proposition

The Moore complex of a [[simplicial group]] is naturally a [[hypercrossed complex]].

=--

This has been established in ([Carrasco-Cegarra](#Carrasco-Cegarra)). In fact, the analysis of the Moore complex and what is necessary to rebuild the simplicial group from its Moore complex is the origin of the abstract motion of hypercrossed complex, so our stated proposition is almost a tautology!

Typically one has pairings  $N G_p \times N G_q \to N G_{p+q}$. These use the [[Conduché decomposition theorem]], see the discussion at [[hypercrossed complex]].



These Moore complexes are easily understood in low dimensions:

* Suppose that $G$ is a simplicial group with Moore complex $N G$, which satisfies $N G_k = 1$ for $k\gt 1$, then $(G_1,G_0,d_1,d_0)$ has the structure of a [[2-group]]. The [[interchange law]] is satisfied since the corresponding equation in $G_1$ is always the image of an element in $N G_2$, and here that must be trivial. If one thinks of the 2-group as being specified by a [[crossed module]] $(C,P,\delta, a)$, then in terms of the original simplicial group, $G$,  $N G_0 = G_0 = P$, $N G_1 \cong C$, $ \partial = \delta$ and the action of $P$ on $C$ translates to an action of $N G_0$ on $N G_1$ using conjugation by $s_0(p)$, i.e., for $p\in G_0$ and $c\in N G_1$, 
$$a(p)(c) = s_0(p)c s_0(p)^{-1}.$$


* Suppose next that $N G_k = 1$ for $k \gt 2$, then the Moore complex is a [[2-crossed module]]. 

## Examples
 {#Examples}

+-- {: .num_example #ChainsOnThe1Simplex}
###### Example

Consider the 1-[[simplex]] $\Delta[1]$ regarded as a [[simplicial set]], and write $\mathbb{Z}[\Delta[1]]$ for the [[simplicial abelian group]] which in each degree is the [[free abelian group]] on the simplices in $\Delta[1]$.

This simplicial abelian group starts out as

$$
  \mathbb{Z}[\Delta[1]]
  =
  \left(
     \cdots
     \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}
     \mathbb{Z}^4 \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
     \mathbb{Z}^3 \stackrel{\overset{\partial_0}{\longrightarrow}}{\underset{\partial_1}{\longrightarrow}} \mathbb{Z}^2
  \right)
$$

(where we are indicating only the face maps for notational simplicity).

Here the first $\mathbb{Z}^2 = \mathbb{Z}\oplus \mathbb{Z}$, the [[direct sum]] of two copies of the [[integers]], is the group of 0-chains generated from the two endpoints $(0)$ and $(1)$ of $\Delta[1]$, i.e. the abelian group of formal linear combinations of the form

$$
  \mathbb{Z}^2 \simeq \left\{ a \cdot (0) + b \cdot (1) | a,b \in \mathbb{Z}\right\}
  \,.
$$

The second $\mathbb{Z}^3 \simeq \mathbb{Z}\oplus \mathbb{Z}\oplus \mathbb{Z}$ is the abelian group generated from the three (!) 1-simplicies in $\Delta[1]$, namely the non-degenerate edge $(0\to 1)$ and the two degenerate cells $(0 \to 0)$ and $(1 \to 1)$, hence the abelian group of formal linear combinations of the form

$$
  \mathbb{Z}^3 \simeq \left\{ a \cdot (0\to 0) + b \cdot (0 \to 1) + c \cdot (1 \to 1) | a,b,c \in \mathbb{Z}\right\}
  \,.
$$

The two face maps act on the basis 1-cells as

$$
  \partial_1 \colon (i \to j) \mapsto (i)
$$

$$
  \partial_0 \colon (i \to j) \mapsto (j)
  \,.
$$

Now of course most of the (infinitely!) many simplices inside $\Delta[1]$ are degenerate. In fact the only non-degenerate simplices are the two 0-cells $(0)$ and $(1)$ and the 1-cell $(0 \to 1)$. Hence the alternating face maps complex modulo degeneracies, def. \ref{ComplexModuloDegeneracies}, of $\mathbb{Z}[\Delta[1]]$ is simply this:

$$
  (C (\mathbb{Z}[\Delta[1]])) / D (\mathbb{Z}[\Delta[1]]))
  =
  \left(
    \cdots
    \to
    0
    \to
    0
    \to
    \mathbb{Z}
    \stackrel{\left(1 \atop -1\right)}{\longrightarrow}
    \mathbb{Z}^2
  \right)
  \,.
$$

Notice that alternatively we could consider the topological 1-simplex $\Delta^1 = [0,1]$ and its [[singular simplicial complex]] $Sing(\Delta^1)$ in place of the smaller $\Delta[1]$, then the free simplicial abelian group $\mathbb{Z}(Sing(\Delta^1))$ of that. The corresponding alternating face map chain complex $C(\mathbb{Z}(Sing(\Delta^1)))$ is "huge" in that in each positive degree it has a free abelian group on uncountably many generators. Quotienting out the degenerate cells still leaves uncountably many generators in each positive degree (while every singular $n$-simplex in $[0,1]$ is "thin", only those whose parameterization is as induced by a degeneracy map are actually regarded as degenerate cells here). Hence even after normalization the singular simplicial chain complex is "huge". Nevertheless it is quasi-isomorphic to the tiny chain complex found above.

=--


## References

Original sources are

* [[John Moore]], _Homotopie des complexes mono&#239;daux, I._  S&#233;minaire Henri Cartan, 7 no. 2 (1954-1955), Expos&#233; No. 18, 8 p. ([numdam]( http://www.numdam.org/item?id=SHC_1954-1955__7_2_A8_0))

 * [[John Moore]], _Semi-simplicial complexes and Postnikov systems_ , Symposium international de topologia algebraica, Mexico 1958, p. 243].

* [[John Moore]], _Semi-simplicial Complexes, seminar notes_ , Princeton University 1956]

There is also a never published

* [[John C. Moore]], _Algebraic homotopy theory_.  Princeton 1956. Mimeographed notes.
[PDF](https://dmitripavlov.org/scans/moore-algebraic-homotopy-theory.pdf)

A proof by Cartan is in

* Cartan, _Quelques questions de topologies_ seminar, 1956-57   


A standard textbook reference for the abelian version is

* {#GoerssJardine} [[Paul Goerss]], [[Rick Jardine]], chapter III.2 of _[[Simplicial homotopy theory]]_ 


Notice that these authors write "normalized chain complex" for the complex that elsewhere in the literature would be called just "Moore complex", whereas what Goerss--Jardine call "Moore complex" is sometime maybe just called "alternating sum complex".

See also

* {#SchwedeShipley03} [[Stefan Schwede]], [[Brooke Shipley]], Section 2.1 of: _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv:math.AT/0209342](http://arxiv.org/abs/math.AT/0209342), [euclid:euclid.agt/1513882376](https://projecteuclid.org/euclid.agt/1513882376))



A discussion with an emphasis of the generalization to non-abelian simplicial groups is in section 1.3.3 of

* [[Tim Porter]], _[[Crossed Menagerie]]_

 
The discusson of the hypercrossed complex structure on the Moore complex of a general simplicial group is in

* {#Carrasco-Cegarra} [[Pilar Carrasco|P. Carrasco]], [[Antonio Cegarra|A. M. Cegarra]], _Group-theoretic Algebraic Models for Homotopy Types_ , J. Pure Appl. Alg., 75, (1991), 195--235


[[!redirects Moore complexes]]


[[!redirects Moore-complex]]

[[!redirects normalized chains complex]]
[[!redirects normalized chain complex]]

[[!redirects alternating face map complex]]

[[!redirects normalized chain complexe]]
[[!redirects normalized chain complexes]]

[[!redirects normalized chains complexe]]
[[!redirects normalized chains complexes]]


[[!redirects normalized cochain complex]]
[[!redirects normalized cochain complexes]]