
#Contents#
* table of contents
{:toc}

## Idea


__Macdonald polynomials__ are a generalization of a [[Schur function]]s; they unify a theory of Hall-Littlewood and [[Jack polynomial]]s. They form a family of [[orthogonal polynomials]] which are [[symmetric functions]] in $x_1,\ldots,x_n$ with coefficients which are rational functions of two additional variables $q$ and $t$. 

Given a [[partition]] $\lambda$, one defines a shift operator $T_{q,x_i}$ which maps $f = f(x_1,\ldots, x_n)$ to $f(x_1,\ldots, x_{i-1}, q x_i, x_{i+1},\ldots,x_n)$ and the operators $D_r$, $r = 0, 1, \ldots, n$ via

$$
D_r = t^{\frac{r(r-1)}{2}} \sum_{I\subset \{1,\ldots,n\}, |I| = r} \prod_{i\in I, j\notin I} \frac{t x_i-x_j}{x_i-x_j}\prod_{i\in I} T_{q, x_i},
$$
and the corresponding generating series $D := \sum_{r=0}^n D_r u^r$. 

The __Macdonald polynomial__ $P_\lambda(x;q,t)$ is an eigenfunction of $D$ with the eigenvalue

$$
\prod_{i=1}^n (1 + u t^{n-i} q^{\lambda_i})
$$

In the case $q = t$ we get the [[Schur function]] $P_\lambda(x; t,t) = s_\lambda(t)$. Similarly, shifted Macdonald polynomials generalize shifted Schur functions. 


## References

* [[Ian G. Macdonald]],  *A New Class of Symmetric Functions*, Publ. I.R.M.A. **372** (S-20) (1988) 131-171 &lbrack;[web](https://www.mat.univie.ac.at/~slc/opapers/s20macdonald.html)&rbrack;

* [[Ian G. Macdonald]], _Symmetric functions and Hall polynomials_, Oxford Math. Monographs, 2nd enlarged ed. (1995) &lbrack;[pdf](https://math.berkeley.edu/~corteel/MATH249/macdonald.pdf)&rbrack;


* Wikipedia, *[Macdonald polynomial](http://en.wikipedia.org/wiki/Macdonald_polynomials)*

* A. M. Garsia, C. Procesi, _On certain graded $S_n$-modules and the $q$-Kostka polynomials_, Adv. Math. __94__ (1992) 82-138
* A. Okounkov, _(Shifted) Macdonald polynomials: q-integral representation and combinatorial formula_, Compositio Math. __112__ (1998), 147&#8211;182. [MR99h:05120](http://www.ams.org/mathscinet-getitem?mr=1626029), [doi](http://dx.doi.org/10.1023/A:1000436921311), _BC-type interpolation Macdonald polynomials and binomial formula for Koornwinder polynomials_, Transform. Groups __3__ (1998) 181&#8211;207, [MR99h:33061](http://www.ams.org/mathscinet-getitem?mr=1628453), _Combinatorial formula for Macdonald polynomials and generic Macdonald polynomials_, Transform. Groups __8__ (2003), no. 3, 293&#8211;305, [MR2004e:05202](http://www.ams.org/mathscinet-getitem?mr=1996418), [doi](http://dx.doi.org/10.1007/s00031-003-0306-0)
* N. Bergeron, A. M. Garsia, _On certain spaces of harmonic polynomials_, in: Hypergeometric functions on domains of positivity, Jack polynomials, and applications (Tampa, FL, 1991), Contemp. Math. __138__, 51&#8211;86 (Amer. Math. Soc. 1992)
* A. Yu. Okounkov, _A remark on the Fourier pairing and the binomial formula for the Macdonald polynomials_, Funktsional. Anal. i Prilozhen. 36 (2002), no. 2, 62--68, 96; translation in Funct. Anal. Appl. 36 (2002), no. 2, 134&#8211;139, [doi](http://dx.doi.org/10.1023/A:1015670523770)
* G. Felder, L. Stevens, [[A. Varchenko]], _Modular transformations of the elliptic hypergeometric functions, Macdonald polynomials, and the shift operator_, Moscow Math. J. __3__, n. 2 (2003), 457-473, [pdf](http://www.ams.org/distribution/mmj/vol3-2-2003/felder-etal.pdf), [arXiv:math.QA/0203049](http://lanl.arxiv.org/abs/math/0203049), [MR2025269](http://www.ams.org/mathscinet-getitem?mr=2025269)
* Mark Haiman, _Hilbert schemes, polygraphs and the Macdonald positivity conjecture_, J. Amer. Math. Soc. __14__ (2001), no. 4, 941&#8211;1006, [MR2002c:14008](http://www.ams.org/mathscinet-getitem?mr=1839919), [doi](http://dx.doi.org/10.1090/S0894-0347-01-00373-3); _Macdonald polynomials and geometry_, in: New perspectives in algebraic combinatorics (Berkeley, CA, 1996&#8211;97), 207&#8211;254, Math. Sci. Res. Inst. Publ. __38__, Cambridge Univ. Press 1999, [pdf](http://math.berkeley.edu/~mhaiman/ftp/nfact/msri.pdf)
* M. Haiman, _Cherednik algebras, Macdonald polynomials and combinatorics_, Proc. ICM, Madrid 2006, Vol. III, 843-872, [djvu scan](http://www.mathunion.org/ICM/ICM2006.3/Main/icm2006.3.0843.0872.ocr.djvu), [author's pdf](http://math.berkeley.edu/~mhaiman/ftp/icm-2006/comb-mac-chered.pdf)
* M. Haiman, A. Woo, _Geometry of $q$ and $q,t$-analogs in combinatorial enumeration_, in: Geometric combinatorics, 207&#8211;248,
IAS/Park City Math. Ser. __13__, Amer. Math. Soc., Providence, RI, 2007, [pdf](http://math.berkeley.edu/~mhaiman/ftp/pcmi-2004/notes.pdf), [ps](http://math.berkeley.edu/~mhaiman/ftp/pcmi-2004/notes.ps)
* A. M. Garsia, M. Haiman, _A graded representation model for Macdonald's polynomials_, Proc. Nat. Acad. Sci. U.S.A. __90__ (1993) 3607&#8211;3610, [MR94b:05206](http://www.ams.org/mathscinet-getitem?mr=1214091), [PNAS](http://www.pnas.org/cgi/reprintframed/90/8/3607)
* A. M. Garsia, G. Tesler, _Plethystic formulas for Macdonald $q, t$-Kostka coefficients_, Advances in Math. __123__ (1996) 144&#8211;222, [MR1420484](http://www.ams.org/mathscinet-getitem?mr=1420484); A. M. Garsia, J. Remmel, _Plethystic formulas and positivity for $q,t$-Kostka coefficients_, Mathematical essays in honor of Gian-Carlo Rota (Cambridge, MA, 1996), 245&#8211;262, Progr. Math. __161__, Birkh&#228;user  1998, [MR99j:05189d](http://www.ams.org/mathscinet-getitem?mr=1627327)
* Friedrich Knop, _Integrality of two variable Kostka functions_,
J. Reine Angew. Math. 482 (1997), 177&#8211;189, [doi](http://dx.doi.org/10.1515/crll.1997.482.177), [MR99j:05189c](http://www.ams.org/mathscinet-getitem?mr=1427661)
* Siddhartha Sahi, _Interpolation, integrality, and a generalization of Macdonald's polynomials_, Internat. Math. Res. Notices 1996, no. 10, 457&#8211;471, [MR99j:05189b](http://www.ams.org/mathscinet-getitem?mr=1399411), [doi](http://dx.doi.org/10.1155/S107379289600030X)
* Anatol N. Kirillov, [[Masatoshi Noumi]], _Affine Hecke algebras and raising operators for Macdonald polynomials_, Duke Math. J. __93__ (1998), no. 1, 1--39, [MR99j:05189a](http://www.ams.org/mathscinet-getitem?mr=1620075), [doi](https://doi.org/10.1215/S0012-7094-98-09301-2)
* Anatol Kirillov Jr., _Traces of intertwining operators and Macdonald's polynomials_, [q-alg/9503012](http://arxiv.org/abs/q-alg/9503012)
* Anton Gerasimov, Dimitri Lebedev, Sergey Oblezin, _Baxter operator formalism for Macdonald polynomials_. [arxiv/1204.0926](http://arxiv.org/abs/1204.0926)
* Persi Diaconis, [[Arun Ram]], _A probabilistic interpretation of the Macdonald polynomials_, [arxiv/1007.4779](http://arxiv.org/abs/1007.4779)
* Anton Khoroshkin, _Highest weight categories and Macdonald polynomials_, [arxiv/1312.7053](http://arxiv.org/abs/1312.7053)
*  E. Carlsson, E. Gorsky, A. Mellit, The $\mathbf{A}_{q,t}$ algebra and parabolic flag Hilbert schemes [arxiv/1710.01407](https://arxiv.org/abs/1710.01407);  A. Garsia, A. Mellit, _Five-term relation and Macdonald polynomials_, [arxiv/1604.08655](https://arxiv.org/abs/1604.08655); A. Mellit, _Plethystic identities and mixed Hodge structures of character varieties_, [arxiv/1603.00193](https://arxiv.org/abs/1603.00193) 
* Wy. Chuang, D-E. Diaconescu, R. Donagi, [[T. Pantev]], _Parabolic refined invariants and Macdonald polynomials_, Commun. Math. Phys. __335__, 1323--1379 (2015) [doi](https://doi.org/10.1007/s00220-014-2184-9)

> A string theoretic derivation is given for the conjecture of Hausel, Letellier and Rodriguez-Villegas on the cohomology of character varieties with marked points. Their formula is identified with a refined BPS expansion in the stable pair theory of a local root stack, generalizing previous work of the first two authors in collaboration with Pan. Haiman’s geometric construction for Macdonald polynomials is shown to emerge naturally in this context via geometric engineering. In particular this yields a new conjectural relation between Macdonald polynomials and refined local orbifold curve counting invariants. The string theoretic approach also leads to a new spectral cover construction for parabolic Higgs bundles in terms of holomorphic symplectic orbifolds.

category: algebra, combinatorics

[[!redirects Macdonald polynomials]]

[[!redirects Hall polynomial]]
[[!redirects Hall polynomials]]
