
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
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
    \stackrel{\overset{f^\ast}{\leftarrow}}{\stackrel{\overset{f_\ast = f_! }{\longrightarrow}}{\underset{f^!}{\leftarrow}}}
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
    \stackrel{\overset{f^\ast}{\leftarrow}}{\underset{f_\ast}{\longrightarrow}}
   QCoh(Y)
  \,.
$$

(all [[derived functors]]) If $f$ is a [[proper morphism of schemes]] then under mild further conditions there is a further [[right adjoint]] $f^!$


$$
  (f^\ast \dashv f_\ast \dashv f^!) 
   \;\colon\;
   QCoh(X)
    \stackrel{\overset{f^\ast}{\leftarrow}}{\stackrel{\overset{f_\ast}{\longrightarrow}}{\underset{f^!}{\leftarrow}}}
   QCoh(Y)
  \,.
$$

This is originally due to [[Grothendieck]], whence the name. Refined accounts are in  ([Deligne 66](#Deligne66), [Verdier 68](Verdier68), [Neeman 96](#Neeman96)).

### Quasicoherent sheaves in $E_\infty$-geometry

Generalization of this to [[E-∞ geometry]] is in ([Lurie, prop. 2.5.12](#Lurie)).

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

Generalization to [[E-∞ geometry]] is in 

* [[Jacob Lurie]], section 2.5 of _[[Quasi-Coherent Sheaves and Tannaka Duality Theorems]]_
 {#Lurie}

A clear discussion of axioms of [[six operations]], their specialization to Grothendieck context and [[Wirthmüller context]] and their consequences is in 

* H. Fausk, P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_ ([pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))
 {#May05}

[[!redirects Grothendieck contexts]]

