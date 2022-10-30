
...

* [[K-theory spectrum]]

* [[topological K-theory]]

* [[algebraic K-theory]]

* [[Karoubi K-theory]]

...
---
## K-theory

Historically, K-theory was the first "generalized cohomology theory" to be developed in algebraic topology. Since then, K-theory has also been developed in algebraic geometry (see [[Algebraic K-theory]]), and there are now many different variations on this theme. We refer to the individual pages for the various versions of K-theory.

category: General Introduction
---
## K-theory

##Memo notes from Karoubi: Bott Periodicity (K-theory handbook)

Omissions: Bivariant K-theory, motivic homotopy theory.

###Classical Bott Periodicity
Homotopy groups of infinite orthogonal and unitary group, related to those of $GL(\mathbb{R})$ and $GL(\mathbb{C})$. Periodicity in these cases. Various homotopy equivalences involving loop spaces, $GL$ and $BGL$. Proofs in Milnor: Morse theory, and also many other sources/versions.

###Interpretation of Bott P. via K-theory
Topological K-theory of Atiyah and Hirzebruch. It can be viewed as a homology theory on rings (of functions?). For a compact space $X$ with Banach algebra $C(X)$, have equivalence of categories between vector bundles over $X$ and f.g. projective $A$-modules. Some details on K-theory of Banach algebras.

###The role of Clifford algebras
Various approaches to periodicity; some key words: Proofs of Suslin, Harris (using $\Gamma$-spaces), nonconnected deloopings, negative Bott element.

###Negative K-theory and Laurent series
Suspension of a ring. Negative K-groups, long exact sequence.

The K-theory space/spectrum: realised as a loopspace, in real or complex case having the homotopy type of the space of Fredholm operators in a Hilbert space modelled on the field.

###Bott periodicity, the Atiyah-Singer index theorem, and KR-theory
Equivariant K-theory (Atiyah, Segal). Proof of Bott periodicity uses the full strength of Atiyah-Singer (i.e. KK-theory in modern terms). KR-theory applies to real Bott periodicity (using Fourier analysis).

###Bott per. in algebraic K-theory
Recall Quillen's K-theory of a discrete ring. (Write $K_n^{top}$ for the previously discussed K-groups of a Banach algebra; this is different from Quillen's def applied to a Banach algebra).

Bass and Karoubi defined $K_n(A)$ for negative $n$. Refs: Bass: Algebraic K-theory (1968), Karoubi: Foncteurs derives et K-thoerie, and La periodicite de Bott en K-theorie generale. (Need accents!!) The def is $K_{-r}(A) = K(S^r A)$ (suspension of a ring). By Bass for negative $n$ and Quillen for all $n$ (assuming $A$ regular Noetherian) we have an exact sequence

$$ 0 \to K_{n+1}(A) \to K_{n+1}(A[t]) \oplus K_{n+1}(A[t^{-1}]) \to K_{n+1}(A[t, t^{-1}]) \to K_n(A) \to 0
$$

We cannot have any "naive" Bott periodicity for the groups $K_n(A)$; for example, Quillen proved that for a finite field:

$$ K_{2n-1}(F_q) \cong \mathbb{Z}/(q^n-1)
$$

Browder and Karoubi introduced K-theory with finite coefficients (ref: Browder in LNM657, Soule: K-theorie des anneaux d'entiers de corps de nombres et cohomologie etale (1979)). Since K-theory is represented by a spectrum $K(A)$ defined through the spaces $BGL(S^n A)^{+}$ (ref: Wagoner: Delooping classifying spaces in algebraic K-theory), there is a well-known procedure in algebraic topology for constructing an associated mod $n$-spectrum, for any positive integer $n >1$. The homotopy groups of this spectrum are the K-theory groups with finite coefficients. An alternative (dual) approach is through a Puppe sequence and Moore spaces. This K-theory mod $n$ may, under some restrictions, be given a ring structure with nice properties (see Browder).

Thm (Suslin: On the K-theory of local fields (?)): Let $F$ be an algebraically closed field and let $n$ be an integer prime to $char(F)$. Then there is a canonical isomorphism of graded rings

$$ K_{2r}(F; \mathbb{Z}/n) \cong (\mu_n)^{\otimes r}
$$

and

$$ K_{2r+1}(F; \mathbb{Z}/n) = 0
$$

where $\mu_n$ denotes the group of roots of unity in $F$, and where $r \geq 0$.

The Lichtenbaum-Quillen Conjecture:

Q: Is there a way to compute $K_{*}(F; \mathbb{Z}/n)$ for an arbitrary field $F$? All questions of this form are a kind of "homotopy limit problem" (ref to Thomason). Define $K(A,n)$ to be the spectrum of the K-theory of $A$ mod $n$. Then $K(F,n)$ is the fixed point set of $K(\bar{F},n)$ (separable closure) wrt the Galois action. We have a map

$$ \phi: K(F,n) = K(\bar{F},n)^G \to K(\bar{F},n)^{hG}
$$

the last term being the homotopy fixed point set, i.e. the set of equivariant maps $EG \to K(\bar{F},n)$, where $EG$ is the "universal" principal $G$-bundle over $BG$. Let us write $K_r^{et}(F; \mathbb{Z}/n)$ for the r-th homotopy group of this space - these are etale K-theory groups. By the previous subsection, and the general theory of homotopy fixed point sets, there is a spectral sequence

$$  E_2^{p,q} = H^p(G; \mu_n^{\otimes (q/2)} ) \implies K_{q-p}^{et}(F; \mathbb{Z}/n)
$$

A version of Lichtenbaum-Quillen says: Assume $n$ is prime to $char(F)$. Then $\phi$ induces an isomorphism on homotopy groups $\pi_r$ for $r > d_n$, where $d_n$ is the n-cohomological dimension of $G$. In other words, the canonical map

$$ K_r(F; \mathbb{Z}/n) \to K_r^{et}(F; \mathbb{Z}/n)
$$

should be an isomorphism for such $r$. Surjectivity of this map was proved in many cases by Soule (K-theorie des anneaux d'entiers... (1979)), Dwyer-Friedlander-Snaith-Thomason (Algebraic K-theory eventually surjects... (1982)).

Thomason's approach:

For comparing systematically algebraic and etale K-theory (which is periodic) there is an approach by Thomason. Description of Bott element $\beta \in K_{2(p-1)}(F; \mathbb{Z}/p)$ mapping to $\beta_{et}$. The latter element is invertible in the etale K-theory ring, which is a say of saying that etale K-theory is periodic with period $2(p-1)$. Hence the canonical map above factors through K-theory with $\beta$ inverted.

Thm: Assume that $F$ is of finite $p$-etale dimension and satisfies some mild conditions. Then the map

$$ K_*(F; \mathbb{Z}/p)[\beta^{-1}] \to K_*^{et}(F; \mathbb{Z}/p)
$$

is an isomorphism.

The Bloch-Kato conjecture:

In order to make more progress on Lichtenbaum-Quillen, Bloch and Kato formulated a conjecture saying: For any integer $n$, the Galois symbol from Milnor K-theory mod $n$ to the corresponding Galois cohomology

$$  K_r^M(F) / n \to H^r(G; \mu_n^{\otimes r} )
$$

is an isomorphism. For $n=2^k$, this is the Milnor conjecture, proved by Voevodsky. This reult, together with a spectral sequence of [Bloch and Lichtenbaum](http://www.math.uiuc.edu/K-theory/0062), many authors were able to solve L-Q for $n  =2^k$ (Kahn, Rognes-Weibel, Ostvaer-Rosenschon). If Bloch-Kato is proved, then L-Q follows in general!

Another consequence of Bloch-Kato is a motivic spectral sequence

$$ E_2^{p,q} \implies K_{q-p}(F; \mathbb{Z}/n)
$$

where $E_2^{p,q} = H^p(G; \mu_n^{\otimes (q/2)} )$ for $p \leq q/2$ and zero otherwise. It should degenerate in many cases, for instance if $n$ is odd, or $F$ is an exceptional field (Kahn: K-theory of semi-local rings..., page 102).

Example: If $F$ is a number field and $n$ is odd, we have $d_n = 1$ above. Then this degenerating spectral sequence shows a direct link between algebraic K-theory and Galois cohomology.

A theorem of Kahn (ibid) gives quite general criteria for injectivity and surjectivity of the map

$$ K_r(F; \mathbb{Z}/p) \to K_r(F; \mathbb{Z}/p)[\beta^{-1}]
$$

for fields and also for finite-dimensional schemes.

Application: Details on the K-groups of $\mathbb{Z}$.

Another class of rings with periodic algebraic K-theory are complex stable $C^*$-algebras. By definition, these are IMic to their completed tensor product with the algebra of compact operators in a complex Hilbert space. Example: The $C^*$-algebra associated to a foliation, or the ring of continuous functions from a compact space to the above algebra of operators. These algebras are non-unital but satisfy excision (Suslin and Wodzicki). 

Thm: For a oomplex stable $C^*$-algebra, algebraic and topological K-theory agree. Hence Bott periodicity for algebraic K-theory in these cases, and in other related cases too.

####Bott periodicity in Hermitian K-theory
Usual K-theory is deeply linked with the general linear group. We could also consider other classical groups...

Def of higher Hermitian K-theory groups of a ring (for $n > 0$).

There are two interesting functors between algebraic and Hermitian K-theory, one in each direction. The homotopy fibers of these functors define "relative theories". These are involved in the statement of the "fundamental theorem of Hermitian K-theory".

Examples...

Implication: Periodicity for higher Witt groups... 

Relation to surgery groups...

###Conclusion
Morel and Voevodsky proved that algebraic K-theory is representable by an infinite Grassmannian in the unstable motivic homotopy category. Voevodsky showed that this, together with Quillen's computation of the K-theory of the projective line, implies that algebraic K-theory is representable in the stable motivic homotopy category by a motivic $(2,1)$-periodic $\Omega$-spectrum. Relation to the two motivic circles. Hornbostel showed the same for Hermitian K-theory, this time by a motivic $(8,4)$-periodic $\Omega$-spectrum. This periodicity is linked with the computation of the Hermitian K-theory of the smash-product of the projective line four times with itself.

category: [Private] Notes
---
## K-theory

[MathSciNet](http://www.ams.org/mathscinet/search/publications.html?pg4=AUCN&s4=&co4=AND&pg5=TI&s5=&co5=AND&pg6=PC&s6=&co6=AND&pg7=ALLF&s7=%22K-theory%22&co7=AND&Submit=Search&dr=all&yrop=eq&arg3=&yearRangeFirst=&yearRangeSecond=&pg8=ET&s8=All)

[Google Scholar](http://scholar.google.co.uk/scholar?q=%22K-theory%22&hl=en&lr=&btnG=Search)

[Google](http://www.google.com/search?hl=en&q=%22K-theory%22&btnG=Search)

[arXiv: Experimental full text search](http://search.arxiv.org:8081/?query=%22K-theory%22&in=)

[arXiv: Abstract search](http://front.math.ucdavis.edu/search?a=&t=&q=%22K-theory%22&c=&n=25&s=Abstracts)

category: Search results
---
## K-theory

KT (K-theory), AG (Algebraic geometry), AT (Algebraic topology), NCG (Algebra and noncommutative geometry)

category: World [private]
---
## K-theory

Kth

category: Labels [private]
---
## K-theory

&lt;http://mathoverflow.net/questions/78409/compatibility-of-pushforward-and-tensor-product-in-k-theory>

category: Properties
---
## K-theory

Preprint in progress of [Rognes](http://www.math.uio.no/~rognes/publications.html):
A note on monochromatic K-theory

Preprint in progress of [Rognes](http://www.math.uio.no/~rognes/publications.html):
Algebraic K-theory of the fraction field of topological K-theory

[arXiv:0912.3635](http://front.math.ucdavis.edu/0912.3635) Algebraic Geometry of Topological Spaces I
from arXiv Front: math.KT by Guillermo Corti&#241;as, Andreas Thom
We use techniques from both real and complex algebraic geometry to study
K-theoretic and related invariants of the algebra C(X) of continuous
complex-valued functions on a compact Hausdorff topological space X. For
example, we prove a parametrized version of a theorem of Joseph Gubeladze; we
show that if M is a countable, abelian, cancellative, torsion-free, seminormal
monoid, and X is contractible, then every finitely generated projective module
over C(X)[M] is free. The particular case when M=N^n gives a parametrized
version of the celebrated theorem proved independently by Daniel Quillen and
Andrei Suslin that finitely generated projective modules over a polynomial ring
over a field are free. The conjecture of Jonathan Rosenberg which predicts the
homotopy invariance of the negative algebraic K-theory of C(X) follows from the
particular case when M=Z^n. We also give algebraic conditions for a functor
from commutative algebras to abelian groups to be homotopy invariant on
C*-algebras, and for a homology theory of commutative algebras to vanish on
C*-algebras. These criteria have numerous applications. For example, the
vanishing criterion applied to nil-K-theory implies that commutative
C*-algebras are K-regular. As another application, we show that the familiar
formulas of Hochschild-Kostant-Rosenberg and Loday-Quillen for the algebraic
Hochschild and cyclic homology of the coordinate ring of a smooth algebraic
variety remain valid for the algebraic Hochschild and cyclic homology of C(X).
Applications to the conjectures of Beilinson-Soule and Farrell-Jones are also
given.

category: Some Research Articles
---
## K-theory

Toen: Note of Chern character, loop spaces and derived algebraic geometry. File Toen web publ Abel-2007.pdf. See [[Derived categorical sheaves]] for more about this article. Contains a remark at the end about algebraic K-theory determining complex topological K-theory, with a ref to Walker 2002 in K-theory.

[arXiv:1008.1346](http://front.math.ucdavis.edu/1008.1346) 18 Lectures on K-Theory
from arXiv Front: math.AT by Ioannis P. Zois
We present 18 Introductory Lectures on K-Theory covering its basic three
branches, namely topological, analytic (K-Homology) and Higher Algebraic
K-Theory, 6 lectures on each branch. The skeleton of these notes was provided
by the author's personal notes from a graduate summer school on K-Theory
organised by the London Mathematical Society (LMS) back in 1995 in Lancaster,
UK.

&lt;http://www.ncatlab.org/nlab/show/Serre-Swan+theorem>

category: Other Information
---
## K-theory

Atiyah: [K-theory Past and Present](http://arxiv.org/abs/math.KT/0012213)

[nLab](http://www.ncatlab.org/nlab/show/K-theory) on K-theory, and on the [K-theory spectrum](http://ncatlab.org/nlab/show/K-theory+spectrum)

Cortinas (K-th folder): Algebraic vs topological K-theory, lecture notes from Sedano. Covers in a rather elementary way topological K-theory of Banach algebras, Karoubi-Villamayor K-theory, Weibel's homotopy K-theory, and Quillen K-theory. Focus on rings, not schemes. Stuff on excision and of comparison between top and alg K-th of topological algebras.

category: Online References
---
## K-theory

Many papers by Atiyah, for example: Vector bundles and homogeneous spaces (1961)

Book by Karoubi: K-theory (1978)

LNM0028 Conner and Floyd. Discusses many different types of cobordism and their relations to K-theories.

Karoubi lecture notes on K-theory, in K-theory folder. Basic intro to top and alg K-th, among other things K-V K-th. Final chapters are on hermitian K-theory and cyclic homology.

category: Paper References

nLab page on [[nlab:K-theory]]
