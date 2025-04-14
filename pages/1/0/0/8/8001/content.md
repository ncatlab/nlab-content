
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[representation]] of the [[metaplectic group]].

The [Segal-Shale-Weil metaplectic representation](#SegalShaleWeilRepresentation) is also called the _[[symplectic spinor]]_ representation.

## Segal-Shale-Weil representations
 {#SegalShaleWeilRepresentation}

The _Segal-Shale-Weil representation_ is the following. By the [[Stone-von Neumann theorem]] there is an essentially unique [[irreducible representation|irreducible]] [[unitary representation]] $W$ of the [[Heisenberg group]] $Heis(V,\omega)$ of a given [[symplectic vector space]].  This being essentially unique implies that for each element $g\in Sp(V,\omega)$ of the [[symplectic group]], there is a unique (up to multiplication by a constant of modulus one) [[unitary operator]] $U_g$ such that for all $v\in V$

$$
  W(g(v)) = U_g W(v) U^{-1}_g
  \,.
$$

The group $Mp^c$ is the [[subgroup]] of the [[unitary group]] of all such $U_g$ for $g\in Sp(V,\omega)$. The map $U_g \mapsto g$ exhibits this as a [[group extension]] by the [[circle group]]

$$
  U(1)\longrightarrow Mp^c(V,\omega) \longrightarrow Sp(V,\omega)
  \,.
$$



## Related concepts

* [[spin representation]]

* [[Langlands program]]



## References

* {#KashiwaraVergne78} M. Kashiwara; [[Michèle Vergne]], _On the Segal-Shale-Weil Representations and Harmonic Polynomials_, Inventiones mathematicae (1978) ([EuDML](https://eudml.org/doc/142517), [pdf](http://gdz-lucene.tc.sub.uni-goettingen.de/gcs/gcs?&&action=pdf&metsFile=PPN356556735_0044&divID=LOG_0008&pagesize=original&pdfTitlePage=http://gdz.sub.uni-goettingen.de/dms/load/pdftitle/?metsFile=PPN356556735_0044%7C&targetFileName=PPN356556735_0044_LOG_0008.pdf&))

* Gérard Lion, [[Michèle Vergne]]: *The Weil representation, Maslov index and Theta series*, Progress in Mathematics **6**, Birkhäuser (1980) &lbrack;[doi:10.1007/978-1-4684-9154-8](https://doi.org/10.1007/978-1-4684-9154-8)&rbrack;


* [[Joel Robbin]], [[Dietmar Salamon]], _Feynman path integrals and the metaplectic representation_, Math. Z. __221__ (1996), no. 2, 307&#8211;-335, ([MR98f:58051](http://www.ams.org/mathscinet-getitem?mr=98f:58051), [doi](http://dx.doi.org/10.1007/BF02622118), [[RobbinSalamonMetaplectic.pdf:file]])


* Maurice de Gosson, _Maslov classes, metaplectic representation and Lagrangian quantization_, Math. Research 95, Akademie-Verlag, Berlin, 1997. 186 pp.
*  Jos&#233; M. Gracia-Bond&#237;a, _On the metaplectic representation in quantum field theory_,  Classical and quantum systems (Goslar, 1991), 611&#8211;614, World Sci. 1993
* R. Ranga Rao, _The Maslov index on the simply connected covering group and the metaplectic representation_, J. Funct. Anal. __107__ (1992), no. 1, 211&#8211;233, [MR93g:22013](http://www.ams.org/mathscinet-getitem?mr=1165870), <a href="http://dx.doi.org/10.1016/0022-1236(92)90104-Q">doi</a>
* G. Burdet, M. Perrin, _Weyl quantization and metaplectic representation_, 
Lett. Math. Phys. 2 (1977/78), no. 2, 93&#8211;99, [MR473105](http://www.ams.org/mathscinet-getitem?mr=473105), [doi](http://dx.doi.org/10.1007/BF00398573)
* Y. Flicker, [[D. Kazhdan]], G. Savin, _Explicit realization of a metaplectic representation_, J. Analyse Math. __55__ (1990), 17&#8211;39, [MR92c:22036](http://www.ams.org/mathscinet-getitem?mr=1094709), [doi](http://dx.doi.org/10.1007/BF02789195)

* [[Gerald B. Folland]], Chapter 4 in: *A course in abstract harmonic analysis*, Studies in Advanced Mathematics. CRC Press (1995) &lbrack;[pdf](https://sv.20file.org/up1/1415_0.pdf), [gBooks](http://books.google.com/books?hl=en&lr=&id=0VwYZI1DypUC)&rbrack;


[[!redirects metaplectic representations]]

[[!redirects Segal-Shale-Weil representation]]
