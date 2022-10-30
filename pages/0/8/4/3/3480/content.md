
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

[[Tannaka]] duality or _Tannaka [[reconstruction theorem]]s_ are statements of the form:

if $A$ is a symmetry object (e.g. a [[locally compact topological group]], [[Hopf algebra]]), [[representation|represented]] on objects in a [[category]] $D$, one may _reconstruct_ $A$ from knowledge of the [[endomorphism]]s of the forgetful functor -- the **fiber functor** --

$$
  F : Rep_D(A) \to D
$$

from the [[category]] $Rep_D(A)$ of [[representation]]s of $A$ on [[object]]s of $D$ that remembers these underlying objects. In a generalization, called mixed Tannakian formalism, not a single fiber functor, but a family of fiber functors over different bases is needed for a reconstruction.

There is a general-abstract and a concrete aspect to this. The general abstract one says that an algebra $A$ is reconstructible from the fiber functor on the category of _all_ its modules. The concrete one says that in nice cases it is reconstructible from the category of _dualizable_ (finite dimensional) modules, even if it is itself not finite dimensional.

More precisely, let $V$ be any [[enriched category theory|enriching category]] (a [[locally small category|locally small]] [[closed monoidal category|closed]] [[symmetric monoidal category]] with all [[limit]]s). Then 


1. for 

   * $A$ a [[monoid]] in $V$;

   * $A Mod$ the $V$-[[enriched category]] of _all_ $A$-[[module]]s in $V$;

   * $F : A Mod \to V$ the [[forgetful functor|forgetful]] _fiber functor_ ;

   $A$ can be reconstructed as 
   the object of [[enriched functor category|enriched endomorphisms]] of $F$, 
   given by the [[end]]

   $$
     A 
     \simeq
     End(F) := \int_{N \in A Mod} V(F(N), F(N))
     \,.
   $$

   This is just the [[enriched Yoneda lemma]] in a slight disguise.   

1. In good cases, this [[end]] is computed already by restriction to the 
   [[full subcategory]] $A Mod_{dual}$ of [[dual object|dualizable modules]]

   $$
     \cdots \simeq \int_{N \in A Mod_{dual}} V(F(N), F(N))
     \,.
   $$

## Statement

So far the following examples concern the abstract algebraic aspect of Tannaka duality only, which is narrated here as a consequence of the [[enriched Yoneda lemma]] in [[enriched category theory]]. Some of the Tannaka duality theorems involve
subtle harmonic analysis. 

### For permutation representations {#ForPermutationRepresentations}

A simple case of Tannaka duality is that of [[permutation representation]]s of a [[group]], i.e. representations on a [[set]]. In this case, Tannaka duality follows entirely from repeated application of the ordinary [[Yoneda lemma]].


+-- {: .un_theorem}
###### Theorem
**(Tannaka duality for permutation representations)**

Let $G$ be a [[group]], $Rep_{Set}(G)$ the category of its [[permutation representation]]s and $F : Rep_{Set}(G) \to Set$ the forgetful functor that sends a representation to its underlying set.

Then there is a canonical [[isomorphism]] of [[group]]s

$$
  Aut(F) \simeq G
  \,.
$$

Here $Aut(F)$ denotes the group of invertible [[natural transformation]]s from $F$ to itself.

=--

+-- {: .proof}
###### Quick Proof


With a bit of evident abuse of notation, the proof is a one-line sequence of applications of the [[Yoneda lemma]]: we show $End(F) \cong G$, i.e., each endomorphism on $F$ is invertible, so $End(F) = Aut(F) \cong G$.  

Write $C := Set^G = Rep_{Set}(G)$.
Observe that the functor $F : C \to Set$ is the [[representable functor|representable]] $F = C(G, -)$. Then the argument is 

$$
  End(F)
  =
  Set^C(F, F) 
    \cong 
  Set^C(C(G, -), C(G, -)) 
    \cong 
  C(G, G) 
   \cong 
  G.
$$

The "$G$" here is used in multiple senses, but each sense is deducible from context.

=--

+-- {: .proof}
###### Long-winded Proof

We repeat the same proof, but with more notational details on what the entities involved in each step are precisely.
 
Let $\mathbf{B}G$ be the [[delooping]] [[groupoid]] of the [[group]] $G$. Then 

$$
  Rep_{Set}(G) := Func(\mathbf{B}G^{op}, Set)
  \,.
$$

The canonical inclusion $i : {*} \to \mathbf{B}G$ induces the fiber functor

$$
  Func(i,Set) : Rep_{Set}(G) \to Set
$$

which evaluates a functor $\rho : \mathbf{B}G^{op} \to Set$ on the unique object of $\mathbf{B}G$. By the [[Yoneda lemma]] this is the same as homming out of the functor [[representable functor|represented by]] that unique object

$$
  Func(i,Set) = Hom_{PSh(\mathbf{B}G)}(Y_{\mathbf{B}G}) {*}, -)
  \,,
$$

where $Y_{\mathbf{B}G} : \mathbf{B}G \to PSh(\mathbf{B}G)$ is the [[Yoneda embedding]].

But this way we see that $Func(i,Set) : PSh(\mathbf{B}G) \to Set$  is itself a representable functor in the presheaf category $PSh(PSh(\mathbf{B}G)^{op})$

$$
  Func(i,Set) = Y_{\mathbf{PSh(\mathbf{B}G)^{op}}} Y_{\mathbf{B}G} *
  \,.
$$

So applying the [[Yoneda lemma]] twice, we find that

$$
  \begin{aligned}
    Aut_{PSh(PSh(\mathbf{B}G)^{op})} Func(i,Set)
    & =
    Aut_{PSh(PSh(\mathbf{B}G)^{op})} Y_{\mathbf{PSh(\mathbf{B}G)^{op}}} Y_{\mathbf{B}G} *
    \\
    & \simeq
    Aut_{PSh(\mathbf{B}G)^{op})} Y_{\mathbf{B}G} *
    \\
    & \simeq
    Aut_{\mathbf{B}G} *
    \\
    & \simeq G
    \,.
  \end{aligned}
$$

=--

Notice that the proof in no way used the fact that $G$ was assumed to be a [[group]], but only that $G$ is a [[monoid]].  So the statement holds just as well for arbitrary monoids.

But moreover, as the long-winded proof above makes manifest, even more abstractly the proof really only depended on the fact that the [[delooping]] $\mathbf{B}G$ is a [[small category]]. It need not have a single object for the proof to go through verbatim. Therefore we immediately obtain the following much more general statement of Tannaka duality for permutation representations of categories:

+-- {: .un_theorem}
###### Theorem
**(Tannaka duality for permutation representations of categories)**

Let $C$ be a [[locally small category]] and $Rep_{Set}(C) := Func(C,Set)$ the [[functor category]]. For every object $c \in C$ let $F_c : C \to Set$ be the fiber-functor that evaluates at $c$.

Then we have a [[natural isomorphism]]

$$
  Hom(F_c,F_{c'}) \simeq Hom_C(c,c')
  \,.
$$


=--

### For $V$-modules
  {#ForVModules}

Let $V$ be a ([[locally small category|locally small]]) [[closed monoidal category|closed]] [[symmetric monoidal category]], so that $V$ is enriched in itself via its [[internal hom]].

Observe that the setup, statement and proof of Tannaka duality for permutation representations given above is the special case for $V = $ [[Set]] of a statement verbatim the same in $V$-[[enriched category theory]], with the ordinary [[functor category]] replaced everywhere by the $V$-[[enriched functor category]]:

Then the statement says:


+-- {: .un_theorem}
###### Theorem
**(Tannaka duality for $V$-modules over $V$-algebras)**

For $A$ a [[monoid]] in $V$ with [[delooping]] $V$-[[enriched category]] $\mathbf{B}A$, and with 

$$
  A Mod := [\mathbf{B}A,V]
$$

the [[enriched functor category]] that encodes the $V$-[[module]]s of $A$, we have that the $V$-enriched [[endomorphism]] algebra $End(F) := [F,F]$ of the $V$-[[enriched functor]] $F : Rep(A) \to V$ is [[natural isomorphism|naturally isomorphic]] to $V$

$$
  End(A Mod \stackrel{F}{\to} V) \simeq A
  \,.
$$


=--

+-- {: .proof}
###### Proof

Apply the [[enriched Yoneda lemma]] verbatim as for the statement about permutation representations as above.

=--

Notice that the [[endomorphism]] object here is taken in the sense of enriched category theory, as described at [[enriched functor category]]. It is given by the [[end]] expression 

$$
  End(F) = \int_{N \in A Mod} V(F(N), F(N))
  \,.
$$

The case of permutation representations is re-obtained by setting $V = $ [[Set]].

As before, the same proof actually shows the following more general statement

+-- {: .un_theorem}
###### Theorem
**(Tannaka duality for $V$-modules over $V$-algebroids)**

Let $C$ be a $V$-[[enriched category]] (a "$V$-[[algebroid]]"). Write $C Mod := [C,V]$ for the $V$-[[enriched functor category]]. For every [[object]] $c \in C$ write $F_c : C Mod \to V $ for the fiber functor that evaluates at $C$. Then we have [[natural isomorphism]]s

$$
  hom(F_c, F_{c'}) \simeq C(c,c')
  \,.
$$

=--

From this statement of Tannaka duality in $V$-enriched category theory
now various special cases of interest follow, by simply choosing suitable enrichement categories $V$.

#### For algebra modules 
  {#ForAlgebraModules}

The general case of Tannaka duality for $V$-modules described [above](#ForVModules) restricts to the classical case of Tannaka duality for linear representations by setting $V :=$ [[Vect]], the category of [[vector space]]s over some fixed [[ground field]].

In this case the above says

+-- {: .un_corollary}
###### Corollary
**(Tannaka duality for linear modules)**

For $A$ an [[algebra]] and $A Mod$ its category of [[module]]s, 
and for $F : A Mod \to Vect$ the fiber functor that sends a module to 
its underlying vector space, we have a natural isomorphism

$$
  End( A Mod \to Vect ) \simeq A
$$

in [[Vect]].

=--

#### For linear group representations

Still for the special case $V = Vect$, let now $G$ be a [[group]] and let the algeba in question specifically be its [[group algebra]] $A = k[G]$ . Then the category of linear [[representation]]s of $G$ is 

$$
  Rep(G) \simeq k[G] Mod
$$ 

and we obtain 

+-- {: .un_corollary}
###### Corollary
**(Tannaka duality for linear group representations)**

There is a natural isomorphism

$$
  End(Rep(G) \to Vect) \simeq k[G]
  \,.
$$

=--


#### For coalgebra comodules {#Coalgebras}

If for $V$ we choose not [[Vect]] but its [[opposite category]] $Vect^{op}$, then a [[monoid]] object $A$ in $V$ is a [[coalgebra]] and $A Mod$ (or $A Mod^{op}$, rather) is the category of comodules over this coalgebra. Again we have a forgetful functor $F : A Mod \to Vect$

In 

* [[André Joyal]], [[Ross Street]], _An introduction to Tannaka duality and quantum groups_, [pdf](http://www.math.mq.edu.au/~street/CT90Como.pdf)

([proposition 5, page 40](http://www.maths.mq.edu.au/~street/CT90Como.pdf#page=40))

and

* Pierre Deligne, [[Catégories Tannakiennes]]

it is shown that $A$ is recovered as the [[coend]]

$$
  \int^{N \in A Mod_{fin}} F(N) \otimes F(N)^*
$$

in [[Vect]], where the coend ranges over finite dimensional modules. 

If $A$ itself is finite dimensional then this is yet again just a special case of the enriched Yoneda lemma for $V$-modules, for the case $V = FinVect^{op}$: this general statement says that $A$ is recovered as the [[end]]

$$
  A = \int_{N \in A Mod_{fin}} V(F(N), F(N))
$$

in $Vect^{op}$. This is equivalently the [[coend]]

$$
  \cdots \simeq \int^{N \in A Mod}( Vect(F(N), F(N)))
$$

in $Vect$. Finally using that $FinVect(V,W) \simeq V\otimes W^*$ the above coend expression follows.

As before, more work is required to show that ven for $A$ itself not finite dimensional, it is still recovered in terms of the above (co)end over just its finite dimensional modules.

### For Lie groupoids

See [[Tannaka duality for Lie groupoids]].

###  For geometric stacks

See [[Tannaka duality for geometric stacks]].

### In higher category theory
 {#InHigherCategoryTheory}

In as far as the proof of Tannaka duality only depends on the [[Yoneda lemma]], the statement immediately generalizes to [[higher category theory]] whenever a higher generalization of the Yoneda lemma is available.

This is notably the case for [[(∞,1)-category]] theory, where we have the [[(∞,1)-Yoneda lemma]].

#### For permutation $\infty$-representations
 {#ForInfinityPermutations}

By applying the $(\infty,1)$-Yoneda lemma verbatim four times in a row as above [for permutation representations](#ForPermutationRepresentations), we obtain the following statement for [[∞-permutation representations]].

+-- {: .un_theorem}
###### Theorem
**(Tannaka duality for $\infty$-permutation representations)**

Let $G$ be an [[∞-group]] and $Rep_{\infty Grpd}(G) := Func(\mathbf{B}G, \infty Grpd)$ the [[category of representations|category of]] [[∞-permutation representations]], the [[(∞,1)-category of (∞,1)-functors]] from its [[delooping]] [[∞-groupoid]] to [[∞Grpd]]. Let $F :  Rep_{\infty Grpd}(G) \to \infty Grpd$ be the fiber functor that remembers the underlying $\infty$-groupoid. Then there is an [[equivalence in a quasi-category]]

$$
  End(Rep_{\infty Grpd}(G) \to \infty Grp) \simeq G
  \,.
$$

=--

As before, this holds immediately even for representations of [[(∞,1)-categories]]


+-- {: .un_theorem}
###### Theorem
**(Tannaka duality for $\infty$-permutation representations)**

Let $c$ be an [[(∞,1)-category]] and $Rep_{\infty Grpd}(C) := Func(C,\infty Grpd)$. For $c \in C$ an [[object]], write $F_c : Rep_{\infty Grpd}(C) \to \infty Grpd$ for the corresponding fiber functor.

Then there is a natural equivalence
 
$$
  hom(F_c, F_{c'}) \simeq C(c,c')
$$

in [[∞Grpd]].

=--

#### $\infty$-Galois theory
 {#InfinityGaloisTheory}

As a special case of this, we obtain a statement about $\infty$-Galois theory. For details and background see [[homotopy groups in an (∞,1)-topos]]. In that context one finds for a [[locally contractible space]] $X$ that the [[∞-groupoid]] $LConst(X)$ of [[locally constant ∞-stack]]s on $X$  is equivalent to $Rep_{\infty Grpd}(\Pi(X))$, where $\Pi(X)$ is the [[fundamental ∞-groupoid]] of $X$. 
For $x \in X$ a point, write $F_x : LConst(X) \to \infty Grpd$ for the corresponding fiber functor.

Then we have

+-- {: .un_theorem}
###### Theorem

For $x \in X$ there is a natural [[weak homotopy equivalence]]

$$
  End(LConst(X) \stackrel{F_x}{\to} \infty Grpd) \simeq 
  \mathbf{B} Aut_{\Pi(X)}(x)
  \,.
$$

In particular do we have [[natural isomorphisms]] of [[homotopy group]]s

$$
  \pi_n End(LConst(X) \stackrel{F_x}{\to} \infty Grpd)
  \simeq
  \pi_n(X,x)
  \,.
$$

=--

More on this is at [[cohesive (∞,1)-topos -- structures]] in the section <a href="http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#Homotopy">Galois theory in a cohesive (∞,1)-topos</a>

## References

* [[André Joyal]], [[Ross Street]], _An introduction to Tannaka duality and quantum groups_, [pdf](http://www.math.mq.edu.au/~street/CT90Como.pdf)

* B.J. Day, _Enriched Tannaka reconstruction_, J. Pure Appl. Algebra __108__ (1996) 17-22, <a href="http://dx.doi.org/10.1016/0022-4049(95)00039-9">doi</a>

* Pierre Deligne, [[Catégories Tannakiennes]]

The following paper shortens the Deligne's proof 

* [[Alexander Rosenberg|Alexander L. Rosenberg]],  _The existence of fiber functors_,  The Gelfand Mathematical Seminars, 1996--1999,  145--154, Birkh&#228;user, Boston 2000.

Deligne's proof in turn fills the gap in the seminal work with the same title 

* N. Saavedra Rivano, _Cat&#233;gories Tannakiennes_, Springer LNM __265__ (1972).

A revival in algebraic geometry related to the theory of mixed motives was marked by

* [[P. Deligne]], [[J. Milne]], _Tannakian categories_, Springer Lecture Notes in Math. __900__, 1982, pp. 101-228.

Ulbrich made a major contribution at the coalgebra and Hopf algebra level

* K-H. Ulbrich, _On Hopf algebras and rigid monoidal categories_, in special volume, Hopf algebras, Israel J. Math. __72__ (1990), no. 1-2, 252--256, [doi](http://dx.doi.org/10.1007/BF02764622)

This Hopf-direction has been advanced by many authors including 

* [[S. L. Woronowicz]], _Tannaka-Krein duality for compact matrix pseudogroups. Twisted $SU(N)$ groups_, Inventiones Mathematicae __93__, No. 1, 35-76, [doi](http://dx.doi.org/10.1007/BF01393687)

* [[Shahn Majid]], _Foundations of quantum group theory_, chapter 9

* Phung Ho Hai, _Tannaka-Krein duality for Hopf algebroids_, Israel J. Math. __167__ (1):193&#8211;225 (2008) [math.QA/0206113](http://arxiv.org/abs/math/0206113)

* [[Volodymyr Lyubashenko|Volodymyr V. Lyubashenko]], _Squared Hopf algebras and reconstruction theorems_, Proc. Workshop "Quantum Groups and Quantum Spaces" (Warszawa), Banach Center Publ. __40__, Inst. Math. Polish Acad. Sci. (1997) 111&#8211;137, [q-alg/9605035](http://arxiv.org/abs/q-alg/9605035); _Squared Hopf algebras_, Mem. Amer. Math. Soc. __142__ (677):x 180, 1999; &#1040;&#1083;&#1075;&#1077;&#1073;&#1088;&#1099; &#1061;&#1086;&#1087;&#1092;&#1072; &#1080; &#1074;&#1077;&#1082;&#1090;&#1086;&#1088;-&#1089;&#1080;&#1084;&#1084;&#1077;&#1090;&#1088;&#1080;&#1080;, &#1059;&#1052;&#1053;, 41:5(251) (1986), 185&#8211;186, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=2247&what=fullt&option_lang=rus), transl. as: _Hopf algebras and vector symmetries_, Russian Math. Surveys 41(5):153154, 1986.

* A. Brugui&#232;res, _Th&#233;orie tannakienne non commutative_, Comm. Algebra __22__, 5817&#8211;5860, 1994

* K. Szlachanyi, _Fiber functors, monoidal sites and Tannaka duality for bialgebroids_, [arxiv/0907.1578](http://arxiv.org/abs/0907.1578)

* B. Day, R. Street, _Quantum categories, star autonomy, and quantum groupoids_, in
"Galois theory, Hopf algebras, and semiabelian categories", Fields Inst. Comm. __43__
(2004) 187-225 

* [[Daniel Schäppi]], _Tannaka duality for comonoids in cosmoi_, [arXiv:0911.0977](http://arxiv.org/abs/0911.0977)

A generalization of several classical reconstruction theorems with nontrivial [[functional analysis]] is in 

* [[Alexander Rosenberg|Alexander L. Rosenberg]],  _[[Reconstruction of Groups|Reconstruction of groups]]_, Selecta Math. (N.S.) __9__, 1 (2003), 101--118, [doi](http://dx.doi.org/10.1007/s00029-003-0322-x).

Categorically oriented notes were written also by Pareigis, emphasising on using [[coend|Coend]] in dual picture. His works can be found [here](http://www.mathematik.uni-muenchen.de/~pareigis/pa_schft.html) but the most important is the chapter 3 of his online book

* Bodo Pareigis, _Quantum groups and noncommutative geometry_, Chapter 3: Representation theory, reconstruction and Tannaka duality, [pdf](http://www.mathematik.uni-muenchen.de/~pareigis/Vorlesungen/98SS/Quantum_Groups/LN3.PDF)

A very neat Tannaka theorem for stacks is proved in

* [[Jacob Lurie]], _Tannaka duality for geometric stacks_, ([arXiv:math.AG/0412266](http://arxiv.org/abs/math/0412266))

* [[Jacob Lurie]], _[[Quasi-Coherent Sheaves and Tannaka Duality Theorems]]_

* [[Bertrand Toen]], [Higher Tannaka duality](http://www.msri.org/publications/ln/msri/2002/hodgetheory/toen/2/index.html), MSRI 2002 (talk, video)

* Moshe Kamensky, _Model theory and the Tannakian formalism_, [arXiv:0908.0604](http://arxiv.org/abs/0908.0604). 

* H. Fukuyama, I. Iwanari, _Monoidal infinity category of complexes from Tannakian viewpoint_, [arxiv/1004.3087](http://arxiv.org/abs/1004.3087)

* remark of [Ben-Zvi on Tannaka reconstruction for monoidal categories](http://mathoverflow.net/questions/3446/tannakian-formalism/3467#3467)

* [[David Kazhdan]], Michael Larsen, Yakov Varshavsky, _The Tannakian formalism and the Langlands conjectures_, [arxiv/1006.3864](http://arxiv.org/abs/1006.3864)

The classical articles are 

* [[Tadao Tannaka]], _&#220;ber den Dualit&#228;tssatz der nichtkommutativen topologischen Gruppen_, Tohoku Math. J. 45 (1938), n. 1, 1&#8211;12 (project euclid has only Tohoku new series!), see [[Tannaka-Krein theorem]].
* N. Tatsuuma, _A duality theorem for locally compact groups_, J. Math., Kyoto Univ.
6 (1967), 187&#8211;293.
* M.G. Krein, _A principle of duality for bicompact groups and quadratic block algebras_, Doklady AN SSSR __69__ (1949), 725&#8211;728. 
* Eiichi Abe, _Dualit&#233; de Tannaka des groupes alg&#233;briques_, Tohoku Mathematical Journal. Volume 12, Number 2  (1960), 327-332. 

The Tannaka-type reconstruction in quantum field theory see [[Doplicher-Roberts reconstruction theorem]].

Tannaka duality in the context of [[(∞,1)-category theory]] is discussed in

* [[James Wallbridge]], _Higher Tannaka duality_ , PhD thesis, Adelaide/Toulouse (2011) ([Adelaide University repository](http://digital.library.adelaide.edu.au/dspace/bitstream/2440/69436/1/02whole.pdf), [arXiv:1204.5787](http://arxiv.org/abs/1204.5787))


[[!redirects Tannaka reconstruction]]