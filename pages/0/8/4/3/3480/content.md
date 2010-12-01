
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

[[Tannaka]] duality or _Tannaka [[reconstruction theorem]]s_ are statements of the form:

for $A$ some [[algebra|algebraic structure]], [[representation|represented]] on objects in a [[category]] $D$, one may _reconstruct_ $A$ from knowledge of the [[endomorphism]]s of the forgetful functor -- the **fiber functor** --

$$
  F : Rep_D(A) \to D
$$

from the [[category]] $Rep_D(A)$ of [[representation]]s of $A$ on [[object]]s of $D$ that remembers these underlying objects.

There is a general-abstract and concrete aspect to this, and a concrete one. The general abstract one says that an algebra $A$ is reconstructible from the fiber functor on the category of _all_ its modules. The concrete one says that in nice cases it is reconstructible from the category of _dualizble_ (finite dimensional) modules, even if it is itself not finite dimensional.

More precisely, let $V$ be any [[enriched category theory|enriching category]] (a [[locally small category|locally small]] [[closed monoidal category|closed]] [[symmetric monoidal category]] with all [[limit]]s). Then 


1. we have in full generality that:

   for 

   * $A$ a [[monoid]] in $V$;

   * $A Mod$ the $V$-[[enriched category]] of _all_ $A$-[[module]]s in $V$;

   * $F : A Mod \to V$ the [[forgetful functor|forgetful]] _fiber functor_ ;

   we have that $A$ is reobtained as 
   the [[enriched functor category|enriched endomorphisms]] of $F$, 
   given by the [[end]]

   $$
     A 
     \simeq
     End(F) := \int_{N \in A Mod} V(F(N), F(N))
     \,.
   $$

   This is just the [[enriched Yoneda lemma]] in slight disguise.   

1. In good cases this [[end]] is computed already by restriction to the 
   [[full subcategory]] $A Mod_{dual}$ of [[dual object|dualizable modules]]

   $$
     \cdots \simeq \int_{N \in A Mod_{dual}} V(F(N), F(N))
     \,.
   $$

## Statement

So far the following examples concern the abstract aspect of Tannaka duality only, which is narrated here as a consequence of the [[enriched Yoneda lemma]] in [[enriched category theory]]. 

### For permutation representations 

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

Here $Aut(F)$ denotes the group of invertbile [[natural transformation]]s from $F$ to itself.

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

The general case of Tannaka duality for $V$-modules described above restricts to the classical case of Tannaka duality for linear representations by setting $V :=$ [[Vect]], the category of [[vector space]]s over some fixed [[ground field]].

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


### In higher category theory

In as far as the proof of Tannaka duality only depends on the [[Yoneda lemma]], the statement immediately generalizes to [[higher category theory]] whenever a higher generalization of the Yoneda lemma is available.

This is notably the case for [[(∞,1)-category]] theory, where we have the [[(∞,1)-Yoneda lemma]].

By applying this verbatim four times in a row as above, we obtain the following statement for "$\infty$-permutation representations".

+-- {: .un_theorem}
###### Theorem
**(Tannaka duality for $\infty$-permutation representations)**

Let $G$ be an [[∞-group]] and $Rep_{\infty Grpd}(G) := Func(\mathbf{B}G, \infty Grpd)$ the [[(∞,1)-category of (∞,1)-functors]] from its [[delooping]] [[∞-groupoid]] to [[∞Grpd]]. Let $F :  Rep_{\infty Grpd}(G) \to \infty Grpd$ be the fiber functor that remembers the underlying $\infty$-groupoid. Then we have an [[equivalence in a quasi-category]]

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

Then we have a natural equivalence
 
$$
  hom(F_c, F_{c'}) \simeq C(c,c')
$$

in [[∞Grpd]].

=--

#### $\infty$-Galois theory

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

In particular do we have naturall isomorphisms of [[homotopy group]]s

$$
  \pi_n End(LConst(X) \stackrel{F_x}{\to} \infty Grpd)
  \simeq
  \pi_n(X,x)
  \,.
$$

=--

## References

* [[André Joyal]], [[Ross Street]], _An introduction to Tannaka duality and quantum groups_, [pdf](http://www.math.mq.edu.au/~street/CT90Como.pdf)

* Pierre Deligne, [[Catégories Tannakiennes]]

The following paper shortens the Deligne's proof 

* [[Alexander Rosenberg|Alexander L. Rosenberg]],  _The existence of fiber functors_,  The Gelfand Mathematical Seminars, 1996--1999,  145--154, Birkh&#228;user, Boston 2000.

Ulbrich made a major contribution at the coalgebra and Hopf algebra level

* K-H. Ulbrich, _On Hopf algebras and rigid monoidal categories_, in special volume, Hopf algebras, Israel J. Math. 72 (1990), no. 1-2, 252--256. 

This Hopf-direction has been advanced by many authors including [[Shahn Majid]] and

* Phung Ho Hai, _Tannaka-Krein duality for Hopf algebroids_, Israel J. Math. __167__ (1):193&#8211;225 (2008) [math.QA/0206113](http://arxiv.org/abs/math/0206113)

* [[Volodymyr Lyubashenko|Volodymyr V. Lyubashenko]], _Squared Hopf algebras and reconstruction theorems_, Proc. Workshop "Quantum Groups and Quantum Spaces" (Warszawa), Banach Center Publ. __40__, Inst. Math. Polish Acad. Sci. (1997) 111&#8211;137, arXiv:q-alg/9605035; _Squared Hopf algebras_, Mem. Amer. Math. Soc. __142__ (677):x 180, 1999. 

* K. Szlachanyi, _Fiber functors, monoidal sites and Tannaka duality for bialgebroids_, [arxiv/0907.1578](http://arxiv.org/abs/0907.1578)

More on Tannaka duality for Hopf algebras is in 

* [[Daniel Schäppi]], _Tannak duality for comonoids in cosmoi_ ([arXiv:0911.0977](http://arxiv.org/abs/0911.0977))

A generalization of several classical reconstruction theorems with nontrivial [[functional analysis]] is in 

* [[Alexander Rosenberg|Alexander L. Rosenberg]],  _Reconstruction of groups_, Selecta Math. (N.S.) __9__, 1 (2003), 101--118, [doi](http://dx.doi.org/10.1007/s00029-003-0322-x).

Categorically oriented notes were written also by Pareigis, emphasising on using [[coend|Coend]] in dual picture. His works can be found [here](http://www.mathematik.uni-muenchen.de/~pareigis/pa_schft.html) but the most important is the chapter 3 of his online book

* Bodo Pareigis, _Quantum groups and noncommutative geometry_, Chapter 3: Representation theory, reconstruction and Tannaka duality, [pdf](http://www.mathematik.uni-muenchen.de/~pareigis/Vorlesungen/98SS/Quantum_Groups/LN3.PDF)

A very neat Tannaka theorem for stacks is proved in

* [[Jacob Lurie]], _Tannaka duality for geometric stacks_, [math.AG/0412266](http://arxiv.org/abs/math/0412266)

* [[Bertrand Toen]], [Higher Tannaka duality](http://www.msri.org/publications/ln/msri/2002/hodgetheory/toen/2/index.html), MSRI 2002 (talk, video)

* Moshe Kamensky, _Model theory and the Tannakian formalism_, [arXiv:0908.0604](http://arxiv.org/abs/0908.0604). 

* H. Fukuyama, I. Iwanari, _Monoidal infinity category of complexes from Tannakian viewpoint_, [arxiv/1004.3087](http://arxiv.org/abs/1004.3087)

* remark of [Ben-Zvi on Tannaka reconstruction for monoidal categories](http://mathoverflow.net/questions/3446/tannakian-formalism/3467#3467)

* [[David Kazhdan]], Michael Larsen, Yakov Varshavsky, _The Tannakian formalism and the Langlands conjectures_, [arxiv/1006.3864](http://arxiv.org/abs/1006.3864)

[[!redirects Tannaka reconstruction]]