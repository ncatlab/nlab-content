
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The __Conner-Floyd isomorphism__ ([Conner-Floyd 66, Thm. 10.1](#ConnerFloyd66), [Conner-Smith 69, Thm. 9.1](#ConnerSmith69)) is a [[natural isomorphism]] 

$$
  KU^\bullet(X)
    \cong 
  MU^\bullet(X)
    \otimes_{\Omega^U}
  \mathbb{Z}
$$

between the [[complex topological K-theory]] [[cohomology group|group]] of a finite [[CW-complex]] $X$ and the [[extension of scalars]] of the [[MU]]-[[cobordism cohomology]] of $X$ along the [[Todd genus]] $\Omega^U \overset{Td}{\longrightarrow} \mathbb{Z}$ (where $\Omega^U_{-\bullet} = MU^\bullet(\ast)$ is the [[MU]]-[[cobordism ring]] of stably almost complex manifolds $\Sigma$, and $Td(\Sigma) \in \mathbb{Z}$ is their [[Todd class]]). 

A slightly more abstract way of saying the same is

$$
  KU^\bullet(X)
    \cong 
  MU^\bullet(X)
    \otimes_{MU^\bullet}
  KU^\bullet\, 
$$

which  -- thinking now of the [[Todd genus]] as coming from the canonical [[complex oriented cohomology|complex orientation]] $MU \longrightarrow KU$ (see at _[[universal complex orientation of MU]]_) -- shows that the Conner-Floyd isomorphism is a special case of the [[Landweber exact functor theorem]].

The analogous statement holds 

* for [[MSp]] and [[KO]] ([Conner-Floyd 66](#ConnerFloyd66))

and 

* for [[MSpin]] and [[KO]] as well as [[MSpin^c]] and [[KU]] under the [[Atiyah-Bott-Shapiro orientation]] ([Hopkins-Hovey 92, Thm. 1](#HopkinsHovey92))

However, the analogous statement for 

* for [[MSU]] and [[KO]]

(via the [[Conner-Floyd orientation]]) _fails_, or rather does hold with a small modification ([Ochanine 87](#Ochanine87)).



## Related concepts

* [[Landweber exact functor theorem]]

* [[Conner-Floyd Chern class]]

## References

The original articles on the cases [[MU]]$\to$[[KU]] and [[MSp]]$\to$[[KO]]:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Theorem 10.1 in: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

  \linebreak

  Russian transl.: &#1050;&#1086;&#1085;&#1085;&#1077;&#1088; &#1055;., &#1060;&#1083;&#1086;&#1081;&#1076; &#1069;. 0 &#1089;&#1086;&#1086;&#1090;&#1085;&#1086;&#1096;&#1077;&#1085;&#1080;&#1080; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080; &#1082;&#1086;&#1073;&#1086;&#1088;&#1076;&#1080;&#1079;&#1084;&#1086;&#1074; &#1080; &#1050;-&#1090;&#1077;&#1086;&#1088;&#1080;&#1080;. - &#1044;&#1086;&#1087;&#1086;&#1083;&#1085;&#1077;&#1085;&#1080;&#1077; &#1082; &#1082;&#1085;.: &#1043;&#1083;&#1072;&#1076;&#1082;&#1080;&#1077; &#1087;&#1077;&#1088;&#1080;&#1086;&#1076;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1077; &#1086;&#1090;&#1086;&#1073;&#1088;&#1072;&#1078;&#1077;&#1085;&#1080;&#1103;. - &#1052;.: &#1052;&#1080;&#1088;, 1969 ([djvu](http://gen.lib.rus.ec/get?nametype=orig&md5=11459C40D0E52BA45BDAD92BC8AC0ACA))

with an alternative proof for [[MU]]$\to$[[KU]] in:

* {#ConnerSmith69} [[Pierre Conner]], [[Larry Smith]], Theorem 9.1 in: _On the complex bordism of finite complexes_, Publications Mathématiques de l'IHÉS, Tome 37 (1969) , pp. 117-221 ([numdam:PMIHES_1969__37__117_0](http://www.numdam.org/item/?id=PMIHES_1969__37__117_0))

Review:

* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], Theorem 6.35 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))

See also:

* Gerhard Wolff, _Der Einfluss von $K^{\ast} (-)$ auf $U^{\ast} (-)$_, Manuscripta Math. __10__ (1973), 141&#8211;-161 ([doi:10.1007/BF01475039](https://doi.org/10.1007/BF01475039))

* Gerhard Wolff,  _Vom Conner-Floyd Theorem zum Hattori-Stong Theorem_,  Manuscripta Math. __17__ (1975), no. 4, 327&#8211;-332 ([doi:10.1007/BF01170729](http://dx.doi.org/10.1007/BF01170729), [MR388420](http://www.ams.org/mathscinet-getitem?mr=388420))

The (failure of the) version for [[MSU]]$\to$[[KO]] is due to:

* {#Ochanine87} [[Serge Ochanine]], _Modules de SU-bordisme. Applications_, Bulletin de la Société Mathématique de France, Tome 115 (1987) , pp. 257-289 ([doi:10.24033/bsmf.2078]( https://doi.org/10.24033/bsmf.2078))
 
The version for [[MSpin^c]]$\to$[[MU]] and [[MSpin]]$\to$[[KO]] is due to:

* {#HopkinsHovey92} [[Michael Hopkins]], [[Mark Hovey]], _Spin cobordism determines real K-theory_, Mathematische Zeitschrift volume 210, pages 181–196 (1992) ([doi:10.1007/BF02571790](https://doi.org/10.1007/BF02571790), [[HopkinsHoveyCobordismK.pdf:file]])

Generalization to [[equivariant cohomology theory]]:

* [[Steven Costenoble]], _Equivariant Conner-Floyd isomorphism_, Trans. Amer. Math. Soc. __304__, No. 2 (Dec., 1987), 801--818, [jstor:2000742](http://www.jstor.org/stable/2000742)

Discussion in [[motivic cohomology]]:

*  [[David Gepner]], [[Victor Snaith]], _On the motivic spectra representing algebraic cobordism and algebraic K-theory_, Doc. Math., 14:359&#8211;396 (electronic), 2009, [pdf](http://www.math.uni-bielefeld.de/documenta/vol-14/14.pdf)

*  [[Ivan Panin]], Konstantin Pimenov, Oliver Röndings, _On the relation of Voevodsky’s algebraic cobordism to Quillen’s K-theory_, Invent. Math., __175__ (2009), no. 2, 435--451., [MR2470112](http://www.ams.org/mathscinet-getitem?mr=2470112)
