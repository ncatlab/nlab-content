
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _2-dimensional TQFT_ is a [[TQFT|topological quantum field theory]] on [[cobordisms]] of dimension 2. 

When formulated (only) "globally" as 1-[[functors]] on a 1-[[category of cobordisms]], then 2d TQFTs have a comparativle simple classification: the [[bulk field theory]] is determined by a commutative [[Frobenius algebra]] structure on the [[finite dimensional vector space]] assigned to the circle ([Abrams 96](#Abrams96)).

However, such global 2d TQFTs with [[coefficients]]in [[Vect]] 
do not capture the 2d TQFTs of most interest in [[quantum field theory]], which instead are "[[cohomological quantum field theories]]" ([Witten 91](#Witten91)) such as the [[topological string]] [[A-model]] and [[B-model]] that participate in [[homological mirror symmetry]].

These richer 2d TQFTs are instead local TQFTs in the sense of _[[extended TQFT]]_, i.e. they are [[(∞,2)-functors]] on a suitable [[(∞,2)-category of cobordisms]], typically on "non-compact" 2-d cobordisms, meaning on those that have non-vanishing outgoing bounary. As such they are now classified by [[Calabi-Yau objects]] in an [[symmetric monoidal (infinity,2)-category]] ([Lurie 09, section 4.2](#Lurie09)). For coefficients in the [[(∞,2)-category]] of [[(∞,n)-vector space|(∞,2)-vector space]] (i.e. [[A-∞ algebras]] with [[(∞,1)-bimodules]] between them in the [[(∞,1)-category of chain complexes]]), these theories had been introduced under the name "[[TCFT]]" in ([Getzler 92](#Getzler92), [Segal 99](#Segal99)) following ideas of [[Maxim Kontsevich]], and have been classified in ([Costello 04](#Costello04)), see ([Lurie 09, theorem 4.2.11, theorem 4.2.14](#Lurie09)).



## Filtrations of the moduli space of surfaces {#FiltrationOfModuliSpace}

The following study of the behaviour of 2-dimensional TQFTs in terms of the [[topology]] of the [[moduli spaces]] of marked hyperbolic surfaces is due to [[Ezra Getzler]]. It provides a powerful way to read off various classification results for 2d QFTs from the [[homotopy groups]] of the corresponding [[modular operad]].

### $A_\infty$-monoid objects

Let  $Core$([[FinSet]]) be the [[core]] of the [[category]] of finite sets.
Under union of sets this is a [[symmetric monoidal category]]. Then for 
$C$ any [[monoidal category]], a [[symmetric monoidal functor]]

$$
 \Phi : Core(FinSet) \to C
$$ 

is a commutative [[monoid]] in $C$.

Let now $C$ be a [[category with weak equivalences]], then we can speak of a lax symmetric opmonoidal functor

$$
  \Phi : Core(FinSet) \to C
$$

if the structure maps

$$
  \Phi(n+m) \stackrel{\simeq}{\to} \Phi(m) \otimes \Phi(n)
$$

$$
  \phi(m) \stackrel{\simeq}{\to} \Phi(1)^{\otimes m}
$$

are weak equivalences. 

Segal called these "$\Delta$-objects". Since [[Carlos Simpson]] they are called
[[Segal object]]s. 

There is also [[Jim Stasheff]]'s notion of an [[A-infinity algebra]], given in terms
of [[associahedra]] $K_n$, which are $(n-2)$-dimensional [[polytope]]s.

There is naturally a filtration on these guys with 

$$
  F_0 K_n \subset F_1 K_n \subset \cdots
  \,,
$$

where $F_0 K_n$ is the set of vertices, $F_1 K_n$ the set of edges, etc.

The collection

$$
  \{
    S_\bullet(K_n)
  \}
$$

of simplicial realizations of the $K_n$ form an [[sSet]]-[[operad]] $P$.

For $X$ a [[simplicial category]] that is symmetric monoidal, a 
$P$-[[algebra over an operad]] $X$ in $C$ is an $A_\infty$-monoid object

$$
  S_\bullet(K_n) \to C_\bullet(X^{\otimes n}, X)
$$

[[Saunders MacLane|MacLane]]'s [[coherence theorem]] says or uses that if $C$ is an [[n-category]],
we may replace $K_m$ here by the $n$-filtration $F_n K_m$.


### Closed 2d quantum field theory

#### Compactified moduli spaces of Riemann surfaces

Let 

$$
  (\Sigma, (z_1, \cdots, z_n))
$$

be a [[compact space|compact]] [[orientation|oriented]] surface
with $n$ distinct marked points. Write

$$
  \mathcal{H}(\Sigma, (z_1, \cdots, z_n))
$$

for the [[moduli space]] of [[hyperbolic metric]]s with cusps at the $(z_i)$.

We have

$$
  M(\Sigma, \vec z)
  =
  \mathcal{H}(\Sigma, \vec z)/Diff_+(\Sigma, \vec z)
$$

and

$$
  M_{g,n} = \Tau_{g,n} / \Gamma^ng
  \,,
$$

where $\Tau_{g,n}$ is the [[Teichmüller space]] and $\Gamma$ the [[mapping class group]].

Here we can assume that the [[Euler characteristic]] $\chi(\Sigma without \{z_i\}) \lt 0$
because otherwise this moduli space is empty.


#### Fenchel-Nielson coordinates on moduli space

We want to parameterize Teichm&#252;ller space by cutting surfaces into pieces with 
geodesic boundaries and [[Euler characteristic]] $\xi = -1$. These building blocks 
(of hyperbolic 2d geometry) are precisely

* the 3-holed sphere;

* the 2-holed cusp;

* the 1-holed 2-cusp;

* the 3-cusp

Each surface of [[genus]] $g$ with $n$ marked points will have

* $2g - 2 + n$ generalized pants;

* $3 g - 3 + n$ closed curves.


The boundary lengths $\ell_i \in \mathbb{R}_+$ and twists 
$t_i \in \mathbb{R}$  of these pieces 
for 

$$
  1 \leq i \leq 3g-3+n
$$

constitute the [[Fenchel-Nielsen coordinates]] on 
[[Teichmüller space]] $\Tau$.

Also use $\theta_i := t_i/\ell_i \in \mathbb{R}/\mathbb{Z}$

This constitutes is a real analytic [[atlas]] of Teichm&#252;ller space. On $M$ this 
reduces to coordinates $t_i \in \mathbb{R}/{\ell_i \mathbb{Z}}$, and these
constitute a real analytic atlas of moduli space.

Allow the lengths $\ell_i$ to go to 0, but keep the angles $\theta_i$.
The resulting space is a real analytic [[manifold with corners]]
$\hat \Tau$ (due to [[Bill Harvey]]) and this constitutes a Borel-Serre
[[bordification]] of $\Tau$.

The [[mapping class group]] $\Gamma$ still acts on $\hat \Tau$ and the 
quotient $\hat M$ is an [[orbifold]] with corners, inside which still sits 
our moduli space $M$.

Kimura-Stasheff-Voronov: add a choice of 
directions at each nodal point in $\Sigma$. This removes
all automorphisms and hence we no longer have to deal with an [[orbifold]].

This yields the [[classifying stack]] $\mathcal{P}_{g,n}$ for $\Gamma_{g,n}$

Then the collection

$$
  \{
    \mathcal{P}_{g,n}
  \}
$$

is a [[modular operad]]: the operad that describes gluing of marked surfaces at
marked points together with the informaiton on how to glue marked points of a single
surface to each other.

A 2-dimensional closed [[TQFT]] is an [[algebra over an operad]] over this in 
a simplicial category, in the above sense.

This involves either the [[de Rham complex]] on $\mathcal{P}_{g,n}$ or
$S_\bullet(\mathcal{P}_{g,n})$.


Let

$$
  F_k \mathcal{P}_{g,n}
  := 
  \left\{
    [\Sigma] |
    ...
  \right\}
$$

where $\Sigma$ has $\geq 2g-2+n-k$ spheres as components (after cutting along zero-length
closed curves).

So for instance

* $F_0 \mathcal{P}_{g,n}$ is the pants-decomposition;

* $F_1 \mathcal{P}_{g,n}$ is decompositions into pants and one piece being the
  result of either gluing two pants to each other or of gluing two circles 
  of a single pant to each other.
  
  This $F_1 ..$ is a connected space, due to a theorem by Hatcher-Thurston. 
**Notice** This is equivalent to the familiar statement that a closed 2d TFT is
a commutative [[Frobenius algebra]].

* $F_2 \mathcal{P}_{g,n} $  is the decomposition into pieces as before
  together with one two-holed torus or one five-holed sphere.
  
  This space has the space [[fundamental group]] as $\mathcal{P}_{g,n}$.
  
  This is equivalent to the theorem by Moore and Seiberg about categorified
  2-d TFT.
  
+-- {: .un_theorem}
###### Theorem
([[Ezra Getzler]])

The inclusion

$$
  F_k \mathcal{P}_{g,n} \hookrightarrow \mathcal{P}_{g,n}
$$

is $k$-[[connected]].

Here a map $X\to Y$ is $k$-connected if

* $\pi_0(X) \to \pi_0(Y)$ is surjective;

* $\pi_i(X,x) \to \pi_i(Y,f(x))$ is a bijection for $i \lt k$ and surjective $i = k$.

This means precisely that the [[mapping cone]] is $k$-connected.

=--

+-- {: .proof}
###### Proof


Use the cellular decomposition of moduli space $\mathcal{M}_{g,1}$
following Mumford, Thurston, Harer, Woeditch-Epstein, Penner.

=--


Some other versions of this:

$$
  F_k \Tau_{g,n} \to \Tau_{g,n}
$$

is $k$-connected. 

One can also use [[Deligne-Mumford compactification]]s

$$
  F_k \bar \mathcal{M}_{g,n} \to \bar \mathcal{M}_{g,n}
$$

and this is also $k$-connected.


### Open-closed case

...

## Related concepts

* [[TQFT]]

  * **2d TQFT**

    * [[2d Chern-Simons theory]]

    * [[TCFT]]

      * [[A-model]], [[B-model]]

    * [[Landau-Ginzburg model]]

    * [[Levin-Wen model]]

  * [[3d TQFT]]

  * [[4d TQFT]]

## References

### Global

The [[folklore]] result that global closed 2d TQFTs with coefficients in [[Vect]] are equivalent to commutative [[Frobenius algebra]] structures is proven rigorously in 

* {#Abrams96} L. Abrams, _Two-dimensional topological quantum eld theories and Frobenius algebras_, J. Knot Theory Ramications 5 (1996) ([ps](http://home.gwu.edu/~labrams/docs/tqft.ps))

The classification result for open-closed 2d TQFTs was famously announced and sketched in 

* [[Greg Moore]], [[Graeme Segal]], _Lectures on branes, K-theory and RR charges, Clay Math Institute Lecture Notes (2002), _ ([web](http://www.physics.rutgers.edu/~gmoore/clay1/clay1.html))

A standard textbook is

* [[Joachim Kock]], _Frobenius algebras and 2D topological quantum field theory_ ([web](http://mat.uab.cat/~kock/TQFT.html), [course notes pdf](http://mat.uab.es/~kock/TQFT/FS.pdf))

A picture-rich description of what's going on is in 

* [[Aaron Lauda]] and Hendryk Pfeiffer, _Open-closed strings: two-dimensional extended TQFTs and Frobenius algebras_ , Topology Appl. 155 (2008) 623-666. ([arXiv:math.AT/0510664](http://arxiv.org/abs/math.AT/0510664))

### Local 

The local ([[extended TQFT]]) version of 2d TQFT which captures the [[topological string]] was mathematically introduced under the name "[[TCFT]]". 

The concept is essentially a formalization of what used to be called [[cohomological field theory]] in

* {#Witten91} [[Edward Witten]], _Introduction to cohomological field theory_, InternationalJournal of Modern Physics A, Vol. 6,No 6 (1991) 2775-2792 ([[WittenCQFT.pdf:file]])

The definition was given independently by 

* {#Getzler92} [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159(2), 265&#8211;285 (1994) ([arXiv:hep-th/9212043](http://arxiv.org/abs/hep-th/9212043))

and 

* {#Segal99} [[Graeme Segal]], _Topological field theory_ , (1999), Notes of lectures at Stanford university. ([web](http://www.cgtp.duke.edu/ITP99/segal/)). See in particular [lecture 5](http://www.cgtp.duke.edu/ITP99/segal/stanford/lect5.pdf) ("topological field theory with cochain values").
 
The classification of TCFTs by [[Calabi-Yau categories]] was discussed in

* {#Costello04} [[Kevin Costello]], _Topological conformal field theories and Calabi-Yau categories_ Advances in Mathematics, Volume 210, Issue 1, (2007), ([arXiv:math/0412149](http://arxiv.org/abs/math/0412149))

* [[Kevin Costello]], _The Gromov-Witten potential associated to a TCFT_ ([arXiv:math/0509264](http://arxiv.org/abs/math/0509264))

following conjectures by [[Maxim Kontsevich]], e.g.

* [[Maxim Kontsevich]], _Homological algebra of mirror symmetry_ , in Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&#252;rich, 1994), pages 120&#8211;139, Basel, 1995, Birkh&#228;user.

This classification is a precursor of the full [[cobordism hypothesis]]-theorem. This, and the reformulation of the original TCFT constructions in full generality is in 

* {#Lurie09} [[Jacob Lurie]], section 4.2 of _[[On the Classification of Topological Field Theories]]_ ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))