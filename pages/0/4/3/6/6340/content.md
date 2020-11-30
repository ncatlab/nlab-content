[[!redirects Index theory]]
[[!redirects index theory]]

> This page is about the notion of index in [[analysis]]/[[operator algebra]]. For other notions see elsewhere.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The notion of _index_ was originally defined

* _[For elliptic differential operators](#IdeaForDifferentialOperators)_

as an invariant correction of the [[kernel]] of such an operator (namely corrected by the [[cokernel]]). The definition has particularly nice properties in the special case

* _[For Dirac operators](#ForDiracOperators)_

where it coincides with the [[partition function]] of [[supersymmetric quantum mechanics]].

More generally the resulting notion is abstractly characterized as being the pairing operation ([[composition]])

* _[in KK-theory](#GeneralIdeaInKKTheory)_.

Even more generally, in [[generalized cohomology theory]] indices are given by [[genera]] and universal [[orientation in generalized cohomology]], such as for instance the [[elliptic genus]] for [[elliptic cohomology]] and the [[Witten genus]] for [[tmf]]. See at _[[genus]]_ for more on this generalized notion of indices.

There is also a quite general [[microlocal formulation of index theory]] due to Kashiwara and Schapira.

### For elliptic differential and Fredholm operators
 {#IdeaForDifferentialOperators}

The _[[analytical index]]_ of an [[elliptic operator|elliptic]] [[differential operator]] $D \colon \Gamma(E_1) \to \Gamma(E_2)$ is defined to be the the difference between the [[dimension]] of its [[kernel]] and that of its [[cokernel]]. 

One reason why this is an interesting invariant of an elliptic differential operator is that when deforming the operator by a [[compact operator]] then the dimension of both the kernel and the cokernel may change, but their difference remains the same. Hence one may think of the analytic index as a "corrected" version of its [[kernel]], such as to make it be more invariant. 

On the other hand, the _[[topological index]]_ of an elliptic differential operator $D$, is defined to be the pairing of the [[cup product]] of its [[Chern character]] and the [[Todd class]] of the base manifold with its [[fundamental class]].

More generally such analytic and topological indices are defined for [[Fredholm operators]].

The _[[Atiyah-Singer index theorem]]_ assert that these two notios of index are in fact equal.

### For Dirac operators 
 {#ForDiracOperators}

If the [[Fredholm operator]] in question happens to be
a _[[Dirac operator]]_ $D$ (such as that encoding the
[[dynamics]] of a [[spinning particle]] or more generally the [[supercharge]] of a system in [[supersymmetric quantum mechanics]]) then the index of $D$ coincides with the [[partition function]] of this quantum mechanical system, namely the [[super-trace]] of the [[heat kernel]] $\exp(-t D^2)$ of the corresponding [[Hamiltonian]] [[Laplace operator]] $D^2$ ([Berline-Getzler-Vergne 04](#BerlineGetzlerVergne04)).


+-- {: .num_prop}
###### Proposition

Let $(X,g)$ be a [[compact topological space|compact]] [[Riemannian manifold]] and $\mathcal{E}$ a smooth [[super vector bundle]] and indeed a [[Clifford module bundle]] over $X$. Consider a [[Dirac operator]] 

$$
  D \colon \Gamma(X,\mathcal{E}) \to \Gamma(X, \mathcal{E})
$$

with components (with respect to the $\mathbb{Z}_2$-[[graded vector space|grading]]) to be denoted

$$
  D = 
  \left[
    \array{
       0 & D^-
       \\
       D^+ & 0
    }
  \right]
  \,,
$$

where $D^- = (D^+)^\ast$. Then $D^+$ is a [[Fredholm operator]] and its index is the [[supertrace]] of the [[kernel]] of $D$, as well as of the [[heat kernel]] of $D^2$:

$$
  \begin{aligned}
    ind(D^+) & \coloneqq dim(ker(D^+)) - dim(coker(D^+))
   \\
   & = dim(ker(D^+)) - dim(ker(D^-))
   \\
   & = sTr(ker(D))
   \\
   & = sTr( \exp(-t \, D^2) ) \;\;\; \forall t \gt 0
  \end{aligned}
  \,.
$$

=--

This appears as
([Berline-Getzler-Vergne 04, prop. 3.48, prop. 3.50](BerlineGetzlerVergne04)), based on ([MacKean-Singer 67](#MacKeanSinger67)).

+-- {: .proof}
###### Proof 

The last step here follows from an argument which is as simple as it is paramount whenever anything involves [[supersymmetry]]:

the point is that if a (hermitean) operator $H$ has a [[supercharge]] $D$, in that $H = D^2$, then all its non-vanishing [[eigenstates]] appear in "[[supermultiplet]]" pairs of the same eigenvalue: if $|\psi\rangle$ has [[eigenvalue]] $E \gt 0$ under $H$, then 

1. $D |\psi\rangle \neq 0$ (since $D D |\psi\rangle = H |\psi\rangle = E |\psi\rangle \neq 0$);

1. also $D |\psi\rangle$ has eignevalue $E$ (since $[H,D] = 0$).

Therefore all eigenstates for non-vanishing eigenvalues appear in pairs whose members have opposite sign under the supertrace. 
So only states with $H |\psi\rangle = 0$ contribute to the supertrace. But if $H$ and $D$ are hermitean operators for a non-degenerate inner product, then it follows that $(D^2 |\psi\rangle = 0) \Leftrightarrow (D|\psi\rangle = 0)$ and hence these are precisely the states which are also annihilated by the supercharge (are in the kernel of $D$), hence are precisely only the _supersymmetric states_.

On these now the weight $\exp(- t D^2) = 1$ and hence the supertrace over this "Euclidean propagator" simply counts the number of supersymmetric states, signed by their fermion number.

=--

+-- {: .num_remark}
###### Remark

If one thinks of $D^2$ as the time-evolution [[Hamiltonian]] of a system of [[supersymmetric quantum mechanics]] with $D$ the [[supercharge]] on the [[worldline]], then $ker(D)$ is the space of supersymmetric [[quantum states]], $\exp(-t \, D^2)$ is the Euclidean time evolution operator and its [[supertrace]] is the [[partition function]] of the system. Hence we have the translation

*  index = partition function .

This kind of argument appears throughout supersymmetric quantum field theory. In dimension 2 it controls the nature of the [[Witten genus]].

=--

### General abstract definition in KK-theory
 {#GeneralIdeaInKKTheory}

The abstract [[universal property|universal]] characterization of indices is: the index is the _pairing_ in [[KK-theory]]/[[E-theory]].

More in detail, by the discussion there [[KK-theory]] ([[E-theory]]) is the [[category]] $KK$ which is the additive and split exact [[localization]] of the category [[C*Alg]] of [[C*-algebras]] at the [[compact operators]]. For $\mathbb{C}$ the base [[C*-algebra]] of [[complex numbers]] the [[morphisms]] in this category have the following equivalent meaning:

* [[morphisms]] $\mathbb{C} \to A$ are [[operator K-theory|operator K-cohomology]] classes which are represented by "[[vector bundles]] over the space represented by $A$", namely by [[Hilbert modules]] $E$ over $A$;

* [[morphisms]] $A \to \mathcal{C}$ are [[K-homology]] classes which are represented by [[Fredholm operators]] $D$;

* the [[composition]] 

  $$
    ind(D_E) 
      \;\colon\;
    \mathbb{C} \stackrel{E}{\to} A \stackrel{D}{\to} \mathbb{C}
    \;\;\;\;
    \in KK(\mathbb{C}, \mathbb{C}) \simeq \mathbb{Z}
  $$

  in the category $KK$ (hence the Kasparov product) is the _index_ of the Fredholm operator $D$ twisted by $E$.

More generally, if $B$ is some other chosen base [[C*-algebra]] then $KK(A,B)$ is the group of [[Fredholm operators]] $D$ on [[Hilbert module]] bundles over the [[C*-algebra]] $B$, and one takes the pairing

$$
  ind \coloneqq \circ_{\mathbb{C}, A, B} \;\colon\;
  KK(\mathbb{C},A) \times KK(A,B) \to KK(\mathbb{C}, B)
$$

to be the index map relative $B$. (See e.g. [Schick 05, section 6](#Schick05).) This is the case that the [[Mishchenko-Fomenko index theorem]] applies to.

And hence even more generally one may regard _any_ composition in $KK$ as as a generalized index map. Via the universal characterizatin of $KK$ itself, this then gives a fundamental and general abstract characterization of the notion of index:

_The index pairing is the [[composition]] operation in the [[KK-theory|KK-]][[localization of a category|localization]] of [[C*Alg]], hence in [[noncommutative stable homotopy theory]].


## Related pages

* [[topological index]]

* [[analytical index]]

* [[fiber integration in K-theory]]

* [[index of a Dirac operator]]

* [[index theorem]]

  * [[Atiyah-Singer index theorem]]

  * [[Mishchenko-Fomenko index theorem]]

  * [[Baum-Connes conjecture]]

* [[zeta function of an elliptic differential operator]], [[eta function]]

* [[Poincaré–Hopf index theorem]]

* [[Gauss-Bonnet theorem]]

[[!include genera and partition functions - table]]


## References

Original articles include

* [[Michael Atiyah]], [[Isadore Singer]], _Index theory for skew-adjoint Fredholm operators_  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/askew.pdf))

With an eye towards application in [[mathematical physics]]:

* [[Mikio Nakahara]], Chapter 12 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)


Lecture notes include

* [[Jean-Michel Bismut]], _Introduction to index theory_, lecture notes ([pdf](http://www.math.leidenuniv.nl/~ajavanp/Notes_Index_TheoryBotao.pdf))

A general introduction with an emphasis of indices as [[Gysin maps]]/[[fiber integration]]/[[Umkehr maps]] is in 

* [[Chris Kottke]], _Talbot Workshop 2010 Talk 2: K-Theory and Index Theory_ ([arXiv:1010.5002](http://arxiv.org/abs/1010.5002))
 {#Kottke}

Textbook accounts include chapter III of

* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], _[[Spin geometry]]_, Princeton University Press (1989)


A standard textbook account of the description of indices of [[Dirac operators]] as [[partition functions]] in [[supersymmetric quantum mechanics]] is 

* [[Nicole Berline]], [[Ezra Getzler]], [[Michèle Vergne]], _Heat Kernels and Dirac Operators_, Springer Verlag Berlin (2004)
  {#BerlineGetzlerVergne04}

based on original articles including

* {#MacKeanSinger67} H. MacKean, [[Isadore Singer]], _Curvature and eigenvalues of the Laplacian_, J. Diff. Geom. 1 (1967)
 

* {#AtiyahBott73} [[Michael Atiyah]], [[Raoul Bott]], [[Vijay Patodi]], _On the heat equation and the index theorem_, Invent. Math. 19 (1973), 279&#8211;330
 

* {#AlvarezGaume83} [[Luis Alvarez-Gaumé]], _Supersymmetry and the Atiyah-Singer index theorem_, Comm. Math. Phys. Volume 90, Number 2 (1983), 161-173. ([Euclid](http://projecteuclid.org/euclid.cmp/1103940278))
 

* {#Getzler83} [[Ezra Getzler]], _Pseudodifferential operators on supermanifolds and the Atiyah-Singer index theorem_, Comm. Math. Phys. 92 (1983), 163-178. ([pdf](http://math.northwestern.edu/~getzler/Papers/1103940796.pdf))
 

* [[D. Quillen]], _Superconnections and the Chern character_ Topology 24 (1985), no. 1, 89&#8211;95; 

* [[Varghese Mathai]], [[Daniel Quillen]], _Superconnections, Thom classes, and equivariant differential forms_. Topology 25 (1986),
no. 1, 85&#8211;110; 

*  [[Ezra Getzler]], _A short proof of the Atiyah-Singer index theorem_, Topology 25 (1986), 111-117 ([pdf](http://math.northwestern.edu/~getzler/Papers/local.pdf))
 {#Getzler86}


* [[D. Quillen]], _Superconnection character forms and the Cayley transform_. Topology 27
(1988), no. 2, 211&#8211;238



For the more general discussion of indices of [[elliptic complexes]] see

* [[Peter Gilkey]], _Invariance theory, the heat equation, and the Atiyah-Singer index theorem_ ([pdf](http://pages.uoregon.edu/gilkey/dirPDF/InvarianceTheory1Ed.pdf))

An explicit formula in [[Chern-Weil theory]] for indices of differential operators on [[Hilbert modules]]-bundles is discussed in detail in 

* [[Thomas Schick]], _$L^2$-index, KK-theory, and connections_, New York J. Math. 11 (2005) ([arXiv:math/0306171](http://arxiv.org/abs/math/0306171))
 {#Schick05}

A standard textbook account in the context of [[KK-theory]] is in section 24.1 of 

* [[Bruce Blackadar]], _[[K-Theory for Operator Algebras]]_


[[!redirects indices]]

[[!redirects index theory]]
[[!redirects index theories]]