
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
* table of contents
{:toc}

## Idea

Let $q$ be a positive-definite [[quadratic form]] over the ring of [[integers]] $\mathbf{Z}$.  The **mass** of $q$ is a weighted count of the number of quadratic forms in the [[genus]] of $q$, up to isomorphism (weighted by multiplicity).  The [[Smith-Minkowski-Siegel mass formula]] gives a (complicated but computable) formula for the mass of $q$.

Over [[number fields]], ideas of Tamagawa and Weil allow a reformulation of this formula as the statement that the [[Tamagawa number]] of a certain [[algebraic group]] associated to $q$ is equal to 1.  _Weil's conjecture_ is then the statement, now a theorem of [[Robert Langlands]], K. F. Lai and Robert Kottwitz, that the [[Tamagawa number]] of any semisimple simply-connected [[algebraic group]] is equal to 1.

There is [[function field analogy|analogue]] of the conjecture for [[function fields]], and it has been proved by [[Dennis Gaitsgory]] and [[Jacob Lurie]].

## The statement 

### Number field case
 {#NumberFieldCase}

Let $q$ be a positive-definite [[quadratic form]] over the ring of [[integers]] $\mathbf{Z}$.

+-- {: .num_defn}
###### Definition
The **mass** of $q$ is the sum
  \[ \sum_{q'} \frac{1}{|O_{q'}(\mathbf{Z})|} \]
taken over the positive-definite [[quadratic forms]] $q'$ in the genus of $g$.
=--

Let $\mathbf{A}$ be the ring of [[adeles]], a [[locally compact]] [[commutative ring]] containing $\mathbf{Q}$ as a [[discrete]] subring.

+-- {: .num_defn}
###### Definition
Let $O_q(\mathbf{A})$ denote the [[automorphism group]] of $q_\mathbf{A}$, the [[base change]] of $q$ to $\mathbf{A}$.  Let $SO_q(\mathbf{A}) \subset O_q(\mathbf{A})$ denote the subgroup of [[automorphisms]] with [[determinant]] 1.
=--

$SO_q(\mathbf{A})$ is a [[locally compact]] [[topological group]] containing $SO_q(\mathbf{Q})$ as a [[discrete]] subgroup and $SO_q(\hat{\mathbf{Z}} \times \mathbf{R})$ as a [[compact]] [[open]] subgroup.

+-- {: .num_theorem}
###### Theorem
**(Tamagawa-Weil reformulation of Siegel mass formula)**.
Let $\mu_{\mathrm{Tam}}$ denote the [[Tamagawa measure]].  Then
  \[ \mu_{\mathrm{Tam}}(SO_q(\mathbf{Q}) \backslash SO_q(\mathbf{A})) = 2. \]
Equivalently,
  \[ \mu_{\mathrm{Tam}}(Spin_q(\mathbf{Q})\backslash Spin_q(\mathbf{A})) = 1, \]
where $\Spin_q$ is the 2-fold universal cover of $SO_q$.
=--

+-- {: .num_theorem}
###### Theorem
**(Langlands-Lai-Kottwitz, "[[Weil conjecture]]")**.
Let $G$ be a semisimple simply-connected [[algebraic group]] over $\mathbf{Q}$.  Then
  \[ \mu_{\mathrm{Tam}}(G(\mathbf{Q})\backslash G(\mathbf{A})) = 1. \]
=--

### Function field case
 {#FunctionFieldCase}

Let $X$ be a [[smooth]] [[projective variety|projective]] [[curve]] over the [[finite field]] $F_q$, for some prime $q$.  Let $K_X$ denote the [[function field]] of $X$.  For $x \in X$, write $O_x$ for the [[completion]] of the [[local ring]] at $x$ and $K_x$ for its [[fraction field]].

+-- {: .num_defn}
###### Definition
The **[[ring of adeles]] of $K_X$** is defined as
  \[ \mathbf{A}_X = \prod^{res}_x K_x \subset \prod_x K_x, \]
i.e. the subgroup consisting of elements $\{g_x\}_{x \in X}$ such that $g \in G(O_x)$ for all but finitely many $x$.
=--

$\mathbf{A}_X$ is a [[locally compact]] [[commutative ring]] with [[discrete]] subring $K_X \subset \mathbf{A}_X$.

Let $G_0$ be a semisimple simply-connected linear [[algebraic group]] over $K_X$.  Then $G_0(K_X) \subset G_0(\mathbf{A})$ is a [[discrete]] subgroup of the [[locally compact]] group $G_0(\mathbf{A})$.  One defines a [[Tamagawa measure]] on $G(\mathbf{A})$ in a similar way as usual, i.e. by choosing a [[differential form]] and multiplying the forms on $G_0(K_x)$ ($x \in X$).  Then the [[function field]] version of [[Weil's conjecture]] is

+-- {: .num_theorem}
###### Theorem
**(Gaitsgory-Lurie, "Weil conjecture for function fields")**.
Let $X$ be a [[smooth]] [[projective variety|projective]] [[curve]] over the [[finite field]] $F_q$, for some prime $q$.  Then
  \[ \mu_{\mathrm{Tam}}(G_0(K_X)\backslash G_0(\mathbf{A}_X)) = 1. \]
=--

This was proved by [[Dennis Gaitsgory]] and [[Jacob Lurie]].  They reformulated the conjecture as a statement about the [[cohomology]] of the [[moduli stack of G-principal bundles]] $Bun_G(X)$ on $X$, in view of the [[function field analogy]]:

+-- {: .num_remark #RelationToModuliStack}
###### Remark

Under the [[function field analogy]], a [[global field]] $K_X$ such as a [[function field]] or a [[number field]] is interpreted as the field of [[global sections]] of the [[rational functions]] on an [[arithmetic curve]] $X$ over a [[finite field]] $\mathbb{F}_q$ or "over $\mathbb{F}_1$" (the would-be [[field with one element]]), respectively. Moreover, under this [[analogy]]

* the [[ring of adeles]] $\mathbb{A}_X$ is the ring of functions on all punctured [[formal disks]] in $X$ subject to the condition that all but at most finitely many of them extend to the un-punctured disk;

* accordingly $G(\mathbb{A}_X)$ is the group of $G$-valued such functions;

* the [[quotient]] $K_{X}\backslash \mathbb{A}_{X}$ is hence the quotient of such functions on punctured formal disks around finitely many points by the functions on $\Sigma$ with these finitely many points removed; and similarly $G(K_X)\backslash G(\mathbb{A}_X)$ is the quotient of group-valued such function;

* the ring $\mathcal{O}$ is the ring of functions on all formal disks in $\Sigma$;

* hence the further double [[quotient stack]] 

  $$
    Bun_G(X) = G(K_X)\backslash G(\mathbb{A}_X)//G(\mathcal{O})
  $$ 
  
  is the [[groupoid]] of [[Cech cohomology|Cech cocycles]] with Cech coboundaries between them for $G$-[[principal bundles]] relative to [[covers]] of $\Sigma$ with patches being the complement of finitely many points and the formal disks around these points.

For more on this see at _[moduli space of bundles -- over curves](http://ncatlab.org/nlab/show/moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence)_.

=-- 


First they proved a [[Grothendieck-Lefschetz trace formula]] for $Bun_G(X)$, generalizing work of [[Kai Behrend]]:

+-- {: .num_theorem}
###### Theorem

**(Gaitsgory-Lurie, "Grothendieck-Lefschetz trace formula for $Bun_G(X)$")**.
Let $X$ be a [[smooth]] [[projective variety|projective]] [[curve]] over the [[finite field]] $F_q$, for some prime $q$.  Then
  \[ \frac{|Bun_G(X)(\mathbf{F}_q)|}{q^{\dim(Bun_G(X))}} = \sum_{i \ge 0} (-1)^i \mathrm{Tr}(Frob^{-1} \mid H^i(\overline{Bun}_G(X) ; \mathbf{Q}_\ell)  \]
where $\overline{Bun}_G(X)$ denotes the [[base change]] of $Bun_G(X)$ to the [[algebraic closure]] of $\mathbf{F}_q$, where ${\vert -\vert}$ denotes [[groupoid cardinality]], and where $Frob : \overline{Bun}_G(X) \to \overline{Bun}_G(X)$ denotes the [[Frobenius map]].

=--

Then they proved the following result, via [[nonabelian Poincaré duality]] which provides a [[local-global principle]].

+-- {: .num_theorem}
###### Theorem
**(Gaitsgory-Lurie)**.
Let $X$ be a [[smooth]] [[projective variety|projective]] [[curve]] over the [[finite field]] $F_q$, for some prime $q$.  Then
  \[ \sum_{i \ge 0} (-1)^i \mathrm{Tr}(Frob^{-1} \mid H^i(\overline{Bun}_G(X) ; \mathbf{Q}_\ell) = \prod_{x \in X} \frac{q^{d \cdot \deg(x)}}{|G(\kappa(x))|} \]
=--

## References

* Wikipedia, _[Weil conjecture on Tamagawa numbers](https://en.wikipedia.org/wiki/Weil_conjecture_on_Tamagawa_numbers)_

A proof of the [[function field]] case was announced in 

* [[Jacob Lurie]], _Tamagawa Numbers via Nonabelian Poincar&#233; Duality_, talk at  [FRG Chern-Simons workshop](http://people.mpim-bonn.mpg.de/teichner/Older/FRG-3.html), Jan. 15-17, 2011

The proof is outlined in the lecture notes

* [[Jacob Lurie]], _Tamagawa Numbers via Nonabelian Poincare Duality (282y)_, lecture notes, 2014 ([web](http://www.math.harvard.edu/~lurie/282y.html))

See also the lecture notes

* [[Jacob Lurie]], _Tamagawa numbers via nonabelian Poincare duality_, 5 lectures at [Young Topologists Meeting 2014](http://www.math.ku.dk/english/research/conferences/2014/ytm2014), notes taken by [[Aaron Mazel-Gee]], [pdf](http://math.berkeley.edu/~aaron/livetex/lurie-tamagawa-poincare.pdf).

The idea of the relationship between [[Tamagawa numbers]] and [[moduli spaces]] of [[vector bundles]] goes back to [[Günter Harder]], who primarily considered the case $G = SL_n$.

* [[Günter Harder]], _Eine Bemerkung zu einer Arbeit von P. E. Newstead._, Journal f&#252;r die reine und angewandte Mathematik, 242 (1970): 16-25, [eudml](http://eudml.org/doc/151010).

* [[Günter Harder]], M. S. Narasimhan, _On the cohomology groups of moduli spaces of vector bundles on curves_, Mathematische Annalen, 212 (1975), Issue 3, pp 215-248.

The [[moduli stack]] of [[principal bundles]] was studied in more generality in

* [[Kai Behrend]], Ajneet Dhillon, _On the Motive of the Stack of Bundles_, 2005,  [arXiv](http://arxiv.org/abs/math/0512640).

* [[Kai Behrend]], Ajneet Dhillon, _Connected components of moduli stacks of torsors via Tamagawa numbers._, Canad. J. Math, 2009, [arXiv](http://arxiv.org/abs/math/0503383).

See also

* Aravind Asok, Brent Doran, Frances Kirwan. _Yang&#8211;Mills theory and Tamagawa numbers: the fascination of unexpected links in mathematics._ Bulletin of the London Mathematical Society (2008), [arXiv](http://arxiv.org/abs/0801.4733).

[[!redirects Weil conjecture on Tamagawa number]]