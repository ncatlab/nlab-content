## Idea

Projective spectrum Proj assigns a locally ringed space $Proj(A)$ to a graded commutative ring $A$. This construction has been introduced by Serre.

Serre proved two elementary theorems concerning the structure of sheaves of $\mathcal{O}_X$-modules on $X = Proj(A)$ relating graded modules over $A$ and sheaves of $\mathcal{O}_X$-modules: one on [[coherent sheaves]] and another on [[quasicoherent sheaves]]. In both cases, the sheaves correspond to objects in the localization of a category of graded modules by a torsion (Serre's) subcategory.

There is an analogue for affine schemes, (affine) [[affine Serre's theorem|Serre's theorem on quasicoherent sheaves over affine schemes]]. 

## Serre's theorem for quasicoherent sheaves

There is a functor $M\mapsto \tilde{M}$ (to do: should be described here) from the category of graded modules over a $\mathbf{Z}_{\geq 0}$-graded ring $A$ to the category of quasicoherent sheaves of $\mathcal{O}_X$-modules on $X = Proj(A)$ which has a fully faithful right adjoint, hence inducing an equivalence of the category of quasicoherent modules $qcoh(X)$ with a localization of the category of graded $A$-modules. The kernel of that localization is the subcategory of modules of finite length.

## Serre's theorem for coherent sheaves

If $A$ is [[Noetherian ring|Noetherian]], the functor $M\mapsto \tilde{M}$ restricted to the category of finitely generated projective modules takes values in the category of coherent sheaves and the induced functor also has a fully faithful right adjoint, which moreover induces an equivalence between the localization of the category of finitely generated projective $A$-modules by the Serre's subcategory of modules of finite length and the category of coherent sheaves over $Proj(A)$.

## Noncommutative and derived analogues

The subject of noncommutative projective algebraic geometry by Artin and Zhang, as well as independent (and different mainly in the level of generality) attempts to 
noncommutative geometry by other authors take the Serre's
theorem to the status of definition of the category of quasicoherent sheaves when the graded ring is generalized to a noncommutative one. 

## References

### Commutative

This is Section 59, Proposition. 7.8, p. 252 in

* J. P. Serre, Faisceaux algébriques cohérents, Ann. of Math. (2) 61 (2) (1955) 197--278

See also 3.3.5 in

* A. Grothendieck, J. Dieudonné, Eléments de géométrie algébrique II, Inst. Hautes Etudes Sci. Publ. Math. 8 (1961)

Hartshorne proves as Proposition 5.15 that the counit of the corresponding adjunction is an isomorphism (hence we have the reflective subcategory that is localization functor)

* Robin Hartshorne, _Algebraic geometry_, Graduate Texts in Mathematics 52, Springer 1977

See also

* [[The Stacks Project]], [Tag 0BXD](https://stacks.math.columbia.edu/tag/0BXD).

* _Serre's theorem on Proj_, [mathOverflow](https://math.stackexchange.com/questions/333325/serres-theorem-for-operatornameproj)

### Noncommutative

* A. B. Verevkin, _On a noncommutative analogue of the category of coherent sheaves on a projective scheme_, Amer. Math. Soc. Transl. (2) 151 (1992)
* [[Michael Artin]], J. Zhang, _Noncommutative projective schemes_, Adv. Math. 109, 228--287 (1994)
* [[Fred van Oystaeyen]], L. Willaert, _Grothendieck topology, coherent sheaves and Serre’s theorem for schematic algebras_, J. Pure Appl. Alg. 104 (1995) 109--122
* [[Alexander Rosenberg]], _Non-commutative algebraic geometry and representations of quantized algebras_, Mathematics and Its Applications __330__, Kluwer Academic Publishers, 1995
* [[Alexander Polishchuk]], _Noncommutative Proj and coherent algebras_, arXiv:[math.RA/0212182](https://arxiv.org/abs/math/0212182)

> We prove that an abelian category equipped with an ample sequence of objects is equivalent to the quotient of the category of coherent modules over the corresponding algebra by the subcategory of finite-dimensional modules. In the Noetherian case a similar result was proved by Artin and Zhang. 

* Andrés Chacón, Armando Reyes, _Noncommutative scheme theory and the Serre-Artin-Zhang-Verevkin theorem for semi-graded rings_, [arXiv:2301.07815](https://arxiv.org/abs/2301.07815)

category: algebraic geometry

[[!redirects Serre's theorem for Proj]]
[[!redirects projective Serre's theorem]]
[[!redirects Serre's theorem on quasicoherent sheaves]]
