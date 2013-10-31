
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The [[equivariant cohomology|equivariant]] version of [[elliptic cohomology]], the higher [[chromatic homotopy theory|chromatic]] analogue of [[equivariant K-theory]].

## Definition 

Let $G$ be a [[compact Lie group]]. Write $T \hookrightarrow G$ for its [[maximal torus]] and $W$ for its [[Weyl group]].

Let $E \in CRing_\infty$ be an [[elliptic spectrum|elliptic]] [[E-∞ ring]] [[spectrum]] with [[elliptic curve]] $A \to Spec E$. 
Write 

$$
  A_G \coloneqq \left[\left[T,\mathbb{T}\right],A\right]/W
  \;\;
  \in Sch_{/Spec E}
$$

for the [[derived scheme]] formed from the [[character group]] of the [[maximal torus]] mapped into the given [[elliptic curve]].
This is the [[moduli space|moduli scheme]] of [[stable bundle|semistable]] $G$-[[principal bundles]] over the dual elliptic curve $A^\vee$ ([Ginzburg-Kapranov-Vasserot 95, (1.4.5)](#GinzburgKapranovVasserot95)). 
Notice that by the [[Narasimhan?Seshadri theorem]] the similar construction over $Spec \mathbb{C}$ gives equivalently a [[moduli space of flat connections]].


Write $Orb(G)$ for the [[orbit category]] of $G$.
We have a [[full sub-(∞,1)-category]]

$$
  L Top_G
  \hookrightarrow
  PSh_\infty(Orb(G))
$$

of [[topological spaces]] equipped with $G$-[[action]] ($G$-CW complexes).

Let the [[global points]] of the [[elliptic curve]] $A$ over $Spec E$ be equipped with an _orientation_ in the sense of a non-degenerate [[∞-group]] homomorphism of the form

$$
  B U(1) \longrightarrow A(Spec E)
$$


Then there is an [[essential geometric morphism]]

$$
  PSh_\infty(Orb(G))
  \stackrel{\overset{(-)\otimes_G A}{\longrightarrow}}{\stackrel{\overset{}{\leftarrow}}{\underset{}{\longrightarrow}}}
  Sh_\infty(Aff_E)_{/A_G}
$$

from the [[(∞,1)-category]] of $G$-[[actions]] to the [[slice (∞,1)-topos]] over $A_G$. 

([Gepner 05, theorem 3](#Gepner05))

Let 

$$
  \mathcal{O}
  \;\colon\;
  Sh_\infty(Aff_E)
  \longrightarrow
  Aff_E 
  \simeq
  E Alg^{op}
$$ 

be the [[left adjoint]] to the [[(∞,1)-Yoneda embedding]] as discussed at _[[function algebras on ∞-stacks]]_.

Then the composite

$$
  L Top_G
  \hookrightarrow
  PSh_\infty(Orb(G))
   \stackrel{(-)\otimes_G A}{\longrightarrow}
  Sh_\infty(Aff_E)_{/A_G}
  \stackrel{\mathcal{O}}{\longrightarrow}
  E Alg^{op}
$$

takes a space with $G$-[[∞-action]] to its $G$-equivariant elliptic cohomology spectrum.

([Gepner 05, theorem 4](#Gepner05))

## Related concepts

* [[equivariant elliptic genus]]

## References

### General

In

* [[Victor Ginzburg]], [[Mikhail Kapranov]], Eric Vasserot, _Elliptic Algebras and Equivariant Elliptic Cohomology_ ([arXiv:q-alg/9505012](http://arxiv.org/abs/q-alg/9505012))
 {#GinzburgKapranovVasserot95}

a set of axioms was proposed that an equivariant elliptic cohomology theory should satisfy. See also

* Ioanid Rosu, _Equivariant Elliptic Cohomology and Rigidity_, American Journal of Mathematics 123 (2001), 647-677 ([arXiv:math/9912089](http://arxiv.org/abs/math/9912089))

In 

* [[David Gepner]], _[[Homotopy topoi and equivariant elliptic cohomology]]_, PhD thesis, University of Illinois at Urbana-Champaign, 2005.
 {#Gepner05}

the proposal of [Ginzburg-Kapranov-Vasserot 95](#GinzburgKapranovVasserot95) was formalized in terms of [[geometric morphisms]] of [[(infinity,1)-toposes]].

See also

* [[Jacob Lurie]], section 5.1 of _[[A Survey of Elliptic Cohomology]]_
 {#Lurie}


### Relation to loop group representations

That equivariant elliptic cohomology is related to [[representations]] of [[loop groups]] as [[equivariant K-theory]] is related to the [[representation theory]] of the underlying groups had long been conjectured. The idea appears in

* I. Grojnowski, _Delocalised equivariant elliptic cohomology_, in _Elliptic
cohomology_, volume 342 of London Math. Soc. Lecture Note
Ser., pages 114&#8211;121. Cambridge Univ. Press, Cambridge, 2007

took shape in 

* [[Matthew Ando]], _The sigma orientation for analytic circleequivariant
elliptic cohomology_ . Geom. Topol., 7:91&#8211;153,
2003

* [[Matthew Ando]], _Power operations in elliptic cohomology and representations of loop groups_ Transactions of the American
Mathematical Society 352, 2000, pp. 5619-5666.

and was then further refined in section 5.2 of ([Lurie](#Lurie)) and in ([Gepner 05](#Gepner05)).


More is in 

* [[Nora Ganter]], _The elliptic Weyl character formula_ ([arXiv:1206.0528](http://arxiv.org/abs/1206.0528))
 {#Ganter12}

### Relation to superstrings and the Witten genus

Relation to the [[Witten genus]] [[partition function]] of [[superstrings]] is discussed in

* [[Matthew Ando]], Maria Basterra, _The Witten genus and equivariant elliptic cohomology_ ([arXiv:math/0008192](http://arxiv.org/abs/math/0008192))

[[!redirects equivariant elliptic cohomology theory]]
[[!redirects equivariant elliptic cohomology theories]]