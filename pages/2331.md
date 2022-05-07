
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea {#Idea}

Deformation theory studies problems of extending structures to  extensions of their domains. __Formal deformation theory__, is the part of the deformation theory where the extensions are _[[infinitesimal object|infinitesimal]]_.

A typical problem in formal deformation theory has the structure that 

* a [[morphism]] $f : X \to Y$ of certain [[space]]s is given, 

* and [[infinitesimal object|infinitesimal]] thickenings $\tilde X$ and $\tilde Y$ of $X$ and $Y$ are prescribed, with injection morphisms $X \to \tilde X$ and $Y \to \tilde Y$

and asks whether a bottom horizontal morphism $\tilde f$ in the diagram

$$
  \array{
    X &\stackrel{f}{\to}& Y
    \\
    \downarrow && \downarrow
    \\
    \tilde X &\stackrel{\tilde f}{\to}& \tilde Y
  }
$$

may be found. This morphism $\tilde f$ would be called an _infinitesimal deformation_ of $f$.

In other words:

+-- {: .standout}

Formal deformation theory studies the **[[obstruction|obstruction theory]]** of extensions to **infinitesimal** thickenings.

=--

A typical example of an _infinitesimal thickening_ is a _square-0-extension_ of a [[ring]]:

let $R$ be a [[ring]], to be thought of as the ring of functions on the [[space]] $X$ in the above diagram. Let furthermore $N$ be an $R$-module, to be thought of as the $R$-module of [[section]]s of a [[vector bundle]] over $X$.

Then consider the new ring, whose underlying group is the [[direct sum]] $R \oplus N$, equipped with the product structure

$$
  (r_1, n_1) \cdot (r_2, n_2) = (r_1 r_2, r_1 n_2 + n_1 r_2)
  \,.
$$

This is the **square 0-extension** of $R$ by $N$. It should be thought of as the algebra of functions that consists of elements of $R$ and  $N$, where the elements in $N$ are thought of as functions with values in [[infinitesimal object|infinitesimal quantities]], so that their would-be product "$n_1 \cdot n_2$" vanishes.

So the ring $R \oplus N$ may be thought of as the ring of functions on the infinitesimal extension $\tilde X$ of $X$, which is the space obtained by adding to $X$ all the _vectors of infinitesimal length_ in the vector bundle over $X$.

There is a canonical ring homomorphism $R\oplus N \to R$ that is the identity on $R$ and $0$ on $N$. This is to be thought of as the pullback of functions on spaces along the inclusion of spaces $X \to \tilde X$ (which in turn may be thought of as the 0-[[section]] of the vector bundle on $X$).

Similarly, let $R_2$ be another ring with module $N_2$ and square-0 extension $R_2 \oplus N_2$, thought of, respectively, as the ring of functions on a space $Y$, the module of sections of a vector bundle on $Y$ and the ring of functions on the space of infinitesimal vectors of this vector bundle.

In terms of these function rings, a morphism $f : X \to Y$ of spaces corresponds to a ring homomorphism $R_1 \leftarrow R_2 : f^*$. Hence we have a situation

$$
  \array{
    R_1 &\stackrel{f^*}{\leftarrow}& R_2
    \\
    \uparrow && \uparrow
    \\
    R_1 \oplus N_1 && R_2 \oplus N_2
  }
  \,.
$$

The obvious obstruction problem now is whether we can **deform** $f^*$ to a morphism $R_1 \oplus N_1 \leftarrow R_2 \oplus N_2 : \tilde f^*$ of rings, such that we get a commuting diagram

$$
  \array{
    R_1 &\stackrel{f^*}{\leftarrow}& R_2
    \\
    \uparrow && \uparrow
    \\
    R_1 \oplus N_1 &\stackrel{\tilde f^*}{\leftarrow}& R_2 \oplus N_2
  }
  \,.
$$

The obstruction to the existence of such lifts is measured by [[cohomology]] with coefficients in the [[cotangent complex]] of $R_1$. 

This is the archetypical problem that deformation theory deals with. As always, after studying this a bit it turns out that in order to obtain a good theory, one needs to adopt the [[nPOV]]. Problems as above may be stated in the [[category]] [[Ring]] of rings, but they may have good answers only in [[vertical categorification|categorifications]] of this for instance to the [[(∞,1)-category]] of [[E-∞-ring]]s.

### Modules, derivations and K&#228;hler differentials {#Modules}

In order to better see the structure of the above archetypical problem of deformation theory, we describe some aspects of the canonical [[bifibration]] of ring modules in a way that nicely organizes all the concepts [[module]], [[derivation]], [[Kähler differential]] in a single picture that lends itself to [[vertical categorification]]. (Following [[Deformation Theory|DefTheory]].)

With [[Ring]] denoting the [[category]] of (commutative, unital) [[rings]], write 

$$
  p : Mod \to Ring
$$ 

for the [[bifibration]] of [[modules]] over [[rings]]: objects of $Mod$ are pairs consisting of a ring $R$ an an $R$-[[module]] $N$, and morphism $(R_1,N_1) \to (R_2, N_2)$ are pairs consisting of a ring homomorphism $f : R_1 \to R_2$ and a morphism $F : N_1 \to N_2 \otimes_f R_2$ of $R_2$-modules.

(Recall for instance from the discussion at [[Sweedler coring]]) 
that this bifibration is a way to think of the [[stack]] of algebraic [[vector bundles]].)

But there is also another functor $G : Mod \to Ring$ of interest: for $N$ any $R$-module, we may form the ring $G(N) := R \oplus N$ called the **square 0-extension** of $R$, in which multiplication is given by

$$
  (r_1,n_1) \cdot (r_2, n_2) := (r_1 r_2, n_1 r_2 + n_2 r_1)
  \,.
$$

Moreover, there is a [[natural transformation|natural]] morphism of rings $G(N) \to R$ given by sending $(r,n) \mapsto r$. A [[section]] $v : R \to G(n)$ of this morphism is precisely a [[derivation]] of $R$ with values in the module $N$.

This may be organized into a single functor

$$
   Mod \to [I,Ring]
$$

into the [[arrow category]] of [[Ring]], that sends to the $R$-module $N$ to the morphism $G(N) \to R$. The original bifibration factors through this morphism by the right endpoint evaluation

$$
  \array{
    Mod &&\stackrel{p}{\to}&& Ring
    \\
    & \searrow && \nearrow_{\mathrlap{d_1}}
    \\
    && [I,Ring]
  }
  \,.
$$

Finally notice that the [[functor]] $G$ has a [[left adjoint|left]] [[adjoint functor]]

$$
  \Omega : Ring \to Mod
$$

that sends a ring $R$ to the $R$-module $\Omega_K(R)$ of [[Kähler differentials]], i.e. to the module that encodes the [[cotangent bundle]].



### Cotangent complex

Using the module of K&#228;hler differentials is not appropriate in general; instead we need to take its derived version. To talk about the nonabelian derived functors, Quillen introduced a model category structure on the category of simplicial commutative rings. Given a morphism $f: A\to B$ of rings, which makes $B$ an $A$-algebra, the category $AbGr(A-Alg/B)$ of abelian group objects in the slice category $A$-$Alg/B$ of $A$-algebras over $B$ is equivalent both to the category of $B$-modules and the trivial (= square zero) extensions of $A$ by $B$-modules. In particular we can consider the forgetful functor $AbGr(A-Alg/B)\to A-Alg/B$ which has a left adjoint $Ab_{B/A} : A-Alg/B\to AbGr(A-Alg/B)\cong {}_B Mod$. All said is true for simplicial commutative rings as well. Now the **relative cotangent complex** $L_{B/A}$ is the value on $B$ of the left [[derived functor]] $\mathbb{L} Ab_{B/A}(B)$. Regarding that the left adjoint at the nonderived level (and for usual rings) can be expressed via K&#228;hler differentials, this explains the phrase "derived version of the module K&#228;hler differentials". 

The above situation generalizes from the category [[Ring]] to an arbitrary presentable [[(∞,1)-category]] $C$ by replacing the [[bifibration]] $Mod \to Ring$ by the [[stabilization]] $T_C \to C$ of the [[codomain fibration]] of $C$: the [[tangent (∞,1)-category]] of $C$.

The projection $p : T_C \to C$ still has a [[left adjoint]]

$$
  \Omega : C \to T_C
$$

for which a representative which is also a section (in a strict sense) of $p$ may be taken; any such representative is called the [[cotangent complex]] functor for $C$. The special property section property, like in the motivating example above, says that the composition 

$$
  C \stackrel{\Omega}{\to} T_C \stackrel{p}{\to} C
$$

is the identity [[(∞,1)-functor]].

### Further categorification

...


## Deformation theory via differential graded Lie algebras

Over a field of characteristic zero, there is an approach to deformation theory via [[differential graded Lie algebras]] (or more generally [[L-infinity algebras]]). One can find some exposition about this approach in the Kontsevich and Lurie references below. See also discussion at MathOverflow: [def theory and dgla-s](http://mathoverflow.net/questions/385/deformation-theory-and-differential-graded-lie-algebras).

In this approach, one begins with an object $X$ (for example a scheme, or a complex manifold, or a vector bundle, or an associative algebra, or a dg category, or ...) that one would like to deform. Then the general principle is that there exists a dgLa $L_X$ with the property that the functor $Def_{L_X} : Art \to Set$, which sends a local Artin algebra $(A,m)$ to the set of [[Maurer-Cartan equation|Maurer-Cartan solutions]] in $(L_X \otimes m)^1$ modulo the gauge action of $(L_X \otimes m)^0$, is isomorphic to the functor which sends a local Artin algebra $(A,m)$ to the set of isomorphism classes of deformations of $X$ over $\operatorname{Spec} A$. Note the similarity with Schlessinger's theory: both here and in Schlessinger's work, we deal with functors from Artin algebras to sets.

In the case of a compact complex manifold, the dgLa in question is given by the so-called [[Kodaira-Spence theory|Kodaira-Spencer]] dgLa: holomorphic vector fields tensor $(0,q)$-forms (this is just the [[Dolbeault cohomology|Dolbeault resolution]] of the sheaf of holomorphic vector fields). In the case of an associative algebra (or a dg algebra, or an A-infinity algebra, or a dg category, or an A-infinity category), the appropriate dgLa is the Hochschild complex with the Hochschild differential and the Gerstenhaber bracket.

In this language, the [[Tian-Todorov theorem]] on the unobstructedness of deformations of [[Calabi-Yau manifold]]s translates to the statement that the [[Kodaira-Spencer theory|Kodaira-Spencer]] dgLa of a Calabi-Yau manifold is homotopy abelian --- that is, it is quasi-isomorphic to an abelian dg Lie algebra. Barannikov-Kontsevich proved more generally that the dgLa given by holomorphic polyvector fields tensor $(0,q)$-forms on a Calabi-Yau manifold is homotopy abelian. The deformation-theoretic consequence is that the "extended deformations" of Calabi-Yau manifolds are unobstructed. These "extended deformations" should be realized by certain $A_\infty$ deformations of (a dg enhancement of) the derived category of coherent sheaves on the Calabi-Yau.

The following paper is a good introduction to these ideas:

* Marco Manetti, _Deformation theory via differential graded Lie algebras_ , &#176;([arXiv:0507284](http://arxiv.org/abs/math/0507284))

The Kontsevich and Soibelman references below are also good.


## Related entries 

* [[Kuranishi deformation theory]]

* [[Kodaira-Spencer theory]]

* [[Artin-Mazur formal group]]

* [[deformation context]], [[formal moduli problem]], [[Lie differentiation]]

* [[tangent complex]], [[André-Quillen cohomology]], [[Hochschild cohomology]]

* [[cotangent complex]], [[André-Quillen homology]], [[Hochschild homology]]

* [[derived deformation theory]], [[derived algebraic geometry]]

* [[formal scheme]], [[formal smoothness]]

* [[deformation quantization]]

* [[Lubin-Tate theory]]

## References

* {#SchlessingerStasheff85} [[Michael Schlessinger]], [[Jim Stasheff]], _The Lie algebra structure of tangent cohomology and deformation theory_, Journal of pure and applied algebra 38 (1985) 313-322

* {#SchlessingerStasheff12} [[Michael Schlessinger]], [[Jim Stasheff]], _Deformation theory and rational homotopy type_ ([arXiv:1211.1647](https://arxiv.org/abs/1211.1647))

* [[Charles Doran]], S. Wong, *Deformation Theory: An Historical Annotated Bibliography*, Chapter 2 in Deformation of Galois Representations, to appear in the AMS-IP Studies in Advanced Mathematics Series.

On [[deformation theory]] in terms of [[L-infinity algebra|$L_\infty$-algebras]] and their [[Maurer-Cartan equations]]:

* [[Martin Doubek]], [[Martin Markl]], [[Petr Zima]], equation (31) in: *Deformation Theory (lecture notes)*, Archivum mathematicum 43(5), 2007, 333-371 ([arXiv:0705.3719](https://arxiv.org/abs/0705.3719))

* [[Martin Markl]], _Deformation theory of algebras and their diagrams_, 129 pp, CBMS __116__, AMS 2012 ([ISBN:978-0-8218-8979-4](http://www.ams.org/bookstore-getitem/item=CBMS-116), [toc pdf](https://www.gbv.de/dms/goettingen/721467989.pdf))

* Wikipedia: [deformation theory](http://en.wikipedia.org/wiki/Deformation_theory), [cotangent complex] (http://en.wikipedia.org/wiki/Cotangent_complex)
* E. Sernesi, _An overview of classical deformation theory_, [pdf](http://www.mat.uniroma3.it/users/sernesi/sernesioverviewdefth.pdf)

* [[Alexander Grothendieck]], _Cat&#233;gories cofibr&#233;es additives et complexe cotangent relatif_, Lecture Notes in Mathematics 79

* [[Luc Illusie]], _Complexe cotangent et d&#233;formations I_, Lec. Notes Math. __239__, Springer 1971, xv+355 pp.; _II_, LNM __283__, Springer 1972. vii+304 xv+355 pp. 

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Deformation theory I_ ([ps](http://www.math.ksu.edu/~soibel/Book-vol1.ps)); _Notes on A-infinity algebras, A-infinity categories and non-commutative geometry. I_, [math.AG/0606241](http://arxiv.org/abs/math/0606241) -- two parts of large unfinished books on the subject; [[Yan Soibelman]], _Lectures on deformation theory and mirror symmetry_ ([ps](http://www.math.ksu.edu/~soibel/ipam-final.ps))

* [[Maxim Kontsevich]], _Topics in deformation theory_ (A rough write up of a Berkeley course, early 90-s), [ps](http://www.math.uchicago.edu/~mitya/langlands/kontsdef.ps)
* [[Jacob Lurie]], [[Deformation Theory]] ([arXiv:0709.3091](http://arxiv.org/abs/0709.3091)) -- describes a very setup for deformation theory over any [[(∞,1)-category]] is described. Then as an application the deformation theory of [[E-∞-ring]]s is developed. An application: J. Lurie, _Moduli problems for ring spectra_, [moduli.pdf](http://www.math.harvard.edu/~lurie/papers/moduli.pdf).

* E. Sernesi, _Deformations of algebraic schemes_ (monograph)
Grundlehren der Math. Wiss. __334__, Springer 2006. xii+339 pp. [MR2008e:14011](http://www.ams.org/mathscinet-getitem?mr=2008e:14011)

* Alexander I. Efimov, [[Valery Lunts|Valery A. Lunts]], [[Dmitri Orlov|Dmitri O. Orlov]], _Deformation theory of objects in homotopy and derived categories_ 
   * _I: general theory_ [arXiv:math/0702838](http://arxiv.org/abs/math/0702838);
   * _II: pro-representability of the deformation functor_ [arXiv:math/0702839](http://arxiv.org/abs/math/0702839);
   * _III: abelian categories_ [arXiv:math/0702840](http://arxiv.org/abs/math/0702840)

* [[Martin C. Olsson]], _Deformation theory of representable morphisms of algebraic stacks_, Mathematische Zeitschrift__253__, n. 1, 25--62 (2006) [doi](http://dx.doi.org/10.1007/s00209-005-0875-9); _Tangent spaces and obstructon theories_, lectures, [MSRISummer07.pdf](http://math.berkeley.edu/~molsson/MSRISummer07.pdf)

* B. Fantechi, M. Manetti, _Obstruction calculus for functors of Artin rings I_, J. Algebra __202__ (1998), no. 2, 541--576, [MR99f:14004](http://www.ams.org/mathscinet-getitem?mr=99f:14004).

* Domenico Fiorenza, Marco Manetti, Elena Martinengo, _Semicosimplicial DGLAs in deformation theory_, [arxiv/0803.0399](http://arxiv.org/abs/0803.0399)

* S. Merkulov, B. Vallette, _Deformation theory of properads_, [arXiv:0707.0889](http://arxiv.org/abs/0707.0889)
* [[Vladimir Hinich]], _Deformations of homotopy algebras_,  Communication in Algebra, 32 (2004), 473-494, [MR2005m:18009](http://www.ams.org/mathscinet-getitem?mr=2101417), [doi](http://dx.doi.org/10.1081/AGB-120027907), [pdf](http://math.haifa.ac.il/hinich/WEB/mypapers/dha.pdf); _Deformations of sheaves of algebras_, Adv. Math. __195__ (2005), no. 1, 102&#8211;164, [MR2007d:13021](http://www.ams.org/mathscinet-getitem?mr=2145794), [doi](http://dx.doi.org/10.1016/j.aim.2004.07.007), [pdf](http://math.haifa.ac.il/hinich/WEB/mypapers/dsa.pdf); _DG coalgebras as formal stacks_, J. Pure Appl. Algebra __162__ (2001), no. 2-3, 209--250 (<a href="http://dx.doi.org/10.1016/S0022-4049(00)00121-3">doi</a>), [math.AG/9812034](http://arxiv.org/abs/math.AG/9812034); _Formal deformations of sheaves of algebras_, video of a talk at MSRI 2002, [link](http://www.msri.org/publications/ln/msri/2002/hodgetheory/hinich/1/index.html)
* V. Hinich, V. Schechtman, _Deformation theory and Lie algebra homology_ I. Algebra Colloq. 4 (1997), no. 2, 213&#8211;240, [MR2000c:14006a](http://www.ams.org/mathscinet-getitem?mr=1682729); part II., Algebra Colloq. 4 (1997), no. 3, 291&#8211;316, [MR2000c:14006b](http://www.ams.org/mathscinet-getitem?mr=1681547); preprint version [alg-geom/9405013](http://arxiv.org/abs/alg-geom/9405013);_Homotopy Lie algebras_, I.M. Gelfand Seminar, Adv. in Sov. Math., 16 (1993), Part 2, 1-28.
* W. Lowen, M. Van den Bergh, _Deformation theory of abelian categories_, Trans. Amer. Math. Soc. __358__  (2006),  no. 12, 5441--5483; [arXiv:math.CT/0405226](http://arxiv.org/abs/math/0405226).

* M. Van den Bergh, _Notes on formal deformations of abelian categories_, [arXiv:1002.0259](http://arxiv.org/abs/1002.0259)

* M. Talpo, [[Angelo Vistoli|A. Vistoli]], _Deformation theory from the point of view of fibered categories_, [arxiv/1006.0497](http://arxiv.org/abs/1006.0497)

* B. Mazur, _Perturbations, deformations, and variations (and "Near-misses") in Geometry, Physics, and Number Theory_, [BAMS 41(3), 307-336](http://www.ams.org/bull/2004-41-03/S0273-0979-04-01024-9/S0273-0979-04-01024-9.pdf)

* M. Artin, _Deformations of singularities_, TATA Lecture Notes vol. 54.

* M. Artin, _Versal deformations and algebraic stacks_, Invent. Math. 1974

* K. Kodaira, L. Nirenberg, D. C. Spencer, _On the existence of deformation of complex analytic structures_, Ann. Math. __68__, 450-459 (1958). 

* K. Kodaira, D. C. Spencer, _On deformation of complex analytic structures_, I II, Ann. Math. __67__, 328-466 (1958). 

* M. Schlessinger, _Functors of Artin rings_, Trans. AMS 130, 208-222 (1968) -- this was a groundbreaking article at the time, still much cited. 

* B. Osserman, _Deformation theory and moduli in algebraic geometry_, [pdf](http://www.msri.org/people/members/defthy07/lectures/brian.pdf)

* [[Robin Hartshorne]], _Deformation theory_, Grad. texts in math. Springer 2010,  viii+234 pp. (draft of the chap. I-IV: [pdf](http://math.berkeley.edu/~robin/math274root.pdf)), [gBooks](http://books.google.hr/books?id=bwhEX01JlXkC&lpg=PP1&ots=2zkSvT3Bvz&dq=Robin%20Hartshorne%20deformation%20theory&pg=PP1#v=onepage&q&f=false), [doi](http://dx.doi.org/10.1007/978-1-4419-1596-2)

* [homepage](http://math.stanford.edu/~vakil/727) of Ravi Vakil's graduate Stanford class on deformation theory and moduli spaces

* [[Kai Behrend]], [[Barbara Fantechi|B. Fantechi]], _The intrinsic normal cone_, Invent. Math. __128__ (1997), no. 1, 45--88, [MR98e:14022](http://www.ams.org/mathscinet-getitem?mr=98e:14022) [arXiv:alg-geom/9601010](http://arxiv.org/abs/alg-geom/9601010)

* [[Dennis Gaitsgory]], _Lie theory from the point of view of derived algebraic geometry_, Lecture notes from a mini-course, Nantes, 2014, [web](http://www.math.harvard.edu/~gaitsgde/Nantes14/).

* Vladimir Dotsenko, Sergey Shadrin, [[Bruno Vallette]], _Pre-Lie deformation theory_, [arxiv/1502.03280](http://arxiv.org/abs/1502.03280)

* M. Gerstenhaber, S. D. Schack, _Algebras, bialgebras, quantum groups, and algebraic deformations_, in: Deformation theory and quantum groups with applications to mathematical physics (Amherst, MA, 1990), 51-92, Contemp. Math. __134__, Amer. Math. Soc. 1992.

* Gregory Ginot, Sinan Yalin, _Deformation theory of bialgebras, higher Hochschild cohomology and formality_, [arxiv/1606.01504](http://arxiv.org/abs/1606.01504)
[[!redirects deformation]]
[[!redirects deformations]]