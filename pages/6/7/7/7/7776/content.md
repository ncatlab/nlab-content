[[!redirects affine Serre&#39;s theorem]]
category: algebra, algebraic geometry

## Idea 

A basic result in the study of coherent and quasicoherent modules over spectra (in algebraic geometry), due to [[Jean-Pierre Serre|Serre]], is that for a [[commutative ring]] $R$, [[quasicoherent modules]] (aka quasicoherent sheaves) over the affine spectrum $Spec(R)$ are equivalent to $R$-modules. 

## Statement 

Recall that given a commutative unital ring $R$, there is an adjunction 

$$\widetilde{(-)} \dashv \Gamma\colon \mathcal{O}(Spec\; R)\text{-}Mod \to R\text{-}Mod,$$ 

between the category of modules over its affine spectrum, i.e., the [[local ring]] object $\mathcal{O}(Spec\; R)$ in the category of [[sheaves]] over the [[topological space]] $Spec(R)$, and the category of ordinary [[modules]] over $R$. In the right adjoint direction, for an $\mathcal{O}(Spec\; R)$-module $\mathcal{F}$, we have the [[presheaf]] value $\mathcal{F}(Spec\; R)$, the module of [[global sections]], usually denoted $\Gamma(\mathcal{F})$. In the left adjoint direction, for a (left) $R$-module $M$, we have a sheaf $\tilde{M}$ over $Spec(R)$, whose value $\tilde{M}(D_f)$ at a typical open $D_f$ of $Spec(R)$ is given by the localization $R[f^{-1}]\otimes_R M$, and where the restriction maps are given by canonical maps between these localizations. This gives a sheaf of modules over the sheaf of rings $\mathcal{O}(Spec\; R)$. 

The unit of this adjunction, with components $M \to \Gamma(\tilde{M})$, is the canonical isomorphism $M \cong R \otimes_R M$. The counit, with components $\widetilde{\Gamma(\mathcal{F})} \to \mathcal{F}$, is the presheaf map whose value at a typical open $D_f$ is the canonical map 

$$R[f^{-1}] \otimes_R \mathcal{F}(Spec\; R) \to \mathcal{F}(D_f)$$ 

induced by the restriction map 

$$\mathcal{F}(Spec\; R) \to \mathcal{F}(D_f)$$ 

of $R$-modules (with $R$ acting on the codomain by restriction of scalars along the ring map $R \to R[f^{-1}]$). 

The theorem of Serre is that this adjunction restricts 
to an [[adjoint equivalence]] of categories, which we denote as 

$$\widetilde{(-)} \dashv \Gamma\colon Qcoh(Spec R) \to R\text{-}Mod,$$

between [[quasicoherent sheaf|quasicoherent modules]] over $\mathcal{O}_{Spec R}$, and ordinary $R$-modules. In particular, an $\mathcal{O}_{Spec\; R}$-module $\mathcal{F}$ is quasicoherent if and only if the counit map 

$$\varepsilon_\mathcal{F} \colon \widetilde{\Gamma(\mathcal{F})} \to \mathcal{F}$$ 

is an isomorphism. 

Furthermore, if $R$ is [[Noetherian ring|Noetherian]], the adjoint equivalence restricts further to an equivalence between [[coherent sheaves|coherent modules]] over $\mathcal{O}_{Spec R}$ and finitely generated modules over $R$. 

## References 

The result was given originally by Serre in 

* [[Jean-Pierre Serre]], *Faisceaux Algebriques Coherents*, Ann. Math. 61(2) (1955), 197. &lbrack;[doi:10.2307/1969915](https://doi.org/10.2307/1969915)&rbrack; 

(see paragraphs 48 and 49). It appears in many texts (often without a name, but elsewhere in the nLab it is referred to as the "affine Serre theorem"), for example in 

* [[Robin Hartshorne]], Algebraic Geometry, Graduate Texts in Mathematics volume 52, Springer 1977. &lbrack;[doi.org/10.1007/978-1-4757-3849-0](https://doi.org/10.1007/978-1-4757-3849-0)&rbrack; 

(see Chapter II, Corollary 5.5), and in 

* [[The Stacks Project]] 

[(see Lemma 26.7.5)](https://stacks.math.columbia.edu/tag/01I6).  