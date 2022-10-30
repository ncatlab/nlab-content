* N. Saavedra Rivano, Cat&#233;gories Tannakiennes, Lecture Notes in Mathematics
265, Springer-Verlag, Berlin-New York, (1972).

* [[Pierre Deligne]], [[James Milne]], A. Ogus, K-y Shih, Hodge cycles, motives, and Shimura varieties, Lecture Notes in Mathematics, 900, Springer-Verlag, Berlin-New York, (1982).  [Annotated and corrected version (2012)](http://www.jmilne.org/math/xnotes/tc.pdf) (PDF).

* [[Pierre Deligne]], [[Catégories Tannakiennes]]. The Grothendieck Festschrift, Volume 2, 111--195. Birkhauser, 1990.

* [[Larry Breen]], Tannakian categories, 1994.  Motives, Proceedings of Symposia in Pure Mathematics, 55, Providence, R.I.: American Mathematical Society.

* [[Yves André]], Une introduction aux motifs (motifs purs, motifs mixtes, p&#233;riodes), 2004.  Panoramas et Synth&#232;ses, 17, Paris: Soci&#233;t&#233; Math&#233;matique de France.

* R. Sujatha, Motives from a categorical point of view, notes from Franco-Asian Conference on Motives, IHES, 2006.  [PDF](http://www.math.tifr.res.in/~sujatha/ihes.pdf)

[[!redirects Tannakian categories]]
[[!redirects Tannaka category]]
[[!redirects Tannaka categories]]
---
See Breen in the Motives volumes

Deligne: Categories tannakiennes (1990) in the Grothendieck Festschrift II.

Deligne and Milne: Tannakian categories (1982)


Saavedra Rivano: Categories tannakiennes. LNM 265, 1972.

Ref: [Levine](http://www.math.neu.edu/%7Elevine/publ/MixMotKHB.pdf), page 26.

&lt;http://mathoverflow.net/questions/71660/why-would-the-category-of-motives-be-tannakian>

---

Let $F$ be a field. A Tannakian category is a F-linear abelian tensor category which is rigid (i.e. has internal Homs) together with an exact faithful $F$-linear tensor functor to $E$-mod for some field extension $E$ of $F$. A Tannakian category is neutral if we can take $E = F$. Example of the latter: The category of finite-dimensional $F$-reps of an affine group scheme $G$ over $F$. If $A$ is neutral Tannakian with fiber functor $\omega$, then there is an affine group scheme $G$ over $F$ and a canonical isomorphism $G(F) \to Aut(\omega)$. 

---

Notes from Andr&#233;:

Let $F$ be a field, let $T$ be an abelian rigid tensor cat such that $End(\mathbf{1}) = F$. A fiber functor on $T$ is an exact and faithful tensor functor $\omega$ from $T$ to finite-dimensional $K$-vector spaces, where $K$ is some extension of $F$. If a fiber functor exists, $T$ is called Tannakian. (If we can take $K=F$, then $T$ is called neutral Tannakian). For a Tannakian cat, one can define an affine $K$-group scheme $G = \underline{Aut}^{\otimes} \omega$; for every extension $K'/K$, $G(K')$ is the group of automorphisms of the tensor functor $\omega_{K'} : T \to Vec_{K'}$.

Thm (Deligne): Let $T$ be a rigid tensor cat over a field $F$ of characteristic zero, which is abelian and such that $End(\mathbf{1}) = F$. Then $T$ is Tannakian iff the rank of every object is a natural number iff for every object $M$, sufficiently high exterior powers of $M$ vanish.

For a neutral Tannakian category, $\omega$ gives an equivalence of rigid tensor cats from $T$ to $Rep_F G$. Furthermore, the cat of fiber functors over $F$ is equivalent to the cat (groupoid) of G-torsors (i.e. principal homogeneous $G$-spaces).

We have a dictionary between properties of a group and properties of its Tannakian category:

- $G$ is an algebraic group (i.e. of finite type over $F$) iff $T$ admits a tensor generator., i.e. and object $M$ such that every object of $T$ is a subquotient of some direct sums of tensor products of $M$ and its dual. In this case, $G$ can be identified with a Zariski-closed algebraic subgroup of $GL(\omega(M))$.
- For $F$ of characteristic zero, $G$ is a pro-reductive group iff $T$ is semisimple.

Have a correspondence between tensor functors $\phi: T' \to T$ between neutral Tannakian cats, and homomorphisms $f: G \to G'$, induced by composition with the fiber functor. Under this correspondence:

- $f$ is a monomorphism (closed immersion) iff every object $M$ of $T$ is a subquotient of an object in the image of $\phi$
- $f$ is an epimorphism (faithfully flat) iff $\phi$ is fully faithful, and for every object $M'$ of $T'$, every subobject of $\phi(M')$ is the image under $\phi$ of a subobject of $M'$. (The last condition is automatic if $T$ is semisimple.
- $\phi$ identifies $T'$ with the cat of objects of $T$ equipped with a $G'$-action factorising the action of $G$.

Note that without a given fiber functor, the group $G$ is not determined by $T$ (example: inner forms). One can attach to every Tannakian cat $T$ over $F$ a commutative Hopf algebra in the cat of Ind-objects of $T$. Details of this.

Def of Tannakian subategory of a Tannakian cat.

nLab page on [[nlab:Tannakian category]]
