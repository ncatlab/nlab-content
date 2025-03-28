
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a context $\mathbf{H}$ of [[differential cohesion]] with $\Im$ the [[infinitesimal shape modality]], then for any object $X\in \mathbf{H}$ the [[base change]] [[comonad]] 

$$
  Jet_X \coloneqq i^\ast i_\ast
$$

for base change along the $X$-component of the [[unit of a monad|unit]] of $\Im$ 

$$
  \mathbf{H}_{/X}
  \stackrel{\overset{i^\ast}{\longleftarrow}}{\underset{i_\ast}{\longrightarrow}}
  \mathbf{H}_{/\Im(X)}
  \,,
$$

may be interpreted as sending any [[bundle]] over $X$ to its [[jet bundle]]. 

{#Kock10Remark731} This characterization via base change is more or less implicit in ([Kock 10, remark 7.3.1](#Kock10)) (to translate from the pull-push $(p_2)_\ast p_1^\ast $ shown there, as in ([Deligne 70](#Deligne70)) use that in a [[topos]] the [[epimorphism]] $X \to \Im X$ is [[effective epimorphism|effective]] and then use the [[Beck-Chevalley condition]] to get the push-pull shown above.)

$$
  \left\{
  \array{
    T^\infty X
    &\stackrel{p_1}{\longrightarrow}&
    X
    \\
    \downarrow^{\mathrlap{p_2}} &(pb)& \downarrow^{\mathrlap{i_X}}
    \\
    X &\stackrel{i_X}{\longrightarrow}& \Im X
  }
  \right\}
  \;\;
  \Rightarrow
  \;\;
  ((p_2)_\ast (p_1)^\ast \simeq (i_X)^\ast (i_X)_\ast)
  \,.
$$

$T^\infty X$ is the [[infinitesimal disk bundle]].

## Properties

The [[Eilenberg-Moore category]] of [[coalgebras]] over the jet comonad has the interpretation of the category of [[partial differential equations]] with [[variables]]  in $X$. The [[co-Kleisli category]] of the jet comonad has the interpretation as being the category of bundles over $X$ with [[differential operators]] between them as morphisms ([Marvan 86](#Marvan86), [Marvan 89](#Marvan89)).

## Related concepts

* [[topos of coalgebras over a comonad]]

* in [[Borger's absolute geometry]] a similar base change as above is interpreted as the [[arithmetic jet space]] construction.

## References
 {#References}

In the context of [[differential geometry]] the comonad structure on the jet bundle construction, as well as the interpretation of its EM-category as that of partial differential equations, is due to

* {#Marvan86} [[Michal Marvan]], _A note on the category of partial differential equations_, in _Differential geometry and its applications_, Proceedings of the Conference August 24-30, 1986, Brno ([[MarvanJetComonadPDE.pdf:file]])


> (Proposition 1.4 in [Marvan 86](#Marvan86) needs an extra "weakened transversality" condition on the equalizer, this is fixed in (Theorem 1.3, [Marvan's thesis](#MarvanThesis)). The extra condition is that the equalizer must remain an equalizer after an application of the $V$ functor, which maps fibered manifolds to their vertical tangent bundles.)

* {#MarvanThesis} [[Michal Marvan]], thesis, 1989 ([[MarvanThesis.pdf:file]], [web](http://www.slu.cz/math/cz/lide/marvan-michal/docs/mar89-ocr.pdf))

* {#Marvan89} [[Michal Marvan]], _On the horizontal cohomology with general coefficients_, 1989 ([web announcement](http://old.math.slu.cz/People/MichalMarvan/Annotations/horizontal.php), [web archive](http://dml.cz/dmlcz/701469))

* {#Marvan93} [[Michal Marvan]], section 1.1 of _On Zero-Curvature Representations of Partial Differential Equations_,  (1993) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.5631))

Discussion in [[synthetic differential geometry]]:

* {#Deligne70} [[Pierre Deligne]], _Equations Diff&#233;rentielles &#224; Points Singuliers R&#233;guliers_, 1970

* {#Kock10} [[Anders Kock]], remark 7.3.1 _Synthetic geometry of manifolds_, Cambridge Tracts in Mathematics 180 (2010). ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))


In the context of [[algebraic geometry]] and [[D-geometry]] the comonad structure is observed in:

* {#Lurie} [[Jacob Lurie]], *Notes on crystals and algebraic $\mathcal{D}$-modules* (2010) &lbrack;[[Lurie-NotesOnCrystals.pdf:file]]&rbrack;


Discussion in [[differential cohesion]]:

* [[Igor Khavkine]], [[Urs Schreiber]], _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))

Discussion in differentially cohesive [[modal homotopy type theory|modal]] [[homotopy type theory]]:

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_ (2017)

* [[Felix Cherubini]]: *Synthetic $G$-jet-structures in modal homotopy type theory*, Mathematical Structures in Computer Science (2024) 1–35 &lbrack;[doi:10.1017/S0960129524000355](https://doi.org/10.1017/S0960129524000355), [arXiv:1806.05966]([arXiv:1806.05966](https://arxiv.org/abs/1806.05966)&rbrack;


For more references see at _[[jet bundle]]_.



[[!redirects jet comonads]]

[[!redirects Jet comonad]]
[[!redirects Jet comonads]]