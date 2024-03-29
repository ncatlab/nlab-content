
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Grothendieck context_ is a pair of two [[symmetric monoidal categories]] $(\mathcal{X}, \otimes_X, 1_{X})$, $(\mathcal{Y}, \otimes_Y, 1_Y)$ which are connected by an [[adjoint triple]] of [[functors]] such that the leftmost one is a [[closed monoidal functor]].

This is the variant/special case of the [[yoga of six operations]] with two [[adjoint pairs]] $(f_! \dashv f^!)$ and $(f^\ast \dashv f_\ast)$ for $f_! \simeq f_\ast$. 

$$
  f^\ast \dashv (f_\ast = f_!) \dashv f^!
  \;\colon\;
  \mathcal{X}
   \;
    \array{
     \overset{f^\ast}{\longleftarrow}
     \\
     \overset{f_\ast = f_! }{\longrightarrow}
     \\
     \overset{f^!}{\longleftarrow}
    }
    \;
  \mathcal{Y}
  \,.
$$

(The other specialization of the [[six operations]] where $f^\ast \simeq f^!$ is called the _[[Wirthmüller context]]_).

The existence of the (derived) right adjoint $f^!$ to $f_\ast$ is what is called _[[Grothendieck duality]]_.

## Examples

### Quasicoherent sheaves on schemes
 {#QuasicoeherntSheavesOnSchemes}

A [[homomorphism]] of [[schemes]] $f \;\colon\; X \longrightarrow Y$ induces an [[inverse image]] $\dashv$ [[direct image]] [[adjunction]] on the [[derived categories]] $QCoh(-)$ of [[quasicoherent sheaves]]

$$
  (f^\ast \dashv f_\ast) 
   \;\colon\;
   QCoh(X)
    \underoverset 
     \overset{f^\ast}{\longleftarrow}
     \overset{f_\ast}{\longrightarrow}
     {\bot}
   QCoh(Y)
  \,.
$$

(all [[derived functors]]) If $f$ is a [[proper morphism of schemes]] then under mild further conditions there is a further [[right adjoint]] $f^!$


$$
  (f^\ast \dashv f_\ast \dashv f^!) 
   \;\colon\;
   QCoh(X)
    \;
    \array{
      \overset{f^\ast}{\longleftarrow}
      \\
      \overset{f_\ast}{\longrightarrow}
      \\
      \overset{f^!}{\longleftarrow}
     }
   \;
   QCoh(Y)
  \,.
$$

This is originally due to [[Grothendieck]], whence the name. Refined accounts are in  ([Deligne 66](#Deligne66), [Verdier 68](Verdier68), [Neeman 96](#Neeman96)).

### Quasicoherent sheaves in $E_\infty$-geometry

Generalization of the pull-push [[adjoint triple]] to [[E-∞ geometry]] is in ([LurieQC, prop. 2.5.12](#LurieQC)) and the [[projection formula]] for this is in ([LurieProp, remark 1.3.14](#LurieProper)).

## Related concepts

* [[Wirthmüller context]]

* [[Verdier-Grothendieck context]]

## References

The original construction for [quasicoherent sheaves on schemes](#QuasicoeherntSheavesOnSchemes) is due to [[Alexander Grothendieck]], whence the name "Grothendieck context". 

Further stream-lined accounts then appeared in 

* [[Pierre Deligne]], _Cohomology &#224; support propre en construction du foncteur $f^!$_, Appendix to: _Residues and Duality_, Lecture Notes in Math., vol. 20, Springer-Verlag, Heidelberg, 1966, pp. 404{421. MR 36:5145
 {#Deligne66}

* [[Jean-Louis Verdier]], _Base change for twisted inverse images of coherent sheaves_, Collection: Algebraic Geometry (Internat. Colloq.), Tata Inst. Fund. Res., Bombay, 1968, pp. 393-408. MR 43:227
 {#Verdier68}

Further refinement and highlighting of the close relation to the [categorical Brown representability theorem](Brown+representability+theorem#CategoricalBrownRepresentability) is in 

* [[Amnon Neeman]], _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, J. Amer. Math. Soc. 9 (1996), 205-236 ([web](http://www.ams.org/journals/jams/1996-9-01/S0894-0347-96-00174-9/))
 {#Neeman96}

Discussion of [[integral transforms]] in Grothendieck contexts is in 

* [[Alexander Polishchuk]], _Kernel algebras and generalized Fourier-Mukai transforms_ ([arXiv:0810.1542](http://arxiv.org/abs/0810.1542))
 {#Polishchuk}

Generalization of the pull-push [[adjoint triple]] to [[E-∞ geometry]] is in 

* {#LurieQC} [[Jacob Lurie]], section 2.5 of _[[Quasi-Coherent Sheaves and Tannaka Duality Theorems]]_
 

and the [[projection formula]] for this triple appears as remark 1.3.14 of 

* {#LurieProper} [[Jacob Lurie]], _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

A clear discussion of axioms of [[six operations]], their specialization to Grothendieck context and [[Wirthmüller context]] and their consequences is in 

* {#May05} [[Halvard Fausk]], [[Po Hu]], [[Peter May]],  *Isomorphisms between left and right adjoints*, Theory and Applications of Categories, **11** 4 (2003) 107-131 &lbrack;[tac:11-04](http://www.tac.mta.ca/tac/volumes/11/4/11-04abs.html), [pdf](http://www.math.uiuc.edu/K-theory

* {#BalmerDellAmbrogioSanders15} [[Paul Balmer]], [[Ivo Dell'Ambrogio]], [[Beren Sanders]], _Grothendieck-Neeman duality and the Wirthm&#252;ller isomorphism_, [arXiv:1501.01999](http://arxiv.org/abs/1501.01999).

[[!redirects Grothendieck contexts]]