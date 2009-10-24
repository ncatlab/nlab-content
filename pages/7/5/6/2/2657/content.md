
> **under construction**

#Related entries#

* [[Hodge star]]

* [[Hodge Laplace operator]]

* [[Betti number]]

* [[nonabelian Hodge theory]]

#References#

* Bertin, Demailly, Illusie, Peters, _Introduction to Hodge theory_ AMS (1996)

* Claire Voisin, _Hodge theory and the topology of complex K&#228;hler and complex projective manifolds_ ([pdf](http://www.math.columbia.edu/~thaddeus/seattle/voisin.pdf))

---
Steenbrink: A Summary of Mixed Hodge theory (in the Motives volumes)

Peters and Steenbrink: Mixed Hodge structures. Book, seems to cover everything you would want to know about MHSs.

Introduction &#224; la th&#233;orie de Hodge: Jos&#233; Bertin - Jean-Pierre Demailly - Luc Illusie - Chris Peters

Deligne: Structures de Hodge mixtes reelles (in Motives vol)

Voisin books

[Griffiths and Cornalba](http://www.ams.org/mathscinet-getitem?mr=0419438)

&lt;http://mathoverflow.net/questions/4083/is-hodge-theory-somehow-connected-with-a-galois-group-action-galc-r>

Brylinski and Zucker: An overview of recent advances in Hodge theory (1990???)

LNM 1335: about "Hodge-Deligne theory"?

LNM 1594: Algebraic cycles and Hodge theory. Contains the following lectures: 

- Green: Infinitesimal methods in Hodge theory
- Murre: Algebraic cycles and algebraic aspects of cohomology and K-theory
- Voisin: Transcendental methods in the study of algebraic cycles
- Pirola
- Van Geemen: An introduction to the Hodge conjecture for abelian varieties
- Muller-Stach: A remark on height pairings

[Du Bois](http://www.ams.org/mathscinet-getitem?mr=613848) on something related to the Hodge filtration for singular varieties.

See everything by Steenbrink.

Toen, Katzarkov, Pantev: Schematic homotopy types and nonabelian Hodge theory. File Toen web publ nht.pdf. Constructs a "Hodge decomposition" (a certain action) on the schematic homotopy type of a smooth projective complex variety. This recovers many other Hodge invariants, short review of these. 

Hodge theory computations: Cox and Batyrev in Duke 75: On the Hodge structure of projective hypersurfaces in toric varieties. Generalizes results of Griffiths and Steenbrink on Hodge str of hypersurfaces.

---

###Brief memo notes from Deligne: Hodge II
Classical Hodge theory: The n-th singular cohomology group with coefficients in $\mathbb{C}$ of a compact Kahler variety carries a Hodge structure of weight $n$. We show here that the cohomology of a non-singular algebraic variety (not necessarily compact) carries a more general structure: here $H^n(X, \mathbb{C})$ is a "successive extension" of Hodge structures of decreasing weights (in the interval $2n$ to $n$), for which the Hodge numbers $h^{pq}$ vanish for $p>n$ or $q>n$.

The proof uses Hironaka's resolution of singularities, which allows us to "express, via a spectral sequence, the cohomology of a quasi-projective nonsingular variety in terms of the cohomology of projective nonsingular varieties".

Section 1: Filtrations. Categories of filtered objects in an abelian category. Associated graded. Induced filtrations on Hom and tensor products, and maps on Gr. Interaction between several filtrations. Bigraded object "looking like a pure Hodge structure" induces a pair of finite n-opposite filtrations, and this construction is an equivalence of cats. Notion of three filtrations being opposite, meaning that two of them induce $(-n)$-opposite filtrations on $Gr^n$ of the third. Basic theorem (1.2.10) on the (abelian!) category of objects with three opposite filtrations, in an abelian category. 

Convention: Filtrations are decreasing unless otherwise mentioned.

Def of spectral sequence associated to a biregular filtered differential complex in an abelian category. Condition for degenaracy at $r=1$. Def of filtered qis of such things. Bifiltered diff complexes; filtrations induced by one filtration on the spectral seq of the other filtration. Various propositions on this, leading to the "lemme de deux filtrations" (Thm 1.3.16).

Hypercohomology of filtered complexes (not using language of derived cats). All complexes assumed bounded below. Setup: Left exakt functor $T: A \to B$ of abelian cats. For a complex $K$ of objects in $A$, def of the hypercohomology objects $R^i T K$ in $B$. If $K$ is filtered, these objects can be computed via a spectral sequence (the hypercohomology spectral sequence of the filtered complex $K$). For example, can take the canonical or stupid filtration on any complex. Example: Leray spectral sequence for the sheaf cohomology groups $H(X,F)$ and a map $f: X \to Y$ of topological spaces.

Section 2: Hodge structures
2.1. Def: A real Hodge structure is a finite-dimensional real vector space $V$ equipped with an action of the real algebraic group $S$. Here $S$ is the group obtained from the multiplicative group $G_m$ by restriction of scalars from $\mathbb{C}$ to $\mathbb{R}$. (So the real points of $S$ is $\mathbb{C}^*$). Such an action is equivalent to giving a bigrading of $V_{\mathbb{C}}$ on which complex conjugation interchanges the grading indices.

Let $V$ be as above. Def of weight grading on $V_{\mathbb{C}}$, a grading defined over the reals. Def of Hodge filtration on $V_{\mathbb{C}}$ by $F^p V_{\mathbb{C}} = \oplus_{i \geq p} V^{i j}$. The category of real Hodge structures is equivalent to the category of finite-dimensional real vector spaces $V$ with a filtration on $V_{\mathbb{C}}$ which is $n$-opposite to its complex conjugate.

Def: A Hodge structure of weight $n$ consists of an abelian group $H_{\mathbb{Z}}$ of finite type together with a real Hodge structure of weight $n$ on $H_{\mathbb{R}} = H_{\mathbb{Z}} \otimes_{\mathbb{Z}} \mathbb{R}$. Def of morphism. The Hodge structures of weight $n$ form an abelian category. Taking tensor products of two Hodge structures $H, H'$ of weights $n$ and $n'$ gives a Hodge structure of weight $n+n'$. Also, have a Hodge structure $Hom(H, H')$ of weight $n'-n$ (internal Hom), exterior powers, and duals. Details on all this. Def of weight $n$ $A$-Hodge structure, for any noetherian subring $A$ of the reals (replace $\mathbb{Z}$ by $A$ above). Def of $A$-Hodge structure, requiring that the weight grading on $H_{\mathbb{R}}$ should be defined over $Frac{A}$.

Def: The Tate Hodge structure $\mathbb{Z}(1)$ of weight $(-2)$, of rank $1$, purely of bidegree $(-1,-1)$, with integral structure $2 \pi i \mathbb{Z} \subset \mathbb{C}$. Description of $\mathbb{Z}(n)$. Remark on choice of $i$.

Def: A polarisation of a Hodge structure $H$ of weight $n$ is a homomorphism $(x,y): H \otimes H \to \mathbb{Z}(-n)$ such that the real bilinear form $(2 \pi i)^n (x, Cy)$ on $H_{\mathbb{R}}$ is symmetric and positive definite. Here $C$ is the element of $S(\mathbb{R}$ determined by a choice of $i$.

Def of $\mathbb{R}(n)$ and of polarisation of real Hodge structures.

2.2. Hodge theory.
Let $X$ be a compact Kahler variety. Poincar&#233; lemma, implying de Rham description of the complex cohomology. Hence the hypercohomology spectral sequence $E_1^{pq} = H^q(X, \Omega^p) \implies H^{p+q}(X, \mathbb{C})$. By Hodge theory, this degenerates ($E_1 = E_{\infty}$) and the Hodge filtration on $H^n(X, \mathbb{C})$ is $n$-opposite to its complex conjugate. Generalisation of this to coefficients in a local system. Can also generalise the Poincar&#233; lemma and the hypercohomology spectral sequence (and the Hodge structure???) to the case where $X$ is complete nonsingular algebraic variety, not necessarily Kahler (use Chow's lemma and RoS, reducing to projective case).

Several constructions of what I think is the first Chern class of an invertible sheaf. Using this, a "trace map", and PD, we construct a map $L^{n-i}$ and a polarisation of the primitive part $Ker(L^{n-i+1}) \subset H^i(X, \mathbb{Z})$. This implies that the rational Hodge structures $H^i(X, \mathbb{Q})$ are polarisable.

2.3 Mixed structures.
Def: A mixed Hodge structure consists of: A abelian group $H_{\mathbb{Z}}$ of finite type, an increasing "weight filtration" $W$ of $H_{\mathbb{Q}}$, and a (decreasing) "Hodge filtration" $F$ of $H_{\mathbb{C}}$. One requires that the triple $(W_{\mathbb{C}}, F, \bar{F})$ is a system of opposite filtrations.

We see that each $Gr_n^{W}(H_{\mathbb{Z}})$ becomes a Hodge structure of weight $n$.

Note: Every Hodge structure of weight $n$ defines a mixed Hodge structure in a trivial way.

Thm (from thm 1.2.10): The category $MHS$ is abelian. Description of kernels and cokernels. Every morphism is strictly compatible with $F$ and $W$, so induces morphisms on the graded pieces. The functor $Gr_n^{W}$ is an exact functor from $MHS$ to weight $n$ $\mathbb{Q}$-Hodge structures. The functor $Gr_F^p$ is exact.

Def: Let $H$ be a MHS. Define $H^{pq} = Gr_F^p Gr_{\bar{F}}^q Gr_{p+q}^W (H_{\mathbb{C}})$, and Hodge numbers. The Hodge number $h^{pq}$ of $H$ is the Hodge number of the Hodge structure $Gr_{p+q}^W (H)$

Def: $\mathbb{Q}$-MHS.

Section 3: Hodge theory of nonsingular algebraic varieties. 

3.1. We recall some features of log poles of holomorphic differential forms. Def of the logarithmic de Rham complex of smooth complex analytic variety $X$ along a normal crossings divisor $Y$. The Poincar&#233; residue. Description of the cohomology of $X-Y$ as the hypercohomology of $X$ with coeffs in the log de Rham complex (I think). 

3.2. Mixed Hodge theory.
Convention: All schemes are of finite type over $\mathbb{C}$, and all sheaves are analytic.

Let $X$ be smooth and separated. By Nagata, $X$ is Zariski open in a complete scheme $\bar{X}$. By Hironaka, one can take $\bar{X}$ to be smooth and $\bar{X}-X$ to be a normal crossings divisor.

There are two filtrations on the log de Rham complex: Hodge and weight. Each gives rise to a spectral sequence converging to the complex cohomology of $X$. Get a MHS on $H^n(X, \mathbb{Z})$. Various lemmas on degenerating and on interaction between the filtrations. erification of functoriality and independence of choices. The above MHS is the classical weight $n$ Hodge structure if $X$ is smooth and complete. The Hodge numbers $h^{pq}$ of the above MHS can be nonzero only if $p \leq n$, $q \leq n$, and $p+q \geq n$.

Let $\omega$ bea  meromorphic p-form on $\bar{X}$ which is holomorphic on $X$ and with at worst log poles along $Y$. The the restriction of $\omega$ to $X$ is closed, and if the cohomology class of $\omega$ in $H^{p}(X, \mathbb{C})$ is zero, then $\omega$ is zero. 

Descriptions of the image of the cohomology of $\bar{X}$ in the cohomology of $X$.

Section 4: "Applications et complements".

4.1. Thm: Let $S$ be a smooth separated scheme, and $f: X \to S$ a smooth proper morphism. (i) In rational cohomology, the Leray spectral sequence $E_2^{pq} = H^p(S, R^q f_* Q) \implies H^{p+q}(X, Q)$ degenerates ($E_2 = E_{\infty}$). (ii) Let $\bar{X}$ be a nonsingular compactification. Then the canonical morphism $H^n(\bar{X}, Q) \to H^0(S, R^n f_* Q)$ is surjective.

In $D^+(S)$, we have $Rf_*\mathbb{Q} = \sum_p R^p f_* \mathbb{Q}[-p]$.

Several remarks, for example: If a global section of $R^n f_* \mathbb{C}$ is of Hodge type $(p,q)$ at a point, then it is so everywhere.

4.2. The theorem of semisimplicity.

Def: Continuous family of Hodge structures on a top space $S$. Various related notions. Lemma: conditions for a subcat of the category of familys of $\mathbb{Q}$-Hodge structures to be semisimple and closed under various operations.

Def: Algebraic family. Algebraic familys satisfy the above conditions. Some further properties of algebraic families.

Thm on semisimplicity of the representation on the fundamental group of $S$ given by the fiber of $H_{\mathbb{Q}}$, assuming $H$ is a family belong to a subcat satisfying the conditions in the above lemma. Corollaries of this.

4.4. Homomorphisms of abelian schemes. 

Recall the description of the category of abelian $S$-schemes as the category of polarisable continuous families of Hodge structures satisfying certain conditions.

Theorem on homomorphisms of abelian schemes.

END.

###Memo notes from Hodge III

Introduction: In Hodge II, we treated Hodge theory of nonsingular (not necessarily complete) varieties. Here we will treat the singular case.

In the case of a complete singular variety $X$, the key idea is to use resolution of singularities to "replace" $X$ by a simplicial smooth projective scheme, having, in a certain sense, the same cohomology. Hence we can express the cohomology of $X$ through a spectral sequence, in terms of the cohomology of the individual components of the simplicial scheme. Using classical Hodge theory for the components, we get a mixed Hodge structure on the cohomology of $X$.

For an arbitrary variety $X$, we replace $X$ by a smooth simplicial scheme, compactified by a smooth projective simplicial scheme. The complement will be a normal crossings divisor and a union of smooth divisors. Get a mixed Hodge structure again.

Review of cohomological descent. Various results about vanishing of Hodge numbers. A form of Alexander duality.

We endow the cohomology of any simplicial scheme with a mixed Hodge structure. This can be applied to relative cohomology, and to cohomology of classifying spaces of algebraic groups.

The theory developed is an absolute theory (not treating $Rf_*$) and only considers constant coefficients.

Convention: Schemes are of finite type over the complex numbers, and sheaves are in the complex topology.

Section 5: Cohomological descent

5.1 Simplicial topological spaces

Extremely clean summary of basic simplicial language. Def of sheaf on a simplicial topological space. The category of such sheaves form a topos, i.e. the category is equivalent to a category of sheaves on some site.

Many nontrivial definitions and details on simplicial topological spaces. Def of global sections functor (nonobvious).

5.2 Cohomology of simplicial topological spaces

Def of geometric realization of a simplicial topological space. Segal defined the cohomology of a simplicial topological space as the cohomology of the realization. Such a definition also works for K-groups. Here we adopt another definition, more suitable for sheaf techniques, namely: cohomology is given by the derived functors of the global sections functor. Here the coefficients are an abelian sheaf on the simplicial topological space. Reformulation in terms of resolutions. We have a spectral sequence $E_1^{pq} = H^q(X_p, F^p) \implies H^{p+q}(X_{\bullet}, F^{\bullet} )$. 

Formulation in terms of derived categories, generalising the above spectral sequence.

5.3 Cohomological descent

Let $a: X_{\bullet} \to S$ be an augmented simplicial topological space. For every sheaf $F$ on $S$, we have an adjunction morphism $\phi: F \to a_* a^* F$. Deriving this gives a morphism $\phi: Id \to Ra_* a^*$ of endofunctors of $D^+(S)$.

Def: We say that $a$ has cohomological descent if for every abelian sheaf $F$ on $S$, we have

$$  F \cong Ker(a_{0*} a_0^*F \to a_{1*} a_1^* F)
$$

and 

$$  R^i a_* a^* F = 0
$$

for all $i > 0$.

I think this definition is equivalent to saying that $\phi: Id \to Ra_* a^*$ is an isomorphism.

If $a$ has cohomological descent, and $K$ is an object of $D^+(S)$, the canonical map 

$$   R \Gamma (S,K) \to R \Gamma (X_{\bullet} , a^* K )
$$

is an isomorphism. In particular, we have a spectral sequence

$$  E_1^{pq} = H^q(X_p, a_p^* K) \implies H^{p+q}( S, K )
$$

(this is hypercohomology).

Def: A continuous map $a: X \to S$ has cohomological descent if the augmentation morphism of $cosq(X \to S)$:

$$  ((X/S)^{\Delta_n})_{n \geq 0} \to S
$$

has cohomological descent. We say that $a$ has universal cohomological descent (UCD) if, for every $u: S' \to S$, the continuous map $a': X \times_S S' \to S'$ has cohomological descent.

Fundamental results, from SGA4: 

- The continuous maps which have UCD form a Grothendieck topology on the category of topological spaces.
- A surjective proper morphism has UCD
- A map $a: X \to S$ admitting sections locally on $S$ has UCD
- Def of k-truncated hypercovering
- Def of what it means for a map $a: x \to y$ of $S$-augmented simplicial topological spaces to be a hypercovering for the UCD topology.
- For such a hypercovering $a$, and any $K \in D^+(S)$, the map $a^*: R y_* y^* K \to R x_* x^* K$ is an isomorphism.

Example: The above recovers the Leray spectral sequence for a covering.

Def: Proper hypercovering.

Section 6: Examples of simplicial topological spaces

6.1. Classifying spaces

Details omitted for now.

6.2. Constructing hypercoverings

Details omitted for now. Come back to this later.

Def: Smooth simplicial scheme, proper simplicial scheme, divisor with normal crossings on a simplicial scheme.

Lemma: For any normal crossings divisor on a simplicial scheme, the logarithmic de Rham complexes, equipped with the weight filtration, form a filtered complex on the simplicial scheme.

We show that for every separated scheme $S$ over $\mathbb{C}$, there exists (i) a smooth proper simplicial $\mathbb{C}$-scheme, which can be taken to be s-split, (ii) a normal crossings divisor $D_{\bullet}$ in $X_{\bullet}$; let $U_{\bullet} = X_{\bullet} - D_{\bullet}$, (iii) an augmentation $a: U_{\bullet} \to S$ such that $U_{\bullet}^{an}$ is a proper hypercovering of $S_{\bullet}^{an}$.

6.3. Relative cohomology

Def: Let $u: Y_{\bullet} \to X_{\bullet}$ be a morphism of simplicial objects in a category $\mathcal{C}$ admitting finite sums and a final object $e$. Define the mapping cone of $u$ by

$$ C(u)_n = X_n \coprod \big( \coprod_{i &lt; n} Y_i \big) \coprod e
$$

For $\mathcal{C}$, we take the category of topological spaces, or the category of pairs consisting of a topological space and an abelian sheaf on the space. A morphism $(X,F) \to (Y,G)$ in the latter category is a continuous map $u: Y \to X$ together with a $u$-morphism $G \to F$.

Let $u: Y_{\bullet} \to X_{\bullet}$ be a morphism of simplicial topological spaces, let $F$ be an abelian sheaf on $X_{\bullet}$ and $G$ the same on $Y_{\bullet}$. Let $f: G \to F$ be a $u$-morphism. Then the cone $C(f)$ of $f$ is an abelian sheaf on $C(u)$, and we define groups

$$  H^n(C(u), C(f) ) = H^n( X_{\bullet} \ mod \ Y_{\bullet}, F \ mod \ G )
$$

called relative cohomology groups. There is a long exact sequence:

$$ \ldots \to H^i( X_{\bullet} \ mod \ Y_{\bullet}, F \ mod \ G ) \to H^i(X_{\bullet}, F) \to H^i(Y_{\bullet}, G) \to \ldots
$$

More generally, can do this for hypercohomology and complexes of sheaves (bounded below). The long exact sequence corresponds to a distinguished triangle in the derived category.

Remark: The above construction is not the only possible one.

6.4. Multisimplicial spaces

Let $r$ be a non-negative integer. An $r$-simplicial object in a category $C$ is a functor $(\Delta)^r \to C$. Precomposing with the functor $\Delta \to (\Delta)^r$ gives the associated (diagonal) simplicial object.

Def of sheaf cohomology for an $r$-simplicial topological space.

Details on bisimplicical sets augmented towards simplicial sets; cohomological descent for this setup.

Section 7. Filtered derived category

Details omitted for now.

Section 8: Hodge theory of algebraic spaces

8.1 Hodge complexes

Many details omitted.

Prop 8.1.20: Functorial MHS on integral cohomology. Degeneration of a spectral sequence in rational cohomology. Nonvanishing of Hodge numbers only in $[0,n] \times [0,n]$, and (I think) for the smooth case, also need $p+q \leq n$. 

8.2 Separated algebraic spaces

Thm 8.2.4: Let $X$ be a separated algebraic space of finite type over $\mathbb{C}$. Then teh following must hold for the pairs $(p,q)$ with nonvanishing Hodge numbers (for $H^n(X)$):

- $(p,q) \in [0,n] \times [0,n]$
- If $dim(X) = N$ and $n \geq N$, then $(p,q) \in [n-N,N] \times [n-N,N]$
- If $X$ is proper, then $p+q \leq n$
- If $X$ is smooth, then $p+q \geq n$

Several other interesting propositions on the behaviour of the Hodge structures on cohomology.

Kunneth isomorphisms and cup products are morphisms of mixed Hodge structures.

8.3 Hodge theory of simplicial schemes

(Or simplicial algebraic space.)

Details omitted for now. One point is that "everything" happening with cohomology groups (spectral sequence for the cohomology of a simplicial scheme, long exact sequence of relative cohomology, ...) actually respects the mixed Hodge structures.

Section 9: Examples and applications

9.1 Cohomology of linear algebraic groups.

9.2 Smooth hypersurfaces.

9.3 Constructing complexes of first order differential operators.

Corollary (Bloom and Herrera): For a quasi-projective scheme over $mathbb{C}$, the map $H^{\bullet}(X^{an}, \mathbb{C}) \to H^{\bullet}(X^{an}, \Omega_X^{\bullet an})$ identifies the first group as a direct factor of the second.

Section 10: Hodge theory "en niveau $\leq 1$"

10.1 1-motives

We construct an equivalence between the category of 1-motives over $\mathbb{C}$ with a certain category of mixed Hodge structures.

Def: Smooth 1-motive.

Def: Hodge, $\ell$-adic and de Rham realizations of a 1-motive.

10.2 1-motives and biextensions

10.3 Algebraic interpretation of mixed $H^1$: the case of curves

10.4 Translation of a theorem of Picard

END
---
In addition to the applications to special values conjectures, we also probably get a new description of the Hodge realization functor, as hinted by CD. Actually Cisinski said that this is not immediate, one needs to do more work ("rewrite Hodge theory in the correct way"). But we can still mention this.


Cisinski said: One should get the Deligne spectrum as the image of 1 under under a right adjoint to the Hodge realization functor, which should exist because DM should be initial in a category of [settings with six functors?]. Maybe one could add here stability, Nis descent etc OSLT. Note that the philosophy of realizations seem to indicate that there should be a strict Deligne spectrum (could it be just E-infty?) and that the Steenrod obstruction somehow is irrelevant since the Betti spectrum is strict when taken with rational coefficients at least.

Question: Is there any chance that the Hodge decomposition can be understood on the level of representing objects, for example the Betti spectrum? Can the map from motivic cohomology then be related to this, and if so, can one use descent or any other technique to prove new cases of algebraic cycle conjectures? See naive notes (filed somewhere)

nLab page on [[nlab:Hodge theory]]
