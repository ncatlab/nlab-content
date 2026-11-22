
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


\tableofcontents


## Idea

The *Waldhausen $S_\bullet$-construction* ([Waldhausen 85, §1.3](#Waldhausen85)) is a procedure that produces [[algebraic K-theory]] (as an [[infinite loop space]] or [[connective spectrum]]) from a [[category]] or [[(infinity,1)-category|$(\infty,1)$-category]] $\mathcal{C}$ equipped with a notion of [[homotopy cofiber|cofiber sequences]].

In degree $n$, the [[simplicial object]] $S_\bullet \mathcal{C}$ consists of length-$n$ filtrations

$$
  0
    \hookrightarrow
  A_1
    \hookrightarrow
  A_2
    \hookrightarrow
  \cdots
    \hookrightarrow
  A_n
$$

together with choices of all their subquotients $A_j/A_i$. Hence the [[geometric realization]] $\left\vert S_\bullet \mathcal{C} \right\vert$ (of the [[core]] or of the subcategory of weak equivalences, see [below](#Definition)) has a single vertex, one edge for each object $A$ of $\mathcal{C}$, and one 2-simplex for each cofiber sequence $A \hookrightarrow B \twoheadrightarrow B/A$, whose three edges are $A$, $B$ and $B/A$. Therefore, in the [[fundamental group]] of $\left\vert S_\bullet \mathcal{C}\right\vert$ the relation

$$
  [B] \,=\, [A] + [B/A]
$$

holds, which is the defining relation of the [[Grothendieck group]] $K_0(\mathcal{C})$, while the higher simplices coherently relate these relations. Accordingly, the *algebraic K-theory space* of $\mathcal{C}$ is the [[loop space]]

$$
  K(\mathcal{C})
  \;\coloneqq\;
  \Omega \left\vert S_\bullet \mathcal{C} \right\vert
  \,,
$$

whose homotopy groups $K_n(\mathcal{C}) \coloneqq \pi_n K(\mathcal{C}) = \pi_{n+1} \left\vert S_\bullet \mathcal{C} \right\vert$ are the *algebraic K-groups* of $\mathcal{C}$, starting with $K_0(\mathcal{C}) \simeq \pi_1 \left\vert S_\bullet \mathcal{C} \right\vert$ ([Weibel 13, Prop. IV.8.4](#Weibel13)).

Waldhausen describes the passage from $\mathcal{C}$ to $\Omega \left\vert S_\bullet \mathcal{C} \right\vert$ as reminiscent of, and in part motivated by, the [[group completion]] of [[Graeme Segal]]'s [[Gamma-space|$\Gamma$-space]] machine ([Segal 74](#Segal74)). The difference is that it imposes additivity over all cofiber sequences, not just over [[direct sum|direct sums]] ([Waldhausen 85, §1.3, §1.8](#Waldhausen85)).

The construction can take as input any of the following kinds of data:

* [[Waldhausen category]] ([below](#ForWaldhausenCategories))

* [[Waldhausen (infinity,1)-category|Waldhausen $(\infty,1)$-category]] ([Barwick 16](#Barwick16))

* [[stable (infinity,1)-category|stable $(\infty,1)$-category]] ([below](#ForStableInfinityCategories))

* [[stable derivator]] ([Maltsiniotis 07](#Maltsiniotis07), [Garkusha 07](#Garkusha07), [Muro & Raptis 17](#MuroRaptis17))


## Definition
 {#Definition}

### For Waldhausen categories
 {#ForWaldhausenCategories}

For $n \in \mathbb{N}$, write $\mathrm{Ar}[n] \coloneqq \mathrm{Fun}\big([1],[n]\big)$ for the [[arrow category]] of $[n] = \{0 \lt 1 \lt \cdots \lt n\}$, hence for the [[poset]] of pairs $(i,j)$ with $0 \leq i \leq j \leq n$, where $(i,j) \leq (i',j')$ iff $i \leq i'$ and $j \leq j'$.

+-- {: .num_defn #SConstructionOfWaldhausenCategory}
###### Definition
**(S-construction of a Waldhausen category)**
\linebreak
Let $\mathcal{C}$ be a [[Waldhausen category]], with [[zero object]] $0$, cofibrations denoted $\hookrightarrow$, and subcategory of weak equivalences $\mathrm{w}\mathcal{C}$.

1. $S_n \mathcal{C}$ is the category whose objects are the [[functor|functors]]

   $$
     A \,\colon\, \mathrm{Ar}[n] \longrightarrow \mathcal{C}
     \,,
     \;\;\;\;\;
     (i,j) \mapsto A_{i,j}
   $$

   such that

   * $A_{j,j} = 0$ for all $j$,

   * for all $i \leq j \leq k$ the morphism $A_{i,j} \to A_{i,k}$ is a cofibration and the square

     $$
       \array{
         A_{i,j} &\hookrightarrow& A_{i,k}
         \\
         \big\downarrow && \big\downarrow
         \\
         0 = A_{j,j} &\hookrightarrow& A_{j,k}
       }
     $$

     is a [[pushout]], hence $A_{i,j} \hookrightarrow A_{i,k} \twoheadrightarrow A_{j,k}$ is a cofiber sequence,

   and whose morphisms are the [[natural transformation|natural transformations]] between these.

1. $\mathrm{w}S_n \mathcal{C} \subset S_n \mathcal{C}$ is the subcategory of those natural transformations $A \to A'$ all of whose components $A_{i,j} \to A'_{i,j}$ are weak equivalences.

Since $[n] \mapsto \mathrm{Ar}[n]$ is a [[cosimplicial object|cosimplicial]] poset, these categories form [[simplicial object|simplicial objects]] $S_\bullet \mathcal{C}$ and $\mathrm{w}S_\bullet \mathcal{C}$ in [[Cat]].

=--

([Waldhausen 85, §1.3](#Waldhausen85), [Weibel 13, Def. IV.8.3](#Weibel13))

+-- {: .num_remark #ExplicitDescription}
###### Remark
**(explicit description)**
\linebreak
An object of $S_n \mathcal{C}$ is equivalently a sequence of cofibrations

$$
  A_{0,1} \hookrightarrow A_{0,2} \hookrightarrow \cdots \hookrightarrow A_{0,n}
$$

together with a choice of all quotients $A_{i,j} \simeq A_{0,j}/A_{0,i}$, as shown here for $n = 3$:

$$
  \array{
    A_{0,1} &\hookrightarrow& A_{0,2} &\hookrightarrow& A_{0,3}
    \\
    && \big\downarrow && \big\downarrow
    \\
    && A_{1,2} &\hookrightarrow& A_{1,3}
    \\
    && && \big\downarrow
    \\
    && && A_{2,3}
  }
$$

In these terms ([Waldhausen 85, §1.3](#Waldhausen85)):

* for $0 \lt i \leq n$, the face map $d_i \colon S_n\mathcal{C} \to S_{n-1}\mathcal{C}$ drops $A_{0,i}$ from the sequence,

* the face map $d_0$ is "quotient by $A_{0,1}$", replacing the sequence by $A_{1,2} \hookrightarrow \cdots \hookrightarrow A_{1,n}$.

In low degrees:

* $S_0 \mathcal{C}$ is the trivial category (one object, one morphism), so that $\left\vert \mathrm{w}S_0 \mathcal{C} \right\vert = \ast$,

* $S_1 \mathcal{C} \simeq \mathcal{C}$,

* $S_2 \mathcal{C}$ is the category of cofiber sequences $A_{0,1} \hookrightarrow A_{0,2} \twoheadrightarrow A_{1,2}$, and the three face maps $S_2 \mathcal{C} \to S_1 \mathcal{C} \simeq \mathcal{C}$ send such a sequence to $d_0 = A_{1,2}$, $d_1 = A_{0,2}$ and $d_2 = A_{0,1}$, respectively.

Moreover, each $S_n \mathcal{C}$ is itself a Waldhausen category, so that $S_\bullet \mathcal{C}$ is a simplicial Waldhausen category ([Waldhausen 85, §1.3](#Waldhausen85)).

=--

+-- {: .num_defn #WaldhausenKTheory}
###### Definition
**(Waldhausen K-theory)**
\linebreak
The *algebraic K-theory space* of a Waldhausen category $\mathcal{C}$ is the [[loop space]]

$$
  K(\mathcal{C})
  \;\coloneqq\;
  \Omega \left\vert \mathrm{w}S_\bullet \mathcal{C} \right\vert
$$

of the [[geometric realization]] of the [[bisimplicial set]] $\big([n],[m]\big) \mapsto N_m\big(\mathrm{w}S_n \mathcal{C}\big)$ (degreewise [[nerve]]), based at its unique vertex. Its homotopy groups are the *K-groups* $K_n(\mathcal{C}) \coloneqq \pi_n K(\mathcal{C}) = \pi_{n+1} \left\vert \mathrm{w}S_\bullet \mathcal{C} \right\vert$.

=--

([Waldhausen 85, §1.3](#Waldhausen85), [Weibel 13, Def. IV.8.5](#Weibel13))

+-- {: .num_remark #KTheorySpectrum}
###### Remark
**(K-theory spectrum)**
\linebreak
Since $S_\bullet \mathcal{C}$ is a simplicial Waldhausen category, the construction can be iterated, giving multisimplicial categories $\mathrm{w}S^{(n)}_\bullet \mathcal{C} \coloneqq \mathrm{w}S_\bullet \cdots S_\bullet \mathcal{C}$ ($n$-fold). In each new $S_\bullet$-direction the 1-skeleton is the [[suspension]] of the previous stage (by $S_0 = \ast$ and $S_1 \simeq \mathrm{id}$), and the resulting inclusions $\Sigma \left\vert \mathrm{w}S^{(n)}_\bullet \mathcal{C} \right\vert \hookrightarrow \left\vert \mathrm{w}S^{(n+1)}_\bullet \mathcal{C} \right\vert$ make the sequence of spaces

$$
  \mathbf{K}(\mathcal{C})_n
  \;\coloneqq\;
  \left\vert \mathrm{w}S^{(n)}_\bullet \mathcal{C} \right\vert
$$

a [[sequential spectrum]], whose $n$th space is $(n-1)$-connected. By the [additivity theorem](#AdditivityTheorem), this is an [[Omega-spectrum|$\Omega$-spectrum]] beyond the zeroth term: the adjoint structure maps $\mathbf{K}(\mathcal{C})_n \to \Omega\, \mathbf{K}(\mathcal{C})_{n+1}$ are weak equivalences for $n \geq 1$ ([Waldhausen 85, §1.3 with Prop. 1.5.3](#Waldhausen85)). Hence $K(\mathcal{C}) \simeq \Omega^\infty \mathbf{K}(\mathcal{C})$ is an [[infinite loop space]], and the [[connective spectrum]] $\mathbf{K}(\mathcal{C})$ is the *algebraic K-theory spectrum* of $\mathcal{C}$.

The first map $\left\vert \mathrm{w}\mathcal{C} \right\vert \to \Omega \left\vert \mathrm{w}S_\bullet \mathcal{C} \right\vert$ is in general not an equivalence; it is the K-theoretic analogue of a [[group completion]].

=--


### For stable $(\infty,1)$-categories
 {#ForStableInfinityCategories}

For $\mathcal{C}$ a [[stable (infinity,1)-category|stable $(\infty,1)$-category]] (or more generally a [[pointed object|pointed]] $(\infty,1)$-category with [[finite colimit|finite colimits]], [Lurie 14, Lec. 16](#Lurie14)), all morphisms serve as cofibrations and the equivalences as weak equivalences, so that the above definition becomes:

+-- {: .num_defn #SConstructionOfStableInfinityCategory}
###### Definition
**(S-construction of a stable $(\infty,1)$-category)**
\linebreak
$S_n \mathcal{C} \subset \mathrm{Fun}\big(\mathrm{Ar}[n], \mathcal{C}\big)$ is the full sub-$(\infty,1)$-category on those functors $A$ with $A_{j,j} \simeq 0$ for all $j$ and such that all squares as [above](#SConstructionOfWaldhausenCategory) are [[homotopy pushout|pushouts]] (equivalently, in the stable case, [[homotopy pullback|pullbacks]]). The *algebraic K-theory space* of $\mathcal{C}$ is

$$
  K(\mathcal{C})
  \;\coloneqq\;
  \Omega \left\vert \big(S_\bullet \mathcal{C}\big)^{\simeq} \right\vert
  \,,
$$

where $(-)^\simeq$ denotes the [[core]] and ${\vert-\vert}$ the [[geometric realization]] ([[(infinity,1)-colimit|$(\infty,1)$-colimit]]) of the resulting simplicial [[infinity-groupoid|$\infty$-groupoid]].

=--

([BGT 13, §7.1](#BGT13), [Barwick 16](#Barwick16), [Lurie 14, Lec. 16](#Lurie14))

As in [this Remark](#ExplicitDescription), restriction to the first row, $A \mapsto \big(A_{0,1} \to A_{0,2} \to \cdots \to A_{0,n}\big)$, is an equivalence

$$
  S_n \mathcal{C}
  \;\simeq\;
  \mathrm{Fun}\big(\Delta^{n-1}, \mathcal{C}\big)
  \,,
$$

since all the quotients are determined up to contractible choice ([Lurie 14, Lec. 16, Rem. 6](#Lurie14)). For Waldhausen categories with suitable models, Waldhausen K-theory agrees with the K-theory of the underlying $(\infty,1)$-category ([BGT 13, §7.2](#BGT13)).

+-- {: .num_remark #RelationToTheNerve}
###### Remark
**(relation to the nerve)**
\linebreak
Beware that $(S_\bullet \mathcal{C})^\simeq$ is *not* the [[complete Segal space]] $[n] \mapsto \mathrm{Fun}(\Delta^n, \mathcal{C})^\simeq$ of $\mathcal{C}$. The geometric realization of the latter is the [[classifying space]] $\left\vert \mathcal{C} \right\vert$ of $\mathcal{C}$ (the $\infty$-groupoid obtained by inverting all morphisms), which is [[contractible]] as soon as $\mathcal{C}$ has an [[initial object]] or [[terminal object]], such as a [[zero object]].

Instead, the two are related by a shift of degrees: by the above equivalence, $S_{n+1} \mathcal{C} \simeq \mathrm{Fun}(\Delta^n, \mathcal{C})$, compatibly with all face and degeneracy maps except $d_0$ and $s_0$ of $S_\bullet \mathcal{C}$. This means that the complete Segal space of $\mathcal{C}$ is the [[décalage]] ("path object") $P(S_\bullet \mathcal{C})^\simeq$ of $(S_\bullet \mathcal{C})^\simeq$, which discards $d_0$ and $s_0$ ([Lurie 14, Lec. 16, Rem. 8](#Lurie14)). Generally, the décalage $P X_\bullet$ of a simplicial object is simplicially homotopy equivalent to the constant simplicial object on $X_0$ ([Waldhausen 85, Lemma 1.5.1](#Waldhausen85)). Here $X_0 = (S_0 \mathcal{C})^\simeq \simeq \ast$, consistent with $\left\vert \mathcal{C} \right\vert \simeq \ast$.

So the K-theoretic information sits in the face map $d_0$, which is invisible to the nerve. It sends a sequence $A_{0,1} \to A_{0,2} \to \cdots \to A_{0,n}$ to the sequence $A_{0,2}/A_{0,1} \to \cdots \to A_{0,n}/A_{0,1}$ of quotients by its first term. The canonical map $\mathcal{C}^\simeq \to K(\mathcal{C})$ arises from the sequence $(S_1\mathcal{C})^\simeq \to \left\vert P(S_\bullet \mathcal{C})^\simeq \right\vert \simeq \ast \to \left\vert (S_\bullet \mathcal{C})^\simeq \right\vert$ ([Waldhausen 85, §1.5](#Waldhausen85)).

=--


## Properties
 {#Properties}

### Additivity
 {#Additivity}

+-- {: .num_prop #AdditivityTheorem}
###### Proposition
**(additivity theorem)**
\linebreak
For $\mathcal{C}$ a Waldhausen category, the functor $S_2 \mathcal{C} \longrightarrow \mathcal{C} \times \mathcal{C}$ which sends a cofiber sequence $A \hookrightarrow B \twoheadrightarrow B/A$ to the pair $(A, B/A)$ induces a homotopy equivalence

$$
  \left\vert \mathrm{w}S_\bullet \big(S_2 \mathcal{C}\big) \right\vert
  \overset{\sim}{\longrightarrow}
  \left\vert \mathrm{w}S_\bullet \mathcal{C} \right\vert
  \times
  \left\vert \mathrm{w}S_\bullet \mathcal{C} \right\vert
  \,.
$$

Equivalently, for every cofiber sequence $F' \to F \to F''$ of exact functors, the map $\left\vert \mathrm{w}S_\bullet F \right\vert$ is homotopic to $\left\vert \mathrm{w}S_\bullet (F' \vee F'') \right\vert$, where $F' \vee F''$ is the objectwise coproduct of functors.

=--

([Waldhausen 85, Prop. 1.3.2, Thm. 1.4.2](#Waldhausen85); for $(\infty,1)$-categories: [Lurie 14, Lec. 17](#Lurie14), [Barwick 16](#Barwick16))

The additivity theorem is what makes $\mathbf{K}(\mathcal{C})$ an $\Omega$-spectrum ([this Remark](#KTheorySpectrum)). In the universal characterization of connective K-theory as the universal additive invariant of stable $(\infty,1)$-categories, the $S_\bullet$-construction becomes the [[suspension]] in the $(\infty,1)$-category of additive [[noncommutative motive|noncommutative motives]] ([BGT 13, §7](#BGT13)).


### Comparison to other constructions
 {#ComparisonToOtherConstructions}

* For an [[exact category]] $\mathcal{A}$, regarded as a Waldhausen category with cofibrations the admissible monomorphisms and weak equivalences the isomorphisms, there is a natural homotopy equivalence $\left\vert \mathrm{i}S_\bullet \mathcal{A} \right\vert \simeq \left\vert Q \mathcal{A} \right\vert$ with Quillen's [[Quillen Q-construction|Q-construction]]. Hence Waldhausen K-theory agrees with Quillen K-theory in this case ([Waldhausen 85, §1.9](#Waldhausen85), [Weibel 13, IV.8.6](#Weibel13)).

* For the comparison with K-theory via Segal's group completion in the case of split cofibrations, see [Waldhausen 85, §1.8](#Waldhausen85).


### Higher structure
 {#HigherStructure}

* $S_\bullet \mathcal{C}$ is a [[higher Segal space|2-Segal space]] (but in general not a [[Segal space]]), and as such it underlies the construction of [[Hall algebra|Hall algebras]] ([Dyckerhoff & Kapranov 19](#DyckerhoffKapranov19)).

* For $\mathcal{C}$ stable, $S_\bullet \mathcal{C}$ refines to a paracyclic object, which yields "rotation invariance" of K-theory: the K-theory functor is equivariant with respect to a [[circle group|$S^1$]]-action on stable $(\infty,1)$-categories (and the trivial action on spaces) under which the generator of $\pi_1(S^1)$ acts by double [[suspension]] $\Sigma^2$ ([Lurie, Rotation invariance](#LurieRotation)). Related cyclic symmetries are discussed in [Nadler 15](#Nadler15).

* Under a [[categorified Dold-Kan correspondence]], $S_\bullet \mathcal{C}$ is the categorified nerve of the chain complex of stable $(\infty,1)$-categories given by $\mathcal{C}$ concentrated in degree 1 ([Dyckerhoff 21, Intro. and Ex. 3.27](#Dyckerhoff17)). This is in analogy to how, under the ordinary [[Dold-Kan correspondence]], an abelian group in degree 1 corresponds to its [[bar construction]].


## Related

* [[algebraic K-theory]]

* [[Waldhausen category]]

* [[Quillen Q-construction]]

* [[K-theory of a stable (infinity,1)-category|K-theory of a stable $(\infty,1)$-category]]

* [[higher Segal space]]

* [[categorified Dold-Kan correspondence]]



## References

### Original article

* {#Waldhausen85} [[Friedhelm Waldhausen]]: *Algebraic K-theory of spaces*, in: A. Ranicki, N. Levitt, F. Quinn (eds.): *Algebraic and Geometric Topology*, Proceedings of a Conference held at Rutgers University, New Brunswick, USA, July 6-13, 1983, Lecture Notes in Mathematics **1126**, Springer (1985) 318-419 &lbrack;[doi:10.1007/BFb0074449](https://doi.org/10.1007/BFb0074449), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/surgery/rutgers/wald.pdf), [pdf](http://www.math.uni-bielefeld.de/~fw/LNM1126_318-419.pdf)&rbrack;

  (the S-construction is defined in §1.3, the additivity theorem is in §1.4, deloopings are in §1.5, the relation to Segal's group completion is in §1.8 and the relation to the Q-construction is in §1.9)

Precursor, by which the S-construction was in part motivated:

* {#Segal74} [[Graeme Segal]]: *Categories and cohomology theories*, Topology **13** (1974) 293-312 &lbrack;<a href="https://doi.org/10.1016/0040-9383(74)90022-6">doi:10.1016/0040-9383(74)90022-6</a>, [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/segalcat.pdf)&rbrack;


### Reviews and textbook accounts

* {#ThomasonTrobaugh90} [[R. W. Thomason]], Thomas Trobaugh: §1 of: *Higher algebraic K-theory of schemes and of derived categories*, in: *The Grothendieck Festschrift* Vol. III, Progress in Mathematics **88**, Birkhäuser (1990) 247-435, reprinted in: Modern Birkhäuser Classics, Birkhäuser (2007) &lbrack;[doi:10.1007/978-0-8176-4576-2_10](https://doi.org/10.1007/978-0-8176-4576-2_10), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/tt.pdf)&rbrack;

* {#Weibel13} [[Charles Weibel]]: §IV.8 of: *The K-book: An introduction to algebraic K-theory*, Graduate Studies in Mathematics **145**, American Mathematical Society (2013) &lbrack;[ISBN:978-0-8218-9132-2](https://bookstore.ams.org/gsm-145), [webpage](https://sites.math.rutgers.edu/~weibel/Kbook.html), [pdf](https://sites.math.rutgers.edu/~weibel/Kbook/Kbook.IV.pdf)&rbrack;

* {#OzornovaRovelli24} [[Viktoriya Ozornova]], [[Martina Rovelli]]: *Waldhausen's $S_\bullet$-construction*, expository contribution to the proceedings of the workshop *Higher Segal Spaces and their Applications to Algebraic K-theory, Hall Algebras, and Combinatorics* &lbrack;[arXiv:2412.17398](https://arxiv.org/abs/2412.17398)&rbrack;


### For Waldhausen $(\infty,1)$-categories and stable $(\infty,1)$-categories

* {#Barwick16} [[Clark Barwick]]: *On the algebraic K-theory of higher categories*, Journal of Topology **9** 1 (2016) 245-347 &lbrack;[arXiv:1204.3607](https://arxiv.org/abs/1204.3607), [doi:10.1112/jtopol/jtv042](https://doi.org/10.1112/jtopol/jtv042)&rbrack;

* {#BGT13} [[Andrew J. Blumberg]], [[David Gepner]], [[Goncalo Tabuada]]: *A universal characterization of higher algebraic K-theory*, Geometry & Topology **17** (2013) 733-838 &lbrack;[arXiv:1001.2282](https://arxiv.org/abs/1001.2282), [doi:10.2140/gt.2013.17.733](https://doi.org/10.2140/gt.2013.17.733)&rbrack;

* {#Lurie14} [[Jacob Lurie]]: *Algebraic K-Theory and Manifold Topology*, lecture notes, Harvard (2014) &lbrack;[webpage](https://people.math.harvard.edu/~lurie/281.html)&rbrack;, in particular: Lecture 16: *Higher K-Theory of $\infty$-Categories* &lbrack;[pdf](https://www.math.ias.edu/~lurie/281notes/Lecture16-Higher.pdf)&rbrack; and Lecture 17: *The Additivity Theorem*


### For stable derivators

* {#Maltsiniotis07} [[Georges Maltsiniotis]]: *La K-théorie d'un dérivateur triangulé* (with an appendix by [[Bernhard Keller]]), in: *Categories in Algebra, Geometry and Mathematical Physics*, Contemporary Mathematics **431**, American Mathematical Society (2007) 341-368 &lbrack;[pdf](https://webusers.imj-prg.fr/~georges.maltsiniotis/ps/streetfest.pdf)&rbrack;

* {#Garkusha07} [[Grigory Garkusha]]: *Systems of diagram categories and K-theory. I*, St. Petersburg Mathematical Journal **18** (2007) 957-997 &lbrack;[arXiv:math/0401062](https://arxiv.org/abs/math/0401062), [doi:10.1090/S1061-0022-07-00978-8](https://doi.org/10.1090/S1061-0022-07-00978-8)&rbrack;

* {#MuroRaptis17} [[Fernando Muro]], [[George Raptis]]: *K-theory of derivators revisited*, Annals of K-Theory **2** 2 (2017) 303-340 &lbrack;[arXiv:1402.1871](https://arxiv.org/abs/1402.1871), [doi:10.2140/akt.2017.2.303](https://doi.org/10.2140/akt.2017.2.303)&rbrack;


### Higher Segal structure and symmetries

On the S-construction as a 2-Segal space, and its role for Hall algebras:

* {#DyckerhoffKapranov19} [[Tobias Dyckerhoff]], [[Mikhail Kapranov]]: *Higher Segal Spaces*, Lecture Notes in Mathematics **2244**, Springer (2019) &lbrack;[arXiv:1212.3563](https://arxiv.org/abs/1212.3563), [doi:10.1007/978-3-030-27124-4](https://doi.org/10.1007/978-3-030-27124-4)&rbrack;

On paracyclic structure on the S-construction and rotation invariance of K-theory:

* {#LurieRotation} [[Jacob Lurie]]: *Rotation invariance in algebraic K-theory* &lbrack;[pdf](https://www.math.ias.edu/~lurie/papers/Waldhaus.pdf)&rbrack;

A combinatorial construction of symmetries with the S-construction as a special case:

* {#Nadler15} [[David Nadler]]: *Cyclic symmetries of $A_n$-quiver representations*, Advances in Mathematics **269** (2015) 346-363 &lbrack;[arXiv:1306.0070](https://arxiv.org/abs/1306.0070), [doi:10.1016/j.aim.2014.10.006](https://doi.org/10.1016/j.aim.2014.10.006)&rbrack;
  > "This short note contains a combinatorial construction of symmetries arising in [[symplectic geometry]] (partially wrapped or infinitesimal [[Fukaya category|Fukaya categories]]), algebraic geometry (derived categories of singularities), and K-theory (Waldhausen's S-construction). Our specific motivation (in the spirit of expectations of Kontsevich, and to be taken up in general elsewhere) is a combinatorial construction of quantizations of Lagrangian skeleta (equivalent to microlocal sheaves in their many guises). We explain here the one dimensional case of ribbon graphs where the main result of this paper gives an immediate solution."

Interpretation in terms of a [[categorified Dold-Kan correspondence]]:

* {#Dyckerhoff17} [[Tobias Dyckerhoff]]: *A categorified Dold-Kan correspondence*, Selecta Mathematica New Series **27** 14 (2021) &lbrack;[arXiv:1710.08356](https://arxiv.org/abs/1710.08356), [doi:10.1007/s00029-021-00618-5](https://doi.org/10.1007/s00029-021-00618-5)&rbrack;


