
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}
 

## Idea


Given a (oriented) [[topological manifold]] $X$, its __mapping class group__ $MCG(X)$ is the [[group]] of [[isotopy]] classes of (orientation preserving) [[homeomorphisms]] $X\to X$. 

Often this is considered specifically for $X$ a [[Riemann surface]] with punctures in which case
a central role is played by [[Dehn twists]]. 

The mapping class group is of importance in many areas of geometry including study of [[Teichmüller spaces]], of [[moduli spaces]] of surfaces, of [[automorphisms]] of [[free groups]] and in geometric and [[combinatorial group theory]], hyperbolic geometry and so on. Some of the key contributors were [[Max Dehn]], [[Jakob Nielsen]], [[William Thurston]], [[David Mumford]]. Recent proof of the related Mumford conjecture has been accomplished by Madsen and Weiss.

## Definition


For $\mathbf{Aut}(X)$ the [[automorphism group]] of the [[manifold]] formed in [[Euclidean-topological infinity-groupoids|Euclidean topological geometry]], hence equipped with its canonical structure of a [[topological group]]. Let furthermore $\mathbf{Aut}_0(X) \hookrightarrow \mathbf{Aut}(X)$ be the inclusion of the connected component of the identity.

Then

$$
  \mathbf{MCG}(X) \coloneqq \mathbf{Aut}(X)/\mathbf{Aut}_0(X)
$$

is the corresponding [[coset space]]/[[quotient group]]. In other words, the mapping class group is the group of [[homeomorphism]] of $X$ onto itself, modulo [[isotopy]]. 

This is a [[discrete group]]. Equivalently it is the group of [[connected components]] of $\mathbf{Aut}(X)$. If $X$ is a [[smooth manifold]], then the mapping class group is the group of connected components of the [[diffeomorphism group]]

$$
  MCG(X) = \pi_0(Diff(X))
 \,.
$$

If $X$ is a manifold with boundary $\partial X$, then it is usual to consider automorphisms which restrict to the identity on the boundary. 


## Properties

### For 2-dimensional surfaces

The mapping class group for 2-dimensional manifolds controls the [[moduli stack of complex curves]]. 

The [[classifying spaces]] of mapping class groups for 2-[[dimension]]al [[manifolds]] may also be encoded combinatorially in the [[geometric realization]] of a [[category]] of [[ribbon graphs]]. See there for details. 

One of the classical results is that the (oriented) mapping class group of the [[torus]] $\mathbb{R}^2/\mathbb{Z}^2 \cong (S^1)^2$ is isomorphic to the [[special linear group]] [[SL(2,Z)|$SL_2(\mathbb{Z})$]], and generally $MCG(\mathbb{R}^n/\mathbb{Z}^n) \cong SL_n(\mathbb{Z})$). 

Certain generators called [[Dehn twists]] may be visualized as cutting a torus along a circle $\{a\} \times S^1$ (or $S^1 \times \{b\}$), thus producing a cylinder, then twisting one of the ends of the cylinder through $2\pi$ and reattaching the two ends. 

Another example is a 2-disk with $n$ punctures. The group of diffeomorphisms (fixing the boundary pointwise) modulo isotopy is the [[braid group]] $B_n$. 

The relation to the [[homotopy type]] of the [[diffeomorphism group]] is as follows:

+-- {: .num_prop}
###### Proposition


For $\Sigma$ a [[closed manifold|closed]] [[orientation|orientable]] [[surface]], then the [[fundamental ∞-groupoid|bare homotopy type]] of its diffeomorphism group is

1. if $\Sigma$ is the [[sphere]] then
 
   $$
     \begin{aligned} 
        \Pi(Diff(S^2)) & \simeq \Pi(O(3))
        \\
        & \simeq MCG(S^2)\times \Pi(SO(3))
        \\
        & \simeq \mathbb{Z}_2 \times \Pi(SO(3))
     \end{aligned}
   $$

1. if $\Sigma$ is the [[torus]] then

   $$
     \begin{aligned}
       \Pi(Diff(S^1 \times S^1)) 
       & \simeq 
       MCG(S^1 \times S^1)\times \Pi(S^1 \times S^1 )
       \\
       & \simeq GL_2(\mathbb{Z}) \times B(\mathbb{Z} \times\mathbb{Z})
     \end{aligned}
   $$ 

1. in all other cases all higher [[homotopy groups]] vanish:

   $$
     \Pi(Diff(\Sigma)) \simeq MCG(\Sigma)
   $$

=--

The first statement is due to ([Smale 58](#Smale58)), see also at _[[sphere eversion]]_. The second and third are due to ([Earle-Eells 67](#EarleEells67), [Gramain 73](#Gramain73)).

See [Hatcher 12](#Hatcher12) for review and see at *[diffeomorphism group -- For surfaces](diffeomorphism+group#HomotopyTypeForSurfaces)* for more.

On equivalently using homeomorphisms instead of diffeomorphisms: [Boldsen 2009](#Boldsen09).



### Rational cohomology

The [[ordinary cohomology]] with rational coefficients of the [[delooping]] of the stable mapping class group of 2-dimensional manifolds (hence essentially the [[orbifold cohomology]] of the [[moduli stack of complex curves]]) is the content of [[Mumford's conjecture]], proven in ([Madsen-Weiss 02](#MadsenWeiss02)).


## Examples

\begin{proposition}
\label{MCGOfClosedOrientedSurfaces}
  The mapping class group of the [[torus]] $T^2 = \Sigma^2_1$ is the [[modular group]] [[SL(2,Z)|$SL_2(\mathbb{Z})$]]
$$
  MCG(T^2) \,\simeq\, Sp_2(\mathbb{Z}) \,\simeq\, SL_2(\mathbb{Z}) 
  \,,
$$
and generally the mapping class group of [[generalized the|the]] [[closed manifold|closed]] [[orientation|oriented]] [[surface]] $\Sigma^2_g$ of [[genus of a surface|genus]] $= g \in \mathbb{N}$ sits in a [[short exact sequence]] of the form
$$
  1 
    \to 
  I_g 
  \longrightarrow
  MCG(\Sigma^2_g)
  \longrightarrow
  Sp_{2g}(\mathbb{Z})
  \to 1
  \mathrlap{\,,}
$$
where $Sp_{2g}(\mathbb{Z}) \coloneqq Sp_{2g}(\mathbb{R}) \cap GL_{2g}(\mathbb{Z})$ is the [[symplectic group]] with [[integer]] [[coefficients]], and where the [[kernel]] is called the *[[Torelli group]]*.

Here the canonical [[group action]] of $MCG(\Sigma^2_g)$ on the [[ordinary homology]] $H_1(\Sigma^2_g;\mathbb{Z}) \simeq \mathbb{Z}^g \times \mathbb{Z}^g$ of the surface is through the defining action of $Sp_2(\mathbb{Z})$.
\end{proposition}
(reviewed by [Morita 2007 §6](#Morita07), [Farb & Margalit 2012 §6](#FarbMargalit12))


## Related concepts

* [[diffeomorphism group]]

* [[Alexander's trick]]

* [[braid group]]


## References

### General

Monographs:

* {#Birman75} [[Joan S. Birman]], _Braids, links, and mapping class groups_, Princeton Univ Press (1975) &lbrack;[ISBN:9780691081496](https://press.princeton.edu/books/paperback/9780691081496/braids-links-and-mapping-class-groups-am-82-volume-82), [preview pdf](https://api.pageplace.de/preview/DT0400.9781400881420_A26691398/preview-9781400881420_A26691398.pdf)&rbrack;

* {#FarbMargalit12} [[Benson Farb]], [[Dan Margalit]]: *A primer on mapping class groups*, Princeton Mathematical Series, Princeton University Press (2012) &lbrack;[ISBN:9780691147949](https://press.princeton.edu/books/hardcover/9780691147949/a-primer-on-mapping-class-groups), [jstor:j.ctt7rkjw](https://www.jstor.org/stable/j.ctt7rkjw), [pdf](http://euclid.nmu.edu/~joshthom/Teaching/MA589/farbmarg.pdf)&rbrack;

Surveys:

* [[Shigeyuki Morita]]: *Structure of the mapping class groups of surfaces: a survey and a prospect*, Geom. Topol. Monogr. **2** (1999) 349-406 &lbrack;[arXiv:math/9911258](https://arxiv.org/abs/math/9911258), [pdf](https://msp.org/gtm/1999/02/gtm-1999-02-020p.pdf)&rbrack;

* Nikolai V. Ivanov: *Mapping class groups*, in: *Handbook of Geometric Topology*, North-Holland (2002) 523-633 &lbrack;[doi:10.1016/B978-0-444-82432-5.X5000-8](https://doi.org/10.1016/B978-0-444-82432-5.X5000-8), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/handgt.pdf), 1998 draft: [pdf](https://math.hawaii.edu/~andrew/GDT2013/I98.pdf), [ps](http://www.mth.msu.edu/~ivanov/m99.ps)&rbrack;

* {#BakalovKirillov} [[Bojko Bakalov]], [[Alexander Kirillov]], chapter 5 of: *Lectures on tensor categories and modular functor*, University Lecture Series **21**, Amer. Math. Soc. (2001)  &lbrack;[web](http://www.math.sunysb.edu/~kirillov/tensor/tensor.html), [ams:ulect/21](https://bookstore.ams.org/view?ProductCode=ULECT/21), [[BakalovKirillovChapter5.pdf:file]]&rbrack;

* {#Morita07} [[Shigeyuki Morita]]: *Introduction to mapping class groups of surfaces and related groups*, in: *Handbook of Teichmüller theory, Volume I*, EMS (2007) 353-386 &lbrack;[doi:10.4171/029-1/8](https://doi.org/10.4171/029-1/8), [[Morita-IntroductionMCG.pdf:file]]&rbrack;

Lecture notes:

* [[Gwénaël Massuyeau]]: _A short introduction to mapping class groups_, presentation at *Master Class on Geometry* Strasbourg (2009) &lbrack;[pdf](https://massuyea.perso.math.cnrs.fr/notes/MCG.pdf), [[Massuyeau-MCG.pdf:file]]&rbrack;

* [[Henry Wilton]]: *Mapping class groups*, lecture notes (2021) &lbrack;[pdf](https://www.dpmms.cam.ac.uk/~hjrw2/MCG%20lectures.pdf), examples: 1:[pdf](https://www.dpmms.cam.ac.uk/~hjrw2/MCGs%20Sheet%201.pdf), 2:[pdf](https://www.dpmms.cam.ac.uk/~hjrw2/MCGs%20Sheet%202.pdf), 3:[pdf](https://www.dpmms.cam.ac.uk/~hjrw2/MCGs%20Sheet%203.pdf)&rbrack;

Via generators-and-relations:

* Sylvain Gervais: *A finite presentation of the mapping class group of an oriented surface* &lbrack;[arXiv:math/9811162](https://arxiv.org/abs/math/9811162)&rbrack;

* Bronisław Wajnryb: *An elementary approach to the mapping class group of a surface*, Geometry & Topology **3** (1999) 405–466 &lbrack;[doi:10.2140/gt.1999.3.405](http://dx.doi.org/10.2140/gt.1999.3.405)&rbrack;

See also:

* Wikipedia: *[Mapping class group](http://en.wikipedia.org/wiki/Mapping_class_group)*

More on the equivalence of MCGs defined via [[diffeomorphisms]] or [[homeomorphisms]]:

* {#Boldsen09} Søren Kjærgaard Boldsen: *Different versions of mapping class groups of surfaces* &lbrack;[arXiv:0908.2221](https://arxiv.org/abs/0908.2221)&rbrack;


In relation to [[motion groupoids]]:

* [[Fiona Torzewska]], [[João Faria Martins]], [[Paul Purdon Martin]], *Motion groupoids and mapping class groupoids*, Comm. Math. Phys. **402** (2023) 1621-1705 &lbrack;[arXiv:2103.10377](https://arxiv.org/abs/2103.10377), [doi:10.1007/s00220-023-04755-0](https://doi.org/10.1007/s00220-023-04755-0)&rbrack;


### Braid groups

Understanding of [[braid groups]] as subgroups of mapping class groups of punctured [[surfaces]] with [[boundary]]:

* [[Wilhelm Magnus]], *Über Automorphismen von Fundamentalgruppen berandeter Flächen*, Mathematische Annalen **109** (1934) 617–646 &lbrack;[doi:10.1007/BF01449158](https://doi.org/10.1007/BF01449158)&rbrack;

* {#MargalitWinarski21} [[Dan Margalit]], [[Rebecca R. Winarski]], *Braid groups and mapping class groups: The Birman–Hilden theory*, Bull. London Math. Soc. **53** 3 (2021) 643-659 &lbrack;[arXiv:1703.03448](https://arxiv.org/abs/1703.03448), [doi:10.1112/blms.12456](https://doi.org/10.1112/blms.12456)&rbrack;


Algebraic descriptions of such mapping class groups/[[braid groups]]:

* [[Warren Dicks]], Edward Formanek, *Algebraic Mapping-Class Groups of Orientable Surfaces with Boundaries*, in: *Infinite Groups: Geometric, Combinatorial and Dynamical Aspects*, Progress in Mathematics **248** Birkhäuser (2005) &lbrack;[doi:10.1007/3-7643-7447-0_4](https://doi.org/10.1007/3-7643-7447-0_4)&rbrack;
   
Exposition and Review:

* [Birman 1975 §4](braid+group#Birman75)

* [González-Meneses 2011 §1.4](braid+group#González-Meneses11)

* [Massuyeau 2021 §3.3](braid+group#Massuyeau21)

* [Abadie 2022 §1.3](braid+group#Abadie22)

See also:

* {#MadsenWeiss02} [[Ib Madsen]], [[Michael Weiss]], _The stable moduli space of Riemann surfaces: [[Mumford's conjecture]]_,  Ann. of Math. (2) __165__ (2007), no. 3, 843--941, [MR2009b:14051](http://www.ams.org/mathscinet-getitem?mr=2009b:14051), [doi](http://dx.doi.org/10.4007/annals.2007.165.843), [math.AT/0212321](http://arxiv.org/abs/math.AT/0212321)

* John Harer, _The second homology group of the mapping class group of an orientable surface_, Invent. Math., **72**  2  221-239 (1983) _The cohomology of the moduli space of curves_ in: Theory of moduli (Montecatini Terme, 1985), Lecture Notes in Math. __1337__, p. 138&#8211;221. Springer, Berlin, 1988.

* Robert C. Penner, _The decorated Teichm&#252;ller space of punctured surfaces_, Commun. Math. Phys. __113__ (2) (1987) 299--339. [MR89h:32044](http://www.ams.org/mathscinet-getitem?mr=89h:32044); _A construction of pseudo-Anosov homeomorphisms_, Trans. Amer. Math. Soc. __310__ (1):179&#8211;197, 1988.

* {#EarleEells67} C.J. Earle,  J. Eells, _The diffeomorphism group of a compact Riemann surface,
Bulletin of the American Mathematical Society 73(4) 557--559, 1967


* [[Allen Hatcher]], [[William Thurston]], _A presentation for the mapping class group of a closed orientable surface_, Topology, 19(3):221&#8211;237, 1980.

* {#Hatcher12} [[Allen Hatcher]], _A 50-Year View of Diffeomorphism Groups_, talk at the 50th Cornell Topology Festival in May 2012 ([pdf](http://www.math.cornell.edu/~hatcher/Papers/Diff%28M%292012.pdf))

* [[Max Dehn]], Papers on group theory and topology. Springer-Verlag, New York, 1987. Transl. from German with intro. and appendix by John Stillwell, and appendix by [[Otto Schreier]].

* [[Jakob Nielsen]], _Untersuchungen zur Topologie der geschlossenen zweiseitigen Fl&#228;chen. I-III_, Acta Math. 50 (1927), no. 1, 189--358, MR1555256, [doi](http://dx.doi.org/10.1007/BF02547775); Acta Math. 53 (1929), no. 1, 1--76, MR1555290, [doi](http://dx.doi.org/10.1007/BF02547566);  Acta Math. 58 (1932), no. 1, 87--167, MR1555345, [doi](http://dx.doi.org/10.1007/BF02547775)

* [[David Mumford]], _Abelian quotients of the Teichm&#252;ller modular group_, J. Analyse Math., 18:227&#8211;244, 1967.
* [[David Mumford]], _Towards an enumerative geometry of the moduli space of curves_, Arithmetic and geometry, Vol. II, Birkh&#228;user Boston, Boston, MA, 1983, pp. 271&#8211;328, [MR85j:14046](http://www.ams.org/mathscinet-getitem?mr=85j:14046)

* [[Ulrike Tillmann]], _On the homotopy of the stable mapping class group_,  Invent. Math. __130__ (1997), no. 2, 257--275, [MR99k:57036](http://www.ams.org/mathscinet-getitem?mr=99k:57036), [doi](http://dx.doi.org/10.1007/BF02421324)


* E. Y. Miller, _The homology of the mapping class group_, J. Differential Geom. __24__ (1986), no. 1, 1&#8211;14, [MR88b:32051](http://www.ams.org/mathscinet-getitem?mr=88b:32051), [euclid](http://projecteuclid.org/euclid.jdg/1214440254)


### Finite-index Subgroups

On [[finite number|finite]] [>index of a subgroup|index]] [[subgroups]] of mapping class groups:

* {#Grossman74} Edna K. Grossman: *On the residual finiteness of certain mapping class groups*,  J. London Math. Soc. **s2-9** 1 (1974) 160–164 &lbrack;[doi;10.1112/jlms/s2-9.1.160](https://doi.org/10.1112/jlms/s2-9.1.160)&rbrack;
  > ($MCG(\Sigma^2_g)$ is [[residually finite group|residually finite]])

* D. B. McReynolds: *The congruence subgroup problem for braid groups: Thurston's proof*, New York Jour. Math. **18** (2012) 925-942 &lbrack;[arXiv:0901.4663](https://arxiv.org/abs/0901.4663), [nyjm:2012/18-47](https://nyjm.albany.edu/j/2012/18-47.html)&rbrack;


* [[Andrew Putman]]: *The Torelli group and congruence subgroups of the mapping class group*, in: *Moduli Spaces of Riemann Surfaces*, IAS/Park City Mathematics Series **20** (2013) &lbrack;[arXiv:1201.3946](https://arxiv.org/abs/1201.3946), [doi:10.1090/pcms/020](https://doi.org/10.1090/pcms/020)&rbrack;


* Luis Paris, Jon A Berrick, Volker Gebhardt: *Finite index subgroups of mapping class groups*, Proceedings of the London Mathematical Society **108** 3 (2013) 575-599 &lbrack;[arXiv:1105.2468](https://arxiv.org/abs/1105.2468), [doi:10.1112/plms/pdt022](https://doi.org/10.1112/plms/pdt022)&rbrack;

* Blazej Szepietowski: *On finite index subgroups of the mapping class group of a nonorientable surface*, Glas. Mat. **49** (2014), 337-350 &lbrack;[arXiv:1401.3557](https://arxiv.org/abs/1401.3557), [doi:10.3336/gm.49.2.08](https://doi.org/10.3336/gm.49.2.08)&rbrack;



### For orbifolds
 {#ReferencesForOrbifolds}

On mapping class groups in the generality of [[orbifold|orbifolded]]-[[surfaces]]:

* Jonas Flechsig: *Braid groups and mapping class groups for 2-orbifolds*, PhD thesis, Bielefeld (2023) &lbrack;[doi:10.4119/unibi/2979933](https://doi.org/10.4119/unibi/2979933), [pdf](https://pub.uni-bielefeld.de/download/2979933/2979943/braid_groups_and_mapping_class_groups_for_2-orbifolds.pdf)&rbrack;

* Jonas Flechsig: *Mapping class groups for 2-orbifolds* &lbrack;[arXiv:2305.04272](https://arxiv.org/abs/2305.04272)&rbrack;

* Jonas Flechsig: *Braid groups and mapping class groups for 2-orbifolds* &lbrack;[arXiv:2305.04273](https://arxiv.org/abs/2305.04273)&rbrack;



[[!redirects mapping class groups]]